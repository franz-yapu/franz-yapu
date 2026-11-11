<h1 align="center">Franz Yapu</h1>
<p align="center"><b>Desarrollador Full Stack</b> · TypeScript de punta a punta · Desarrollo asistido por IA<br>
El Alto, Bolivia · Disponible para trabajo remoto · Inglés B1–B2</p>
<p align="center">
  <a href="https://franz-yapu.github.io">Portafolio</a> ·
  <a href="https://www.linkedin.com/in/franz-jhonny-yapu-mamani-bab89018a">LinkedIn</a>
</p>

Más de 7 años construyendo y operando plataformas web, los últimos 6 en remoto para una empresa con sede
en Panamá. Más de 30 proyectos web en producción, usados en Latinoamérica, Europa, África y Medio Oriente,
con interfaz multiidioma (incluida de derecha a izquierda) y funcionamiento offline-first donde la
conectividad es parcial. Cubro el ciclo completo: análisis, modelado de datos, frontend, backend,
despliegue y los servidores donde corre todo.

En el último año me especialicé en **desarrollo asistido por IA**: la IA acelera la generación y el cuello
de botella pasa a ser la validación, que es donde pongo el trabajo.

---

## Proyectos propios (código público)

> El código de mi experiencia profesional está en repositorios privados de la organización.
> Estos son proyectos míos, abiertos para que se puedan revisar.

### [VentaFácil](https://github.com/franz-yapu/ventafacil) · punto de venta offline-first y multi-negocio
POS para negocios con varias sucursales e internet intermitente: el vendedor sigue vendiendo sin conexión y
todo se sincroniza al volver la red.
- Ventas guardadas en el dispositivo (IndexedDB) con identificadores generados en el cliente, sin duplicados al sincronizar.
- Multi-negocio con aislamiento por **Row-Level Security**; la API se conecta con un rol sin privilegios para que las políticas se apliquen.
- Dos mundos de tokens con secretos distintos, límites de intentos y bitácora de auditoría.
- Pruebas contra un PostgreSQL real, sin mocks, y CI en GitHub Actions.

`React` `Vite` `Fastify` `Drizzle` `PostgreSQL` `Dexie` `PWA` `Zod`

### Subastas de café en vivo · [API](https://github.com/franz-yapu/subastas-cafe-api) y [Web](https://github.com/franz-yapu/subastas-cafe-web)
Subastas en línea con pujas en tiempo real, cierre automático y avisos por correo.
- **Sin doble adjudicación:** *advisory lock* de PostgreSQL por lote, verificado con una prueba de concurrencia contra base real.
- **Una sola subasta activa** garantizada por un índice único parcial en la base de datos.
- Cierre programado con **anti-sniping** configurable.
- Angular 19 con **SSR**, multiidioma, marca blanca con contraste WCAG calculado automáticamente y editor de traducciones.

`NestJS` `Prisma` `PostgreSQL` `Socket.io` `Angular 19` `SSR` `PrimeNG` `Tailwind`

### [JobRadar](https://github.com/franz-yapu/jobradar) · radar de ofertas con IA
n8n recolecta vacantes, un agente con Claude las evalúa contra un perfil y un panel muestra el veredicto.
- Arquitectura hexagonal con un puerto de IA agnóstico de proveedor y evaluaciones automatizadas con promptfoo.
- Cola de evaluación en AWS (SQS, Lambda, IAM) provisionada con Terraform.
- Cada llamada a la IA registra tokens, latencia y costo, con tope de gasto diario por cuenta; Grafana para observarlo.
- Pruebas E2E con Playwright y CI.

`NestJS` `React 19` `Claude` `n8n` `SQS` `Terraform` `Playwright`

### [SISET](https://github.com/franz-yapu/siset-esfm) · gestión y seguimiento de trámites
Sistema para digitalizar hojas de ruta y seguimiento de expedientes.
- Monolito modular con decisiones registradas en **ADR** y desarrollo con especificación previa.
- Auditoría de todas las escrituras, OpenAPI y E2E con Playwright para seis roles.
- CI con typecheck, lint, pruebas, build y auditoría de dependencias.

`Node` `Express 5` `Prisma` `PostgreSQL` `React` `Docker` `Nginx`

---

## Stack

| | |
| --- | --- |
| **Frontend** | Angular v9 a v19 (NGRX, RxJS, PrimeNG) · React 18/19 · Next.js · TanStack Query · Tailwind · PWA · SSR |
| **Backend** | Node.js · Fastify · NestJS · Express · Prisma · Drizzle · Socket.io · BullMQ · JWT y passkeys · Casbin |
| **Datos** | PostgreSQL · MySQL · Redis · Row-Level Security |
| **Móvil** | Flutter (módulos en dos apps en producción) · Ionic · Android |
| **Calidad** | Vitest · Playwright · Testing Library · axe-core · Storybook · GitHub Actions |
| **Infraestructura** | Linux · Docker · Coolify · Nginx · PM2 · PgBouncer · AWS (SQS, Lambda) con Terraform · Sentry · OpenTelemetry · Grafana |
| **IA** | Claude Code · SDK de Anthropic (agentes con herramientas tipadas) · MCP · skills propias · promptfoo · Langfuse · n8n |

## Cómo trabajo con IA

- **Herramientas:** Claude Code a diario, con skills propias, plantillas de prompts y traspaso de contexto entre sesiones.
  Servidores MCP que conectan a los agentes con sistemas reales para que trabajen con hechos y no con suposiciones.
- **En producto:** agentes multipaso con herramientas tipadas, OCR y transcripción, con una política que elimina datos personales antes de que salgan del sistema.
- **Validación:** el código y la documentación generados se verifican contra el repositorio real antes de integrarse.
- **Transferencia:** documenté el flujo y formé a personal nuevo del equipo.

## Contacto

[LinkedIn](https://www.linkedin.com/in/franz-jhonny-yapu-mamani-bab89018a) · [Portafolio](https://franz-yapu.github.io)
