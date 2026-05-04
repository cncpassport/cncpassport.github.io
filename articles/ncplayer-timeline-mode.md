---
layout: post
title: "Timeline Mode in NCPlayer: Reviewing CNC Program Execution Over Time"
date: 2026-05-04
categories: ncplayer gcode-simulation cnc-programming
---

NCPlayer Timeline Mode is a program viewing feature for inspecting CNC program execution as a sequence of movements over time.

![NCPlayer Timeline Mode screenshot](https://cncpassport.com/blog/images/2026/05/ncplayer_timeline_mode-1.png)

## Problem context

When checking a CNC program, the risky part is not always one isolated G-code block. It may be the transition between blocks or states: a rapid move after a coordinate or mode change, movement after compensation, return motion, or a repeated subprogram call.

Reading the code and looking at the toolpath are both necessary, but they do not always make the execution order obvious.

## What Timeline Mode adds

Timeline Mode gives the user another view next to the G-code and toolpath. It helps show:

- where G00 rapid movements are located;
- where G01, G02 and G03 cutting moves begin;
- how the program moves between machining sections;
- which blocks appear before and after a mode change;
- where unexpected movement deserves closer review.

## Practical use cases

This view is useful during first program checks, after edits, during CNC training, and when a user needs to understand someone else's NC program quickly.

For a beginner, it also supports an important mental model: a CNC machine does not execute definitions in isolation. It executes a sequence of actions.

## Scope

Timeline Mode does not make a program automatically safe. It does not replace simulation, dry run, machine documentation, tooling checks, workholding checks, controller-specific limits, or local safety procedures.

It is one more inspection layer for understanding the program before real machine use.

## Links

- [Source article in CNC Passport Blog](https://cncpassport.com/blog/en/timeline-mode-in-ncplayer-viewing-a-cnc-program-over-time/)
- [NCPlayer](https://nc.cncpassport.com/)
- [CNC Passport](https://cncpassport.com/)
