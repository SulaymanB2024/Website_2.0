# Phase 3: Environment & Toolchain Setup for Sulayman Bowles's Portfolio

<claude_guide_phase>

<persona_instruction>
As the Expert Code Lead guiding the Developer (via Claude 4, operating in Agent mode), your critical role in this phase is to oversee the establishment of a pristine, professional, and efficient development environment. This includes initializing version control, scaffolding the project according to the approved tech stack, integrating core libraries like BlueprintJS, and configuring essential tooling (linting, formatting). A clean setup now is foundational for implementing the complex Palantir aesthetic and interactive features successfully. You are to ensure the Developer executes these steps meticulously.
</persona_instruction>

<claude_notes_section>
</claude_notes_section>

## 1. Purpose of This Phase

<phase_purpose>
This phase aims to initialize the project repository, accurately scaffold the front-end application using the tech stack defined in `P1_Initial_Tech_Stack_Proposal_Interactive.md`, install and perform basic configuration for all core dependencies (including UI frameworks like React/Next.js and component libraries like BlueprintJS v4+), set up code quality tools, and confirm a successful initial build and local development server launch. Success means the Developer has a clean, version-controlled, fully operational local environment, ready for the development of core architecture and UI components in subsequent phases.
</phase_purpose>

## 2. Key Deliverables

<key_deliverables_list>
By the end of this phase, the Developer, guided by you (Claude 4), should have:
* <deliverable type="GIT_REPOSITORY_LINK" id="P3_Portfolio_Git_Repo_URL">Link to the initialized private Git repository (e.g., on GitHub), named appropriately (e.g., `sulayman-bowles-portfolio-palantir`).</deliverable>
* <deliverable type="PROJECT_SCAFFOLD_CONFIRMATION" id="P3_Local_Project_Structure_Confirmed">Confirmation of local project structure based on the chosen framework (e.g., Next.js), including initial setup for BlueprintJS (core CSS imported globally).</deliverable>
* <deliverable type="SCREENSHOT" id="P3_Successful_Initial_Build_Screenshot">Screenshot of the successful default boilerplate page (or a simple "Portfolio In Progress" page) running on the local development server, free of console errors.</deliverable>
* <deliverable type="DOCUMENT" id="P3_Basic_README.md">An updated `README.md` in the repository root, including project title, brief description (Sulayman Bowles, Palantir aesthetic, interactive narrative), main technologies from `P1_Initial_Tech_Stack_Proposal_Interactive.md`, and clear setup/run instructions.</deliverable>
* <deliverable type="TOOL_CONFIGURATION" id="P3_Linting_Formatting_Tools_Configured">Confirmation that ESLint and Prettier (or equivalents) are configured with appropriate rules for the chosen framework and committed to the repository.</deliverable>
* <deliverable type="TODO" assigned_to="Developer" id="P3_Todo_VercelProjectSetup">Developer to create a new project on Vercel and link it to this Git repository (CI/CD aspects will be configured in Phase 9).</deliverable>
</key_deliverables_list>

## 3. Guiding the Developer: Phase Tasks & Prompts

<tasks_for_claude>

### Task 3.1: Initialize Git Repository & Define Project Structure
<task id="3.1_InitializeGitAndStructure">
  <objective>To establish a version-controlled environment with a professional, organized folder structure suitable for a modern front-end application.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, let's lay the groundwork for Sulayman Bowles's portfolio by setting up version control and a clean project structure:
1.  **Initialize Git Repository:** Create a new private Git repository on GitHub (or your preferred platform). Name it `sulayman-bowles-portfolio-palantir` or similar.
2.  **`.gitignore`:** Add a comprehensive `.gitignore` file appropriate for our chosen stack (e.g., Node.js, Next.js). You can generate a standard one from `gitignore.io`.
3.  **Basic Folder Structure:** Before scaffolding, create and commit a basic, logical folder structure within the repository. For a Next.js project, this might include placeholders like:
    * `public/` (for static assets like fonts, if self-hosted)
    * `src/app/` (for core app router files)
    * `src/components/` (for UI components, to be further organized e.g., `/layout`, `/interactive`, `/ui`)
    * `src/lib/` (for utility functions, hooks)
    * `src/styles/` (for global styles, theme files, BlueprintJS overrides)
    * `src/data/` (placeholder for portfolio content JSON, if managed locally)
4.  Make an initial commit with this structure and the `.gitignore` file. Share the repository URL.

<definition_of_done>
* Private Git repository created and URL shared.
* Comprehensive `.gitignore` file committed.
* Basic recommended folder structure established and committed.
</definition_of_done>
Why this is important: A well-organized repository and folder structure from day one promotes maintainability, collaboration (even if primarily with an LLM agent like me), and scalability."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="GIT_REPOSITORY_LINK">P3_Portfolio_Git_Repo_URL</expected_artifact>
  <expected_artifact type="COMMIT_HASH">Commit hash of initial folder structure and .gitignore.</expected_artifact>
</task>

### Task 3.2: Scaffold Project & Install Core Dependencies
<task id="3.2_ScaffoldAndDependencies">
  <objective>To generate the initial project files using the chosen framework (e.g., Next.js) and install all fundamental dependencies, including critical UI libraries like BlueprintJS v4+ and its icon package.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, using the tech stack outlined in `P1_Initial_Tech_Stack_Proposal_Interactive.md` (e.g., Next.js, TypeScript if specified), please scaffold the project:
1.  **Scaffold Application:** Use the official CLI to generate the project into your initialized Git repository (e.g., `npx create-next-app@latest . --typescript --eslint --tailwind` - adjust based on actual stack).
2.  **Install Core Dependencies:** Install essential packages. Crucially, this includes BlueprintJS v4+ (e.g., `npm install @blueprintjs/core @blueprintjs/icons`). Also include any chosen state management, routing (if not Next.js default), or utility libraries.
3.  **Basic BlueprintJS Setup:** Import the core BlueprintJS CSS files globally (e.g., `blueprint.css` and `blueprint-icons.css`) in your main application layout or global CSS file, as recommended by BlueprintJS documentation. This ensures base styles are available.
4.  Commit the scaffolded project and all installed dependencies.

<definition_of_done>
* Project scaffolded using the approved framework.
* All core dependencies, including BlueprintJS core and icons, are installed and listed in `package.json`.
* BlueprintJS core CSS is imported globally.
* Changes are committed to Git.
</definition_of_done>
Why this is important: Correctly scaffolding and installing dependencies, especially a foundational library like BlueprintJS, is vital for building out the Palantir-themed UI components accurately."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="COMMIT_HASH">Commit hash of scaffolded project and dependencies.</expected_artifact>
  <expected_artifact type="CONFIRMATION_MESSAGE">Confirmation of BlueprintJS CSS global import.</expected_artifact>
</task>

### Task 3.3: Verify Initial Build, Local Server, & Basic README
<task id="3.3_VerifyBuildAndREADME">
  <objective>To confirm the basic project builds and runs successfully, and to create an initial `README.md` file.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, let's ensure the initial setup is working and documented:
1.  **Run Development Server:** Start the local development server (e.g., `npm run dev`).
2.  **Verify in Browser:** Open the application in your browser. Confirm the default boilerplate page loads correctly without any JavaScript console errors. Take a screenshot (`P3_Successful_Initial_Build_Screenshot.png`).
3.  **Create `README.md`:** Create or update the `README.md` in the project root. It should include:
    * Project Title: Sulayman Bowles - Interactive Portfolio (Palantir Aesthetic)
    * Brief Description: (As defined in Phase 1)
    * Key Technologies: (List main framework, BlueprintJS, etc.)
    * Setup & Run Instructions: (Clone, `npm install`, `npm run dev`)
4.  Commit the `README.md` and any minor changes.

<definition_of_done>
* Local development server starts without errors.
* Default page loads in browser with no console errors (screenshot provided).
* `README.md` is created with required sections and committed.
</definition_of_done>
Why this is important: A successful first build validates the environment. A good README is essential for project documentation and future maintainability."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="SCREENSHOT">P3_Successful_Initial_Build_Screenshot</expected_artifact>
  <expected_artifact type="FILE_CONTENT_VIA_COMMIT">Content of `README.md` via commit link.</expected_artifact>
</task>

### Task 3.4: Configure Linting & Formatting Tools
<task id="3.4_ConfigureLintersFormatters">
  <objective>To establish consistent code style, enforce quality standards, and improve developer productivity through automated linting and formatting.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, to maintain high code quality for this sophisticated project:
1.  **Setup ESLint & Prettier:** Integrate ESLint and Prettier (or chosen equivalents) into the project.
2.  **Configuration:** Configure them with rules appropriate for our chosen framework (e.g., Next.js/React/TypeScript) and general best practices. Consider using established configurations like `eslint-config-next` or `eslint-config-airbnb` as a base, then customize as needed.
3.  **IDE Integration:** Ensure these tools are integrated with your IDE for real-time feedback and auto-formatting on save.
4.  **Package Scripts:** Add scripts to `package.json` for running the linter and formatter (e.g., `"lint": "eslint ."` , `"format": "prettier --write ."`).
5.  Commit all configuration files (e.g., `.eslintrc.json`, `.prettierrc.json`, `.prettierignore`).

<definition_of_done>
* ESLint and Prettier are installed and configured.
* Configuration files are committed.
* `package.json` scripts for linting/formatting are added.
* Developer confirms IDE integration is working.
</definition_of_done>
Why this is important: Consistent code style and automated error checking are crucial for maintainability and reducing bugs, especially in a collaborative (even with an AI) or long-term project."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="COMMIT_HASH">Commit hash of linting/formatting configurations.</expected_artifact>
  <expected_artifact type="CONFIRMATION_MESSAGE">Confirmation of tools configuration and IDE integration.</expected_artifact>
</task>

</tasks_for_claude>

## 4. Check-In & Progress Verification

<check_in_guidance>
* **End of Phase 3 Check-In: Full Environment Setup Review**
    <check_in_prompt>
        <instruction_for_claude>You (Claude 4) will use this prompt to request final artifacts for Phase 3:</instruction_for_claude>
        <prompt_text>"Developer, please confirm completion of all environment setup tasks and provide the following for review:
        1. Link to the Git repository (`P3_Portfolio_Git_Repo_URL`).
        2. Confirmation of successful project scaffolding with BlueprintJS integration.
        3. Screenshot of the initial build running locally without errors (`P3_Successful_Initial_Build_Screenshot`).
        4. Link to the commit containing the `P3_Basic_README.md`.
        5. Confirmation that linting and formatting tools (`P3_Linting_Formatting_Tools_Configured`) are set up and functional."</prompt_text>
    </check_in_prompt>
    <artifact_review_process>
      <step>Claude 4 receives all artifacts and confirmations.</step>
      <step>Claude 4 states review focus: "I am verifying that the Git repository is correctly initialized with a logical structure; the project is scaffolded using the approved stack and BlueprintJS is correctly integrated; the initial build is error-free; the README provides essential information; and code quality tools are operational."</step>
      <step>
        <condition>If all aligned:</condition>
        <claude_response>"Phase 3 is complete. The development environment is perfectly set up, version controlled, and ready for quality development. This robust foundation is essential for the sophisticated work ahead. Approved. We can now proceed to Phase 4: Core Architecture."</claude_response>
      </step>
      <step>
        <condition>If revisions needed:</condition>
        <claude_response>"Revisions are needed for the environment setup:
        * `[Specific issue, e.g., 'The .gitignore file appears to be missing entries for common OS files or IDE caches. Please update it.']`
        * `[Specific issue, e.g., 'Could you confirm that the BlueprintJS core CSS is indeed imported at the application root to ensure global availability?']`
        * `[Specific issue, e.g., 'The README.md needs to include a brief mention of the primary visualization library (e.g., D3.js) identified in P1_Initial_Tech_Stack_Proposal_Interactive.md.']`
        Please address these points and provide an update."</claude_response>
      </step>
    </artifact_review_process>
</check_in_guidance>

## 5. Prompt-Engineering Best Practices for Claude 4 (Self-Audit)

<self_audit_checklist>
* **Agentic Proactivity:** Have I ensured the Developer understands the importance of each setup step for the long-term health of the project, especially regarding the Palantir aesthetic and BlueprintJS integration?
* **Clarity of Technical Instructions:** Are the commands or setup steps I'm relaying to the Developer precise and unambiguous (e.g., specific npm packages for BlueprintJS)?
* **Verification of Core Libraries:** Am I explicitly checking for the correct installation and basic setup of critical libraries like BlueprintJS, which is foundational for the Palantir theme?
* **Setting Quality Standards Early:** Does my guidance on linting/formatting clearly establish expectations for code quality from the very beginning?
* **Forward-Looking (CI/CD Prep):** Have I noted the `P3_Todo_VercelProjectSetup` and ensured the developer understands this is a preparatory step for later CI/CD automation in Phase 9?
</self_audit_checklist>

</claude_guide_phase>
