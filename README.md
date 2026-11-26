# Mi Primer Sintetizador · Max/MSP

**Unidad 1 · Interfaces Sonoras · Entrega 3** · Taller de Diseño de Interfaces, Universidad Adolfo Ibáñez · 2026
Autores: Luis-Felipe Benitez y Martín Donoso · Ficha: https://portafolio.insta3d.cl/sintetizador/

## Objetivos
- Construir un sintetizador sustractivo controlable en tiempo real.
- Diseñar su interfaz de uso en **Presentation Mode**, separada del parche de programación.
- Incorporar un reproductor de samples y visualizadores de la señal.

## Descripción
Un instrumento digital donde se ve y se oye la cadena completa del sonido: generar (oscilador y ruido), esculpir (filtro), dar forma en el tiempo (envolvente) y escuchar. La interfaz en Presentation Mode deja a la vista solo los controles necesarios para tocar.
**Público y contexto:** estudiantes que aprenden síntesis de sonido; se usa en un computador con Max/MSP y audífonos o parlantes.

## Tecnologías
Max/MSP (Cycling '74). Objetos principales: `cycle~`, `noise~`, `biquad~`, `line~`, `*~`, `dac~`, `sfplay~`, `scope~`, `spectroscope~`.

## Cómo ejecutarlo
1. Instala Max (la versión gratuita permite abrir y tocar parches).
2. Abre `mi-primer-sintetizador.maxpat`.
3. Crea una carpeta `audio/` junto al parche con un archivo `audio.mp3` para el reproductor de samples.
4. Activa el audio (DSP) y usa los controles en Presentation Mode.

## Flujo de la señal
```
[cycle~] + [noise~] → [biquad~ filtro] → [line~ · *~ envolvente] → [dac~]
[sfplay~ samples] ─────────────────────────────────────────────→ [dac~]
[scope~ · spectroscope~] ← visualización
```

## Proceso
> 📌 **Por aportar:** capturas del parche en modo Edición y en Presentation Mode, y notas de las pruebas (carpeta `proceso/`).

## Video demostrativo
> 📌 **Por aportar:** video tocando el sintetizador, subido a YouTube y enlazado aquí.
