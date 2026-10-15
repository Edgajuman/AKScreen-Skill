# Focused workflows

## Grade a clip

Inspect the active sequence, find the requested clip by name and timing, then
discover `effects.*` commands and their parameter docs. Apply or update the
requested effect on that clip. Preserve existing effects unless replacement was
requested. Inspect its values and preview the relevant frame.

## Motion graphics

Discover the current `graphics.*`, `motion.*` and `camera.*` commands. Create text
or shapes with supported engine commands. Confirm font availability before
choosing a family. For generated movement, use a small bounded duration; repeated
layers and sampled animation can increase project size. Render a preview after
the meaningful composition changes.

## Captions

Discover `captions.*`, inspect the target track and confirm caption timing.
Use the track style for family, size and appearance. Preserve caption text and
language unless asked to change them. Automatic transcription requires the
user's optional model; do not download it silently.

## Export

Discover export parameter docs and output presets in this build. Confirm the
destination path from the request. `command_run` sends `file.exportMedia` as a
background job. Keep its returned job ID; poll `jobs.list` at reasonable intervals
until finished. A failed or interrupted render is not a delivered file.

## Reconnection

Check that the editor is the intended project/session. The MCP launch mode uses
a private session token; another unrelated editor on the same port cannot be
controlled with it. Never expose the bridge on a public IP. After a lost edit
reply, inspect the timeline/effect state before repeating that edit.
