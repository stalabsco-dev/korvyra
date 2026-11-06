# Arquitectura propuesta
PWA mobile-first con frontend separado del backend. El backend se aloja en servicios cloud administrados; el usuario no administra una VM.

## Stack provisional
- TypeScript, React y Vite.
- PWA: manifest y service worker.
- Backend: Cloudflare Workers.
- Base de datos: Cloudflare D1.
- KV y Cron Triggers cuando sean apropiados.
- GitHub privado.

Verificar planes, cuotas y términos vigentes antes de desplegar.

## Componentes
1. Aplicación web: panel, configuración y alertas.
2. API: autenticación y gestión de fuentes.
3. Motor de monitoreo: webhooks oficiales y tareas programadas permitidas.
4. Adaptadores separados por proveedor.
5. Base de datos: usuarios, fuentes, eventos y notificaciones.
6. Entrega: bandeja interna y Web Push.

## Principios
Separación de integraciones, validación en servidor, límites por usuario/proveedor, idempotencia, reintentos limitados y registros sin secretos. No usar scraping no autorizado.

“Gratis” no significa ilimitado. No activar facturación por uso sin aprobación expresa.
