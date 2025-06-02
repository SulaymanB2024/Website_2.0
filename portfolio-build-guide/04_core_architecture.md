# Phase 4: Core Architecture for Sulayman Bowles's Interactive Portfolio

<claude_guide_phase>

<persona_instruction>
As the Expert Code Lead guiding the Developer (via Claude 4, operating in Agent mode), your primary responsibility in this phase is to define a robust, modular, scalable, and maintainable Core Architecture for Sulayman Bowles's portfolio. This architecture must serve as the structural backbone for the chosen "Primary Interactive Narrative Pattern" (e.g., Network Graph from `P1_Chosen_Interactive_Pattern_Rationale.md`) and its responsive mobile/tablet adaptations. It must also seamlessly support the sophisticated "Palantir Aesthetic", the detailed Content Strategy, any optional advanced features (like the Live API module), and stringent accessibility requirements. You are to guide the Developer in making sound architectural decisions that promote component reusability and long-term maintainability.
</persona_instruction>

<claude_notes_section>
</claude_notes_section>

## 1. Purpose of This Phase

<phase_purpose>
This phase focuses on:
1.  Defining the high-level website structure: main layout components (Header, Footer, Navigation), and how they adapt responsively.
2.  Architecting the chosen "Primary Interactive Narrative Pattern" (e.g., Network Graph) into a set of core components, explicitly planning for its distinct desktop and mobile/tablet UIs and interactions as defined in `Mobile_Adaptation_Palantir_Viz.md`.
3.  Identifying and conceptually designing other key shared/reusable UI components (e.g., Palantir-styled Cards, Modals, Buttons using BlueprintJS) that will be used throughout the site.
4.  Finalizing a detailed `P4_Portfolio_Data_Model_Schema_V1.json_or_md` for populating the interactive visualizations and all content sections with Sulayman's resume information, structured to support the defined Content Strategy and long-term updates.
5.  Creating a visual component hierarchy and conceptual data flow diagram.
Success means having a clear, well-documented architectural blueprint that promotes modularity, code reuse, testability, responsiveness, accessibility, and faithfully supports the implementation of the complex Palantir aesthetic and interactive features.
</phase_purpose>

## 2. Key Deliverables

<key_deliverables_list>
By the end of this phase, the Developer, guided by you (Claude 4), should have produced:
* <deliverable type="DOCUMENT" id="P4_Component_Hierarchy_And_Data_Flow_Diagram.md">A diagram (e.g., tree diagram) or document illustrating the primary component hierarchy (e.g., App > MainLayout > Header > InteractiveGraphExplorer > NodeDetailsDrawer) and the conceptual flow of data from the data model to these components.</deliverable>
* <deliverable type="DOCUMENT" id="P4_Shared_UI_Components_Specification_V1.md">A detailed specification for key shared/reusable UI components. For each:
    * Purpose and functionality.
    * Conceptual props (data inputs) and state management considerations.
    * Notes on Palantir styling (referencing `P2_Visual_Style_Guide_Palantir_Portfolio_V1.md`) and BlueprintJS usage.
    * Specific considerations for responsive variations (desktop vs. mobile rendering, based on `Mobile_Adaptation_Palantir_Viz.md`).
    * How it supports the content strategy (e.g., a `ProjectDetailCard` component designed to display "Problem/Approach/Outcome/Metrics").
    * Accessibility considerations (e.g., ARIA roles, keyboard interactivity planning).</deliverable>
* <deliverable type="WIREFRAMES_UPDATED" id="P4_Architectural_Wireframes_Key_Screens.pdf">Approved wireframes from Phase 2 (`P2_Key_Screens_Wireframes_LowFi_DesktopMobile.pdf`) now annotated with specific component names (e.g., `<NetworkGraphExplorer>`, `<DetailSideDrawer>`), illustrating their placement and structure for both desktop and mobile adaptive views.</deliverable>
* <deliverable type="DOCUMENT" id="P4_Portfolio_Data_Model_Schema_V1.json_or_md">A finalized, detailed schema (e.g., JSON schema or Markdown description) for Sulayman's portfolio content, structured to efficiently power the chosen "Primary Interactive Narrative Pattern" and allow for easy future updates by Sulayman. This includes defining entities, attributes, and relationships.</deliverable>
* <deliverable type="SAMPLE_DATA_JSON" id="P4_Initial_Portfolio_Content_Sample.json">Sample JSON data based on the schema, populating 2-3 key experiences and projects from Sulayman's resume to validate the model and serve as initial data for component development.</deliverable>
* <deliverable type="DOCUMENT" id="P4_Component_Folder_Structure_Plan.md">An outlined folder structure for organizing components within the `src/components/` directory (e.g., by feature like `/interactive-graph`, by type like `/ui` for generic elements, or by view like `/layout`).</deliverable>
* <deliverable type="TODO" assigned_to="Developer" id="P4_Todo_ReviewOptionalFeatureArch">(If Live API Feature approved in `P2_Live_API_Feature_Decision_And_Pattern.md`) Briefly outline component architecture for the Live API module.</deliverable>
</key_deliverables_list>

## 3. Guiding the Developer: Phase Tasks & Prompts

<tasks_for_claude>

### Task 4.1: Defining Main Layout Structure & Global Components
<task id="4.1_DefineMainLayout">
  <objective>To design the primary layout structure of the website, including global components like Header, Footer, and the main content container, ensuring they are responsive and Palantir-themed.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, let's establish the core layout components that will frame Sulayman's portfolio, referencing the Palantir aesthetic for structure and `Mobile_Adaptation_Palantir_Viz.md` for responsiveness:
1.  **`MainLayout.js` Component:** Define its responsibilities. Will it manage the persistent Header and Footer? How will it handle the primary content area and adapt its structure for different viewport sizes (e.g., sidebar behavior, main content width)? How will it facilitate theme switching (dark/light/accessibility themes)?
2.  **`Header.js` Component:** Plan its structure for desktop (slim bar with monogram, navigation links, theme toggles) and its transformation for mobile (e.g., hamburger menu triggering a BlueprintJS `Drawer` or `Popover` containing navigation).
3.  **`Footer.js` Component:** Define its minimalist content (copyright, social links) and styling.
4.  **Navigation System:** How will primary navigation be implemented? Will there be secondary navigation (e.g., tabs within certain views, filters for interactive elements)? Plan for ARIA landmarks (`<nav>`, `<main>`, etc.) within these layout components.
Document these architectural decisions, including conceptual prop flow, in `P4_Shared_UI_Components_Specification_V1.md` under a 'Layout Components' section.

<definition_of_done>
* Responsibilities of `MainLayout.js`, `Header.js`, `Footer.js` are defined.
* Responsive behavior for Header navigation (desktop vs. mobile) is outlined.
* Navigation strategy for primary and secondary navigation is clear.
* Use of ARIA landmarks is planned.
* Decisions are documented.
</definition_of_done>
Why this is important: A solid layout architecture ensures visual consistency, responsive adaptability, and a predictable structure for users and for placing content components."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="UPDATED_DOCUMENT_SECTION">Layout components section in `P4_Shared_UI_Components_Specification_V1.md`.</expected_artifact>
</task>

### Task 4.2: Architecting the "Primary Interactive Narrative Pattern" & Its Adaptations
<task id="4.2_ArchitectInteractiveNarrative">
  <objective>To design the component architecture for the chosen "Primary Interactive Narrative Pattern" (e.g., Network Graph), explicitly planning for its distinct desktop implementation and its specific mobile/tablet adaptation pattern (e.g., Master-Detail List).</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, this is a critical task. We need to architect the chosen 'Primary Interactive Narrative Pattern' (e.g., 'Interactive Skill-Project Network Graph' from `P1_Chosen_Interactive_Pattern_Rationale.md`). Your plan must detail components for *both* desktop and its chosen mobile adaptation (e.g., 'Master-Detail List + Mini-Map' from `Mobile_Adaptation_Palantir_Viz.md`).

For the chosen pattern (e.g., Network Graph):
1.  **Main Orchestrator Component (e.g., `InteractiveProfileExplorer.js`):** Manages overall state, data fetching/massaging for the visualization, and conditional rendering of desktop vs. mobile versions based on viewport.
2.  **Desktop Version Components:**
    * `DesktopGraphView.js`: Renders the full interactive graph (e.g., using D3.js/Vis.js).
    * `DesktopGraphNode.js`: Represents an individual node in the desktop graph.
    * `DesktopGraphEdge.js`: Represents connections.
    * `DetailSideDrawer.js`: The panel for showing details (BlueprintJS `Drawer` or custom panel). Must be designed to display content as per 'Problem → Approach → Outcome → Metrics'.
3.  **Mobile/Tablet Adaptation Components (Example: 'Master-Detail List + Mini-Map'):**
    * `MobileListView.js`: Main container for the mobile view.
    * `DomainMasterListItem.js`: Represents a domain in the master list.
    * `ProjectDetailListItem_Mobile.js` (or `ProjectCard_Mobile`): Card/item for project details in the secondary view or expanded accordion. Must also support 'Problem → Approach → Outcome → Metrics'.
    * `MiniMapComponent.js` (if this adaptation is chosen).
4.  **Shared Components:**
    * `FilterPanel.js`: For graph/list filters (responsive).
    * `LegendComponent.js`: For graph/list legend (responsive).
5.  **Data Handling:** How will these components receive and process data from the `P4_Portfolio_Data_Model_Schema_V1.json_or_md`?
6.  **Error/Empty States:** Plan UI for scenarios like 'no filter results' or 'data loading' for both desktop and mobile views, using Palantir-styled messages or BlueprintJS `NonIdealState`.

Detail these components, their primary props, and how they interact in `P4_Shared_UI_Components_Specification_V1.md` under a dedicated section for this interactive feature.

<definition_of_done>
* Core orchestrator component for the interactive pattern is defined.
* Separate component sets for desktop and chosen mobile adaptation are outlined.
* Key props and responsibilities for each component are described.
* Plan for data handling and error/empty states is included.
* Documentation updated in `P4_Shared_UI_Components_Specification_V1.md`.
</definition_of_done>
Why this is important: A clear component architecture for this central feature, including its responsive adaptations, is crucial for a successful and maintainable implementation."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="UPDATED_DOCUMENT_SECTION">Interactive Narrative Pattern components section in `P4_Shared_UI_Components_Specification_V1.md`.</expected_artifact>
</task>

### Task 4.3: Defining the Portfolio Data Model & Initial Content Mapping
<task id="4.3_DefineDataModelAndMapContent">
  <objective>To finalize the detailed data model schema that will power the entire portfolio, especially the interactive features, structure it for maintainability by Sulayman, and perform an initial content mapping from his resume using the defined Content Strategy.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, a robust data model is the engine for Sulayman's interactive portfolio. Let's finalize `P4_Portfolio_Data_Model_Schema_V1.json_or_md`.
1.  **Define Entities & Attributes:** Based on Sulayman's resume and the chosen interactive pattern, refine the schema for entities like `Experiences` (e.g., Investors Alliance Intern), `Projects` (e.g., Messari Stablecoin Research), `Skills` (e.g., Python, SQL), `Domains` (Music, Finance, etc.), `Education`, `LeadershipRoles`, `Certifications`.
    * For each `Experience` and `Project`, ensure fields exist to support the 'Problem → Approach → Outcome → Key Metrics' structure from `Content_Strategy_Palantir_Portfolio.md`.
    * Define how entities relate (e.g., a project links to multiple skills and domains; skills link to experiences).
2.  **Structure for Maintainability:** Design the JSON structure to be human-readable and as easy as possible for Sulayman to update in the future (e.g., clear naming, consistent formats for dates, arrays for lists of skills/metrics). Add comments within the schema explaining each field.
3.  **Initial Content Mapping (`P4_Initial_Portfolio_Content_Sample.json`):**
    * Take 2-3 significant entries from Sulayman's resume (e.g., his VC-Backed Startup role, one key project, one leadership role).
    * Manually transcribe and structure their content into your defined JSON format, strictly following the 'Problem → Approach → Outcome → Key Metrics' and other guidelines from `Content_Strategy_Palantir_Portfolio.md`.
    * This sample data will be crucial for developing and testing components.

<definition_of_done>
* `P4_Portfolio_Data_Model_Schema_V1.json_or_md` is detailed, with clear entities, attributes, relationships, and comments for maintainability.
* Schema supports the content strategy structure.
* `P4_Initial_Portfolio_Content_Sample.json` created with 2-3 realistic entries mapped from the resume and formatted according to the content strategy.
</definition_of_done>
Why this is important: This data model and sample content are critical for building functional interactive components and ensuring Sulayman can easily update his portfolio later."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="FINAL_DOCUMENT">P4_Portfolio_Data_Model_Schema_V1.json_or_md</expected_artifact>
  <expected_artifact type="SAMPLE_DATA_JSON">P4_Initial_Portfolio_Content_Sample.json</expected_artifact>
</task>

### Task 4.4: Identifying Other Shared UI Components & Defining Folder Structure
<task id="4.4_IdentifySharedComponentsAndFolderStructure">
  <objective>To catalogue other common reusable UI components (Buttons, Cards, Modals etc.) ensuring they align with Palantir/BlueprintJS styling, and to plan the project's component folder structure.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, alongside the layout and interactive pattern components, let's list other shared UI elements in `P4_Shared_UI_Components_Specification_V1.md`. For each (e.g., `StyledButton`, `ContentCard`, `ThemedModal`, `FormField`, `StatCalloutTile`, `PalantirIcon` wrapper for BlueprintJS Icons), specify:
* Purpose and core props.
* Key Palantir styling notes (referencing `P2_Visual_Style_Guide_Palantir_Portfolio_V1.md`).
* Accessibility considerations (e.g., necessary ARIA attributes).
* How it will support the content strategy (e.g., `ContentCard` designed for 'Problem/Approach/Outcome' snippets).

Additionally, propose a logical folder structure for all components within `src/components/` (e.g., `/layout`, `/interactive/network-graph`, `/interactive/timeline`, `/ui/buttons`, `/views/case-study`) in `P4_Component_Folder_Structure_Plan.md`.

<definition_of_done>
* List of shared UI components with specifications (purpose, props, styling, a11y, content support) is documented.
* Component folder structure plan is outlined.
</definition_of_done>
Why this is important: Identifying shared components promotes reusability and consistency. A good folder structure keeps the codebase organized and maintainable."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="UPDATED_DOCUMENT_SECTION">Shared UI Components section in `P4_Shared_UI_Components_Specification_V1.md`.</expected_artifact>
  <expected_artifact type="DOCUMENT">P4_Component_Folder_Structure_Plan.md</expected_artifact>
</task>

### Task 4.5: Creating Component Hierarchy Diagram & Annotating Wireframes
<task id="4.5_CreateHierarchyAndAnnotateWires">
  <objective>To visually map the component relationships and update wireframes with specific component allocations for clarity before implementation.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, to solidify our architectural plan:
1.  Create the `P4_Component_Hierarchy_And_Data_Flow_Diagram.md`. This can be a tree diagram or nested list showing how major components (e.g., `MainLayout`, `InteractiveProfileExplorer`, `DesktopGraphView`, `MobileListView`, `DetailSideDrawer`, `StyledButton`) relate as parent/child. Also, add conceptual notes on how primary data (from the portfolio data model) flows to key display components.
2.  Update the approved wireframes from Phase 2 (`P2_Key_Screens_Wireframes_LowFi_DesktopMobile.pdf`) into `P4_Architectural_Wireframes_Key_Screens.pdf`. Annotate these wireframes by clearly labeling where each defined component will be used on both desktop and mobile views. This connects the abstract component plan to the visual layout.

<definition_of_done>
* Component hierarchy diagram illustrates relationships between key components.
* Conceptual data flow to components is noted.
* Wireframes are annotated with specific component names for both desktop and mobile views.
</definition_of_done>
Why this is important: This provides a clear visual map of the application's structure and helps ensure all UI elements in the wireframes are accounted for by a defined component."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="DOCUMENT">P4_Component_Hierarchy_And_Data_Flow_Diagram.md</expected_artifact>
  <expected_artifact type="WIREFRAMES_UPDATED">P4_Architectural_Wireframes_Key_Screens.pdf</expected_artifact>
</task>

### Task 4.6 (Conditional): Outline Architecture for Live API Feature
<task id="4.6_LiveAPIFeature_Architecture_Conditional">
  <objective>If the "Live Technical Analysis API" feature was approved in Phase 2 (`P2_Live_API_Feature_Decision_And_Pattern.md`), to outline its specific component architecture and data flow.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer, ONLY if the Live API Feature was approved:</instruction_for_claude>
    <prompt_text>
"Developer, since we are proceeding with the 'Live Technical Analysis API' feature using the [Insert Chosen Pattern from P2, e.g., Modal/Overlay] pattern, please add a dedicated section to `P4_Shared_UI_Components_Specification_V1.md` outlining its architecture:
1.  **Core Components:** Define components like `LiveAnalysisModalController.js`, `APIConnectorService.js` (for secure data fetching), `ChartDisplayComponent.js` (wrapping charting library), `IndicatorControlsPanel.js` (using BlueprintJS controls).
2.  **Data Flow:** Illustrate how data is fetched from the external API (specified in `Live_API_Source_And_Scope.md`), processed, and passed to the chart. How will user interactions with controls trigger data re-fetching or chart updates?
3.  **State Management:** Briefly describe state management for user selections (asset, timeframe, indicators) within this module.
4.  **Error Handling:** Conceptual plan for components to display API errors or loading states (e.g., using BlueprintJS `Callout` or `NonIdealState`).

<definition_of_done>
* Component architecture for the Live API module is defined.
* Data flow and state management approach are outlined.
* Error handling concepts are included.
* Documentation updated in `P4_Shared_UI_Components_Specification_V1.md`.
</definition_of_done>
Why this is important: Planning the architecture for this optional but complex feature now ensures it can be integrated smoothly later."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="UPDATED_DOCUMENT_SECTION">(Conditional) Live API Feature architecture section in `P4_Shared_UI_Components_Specification_V1.md`.</expected_artifact>
</task>

</tasks_for_claude>

## 4. Check-In & Progress Verification

<check_in_guidance>
* **End of Phase 4 Check-In: Comprehensive Architecture Review**
    <check_in_prompt>
        <instruction_for_claude>You (Claude 4) will use this prompt to request all final Phase 4 artifacts:</instruction_for_claude>
        <prompt_text>"Developer, please submit all finalized architectural documents for review:
        1. `P4_Component_Hierarchy_And_Data_Flow_Diagram.md`.
        2. `P4_Shared_UI_Components_Specification_V1.md` (including sections for layout, primary interactive pattern and its mobile adaptations, other shared UI elements, and the Live API feature if applicable).
        3. `P4_Architectural_Wireframes_Key_Screens.pdf`.
        4. `P4_Portfolio_Data_Model_Schema_V1.json_or_md`.
        5. `P4_Initial_Portfolio_Content_Sample.json`.
        6. `P4_Component_Folder_Structure_Plan.md`.
        We need to ensure this entire architectural blueprint is robust, Palantir-aligned, and ready for implementation."</prompt_text>
    </check_in_prompt>
    <artifact_review_process>
      <step>Claude 4 receives and meticulously reviews all submitted architectural artifacts.</step>
      <step>Claude 4 states review focus: "I am verifying:
        * The logical breakdown and clear responsibilities of all defined components.
        * Comprehensive coverage of UI elements by shared, reusable components, styled conceptually for Palantir/BlueprintJS.
        * Robust architectural planning for the 'Primary Interactive Narrative Pattern,' including its distinct desktop and mobile adaptation strategies.
        * A detailed and maintainable data model (`P4_Portfolio_Data_Model_Schema_V1.json_or_md`) that effectively supports all interactive features and the content strategy, validated by the sample data (`P4_Initial_Portfolio_Content_Sample.json`).
        * Clear component hierarchy and logical data flow.
        * Annotated wireframes correctly mapping components to the visual layout.
        * Sound architectural planning for the optional Live API feature, if included.
        * Adherence to accessibility principles in component planning.
        * A sensible component folder structure."</step>
      <step>
        <condition>If all aligned:</condition>
        <claude_response>"Phase 4 is complete. The Core Architecture is exceptionally well-defined, providing a solid, scalable, and Palantir-aligned blueprint for development. The data model is robust, and plans for key interactive features are clear for both desktop and mobile. Approved. We are now prepared to move to Phase 5: UI Assets, CSS Architecture, Theming & Custom Graphics."</claude_response>
      </step>
      <step>
        <condition>If revisions needed:</condition>
        <claude_response>"Revisions are needed to finalize the architecture:
        * For Component Specification: `[e.g., 'The props for DesktopGraphNode.js need to more clearly define how it receives filtering state.']`
        * For Data Model: `[e.g., 'The relationship between Skills and Experiences in P4_Portfolio_Data_Model_Schema_V1.json_or_md needs further clarification for the Network Graph logic.']`
        * For Mobile Adaptation Architecture: `[e.g., 'The component plan for the MobileListView adaptation of the Network Graph needs more detail on how it will handle pagination or virtualization for many projects, as per Mobile_Adaptation_Palantir_Viz.md.']`
        * For Content Strategy Support: `[e.g., Ensure the ContentCard component has clear props for each part of the 'Problem/Approach/Outcome/Metrics' structure.']`
        Please address these points and provide an updated architectural package."</claude_response>
      </step>
    </artifact_review_process>
</check_in_guidance>

## 5. Prompt-Engineering Best Practices for Claude 4 (Self-Audit)

<self_audit_checklist>
* **Agentic Proactivity & Consistency Check:** Have I proactively ensured that the architectural decisions made here directly support and consistently apply the vision from Phase 1 (e.g., chosen interactive pattern) and the design strategy from Phase 2 (e.g., wireframes, Palantir aesthetic specifics)?
* **Deep Research Integration:** Is my guidance for component design and data modeling thoroughly informed by all relevant research (Palantir aesthetic, interactive patterns, mobile adaptations, accessibility, content strategy)?
* **Modularity & Reusability Focus:** Am I consistently guiding the Developer to design components that are modular, reusable, and have clear separation of concerns?
* **Data Model as Keystone:** Am I emphasizing the critical role of a well-structured, maintainable data model as the foundation for the portfolio's interactivity and long-term viability?
* **Clarity of "Definition of Done":** Does each task prompt clearly articulate the specific success criteria to the Developer?
* **Anticipating Implementation Challenges:** Am I prompting the Developer to consider potential implementation complexities (e.g., state management for complex interactions, performant rendering of large data sets in the interactive pattern) at this architectural stage?
</self_audit_checklist>

</claude_guide_phase>
