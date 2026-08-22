# Duck Lab

**Duck Lab** es una estación de trabajo de audio digital en el navegador. Permite organizar pistas, controlar volumen, panorama, solo, silencio y armado de grabación; gestionar el transporte; explorar una biblioteca de activos y exportar mezclas WAV mediante Web Audio API.

## Estado de la versión

| Área | Estado verificado |
|---|---|
| Linter | Correcto |
| TypeScript estricto | Correcto |
| Compilación de producción | Correcta |
| Auditoría de dependencias de producción | Sin vulnerabilidades reportadas |
| Biblioteca de activos | 3.013 metadatos generados |

## Requisitos

Se requiere **Node.js 20 o superior** y `pnpm`. La aplicación ya no requiere Bun para ejecutarse.

## Inicio rápido

```bash
pnpm install --frozen-lockfile
pnpm run dev
```

La interfaz estará disponible en `http://localhost:3000`.

## Validación y producción

```bash
pnpm run check
pnpm run build
pnpm run start
```

El comando `check` ejecuta ESLint y el chequeo estricto de TypeScript. El comando `build` genera una salida independiente de Next.js y `start` la sirve con Node.js.

## Flujo de uso

La sesión comienza con una única pista llamada **Faixa 1**. Añada pistas con el botón `+`; seleccione una pista por su nombre; use los controles de volumen, panorama, mute, solo y armado según sea necesario. Al reproducir o grabar, el motor de audio se crea a partir de la interacción del usuario, que es el comportamiento requerido por los navegadores modernos. La grabación solicita permiso de micrófono solo cuando existe al menos una pista armada.

Abra **Biblioteca de Sons** para buscar y filtrar activos por texto, categoría o género. El catálogo es de metadatos generados para explorar el flujo de interfaz; no incluye archivos de audio empaquetados ni previsualizaciones descargables. El botón **Exportar WAV** necesita que el motor de audio se haya iniciado durante la sesión.

## Límites conocidos

Duck Lab es una base de DAW web en evolución. La reproducción de clips importados, la incorporación de activos de la biblioteca como buffers reales, las pruebas automatizadas de interacción y la persistencia remota de proyectos no forman parte de esta versión. El informe `AUDIT_REPORT.md` documenta el alcance de la revisión y las mejoras aplicadas.

## Licencia

No se incluyó una licencia en el material de origen. Añada una antes de distribuir el repositorio públicamente.
