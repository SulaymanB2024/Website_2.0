# Phase 5: UI Assets, CSS Architecture, Theming & Custom Graphics for Sulayman Bowles's Portfolio

<claude_guide_phase>

<persona_instruction>
As the Expert Code Lead guiding the Developer (via Claude 4, operating in Agent mode), this phase is pivotal for establishing the complete visual and stylistic DNA of Sulayman Bowles's portfolio. Your focus encompasses:
1.  Meticulous integration of standard UI assets (fonts, icons, images).
2.  Implementation of a sophisticated CSS architecture and theming system for the "Palantir Aesthetic" over BlueprintJS components, leveraging the detailed strategies in `Optimal_CSS_Architecture_For_Palantir_BlueprintJS.md`.
3.  Guidance on the design, creation (vector, optimized SVGs), and integration of **Custom Graphic Elements** (subtle background textures, minimalist section dividers, abstract spot glyphs) that reinforce the Palantir aesthetic and Sulayman's unique brand, as detailed in `Custom_Graphic_Elements_For_Palantir_Aesthetic.md`.
All work must adhere to the highest standards of visual precision, performance (asset optimization), and accessibility (theme adaptability, graphic alternatives). You are to ensure the Developer translates the approved design strategy (`P2_Visual_Style_Guide_Palantir_Portfolio_V1.md`) into a fully realized visual system.
</persona_instruction>

<claude_notes_section>
</claude_notes_section>

## 1. Purpose of This Phase

<phase_purpose>
This phase aims to:
1.  Finalize and implement a comprehensive strategy for sourcing, managing, optimizing, and integrating all UI assets (fonts like Inter/Roboto, icons like BlueprintJS Icons, Sulayman's professional photo, custom-designed graphics).
2.  Implement the selected CSS architecture (e.g., ITCSS, Scoped CSS-in-JS as per `P2_Chosen_CSS_Architecture.md`) to facilitate a maintainable and scalable Palantir theme over the BlueprintJS component library.
3.  Develop and deploy a complete design token system using CSS Custom Properties. This system will manage all stylistic values (colors for dark/light/warm-dark/high-contrast themes, typography scales, spacing units, shadows, border radii) as defined in `P2_Visual_Style_Guide_Palantir_Portfolio_V1.md` and inspired by `Optimal_CSS_Architecture_For_Palantir_BlueprintJS.md`.
4.  Oversee the design, vector creation, optimization (e.g., using SVGO), and seamless integration of custom graphic elements (e.g., low-opacity polygonal background meshes, minimalist SVG section dividers, abstract spot glyphs like a Data-Music Fusion Glyph), ensuring they are themable for dark/light modes.
5.  Implement all global styles, precise BlueprintJS component overrides, and Palantir-themed utility classes, all driven by the design token system.
6.  Ensure functional implementation of theme switchers for dark/light modes and any planned accessibility themes (e.g., high-contrast, warm dark mode).
Success in this phase means the portfolio has a fully realized, high-fidelity visual foundation: a well-organized asset pipeline, a robust and maintainable CSS codebase, a functional multi-theme system, and bespoke graphic elements that cohesively elevate the Palantir aesthetic and Sulayman's brand.
</phase_purpose>

## 2. Key Deliverables

<key_deliverables_list>
By the end of this phase, the Developer (potentially collaborating with a designer for custom graphics, if applicable), guided by you (Claude 4), should have:
* <deliverable type="DOCUMENT" id="P5_Asset_Management_And_Optimization_Plan_Final.md">The finalized plan for sourcing, storing, optimizing, and licensing all standard and custom graphic assets.</deliverable>
* <deliverable type="CODE_IMPLEMENTATION" id="P5_CSS_Architecture_Setup_Done">The chosen CSS architecture (from `P2_Chosen_CSS_Architecture.md`) fully set up in the project structure.</deliverable>
* <deliverable type="CODE_IMPLEMENTATION" id="P5_Design_Token_System_CSS_Variables.css">The core CSS file(s) defining all Palantir design tokens as CSS Custom Properties (e.g., `--palantir-bg: #1F1F1F`, `--palantir-accent-blue: #0052CC`, `--palantir-font-family: 'Inter'`), including tokens for dark, light, and accessibility themes (warm-dark, high-contrast).</deliverable>
* <deliverable type="CODE_IMPLEMENTATION" id="P5_Global_Styles_And_Blueprint_Overrides.css_or_scss">Implementation of global styles, comprehensive BlueprintJS component overrides (achieved via SASS recompilation or scoped CSS), and Palantir-themed utility classes, all consistently leveraging the design token system.</deliverable>
* <deliverable type="ASSET_COLLECTION" id="P5_Custom_Graphic_Elements_SVG_Optimized.zip">A version-controlled collection of all custom-designed background patterns, section dividers, and spot illustrations/glyphs as optimized SVG files (e.g., via SVGO), designed according to `Custom_Graphic_Elements_For_Palantir_Aesthetic.md`.</deliverable>
* <deliverable type="CODE_INTEGRATION_DEMO" id="P5_Custom_Graphics_Integration_Examples">Demonstrable examples (e.g., screenshots, Storybook stories, or a live dev server view) of custom graphics integrated into components or CSS (e.g., as background images, inline SVGs), correctly adapting to dark/light mode themes.</deliverable>
* <deliverable type="FEATURE_IMPLEMENTATION" id="P5_Theme_And_Accessibility_Toggle_Functionality_Done">Fully functional theme switcher for dark/light modes and any implemented accessibility themes (e.g., high-contrast, warm-dark mode), with user preferences persisted (e.g., via `localStorage`).</deliverable>
* <deliverable type="CODE_REVIEW_NOTES" id="P5_CSS_Graphics_And_Theming_Review.md">Notes from your (Claude 4's) review, confirming the CSS implementation adheres to the chosen architecture, effectively themes BlueprintJS, correctly uses design tokens, and that custom graphics are well-integrated and themable.</deliverable>
* <deliverable type="TODO" assigned_to="User/Sulayman" id="P5_Todo_ApproveCustomGraphics">Sulayman to review and approve final designs for custom graphic elements (monogram, glyphs, background patterns).</deliverable>
* <deliverable type="TODO" assigned_to="Developer" id="P5_Todo_FontIconLicensingConfirmed">Developer to confirm and document licensing for all chosen fonts and icon sets if not open source.</deliverable>
</key_deliverables_list>

## 3. Guiding the Developer: Phase Tasks & Prompts

<tasks_for_claude>

### Task 5.1: Finalizing Asset Management & Sourcing All UI Assets
<task id="5.1_FinalizeAssetManagementAndSourcing">
  <objective>To complete the sourcing of all standard UI assets (fonts, icons, photos) and finalize the creation pipeline and initial concepts for custom graphic elements, ensuring the `P5_Asset_Management_And_Optimization_Plan_Final.md` is comprehensive.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, let's ensure our asset foundation is complete. Please finalize and update the 'P5_Asset_Management_And_Optimization_Plan_Final.md':
1.  **Standard Assets:**
    * Confirm all fonts (e.g., Inter/Roboto, Source Code Pro) and their specific weights are sourced. Finalize the import/hosting strategy (e.g., self-host in `/public/assets/fonts/` for performance control). Document licensing (`P5_Todo_FontIconLicensingConfirmed`).
    * Finalize the icon strategy (e.g., primarily using BlueprintJS Icons, supplemented by Feather Icons if needed). Confirm integration method (e.g., React components via `@blueprintjs/icons`).
    * Obtain Sulayman's professional headshot, styled as per `Project_Aesthetic_Guidelines_Palantir.md` (`P5_Todo_ApproveCustomGraphics` for photo itself).
2.  **Custom Graphic Elements (Initial Concepts & Pipeline from `Custom_Graphic_Elements_For_Palantir_Aesthetic.md`):**
    * Review and refine initial concepts for 1-2 subtle background textures (e.g., low-opacity polygonal mesh), 1-2 minimalist SVG section dividers (e.g., thin line fragments with polygonal wedges), and 3-5 abstract spot glyphs relevant to Sulayman's domains (e.g., Data-Music Fusion Glyph).
    * Confirm the tooling for creation (e.g., Figma/Illustrator) and optimization (SVGO).
    * Define naming conventions and storage paths (e.g., `/src/assets/custom-graphics/backgrounds/`, `/src/assets/custom-graphics/glyphs/`).
3.  **Optimization Strategy:** Reconfirm optimization techniques for all assets (SVGO for SVGs, WebP/AVIF for raster images where appropriate, font subsetting).

<definition_of_done>
* `P5_Asset_Management_And_Optimization_Plan_Final.md` is updated and complete.
* All standard assets are sourced/planned.
* Initial concepts for custom graphics are refined and the creation/optimization pipeline is clear.
* Licensing for fonts/icons is confirmed and documented.
</definition_of_done>
Why this is important: A complete and well-organized asset plan is crucial for visual consistency, performance, and legal compliance."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="FINAL_DOCUMENT">P5_Asset_Management_And_Optimization_Plan_Final.md</expected_artifact>
  <expected_artifact type="CONCEPT_REFINEMENT_NOTES">Notes on refined concepts for custom spot glyphs and graphics.</expected_artifact>
</task>

### Task 5.2: Implementing Chosen CSS Architecture & Design Token System
<task id="5.2_ImplementCSSArchitectureAndTokens">
  <objective>To implement the CSS architecture selected in `P2_Chosen_CSS_Architecture.md` and develop the comprehensive Palantir design token system using CSS Custom Properties, as detailed in `Optimal_CSS_Architecture_For_Palantir_BlueprintJS.md`.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, it's time to build our CSS foundation, referencing `Optimal_CSS_Architecture_For_Palantir_BlueprintJS.md`:
1.  **Implement CSS Architecture:** Set up the project's CSS structure according to your `P2_Chosen_CSS_Architecture.md` (e.g., establish ITCSS layers, configure CSS-in-JS environment, or set up BEM naming conventions with CSS Modules). Ensure BlueprintJS core CSS is imported correctly within this architecture.
2.  **Develop Design Token System (`P5_Design_Token_System_CSS_Variables.css`):** Create the central CSS file(s) defining all Palantir design tokens as CSS Custom Properties. This must be comprehensive:
    * **Color Tokens:** Define variables for all themes:
        * Default (Dark Mode): `--palantir-bg: #1F1F1F; --palantir-text: #F5F5F5; --palantir-accent-blue: #0052CC; --palantir-accent-yellow: #FFD60A;` etc.
        * Light Mode: `--palantir-bg-light: #F5F5F5; --palantir-text-light: #1F1F1F;` etc.
        * Warm Dark Mode: `--palantir-bg-warm-dark: #2B2B2B; --palantir-text-warm-dark: #F0E6D2;` etc. (adjust as per specific warm palette).
        * High-Contrast Mode: `--palantir-bg-high-contrast: #000000; --palantir-text-high-contrast: #FFFFFF; --palantir-accent-high-contrast: #FFCC00;` etc..
    * **Typography Tokens:** `--palantir-font-family-sans: 'Inter', sans-serif; --palantir-font-family-mono: 'Source Code Pro', monospace; --palantir-font-size-base: 16px; --palantir-line-height-base: 1.5;` etc.. Include tokens for dynamic scaling if planned (e.g., `--palantir-font-scale-ratio: 1.2;`).
    * **Spacing, Sizing, Shadows, Borders:** `--palantir-spacing-unit: 8px; --palantir-border-radius: 4px; --palantir-shadow-level-1: 0 1px 3px rgba(0,0,0,0.12);` etc..
    * **Interactive State Tokens:** `--palantir-button-bg-hover: [calculated_value];` etc..
    Define these in `:root` for global scope, with theme variations applied via classes on a root element (e.g., `.theme-light`, `.theme-warm-dark`, `.accessibility-high-contrast`).

<definition_of_done>
* Chosen CSS architecture is structurally implemented in the codebase.
* `P5_Design_Token_System_CSS_Variables.css` is created and comprehensively defines all necessary CSS Custom Properties for all themes and stylistic elements.
* Token definitions are well-organized and commented.
</definition_of_done>
Why this is important: This token system is the heart of our theming strategy, enabling consistency, maintainability, and support for multiple themes including crucial accessibility variations."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="CODE_COMMIT">Commit hash for CSS architecture setup (`P5_CSS_Architecture_Setup_Done`).</expected_artifact>
  <expected_artifact type="CODE_IMPLEMENTATION">`P5_Design_Token_System_CSS_Variables.css` file(s).</expected_artifact>
</task>

### Task 5.3: Designing, Creating, and Optimizing Custom Graphic Elements
<task id="5.3_DesignCreateOptimizeCustomGraphics">
  <objective>To design, create as vector SVGs, and optimize all custom graphic elements (backgrounds, dividers, glyphs) according to `Custom_Graphic_Elements_For_Palantir_Aesthetic.md`, ensuring they are themable for dark/light modes.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer (or coordinate with a Graphic Designer if that role exists):</instruction_for_claude>
    <prompt_text>
"Developer/Designer, referencing `Custom_Graphic_Elements_For_Palantir_Aesthetic.md` and our refined concepts from Task 5.1:
1.  **Design & Create Vector Assets (SVGs):**
    * **Background Textures:** Develop 1-2 subtle vector patterns (e.g., low-opacity polygonal mesh with thin lines and small nodes).
    * **Section Dividers:** Create 1-2 minimalist SVG divider styles (e.g., thin line fragments with small angular/hexagonal accents).
    * **Spot Illustrations/Glyphs:** Design the 3-5 abstract glyphs (e.g., Data-Music Fusion Glyph, Blockchain Chain-Link Segment, Leadership/Growth Abstract Mark). Ensure they are single-color line-art (or exceptionally minimal dual-tone if pre-approved for specific domain accents), consistently sized (e.g., target ≤32x32px viewbox), and use uniform stroke weights (0.5px-1px). Use vector tools like Figma, Illustrator, or Inkscape.
2.  **Implement Dark/Light Mode Adaptability in SVGs:**
    * For each SVG, embed a `<style>` block with `prefers-color-scheme` media queries to automatically adjust `fill` or `stroke` colors based on the OS/browser theme preference. Alternatively, ensure paths are structured so their colors can be controlled by CSS Custom Properties inherited from the parent HTML context.
3.  **Optimize SVGs:**
    * Run all created SVGs through SVGO with an optimized configuration (e.g., remove metadata, cleanup IDs, merge paths, convert colors to hex) to minimize file size (aim for ≤5KB per graphic where feasible).
Organize these optimized SVGs in the designated project asset folder (e.g., `/src/assets/custom-graphics/`).

<definition_of_done>
* All planned custom graphic elements are created as SVGs.
* SVGs are optimized using SVGO and meet file size targets where possible.
* SVGs are designed to adapt to dark/light modes either internally or via external CSS.
* The collection of SVGs is committed to the repository (`P5_Custom_Graphic_Elements_SVG_Optimized.zip` or equivalent folder commit).
</definition_of_done>
Why this is important: High-quality, optimized, and themable custom graphics will significantly elevate the portfolio's unique Palantir-inspired visual identity."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="ASSET_COLLECTION">`P5_Custom_Graphic_Elements_SVG_Optimized.zip` (or commit link to the SVG assets folder).</expected_artifact>
</task>

### Task 5.4: Implementing Global Styles, BlueprintJS Overrides, Utility Classes & Integrating Custom Graphics
<task id="5.4_ImplementGlobalThemingAndCustomGraphicsIntegration">
  <objective>To apply the design token system to global HTML elements, create specific and maintainable style overrides for BlueprintJS components, define a minimal set of Palantir-themed utility classes, and integrate the custom graphic elements into the site's styling, as per `Optimal_CSS_Architecture_For_Palantir_BlueprintJS.md` and `Custom_Graphic_Elements_For_Palantir_Aesthetic.md`.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, with the design tokens and custom graphics ready, let's implement the full Palantir theme:
1.  **Apply Global Styles:** Using the design tokens, style base HTML elements (`html`, `body`, headings, paragraphs, links, lists) in your global CSS file. Ensure default text color, background color, and font families are set from `--palantir-*` variables. Enforce minimalist text formatting from the Content Strategy.
2.  **Implement BlueprintJS Component Overrides:** This is a critical step. Based on your chosen CSS architecture and `Optimal_CSS_Architecture_For_Palantir_BlueprintJS.md`:
    * If recompiling BlueprintJS SASS: Inject your CSS Custom Properties into Blueprint's SASS variables (e.g., `$pt-dark-bg3: var(--palantir-bg-dark); $pt-intent-primary: var(--palantir-accent-blue);`).
    * If using CSS overrides: Create scoped override files (e.g., `styles/components/Button.css`, `Dialog.css`) targeting Blueprint classes (e.g., `.bp3-button.palantir`, `.bp3-dialog.palantir-dialog`). Use your design tokens for all color, typography, spacing, border, and shadow properties. Ensure interactive states (hover, active, disabled, focus) are meticulously styled using stateful tokens (e.g., `--palantir-button-bg-hover`). Manage specificity carefully (e.g., using `&&` in CSS-in-JS if needed).
3.  **Define Utility Classes:** Create a small, purposeful set of Palantir-themed utility classes (e.g., `.u-text-accent-blue { color: var(--palantir-accent-blue) !important; }`, `.u-bg-panel { background-color: var(--palantir-bg-panel); }`, responsive utilities like `.u-hide-on-mobile`).
4.  **Integrate Custom Graphic Elements:**
    * Implement subtle background textures using CSS `background-image` with `url()` pointing to your optimized SVGs, controlling opacity and tiling.
    * Place SVG section dividers in relevant layout components or page templates.
    * Integrate spot illustrations/glyphs where planned (e.g., next to 'Stat Callouts', in component headers), ensuring they are accessible (`aria-hidden="true"` or `role="img"` with `aria-label`).
    * Verify all custom graphics respond correctly to dark/light theme changes based on their internal styling or inherited CSS variables.
Commit these extensive styling implementations.

<definition_of_done>
* Global styles correctly apply design tokens.
* BlueprintJS components are comprehensively and accurately themed to the Palantir aesthetic using the chosen override strategy.
* All interactive states of BlueprintJS components are correctly styled.
* A minimal, effective set of utility classes is defined.
* Custom graphic elements (backgrounds, dividers, glyphs) are integrated and correctly themed for dark/light modes.
* Code is committed and well-organized according to the chosen CSS architecture.
</definition_of_done>
Why this is important: This task brings the Palantir visual design to life across the entire application, ensuring every element, from a button to a complex dialog, reflects the desired aesthetic and quality."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="CODE_COMMIT">Commit hash for `P5_Global_Styles_And_Blueprint_Overrides.css_or_scss` and custom graphics integration.</expected_artifact>
  <expected_artifact type="SCREENSHOT_EXAMPLES_OR_STORYBOOK">`P5_Custom_Graphics_Integration_Examples` demonstrating integrated graphics in themed components.</expected_artifact>
</task>

### Task 5.5: Implementing All Theme & Accessibility Toggles Functionality
<task id="5.5_ImplementAllThemeTogglesFunctionality">
  <objective>To create fully functional UI controls in the global header for switching between dark/light modes and all defined accessibility themes (e.g., high-contrast, warm-dark), ensuring user preferences are persisted, as per `Optimal_CSS_Architecture_For_Palantir_BlueprintJS.md`.</objective>
  <prompt_to_developer>
    <instruction_for_claude>You (Claude 4) will say this to the Developer:</instruction_for_claude>
    <prompt_text>
"Developer, implement the complete theme and accessibility toggle functionality:
1.  **UI Controls:** Place BlueprintJS-styled toggle switches or icon buttons in the global header for:
    * Dark Mode / Light Mode.
    * High-Contrast Mode (if tokens and styles are defined for `.accessibility-high-contrast`).
    * Warm Dark Mode (if tokens and styles are defined for `.accessibility-warm-dark`).
2.  **JavaScript Logic for Theme Switching:**
    * Write robust JavaScript to toggle the appropriate CSS classes on the `<html>` or `<body>` element (e.g., `.theme-light`, `.theme-dark`, `.accessibility-high-contrast`, `.accessibility-warm-dark`).
    * Ensure that your CSS Custom Property definitions within these theme classes correctly override the default tokens (e.g., `:root.theme-light { --palantir-bg: var(--palantir-bg-light); /* ...other light tokens */ }`).
3.  **Persistence:** Use `localStorage` to save the user's selected theme (dark/light) and any active accessibility theme settings. Reapply these preferences on subsequent page loads.
4.  **Thorough Verification:** Test extensively:
    * All themes apply correctly across global styles, all key BlueprintJS components, and all custom graphic elements.
    * Toggling one theme doesn't negatively impact others.
    * Preferences are correctly saved and restored.
    * All theme combinations maintain required accessibility contrast ratios as per `Advanced_Accessibility_Techniques.md`.

<definition_of_done>
* All planned theme toggles (dark/light, accessibility themes) are implemented and functional.
* UI controls for toggles are styled according to Palantir/BlueprintJS.
* JavaScript logic correctly applies theme classes to the root element.
* CSS Custom Properties correctly override defaults for each theme.
* User preferences for all themes are persisted via `localStorage`.
* All theme combinations are visually correct and meet accessibility contrast standards.
</definition_of_done>
Why this is important: Providing user control over themes, especially for accessibility, is crucial for a high-quality, inclusive user experience."
    </prompt_text>
  </prompt_to_developer>
  <expected_artifact type="FEATURE_DEMO_SCREENSHOT_OR_GIF">`P5_Theme_And_Accessibility_Toggle_Functionality_Done` (Screenshots/GIFs demonstrating all functional theme and accessibility toggles and their comprehensive effects across various UI elements).</expected_artifact>
</task>

</tasks_for_claude>

## 4. Check-In & Progress Verification

<check_in_guidance>
* **End of Phase 5 Check-In: Comprehensive UI Asset, Theming, and Custom Graphics Review**
    <check_in_prompt>
        <instruction_for_claude>You (Claude 4) will use this prompt to request all final Phase 5 artifacts:</instruction_for_claude>
        <prompt_text>"Developer, this is a major review point. Please submit for review:
        1. Your finalized `P5_Asset_Management_And_Optimization_Plan_Final.md`.
        2. Your `P2_Chosen_CSS_Architecture.md` and evidence of its setup (`P5_CSS_Architecture_Setup_Done`).
        3. The implemented `P5_Design_Token_System_CSS_Variables.css`.
        4. The codebase for `P5_Global_Styles_And_Blueprint_Overrides.css_or_scss`.
        5. The collection of `P5_Custom_Graphic_Elements_SVG_Optimized.zip` (or link to folder).
        6. Demonstrations/screenshots of `P5_Custom_Graphics_Integration_Examples`.
        7. A full demonstration of the `P5_Theme_And_Accessibility_Toggle_Functionality_Done`.
        I will be conducting a thorough review (`P5_CSS_Graphics_And_Theming_Review.md`) to ensure every aspect aligns with our detailed Palantir aesthetic and technical guidelines."</prompt_text>
    </check_in_prompt>
    <artifact_review_process>
      <step>Claude 4 receives all artifacts and live demonstrations.</step>
      <step>Claude 4 states review focus: "I am conducting a comprehensive review to verify:
        * The asset plan is finalized and all assets (standard and custom graphics) are managed according to plan.
        * The chosen CSS architecture is correctly implemented and supports maintainable theming.
        * The design token system is robust, comprehensive for all themes (dark, light, accessibility), and accurately reflects Palantir color palettes (e.g., #1F1F1F, #0052CC, #FFD60A), typography (Inter/Roboto), etc.
        * Custom graphic elements are well-designed, optimized, integrated, and correctly adapt to all themes.
        * BlueprintJS components are meticulously and accurately themed to the Palantir aesthetic using the token system, without unintended global conflicts.
        * All theme and accessibility toggles are fully functional, persistent, and maintain accessibility contrast standards in all states.
        * The overall visual implementation achieves the sophisticated, minimalist, and data-centric feel of the Palantir brand."</step>
      <step>
        <condition>If all aligned:</condition>
        <claude_response>"Phase 5 is complete. This is outstanding work. The asset pipeline is solid, the CSS architecture and design token system are robustly implemented, custom graphics are beautifully integrated, and the Palantir theme, including all accessibility variations, is flawlessly applied to BlueprintJS and global styles. The visual foundation of Sulayman's portfolio is exceptionally strong. Approved. We are now ready to move to Phase 6: Interactivity Strategy."</claude_response>
      </step>
      <step>
        <condition>If revisions needed:</condition>
        <claude_response>"Revisions are needed to perfect the UI assets and theming:
        * For Custom Graphics Integration: `[e.g., 'The Data-Music Fusion Glyph SVG appears slightly misaligned when the Warm Dark Mode accessibility theme is active. Please check its positioning or color application under this theme.']`
        * For BlueprintJS Theming: `[e.g., 'The hover state on BlueprintJS Tooltips doesn't seem to be picking up the correct `--palantir-accent-blue-hover` token; it's defaulting to a standard Blueprint color. Please investigate the override specificity.']`
        * For Design Tokens: `[e.g., 'The CSS custom property for --palantir-shadow-level-3 seems to be missing from the tokens.css file, though it was referenced in the style guide for elevated cards.']`
        Please address these points and provide updates for a final review."</claude_response>
      </step>
    </artifact_review_process>
</check_in_guidance>

## 5. Prompt-Engineering Best Practices for Claude 4 (Self-Audit)

<self_audit_checklist>
* **Agentic Proactivity & Cross-Phase Consistency:** Have I proactively verified that the CSS architecture and design tokens implemented here fully support the component architecture defined in Phase 4 and the visual style guide from Phase 2?
* **Deep Research Synthesis:** Is my guidance to the Developer fully saturated with specifics from `Optimal_CSS_Architecture_For_Palantir_BlueprintJS.md` (e.g., ITCSS layers, BEM for overrides, SASS recompilation vs. CSS overrides) and `Custom_Graphic_Elements_For_Palantir_Aesthetic.md` (e.g., SVG optimization with SVGO, `prefers-color-scheme` in SVGs)?
* **Precision in Technical Detail:** Am I using precise terminology when discussing CSS Custom Properties, design tokens, BlueprintJS class targeting, SVG optimization, and theme switching logic?
* **Emphasis on BlueprintJS Customization Nuances:** Am I clearly guiding the Developer on the challenges and best practices for deeply customizing a comprehensive library like BlueprintJS while maintaining code health?
* **Accessibility as a Core Theming Requirement:** Does my guidance consistently ensure that all themes (dark, light, warm-dark, high-contrast) are designed and implemented to meet or exceed accessibility contrast standards?
* **Iterative Visual Review Cycle:** Am I prepared to guide the Developer through potentially multiple cycles of visual review and refinement for this highly detailed theming and custom graphics work?
</self_audit_checklist>

</claude_guide_phase>
