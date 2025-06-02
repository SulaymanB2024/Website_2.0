# Phase 6: Interactivity Strategy for Sulayman Bowles's Portfolio (Palantir Aesthetic)

<claude_guide_phase>

<persona_instruction>
As the Expert Code Lead guiding the Developer (via Claude 4, operating in Agent mode), your primary objective in this phase is to define and oversee the implementation of all interactive behaviors and animations for Sulayman Bowles's portfolio. This includes bringing to life the "Primary Interactive Narrative Pattern" (e.g., Network Graph from `P1_Chosen_Interactive_Pattern_Rationale.md`), its mobile adaptations, any optional features like the "Live Technical Analysis API" module, and all general UI micro-interactions. All interactivity must be purposeful, performant, strictly adhere to the Palantir aesthetic's minimalist and utilitarian motion design principles (as defined in `P2_Motion_Design_Detailed_Specs_V1.md`), and be fully accessible. You are to ensure that every animation and interaction enhances clarity, provides meaningful feedback, and contributes to the overall sophisticated user experience.
</persona_instruction>

<claude_notes_section>
</claude_notes_section>

## 1. Purpose of This Phase

<phase_purpose>
This phase aims to:
1.  Implement all defined animations and micro-interactions for global elements (page load, navigation, header, buttons, icons), ensuring they are subtle, purposeful, and Palantir-aligned.
2.  Fully realize the interactive functionality of the chosen "Primary Interactive Narrative Pattern" (e.g., Network Graph), including node interactions, filtering, detail reveals (Side Drawer Panel), and its specific mobile adaptation behaviors.
3.  Implement animations for data visualization elements, such as "Data Flow" on graph edges, chart data materialization, and animated "Stat Callouts".
4.  Develop the interactivity for any approved optional features, such as the "Live Technical Analysis API" module, including its user controls and real-time data update displays.
5.  Ensure all interactive elements are highly performant, fully keyboard accessible, and provide appropriate ARIA attributes for assistive technologies.
6.  Implement and thoroughly test the "Reduce Motion" preference across all animations.
Success means a portfolio that feels alive, responsive, and intelligent, where every interaction is intuitive and enhances the user's understanding of Sulayman's capabilities, all while maintaining the sophisticated Palantir aesthetic.
</phase_purpose>

## 2. Key Deliverables

<key_deliverables_list>
By the end of this phase, the Developer, guided by you (Claude 4), should have:
* <deliverable type="FEATURE_IMPLEMENTATION" id="P6_Global_Animations_Implemented">All global animations (page load, monogram reveal, navigation transitions, button/icon micro-interactions) implemented as per `P2_Motion_Design_Detailed_Specs_V1.md`.</deliverable>
* <deliverable type="FEATURE_IMPLEMENTATION" id="P6_Primary_Interactive_Narrative_Pattern_Fully_Interactive">The chosen "Primary Interactive Narrative Pattern" (e.g., Network Graph) is fully interactive on desktop, including node hover/click states, "Data Flow" animations, filter functionality, detail panel reveals, and any "Guided Discovery Path" interactions.</deliverable>
* <deliverable type="FEATURE_IMPLEMENTATION" id="P6_Mobile_Adaptation_Interactive_Narrative_Interactive">The mobile/tablet adaptation of the "Primary Interactive Narrative Pattern" (e.g., Master-Detail List for Network Graph) is fully interactive with touch-optimized behaviors.</deliverable>
* <deliverable type="FEATURE_IMPLEMENTATION" id="P6_Data_Viz_And_Content_Reveal_Animations_Implemented">Animations for data visualization elements (chart loading, "Stat Callout" count-ups) and content block reveals (sequential fade-ins) are implemented.</deliverable>
* <deliverable type="FEATURE_IMPLEMENTATION_CONDITIONAL" id="P6_Live_API_Module_Interactive">(If approved in Phase 2) The "Live Technical Analysis API" module is fully interactive, including user controls, chart updates, and data feedback mechanisms.</deliverable>
* <deliverable type="ACCESSIBILITY_FEATURE" id="P6_Reduce_Motion_Functionality_Implemented">A global "Reduce Motion" setting (respecting OS preference and/or site toggle) is implemented and demonstrably disables or minimizes all non-essential animations site-wide.</deliverable>
* <deliverable type="DOCUMENTATION_UPDATE" id="P6_Motion_Design_Specs_Refined.md">(If necessary) Updates or refinements to `P2_Motion_Design_Detailed_Specs_V1.md` based on implementation experience.</deliverable>
* <deliverable type="DEMO_VIDEO_COLLECTION" id="P6_Interactivity_Demos.zip">A collection of short screen recordings demonstrating all key implemented interactive features and animations on desktop and mobile.</deliverable>
* <deliverable type="TODO" assigned_to="Developer" id="P6_Todo_PerformanceProfileAnimations">Developer to perform initial performance profiling of key animations and interactive components using browser developer tools.</deliverable>
</key_deliverables_list>

## 3. Guiding the Developer: Phase Tasks & Prompts

<tasks_for_claude>

### Task 6.1: Implementing Global & UI Element Micro-Interactions
<task id="6.1_ImplementGlobalMicroInteractions">
  <objective>To implement site-wide entry animations, navigation transitions, and standard micro-interactions for common UI elements, based on `P2_Motion_Design_Detailed_Specs_V1.md`.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, let's bring the foundational elements of the site to life with purposeful micro-interactions and animations, adhering to the parameters in `P2_Motion_Design_Detailed_Specs_V1.md`:
1.  **Entry Animations:**
    * Implement the 'SB' monogram reveal in the header (e.g., SVG lines drawing over 300ms).
    * Implement the staggered fade-in/translate-up for the homepage tagline (50ms delay, 150ms duration per word/line).
2.  **Navigation & Page Transitions:**
    * Implement the smooth transition for the active link indicator in the main navigation (slide/resize over 200ms).
    * Implement the chosen site-wide page transition effect (e.g., 'Data Grid Overlay' fade over 300ms). This must be tied to your routing solution.
3.  **UI Element Micro-interactions:**
    * Style BlueprintJS `Button` press states (1px downward/inward shift, 100ms) as defined.
    * Implement smooth transitions (150ms) for interactive icon hovers/activations (rotation for chevrons, scale/fill for others).
    * Ensure filter control applications (e.g., BlueprintJS `Checkbox`) have a brief accent color flash or checkmark animation (150ms).
4.  **Loading States:** Implement the 'shimmer' animation for BlueprintJS `Skeleton` components (1.5s gradient wipe, linear, infinite).
5.  **Tooltip/Popover Animations:** Ensure BlueprintJS `Popover`/`Tooltip` transitions are quick (100-150ms fade-in/scale-up, ease-out).
6.  **"Reduce Motion" Foundation:** Ensure all these animations are implemented in a way that they can be disabled or significantly reduced by a global 'Reduce Motion' CSS class or JavaScript flag.

<definition_of_done>
* All listed global and UI element animations are implemented as specified.
* Timings, easing, and visual effects match `P2_Motion_Design_Detailed_Specs_V1.md`.
* Animations are smooth and performant in initial tests.
* All animations are designed to respect a future "Reduce Motion" toggle.
</definition_of_done>
Why this is important: These subtle interactions contribute significantly to the perceived quality, responsiveness, and sophisticated feel of the Palantir aesthetic."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DEMO_VIDEO_OR_STORYBOOK">Demonstration of global animations and UI micro-interactions.</expected_artifact>
</task>

### Task 6.2: Implementing Interactivity for the "Primary Interactive Narrative Pattern" (Desktop)
<task id="6.2_ImplementDesktopInteractiveNarrative">
  <objective>To fully implement all interactive features of the chosen "Primary Interactive Narrative Pattern" (e.g., Network Graph) for desktop viewports, including data binding, visual feedback, and detail reveals.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, this is a core task: bringing the desktop version of our chosen 'Primary Interactive Narrative Pattern' (e.g., 'Interactive Skill-Project Network Graph' from `P1_Chosen_Interactive_Pattern_Rationale.md`) to life.
1.  **Data Binding:** Connect the main interactive component (e.g., `InteractiveProfileExplorer.js`) to the `P4_Initial_Portfolio_Content_Sample.json` data. Ensure nodes (Domains, Projects, Skills) and their relationships are correctly rendered by `DesktopGraphView.js` (or equivalent).
2.  **Node Hover/Focus States:** Implement hover effects (e.g., node glow, connection highlight, dimming of unrelated nodes) and keyboard focus states (animated focus indicator) as defined in `P2_Motion_Design_Detailed_Specs_V1.md`. Ensure `aria-label`s are dynamically set for nodes.
3.  **"Data Flow" Animation:** Implement the subtle 'Data Flow' animation on graph edges when hovering a domain or applying filters (e.g., 500ms accent-colored pulse).
4.  **Detail Reveal (Side Drawer/Modal):**
    * On node click, implement the smooth opening of the `DetailSideDrawer.js` (or modal).
    * Populate the drawer with content from the selected node's data, structured per the 'Problem → Approach → Outcome → Metrics' format.
    * Implement "Stat Callout" number animations (count-up) and associated glyph animations.
    * Implement the "Focus Scope" effect (blur/desaturate main graph) when the drawer is open.
5.  **Filter Functionality:** Implement interactivity for the `FilterPanel.js`. Applying filters should dynamically update the graph with smooth transitions (e.g., nodes/edges fading in/out, layout re-settling gently).
6.  **Legend Interactivity:** If the legend is interactive (e.g., clicking a domain highlights it on the graph), implement this.
7.  **"Guided Discovery Paths" (If planned):** Implement the UI for selecting paths and the corresponding graph highlighting/annotation reveal sequence.
8.  **Keyboard Navigation:** Ensure the entire graph (nodes, interactive legend/filter elements) is navigable and operable via keyboard.

<definition_of_done>
* Interactive pattern correctly renders and updates based on sample data.
* All defined hover, focus, and selection interactions are implemented with specified animations.
* Detail reveal mechanism (drawer/modal) is fully functional and populated with structured content.
* Filtering and legend interactions work as designed.
* "Guided Discovery Paths" (if applicable) are functional.
* All interactions are keyboard accessible and performant on desktop.
</definition_of_done>
Why this is important: This central interactive feature is key to Sulayman's unique portfolio presentation. Its flawless execution is paramount."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DEMO_VIDEO_OR_STORYBOOK">Demonstration of the fully interactive desktop version of the Primary Interactive Narrative Pattern.</expected_artifact>
</task>

### Task 6.3: Implementing Interactivity for Mobile/Tablet Adaptations of the Narrative Pattern
<task id="6.3_ImplementMobileInteractiveNarrative">
  <objective>To implement all interactive features of the chosen mobile/tablet adaptation for the "Primary Interactive Narrative Pattern" (e.g., Master-Detail List or Filtered Accordion for a Network Graph).</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, now adapt the interactivity of the 'Primary Interactive Narrative Pattern' for mobile/tablet, using the chosen adaptation strategy from `Mobile_Adaptation_Palantir_Viz.md` (e.g., 'Master-Detail List + Mini-Map' or 'Filtered Accordion').
1.  **Implement Mobile UI Pattern:** Build the components for the mobile adaptation (e.g., `MobileListView.js`, `DomainMasterListItem.js`, `ProjectCard_Mobile.js`, `AccordionSection_Mobile.js`).
2.  **Touch-Optimized Interactions:**
    * Ensure tap interactions are responsive for list item selection, accordion expansion, etc.
    * Implement any specified swipe gestures (e.g., for navigating between related items in the Filtered Accordion pattern).
    * Convert hover-based detail reveals (like tooltips) to tap-based reveals (e.g., opening a small BlueprintJS `Popover` or a bottom sheet for details).
3.  **Data Binding & Content Display:** Ensure mobile components correctly display data from `P4_Initial_Portfolio_Content_Sample.json`, formatted for smaller screens but still adhering to the Content Strategy.
4.  **Filter/Sort Functionality (Mobile):** Implement mobile-friendly filter controls (e.g., filter chips, dropdowns in a sticky header/footer).
5.  **Performance:** Pay close attention to performance on mobile devices, especially for list rendering (consider virtualization for long lists) and transitions.
6.  **Accessibility:** Ensure all mobile interactive elements are keyboard accessible (if a physical keyboard is connected) and screen-reader friendly.

<definition_of_done>
* Chosen mobile adaptation pattern for the interactive narrative is fully implemented and functional.
* Interactions are touch-optimized and performant on target mobile/tablet viewports.
* Data is correctly displayed and formatted for smaller screens.
* Mobile-specific filter/sort controls are implemented.
* Accessibility for mobile interactions is verified.
</definition_of_done>
Why this is important: A seamless and intuitive mobile experience is critical. The interactive narrative must be just as compelling on smaller devices."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DEMO_VIDEO_OR_SCREENSHOTS">Demonstration of the interactive mobile/tablet adaptation of the Primary Interactive Narrative Pattern.</expected_artifact>
</task>

### Task 6.4 (Conditional): Implementing Interactivity for "Live Technical Analysis API" Module
<task id="6.4_ImplementLiveAPIInteractivityConditional">
  <objective>If the "Live Technical Analysis API" feature is approved (`P2_Live_API_Feature_Decision_And_Pattern.md`), to implement all its interactive functionalities, including user controls, real-time chart updates, and data feedback mechanisms, as per `Live_API_Feature_Integration_Patterns.md`.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer, ONLY if the Live API Feature was approved:</instruction_for_claude>
    <prompt_text>
"Developer, as we are implementing the 'Live Technical Analysis API' module using the [Insert Chosen Pattern, e.g., Modal/Overlay], let's build its interactivity:
1.  **API Connection & Initial Data Load:** Implement `APIConnectorService.js` to fetch initial data from the specified API (from `Live_API_Source_And_Scope.md`). Display loading states using BlueprintJS `Spinner` with the shimmer animation. Handle API errors gracefully with styled `Callout` messages.
2.  **Chart Rendering & Theming:** Ensure `ChartDisplayComponent.js` renders the chart with data, styled according to Palantir guidelines (colors, fonts, gridlines).
3.  **Control Panel Functionality (`IndicatorControlsPanel.js`):**
    * Implement functionality for selecting assets, timeframes (BlueprintJS `ButtonGroup`), and adding/removing/configuring technical indicators (BlueprintJS `Select`/`MultiSelect`).
    * Ensure the chart updates dynamically and performantly in response to these controls.
4.  **Real-Time Data Updates:** Implement polling or WebSocket connection (if API supports) for live data updates. Animate chart updates smoothly (e.g., data point materialization). Update the 'Last Updated' timestamp and 'Data Pulse' effect.
5.  **Interactive Chart Tooltips:** Implement custom tooltips (e.g., styled BlueprintJS `Popover`) that display precise values on chart hover.
6.  **Keyboard Accessibility:** Ensure all controls and chart interactions (if feasible with charting library) are keyboard accessible.

<definition_of_done>
* Live API module fetches and displays initial data correctly.
* All user controls are functional and dynamically update the chart.
* Real-time data updates are implemented and visually indicated.
* Interactive tooltips are functional.
* Error states and loading states are handled gracefully.
* Module is keyboard accessible and performant.
</definition_of_done>
Why this is important: This feature, if included, is a direct demonstration of Sulayman's technical and analytical skills; its interactivity must be flawless."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="FEATURE_DEMO_GIF_OR_VIDEO">(Conditional) `P6_Live_API_Module_Interactive.gif` - Demonstration of the fully interactive Live API module.</expected_artifact>
</task>

### Task 6.5: Implementing Content Reveal & Other Specified Animations
<task id="6.5_ImplementContentAndMiscAnimations">
  <objective>To implement remaining animations such as data/stat callout animations, sequential content block reveals, animated section dividers, and any other subtle effects defined in `P2_Motion_Design_Detailed_Specs_V1.md`.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, let's implement the remaining content-focused and subtle animations, guided by `P2_Motion_Design_Detailed_Specs_V1.md` and our discussions on enhancing graphics/effects:
1.  **Animated "Stat Callouts":** Implement the number count-up animation and associated glyph animation for stat callouts when they become visible.
2.  **Sequential Content Block Reveals:** For structured text (e.g., "Problem → Approach → Outcome" in case studies or detail drawers), implement the staggered fade-in/translate-up effect for blocks as they scroll into view or upon container reveal.
3.  **Animated Section Dividers:** If custom SVG section dividers are used, implement their "construction" or "draw-in" animation on scroll (e.g., using Vivus.js or GSAP DrawSVGPlugin).
4.  **Subtle Parallax on Backgrounds (If Approved & Performant):** Implement the conservative parallax effect for designated background graphics, ensuring it's minimal and tied to the 'Reduce Motion' setting.
5.  **"Insight Unlocked" Cue (If data model supports from Phase 4):** Implement the subtle animation for this conditional cue on the Network Graph.
<definition_of_done>
* Stat callout animations are implemented.
* Sequential content block reveals are functional.
* Animated section dividers (if any) are implemented.
* Any approved subtle parallax or conditional "Insight Unlocked" cues are implemented.
* All animations are smooth, purposeful, and respect 'Reduce Motion'.
</definition_of_done>
Why this is important: These refined animations contribute to the overall polish and sophisticated feel of the portfolio, enhancing the communication of key information."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DEMO_VIDEO_OR_SCREENSHOTS">`P6_Data_Viz_And_Content_Reveal_Animations_Implemented` - Demonstration of these various content and graphical animations.</expected_artifact>
</task>

### Task 6.6: Implementing and Verifying "Reduce Motion" Functionality
<task id="6.6_ImplementReduceMotion">
  <objective>To ensure a global "Reduce Motion" preference (OS-level and/or site toggle) effectively disables or minimizes all non-essential animations across the entire website.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, a critical accessibility feature is robust 'Reduce Motion' support:
1.  **Implement Detection:** Ensure your JavaScript and/or CSS can detect the `prefers-reduced-motion` media query.
2.  **Implement Site Toggle (If planned in Header - Accessibility Settings):** If a site-specific toggle is planned, ensure it sets a global class (e.g., `.reduce-motion-active`) or state that overrides the OS preference if explicitly set by the user.
3.  **Apply to ALL Animations:** Go through every animation and transition implemented in this phase (entry animations, navigation, micro-interactions, graph animations, data reveals, scroll effects, etc.). Ensure each one is either:
    * Completely disabled when 'Reduce Motion' is active.
    * Reduced to a very simple, essential fade (e.g., 150ms opacity transition) if some minimal feedback is still necessary for usability.
    * Purposeful animations critical for understanding state changes (like a tab selection indicator moving) might be preserved but significantly sped up or simplified.
4.  **Thorough Testing:** Test the site with 'Reduce Motion' enabled (both via OS and site toggle if applicable) to confirm all non-essential motion is correctly suppressed.

<definition_of_done>
* `prefers-reduced-motion` media query is respected.
* Site-specific 'Reduce Motion' toggle (if any) functions correctly and overrides OS preference if set.
* All non-essential animations and transitions across the site are demonstrably disabled or minimized when 'Reduce Motion' is active.
* Essential feedback animations (if any remain) are minimal and non-disruptive.
</definition_of_done>
Why this is important: This is a crucial accessibility requirement, ensuring users sensitive to motion can use the portfolio comfortably and without issues like vertigo or distraction."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DEMO_VIDEO_OR_CONFIRMATION">`P6_Reduce_Motion_Functionality_Implemented` - Demonstration or detailed confirmation of 'Reduce Motion' working across all animated features.</expected_artifact>
</task>

</tasks_for_claude>

## 4. Check-In & Progress Verification

<check_in_guidance>
* **End of Phase 6 Check-In: Full Interactivity & Animation Review**
    <check_in_prompt>
        <instruction_for_claude>You (Claude 4) will use this prompt to request all final Phase 6 artifacts and demonstrations:</instruction_for_claude>
        <prompt_text>"Developer, this phase culminates in bringing the portfolio to life. Please provide for review:
        1. Demonstrations (`P6_Interactivity_Demos.zip` or links to live dev server showcases) covering:
            * `P6_Global_Animations_Implemented`.
            * `P6_Primary_Interactive_Narrative_Pattern_Fully_Interactive` (desktop).
            * `P6_Mobile_Adaptation_Interactive_Narrative_Interactive` (mobile/tablet).
            * `P6_Data_Viz_And_Content_Reveal_Animations_Implemented`.
            * (If applicable) `P6_Live_API_Module_Interactive`.
            * `P6_Reduce_Motion_Functionality_Implemented`.
        2. Any updates to `P6_Motion_Design_Specs_Refined.md`.
        3. Confirmation of initial performance profiling (`P6_Todo_PerformanceProfileAnimations`).
        I will conduct a thorough review of all interactive elements and animations for functionality, performance, aesthetic alignment, and accessibility."</prompt_text>
    </check_in_prompt>
    <artifact_review_process>
      <step>Claude 4 receives all demonstrations and documentation.</step>
      <step>Claude 4 states review focus: "I am meticulously reviewing all implemented interactivity and animations to ensure:
        * They function precisely as specified in `P2_Motion_Design_Detailed_Specs_V1.md` and the task descriptions for this phase.
        * They are purposeful and enhance the Palantir aesthetic, rather than distract.
        * Performance is smooth across interactions, especially for the primary interactive narrative pattern and any data visualizations.
        * Mobile/tablet interactions are touch-optimized and effective.
        * All interactive elements are fully keyboard accessible and ARIA-compliant.
        * The 'Reduce Motion' functionality is comprehensively implemented and respected by all animations."</step>
      <step>
        <condition>If all aligned:</condition>
        <claude_response>"Phase 6 is complete. The portfolio is now dynamically interactive and animated with precision and purpose. All features adhere to the Palantir aesthetic, perform well, and meet our accessibility standards for motion. This is a significant milestone. Approved. We are ready for Phase 7: Responsiveness & Comprehensive Accessibility."</claude_response>
      </step>
      <step>
        <condition>If revisions needed:</condition>
        <claude_response>"Revisions are necessary to perfect the interactivity and animations:
        * For Primary Interactive Pattern: `[e.g., 'The 'Data Flow' animation on the Network Graph edges feels a bit too slow; please adjust duration to 300ms and ensure it uses an ease-out timing function.']`
        * For Mobile Interactivity: `[e.g., 'Tapping project cards in the MobileListView does not consistently open the detail view; please debug.']`
        * For Accessibility: `[e.g., 'The 'Reduce Motion' toggle is not disabling the scroll-based parallax effect on background graphics. This needs to be addressed.']`
        * For Performance: `[e.g., 'The initial 'Constellation Activation' animation for the Network Graph is causing noticeable jank on initial load; please profile and optimize its rendering, perhaps by reducing node count during activation or simplifying edge drawing.']`
        Please address these points and provide updated demonstrations."</claude_response>
      </step>
    </artifact_review_process>
</check_in_guidance>

## 5. Prompt-Engineering Best Practices for Claude 4 (Self-Audit)

<self_audit_checklist>
* **Agentic Proactivity & Parameter Detail:** Have I provided the Developer with extremely precise, parameter-driven descriptions for each animation and interaction, sufficient for an LLM (Claude 4 guiding them) to translate into code? Are timings, easing functions, target properties, and visual outcomes clearly defined?
* **Deep Research Integration (Motion & Accessibility):** Is my guidance fully leveraging `P2_Motion_Design_Detailed_Specs_V1.md`, `Advanced_Accessibility_Techniques.md` (especially regarding motion and keyboard interaction), and `Mobile_Adaptation_Palantir_Viz.md` (for touch interactions)?
* **Purposeful Animation Reinforcement:** Am I consistently reminding the Developer (via my prompts for Claude 4) that every animation must be purposeful (feedback, guidance, state change, clarity) and align with Palantir's utilitarian ethos?
* **Performance as a Core Requirement:** Does my guidance treat performance not as an afterthought, but as a fundamental requirement for all interactive elements and animations, especially on mobile?
* **"Reduce Motion" as Non-Negotiable:** Have I ensured that the requirement to respect "Reduce Motion" is applied to *every single* animation discussed?
* **Clarity of "Definition of Done":** Is it clear for each task what constitutes a successfully implemented interactive feature or animation?
</self_audit_checklist>

</claude_guide_phase>
