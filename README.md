# API Gateway - Puerta de Entrada

Este servicio enruta las peticiones hacia los microservicios `UserService` y `ProductService`.

## 🧩 Funcionalidades

- Reenvío de peticiones a servicios internos
- Validación y propagación de token JWT
- Endpoint unificado: `http://localhost:5022`

## 🔁 Rutas disponibles

| Ruta               | Descripción                       |
|--------------------|-----------------------------------|
| POST /auth/register | Registro de usuario (UserService)|
| POST /auth/login    | Login de usuario (UserService)   |
| GET /products       | Listar productos (ProductService)|
| POST /products      | Crear producto + AI (ProductService)|
| PUT /products/{id}  | Editar producto (ProductService) |

## ⚙️ Tecnologías

- C# con .NET 8
- HttpClientFactory para proxy
- Validación de tokens en headers

## 🧪 Cómo probar

1. Ejecutar: `dotnet run`
2. Usar Swagger: `http://localhost:5022/swagger/index.html`
3. Todas las peticiones se redirigen internamente

## 🔐 Seguridad

- Se requiere JWT válido en las rutas protegidas
- El Gateway no almacena datos, solo enruta
