---
name: video-production
description: Plan, create, revise, or deliver a video project from a brief, script, footage, images, or an existing edit. Use for narrative films, social videos, explainers, product videos, documentaries, motion graphics, and AI-generated video; route to the project's existing tools and review the actual rendered result. Do not use for general video-tool questions that do not ask to make or change a video.
---

# Video Production

Guide a video project from its current state to the result the user asked for. This is a production director skill, not a renderer or a fixed template. Work with the user's chosen creative direction and tools; choose only the stages needed for this request.

## Start from the actual project

1. Read the applicable `AGENTS.md`, project brief, current edit or shot data, and status notes. Identify existing assets, approved decisions, unfinished work, and the active editing or generation project. Preserve prior user decisions and do not treat rejected drafts as approved source material.
2. Establish the requested outcome and current stage: new video, script or shot revision, asset creation, generation, edit, review, or export. Continue from that stage when the user says “continue” or equivalent; do not restart completed work.
3. Resolve only choices that change the work: audience and purpose, platform and aspect ratio, target duration, language, creative constraints, delivery format, tool or cost limits, and whether the user wants collaborative checkpoints or autonomous execution. Infer from available project evidence when reliable. Ask only for material missing information that cannot be safely inferred.
4. Inspect the existing project stack before choosing software. Do not replace an established editor, model, or workflow just because another tool is available. For unfamiliar tools, formats, model versions, licenses, or materially changed workflows, check current authoritative documentation and a relevant working example before implementation.

For a simple requested edit or a well-defined continuation, make the change directly. For a new, multi-stage, high-cost, or technically uncertain production, make a concise brief and production plan first. Reuse suitable current research; record new research only when it changes the tool or production decision. Do not pause at routine implementation details after the user has authorized the work.

## Plan the story and the images

Use or preserve the existing script. If a script is needed, define its central promise or dramatic question, audience, tone, and ending before polishing lines. Choose a structure appropriate to the project: narrative, documentary, explainer, promotion, social short, music-led, or another form. Do not force a single hook/problem/proof/CTA formula on every video. For factual work, distinguish sourced fact, interpretation, and invention; never invent evidence, product behavior, numbers, or quotations.

Break the script or brief into scenes and shots before building the final sequence. A shot plan should be as detailed as the production needs, and usually records:

- shot/scene ID, story beat, purpose, and target duration;
- visible subject and the action or change the audience will see;
- framing, camera intent, composition, and start/end state;
- relevant continuity: people, appearance, screen direction, place, props, light, and time;
- dialogue, narration, on-screen words, music or sound cues, and transition intent;
- source asset or generation method, status, and review notes.

Keep one principal action per generated shot when that improves control. Plan preparation, action, consequence, and a readable hold; do not make characters rush merely to fit a prompt. Use an animatic or a few representative frames when pacing, continuity, or sequence structure is uncertain. Make each scene advance story, information, mood, or action. Text, icons, zooms, blur, and transitions should support the image rather than substitute for meaningful visual events.

Create only the continuity guide the project needs: character or subject identity, age/state changes, wardrobe, locations, props, palette, lighting direction, typography, and screen direction. For a factual or period project, check claims and visual references against appropriate sources. Choose generated lettering or editable text according to visual intent, spelling accuracy, localization, and later editing needs. Inspect generated text character by character; preserve user-approved lettering and use a separate layer when exact wording needs reliable revision.

For multi-session or multi-shot work, maintain a small project record using the existing format: active brief/script versions, shot IDs and durations, asset provenance and usage terms, approved/candidate/rejected takes, edit references, and the next action. Keep original and derived media traceable; record crop/mask coordinates, transparency, and resolution when extracting reusable elements from generated images. Create files only for information the project actually needs.

## Choose the production method

Select the lightest method that can meet the visual goal, using the project's installed tools and skill instructions:

- use existing footage when it carries the needed event or evidence;
- use generated images, video, audio, animation, or local models when they serve the brief and fit the user's cost, privacy, and quality limits;
- use a code-based timeline or motion graphics when deterministic timing, typography, data, or repeatable layout matters;
- use the project's NLE or composition framework for the main edit when one is already established.

Treat tools and models as replaceable adapters. Do not assume a subscription includes API access, that an API is free, that an account can be connected to a local tool, or that a model can run on the current machine. Before external generation, uploads, paid calls, downloads, installation, or long local jobs, check the user's authorization, cost/privacy constraints, queue, and resource impact. Do not interrupt another user's process or occupied GPU job. If capacity or authorization is missing, prepare reviewable inputs and state what is pending.

For a new visual style, generation model, or expensive batch, first make a small representative test. Change one meaningful variable at a time and keep seeds, references, and other settings fixed when comparing alternatives. Preserve source files, versions, prompts, seeds, model/workflow settings, and output mapping where reproducibility or later repair matters. Do not claim a generated shot passed because it encoded successfully.

When writing generative-shot prompts or preparing local-model jobs, read [references/generative-shots.md](references/generative-shots.md). Keep the cinematic shot record separate from model-specific input syntax and parameters.

## Produce in reviewable units

Create or revise one scene, short sequence, or representative shot at a time when quality is uncertain. Put each candidate back into its neighboring context early; check the cut, not just isolated attractive frames. Preserve approved assets and keep rejected or experimental outputs clearly marked outside the final edit.

For AI-generated or composited shots, inspect the actual sequence for identity consistency, anatomy, action clarity, contact with props, spatial depth, lighting motivation, unwanted motion, text artifacts, and continuity. Use first/middle/last frames plus additional frames around movement or transitions; a single poster frame is not sufficient. For motion graphics or code-rendered sequences, preview timing and motion in the target renderer. Use the exact relevant project skill before modifying a specialized framework.

Iterate on the weakest responsible layer: script/beat, blocking, source image, motion prompt, generation settings, edit timing, transition, sound, or color. Preserve successful layers and avoid changing many variables together. Human visual and audio review decides whether a shot is useful; automated checks support but do not replace that review.

Bound generation by the user's time/cost budget and a small candidate batch. If the same failure persists, revise the responsible input or method before spending more on retries. On OOM, persistent overheating, or loss of required monitoring, stop new submissions and investigate; cancel only work this task owns when necessary. Record observed resource measurements and missing telemetry. Do not claim hardware safety from an idle snapshot or invented universal temperature/memory limits.

## Edit, finish, and verify

As shots become usable, assemble them into the intended timeline and check rhythm, shot order, geography, eyelines, action handoffs, repeated information, and transitions. Use transitions that have a story, movement, shape, light, or sound motivation. Do not add effects merely to disguise a weak shot. Design sound and music with the picture, keep dialogue intelligible, and respect silence and holds. Add captions and on-screen copy for the target platform and verify spelling, reading time, safe areas, and contrast.

Before delivery:

1. Use available playback and audio tools to review the full cut and mix; inspect problem sections frame by frame. If the agent can only inspect samples or cannot listen, report that limit and request human review for the unverified dimensions. Do not label sampled frame inspection as full-speed playback or waveform analysis as listening.
2. Confirm the brief, script, approved decisions, and required scenes are represented. Check visual and narrative continuity, readable text, captions, sound levels, and transition quality.
3. Verify the exported file's path, duration, dimensions, frame rate, audio streams, and full decode with suitable tools. Check that the output is playable in the intended viewer.
4. Report what was actually rendered and reviewed, where it is, which checks passed, and any limitations. Provide a clickable absolute local media link or supported inline preview; use a verified remote URL for remote deliverables. Separate a plan, candidate, preview, and approved final. Do not overstate resolution, frame interpolation, motion quality, or resource safety based on metadata alone.

## Use specialized skills when relevant

Read only the specialized skill needed for the current production operation. Examples include scriptwriting for script craft, image-generation for image assets, HyperFrames or Remotion skills for their respective compositions, and audio/media skills for their supported tasks. Follow the project's own `AGENTS.md` and specialized skill contracts. This skill does not override user instructions, project rules, factual-source requirements, tool permissions, or the renderer's technical requirements.
