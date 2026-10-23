# Generative shots

Read when preparing image/video assets, motion prompts, or local-model generation. Adapt to the documented capabilities of the selected model; this is a shot contract, not universal model syntax.

## Prepare a shot packet

Use the project's existing record format. Include the shot ID and narrative purpose; source/reference asset versions; framing and camera intent; start state; main action with preparation, action, consequence and settle/hold; end state and next-shot handoff; continuity locks; sound intent; and the specific failure conditions to inspect.

Separate these three inputs:

- **Asset description:** identity, appearance, clothing or materials, scene geometry, light and style. Make image assets with enough framing margin and resolution for intended camera movement or extraction. Use stable references for recurring subjects. A cutout or layered element must have usable edges, contact shadows where appropriate, and sufficient off-frame extent to avoid severed limbs or props during motion.
- **Motion direction:** what changes in the shot, its direction, extent, pace and result. In I2V, let the reference carry visible identity/composition; avoid redescribing it in ways that conflict. Keep camera intent distinct from subject movement. Use temporal beats when supported; do not assume prose timestamps create exact keyframes.
- **Execution settings:** model and checkpoint/version, conditioning mode, resolution, frame count/rate, steps, sampler/scheduler, seed, precision/offload, and workflow version. Record only applicable fields; do not invent parameter equivalence between models.

For a new image, inspect identity, anatomy, wardrobe/materials, composition, light, any text, and downstream animation feasibility before generation. Start/end frames or pose/control references can help when the model supports them; a storyboard is useful for planning even when the generator consumes only one image or plain text.

## Prompt structure

Translate the shot packet into concise model-supported language:

> [Reference/initial state]. [Main visible action, direction and extent]. [Pace and settle/hold]. [One clear camera intention]. [Relevant environmental response and motivated lighting]. [Critical continuity constraints].

Select detail by risk. For a hand-object shot, describe contact and limited travel; for a running shot, describe trajectory and body mechanics. For a practical lamp, relate light changes to distance, direction and nearby surfaces rather than applying global exposure flicker. Describe foreground/midground/background and occlusion when depth matters. Use negative prompts only if supported, targeting observed defects rather than accumulating generic bans.

## Generate and compare

Check official workflow/model compatibility, required files and installed versions before running. Probe service/queue state and available memory, disk and relevant telemetry. On a shared device, defer GPU submissions while another workload occupies it unless sharing is explicitly authorized and feasible. Preserve other jobs and append only this task's jobs to the appropriate queue.

Choose a short test that still contains the complete intended action. Very short, low-resolution or heavily distilled tests can change the action and perceived quality; label them as feasibility tests rather than substitutes for the final configuration. Use one job/batch first when resource requirements are unmeasured. Do not invent a memory or temperature threshold; use applicable device guidance, existing controls and observed measurements.

For A/B work, record the hypothesis and one changed factor; retain the raw outputs and exact settings. Compare identity, action completion, anatomy/contact, camera behavior, local light, detail and usable edit range. Keep failed tests out of production selections.

After choosing a useful take, preserve its raw file and first/last usable frames, place it beside neighboring shots, and check continuity. Apply denoise, stabilization, grading, super resolution or interpolation only where needed, comparing the result to the source for loss of texture, ghosts, invented detail and broken motion. Changing export FPS does not create new motion, and a larger raster does not prove native detail. Retain the approved source and record each derivative.
