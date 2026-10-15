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

## Tracking, stabilization and audio animation

Discover `tracking.analyze`, `tracking.inspect`, `tracking.apply`, `audio.reactive`
and `audio.spectrum`. Resolve source and target clip IDs first. Tracking regions
use source-image pixels, not preview-window coordinates. Choose a textured
object and start before the last frame. Tracking may stop at cuts or occlusion;
report that failure instead of applying an invented trajectory.

Analyses are asynchronous jobs. Keep the returned job ID, poll `jobs.list`, and
avoid editing the sequence while analysis runs: the editor rejects stale results.
Use `jobs.cancel` for cancellation. Inspect generated keyframes and preview the
start, middle and end after successful completion. Bands become editable vector
layers; reactive animation uses an audio-track clip or the timeline mix.

Discover `physics.emitter`, `camera.target` and `motion.blur` for particles,
targeted cameras and temporal sampling. Match emitter coordinates to the sequence
dimensions. Particles are deterministic 2D physics; they do not simulate 3D rigid
bodies. Motion blur increases render cost, so use bounded samples and a short
preview before an export. Character transforms are graphic text-layer properties;
discover current property IDs before setting ranges or animation progress.

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
