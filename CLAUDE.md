# validacion-tickets — contexto para Claude

Repo **heredado**. El lector de QR de MG Eventos se movió a
**https://mgeventos.co/lector** (repo `mg-eventos`, carpeta `lector/`), porque
la sesión del lector se guarda por dominio y en github.io no veía el token.

Hoy el repo solo tiene `index.html`, que redirige a
`https://mgeventos.co/lector/?lector=1`. Los archivos viejos del lector
(`lector.js`, `lector.css`, `config.js` y `vendor/`) se borraron el 24/10/2026
(auditoría de seguridad, B3): el repo es público y seguían publicados con una
URL vieja de la API. Quedan en el historial de Git (pasos 4 y 11 de la
auditoría: validar con sesión LEER_QR y librería local + CSP estricta).

- Los cambios al lector se hacen en `mg-eventos/lector/`, no aquí.
- El backend es `ticketera-apps-script`; su `CLAUDE.md` tiene el contexto
  completo.
- Pendiente X7 del Plan de auditoría: migrar el lector a `qr-scanner` y
  soportar pistolas Bluetooth (se hace en `mg-eventos/lector/`).
- Trazabilidad (regla de Mauricio, 23/10/2026): todo cambio se documenta en el
  `CLAUDE.md` del repo y en el Plan de auditoría (Google Sheet
  `1YnAFnOSULsJO4Ieg8fyX3opJRYzmvcshfinGDyAgmts`).
