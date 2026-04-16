Title
Can Generative AI Become the Emotional and Narrative Heart of an Interactive Experience?
Optional subtitle:
A 3D Prototype of AI-Driven Interrogation, Trauma, and Rehabilitation
1. Abstract
Include:
the project’s central research question
what kind of prototype you built
the main AI methods used
what the prototype demonstrates
the main limitation or challenge
What this section should say:
you built a 3D game prototype where AI generates dialogue and voice for unstable soldiers and the Mad God
the goal was to see whether AI could become central to narrative and emotion rather than decorative
the system used Unity, Ollama, TTS, RAG, and authored prompt/context assets
the result was promising but challenged by coherence, pacing, and live-generation reliability

Abstract
This project investigates whether generative AI can become the emotional and narrative heart of an interactive experience rather than functioning as a supplementary effect. To explore this question, we developed a first-person 3D prototype in which the player encounters unstable soldier figures and a companion-antagonist called the Mad God inside a haunted environment. The project combines Unity-based gameplay systems with a local Python backend that connects a language model through Ollama, a text-to-speech pipeline, and retrieval-augmented grounding from research material. Rather than relying on generic prompting alone, the system uses authored context assets including a Mad God lore file, structured soldier profiles, and testimony fragment banks to shape character identity, trauma, and reveal progression.
The prototype tests several AI-driven interaction modes, including generated choices, debate-style exchanges, and typed player input. These systems were designed to support an interrogation and rehabilitation loop in which dialogue affects how characters are perceived and resolved. The project demonstrates that generative AI can meaningfully support dynamic characterization and replay variability, but only when it is scaffolded by careful prompt design, contextual data, runtime safeguards, and clear interface design. The development process also revealed major challenges, including response coherence, structured output reliability, latency, and the difficulty of making AI dialogue feel psychologically grounded in a live game loop.


2. Introduction
This section should establish:
the broader context of generative AI in games and interactive storytelling
why this question matters
what gap your project is addressing
your research question and objective
Subsections you can use:
Context
Research Question
Significance
Objectives
Points to include:
many creative AI projects use generative systems as content add-ons
your project instead asks whether AI can carry the emotional core of an encounter
your prototype focuses on unstable characters whose dialogue shapes player experience and progression
the main objective was to test whether live AI dialogue could support an interrogation/therapy loop in a 3D world

2. Introduction

As programmers, game makers, and players, we have become familiar with NPCs and scripted dialogue in games. We know how these NPC characters are usually constructed, and we are equally familiar with the monotony of their repeated delivery. Because of this, we wanted to experiment with what it might feel like if not only the main story were unscripted, but even smaller NPC interactions as well. Minor NPCs are often characters with only one to three preset lines that never change; even in an open-world experience, this can still limit immersion and the experience. By shifting away from that model and allowing an NPC to generate new dialogue each time the player interacts with them, we hoped to create a more interactive and immersive experience that feels less fixed and more alive.
This idea was also extended to the main characters in order to explore whether they could develop more of their own uniqueness and personality through generative dialogue.
Generative AI has become increasingly visible in creative practice, especially in projects that use image generation, chatbot systems, or procedural content tools. In games and interactive media, however, generative AI is often positioned as an add-on rather than as the center of the player’s experience. It may be used to produce flavor text, assist with asset creation, or create occasional variation, but the core emotional and narrative structure of the work usually remains authored through conventional scripting. This project begins from a different question: can generative AI become the emotional and narrative heart of an interactive experience rather than simply extending one?
This question is particularly relevant in the context of interactive storytelling. Many games already rely on branching dialogue, authored narrative states, and carefully controlled emotional pacing. Generative language models offer the possibility of variability, responsiveness, and replayability that exceed the limits of fixed dialogue trees. At the same time, these systems introduce significant risks. AI-generated dialogue can become generic, repetitive, incoherent, or emotionally shallow, especially when it is inserted into a game without sufficient narrative framing or technical control. The challenge, then, is not only whether AI can generate text, but whether it can sustain character, emotional tone, and narrative progression inside a live interactive loop.
This project addresses that challenge through a first-person 3D prototype built in Unity. In the game, the player moves through a haunted environment populated by unstable soldier figures and guided or manipulated by a companion-antagonist called the Mad God. The soldier characters are imagined as figures whose identities have been fractured by war, trauma, and moral injury. The player’s role is not simply to defeat them in combat, but to confront, destabilize, interpret, and eventually rehabilitate them through dialogue. These encounters are supported by generative AI systems that produce spoken lines, testimony fragments, and emotionally responsive exchanges. In this way, the project treats AI dialogue not as background flavor, but as a core gameplay and narrative mechanism.
The significance of this project lies in its attempt to combine several layers of generative AI into one embodied, playable system. The prototype does not only use AI for text generation. It also integrates text-to-speech, retrieval-augmented grounding, authored lore and profile files, and runtime interaction logic. This combination was intended to test whether AI-driven characters could feel more alive and narratively central when their responses were shaped both by generative variation and by designed contextual scaffolding. The project therefore sits at the intersection of interactive storytelling, generative dialogue systems, and experimental game design.
The main objective of the project was to build a playable prototype in which AI-driven dialogue facilitates an interrogation and rehabilitation loop inside a 3D environment. More specifically, the project aimed to test whether live-generated dialogue could support emotional confrontation, reveal fractured character identity, and create a sense that each playthrough might expose different aspects of a character’s memory or instability. A secondary objective was to compare different interaction forms, such as generated choices, debate-like exchanges, and typed player input, in order to better understand which modes make AI feel most central to the encounter.
A further motivation of the project came from dissatisfaction with the way AI is often presented in games as either a novelty or an invisible backend tool. This prototype instead treats AI as a co-constructed performance system. The player does not simply receive generated content; they encounter it through voice, subtitles, timing, scene framing, and escalating interaction states. In that sense, the project is both technical and artistic. It asks not only whether a model can produce dialogue, but whether a system built around that dialogue can sustain tension, personality, and emotional meaning.
The project also responds to a broader problem in generative AI design: the assumption that better outputs come mainly from larger or more powerful models. During development, it became increasingly clear that model capability alone was not enough. The quality of the interaction depended just as much on authored prompt assets, character profiles, testimony fragments, reveal stages, fallback behaviour, and UI design. One of the central findings of the project is therefore that generative AI becomes more compelling in narrative games when it is treated as part of a larger designed system of context and performance, rather than as an autonomous intelligence dropped into a scene.
Taken together, these concerns frame the central research question of the project: can generative AI become the emotional and narrative heart of an interactive experience rather than just an add-on? This report argues that the answer is partially yes, but only when AI output is carefully scaffolded through authored context, scene integration, and interaction design. The prototype demonstrates both the promise of such systems and the practical difficulties involved in making them coherent, responsive, and emotionally convincing in real time.

3. Project Description
This will likely be the biggest section.
Suggested subsections:
3.1 Vision for Generative AI in Creative Practice
Include:
the conceptual idea behind the game
the role of trauma, moral injury, identity loss, and instability
why AI was important to the concept
Points:
the game imagines soldiers whose identities have fractured through war and PTSD-like trauma
the player encounters them in a haunted 3D environment
the AI was intended to produce variability, emotional unpredictability, and character-specific testimony
the Mad God functions as a companion/antagonist that frames the emotional tone of the world

3. Project Description
3.1 Vision for Generative AI in Creative Practice
This project explores whether generative AI can function as the emotional and narrative core of an interactive experience rather than as a decorative or supplementary feature. The prototype takes the form of a first-person 3D environment in which the player encounters hostile, unstable soldier figures and a companion-antagonist entity called the Mad God. These characters are not intended to behave like static non-player characters with fixed dialogue trees. Instead, they are designed as partially generative characters whose speech, emotional tone, and narrative revelations can shift across playthroughs.
The central thematic concern of the project is the erosion of identity through war, trauma, and moral injury. The soldiers are not presented as representatives of any one nationality, ethnicity, or historical conflict. Instead, they are deliberately generalized and partially obscured figures whose instability reflects broader questions about memory, violence, and the psychological afterlife of war. This decision shaped both the visual design of the soldier sprites and the design of the AI prompt system. Rather than grounding each character in a specific country or army, the project focuses on fractured identity, sensory triggers, guilt, dissociation, and altered behavior. In this sense, the game is less interested in realism as historical simulation than in realism as emotional and psychological texture.
Generative AI was important to this concept because the project aimed to produce encounters that felt variable, unstable, and partially unknowable. A fixed dialogue tree could support branching outcomes, but it would not easily create the feeling that each encounter might expose a different memory, contradiction, or emotional fracture. The use of generative dialogue allowed the project to test whether character testimony, confrontation, and rehabilitation could feel more alive if the system responded dynamically to the player rather than repeating the same authored lines.

3.2 Technologies Used
Include:
Unity
C#
Python
Ollama
TTS system
RAG module
subtitle/UI systems
Points:
Unity handled world logic, encounters, UI, and scene transitions
TTSRunner connected Unity to the Python backend
the Python backend assembled prompts, called Ollama, and produced TTS output
prompt asset files were used to keep character design editable outside code

3.2 Technologies Used
The prototype was developed primarily in Unity using C# for gameplay systems, scene logic, UI behavior, and interaction management. Unity handled the 3D environment, player movement, soldier encounters, Mad God sequencing, subtitles, and scene transitions. On the AI side, the project used a Python backend to manage dialogue generation, prompt assembly, retrieval-augmented context, and text-to-speech output. A key bridge between Unity and Python was the TTSRunner script, which handled process startup, request dispatch, response parsing, audio loading, and subtitle display.
Text generation was handled locally through Ollama, which allowed the project to experiment with live generation during gameplay rather than relying on static prewritten dialogue. Spoken delivery was produced through a text-to-speech pipeline so that generated lines could be voiced in real time. This combination of local language generation and TTS was essential to the project’s design, since one of the research goals was to see whether AI could feel embodied and present inside the scene rather than operating invisibly in the background.
Additional prompt assets were stored in editable files outside the gameplay code. This allowed character identity and lore to be developed as authored context rather than being hardcoded directly into the interaction logic. In practice, this meant that the project blended procedural generation with authored narrative scaffolding.

3.3 Machine Learning and Generative AI Implementation
Explain:
what AI tasks were actually implemented
how they differ from one another
Tasks to mention:
text generation for live character dialogue
text-to-speech synthesis for spoken delivery
retrieval-augmented grounding from research PDFs
structured reply generation for debate and typed interaction modes
prompt-conditioned role behavior for Mad God and soldiers
Important clarification:
the model was not trained from scratch
instead, a pretrained model was conditioned with authored prompts, profile assets, and retrieved context 
3.3 Machine Learning and Generative AI Implementation
The project did not involve training a new model from scratch. Instead, it used pretrained generative systems and shaped their output through prompt design, retrieval context, structured character assets, and runtime logic. Several generative tasks were implemented.
The first was conditional text generation. When the player interacted with the Mad God or a soldier, Unity sent contextual information to the Python backend, which assembled a prompt including the speaker role, recent interaction history, and optional character-specific context. Ollama then generated a short line or structured response depending on the interaction mode. This was used for general speech, generated choice interactions, debate-style exchanges, and typed conversation experiments.
The second was text-to-speech synthesis. Once a line of dialogue had been generated, the backend synthesized speech for that line and returned it to Unity as audio that could be played in scene. This step was not purely cosmetic; the voice output was part of the project’s attempt to make the AI characters feel present and performative, especially in tense or cinematic moments.
The third was retrieval-augmented grounding. The project included a PDF-based RAG pipeline that indexed research material and injected retrieved fragments into prompt context. This was intended to reduce purely generic improvisation and to push the generated dialogue toward more grounded themes related to trauma, war memory, dissociation, and moral injury. RAG was not used as a source of verbatim reproduction, but rather as a thematic grounding layer.
The fourth was prompt-conditioned role behavior. The Mad God and the soldiers did not share one generic prompt. The Mad God used a separate lore bible and strong role-conditioning to maintain a coherent tone: bored, powerful, unstable, amused, and predatory. Soldiers used profile-specific prompt fields and testimony fragments that supported more individualized emotional behavior. These systems were especially important because one of the central problems encountered in development was that unconstrained AI dialogue quickly became generic, repetitive, or emotionally shallow.
3.4 Infrastructure
Include:
local runtime design
Unity-to-Python pipeline
runtime controls for speed/testing
performance tuning
Points:
the system runs locally with Unity calling a Python process
startup and response speed were tuned using runtime settings
fast/normal reply modes and restart utilities supported playtesting
lazy vs warm initialization was explored to manage RAG performance

3.4 Infrastructure
The project used a local runtime architecture in which Unity launched and communicated with a Python process responsible for the AI pipeline. This design allowed the team to keep the game logic and scene systems in Unity while offloading prompt construction, LLM interaction, and TTS generation to Python. The TTSRunner component was used to manage this connection at runtime. It exposed readiness state, request functions, subtitle behavior, and utility features such as restarting the backend during playtesting.
Because real-time AI use inside a game can quickly become slow or unstable, the project also included several performance and testing controls. Startup behavior was tuned so that model pulling and RAG initialization could be adjusted for faster iteration. The system also exposed faster and slower response modes to help balance dialogue richness against playability. These optimizations were necessary because a technically successful AI pipeline is not enough for an interactive project if the player must wait too long for the scene to continue.


3.5 Data and Prompt Assets
This section directly addresses your professor’s feedback.
Break it into:
Research grounding
Character scaffolding
Prompt design
Points:
research PDFs were used for RAG grounding, not for full model training
Mad God used a custom lore bible
soldiers used structured profile assets
testimony fragment banks provided concrete emotional and sensory material
these assets were used to make responses more distinct, less generic, and more psychologically grounded
Things to describe in detail:
mad_god_lore.txt
soldier_profiles.json
soldier_testimony_fragments.json
Mention that soldier profiles include:
role
former identity
defining trauma
trigger stimulus
moral wound
taboo topic
reveal stages
Mention that fragments include:
emotion
trigger
body sensation
moral wound
identity theme
speech style

3.5 Data and Prompt Assets
One of the most important developments in the project was the shift from generic prompting toward authored context assets. Rather than depending entirely on one broad instruction like “speak as a traumatized soldier,” the project introduced several layers of supporting material.
First, the Mad God used a dedicated lore file that described the character’s identity, tone, recurring motifs, power dynamics, and preferred speech style. This made it possible to tune the character’s personality without rewriting core code and helped keep the Mad God’s dialogue more coherent across encounters.
Second, the soldiers used a structured profile file. Each soldier profile included fields such as military role, former identity, war theater, defining trauma, trigger stimulus, identity fracture, physical tell, taboo topic, public persona, hidden fear, moral wound, false belief, and reveal progression. These fields were designed to support stronger individuality and to make each soldier feel like a different psychological case rather than a reskinned version of the same prompt.
Third, the project used a testimony fragment bank. These fragments were tagged with emotional and sensory categories such as memory type, emotion, trigger, body sensation, moral wound, identity theme, and speech style. By injecting these fragments into prompts, the system gave the model more concrete material to draw from. This was particularly important because one of the recurring issues during development was that freeform AI dialogue tended to rely on vague trauma language unless it was given more specific authored cues.
Taken together, these assets functioned as the project’s working “dataset.” Although no new model training occurred, the project still relied heavily on data design in the form of lore files, profiles, fragments, and retrieved research documents. In practice, this authored context became one of the most important determinants of output quality.


3.6 System Integration
Explain the flow:
player input in Unity
request sent through TTSRunner
Python assembles context
Ollama generates text
TTS synthesizes voice
Unity displays subtitles and plays the line
interaction state updates in scene
You can describe this as a pipeline.
3.6 System Integration
All of these components were integrated into a single gameplay loop. The player moved through a 3D environment and encountered soldiers or the Mad God. Unity scripts handled movement, triggering, confrontation logic, and UI presentation. When an interaction required AI dialogue, Unity packaged the relevant context and sent it through the runtime bridge. The Python backend then assembled a prompt using role, profile data, recent conversation memory, and optional retrieved context. Ollama generated text, the TTS system synthesized the result, and Unity received the line as both audio and subtitle content.
This architecture allowed the project to combine authored game structure with generative variability. The environment, pacing, and interaction triggers were still designed in Unity, but the emotional content of many encounters was shaped live through generative dialogue. In this way, the system attempted to place AI not at the edge of the experience, but inside its core dramatic loop.

4. Process
This should document how the project evolved.

Suggested subsections:
4. Process
4.1 Development Stages
Possible structure:
initial prototype and baseline AI/TTS integration
Mad God intro and companion development
soldier interaction systems
RAG integration
profile/testimony context system
subtitle/UI and scene presentation refinements
4.1 Development Stages
The development of this project moved through several overlapping stages rather than a single linear pipeline. Although the original concept centered on a 3D environment in which the player confronts unstable soldiers and later rehabilitates them, the actual development process quickly showed that the most difficult part of the project would not be building the environment itself, but designing an AI interaction system that felt emotionally meaningful, technically stable, and integrated into gameplay.
The first stage focused on establishing the baseline interactive loop in Unity. This included the first-person environment, soldier encounters, combat behavior, transitions into dialogue, and the therapy room sequence. At this point, the AI component was still relatively simple. The priority was to get a minimal pipeline working so that generated text and voice could appear inside the game rather than existing only as a separate prototype.
The second stage focused on making the AI pipeline functional at runtime. This involved connecting Unity to a Python backend capable of calling a language model through Ollama and returning generated lines to the game. In parallel, the text-to-speech system was integrated so that AI-generated lines could be voiced and played in scene. This was a crucial stage because it transformed the idea from a static design concept into a live system: Unity could ask for a line, Python could generate it, TTS could speak it, and the player could hear the result in context.
The third stage concentrated on the Mad God. The Mad God became a useful early test case because the character had a strong narrative role and a distinctive tone. This part of development included the intro sequence, camera reframing, player locking, rush-in and retreat behavior, subtitle support, skip behavior, and personality tuning. Building the Mad God helped clarify that the project needed stronger authored prompt control if AI characters were going to feel memorable rather than generic.
The fourth stage focused on soldier interaction systems. Initially, the goal was simply to let the player damage a soldier, trigger dialogue, and then resolve the encounter through AI-assisted conversation. As development progressed, however, the limits of simple generated choice interactions became clearer. This led to experiments with multiple interaction forms, including generated response options, a debate interaction, and a typed conversation mode. These experiments were not just feature additions; they were attempts to answer a core design question about what kind of interaction would make AI feel central rather than ornamental.
The fifth stage involved strengthening the context used by the AI. Early outputs often felt too generic, repetitive, or disconnected from the intended themes. In response, the project introduced a separate Mad God lore file, structured soldier profiles, and a testimony fragment bank. At the same time, RAG was integrated to bring research-based thematic grounding into the prompts. This stage marked a major conceptual shift in the project: instead of asking the model to “be a traumatized soldier,” the system began to treat character generation as something that had to be scaffolded through authored context, memory, and emotional staging.
The sixth stage focused on UI and presentation. Because AI interactions only felt convincing if they were readable and situated properly, substantial work went into subtitles, top-of-screen dialogue presentation, typed-input layout, generated choice placement, and visual integration. The project also added runtime utilities such as faster testing modes and backend restart controls so that the AI systems could be iterated on more quickly during playtesting.


4.2 Challenges and Solutions
This is one of the most important sections.
Challenges to discuss:
generic or repetitive AI outputs
unstable structured JSON generation
response latency in a live game loop
typed and debate interactions feeling too similar
interactions resolving too quickly
UI conflicts and readability issues
balancing authored control with generative variability
Solutions to discuss:
added character-specific lore and profile assets
added testimony fragments for concrete context
added short conversation memory
added fallback logic and debug tracing
added top-layout dialogue UI and subtitles
tuned emotional stages and speech shaping
4.2 Challenges and Solutions
One of the biggest challenges in the project was that AI-generated dialogue did not automatically feel like meaningful character dialogue. Early outputs were often coherent at the sentence level but emotionally shallow at the encounter level. Soldiers could sound vaguely unstable, but not necessarily distinct, psychologically grounded, or narratively specific. This created a mismatch between the ambition of the project and the actual player experience. The intended effect was not simply “the NPC talks with AI,” but rather “the player feels they are confronting a damaged and unstable person whose speech reveals identity, memory, and emotional fracture.”
The first major response to this problem was prompt refinement. However, prompt refinement alone was not enough. The deeper solution was the addition of authored character scaffolding. Mad God lore, soldier profiles, and testimony fragments were introduced so that the AI had stronger character material to work with. This shifted the system away from generic role prompting toward profile-driven generation. The improvement here was both technical and conceptual: it became clear that generative systems in a narrative game require authorship at the level of context design, not just model access.
A second major challenge involved structured output reliability. Some gameplay systems, especially the debate and typed interaction modes, depended on the backend returning parseable structured data. In practice, the language model did not always return valid JSON, even when asked to. This caused failures in choice generation, odd repetition, or generic fallback replies that weakened the illusion of live intelligence. To address this, the system introduced stronger JSON forcing, raw-text salvage logic, explicit debug logging, and safer fallback behavior. These changes did not eliminate all instability, but they made the system more debuggable and made failure more visible rather than silently degrading the encounter.
A third challenge was latency. Because the project relied on live local generation and speech synthesis, delays in response time could interrupt the flow of the encounter. A player who waits too long for a line or a choice to appear begins to perceive the system as broken rather than dramatic. In response, the project introduced several runtime and startup optimizations, including model-pull controls, lazy versus warm RAG initialization, fast versus normal response settings, and a backend restart utility exposed through Unity. These improvements were necessary not just for convenience, but for playability.
A fourth challenge emerged in interaction design. The project explored generated choice interactions, debate-based exchanges, and typed/freeform input. These systems were meant to feel different, but in practice they often felt too similar because they were driven by the same underlying model behavior. This revealed a key lesson: changing the UI format does not automatically produce a different emotional experience if the prompt logic, pacing, and state transitions remain too similar underneath. The typed system was intended to feel more personal and open-ended, while the debate system was intended to feel more confrontational and game-like, but both required much stronger internal structure to truly diverge.
A fifth challenge was conversation quality in the typed interaction mode. Although the promise of typed interaction was that it would feel more like a real conversation, it often drifted, fixated on the wrong topic, or responded in ways that felt disconnected from the player’s actual sentence. This was particularly frustrating because typed conversation seemed like the most promising route for making the AI feel central and original. The solution was only partial: local tagging was improved so that player inputs could be categorized more intelligently, prompt instructions were made more explicit, and optional trigger words were reframed as emotional pressure tools rather than mandatory correctness checks. Even with these changes, the typed mode remained one of the most ambitious but also most unstable parts of the prototype.
Finally, the project encountered the challenge of emotional delivery. Even when text generation improved, voice synthesis could still make lines sound flatter than intended. Since direct emotional controls in the TTS model were limited, the project addressed this through stage-based speech shaping before synthesis. By altering the structure of generated lines according to emotional stage, the system could produce more fragmented, hesitant, repetitive, or urgent speech. This helped move the AI voice closer to the intended emotional tone without changing the underlying TTS engine.
4.3 Successes
Talk about what genuinely worked:
Mad God personality became strong and memorable
AI/TTS worked in a live 3D scene
subtitles and voice made AI more present
soldiers became more distinct after profile-based prompting
RAG and authored context gave stronger thematic grounding
you learned how much authored structure matters in AI systems

4.3 Successes
One of the clearest successes of the project was the Mad God. Once the character was given a dedicated lore file and stronger prompt conditioning, the Mad God became a compelling example of how AI could support a distinct narrative voice. The character’s speech no longer felt like generic “fantasy AI dialogue,” but began to reflect a more deliberate tone: ancient, bored, cruel, amused, and rhetorically sharp. The Mad God also benefited from strong scene integration through movement, reframing, subtitles, pre-recorded intro clips, and direct interaction support, making the AI feel embodied rather than abstract.
Another major success was the integration of a live Unity-to-Python AI pipeline into a playable 3D prototype. The system was not simply demonstrated as a tech experiment in isolation; it was embedded inside a world with combat, transitions, rehabilitation scenes, and ongoing character encounters. This matters because one of the project’s core questions was whether AI could function inside a real interactive loop. Even with imperfections, the prototype demonstrated that generative dialogue and TTS could operate as active systems inside the game rather than as a separate demo.
A third success was the growing distinctiveness of the soldier characters after the introduction of profiles and testimony fragments. Earlier in development, soldiers often felt too similar. With structured prompt assets, they began to acquire clearer identities, different emotional triggers, and more differentiated narrative material. The project demonstrated that variation in AI output does not come only from model randomness; it comes from the quality and specificity of the authored context feeding the model.
The subtitle and dialogue presentation systems were also successful in making AI encounters more legible. Generated dialogue in an interactive environment can easily become hard to follow, especially when mixed with combat or scene transitions. By improving the subtitle display, top-aligned dialogue layout, and interaction-specific UI, the project made AI outputs feel more present and intentional. This was particularly important for preserving readability during emotionally dense or mechanically complex scenes.
4.4 Learning Experiences
Reflect on:
AI in games is not only about generation quality
interaction design and prompt design are inseparable
generative systems need scaffolding, not just model access
live systems expose failure modes that static demos hide
Meaningful AI characters require authored constraints as much as openness

4.4 Learning Experiences
The most important lesson of the project was that generative AI in games is not solved by simply adding a language model to a character. The real challenge lies in designing the conditions under which the model can produce meaningful, characterful, and context-aware output. In practice, this meant that prompt design, authored context assets, runtime handling, UI presentation, and fallback behavior were all just as important as the model itself.
A second major lesson was that character depth has to be authored even in a generative system. The project began with the hope that AI could create dynamic testimony and emotional variability on its own. Over time, it became clear that the strongest outputs came not from leaving the model unconstrained, but from giving it carefully designed profile information, testimony fragments, recurring imagery, reveal stages, and explicit role framing. In other words, the project taught that AI is most compelling when combined with deliberate narrative scaffolding.
A third lesson was that interaction design and generation quality are inseparable. It was not enough for the model to produce an interesting line; the surrounding interaction had to make that line matter. Waiting too long, losing choice visibility, or resolving an encounter too quickly could make even a strong line feel weak. This led to a broader understanding that generative systems in games must be evaluated as part of a whole player experience rather than as isolated outputs.
Finally, the project made clear that experimentation itself was an important part of the research. Not every interaction mode succeeded equally well, and some of the most useful insights came from systems that did not fully meet their original goals. The debate and typed interaction experiments, for example, exposed both the potential and the limitations of different approaches to AI conversation in games. These experiments helped clarify what kinds of authored support and technical robustness are necessary if AI is to feel like the emotional and narrative core of an interactive experience.


5. Future Work
Keep this concrete and realistic.
Possible subsections:
Dialogue quality and evaluation
Interaction refinement
System robustness
Narrative expansion
Points to include:
more systematic evaluation criteria for dialogue quality
stronger differentiation between debate and typed interaction
better long-term memory and coherence
improved structured output reliability
larger cast of soldier profiles
stronger emotional state tracking
more consistent consequences across the game loop

5. Future Work
Although the prototype demonstrates that generative AI can play a meaningful role in a narrative game loop, it also makes clear that this approach remains incomplete and open to further development. Future work would focus not only on extending the system with more content, but also on improving the quality, consistency, and evaluability of the AI interactions.
One important direction for future work is the development of a more systematic evaluation framework for dialogue quality. During this project, outputs were assessed primarily through iterative playtesting and qualitative judgment. While this was appropriate for prototyping, a future version would benefit from clearer evaluation criteria for coherence, emotional specificity, responsiveness to player input, repetition, and perceived character distinctiveness. These criteria could support more structured testing across different prompts, interaction modes, and generation parameters, making it easier to compare versions of the system and justify design choices more rigorously.
A second area for future work is improving conversational coherence over multiple turns. One of the persistent challenges in the prototype was that freeform conversation could drift, repeat itself, or latch onto the wrong topic. Although short-term memory and profile-driven prompting improved this behavior, the interactions still sometimes lacked the continuity required for a fully convincing long-form exchange. Future iterations could strengthen this by introducing better memory summarization, more explicit topic tracking, stronger turn-level goals, and more reliable control over structured outputs. These improvements would be especially important if typed conversation becomes the primary interaction mode.
A third area of expansion is the refinement of interaction design itself. The project experimented with generated choices, debate-style confrontation, and typed conversation, but these systems did not always feel as distinct in practice as they did in concept. Future work could push each mode further toward a specific dramatic function rather than treating them as parallel versions of the same conversation. For example, debate could be tuned more explicitly toward destabilization and escalation, while typed conversation could focus more on confession, memory reconstruction, and identity probing. Clearer differentiation between interaction modes would also make the player’s choices feel more meaningful.
The character system could also be expanded significantly. At present, the strongest improvements in dialogue quality came from authored assets such as lore files, soldier profiles, and testimony fragments. This suggests that future work should include a larger and more carefully curated bank of profiles, reveal stages, sensory triggers, and emotional fragment sets. Additional characters with more sharply differentiated speech patterns, trauma responses, and narrative arcs could help the system demonstrate stronger replay variation. A future version could also connect these character structures more directly to scene outcomes, visual changes, or world state consequences.
On the technical side, future work should improve robustness in live generation. Structured outputs remain a fragile part of many generative systems, and this project was no exception. More reliable parsing, stronger schema enforcement, repair strategies, and clearer debugging tools would make the AI pipeline less brittle. Latency also remains an important design constraint. While the project introduced faster testing modes and startup optimizations, future iterations could continue to reduce waiting time through better precomputation, caching, and response planning.
Finally, future work could address the broader question that motivated the project in a more comparative way. This prototype suggests that generative AI can contribute meaningfully to the emotional and narrative center of a game, but that success depends heavily on authored scaffolding and careful system design. A future project could compare fully scripted, partially generative, and heavily generative versions of the same encounter in order to better understand what AI adds, what it risks, and where the strongest balance lies between authorship and generation.

6. References
You will need:
AI / interactive storytelling references
trauma / war memory / PTSD references if cited
relevant projects or artworks
any technical references if cited in the report
What You Need References For
Your report will probably need sources in 5 groups:
generative AI and interactive storytelling
AI dialogue / procedural narrative in games
trauma, PTSD, memory, and moral injury
critical/creative writing on AI in art or game design
technical tools or systems only if you directly discuss them

7. Appendix
Include:
GitHub repo link
demo video link
presentation PDF link if useful
optional system diagram
optional table of prompt assets and file paths

