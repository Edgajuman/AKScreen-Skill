# AK Screen Editing · Skill

Instrucciones para editar proyectos de **AK Screen** con un agente compatible
con skills y [AK Screen MCP](https://github.com/Edgajuman/AKScreen-MCP).

El MCP aporta las herramientas reales. La skill guía al agente para descubrir
comandos, utilizar los IDs del proyecto abierto, conservar el trabajo, revisar
el resultado y exportar sin repetir operaciones por error.

## Instalar

- **Claude Code:** copia `skills/akscreen-editing/` a
  `~/.claude/skills/akscreen-editing/` o a `.claude/skills/akscreen-editing/`
  dentro del proyecto donde la quieras usar.
- **Codex:** copia la carpeta a `~/.codex/skills/akscreen-editing/`.
- **Otros clientes:** importa la carpeta si admiten el formato `SKILL.md`.

Configura también el servidor MCP siguiendo su README. Una skill por sí sola
no ejecuta herramientas ni proporciona acceso al editor.

**Requiere el editor con el nuevo puente autenticado.** El instalador 2.4.0 del
12 de octubre de 2026 todavía no lo incluye. No cambia ni instala esa aplicación.

## Ejemplos

> Usa AK Screen para recortar este proyecto y hacer una copia de 30 segundos.

> Añade un título con mi fuente, anima su entrada y comprueba la vista previa.

> Crea un gráfico animado de ventas, conserva mis clips y exporta un MP4.

Los ejemplos dependen de los comandos disponibles en la compilación conectada;
el agente debe consultarlos, no inventarlos. Las instrucciones y referencias
están en [SKILL.md](skills/akscreen-editing/SKILL.md).

MIT · @edgajuman.
