# reimagine

[Português](README.md) · [English](README.en.md) · **Español**

**Una skill que hace que tu agente de IA rediseñe el proceso a partir del objetivo, en lugar de parchear los pasos.**

Pulir pasos da un 10%. Reimaginar da 10 veces más, porque cambia la estructura que obliga a que esos pasos existan.

Tú dices el resultado que quieres, idealmente uno absurdo ("quiero este video listo en 5 minutos, no en 2 horas"). El agente lee tus archivos y el historial, encuentra de dónde viene el ir y venir y te entrega un sistema nuevo. No cambia nada antes de tu OK.

## Por qué funciona un objetivo absurdo

"20 minutos" invita al agente a ajustar lo que ya existe. "5 minutos" lo obliga a borrar, juntar y reordenar. La meta absurda es una herramienta: prohíbe el parche. Si la meta es realmente imposible, la skill lo dice con honestidad y muestra hasta dónde se puede llegar, y por qué camino.

Pide el **resultado**, no las etapas. Quien describe etapas describe el sistema que ya tiene, y el agente solo lo va a reacomodar.

## Qué hace

1. **Fija el objetivo y la meta** en una línea. Si no das meta, crea una y te avisa: tiempo dividido entre 10, una ronda de correcciones, como máximo 2 paradas tuyas.
2. **Mide la realidad antes de opinar.** Lee los archivos, el historial de Git, las conversaciones anteriores y las versiones viejas, y cuenta: cuántas rondas, cuánto se rehízo, dónde se va el tiempo. El hallazgo más común es "está escrito, pero nada lo verifica".
3. **Encuentra las causas de fondo.** Reglas que nacen solo en la revisión, fuentes que se contradicen, lo caro antes que lo barato, una pieza haciendo 4 trabajos, candado sobre candado, lo mismo hecho dos veces, todo hecho desde cero cada vez.
4. **Corta en el orden correcto.** Cuestiona cada exigencia (y averigua por qué existe antes de cortarla), borra, simplifica, pone lo barato antes de lo caro y solo después automatiza.
5. **Diseña el sistema nuevo:** una frase-tesis, una sola fuente de verdad, una tarea por pieza, piezas aprobadas en lugar de trabajo nuevo, cada rechazo convertido en una verificación automática, la lista de lo que sale y una meta medible.
6. **Hace un pre-mortem:** las 3 formas más probables en que el diseño nuevo falle.
7. **Entrega y espera:** la estructura en tabla, árbol o boceto, lo que no se verificó y una única decisión para ti.

Sirve para procesos y líneas de producción, pantallas y paneles, bots y agentes de IA, y estructuras de carpetas. No sirve para arreglar un error conocido ni para un ajuste pequeño de texto.

## Instalación

**Claude Code:** en la caja de mensajes, escribe:

```
/plugin marketplace add vibe-gifts/reimagine
/plugin install reimagine@reimagine
```

En la app de Claude (pestaña Code), haz clic en **+** junto a la caja de mensajes, luego en **Plugins** y **Añadir marketplace**. Escribe `vibe-gifts/reimagine` y haz clic en **Añadir plugin**.

**Codex u otro agente:** descarga este repositorio (botón **Code** → **Download ZIP**), descomprímelo y apunta el agente a la carpeta `skills/reimagine`.

Después, solo pide:

> reimagina cómo publicamos los posts del blog. Hoy tarda 3 días y va y viene demasiado. Objetivo: post publicado en 1 hora, aprobado a la primera.

## Bueno saber

- **Solo propone.** Nada en tu proyecto cambia antes de tu OK.
- Responde en tu idioma.
- La carpeta `skills/reimagine/evals` tiene 3 casos de prueba en el formato de `claude plugin eval`.

## Licencia

MIT
