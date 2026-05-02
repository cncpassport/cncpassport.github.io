---
layout: post
title: "Nesting Tools: Browser-Based Sheet Nesting for Rectangular Layouts"
date: 2026-05-02
categories: cnc-passport sheet-nesting dxf svg manufacturing
---

Nesting Tools is a browser-based CNC Passport service for preparing sheet cutting layouts. The initial version focuses on rectangular sheets and rectangular parts, which covers many everyday production and training cases: furniture panels, blanks, cabinet elements, simple fronts, process trials, and layout exercises.

![Nesting Tools demo image](/images/nest-tools.png)

The service is available at [nest.cncpassport.com](https://nest.cncpassport.com/).

CNC Passport and its services are proprietary projects. This public note describes the workflow and technical scope of the service; it does not publish the application source code.

## Problem Context

In sheet production, material waste can be introduced before any cutting begins. A layout may leave too much unused space, ignore the required distance from the sheet edge, omit kerf, or be saved in a form that is difficult to reuse later.

A fast nesting tool is useful when a user needs to answer practical questions before the job moves further into production:

- How many sheets are required for this part list?
- Can the required parts fit into the available sheet size?
- What happens if spacing, margin, or kerf changes?
- Is the result suitable for export into the next CAD/CAM or documentation step?

Nesting Tools is designed as a working layer between a layout idea and the next production action. It is not intended to replace a full manufacturing system. Its first role is narrower: prepare a clear layout, compare the result, and export it in a usable format.

## Current Technical Scope

The current version supports rectangular nesting scenarios:

- rectangular sheet width and height;
- rectangular part dimensions and quantities;
- spacing between parts;
- edge margins;
- kerf allowance;
- alternative placement strategies;
- sheet, material-use, and waste statistics;
- saving the result;
- export to DXF and SVG.

This scope is intentionally direct. Rectangular nesting is common in furniture production, panel processing, shop-floor planning, and training. It is also a useful first step because parameter changes are easy to inspect visually: a changed gap, margin, part size, or sheet size immediately affects the layout.

## DXF and SVG Export

Export is part of the first release because a layout should not remain only as a screen image.

DXF is useful when the layout needs to continue into a CAD/CAM chain or another internal workflow. SVG is useful for visual review, documentation, quick approval, and sharing a readable version of the layout.

Not every layout goes directly to a machine. In many cases, it first needs to be checked, discussed, archived, or compared with another option. Supporting both DXF and SVG keeps the result usable in technical and communication workflows.

## Practical Use Cases

Nesting Tools can be used for:

- estimating sheet requirements for a small order;
- checking whether a set of parts fits into an offcut;
- comparing layout strategies before cutting;
- preparing simple rectangular panel layouts;
- explaining material use in training rooms;
- documenting a layout for review or approval.

The training case is especially clear: when a learner changes spacing, rotates parts, or adjusts sheet size, the effect on material use becomes visible immediately. This helps explain why a layout that "almost fits" may still fail in production.

## Development Direction

The first release establishes the browser workflow for rectangular sheet cutting layouts. Future development is expected to move toward more complex contours, geometry import, improved placement strategies, and broader production scenarios.

The current public release article is available in the [CNC Passport Blog](https://cncpassport.com/blog/en/introducing-nesting-tools-new-cnc-passport-service-for-sheet-nesting/).

For the broader platform, visit [CNC Passport](https://cncpassport.com/).
