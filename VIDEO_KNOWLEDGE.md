# VIDEO_KNOWLEDGE — reference library for VIDEO DIRECTOR AI
Silent reference. Use it to write better scenarios and prompts. Never paste this file to the user; quote only the parts that are needed.

---

## 1. STYLE LIBRARY (for Step 6 and STYLE LOCK)
Each entry = what to show the user (short) + the English STYLE LOCK core to expand.

| # | Style | STYLE LOCK core (English) | Best for |
|---|---|---|---|
| 1 | Cinematic realistic | photorealistic cinematic film still, 35mm lens, shallow depth of field, natural skin texture, soft film grain, teal-and-orange grade | drama, stories, ads |
| 2 | Documentary | handheld documentary footage, natural available light, 24mm lens, realistic imperfections, muted colors | history, social topics, education |
| 3 | 3D animated film | high-end 3D animated feature film style, soft global illumination, expressive stylized characters, rich saturated colors, subsurface skin | kids, family, fairy tales |
| 4 | 2D cartoon | clean 2D cartoon animation, bold outlines, flat bright colors, simple shapes, smooth cel shading | kids, humor, explainers |
| 5 | Anime | Japanese anime style, cel-shaded, detailed painted backgrounds, dramatic lighting, expressive eyes | youth, emotion, action |
| 6 | Claymation | stop-motion claymation, handmade plasticine textures, visible fingerprints, miniature set, warm practical lights | humor, kids, ads |
| 7 | Watercolor storybook | hand-painted watercolor illustration, soft bleeding edges, paper texture, pastel palette, gentle light | fairy tales, poems, lullabies |
| 8 | Vintage film | 1970s 16mm film look, warm faded colors, heavy grain, light leaks, slight gate weave | nostalgia, memories, music |
| 9 | Film noir | black-and-white film noir, high-contrast hard light, deep shadows, venetian-blind light patterns, rain-wet streets | mystery, crime, suspense |
| 10 | Epic fantasy | epic fantasy cinematic, volumetric god rays, grand scale, mist, rich golden and deep blue palette | legends, myths, history |
| 11 | Cyberpunk neon | cyberpunk night city, neon magenta and cyan lights, rain reflections, holographic signs without readable text | sci-fi, tech, future |
| 12 | Miniature diorama | tilt-shift miniature diorama, tiny detailed models, shallow focus, bright toy-like colors | explainers, cities, processes |
| 13 | Historical epic | historically accurate period drama, practical costumes, candle and daylight, earthy desaturated palette | history channels, biographies |
| 14 | Cozy stylized 3D | cozy stylized 3D, rounded shapes, warm rim light, playful proportions | kids education |
| 15 | Paper cut-out | layered paper cut-out animation, visible paper edges, soft drop shadows, craft textures | explainers, kids |
| 16 | Low-poly | low-poly 3D, faceted geometry, gradient sky, clean minimal palette | tech, games, explainers |
| 17 | Ink wash / oriental miniature | traditional ink wash painting, flowing brush strokes, muted earth tones, rice-paper texture | poetry, Eastern history, legends |
| 18 | Comic book | comic book style, halftone dots, bold inks, dynamic angles, saturated primaries | action, humor |
| 19 | Horror atmospheric | dark atmospheric horror, cold desaturated palette, low-key lighting, fog, unsettling stillness | mystery, horror stories |
| 20 | Commercial product | clean premium commercial look, studio softbox lighting, glossy reflections, seamless background | ads, product videos |

Pairing tips: kids/education → 3, 4, 7, 12, 15. History → 2, 10, 13, 17. Drama/life stories → 1, 8. Ads → 1, 20, 6. Mystery → 9, 19.

A good STYLE LOCK line contains: style + medium, color palette, lighting, lens/camera, texture/grain, aspect ratio. Example:
`STYLE LOCK: photorealistic cinematic film, warm amber and deep teal palette, soft golden-hour side light, 35mm lens, shallow depth of field, subtle film grain, 9:16 vertical`

---

## 2. CAMERA VOCABULARY
Shot sizes: extreme wide shot (EWS), wide shot (WS), full shot, medium shot (MS), medium close-up (MCU), close-up (CU), extreme close-up (ECU), over-the-shoulder (OTS), point-of-view (POV), insert shot.
Angles: eye level, low angle (power), high angle (weakness), bird's-eye / top-down, Dutch angle (unease), worm's-eye.
Movements: static locked-off, slow push-in (emotion, realization), pull-back / dolly-out (reveal, loneliness), pan left/right, tilt up/down, tracking / follow shot, orbit / arc around subject, crane up (ending, scale), handheld (urgency, realism), slow motion.
Lenses: 14–24mm wide (space, distortion), 35mm (natural storytelling), 50mm (neutral human eye), 85mm (portrait, soft background), macro (details).
Rules:
- ONE camera move per 8-second clip. Two fast moves in one clip = chaos.
- Slow moves look more cinematic in AI video than fast ones.
- For dialogue: MCU or CU, static or very slow push-in.
- End each clip with the camera settled (no motion in the last ~0.5 s) so the last frame is sharp.

---

## 3. LIGHT, COLOR AND MOOD
| Mood | Light | Palette |
|---|---|---|
| Hope, warmth | golden hour, soft side light | amber, honey, soft green |
| Sadness | overcast, window light, low contrast | blue-grey, desaturated |
| Tension | low-key, hard single source, deep shadows | cold teal, black |
| Mystery | fog, backlight, silhouettes | deep blue, violet |
| Joy, kids | bright even daylight | saturated primaries, pastel |
| Nostalgia | warm practical lamps, haze | sepia, faded orange |
| Epic | volumetric god rays, backlit dust | gold, deep blue |
Keep time of day and light direction identical inside one location across chained clips.

---

## 4. AUDIO AND SPEECH (Veo / Flow)
- Veo generates speech, SFX, ambience and music together with the video.
- Speech format inside the video prompt:
  `[AZIZ] (tired, gentle, speaking Uzbek): "Onajon, men qaytdim."`
  Always state the language explicitly: "speaking Uzbek" / "speaking Russian" / "speaking English".
- Word limits per clip (natural pace, leave ~1 s silence at the end):
  8 s → ~20 English words / ~16 Russian or Uzbek words.
  10 s → ~25 English / ~20 Russian or Uzbek.
  If the line is longer, split it across two clips.
- Only ONE character speaks per clip whenever possible. Two speakers in 8 s often mixes up lips.
- Uzbek speech: generators may mispronounce or drift into another accent. Offer the user:
  a) try in-video speech, check it, regenerate if bad; or
  b) Audio mode B: generate video with ambience/music only, and record the narration separately (own voice or a TTS tool), then add in the editor. This is the most reliable.
- Voice-over (mode B) text is written separately per scene, labelled `🎙 NARRATION (Xs):`, in the chosen language, with the same word limits.
- Always add "no subtitles, no captions, no on-screen text" — Veo sometimes burns subtitles into the frame when there is dialogue.
- Audio line structure: `Audio: [ambience], [2–3 specific SFX with timing], [music: genre + mood + intensity], no background dialogue.`
- Keep the same music mood across chained clips, otherwise the edit sounds cut.

---

## 5. STORY STRUCTURES BY LENGTH
Hook formulas (first 3 seconds): an unexpected image; a question; a conflict already in progress; a striking contrast; a "what happens next" moment; a strong emotion on a face in close-up.

30 s (4 clips of 8 s):
1 Hook — 2 Problem/setup — 3 Turn — 4 Payoff + final image.

60 s (8 clips):
1 Hook — 2 Setup/world — 3 Character goal — 4 Obstacle — 5 Escalation — 6 Lowest point / turn — 7 Resolution — 8 Final image + message/CTA.

2–3 min (15–23 clips) — three acts:
Act 1 (25%): hook, world, character, inciting event.
Act 2 (50%): attempts, obstacles, midpoint twist, escalation, darkest moment.
Act 3 (25%): decision, climax, resolution, closing image mirroring the opening.

By goal:
- Story/drama: emotion first; show, don't tell; one clear protagonist.
- Education/explainer: question → simple example → visual metaphor → key fact → recap. One idea per clip.
- Ad: problem → pain → product as solution → result → CTA. Never show real brand logos; use the user's own product description.
- Motivation: struggle → failure → persistence → small win → big message.
- Humor: setup → expectation → twist; keep the punchline in its own clip.
- History: place + date hook → context → key event → consequence → reflection. Keep costumes and architecture period-accurate.

---

## 6. CONTINUITY RULES (the heart of the chaining method)
- 🔗 CONTINUE clip = image-to-video from the previous clip's LAST frame. The first line of its prompt must describe that frame exactly as it is in the screenshot (position, pose, light, camera), not as originally planned.
- 🎬 NEW SHOT = new location, time jump, or a big change of angle. It gets a fresh image prompt; the character sheet must be attached as a reference.
- After 3–4 chained clips the quality drifts (faces soften, colors shift). Insert a NEW SHOT (cutaway, close-up, different angle) to reset.
- 180° rule: in a dialogue keep the camera on one side of the line between characters; A always looks right, B always looks left.
- Screen direction: if a character walks left→right, keep that direction in the next clips unless there is a deliberate turn.
- Keep clothing, props, hair, injuries, weather and time of day identical unless the story changes them — and if it does, update the Bible and say so.
- Character tags: always refer to people as [NAME] with the full bible description. Never write "the man" in one clip and "a young guy" in the next.
- Emotions change gradually between clips (neutral → worried → scared), not jump.
- The end frame of every clip: character's face visible, no motion blur, no fade, no dissolve, no cut.

---

## 7. SCREENSHOT ANALYSIS CHECKLIST (Step 9)
Check in this order:
1. Composition: shot size, camera angle, where each character is in the frame.
2. Characters: face matches bible? hair, clothes, colors, signature detail present?
3. Environment and light: same location details, time of day, light direction?
4. Defects: extra/missing fingers, melted hands, distorted faces, duplicated people, floating objects, garbled text or subtitles, watermarks, heavy blur.
5. Story position: did the clip reach the planned beat or stop earlier/later?
Verdict:
- ✅ Everything matches → continue from this frame.
- ⚠️ Small drift (slightly different shirt shade, minor background change) → continue; add corrective phrases in the next prompt ("his jacket is dark green wool, same as before").
- ❌ Broken (face changed, wrong character, extra limbs in focus, text in frame) → do not chain from it. Recommend regenerating the previous clip; give a corrected prompt with the problem addressed explicitly.
- If the frame is fine but the story stopped early, adjust the next clip's action to cover the missing part and shorten later beats.

---

## 8. COMMON PROBLEMS AND FIXES
| Problem | Fix phrase / action |
|---|---|
| Subtitles or text appear | add "no subtitles, no captions, no text, no letters anywhere in the frame"; keep dialogue shorter |
| Face changes between clips | paste full character description; attach character sheet; reset with NEW SHOT; use close-ups less often after long chains |
| Too much motion / chaos | "slow, deliberate movement", one action, "camera slowly pushes in" |
| Nothing happens | give a concrete verb with timing: "at 3s she opens the door and steps outside" |
| Extra fingers / broken hands | hide hands or keep them still; avoid holding small objects; "anatomically correct hands" |
| Lip sync off | fewer words, one speaker, MCU framing, "clear lip movements matching speech" |
| Wrong accent/language | "speaking fluent Uzbek with a natural Uzbek accent"; or switch to voice-over mode |
| Color shift across clips | repeat STYLE LOCK verbatim; mention light direction and time of day |
| Camera spins/zooms randomly | "static camera" or one named move with speed: "slow 2-second push-in" |
| Ending is blurry | "the final second holds still, sharp, stable composition" |
| Crowds look melted | reduce to 2–3 people in focus, crowd blurred in the background |

---

## 9. PROMPT EXAMPLES

### Scene 1 — image prompt (first frame)
```
Vertical 9:16 frame. Medium close-up of [DILNOZA], a 9-year-old Uzbek girl with two long black braids tied with red ribbons, round face, big dark brown eyes, wearing a white school blouse and a navy-blue pinafore, small silver star pendant. She sits at a wooden desk by a window in a modest village classroom, holding a pencil, looking at a blank notebook with a worried face. Morning sunlight from the left window, dust particles in the air.
STYLE LOCK: high-end 3D animated feature film style, soft global illumination, warm honey and soft green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical.
Avoid: text, letters, subtitles, watermark, logos, extra fingers, distorted face.
```

### Scene 1 — video prompt
```
[Scene 1/8 — 8s]
Start frame: [DILNOZA] at her desk by the window, pencil in hand, looking worried at a blank notebook.
Style: high-end 3D animated feature film style, soft global illumination, warm honey and soft green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical.
Characters: [DILNOZA] — 9-year-old Uzbek girl, two long black braids with red ribbons, round face, big dark brown eyes, white school blouse, navy-blue pinafore, small silver star pendant.
Action: 0–3s she taps the pencil on the notebook and sighs / 3–6s she looks up at the window as a small yellow butterfly lands on the glass / 6–8s her face slowly lights up with a curious smile; she holds still.
Camera: static medium close-up, very slow push-in toward her face.
Speech: [DILNOZA] (quiet, curious, speaking Uzbek): "Sen qayerdan kelding?"
Audio: quiet classroom ambience, distant birds, soft pencil taps, gentle piano with light strings, hopeful mood.
End frame: [DILNOZA] smiling at the butterfly on the window, face clearly visible, sharp, still.
Avoid: subtitles, captions, on-screen text, watermark, logos, extra fingers, face morphing, flicker.
```

### Scene 2 — continuation after screenshot (🔗 CONTINUE)
```
[Scene 2/8 — 8s]
Start frame: exactly as in the provided image — [DILNOZA] in medium close-up, smiling at a yellow butterfly on the left window glass, morning light from the left.
Style: (STYLE LOCK verbatim)
Characters: (bible text verbatim)
Action: 0–3s the butterfly lifts off the glass and flies toward her desk / 3–6s it lands on her open notebook; she gasps softly / 6–8s the pencil lines on the page begin to glow faintly gold; she holds still, amazed.
Camera: slow tilt down from her face to the notebook, then settles.
Audio: soft wing flutter, a gentle magical chime at 6s, music builds slightly.
End frame: close view of the glowing notebook with the butterfly on it, her hands resting still beside it, sharp and stable.
Avoid: (AVOID list)
```

---

## 10. CHARACTER SHEET PROMPT TEMPLATE
```
Character reference sheet, [STYLE LOCK core], plain light-grey background, even studio lighting.
[NAME]: full description. Shown in three views side by side: front view, three-quarter view, side profile, full body, neutral pose, neutral expression. Consistent proportions and colors across all views.
No text, no labels, no watermark.
```
For 2–3 characters: either one sheet with all of them standing side by side (front view), or one sheet per character (better consistency).

---

## 11. PLATFORM NOTES
- Google Flow: Text to Video, Frames to Video (start image → clip; optional end image), Ingredients to Video (reference images of characters/objects), Extend (continues from the last frame automatically). If the user prefers Extend over screenshots, still use the same video-prompt structure but drop the "Start frame" line.
- Gemini app: upload the start image and paste the video prompt; clips are up to 8 s.
- Kling and similar: usually 5 or 10 s; can use start and end frames.
- Screenshots: pause at the very end (on YouTube-style players use the "." key to step frame by frame if available), hide player controls, crop out UI. A downloaded video opened in a player and paused at the end gives the cleanest frame.
- Aspect ratio of the image must match the video ratio.

---

## 12. FINAL PACKAGE TEMPLATES
Editing guide (chosen language):
1. Import clips in order 1…N.
2. For each 🔗 clip trim the first ~0.2–0.5 s (duplicate of the previous last frame) to avoid a visible freeze.
3. Transitions: straight cuts inside a scene; short cross-dissolve only on time jumps.
4. Audio: normalize dialogue, add one music track under all clips at low volume if the generated music is inconsistent; add narration (mode B).
5. Subtitles: auto-captions in the chosen language, check spelling manually.
6. Export: 1080×1920 for 9:16, 1920×1080 for 16:9, 30 fps.

Titles: 3 variants — curiosity, emotion, benefit. Description: 2–3 lines + a question to viewers. Hashtags: 10, mix of broad and niche, in the chosen language.
Thumbnail prompt: the most emotional moment, one face in close-up, strong contrast, clean space for the user to add their own title text later (do not render text in the image).
