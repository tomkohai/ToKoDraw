---
title: Changelog
description: ToKoDraw changelog: release notes, new features, bug fixes and improvements for each version of the Blender addon.
---

## Changelog V0 - V1

### V0.1 — Core System (Initial Prototype)

Creation of the LF material system

First version of the layer system

Addition of the base nodes (Layer, NBAdd, Master)

Initial handling of internal images (TEX_IMAGE)

First version of the 2D canvas inside Blender

Beginning of the painting mode (Texture Paint + LF routing)

### V0.2 — Add / Remove / Reorder (Foundations of the Layer Stack)

Addition of the Add Layer button

Layer removal with proper node cleanup

Full stack reordering

Automatic renumbering of layers and NBAdd nodes

Fixes for LF indices (lf_index)

Automatic update of the merge map

Stabilization of the UID system for each layer

### V0.3 — Duplicate & Internal Image System

Addition of Duplicate Layer

CPU/GPU buffer handling for painted images

Fixes for TEX_IMAGE copy behavior

First version of straight anti‑halo

First version of soft correction

Introduction of the lf_is_processed flag

Stabilization of duplicate to avoid gray halos

### V0.4 — Merge (First Version)

Merge of checked layers

NumPy compositing (NORMAL, MULTIPLY, SCREEN, OVERLAY)

Per‑layer opacity handling

Automatic creation of a merged image

Automatic removal of merged layers

Merge map update after deletion

Automatic selection of the base layer

### V0.5 — Layer System Refactor & Normal Map Pipeline

Full refactor of the Layer/NBAdd system

Rewrite of get_real_layer_nbadd_chain

Stabilization of dynamic stacks

Fixes for UID/index offsets

Safe cleanup of visual labels

Canvas update after every operation

Fixes for GPU→CPU sync issues

Node pipeline for hand‑painted normal maps

Creation, assignment, and render mode switching for normal maps

### V0.6 — 2D Canvas Mode & Line Art Camera View

Addition of the 2D Canvas mode

Dedicated camera view for drawing

Object transform panel (scale/rotate/move)

Framing tools for 2D painting

Viewport stabilization for drawing

Fixes for canvas behavior in Texture Paint

### V0.7 — Outline & Auto Line Art

Addition of the automatic Outline system

Geometry‑based automatic Line Art

Automatic thickness adjustment

Fixes for 2D mode behavior

Integration into the LF stack

### V0.8 — Stabilized Straight Merge (Final Pipeline)

Full transition to a straight pipeline

Complete removal of internal premultiplied alpha

Stabilized straight anti‑halo

Conditional soft correction (lf_is_processed)

Merge without white halos

Merge without gray halos

Falloff preserved

Colors remain unmixed

Final stable pipeline

### V0.9 — UI & Panels

Layer management panel

Merge panel

Transform panel

2D camera panel

UI cleanup

Menu reorganization

Addition of warnings (merge popup)

## V1.0 — Final Version (Release)

Finalized straight pipeline

Stabilized duplicate

Stabilized merge

Complete layer system (Add, Remove, Reorder, Duplicate, Merge)

Fully functional 2D canvas

Automatic Outline & Line Art

Complete UI



# Chaglog V1 - V2

## 🔄 Update & Bug Fixes 

### V1.0.1

- Fixed: "Delete Line Art" naming issue after LF → TDK refactor (#2)
