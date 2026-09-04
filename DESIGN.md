---
version: alpha
name: "CODEV"
description: "A software development studio presented as a measured build log: heavy typography, interface light, and one signal-orange progress marker."
colors:
  ink: "#000000"
  ink-2: "#07090D"
  glacier: "#F2F4F1"
  white: "#FAFBFA"
  accent: "#FF4D00"
  text-dark: "#E9EDF2"
  text-light: "#12161D"
typography:
  display:
    fontFamily: "Archivo, system-ui, sans-serif"
  body:
    fontFamily: "Archivo, system-ui, sans-serif"
  mono:
    fontFamily: "Space Mono, ui-monospace, monospace"
rounded:
  DEFAULT: "2px"
  pill: "99px"
spacing:
  page-gutter: "4vw"
  section-y: "8rem"
  hairline: "1px"
components:
  navigation:
    treatment: "fixed, blend-mode difference, quiet until hovered"
  cta:
    treatment: "underlined text link with orange reveal and magnetic hover on fine pointers"
  waypoint-rail:
    treatment: "fixed hairline rail with diamond waypoints and orange progress marker"
  image-frame:
    treatment: "square-edge crop with restrained scale/parallax and no decorative card chrome"
---

# CODEV Design System

## Overview

### Creative North Star

CODEV should feel like reading a build log at the moment a product becomes real: low light, precise signals, interface states turned into a severe digital instrument. It is a brand-led landing page for people choosing a software partner, not a generic agency brochure.

### Product context and register

- **Audience and primary job:** Founders, product teams, and organizations deciding whether Codev is the right software partner and moving toward a project conversation.
- **Target market(s) and evidence:** English-language software buyers; the current page copy is positioned around websites, web apps, mobile apps, digital products, and custom software.
- **Locale(s) and language policy:** English content with technical terms preserved in their familiar spelling; no locale switch is currently implemented.
- **Usage scene:** Visual browsing on desktop or phone, often with image-heavy scrolling; key information must remain readable without hover or motion.
- **Register:** Brand / editorial landing page.
- **Memorable signature:** The build rail: a visible phase instrument that turns the page into a software journey, with the single pinned “THE BUILD” sequence as its launch moment.
- **Restraint:** Navigation, copy, and service information stay sparse and typographic; orange is reserved for phase markers, actions, and live status.
- **Anti-references:** Generic luxury travel, glossy adventure-tourism gradients, rounded SaaS cards, and dashboard-like metric grids.
- **Rebrand staging:** The supplied white Codev mark is integrated in the fixed navigation and the page copy now uses the Codev software-studio narrative. The supplied mountain imagery remains temporarily until the asset pass.
- **Token ownership/runtime mapping:** This file documents the tokens implemented in the inline `:root` block in `index.html`; that stylesheet is the runtime source for this static one-page site. If the page becomes multi-route, extract these values into a shared stylesheet and keep this mapping current.

## Colors

The page uses a solid black field `#000000` and footer night `#07090D` as its primary atmosphere. Glacier `#F2F4F1` and white `#FAFBFA` create the light / signal turn. Signal orange `#FF4D00` is expressive and semantic: it marks actions, live progress, build waypoints, and the product's decisive moments. Text-dark `#E9EDF2` and text-light `#12161D` preserve contrast on their respective surfaces. Keep the contrast-first scrollbar and keyboard focus treatment visible on every theme.

## Typography

Archivo carries both display and body, using its width axis and heavy weights for the compressed wordmark and section statements. Space Mono is reserved for phase, progress, labels, and other instrument-like data. Display copy is uppercase; prose remains sentence case. The current site is English-only, with system fallbacks preserving a usable result if Google Fonts is unavailable.

## Layout

The page uses full-width sections with a fluid side gutter, hairline opening rules, and long vertical travel that mirrors a product moving from idea to release. The hero is viewport-height; “THE BUILD” owns the page's only intentional pin. Desktop layouts use editorial two-column compositions, while the existing breakpoints collapse them to one column below tablet widths. Intrinsic image dimensions and aspect ratios reserve media geometry before remote images load. Native scrolling remains available alongside the custom rail.

## Elevation & Depth

Hierarchy comes from tonal shifts, crop, overlap, blend modes, and occasional image shadow rather than card stacks. The build line and phase rail are the main depth devices. Cards, rules, and product imagery remain visually quiet; avoid adding generic drop shadows or glassmorphism.

## Shapes

The visual language is almost square: `2px` is the default radius and the intentional exception is the `99px` live-state pill. Dividers are one-pixel hairlines. Waypoints and the favicon use diamonds / triangles, echoing technical system notation; the Codev mark is a separate white raster brand asset used in navigation.

## Components

### Foundational visual states

Interactive links and buttons retain a visible underline or border, gain an orange hover transition, and keep a clear keyboard focus ring. Reduced-motion mode removes smooth scrolling, pinned sequences, and reveal choreography while preserving the full content and final visual state.

### Buttons and actions

The supplied page uses text CTAs rather than a button library. Actions are native anchors, named by their destination: “START A PROJECT” and section links. Orange communicates the action without being the sole cue; the underline and arrow remain present.

### Navigation and data display

The fixed navigation is minimal and paired with the phase rail. Tables and project rows are read-oriented, with the full value available in the row itself; image previews enhance desktop hover but are hidden on smaller screens rather than becoming hover-only content.

### Forms and overlays

No application form or modal is currently present. The loader is an app-owned status layer and is removed when the document is ready; `noscript` exposes the page content without it.

### Iconography

Icons are inline SVGs or typographic marks already present in the supplied document. They use simple, technical geometry and never replace a text label for a primary action.

### Motion

The motion personality is one expo-out easing, with Lenis for weighted scroll and GSAP for the build choreography. Motion is concentrated in scroll reveals, the light crossfade, the phase rail, and the single pinned build sequence. `prefers-reduced-motion` and `?static` provide a no-motion path with content intact.

### Content and data visualization

Copy is concise, observational, and operational. Phase labels use short uppercase notation such as `03 DEVELOP`; progress uses percentages. Orange markers and build progress are paired with labels so state is not color-only.

## Do's and Don'ts

- **Do:** Let phase, progress, service type, and section labels carry real information.
- **Do:** Keep orange scarce so every orange mark feels like rope hardware or a deliberate action.
- **Don't:** Add rounded dashboard panels, gratuitous gradients, or extra animation systems.
- **Don't:** Hide the native scrollbar or make hover previews the only way to access content.
