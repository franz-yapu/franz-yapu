# Franz Yapu

**Ingeniero Full Stack** · El Alto, Bolivia · Remoto

Siete años construyendo y operando plataformas web de punta a punta: TypeScript desde la base de datos
hasta la interfaz, y los servidores Linux donde corren. Desde hace un año trabajo con agentes de IA
y reviso lo que producen: la IA acelera la generación, y el cuello de botella pasa a ser la validación.

[Portafolio](https://franz-yapu.github.io) · [LinkedIn](https://www.linkedin.com/in/franz-jhonny-yapu-mamani-bab89018a)

---

## Proyectos

### [VentaFácil](https://github.com/franz-yapu/ventafacil) — punto de venta offline-first y multi-negocio
POS para negocios medianos con varias sucursales e internet intermitente. El vendedor sigue vendiendo sin
conexión y todo se sincroniza al volver la red.

- Ventas guardadas en el dispositivo (IndexedDB) con identificadores generados en el cliente, sin duplicados al sincronizar.
- Multi-negocio con aislamiento por **Row-Level Security** en PostgreSQL; la API se conecta con un rol sin privilegios para que las políticas se apliquen.
- Dos mundos de tokens (negocio y plataforma) con secretos distintos, límites de intentos y bitácora de auditoría.
- Pruebas contra un PostgreSQL real (no mocks) y CI en GitHub Actions.

`React` `Vite` `Fastify` `Drizzle` `PostgreSQL` `Dexie` `PWA` `Zod`

### Plataforma de subastas de café en vivo — [API](https://github.com/franz-yapu/subastas-cafe-api) · [Web](https://github.com/franz-yapu/subastas-cafe-web)
Subastas en línea con pujas en tiempo real, cierre automático y notificaciones por correo.

- **Sin doble adjudicación:** las pujas al mismo lote se serializan con un *advisory lock* de PostgreSQL, y una prueba de concurrencia contra base real lo verifica.
- **Una sola subasta activa**, garantizada por un índice único parcial en la base de datos, no solo en la aplicación.
- Cierre programado en el servidor con **anti-sniping** configurable (extiende el cierre si hay pujas al final).
- Web en Angular 19 con **SSR**, multiidioma (español/inglés), marca blanca con contraste WCAG calculado automáticamente y editor de traducciones.

`NestJS` `Prisma` `PostgreSQL` `Socket.io` `Angular 19 SSR` `PrimeNG` `Tailwind`

### [JobRadar](https://github.com/franz-yapu/jobradar) — radar de ofertas con IA
n8n recolecta ofertas, un agente con Claude (tool use) las puntúa contra un perfil de candidato y un panel muestra el veredicto y borradores de respuesta.

- Arquitectura hexagonal en NestJS, con puerto de IA intercambiable (Claude, OpenAI, Gemini) y evaluaciones con promptfoo.
- Cola de puntuación en AWS (SQS + Lambda) aprovisionada con Terraform.
- Cada llamada a la IA queda registrada con tokens, latencia y coste, con **tope de gasto diario** por cuenta.
- Observabilidad en Grafana, pruebas E2E con Playwright y CI.

`NestJS` `React 19` `Claude` `n8n` `SQS` `Terraform` `Playwright`

---

## Stack

| | |
| --- | --- |
| **Frontend** | TypeScript · Angular (v9 a v19) · React · Tailwind · PWA · SSR |
| **Backend** | Node.js · NestJS · Fastify · Prisma · Drizzle · WebSockets |
| **Datos** | PostgreSQL · Row-Level Security |
| **Infraestructura** | Linux · Docker · Coolify · GitHub Actions · Terraform · AWS |
| **IA** | Claude Code, MCP y Claude SDK en producto, con validación automatizada de lo que generan los agentes |

## Contacto

[LinkedIn](https://www.linkedin.com/in/franz-jhonny-yapu-mamani-bab89018a) · [Portafolio](https://franz-yapu.github.io)
