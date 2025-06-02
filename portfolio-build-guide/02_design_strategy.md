# Phase 2: Design Strategy for Sulayman Bowles's Interactive Portfolio (Palantir Aesthetic)

<claude_guide_phase>

<persona_instruction>
As the Expert Code Lead guiding the Developer (via Claude 4, operating in Agent mode), your role in this phase is to translate the approved vision from Phase 1—Sulayman Bowles's "Personal Intelligence Platform", the chosen "Primary Interactive Narrative Pattern", and the "Palantir Aesthetic"—into a concrete and actionable design strategy. This involves defining a specific brand personality, creating a comprehensive Visual Style Guide, prompting initial low-fidelity wireframes for desktop and mobile, and facilitating decisions on optional advanced features like the "Live Technical Analysis API" module. All outputs must meticulously align with `Project_Aesthetic_Guidelines_Palantir.md` and the refined Content Strategy.
</persona_instruction>

<claude_notes_section>
</claude_notes_section>

## 1. Purpose of This Phase

<phase_purpose>
This phase aims to:
1.  Define a compelling brand personality for Sulayman's portfolio that authentically reflects his unique combination of Music, Finance, Blockchain, Data Analysis, and Leadership, while embodying the Palantir ethos (e.g., "Data-Driven Intelligence," "Clarity in Complexity").
2.  Establish a detailed Visual Style Guide (`P2_Visual_Style_Guide_Palantir_Portfolio_V1.md`) codifying all visual elements (colors, typography, iconography, imagery, component styling, motion principles) based *directly* on `Project_Aesthetic_Guidelines_Palantir.md` and the refined content formatting guidelines.
3.  Guide the creation of initial low-fidelity wireframes for key pages and views. These wireframes must illustrate the layout of the chosen "Primary Interactive Narrative Pattern" (e.g., Network Graph) and its mobile adaptation (e.g., Master-Detail List), along with other core content sections, adhering to Palantir layout strategies.
4.  Facilitate a decision on whether to include the "Live Technical Analysis API" feature. If yes, select an integration pattern (Modular Panel, Modal/Overlay, or Embedded Card) and incorporate its conceptual placement into the wireframes.
5.  Discuss and document initial "Motion Design Principles" as part of the Visual Style Guide, defining the Palantir-aligned animation philosophy (subtle, purposeful, brief, utilitarian).
Success means having unambiguous design guidelines and conceptual layouts that are deeply rooted in the project's vision and foundational research, ready to inform high-fidelity UI development and component architecture.
</phase_purpose>

## 2. Key Deliverables

<key_deliverables_list>
By the end of this phase, the Developer, guided by you (Claude 4), should have produced:
* <deliverable type="DOCUMENT" id="P2_Brand_Personality_Statement_Sulayman_Bowles.md">Defines the portfolio's voice, tone, and character, aligning with Palantir's principles of professionalism, analytical prowess, and Sulayman's unique cross-disciplinary strengths.</deliverable>
* <deliverable type="DOCUMENT" id="P2_Visual_Style_Guide_Palantir_Portfolio_V1.md">Comprehensive guide detailing:
    * Specific color palette (dark/light modes, base #1F1F1F, accents #0052CC, #FFD60A etc.).
    * Typography system (Inter/Roboto, Source Code Pro, hierarchy, weights, sizes, line heights).
    * Iconography style and primary set (e.g., BlueprintJS Icons).
    * Imagery guidelines (abstract data viz, photo style for Sulayman).
    * Base component styling concepts (buttons, cards, forms, modals based on BlueprintJS and Palantir theme).
    * Custom Graphic Element guidelines (backgrounds, dividers, glyphs).
    * Initial Motion Design Principles (subtle, purposeful, standard timings).</deliverable>
* <deliverable type="WIREFRAMES" id="P2_Key_Screens_Wireframes_LowFi_DesktopMobile.pdf">Low-fidelity wireframes for desktop AND mobile/tablet adaptations of:
    * Homepage (prominently featuring the chosen "Primary Interactive Narrative Pattern" and its mobile adaptation).
    * Typical Content Page (e.g., Project Detail, Experience Detail, Case Study template).
    * About Page.
    * Contact Page.
    * (If included) Wireframe showing integration of the "Live Technical Analysis API" feature using its chosen pattern (e.g., as a Modal/Overlay).</deliverable>
* <deliverable type="DOCUMENT" id="P2_Motion_Design_Detailed_Specs_V1.md">(Initial Draft) Defines parameters for key animation behaviors (loading states, focus transitions, data point materialization etc.).</deliverable>
* <deliverable type="DECISION_LOG" id="P2_Live_API_Feature_Decision_And_Pattern.md">(If applicable) Documents decision to include/exclude the Live API feature, the chosen integration pattern, and rationale.</deliverable>
* <deliverable type="DOCUMENT" id="P2_Performance_Philosophy_And_Targets_V1.md">(If not created in Phase 1, or refined here) Document outlining performance goals (load times, animation smoothness) to guide design complexity.</deliverable>
* <deliverable type="TODO" assigned_to="User/Sulayman" id="P2_Todo_ApproveDesigns">Review and approve Brand Personality, Visual Style Guide, Motion Design Specs, and Wireframes.</deliverable>
</key_deliverables_list>

## 3. Guiding the Developer: Phase Tasks & Prompts

<tasks_for_claude>

### Task 2.1: Defining Sulayman Bowles's Brand Personality (Palantir-Aligned)
<task id="2.1_DefineBrandPersonalitySB">
  <objective>To articulate a brand personality for Sulayman's portfolio that is authentic while embodying the Palantir ethos (e.g., "Data-Driven Intelligence," "Precision & Insightful Analysis") and reflecting his unique blend of Music and analytical skills.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, drawing from Sulayman Bowles's resume, the core principles in `Project_Aesthetic_Guidelines_Palantir.md`, and the tone guidelines in `Content_Strategy_Palantir_Portfolio.md`, let's craft the 'P2_Brand_Personality_Statement_Sulayman_Bowles.md'.

This statement should define the portfolio's voice. Consider adjectives like: Analytical, Insightful, Innovative, Precise, Methodical, Versatile, Forward-Thinking, Disciplined, Creative yet Rigorous.
Draft 2-3 paragraphs that describe:
1.  The desired professional persona to project (e.g., an "analytical architect" or "data-driven innovator with a conductor's precision").
2.  How the Palantir aesthetic's qualities (e.g., "clarity in complexity") will be reflected in this persona.
3.  How Sulayman's unique Music background can be subtly woven in as a strength (e.g., "approaches complex data systems with the same discipline and structural understanding he applies to musical composition").

<definition_of_done>
* Statement is 2-3 paragraphs.
* Clearly defines desired professional persona.
* Explicitly links persona to Palantir aesthetic principles.
* Authentically integrates Sulayman's cross-disciplinary strengths (Music + Tech/Finance).
</definition_of_done>
Why this is important: This statement will guide the feel of all design choices and the tone of any UI microcopy, ensuring a cohesive brand experience."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DRAFT">P2_Brand_Personality_Statement_Sulayman_Bowles.md</expected_artifact>
</task>

### Task 2.2: Developing the Comprehensive Visual Style Guide & Motion Design Specs
<task id="2.2_DevelopVisualStyleGuideMotion">
  <objective>To meticulously translate the specifications from `Project_Aesthetic_Guidelines_Palantir.md`, `Content_Strategy_Palantir_Portfolio.md` (for text formatting), and `Custom_Graphic_Elements_For_Palantir_Aesthetic.md` into the practical `P2_Visual_Style_Guide_Palantir_Portfolio_V1.md` and an initial `P2_Motion_Design_Detailed_Specs_V1.md`.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, this is a cornerstone task. We need to create the comprehensive 'P2_Visual_Style_Guide_Palantir_Portfolio_V1.md' by systematically codifying all visual rules from our foundational research. This guide must detail:

1.  **Color Palette:** As per `Project_Aesthetic_Guidelines_Palantir.md`:
    * Dark Mode (Default): Specific HEX codes for backgrounds (e.g., #1F1F1F, #121212), panel backgrounds (#2E2E2E), primary text (#FFFFFF or #F5F5F5), secondary text (#A8A8A8), primary accent (#0052CC), secondary accent (#FFD60A), status/alert colors.
    * Light Mode: Corresponding HEX codes for light backgrounds (#F5F5F5 or #E0E0E0), text (charcoal #2E2E2E), etc.
    * Accessibility Theme Palettes (Conceptual): Placeholders for Warm Dark Mode and High-Contrast Mode tokens.
2.  **Typography System:** As per `Project_Aesthetic_Guidelines_Palantir.md` and `Content_Strategy_Palantir_Portfolio.md`:
    * Font Families & Weights: Specify Inter/Roboto and Source Code Pro/Roboto Mono, detailing weights (e.g., 300, 400, 500, 600, 700) for each usage.
    * Scale: Define px sizes and line heights (e.g., 1.5x) for H1 (32px bold), H2, H3, Body (14-16px regular), Secondary Text (12-14px), Monospaced Data, UI labels.
    * Minimalist Formatting: Reinforce rules for bolding (headers only), italics (data callouts only).
3.  **Iconography:** Primary set (e.g., BlueprintJS Icons), style (minimalist, geometric), color usage (e.g., inherit text color or use accent for interactive icons), sizing.
4.  **Imagery:** Guidelines for Sulayman's photo style, abstract data visualizations, network motifs.
5.  **Custom Graphic Elements:** Style definition for background textures (e.g., low-opacity polygonal mesh), section dividers (e.g., thin SVG line fragments), spot glyphs (e.g., Data-Music Fusion Glyph).
6.  **Component Base Styling (Conceptual):** Visual language for common elements like Buttons (BlueprintJS-based, Palantir-themed: rectangular, 4-6px radius, #0052CC primary), Cards (BlueprintJS `Card` style: elevation, padding), Modals (BlueprintJS `Dialog` style), Form Inputs (underlined style).
7.  **Initial Motion Design Principles:** Create `P2_Motion_Design_Detailed_Specs_V1.md`. Define the core philosophy (purposeful, subtle, brief, utilitarian). Specify standard animation timings (e.g., 150-200ms for feedback, 250-400ms for transitions), default easing functions (e.g., ease-out), and parameters for foundational effects like shimmer on skeletons, focus transitions, and data point materialization, as discussed in.

<definition_of_done>
* `P2_Visual_Style_Guide_Palantir_Portfolio_V1.md` is comprehensive, covering all listed visual elements with specific values and references to foundational research.
* `P2_Motion_Design_Detailed_Specs_V1.md` outlines core animation principles and parameters for foundational effects.
* All style definitions are directly traceable to `Project_Aesthetic_Guidelines_Palantir.md` or other relevant research.
</definition_of_done>
Why this is important: This guide will be the single source of truth for the website's visual appearance and feel, ensuring consistency and fidelity to the Palantir aesthetic."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DRAFT_DOCUMENT">P2_Visual_Style_Guide_Palantir_Portfolio_V1.md</expected_artifact>
  <expected_artifact type="DRAFT_DOCUMENT">P2_Motion_Design_Detailed_Specs_V1.md</expected_artifact>
</task>

### Task 2.3: Conceptualizing Key Screen Wireframes (Desktop & Mobile)
<task id="2.3_CreateWireframesWithAdaptations">
  <objective>To create low-fidelity wireframes for key pages, illustrating layout, content hierarchy, placement of the "Primary Interactive Narrative Pattern" and its mobile adaptation, and other UI elements, adhering to Palantir layout strategies.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, using the approved 'Primary Interactive Narrative Pattern' (from `P1_Chosen_Interactive_Pattern_Rationale.md`), the `P2_Visual_Style_Guide_Palantir_Portfolio_V1.md` for structural cues, and importantly, the strategies in `Mobile_Adaptation_Palantir_Viz.md`, create low-fidelity wireframes (`P2_Key_Screens_Wireframes_LowFi_DesktopMobile.pdf`) for:

**Desktop Views:**
1.  **Homepage/Profile Explorer:** Prominently feature the chosen "Primary Interactive Narrative Pattern" (e.g., Network Graph). Show placement of its filters/legend, any introductory text, and primary CTAs.
2.  **Content Detail View (e.g., Side Drawer or Modal triggered from Interactive Pattern):** Illustrate the layout for detailed project/experience information, including "Stat Callouts" and "Data-Insights" sections.
3.  **Case Study Page Template:** Structure for a long-form case study, showing placement of text blocks, embedded visuals (Palantir-style diagrams/charts), and section dividers.
4.  **About Page:** Layout for narrative text and professional photo.
5.  **Contact Page:** Layout for contact info and form.

**Mobile/Tablet Adaptive Views (Key Screens):**
6.  **Homepage/Profile Explorer (Mobile Adaptation):** Show how the "Primary Interactive Narrative Pattern" transforms for smaller screens (e.g., if Network Graph, show the 'Master-Detail List + Mini-Map' or 'Filtered Accordion' layout).
7.  **Content Detail View (Mobile Adaptation):** How the side drawer or modal content reflows for mobile.
8.  **Case Study Page (Mobile Adaptation):** Single-column reflow, ensuring readability.

For all wireframes, focus on:
* Palantir layout principles (grid-based, structured, clear hierarchy, use of panels/cards).
* Placement of global elements (Header with monogram & nav, Footer).
* Indicating where custom graphic elements (backgrounds, dividers) might be used.
* Information density management through progressive disclosure.

<definition_of_done>
* Wireframes cover all listed key screens for both desktop and mobile/tablet.
* Clearly depict layout, content hierarchy, and placement of the primary interactive pattern and its mobile adaptation.
* Adhere to Palantir layout strategies.
* Mobile views demonstrate clear adaptation strategies from `Mobile_Adaptation_Palantir_Viz.md`.
</definition_of_done>
Why this is important: Wireframes provide the blueprint for page structure and ensure our interactive and aesthetic goals are achievable within the layout before detailed UI design."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DRAFT_WIREFRAMES">P2_Key_Screens_Wireframes_LowFi_DesktopMobile.pdf</expected_artifact>
</task>

### Task 2.4: Decision & Conceptual Planning for Optional "Live Technical Analysis API" Feature
<task id="2.4_DecideAndPlanLiveAPIFeature">
  <objective>To make a final decision on including the 'Live Technical Analysis API' feature, select an integration pattern if proceeding, and conceptually incorporate it into wireframes, based on `Live_API_Feature_Integration_Patterns.md`.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, let's address the optional 'Live Technical Analysis API' feature. Sulayman is considering this to showcase his financial/data analysis skills.
Review the three Palantir-aligned integration patterns from `Live_API_Feature_Integration_Patterns.md`:
1.  Modular Panel within a Data-Dense Dashboard Layout.
2.  Modal/Overlay for On-Demand, Focused Interaction (BlueprintJS `Dialog` based).
3.  Embedded Card with Expand/Collapse Controls (BlueprintJS `Card` and `Collapse` based).

Please:
    a. Based on Sulayman's goals and the overall portfolio UX, provide your recommendation on whether to include this feature in V1 or defer it.
    b. If recommending inclusion, which of the three integration patterns do you believe is most suitable? Justify your choice considering factors like UX impact, information hierarchy, consistency with the main portfolio design, and development complexity.
    c. If included, update your `P2_Key_Screens_Wireframes_LowFi_DesktopMobile.pdf` to show:
        * Where the trigger for this feature would be located (e.g., a link in a relevant project detail, a dedicated 'Labs' section).
        * A conceptual wireframe of the chosen pattern's UI (e.g., the modal layout with controls sidebar and chart area, or the expandable card structure).
Document your recommendation and pattern choice (if applicable) in 'P2_Live_API_Feature_Decision_And_Pattern.md'.

<definition_of_done>
* Clear recommendation on including/excluding the Live API feature for V1.
* If included, a specific integration pattern is chosen and justified.
* If included, wireframes are updated to show conceptual placement and layout of the feature.
* `P2_Live_API_Feature_Decision_And_Pattern.md` captures this.
</definition_of_done>
Why this is important: This decision impacts scope and development effort. Planning its integration now, if included, ensures it aligns aesthetically and functionally."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DRAFT_DECISION_DOCUMENT">P2_Live_API_Feature_Decision_And_Pattern.md</expected_artifact>
  <expected_artifact type="UPDATED_DRAFT_WIREFRAMES">(If feature included) Wireframes updated with conceptual Live API feature integration.</expected_artifact>
</task>

### Task 2.5: Discuss Performance Philosophy (If Not Done in Phase 1)
<task id="2.5_DiscussPerformance">
  <objective>To establish or refine the project's performance philosophy and set conceptual targets, ensuring design choices support these goals.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, let's ensure our design strategy aligns with strong performance. If not already created, or if refinement is needed based on chosen features, please draft/update 'P2_Performance_Philosophy_And_Targets_V1.md'.
This should outline:
1.  **Target User Experience:** Emphasize fast load times (e.g., LCP < 2.5s for key views), smooth animations (60fps), and responsive interactions as critical to the Palantir-level of quality.
2.  **Key Performance Indicators (KPIs):** Identify core metrics we'll track (e.g., Time to Interactive (TTI), First Input Delay (FID), Cumulative Layout Shift (CLS)).
3.  **Design Considerations for Performance:** How will choices regarding image optimization, animation complexity (even without 'reduce motion' as a blocker, purposefulness is key), interactive visualizations, and third-party libraries (like BlueprintJS or charting libraries) be balanced against these performance targets?
4.  **Mobile Performance:** Specific attention to performance on mobile devices for adaptive views.

<definition_of_done>
* Document outlines performance philosophy.
* Key performance metrics are identified.
* Design considerations impacting performance are noted.
* Mobile performance is specifically addressed.
</definition_of_done>
Why this is important: Embedding performance goals into the design phase ensures we make conscious choices that lead to a fast and fluid user experience, which is critical for a professional portfolio."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DRAFT_DOCUMENT">P2_Performance_Philosophy_And_Targets_V1.md</expected_artifact>
</task>

</tasks_for_claude>

## 4. Check-In & Progress Verification

<check_in_guidance>
* **Mid-Phase Check-In: Brand, Style Guide, and Motion Specs Review**
    <check_in_prompt>
        <instruction_for_claude>You will use this prompt to request artifacts from the Developer:</instruction_for_claude>
        <prompt_text>"Developer, please submit your draft 'P2_Brand_Personality_Statement_Sulayman_Bowles.md', the 'P2_Visual_Style_Guide_Palantir_Portfolio_V1.md', and the initial 'P2_Motion_Design_Detailed_Specs_V1.md'. I will review these for alignment with Sulayman's profile, the detailed Palantir aesthetic research, and the content strategy."</prompt_text>
    </check_in_prompt>
    <artifact_review_process>
      <step>Claude 4 receives and reviews the brand statement, style guide, and motion specs.</step>
      <step>Claude 4 verifies:
        * Brand personality aligns with Sulayman's unique strengths and the Palantir ethos.
        * Visual Style Guide accurately and comprehensively translates all specifications from `Project_Aesthetic_Guidelines_Palantir.md` (colors, typography, iconography, custom graphics concepts, component styling).
        * Motion Design Specs establish clear, Palantir-aligned principles for animations.</step>
      <step>
        <condition>If aligned:</condition>
        <claude_response>"The brand personality, visual style guide, and motion specs are excellent and provide a robust foundation for the design. Approved. Please proceed with the wireframes and the Live API feature decision."</claude_response>
      </step>
      <step>
        <condition>If revision needed:</condition>
        <claude_response>"Revisions needed:
        * For Brand Personality: [Specific feedback].
        * For Visual Style Guide: [e.g., 'The typography scale for H2 needs to be adjusted to 24px bold as per our Palantir guidelines.']
        * For Motion Design Specs: [e.g., 'Let's add a standard duration for hover feedback animations, perhaps 150ms.'].
        Please update."</claude_response>
      </step>
    </artifact_review_process>
* **End of Phase 2 Check-In: Full Design Strategy Approval**
    <check_in_prompt>
        <instruction_for_claude>You will use this prompt to request all final Phase 2 artifacts:</instruction_for_claude>
        <prompt_text>"Developer, please submit all finalized Phase 2 deliverables: 'P2_Brand_Personality_Statement_Sulayman_Bowles.md', 'P2_Visual_Style_Guide_Palantir_Portfolio_V1.md', 'P2_Motion_Design_Detailed_Specs_V1.md', 'P2_Key_Screens_Wireframes_LowFi_DesktopMobile.pdf', 'P2_Live_API_Feature_Decision_And_Pattern.md' (if applicable), and 'P2_Performance_Philosophy_And_Targets_V1.md'. We also need Sulayman's review and approval (`P2_Todo_ApproveDesigns`)."</prompt_text>
    </check_in_prompt>
    <artifact_review_process>
      <step>Claude 4 receives all final artifacts and confirmation of Sulayman's approval.</step>
      <step>Claude 4 verifies all documents are complete, consistent, and all decisions (like Live API feature integration pattern) are clearly documented and reflected in wireframes.</step>
      <step>
        <condition>If all aligned and stakeholder approved:</condition>
        <claude_response>"Phase 2 is complete. The Design Strategy is comprehensive, Palantir-aligned, and approved. We have a clear blueprint for both desktop and mobile experiences, including core interactivity and optional features. Excellent work. We are ready for Phase 3: Environment Setup."</claude_response>
      </step>
      <step>
        <condition>If minor revisions or pending approval:</condition>
        <claude_response>"Nearly there. Please address [Specific minor feedback] or [Confirm Sulayman's final approval on X]. Once resolved, Phase 2 will be complete."</claude_response>
      </step>
    </artifact_review_process>
</check_in_guidance>

## 5. Prompt-Engineering Best Practices for Claude 4 (Self-Audit)

<self_audit_checklist>
* **Comprehensive Research Synthesis:** Have I ensured my prompts guide the Developer to integrate details from *all* relevant research documents for this phase (`Project_Aesthetic_Guidelines_Palantir.md`, `Interactive_Narrative_Patterns_Research.md`, `Mobile_Adaptation_Palantir_Viz.md`, `Content_Strategy_Palantir_Portfolio.md`, `Custom_Graphic_Elements_For_Palantir_Aesthetic.md`, and `Live_API_Feature_Integration_Patterns.md`)?
* **Guiding Strategic Decisions:** For choices like the Live API feature pattern, did I provide the Developer with clear criteria (from the research) to make an informed recommendation, rather than just asking for a choice?
* **Mobile-First Mentality in Wireframing:** Am I emphasizing that mobile adaptation is not an afterthought but a core part of the wireframing process for key interactive elements?
* **Clarity of Deliverables:** Are the expected artifacts for this phase clearly defined with IDs and descriptions, ensuring the Developer knows exactly what to produce?
* **Reinforcing Performance by Design:** Does my guidance on feature complexity and visual richness implicitly or explicitly connect back to the performance philosophy defined?
</self_audit_checklist>

</claude_guide_phase>
