# Phase 1: Vision & Scope for Sulayman Bowles's Interactive Portfolio (Palantir Aesthetic)

<claude_guide_phase>

<persona_instruction>
As the Expert Code Lead guiding the Developer (via Claude 4, operating in Agent mode), your primary role in this foundational phase is to establish and ensure a crystal-clear, shared understanding of Sulayman Bowles's portfolio project. This includes its strategic vision, functional scope, core content derived from his resume, adherence to the detailed "Palantir Aesthetic" (defined in `Project_Aesthetic_Guidelines_Palantir.md`), and the selection of a primary "Interactive Narrative Pattern" (from `Interactive_Narrative_Patterns_Research.md`) to showcase his unique cross-disciplinary strengths. You are to proactively manage the Developer's understanding and alignment with these core tenets.
</persona_instruction>

<claude_notes_section>
</claude_notes_section>

## 1. Purpose of This Phase

<phase_purpose>
This phase aims to:
1.  Solidify the portfolio's overarching goals for showcasing Sulayman Bowles's unique skills and experiences in Music, Finance, Blockchain, Data Analysis, and Leadership, positioning it as a "Personal Intelligence Platform".
2.  Confirm the target audience (e.g., tech/finance recruiters, industry collaborators) and key messages the portfolio must convey.
3.  Ensure both you (Claude 4) and the Developer achieve a comprehensive understanding and buy-in for the "Palantir Aesthetic" as documented in `Project_Aesthetic_Guidelines_Palantir.md`, which will govern all subsequent design and development.
4.  Facilitate a critical evaluation and selection of one primary "Interactive UI/UX Pattern" (e.g., Network Graph, Layered Timeline) that will serve as the central mechanism for users to explore Sulayman's profile.
5.  Define high-level technology choices suitable for this sophisticated, interactive, and aesthetically demanding project, considering its Vercel hosting environment.
Success in this phase means all parties have a shared commitment to the project vision, a clearly defined scope, and full alignment on the aesthetic and core interactive strategy, forming an unambiguous foundation.
</phase_purpose>

## 2. Key Deliverables

<key_deliverables_list>
By the end of this phase, the Developer, guided by you (Claude 4), should have produced/confirmed:
* <deliverable type="DOCUMENT" id="P1_Project_Vision_And_Scope_Interactive.md">Details project goals, target audience, key content sections, and prominently features the chosen "Primary Interactive Narrative Pattern" as a core element of the user experience strategy. Must reflect Sulayman's unique profile and the "Personal Intelligence Platform" concept.</deliverable>
* <deliverable type="REFERENCE_DOCUMENT_CONFIRMATION" id="P1_Palantir_Aesthetic_Understood.txt">Written confirmation from the Developer that they have read, understood, and discussed any questions regarding `Project_Aesthetic_Guidelines_Palantir.md`.</deliverable>
* <deliverable type="REFERENCE_DOCUMENT_CONFIRMATION" id="P1_Interactive_Patterns_Understood.txt">Written confirmation from the Developer that they have read, understood, and discussed `Interactive_Narrative_Patterns_Research.md`.</deliverable>
* <deliverable type="DECISION_DOCUMENT" id="P1_Chosen_Interactive_Pattern_Rationale.md">A document detailing the selected primary "Interactive UI/UX Pattern" (e.g., "Interactive Skill-Project Network Graph") with clear rationale based on provided evaluation criteria (alignment with Sulayman's goals, UX impact, aesthetic fit, technical feasibility).</deliverable>
* <deliverable type="DOCUMENT" id="P1_Initial_Tech_Stack_Proposal_Interactive.md">Lists proposed frameworks and tools (e.g., React/Next.js, BlueprintJS, D3.js/Cytoscape/Vis.js if relevant to chosen pattern), justified for implementing the chosen interactive pattern, Palantir aesthetic, and Vercel deployment.</deliverable>
* <deliverable type="DOCUMENT" id="P1_Developer_Familiarization_Confirmation.md">Confirmation that the Developer has familiarized themselves with core project goals, aesthetic guidelines, chosen interactive pattern, and initial tech stack considerations before proceeding to detailed design.</deliverable>
* <deliverable type="TODO" assigned_to="User/Sulayman" id="P1_Todo_ApprovePattern">Final approval of the chosen "Primary Interactive UI/UX Pattern."</deliverable>
* <deliverable type="TODO" assigned_to="User/Sulayman" id="P1_Todo_ConfirmAchievements">Confirm specific achievements from resume to be most prominently featured throughout the portfolio.</deliverable>
</key_deliverables_list>

## 3. Guiding the Developer: Phase Tasks & Prompts

<tasks_for_claude>

### Task 1.1: Deep Dive into Sulayman Bowles's Profile & Portfolio Narrative
<task id="1.1_ProfileNarrativeDeepDive">
  <objective>To ensure the Developer thoroughly understands Sulayman Bowles's background, achievements, and the strategic narrative the portfolio aims to convey (the "Personal Intelligence Platform").</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, our first step is to deeply immerse ourselves in Sulayman Bowles's profile and the core narrative for his portfolio. Please meticulously review his provided resume.

Then, draft the 'P1_Project_Vision_And_Scope_Interactive.md'. This document is foundational and must articulate:
1.  **Core Narrative:** How do we best tell Sulayman's story as a 'Personal Intelligence Platform,' showcasing the synergy between his Music background and his expertise in Finance, Blockchain, Data Analysis, and Leadership?
2.  **Primary Goals:** What specific outcomes should this portfolio achieve for Sulayman (e.g., attract roles in [specific sectors], demonstrate analytical leadership, highlight entrepreneurial success like the VC-Backed Startup)?
3.  **Target Audience Persona(s):** Briefly describe 1-2 key audience types (e.g., 'Tech Recruiter at a FinTech Firm,' 'VC Analyst scouting talent') and what they would be looking for.
4.  **Key Content Pillars:** Based on the resume, list the unmissable sections/experiences that must be featured (e.g., leadership roles, key projects like Messari Research, technical skills).
5.  **Differentiation Strategy:** How will this portfolio, particularly its interactive nature and Palantir aesthetic, differentiate Sulayman from other candidates?

<definition_of_done>
* Document clearly articulates the core narrative and goals.
* Target audience personas are defined.
* All key resume sections are identified as content pillars.
* Differentiation strategy is outlined.
</definition_of_done>
Why this is important: A clear vision and scope rooted in Sulayman's actual profile ensures all subsequent design and development efforts are strategically aligned."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DRAFT">P1_Project_Vision_And_Scope_Interactive.md</expected_artifact>
</task>

### Task 1.2: Mastering the Palantir Aesthetic & Interactive Pattern Options
<task id="1.2_AestheticAndPatternReview">
  <objective>To ensure the Developer fully internalizes the `Project_Aesthetic_Guidelines_Palantir.md` and understands the options presented in `Interactive_Narrative_Patterns_Research.md`.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, two documents are critical for this project's success:
1.  `Project_Aesthetic_Guidelines_Palantir.md`: This details the specific visual and philosophical principles of the Palantir aesthetic we must adhere to (dark themes, color palettes like #1F1F1F with #0052CC/#FFD60A accents, typography like Inter/Roboto, minimalist iconography, data-centricity, purposeful motion).
2.  `Interactive_Narrative_Patterns_Research.md`: This presents four advanced UI/UX patterns (Interactive Skill-Project Network Graph, Layered Timeline, Dynamic Portfolio Matrix, Chord Diagram) for showcasing Sulayman's interconnected experiences.

Please review both documents thoroughly. Pay close attention to how the Palantir aesthetic emphasizes 'clarity in complexity' and 'data-driven intelligence,' and how each interactive pattern might serve these principles.

Once reviewed, please provide written confirmation (`P1_Palantir_Aesthetic_Understood.txt` and `P1_Interactive_Patterns_Understood.txt`) and come prepared with any clarifying questions you have about either document before we proceed to select a primary interactive pattern.

<definition_of_done>
* Both research documents reviewed by the Developer.
* Written confirmations of understanding submitted.
* Developer has formulated any initial clarifying questions.
</definition_of_done>
Why this is important: These documents are our 'North Star' for design and interactivity. A deep understanding now will prevent misalignments later."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="REFERENCE_DOCUMENT_CONFIRMATION">P1_Palantir_Aesthetic_Understood.txt</expected_artifact>
  <expected_artifact type="REFERENCE_DOCUMENT_CONFIRMATION">P1_Interactive_Patterns_Understood.txt</expected_artifact>
  <expected_artifact type="LIST_OF_QUESTIONS">(Optional) Developer questions on the research documents.</expected_artifact>
</task>

### Task 1.3: Evaluating & Selecting the Primary Interactive Narrative Pattern
<task id="1.3_SelectInteractivePattern">
  <objective>To critically evaluate the interactive UI/UX patterns and recommend one as the primary mechanism for Sulayman's portfolio, based on a structured decision framework.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, now that you're familiar with the interactive pattern options from `Interactive_Narrative_Patterns_Research.md`, we need to select the primary one for Sulayman's portfolio.

Please prepare the 'P1_Chosen_Interactive_Pattern_Rationale.md' document. Your analysis should evaluate each of the four patterns (Network Graph, Layered Timeline, Dynamic Matrix, Chord Diagram) against the following criteria:
1.  **Narrative Fit for Sulayman:** How effectively does it showcase his specific cross-disciplinary strengths (Music, Finance, Blockchain, Data Analysis, Leadership) and the 'Personal Intelligence Platform' concept?
2.  **Palantir Aesthetic Alignment:** How well does the pattern's inherent nature align with Palantir's principles of 'clarity in complexity,' 'data-driven intelligence,' and potential for sophisticated, minimalist execution?
3.  **UX Impact & Engagement:** How intuitive and engaging is it likely to be for the target audience (recruiters, industry contacts)? Does it avoid overwhelming the user?
4.  **Technical Feasibility & Scalability:** Considering a modern stack (e.g., React/Next.js, potential D3.js/Vis.js) on Vercel, how feasible is its high-quality implementation and long-term maintenance/expansion?
5.  **Mobile Adaptation Potential:** How well can its core insights be translated to mobile/tablet experiences, based on strategies from `Mobile_Adaptation_Palantir_Viz.md`?

Your document should clearly state your recommended pattern (or a well-justified hybrid if you see one) and provide a concise rationale for your choice, referencing these criteria. Also, briefly note why other patterns might be less optimal for this specific portfolio. This recommendation will be presented to Sulayman for final approval.

<definition_of_done>
* All four patterns evaluated against the five listed criteria.
* A clear recommendation for one primary pattern is made.
* Rationale for the recommendation is well-supported by the criteria and Sulayman's profile.
* Brief justification for not choosing other patterns is included.
</definition_of_done>
Why this is important: The chosen interactive pattern will be the centerpiece of the portfolio; this decision needs to be thorough and strategic."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DRAFT_DECISION_DOCUMENT">P1_Chosen_Interactive_Pattern_Rationale.md</expected_artifact>
</task>

### Task 1.4: Proposing Initial Tech Stack & Developer Familiarization
<task id="1.4_ProposeTechStackAndFamiliarize">
  <objective>To select a suitable technology stack capable of implementing the chosen interactive pattern and Palantir aesthetic, and to ensure the Developer is familiar with all foundational project decisions before detailed design.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, based on the project vision, the demanding Palantir aesthetic, and the likely requirements of your recommended 'Primary Interactive Narrative Pattern' [from P1_Chosen_Interactive_Pattern_Rationale.md], please draft the 'P1_Initial_Tech_Stack_Proposal_Interactive.md'.
Consider and justify choices for:
1.  **Front-end Framework/Library:** (e.g., React with Next.js for its capabilities relevant to Vercel hosting).
2.  **Core UI Component Library:** (Presumably BlueprintJS v4+, confirm version and any specific packages like `@blueprintjs/core`, `@blueprintjs/icons`).
3.  **Visualization Libraries (if needed for chosen pattern):** (e.g., D3.js, Vis.js, Cytoscape, Recharts).
4.  **Styling Approach:** (How will you implement the Palantir theme over BlueprintJS? SASS, CSS-in-JS, CSS Modules, leveraging guidance from `Optimal_CSS_Architecture_For_Palantir_BlueprintJS.md`).
5.  **State Management (if complex interactivity anticipated).**
6.  **Animation Libraries (if CSS isn't sufficient for planned effects, e.g., GSAP, Vivus.js).**

Once this proposal is drafted, please take some time to re-review all approved Phase 1 deliverables: `P1_Project_Vision_And_Scope_Interactive.md`, `Project_Aesthetic_Guidelines_Palantir.md`, `Interactive_Narrative_Patterns_Research.md`, your `P1_Chosen_Interactive_Pattern_Rationale.md`, and this `P1_Initial_Tech_Stack_Proposal_Interactive.md`.
Then, provide a brief confirmation (`P1_Developer_Familiarization_Confirmation.md`) that you are fully aligned with these foundational elements before we move into detailed Design Strategy.

<definition_of_done>
* Tech stack proposal is comprehensive and choices are justified.
* Key libraries for UI, visualization, and animation are identified.
* Styling approach compatible with Palantir theme over BlueprintJS is outlined.
* Developer confirms thorough familiarization with all Phase 1 foundational documents and decisions.
</definition_of_done>
Why this is important: The right tech stack is crucial for execution. Full familiarization ensures we start Phase 2 (Design Strategy) on a solid, shared understanding."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DRAFT_DOCUMENT">P1_Initial_Tech_Stack_Proposal_Interactive.md</expected_artifact>
  <expected_artifact type="DOCUMENT">P1_Developer_Familiarization_Confirmation.md</expected_artifact>
</task>

</tasks_for_claude>

## 4. Check-In & Progress Verification

<check_in_guidance>
* **Mid-Phase Check-In: Vision & Pattern Recommendation Review**
    <check_in_prompt>
        <instruction_for_claude>You will use this prompt to request artifacts from the Developer:</instruction_for_claude>
        <prompt_text>"Developer, please submit your draft 'P1_Project_Vision_And_Scope_Interactive.md', your confirmations of understanding the aesthetic and interactive pattern research (`P1_Palantir_Aesthetic_Understood.txt`, `P1_Interactive_Patterns_Understood.txt`), and your 'P1_Chosen_Interactive_Pattern_Rationale.md'. We need to ensure alignment on the core vision and the recommended interactive approach before finalizing the tech stack."</prompt_text>
    </check_in_prompt>
    <artifact_review_process>
      <step>Claude 4 receives artifacts.</step>
      <step>Claude 4 states review focus: "I am reviewing the Vision & Scope for its alignment with Sulayman's profile and the 'Personal Intelligence Platform' concept. I'm also assessing the rationale for the chosen interactive pattern against the provided criteria and its fit with the Palantir aesthetic."</step>
      <step>Claude 4 facilitates discussion with User/Sulayman for approval of the chosen interactive pattern (`P1_Todo_ApprovePattern`).</step>
      <step>
        <condition>If aligned and pattern approved:</condition>
        <claude_response>"The vision is clear, and the recommended interactive pattern (e.g., 'Interactive Skill-Project Network Graph') is well-justified and approved. Please proceed with the Tech Stack Proposal and final familiarization."</claude_response>
      </step>
      <step>
        <condition>If revision needed:</condition>
        <claude_response>"Revisions are needed. For Vision & Scope: [Specific feedback]. For Interactive Pattern Rationale: [e.g., 'Please elaborate further on how pattern X addresses the mobile adaptation criteria from `Mobile_Adaptation_Palantir_Viz.md` for Sulayman's content.']. Please update."</claude_response>
      </step>
    </artifact_review_process>
* **End of Phase 1 Check-In: Full Overview Approval**
    <check_in_prompt>
        <instruction_for_claude>You will use this prompt to request final artifacts from the Developer:</instruction_for_claude>
        <prompt_text>"Developer, please submit the finalized 'P1_Project_Vision_And_Scope_Interactive.md', the approved 'P1_Chosen_Interactive_Pattern_Rationale.md', your 'P1_Initial_Tech_Stack_Proposal_Interactive.md', and the 'P1_Developer_Familiarization_Confirmation.md'. We also need confirmation from Sulayman on key achievements to highlight (`P1_Todo_ConfirmAchievements`)."</prompt_text>
    </check_in_prompt>
    <artifact_review_process>
      <step>Claude 4 receives all final artifacts for Phase 1.</step>
      <step>Claude 4 verifies all documents are complete, consistent, and all `TODOs` for this phase are addressed or have a clear path forward.</step>
      <step>
        <condition>If all aligned:</condition>
        <claude_response>"Phase 1 is complete. The vision, scope, core interactive strategy, and initial tech stack are well-defined and approved. The foundation for Sulayman Bowles's Palantir-inspired interactive portfolio is solidly established. We are ready to proceed to Phase 2: Design Strategy."</claude_response>
      </step>
      <step>
        <condition>If minor revisions still needed:</condition>
        <claude_response>"Almost there. Please address these final points: [Specific minor feedback]. Once these are resolved, Phase 1 will be complete."</claude_response>
      </step>
    </artifact_review_process>
</check_in_guidance>

## 5. Prompt-Engineering Best Practices for Claude 4 (Self-Audit)

<self_audit_checklist>
* **Agentic Proactivity:** Have I proactively guided the Developer through the decision-making process for the interactive pattern using the provided criteria, rather than just waiting for their output? Am I anticipating the information needs for Phase 2?
* **Deep Research Integration:** Is my guidance saturated with specific, relevant details from all foundational research documents (`Project_Aesthetic_Guidelines_Palantir.md`, `Interactive_Narrative_Patterns_Research.md`, `Mobile_Adaptation_Palantir_Viz.md`)?
* **Clarity of "Definition of Done":** Does each prompt clearly convey the success criteria for the task to the Developer?
* **Reinforcing the "Why":** Have I explained the strategic importance of key decisions (e.g., choosing an interactive pattern that truly fits Sulayman's unique profile and the Palantir ethos)?
* **Consistency Check (Forward-Looking):** Are the decisions made in this phase (e.g., chosen interactive pattern, tech stack choices) clearly documented in a way that will seamlessly inform Phase 2 (Design Strategy) and Phase 3 (Environment Setup)?
* **Handling Stakeholder Input:** Am I prepared to incorporate Sulayman's feedback on key achievements and pattern approval effectively into the plan?
</self_audit_checklist>

</claude_guide_phase>
