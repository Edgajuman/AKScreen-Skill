# AK Screen Editing · Skill

Instrucciones para editar proyectos de **AK Screen** con un agente compatible
con skills y [AK Screen MCP](https://github.com/Edgajuman/AKScreen-MCP).

**Compatible con AK Screen 3.0 y versiones posteriores.**

[**Descargar AK Screen**](https://github.com/Edgajuman/AKScreen-Downloads/releases)
· [Repositorio de descargas](https://github.com/Edgajuman/AKScreen-Downloads)
· [Configurar el MCP](https://github.com/Edgajuman/AKScreen-MCP)

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

Instala AK Screen 3.0 o posterior y configura el MCP para utilizar el ejecutable
de esa versión.

## Ejemplos

> Usa AK Screen para recortar este proyecto y hacer una copia de 30 segundos.

> Añade un título con mi fuente, anima su entrada y comprueba la vista previa.

> Crea un gráfico animado de ventas, conserva mis clips y exporta un MP4.

Los ejemplos utilizan los comandos disponibles en la versión conectada;
el agente debe consultarlos, no inventarlos. Las instrucciones y referencias
están en [SKILL.md](skills/akscreen-editing/SKILL.md).

MIT · @edgajuman.
