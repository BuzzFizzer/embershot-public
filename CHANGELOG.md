# Embershot Release Notes

All notable user-facing features, improvements, and bug fixes across Embershot releases.

## v1.6.0 (2026-11-24)

> Live CSS Studio, local MP4/WebM Video Bay, Alt+0 Flight Recorder, BYO R2/Webhook push, and SVG minifier.

### Features
- Added a Shadow DOM Live In-Page CSS & DOM Studio with hover redlines, breadcrumbs, visual/raw CSS & live text editing, Undo/Redo, Tailwind v4 mapping, and 1-click Before/After Studio Compare.
- Added an integrated Studio MP4/WebM + Microphone Video Bay with zero new permissions, IndexedDB & Encrypted Vault storage, In/Out trim, GIF conversion, and Snap Still Frame to Studio.
- Added a session-scoped Console, Network, Core Web Vitals & Breadcrumb Flight Recorder (Alt+0) with Reload & Record Boot, secret scrubbing, and automatic Evidence Bundle inclusion.
- Added 1-click zero-auth GitHub, GitLab, Linear & Jira issue handoff plus optional Bring-Your-Own Slack/Discord Webhooks and WebCrypto AWS4 S3/Cloudflare R2 direct upload (Settings -> 06 · Integrations).
- Added a zero-dependency pure-TypeScript SVG Minifier in Page Assets & SEO (Alt+5) and a cycling Post-Capture Quick Route bar in the zero-scroll Popup.

### Improvements & Changes
- Upgraded Full-Page and Element scroll stitching to score inner scroll containers even when body overflows slightly, traverse open Shadow DOM roots, stitch self-scrolling panes, and disable scroll-snap seams.
- Expanded passive page performance telemetry to capture TTFB, FCP, LCP, CLS, transfer size, and slow resources alongside failed HTTP statuses.
- Added Encrypted Vault AES-256-GCM support and quota accounting for recorded video clips.

### Bug Fixes
- Fixed Element capture mode scrolling window instead of el.scrollTop when snapping self-scrolling overflow-y panes on multi-pane dashboards.
- Prevented CSS scroll-snap-type mandatory rules from snapping mid-slice and duplicating full-page capture seams.

## v1.5.0 (2026-11-17)

> Optical searchbars, 1,300+ Tech Stack & Proof, live Link Health, SVG fixes, multi-Locate, and Replace Image Text.

### Features
- Overhauled all 12 searchbars into Optical Telemetry Bars with reticle wells, top scanline glow, live match counters, Escape-to-clear, and global / quick-focus.
- Expanded Tech Stack detection to 1,300+ signatures across 16 categories (including AI & LLM) with a per-framework Detection Proof modal and 1-click Copy.
- Added live per-URL Link Health streaming with an active URL ticker, pulsing CHECKING cards, smart auto-follow, same-origin auth fallback, and a Restricted (401/403) status filter.
- Added multi-occurrence Locate on Canvas across Design System Colors, Typography, Shadows, and Shapes, highlighting every match simultaneously and cycling 1/N on repeat clicks.
- Added a Patch Fill color picker, 1-click DOM text hit-testing, empty-string blanking, and auto-expanding patches to Replace Image Text, plus 2-column HTML Evidence Bundles, Google Fonts launcher, and stroke opacity.

### Improvements & Changes
- Upgraded Pro Upgrade modal plan cards with hover bleed clearance, billing value pills, persona callouts, and 6 concrete capabilities per tier alongside uniform full-height tabs and a one-time crypto notice.
- Made Detected Tech Stack collapsible and collapsed by default in Image Info, and updated the 4 Image Info metadata cards to recessed accent-bordered cards.
- Added smart per-tile Checker contrast for monochrome white and black SVGs in Page Assets & SEO.
- Removed summary/spec canvas-pinning buttons from Page Assets & SEO, Design System Tokens, Cookies & Web Storage, and Page Links while preserving visual Broken Link box pinning, and synced the public companion repo.

### Bug Fixes
- Fixed empty standalone inline and sprite SVGs in Page Assets & SEO by rewriting computed URL paint-server IDs, preserving black fills under fill='none' ancestors, stripping hidden sprite styles, and inlining SVG2 CSS geometry.
- Fixed false HTTP 403 link-check failures on valid links via browser-standard Accept headers, expanded HEAD-to-GET status fallbacks, same-origin live-tab probing, and non-broken Restricted classification.
- Fixed Replace Image Text dropdown node selection, persistent Brush/Marker stroke opacity across sessions, and Popup Trial countdown badge clipping.

## v1.4.0 (2026-11-10)

> Live screenshot progress HUD, rate-safe link verification, collapsible Tech Stack, and unified recessed callout cards.

### Features
- Added a live on-page Screenshot-in-Progress HUD across Visible, Full-Page, Region, and Element modes with slice progress, countdowns, Cancel, and rAF shutter hiding.
- Added collapsible framework category groups with Expand / Collapse All controls in Tech Stack & Frameworks.
- Added Cancel and 1-click Retry 429 actions to Page Links & Health with a dedicated Rate Limited warning badge.

### Improvements & Changes
- Unified EmptyState, Inspector empty states, DOM CSS Telemetry header icon, and modal intro banners around recessed accent-bordered cards.
- Removed canvas stack-card pinning from Tech Stack & Frameworks and hid the export bar when zero technologies are detected.
- Deferred same-origin response-header probing until after pixel capture for instant screenshot shutter response.
- Updated Pro tier pricing to $5.99/mo, $29.99/yr (Save 58%), and $69.99 one-time Lifetime.

### Bug Fixes
- Eliminated chrome-extension:// CORS errors when capturing or recording over cross-origin CDN GIFs and page assets.
- Prevented HTTP 429 bursts during link verification via #hash deduplication, per-host round-robin pacing, and Retry-After backoff.

## v1.3.0 (2026-11-03)

> 24-guide interactive overhaul, Demo Samples folder, click-through spotlight, and completion tracking.

### Features
- Expanded the Interactive Guide library to 24 workflows with new guides for Capture Modes & GIF Hydration, Explorer Capture Folders, Encrypted Private Vault, Crop/Markup/Dual Eraser, GIF Studio, and Command Palette/Shortcuts/Permissions.
- Added persistent Demo Samples seeding into a dedicated Demo Samples folder (SaaS v2/v1 compare pair, Chroma card with letter holes, and a 4-frame animated GIF89a) so guides work even in an empty Studio.
- Rebuilt the spotlight engine with a live 4-pane click-through cutout so highlighted controls stay interactive without closing the guide, plus ResizeObserver, modal, dock, and Arabic RTL collision-free card placement.
- Added guide launch triggers to Command Palette (Ctrl+K), a rebindable F1 Studio shortcut, Empty Studio, Tool/GIF/Compare Docks, and Popup Quick Settings.

### Improvements & Changes
- Replaced 4-per-page Guide Catalog pagination with a pinned search and 5-category filter bar above a scrollable 2-column grid with persistent X/24 completion badges.
- Retired the legacy YouTube/video walkthrough player and hardened extension CSP in favor of 100% local, click-through interactive Studio guides.

### Bug Fixes
- Fixed broken guide targets, mismatched Overview Tour step descriptions, missing staged PII/broken-link/GIF states, and un-reverted Chroma/X-Ray preview toggles when closing a guide.
- Fixed the DOM & CSS Telemetry inspector header quick-launch button opening the wrong guide.

## v1.2.1 (2026-10-27)

> Vault & Explorer folders, 4-tab Shortcuts, dual-edge card accents, and refresh persistence.

### Features
- Overhauled Capture Folders into an in-list Explorer directory with color-coded tactile rows, mini thumbnail peeks, count badges, root decluttering, and a sticky Back breadcrumb bar.
- Added zero-knowledge Encrypted Vault Folders: move entire folders into the Vault with AES-256-GCM encrypted folder metadata, browse folders inside unlocked Vault view, or restore folders back to the buffer.
- Added a non-empty Folder Deletion choice dialog so users can choose between moving captures back to All or permanently deleting both the folder and its captures.
- Reorganized Studio Keyboard Shortcuts into 4 single-row category tabs (Tools, Canvas & History, Inspector, Workspace & Export) with live search filtering and per-binding reset buttons.
- Persisted the active Studio capture (and open folder view) across page refreshes and Studio reopens while automatically prioritizing newly taken captures.

### Improvements & Changes
- Redesigned the Optical Buffer selected capture card indicator into a top-right corner 30% feathered accent (top-end right-to-left and end-edge top-to-bottom) paired with a subtle neutral hover lift.
- Introduced raised 2px-accented hardware cards inside recessed wells across Studio Settings, Popup Quick Settings, Keyboard Shortcuts, Release Notes, and Inspector helper callouts, and downsized shortcut item titles.
- Streamlined Version History & Release Notes to three single-line tabs (Features, Changes, Bug Fixes) with numbered tactile cards.

### Bug Fixes
- Fixed duplicate checkmarks appearing on Copy and Apply buttons across Custom Swatches, Image Info, Evidence Export, and Crop subbars.
- Fixed top version switcher buttons in Release Notes having their bottom hardware lips and hover lifts clipped, and centered the Capture Folders header label beside its icon.

## v1.2.0 (2026-10-20)

> Region GIF recording, faster Firefox modals, tabbed release notes, and sharper Studio tools.

### Features
- Added interactive Region GIF Recording inside the region picker with an outside-region Stop HUD that opens straight into the GIF Timeline Editor.
- Added Selected-Object controls in Select (V) mode with Tab/Shift+Tab annotation cycling, Hold-O Peek Original, 1-click X-Ray Crop & Spotlight, Retina <img> copy, PNG drag-out, and expanded Dev/Cloud secret PII presets.
- Added Width × Height numeric controls, aspect-ratio lock, and truly borderless mode for the Optical Loupe tool.

### Improvements & Changes
- Standardized all Studio and Popup modals onto unified sm, md, and lg size tiers.
- Switched the Release Notes modal to tabbed category navigation with a raised release date badge and concise at-a-glance summaries.
- Opened both Chroma Key and Advanced Chroma Refinement cards by default with independent ON/OFF switches, auto-enable on interaction, and an on-canvas draggable Before/After split line.
- Pinned top controls and search filters above full-height bordered scrollable lists across Links, Tech Stack, Cookies & Storage, Assets & SEO, and Design System Tokens, and removed the Vault UNLOCKED badge.

### Bug Fixes
- Eliminated severe modal opening lag in Firefox by bypassing full-viewport backdrop-blur readbacks in Gecko, optimizing dialog focus-trap checks, teleporting all dialogs, and deferring canvas PNG readbacks.
- Fixed Loupe lens and selection box detaching when dragged against or outside screenshot edges by clamping both to active screenshot bounds.
- Fixed the DOM Hierarchy Tree jumping vertically when hovering elements in DOM CSS Telemetry.

## v1.1.1 (2026-10-13)

> Added right-click copying inside modals and stabilized the Release Notes window.

### Features
- Added dialog-scoped right-click Copy and Select All actions across Studio and Popup modals with toast confirmation.
- Added right-click Copy Section and Copy Release Notes (Markdown) menu actions inside the Release Notes modal.

### Improvements & Changes
- Replaced the version number on the lower Right Rail trigger with the Lucide ScrollText icon and localized Release Notes label when expanded.
- Raised ContextMenu z-index stacking (z-130 / z-135) above modals, selects, color pickers, and notification toasts, and coordinated dialog focus traps with open menus.

### Bug Fixes
- Fixed right-click context menus opening invisibly behind lazy-mounted z-100 modals such as StudioChangelogModal.
- Fixed Select All inside modals targeting the background page instead of the active modal body container.
- Fixed Release Notes modal resizing vertically when switching between v1.1.1, v1.1.0, and v1.0.0.

## v1.1.0 (2026-10-06)

> Faster GIF playback, viewport-smart dropdowns, unified tool docks, and crisp SVG previews.

### Features
- Added Extension Versioning and a fixed-height Release Notes modal triggered from the lower Right Rail icon with an unseen-update indicator dot.
- Added global body-teleported Select dropdown panels with viewport boundary clamping, auto-flip collision detection, and RTL-aware alignment.
- Upgraded GIF playback with ImageBitmap decoding, background idle frame pre-warming, drift-compensated frame pacing, and lazy 160 px hover thumbnails.
- Hardened Full-Page GIF capture with taint-safe and CSP-safe canvas freeze overlays plus a best-slice patch pass for CSS background GIFs and late video frames.
- Upgraded Page Assets preview cards with a persisted Checker / Light / Dark backdrop toggle and broken-image fallback.
- Redesigned Input controls with a CNC recessed-well chassis, top-edge focus hairline, embedded icons, clear button, and matched height alignment.

### Improvements & Changes
- Moved the Language selector from the Right Rail into the Studio and Popup headers (PRO | Theme | Language | Settings) with mutually exclusive popovers.
- Unified Tool Controls, GIF Edit & Trim, and Compare docks (w-9 collapsed tab, SlidersHorizontal header, w-56 / w-64 chassis) with zero internal scrollbars.
- Moved the Canvas Minimap cleanly to the opposite edge (inset-s-4) whenever any right-edge dock is expanded.
- Matched height parity (28px / 32px) across all Input and adjacent Button pairs and embedded search icons inside filter inputs.
- Updated Pro Lifetime tier pricing to $34.99 one-time.

### Bug Fixes
- Fixed blank inline SVGs in Page Images, SVGs & SEO by resolving same-document <use> sprites, defs, computed styles, CSS variables, currentColor, and viewBox/dimensions.
- Fixed Text Replace Image Text dropdown menu clipping and subbar scrolling by teleporting Select overlays to document.body.
- Fixed Page Links & Health list stopping short at 420px inside the Right Inspector.
- Fixed solo GIF Edit & Trim dock scrollbar and bottom-clamped full-page overlap slicing over animated GIFs.

## v1.0.0 (2026-09-29)

> First release of Embershot with multi-mode capture, Studio editing, and 9-format export.

### Features
- Viewport, Full-Page, Region, DOM Element, and manual image upload capture modes.
- 14-tool non-destructive canvas Studio with PII Auto-Redact, Chroma Key BG removal, Presentation Chassis, and Compare workspace.
- Dedicated multi-frame GIF timeline editor with delay adjustment, trim bounds, reverse, boomerang, and lossless raw passthrough.
- Right Inspector suite for DOM CSS Telemetry, Design System Tokens, Page Assets & SEO, Tech Stack, Links, Cookies, and QA Issues.
- Local 9-format exporter & batch converter (PNG, WEBP, JPEG, AVIF, BMP, Hybrid Vector SVG, GIF, ICO, PDF).

### Improvements & Changes
- Local IndexedDB blob storage and Encrypted Vault protection paired with tactile hardware themes across 9 locales.

### Bug Fixes
- Initial baseline release hardening for Chrome MV3 and Firefox MV3.
