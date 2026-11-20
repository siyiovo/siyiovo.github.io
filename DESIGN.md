---
name: Jinhua Deng Robotics Portfolio
description: A bilingual engineering portfolio for SLAM localization and motion control work.
colors:
  ink: "#17202A"
  ink-muted: "#52606D"
  canvas: "#F5F7F9"
  surface: "#FFFFFF"
  line: "#D8E0E7"
  cobalt: "#155EEF"
  cobalt-soft: "#E8F0FF"
  amber: "#C2410C"
typography:
  display:
    fontFamily: "Archivo, Arial, sans-serif"
    fontSize: "4rem"
    fontWeight: 600
    lineHeight: 0.96
    letterSpacing: "0em"
  body:
    fontFamily: "IBM Plex Sans, Arial, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "0em"
  label:
    fontFamily: "IBM Plex Mono, monospace"
    fontSize: "0.75rem"
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "0em"
rounded:
  sm: "4px"
  md: "8px"
spacing:
  sm: "8px"
  md: "16px"
  lg: "32px"
components:
  button-primary:
    backgroundColor: "{colors.cobalt}"
    textColor: "{colors.surface}"
    rounded: "{rounded.sm}"
    padding: "12px 18px"
  project-card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "24px"
---

# Design System: Jinhua Deng Robotics Portfolio

## Overview

**Creative North Star: "The Lab Notebook"**

The portfolio should feel like a clear engineering notebook opened for review: measured, legible, and grounded in real artifacts. The page uses editorial spacing and restrained visual signals so project evidence stays more prominent than decoration.

The surface is light, calm, and structured around strong type, thin rules, compact labels, and real repository imagery. It keeps the technical character in the content and typography rather than dressing every block as a control panel.

**Key Characteristics:**
- Chinese-first reading order with an explicit English route.
- Strong display typography for identity, readable sans-serif body copy, and mono labels for repository metadata.
- Light neutral canvas with cobalt and amber signals used sparingly.
- Flat surfaces with small radii and structural borders.

## Colors

The palette uses a cool paper-like canvas, dark ink, cobalt action signals, and amber for provisional or attention states.

### Primary
- **Cobalt action** (`#155EEF`): primary links, selected language, and direct actions.
- **Amber note** (`#C2410C`): example and unfinished states that need attention without looking like errors.

### Neutral
- **Ink** (`#17202A`): headings and primary text.
- **Muted ink** (`#52606D`): supporting text and metadata.
- **Canvas** (`#F5F7F9`): page background.
- **Surface** (`#FFFFFF`): project media and content surfaces.
- **Line** (`#D8E0E7`): dividers and quiet boundaries.

**The Signal Rule.** Cobalt and amber identify action or status; they do not decorate large areas.

## Typography

**Display Font:** Archivo (with Arial, sans-serif fallback)
**Body Font:** IBM Plex Sans (with Arial, sans-serif fallback)
**Label/Mono Font:** IBM Plex Mono (with monospace fallback)

**Character:** Archivo gives the name and section headings a compact technical voice. IBM Plex Sans keeps Chinese and English body copy readable, while IBM Plex Mono is reserved for project metadata and small technical labels.

### Hierarchy
- **Display** (600, `4rem` desktop / `2.875rem` mobile, `0.96`): the name and the lead statement.
- **Headline** (600, `clamp(2rem, 4vw, 3.5rem)`, `1.05`): major content sections.
- **Title** (600, `1.25rem`, `1.2`): project and subsection titles.
- **Body** (400, `1rem`, `1.6`): descriptions and project evidence, limited to approximately 70ch.
- **Label** (500, `0.75rem`, `1.4`, normal case): routes, dates, statuses, and repository metadata.

## Layout

The page uses a centered `min(1120px, calc(100% - 40px))` content frame. The first screen uses a two-column identity layout on wide screens and one column below 760px. Sections use a full-width band with an inner constrained frame; repeated project entries are separated by borders and spacing instead of stacked decorative cards.

The layout follows an 8px spacing rhythm. Body copy stays within 65–75ch. Media uses fixed aspect-ratio containers so images cannot shift surrounding content while loading.

## Elevation & Depth

The system is flat by default. Depth comes from canvas-to-surface contrast, thin borders, and modest image framing. Shadows appear only on interactive hover or focus states and remain soft with a visible offset.

## Shapes

Use 4px for controls and 8px for project surfaces. Avoid pill-shaped containers except for compact status labels. Borders are 1px and low contrast. Focus uses a 3px cobalt outline with a 2px offset.

## Components

### Skills
- **Structure:** Six evidence-oriented entries in a responsive grid: C++ / Python, ROS, PCL, State Estimation, Lie Theory, and Optimization.
- **Icons:** Local Lucide SVGs provide a consistent technical cue; skill names and supporting text remain visible.
- **State:** The section is informational and does not imply a proficiency score.

### Buttons
- **Shape:** 4px radius, minimum 44px height.
- **Primary:** cobalt background, white text, 12px by 18px padding.
- **Hover / Focus:** darken cobalt slightly; focus adds a visible outline without moving the element.
- **Secondary:** transparent surface with ink text and a line border.

### Project Entries
- **Shape:** 8px radius, flat white surface, 1px line border.
- **Media:** fixed 16:10 ratio, object-fit cover, descriptive alt text.
- **Metadata:** mono labels for status, technology, and source.
- **Action:** project title and explicit text link remain available without hover.

### Language Switch
- **Shape:** compact text control with 44px touch target.
- **State:** active language uses cobalt text and a bottom rule.
- **Behavior:** preserves the current page translation when available.

## Do's and Don'ts

- Do put project evidence close to the claim it supports.
- Do keep status labels honest and visible.
- Do use real repository imagery when available.
- Do preserve visible focus and reduced-motion behavior.
- Do not use gradients, emoji, fake metrics, or generic stock imagery.
- Do not make every section a floating card.
- Do not use monospace for all text; reserve it for technical metadata.
