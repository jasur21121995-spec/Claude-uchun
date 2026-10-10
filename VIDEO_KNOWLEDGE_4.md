# VIDEO_KNOWLEDGE — reference library for VIDEO DIRECTOR AI
Silent reference. Use it to write better scenarios and prompts. Never paste this file to the user; quote only the parts that are needed.

---

## 1. STYLE LIBRARY (for S5 and the STYLE LOCK)
Each entry = the name shown to the user + the English STYLE LOCK core to expand. In S5, pick the 8–12 that suit the video, renumber them (names in the chosen language) and add a last option "Own style".

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
- Word limits per clip (about 2 words per second in Uzbek/Russian, 2.5 in English, leaving ~1 s of silence):
  8 s → 14 Uzbek/Russian words or 17 English words.
  10 s → 18 Uzbek/Russian or 22 English.
  If the line is longer, split it across two clips. For children, use fewer words.
- Mark when speech starts: `SPEECH (from 3s): …`, so it does not collide with the key action. An off-screen speaker is allowed: `[BOBO] (off-screen, warm, speaking Uzbek): "…"`.
- Only ONE character speaks per clip whenever possible. Two speakers in 8 s often mix up the lips.
- Sound 2 or 3: write `SPEECH: none, no one speaks` and add "no background dialogue" to AUDIO; otherwise the model may still invent voices and moving mouths.
- Uzbek speech: generators may mispronounce or drift into another accent. Offer the user:
  a) try in-video speech, check it, regenerate if bad; or
  b) Sound 2: generate video with ambience/music only (SPEECH: none), record the narration separately (own voice or a TTS tool) and add it in the editor. This is the most reliable.
- Sound 2 narration is sent as its own numbered code block 🎙 NARRATION: line k is read over clip k, in the chosen language, with the same word limits.
- Always add "no subtitles, no captions, no on-screen text" — Veo sometimes burns subtitles into the frame when there is dialogue.
- Audio line structure: `Audio: [ambience], [2–3 specific SFX with timing], [music: genre + mood + intensity], no background dialogue.`
- Keep the same music mood across chained clips, otherwise the edit sounds cut.

---

## 5. STORY STRUCTURES BY LENGTH
Hook formulas (first 3 seconds): an unexpected image; a question; a conflict already in progress; a striking contrast; a "what happens next" moment; a strong emotion on a face in close-up.

30 s (4 clips of 8 s):
1 Hook — 2 Problem/setup — 3 Turn — 4 Payoff + final image.

60 s with 10 s clips (6 clips):
1 Hook — 2 Setup/goal — 3 Obstacle — 4 Turn — 5 Resolution — 6 Final image + message/CTA.

60 s with 8 s clips (8 clips):
1 Hook — 2 Setup/world — 3 Character goal — 4 Obstacle — 5 Escalation — 6 Lowest point / turn — 7 Resolution — 8 Final image + message/CTA.

2–3 min (15–23 clips) — three acts:
Act 1 (25%): hook, world, character, inciting event.
Act 2 (50%): attempts, obstacles, midpoint twist, escalation, darkest moment.
Act 3 (25%): decision, climax, resolution, closing image mirroring the opening.
Example 2 min = 15 clips: Act 1 = clips 1–4, Act 2 = clips 5–11 (midpoint twist at 8), Act 3 = clips 12–15.

By goal:
- Story/drama: emotion first; show, don't tell; one clear protagonist.
- Education/explainer: question → simple example → visual metaphor → key fact → recap. One idea per clip.
- Ad: problem → pain → product as solution → result → CTA. Never show real brand logos; use the user's own product description.
- Motivation: struggle → failure → persistence → small win → big message.
- Humor: setup → expectation → twist; keep the punchline in its own clip.
- History: place + date hook → context → key event → consequence → reflection. Keep costumes and architecture period-accurate.

---

## 6. THE KEYFRAME CHAIN (the heart of batch mode)
Goal: N image prompts + N video prompts, where every video ends exactly where the next one begins.

How to plan (do this in your head before writing any prompt):
1. Take the approved Scene Map (N rows).
2. Write the keyframe chain K1 … KN: Kk = the exact state at the START of clip k = the SCENE text of image k. Also decide the END of the last clip = the final image of the film.
3. For every 🔗 link, check that going from Kk to K(k+1) takes ONE main action and ONE gentle camera move, doable in L seconds. "One main action" = one simple movement toward the END state; small reactions, speech and background motion don't count. Multi-step work (digging, planting, cooking) is split over several clips. If it doesn't fit, split the beat or change the link to ✂️.
4. Plan the camera path across the chain: if clip k pushes in to a close-up, K(k+1) IS a close-up. Alternate push-in / pull-back / static / tilt, so the camera does not drift into extreme close-ups.
5. Only then write image prompts (SCENE = Kk) and video prompts (START = Kk, END = K(k+1) for 🔗).

What a SCENE text must contain (≤45 words, so image k+1 and the END of video k are the same picture):
- shot size + angle ("Medium close-up at eye level")
- the place in short ("in the classroom", "on the school yard path"), so a clip after a ✂️ is clear even without the image
- every visible character by [NAME] and position in the frame (left / center / right = SCREEN side; foreground / background)
- pose, where they look, facial expression
- what they hold, and in which hand: hands are always the character's OWN ("in his own left hand"). Careful: a character facing the camera on screen-left has their own right hand on screen-left.
- key props and their position
- light direction + time of day
Write it as 1–3 plain sentences. No camera movement words inside SCENE (it is a still frame). Movement is described as a frozen moment: "mid-stride", "reaching toward", "ripples spreading around the float".
- Props that are in view stay mentioned in every SCENE until the story removes them; don't let them vanish and reappear.

Link types:
- 🔗 continuous: same location, same moment. END(k) = SCENE(k+1) copied word for word. Best joins; use it by default.
- ✂️ cut: a new angle, a new place or a time jump. END(k) is clip k's own final moment (it may end mid-motion; the cut carries the movement on). Clip k+1 must follow logically:
  • match on action: clip k ends as she pushes the door; clip k+1 starts outside as the door swings open and she steps out;
  • bridge: clip k ends looking at the setting sun; clip k+1 starts on the same sky, now at night;
  • reaction: clip k ends on a sound or a call; clip k+1 starts on the person turning toward it.
  Never an unexplained jump (a different outfit, a missing prop, a new place without a bridge).
- Never more than 5 clips in a row without a ✂️: a cut refreshes the image quality and keeps the edit dynamic.
- Every END (also before a ✂️ and in the last clip) is ≤45 words and written like a SCENE.

Continuity rules for the whole chain:
- The same clothes, hair, props and injuries in every prompt unless the story changes them (then update the Bible and mention it). Props may change state when the action shows it (grain → flour → dough), but the object itself stays the same.
- Characters should already be in the start image. Anyone who enters mid-clip gets their full Bible text in CHARACTERS.
- 180° rule in dialogues: A always looks screen-right, B always screen-left.
- Screen direction: a character walking left→right keeps that direction unless the story turns them.
- Light and time of day stay constant inside one location.
- Emotions change gradually between clips (calm → worried → scared), not in jumps.
- The music mood is described the same way in every clip between two ✂️ (a sequence).
- The last frame of every clip is sharp and clear: no fade, no dissolve, no motion blur.

Length budget (keeps prompts inside generator limits and chat message limits):
- STYLE LOCK ≤25 words · each character ≤25 words · each location ≤20 words · each prop ≤15 words · SCENE ≤45 words
- image prompt ≤150 words (≈1,000 characters) · video prompt ≤300 words (≈2,000 characters)

Self-check before sending a list:
□ count = N, numbering 1…N, one paragraph per prompt, one empty line between prompts
□ START(k) = SCENE(k) word for word
□ for every 🔗: END(k) = SCENE(k+1) word for word
□ each ✂️ has a clear next-moment logic
□ every prompt has the full STYLE LOCK and full character text (no "same as above"); length budget kept
□ speech lines within limits and in the chosen language

---

## 7. /check — IMAGE AND SCREENSHOT ANALYSIS
The user may send a generated image or a screenshot of a clip's last frame. Check in this order:
1. Composition: shot size, angle, where each character is.
2. Characters: face, hair, clothes, colors and signature detail match the Bible?
3. Environment and light: the same location details, time of day, light direction?
4. Defects: extra or missing fingers, melted hands, distorted faces, duplicated people, floating objects, text or subtitles, watermarks, heavy blur.
5. Chain: does the image match SCENE(k)? Does the end of the clip match SCENE(k+1)?
Verdict:
- ✅ matches → keep all prompts.
- ⚠️ small drift → keep the image; add corrective phrases to video k and image k+1 ("his jacket is dark green wool, as before").
- ❌ broken → regenerate: give a corrected image prompt k (and video k) that names the problem explicitly.
If the real image differs from the plan but is usable, rewrite START of video k to describe the real image, and keep END unchanged, so the chain still holds.

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
| Ending is blurry | "the last frame is sharp and clear, stable composition, no motion blur" |
| Crowds look melted | reduce to 2–3 people in focus, crowd blurred in the background |

---

## 9. FULL CHAIN EXAMPLE (4 clips, 3D animated, 9:16, Uzbek, Sound 1)
Shorter than a real film, but the format is exactly what the user receives. In a real chat all headings are in the chosen language.

📘 BIBLE
- STYLE LOCK: high-end 3D animated film style, soft global illumination, warm honey and green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical
- [DILNOZA]: 9-year-old Uzbek girl, round face, dark brown eyes, two long black braids with red ribbons, white school blouse, navy-blue pinafore dress, small silver star pendant
- L1 CLASSROOM: village classroom, wooden desks, green chalkboard, tall white-framed window on the left with a geranium, open wooden door back right
- L2 SCHOOL YARD: sunny school yard, dusty path, tall poplars on both sides, low white-washed school building behind
- PROPS: P1 small yellow butterfly; P2 open school notebook, blank page; P3 yellow wooden pencil; P4 glowing golden paper butterfly (from clip 3)
- AVOID: text, letters, watermark, logos, extra fingers, distorted face

SCENE MAP
| # | time | what happens | line | link |
|---|---|---|---|---|
| 1 | 0:00–0:08 | Dilnoza notices a butterfly on the window | [DILNOZA]: "Sen qayerdan kelding?" | 🔗 |
| 2 | 0:08–0:16 | The butterfly lands on her notebook, lines glow | [DILNOZA]: "Voy, chizig'im yonyapti!" | 🔗 |
| 3 | 0:16–0:24 | The glowing drawing flies out through the door | [DILNOZA]: "To'xta! Qayoqqa ketyapsan?" | ✂️ |
| 4 | 0:24–0:32 | In the yard she runs after the paper butterfly | [DILNOZA]: "Meni qayerga boshlayapsan?" | 🏁 |

🖼 IMAGE PROMPTS
```
1. Vertical 9:16 frame. SCENE: Medium close-up at eye level in the classroom. [DILNOZA] sits at her desk by the left window, pencil in her right hand, looking down worried at a blank open notebook; a small yellow butterfly rests on the window glass; soft morning sun from the left. CHARACTERS: [DILNOZA]: 9-year-old Uzbek girl, round face, dark brown eyes, two long black braids with red ribbons, white school blouse, navy-blue pinafore dress, small silver star pendant. LOCATION: village classroom, wooden desks, green chalkboard, tall white-framed window on the left with a geranium, open wooden door back right. STYLE: high-end 3D animated film style, soft global illumination, warm honey and green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical. AVOID: text, letters, watermark, logos, extra fingers, distorted face.

2. Vertical 9:16 frame. SCENE: Medium close-up at eye level in the classroom. [DILNOZA] sits at her desk, turned left toward the window, smiling curiously at the small yellow butterfly on the glass; pencil in her right hand; blank notebook open on the desk; soft morning sun from the left. CHARACTERS: [DILNOZA]: 9-year-old Uzbek girl, round face, dark brown eyes, two long black braids with red ribbons, white school blouse, navy-blue pinafore dress, small silver star pendant. LOCATION: village classroom, wooden desks, green chalkboard, tall white-framed window on the left with a geranium, open wooden door back right. STYLE: high-end 3D animated film style, soft global illumination, warm honey and green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical. AVOID: text, letters, watermark, logos, extra fingers, distorted face.

3. Vertical 9:16 frame. SCENE: High-angle close-up of the open notebook on the classroom desk. The small yellow butterfly sits mid-page on faint glowing golden lines shaped like a butterfly; [DILNOZA]'s hands rest on both sides, pencil in her right hand; soft morning sun from the left. CHARACTERS: [DILNOZA]: 9-year-old Uzbek girl, round face, dark brown eyes, two long black braids with red ribbons, white school blouse, navy-blue pinafore dress, small silver star pendant. LOCATION: village classroom, wooden desks, green chalkboard, tall white-framed window on the left with a geranium, open wooden door back right. STYLE: high-end 3D animated film style, soft global illumination, warm honey and green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical. AVOID: text, letters, watermark, logos, extra fingers, distorted face.

4. Vertical 9:16 frame. SCENE: Wide shot at eye level on the school yard path. A glowing golden paper butterfly flutters out of the school door toward the camera; [DILNOZA] runs out after it, laughing, pencil in her right hand; poplars on both sides; bright morning sun from the left. CHARACTERS: [DILNOZA]: 9-year-old Uzbek girl, round face, dark brown eyes, two long black braids with red ribbons, white school blouse, navy-blue pinafore dress, small silver star pendant. LOCATION: sunny school yard, dusty path, tall poplars on both sides, low white-washed school building behind. STYLE: high-end 3D animated film style, soft global illumination, warm honey and green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical. AVOID: text, letters, watermark, logos, extra fingers, distorted face.
```

🎥 VIDEO PROMPTS
```
1. [Clip 1/4, 8 s] START: Medium close-up at eye level in the classroom. [DILNOZA] sits at her desk by the left window, pencil in her right hand, looking down worried at a blank open notebook; a small yellow butterfly rests on the window glass; soft morning sun from the left. ACTION: 0–3s she taps the pencil on the empty page and sighs; 3–6s a soft flutter makes her lift her head and turn left; 6–8s she sees the butterfly and a curious smile slowly appears. CAMERA: static, very slow push-in, settling on the same medium close-up. SPEECH (from 5s): [DILNOZA] (quiet, curious, speaking Uzbek): "Sen qayerdan kelding?" AUDIO: quiet classroom ambience, distant birds, soft pencil taps, gentle piano with light strings, hopeful mood. END: Medium close-up at eye level in the classroom. [DILNOZA] sits at her desk, turned left toward the window, smiling curiously at the small yellow butterfly on the glass; pencil in her right hand; blank notebook open on the desk; soft morning sun from the left. STYLE: high-end 3D animated film style, soft global illumination, warm honey and green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical. CHARACTERS: [DILNOZA]: 9-year-old Uzbek girl, round face, dark brown eyes, two long black braids with red ribbons, white school blouse, navy-blue pinafore dress, small silver star pendant. AVOID: text, letters, watermark, logos, extra fingers, distorted face, subtitles, captions, on-screen text, face morphing, flicker; the last frame is sharp, no fade, no motion blur.

2. [Clip 2/4, 8 s] START: Medium close-up at eye level in the classroom. [DILNOZA] sits at her desk, turned left toward the window, smiling curiously at the small yellow butterfly on the glass; pencil in her right hand; blank notebook open on the desk; soft morning sun from the left. ACTION: 0–3s the butterfly lifts off the glass and flies to the desk; 3–6s it lands mid-page and she gasps softly, placing both hands beside the notebook; 6–8s faint golden lines shaped like a butterfly begin to glow under it. CAMERA: slow tilt down from her face to the notebook, ending on a high-angle close-up of the page. SPEECH (from 4s): [DILNOZA] (whispering, amazed, speaking Uzbek): "Voy, chizig'im yonyapti!" AUDIO: soft wing flutter, a gentle magical chime at 6s, the same gentle piano with light strings, slowly building. END: High-angle close-up of the open notebook on the classroom desk. The small yellow butterfly sits mid-page on faint glowing golden lines shaped like a butterfly; [DILNOZA]'s hands rest on both sides, pencil in her right hand; soft morning sun from the left. STYLE: high-end 3D animated film style, soft global illumination, warm honey and green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical. CHARACTERS: [DILNOZA]: 9-year-old Uzbek girl, round face, dark brown eyes, two long black braids with red ribbons, white school blouse, navy-blue pinafore dress, small silver star pendant. AVOID: text, letters, watermark, logos, extra fingers, distorted face, subtitles, captions, on-screen text, face morphing, flicker; the last frame is sharp, no fade, no motion blur.

3. [Clip 3/4, 8 s] START: High-angle close-up of the open notebook on the classroom desk. The small yellow butterfly sits mid-page on faint glowing golden lines shaped like a butterfly; [DILNOZA]'s hands rest on both sides, pencil in her right hand; soft morning sun from the left. ACTION: 0–3s the glowing lines peel off the page and fold into a golden paper butterfly; 3–6s it rises and flies toward the open door at the back right; 6–8s [DILNOZA] stands up behind her desk, amazed, watching it fly out. CAMERA: slow tilt up and pull back to a medium shot at eye level. SPEECH (from 5s): [DILNOZA] (surprised, calling out, speaking Uzbek): "To'xta! Qayoqqa ketyapsan?" AUDIO: paper rustle, a rising magical shimmer, a chair scraping at 6s, the same gentle piano with light strings, now faster. END: Medium shot at eye level in the classroom. [DILNOZA] stands behind her desk, pencil in her right hand, amazed, watching a glowing golden paper butterfly fly out through the open door at the back right; soft morning sun from the left. STYLE: high-end 3D animated film style, soft global illumination, warm honey and green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical. CHARACTERS: [DILNOZA]: 9-year-old Uzbek girl, round face, dark brown eyes, two long black braids with red ribbons, white school blouse, navy-blue pinafore dress, small silver star pendant. AVOID: text, letters, watermark, logos, extra fingers, distorted face, subtitles, captions, on-screen text, face morphing, flicker; the last frame is sharp, no fade, no motion blur.

4. [Clip 4/4, 8 s] START: Wide shot at eye level on the school yard path. A glowing golden paper butterfly flutters out of the school door toward the camera; [DILNOZA] runs out after it, laughing, pencil in her right hand; poplars on both sides; bright morning sun from the left. ACTION: 0–3s she runs along the path after the butterfly; 3–6s she slows down and stretches out her open left hand; 6–8s the paper butterfly hovers just above her palm and she stops, smiling up at it. CAMERA: slow tracking backward in front of her, stopping on a stable wide shot. SPEECH (from 5s): [DILNOZA] (breathless, happy, speaking Uzbek): "Meni qayerga boshlayapsan?" AUDIO: footsteps on dust, birds, leaves in the wind, the same piano with strings reaching a warm final chord. END: Wide shot at eye level on the school yard path. [DILNOZA] stands still, smiling, looking up at the golden paper butterfly hovering above her open left palm; poplars on both sides; bright morning sun from the left. STYLE: high-end 3D animated film style, soft global illumination, warm honey and green palette, gentle morning side light, 35mm lens, shallow depth of field, 9:16 vertical. CHARACTERS: [DILNOZA]: 9-year-old Uzbek girl, round face, dark brown eyes, two long black braids with red ribbons, white school blouse, navy-blue pinafore dress, small silver star pendant. AVOID: text, letters, watermark, logos, extra fingers, distorted face, subtitles, captions, on-screen text, face morphing, flicker; the last frame is sharp, no fade, no motion blur.
```
Why it works: END of 1 = SCENE of 2 and END of 2 = SCENE of 3, word for word (🔗). Clip 3 → 4 is a ✂️ match on action: the paper butterfly flies out of the classroom door, and clip 4 starts in the yard as it comes out of the school door with her following it. The ✂️ clip ends mid-motion; that is fine, because the cut carries the movement on.

If Sound = 2, the video prompts say "SPEECH: none, no one speaks" and a narration block follows (line k is read over clip k):
```
1. Dilnoza sinfda yolg'iz o'tirardi. Daftari hamon bo'sh edi.

2. Shunda derazaga kichkina kapalak qo'ndi.

3. Va uning chizig'i birdan jonlandi.

4. Ba'zan orzu seni o'zi yetaklab ketadi.
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
- Pairing is always 1:1: image k is the start frame of video k. Batch tools that take an image list plus a video-prompt list depend on this, so never add, drop or reorder prompts between the two lists.
- Google Flow: Frames to Video takes a start frame and optionally an end frame. For a 🔗 join, image k (start) + image k+1 (end) gives an almost perfect join. Do not set an end frame across a ✂️ join. Ingredients to Video / reference images help keep the same face and clothes.
- For better look-alike keyframes: when generating image k+1, attach image k (and the character reference) as a reference image, so the room, light and clothes stay the same.
- Gemini app: upload image k, paste video prompt k; clips up to 8 s.
- Kling and similar: 5 or 10 s clips; start and end frames supported.
- The aspect ratio in the prompts must match the generator's ratio setting for both images and videos.
- Long films: N > 16 → lists are sent in parts of 16; the user pastes the parts one after another. Numbering never restarts.

---

## 12. FINAL PACKAGE TEMPLATES
Editing guide (in the chosen language):
1. Import the clips in order 1…N.
2. On 🔗 joins the last frame of clip k and the first frame of clip k+1 are the same picture: trim 2–5 frames at the join so there is no visible freeze.
3. Transitions: straight cuts on 🔗 and ✂️ joins; a short cross-dissolve only on time jumps.
4. Sound: if the generated music differs between clips, mute it and lay one music track under the whole film; add the narration (Sound 2).
5. Subtitles: auto-captions in the chosen language; check the spelling by hand.
6. Export: 1080×1920 for 9:16, 1920×1080 for 16:9, 1080×1080 for 1:1, 30 fps.

Titles: 3 variants (curiosity, emotion, benefit). Description: 2–3 lines + a question to viewers. Hashtags: 10, broad + niche, in the chosen language.
Thumbnail prompt: the most emotional moment, one face in close-up, strong contrast, empty space for a title the user adds later (no text rendered in the image).
