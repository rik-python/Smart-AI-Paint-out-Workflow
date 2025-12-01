# 🧹 Smart AI Paint-Out Workflow (ComfyUI)

Watch demo and a video guide here - https://youtu.be/H__el-RhzuM

A powerful ComfyUI workflow that removes any object from video and generates clean, stable plates automatically — without Nuke, roto, or frame-by-frame paint-out.

Built using:

Wan 2.1 VACE Model – for ultra-stable video consistency

QWEN VL3 – auto-generates detailed, shot-specific prompts

Florence 2 – fast segmentation & point-guided mask proposals

SAM2 – refined, accurate, stable masks across the whole clip

This workflow is designed for real VFX use: reliable, repeatable, fast, and visually consistent.

✨ Features

Erase anything: actors, props, boom mics, shadows, unwanted objects

Stable clean plates: no flicker, no AI mush, no patchy fills

Auto prompt generation: QWEN VL3 analyzes your reference frame

Precision masking: Florence2 + SAM2 blend for clean tracking

Video-safe: Wan 2.1 maintains temporal consistency

ComfyUI-native: simple, modular node layout

🧠 How It Works (High-Level)

Load Your Video
Import the shot you want to clean up.

Pick a Clean Reference Frame
This becomes the “target plate” that the model reconstructs.

Auto-Generate the Prompt
QWEN VL3 analyzes the clean frame and produces a perfect video-style prompt.

Mark the Object to Remove
Add point markers (positive) on the unwanted object.

Mask Generation
Florence2 creates a segmentation proposal → SAM2 refines and stabilizes it.

Smart AI Paint-Out
Wan 2.1 fills in the missing region using the prompt + your clean plate reference.

Output Stable Clean Plate
Export as a video ready for comp or direct use in production.

🛠 Installation

Install the latest ComfyUI

Download required models:

Wan 2.1 VACE

QWEN VL3

Florence2

SAM2 masks

Place models into:

ComfyUI/models/checkpoints
ComfyUI/models/clip
ComfyUI/models/vision
ComfyUI/models/sam2


Load the .json workflow.

Drop your video → your clean frame → run!

🧪 Best Practices

Use at least 30–50 positive points for complex shapes

Add a slight mask expansion + blur for softer blending

Keep prompts simple and factual

If reconstruction is too smooth → add grain in comp

For moving cameras → use a stabilized input

🎯 Use Cases

Paint-out for VFX

Clean plates for DMP

Removing BG clutter on set

Quick continuity fixes

Removing shadows/boom mics

Projection prep in Nuke

Fast editorial cleanup

📁 Workflow File

👉 Download the full workflow here:
(Add your GitHub workflow JSON link)

🙏 Credits

Huge thanks to the creators of:

Wan 2.1

QWEN VL3

Florence2

SAM2

The entire ComfyUI community
