# AOSSIE Project Videos Guide

A practical, step-by-step handbook for open-source contributors to produce high-quality product videos (Teasers and Explainers) for AOSSIE projects.

---

## 1. Teaser vs. Explainer

When creating a video for an AOSSIE project, first decide which type of video you are producing. Both serve distinct purposes, target different viewer states, and require different pacing.

### Teaser Video

* **Core Purpose**: Generate excitement, curiosity, and interest in the project.
* **Core Question Answered**: *"Why should I care about this?"*
* **Characteristics**:
  * **Short**: Typically 15 to 45 seconds.
  * **Fast-Paced & Energetic**: Quick visual cuts, high-energy music, punchy text callouts.
  * **Problem- & Value-Centric**: Highlights the frustration developers face and teases the solution.
  * **Selective**: Does not explain the technical inner workings or full feature set.
  * **Curiosity-Driven**: Leaves the viewer wanting to visit the repository or try the live demo.

> **Analogy**: A teaser is like a **movie trailer**—it gives you a taste of the plot and the best scenes to make you want to watch the movie, without giving away the ending.

---

### Explainer Video

* **Core Purpose**: Help viewers understand what the project actually is, how it works, and how it solves their problem.
* **Core Question Answered**: *"What is this, how does it help me, and what does it actually do?"*
* **Characteristics**:
  * **Clear & Methodical**: Typically 60 to 90 seconds (hard maximum: 120 seconds).
  * **Shows Real Product UI**: Must demonstrate the actual live application, CLI, or repository outputs—not abstract concept art.
  * **Feature Demonstrations**: Walks through 2 to 3 core workflows step-by-step.
  * **Guided Narration**: A clean, natural voiceover guides the viewer through the interface.
  * **Grounding**: Never relies on generic, AI-generated stock footage (e.g., floating tech cubes, stock business handshakes).

> **Analogy**: An explainer is like a **guided product walkthrough**—it respects the viewer's time by proving that the software works and showing exactly how to use it.

---

## 2. The Difference in One Table

| Dimension | Teaser Video | Explainer Video |
| :--- | :--- | :--- |
| **Primary Objective** | Create interest & curiosity | Create clear understanding |
| **Viewer Question** | *"Why should I care?"* | *"What is this and how does it work?"* |
| **Pacing** | Fast / Dynamic | Clear / Measured / Steady |
| **Duration** | 15–45 seconds | 60–90 seconds (max 120s) |
| **Level of Detail** | High-level summary | Practical, workflow-level detail |
| **Product UI Visibility** | Optional or quick hero snippets | **Mandatory** (at least 60% of runtime) |
| **Features Covered** | Hinted at / teased | Demonstrated with live interaction |
| **Viewer Reaction** | *"I want to check this out!"* | *"Now I understand how this solves my problem."* |


> **Neither format is "better"—they solve different problems.**  
> Do not attempt to force one video to do both jobs. A teaser that tries to explain technical features becomes sluggish; an explainer that moves at breakneck teaser speed leaves the viewer confused.

---

## 3. How to Create an Explainer Video: Step-by-Step

This workflow uses **[Arcade](https://app.arcade.software/)** for automated UI-aware screen capture, brand analysis, and pacing, combined with lightweight video editing tools for final community branding.


---

### Step 1 — Understand the Project

Before opening any recording software or writing prompts, study the project thoroughly:
1. **What does the project do?** (Summarize in one sentence without buzzwords).
2. **Who is it for?** (Open-source maintainers? Developers? GSoC students? General users?).
3. **What specific problem does it solve?** (What manual, painful task does it eliminate?).
4. **What are the top 2–3 features that prove this?** (Identify the exact screens or buttons).

---

### Step 2 — Create an Arcade Workspace & Setup Brand Kit

1. Navigate to **[app.arcade.software](https://app.arcade.software/)** and create a free account.
   * **Workspace Access & Credits**: AOSSIE does not provide access to a paid Arcade workspace, so contributors use individual free accounts. Arcade gives you **200 credits per month** on a free tier, which means you can create roughly **4 videos a month** (50 credits for generating each video). Importantly, **editing and prompting an existing video does not cost any extra credits**, whereas generating a video from scratch takes an extra 50 credits each time.
   * **H.264 MP4 Export & Watermark Policy**: Videos exported on the free tier include an Arcade watermark. Official AOSSIE project videos require a clean, watermark-free H.264 MP4. To remove the watermark before final submission:
     1. Export your completed video from Arcade.
     2. Visit [Online Video Cutter - Remove Watermark from Video](https://online-video-cutter.com/remove-logo).
     3. Choose and upload your video file.
     4. Highlight the area where the watermark is placed.
     5. Check the preview to ensure the underlying UI is clean, then export the watermark-free video.
2. In your workspace settings, set up a **Brand Kit**:
   * Paste the link to the deployed application (e.g., `https://aossie-org.github.io/OrgExplorer/` or local demo).
   * Arcade automatically scans the site to extract the project's color palette, typography, and logos.
3. **Why this matters**: Grounding the tool in your actual brand kit prevents generic video styles and ensures visual continuity across AOSSIE projects.

---

### Step 3 — Decide What the Video Must Communicate

Before drafting prompts or recording, define the **single takeaway statement**:

> *Example (OrgExplorer)*:  
> "After watching this video, a developer should understand that OrgExplorer transforms GitHub organization data into interactive visual dashboards to analyze contributor networks, repository health, and activity trends."

Once your statement is written, pick **only 2 to 3 core workflows** that provide visual proof of that statement:
* *Workflow 1*: Searching for an organization and loading real metrics.
* *Workflow 2*: Interacting with the contributor collaboration graph.
* *Workflow 3*: Viewing repository risk analysis (e.g., bus factor detection).

---

### Step 4 — Write the Generation Prompt

The prompt provides structure and constraints to Arcade's generator. A weak prompt yields generic AI stock visuals; a precise prompt enforces product accuracy.

#### Recommended Prompt Structure:
* **Video Purpose**: Product explainer walkthrough.
* **Target Audience**: Developers, open-source contributors, project maintainers.
* **Tone**: Professional, clear, engaging, developer-friendly.
* **Pacing**: Measured and easy to follow (approx. 130–140 words per minute).
* **Core Problem**: Hard to see health and collaboration patterns across multi-repo organizations.
* **Features to Demonstrate**: List the exact UI pages/components (e.g., Overview Dashboard, Contributor Graph, Risk Metrics).
* **Narration Style**: Natural, active voice, avoiding corporate jargon.
* **Length**: 60 to 90 seconds.
* **Negative Constraints ("What NOT to do")**: Do not use stock footage of offices or abstract floating geometric shapes. Do not invent features not present in the repository.

#### Example Prompt:
```text
Create a 75-second explainer video for OrgExplorer, an open-source tool by AOSSIE.
Target audience: Open-source developers and maintainers.
Tone: Concise, informative, and modern.
Narrator style: Friendly, clear, natural pace.

Structure:
1. Problem (0-15s): Managing large GitHub organizations makes it difficult to track contributor networks and repository health across dozens of repos.
2. Solution (15-30s): Introduce OrgExplorer as an interactive visual intelligence dashboard that runs directly in the browser.
3. Feature Demo 1 (30-45s): Show entering an org name and loading the overview metrics and technology stack breakdown.
4. Feature Demo 2 (45-60s): Demonstrate the interactive contributor network graph and repository risk metrics.
5. Outro & Call to Action (60-75s): Invite viewers to star the repo on GitHub, explore the live demo, and contribute to AOSSIE.

Important Constraints:
- Use real UI footage and screens from the OrgExplorer application.
- Do NOT generate abstract sci-fi visuals, floating 3D cubes, or generic office stock video.
- All narration must accurately reflect live functionality.
```

---

### Step 5 — Generate the Initial Draft

Arcade processes the prompt and brand kit to assemble:
* A structured spoken script
* AI voiceover narration
* Scene transitions
* Visual mockups / recorded UI steps

Your primary role in this stage is **director and editor**, not passive consumer.

---

### Step 6 — Critically Review the Generated Draft

Run through this quality check:

1. **Product Visibility**: Is the actual product interface visible on screen for at least 60% of the video?
2. **Feature Authenticity**: Are the buttons, menus, and graphs shown real parts of the codebase?
3. **Narration Accuracy**: Does the voiceover describe actual features rather than hallucinated capabilities?
4. **Pacing**: Does the visual stay on screen long enough for a viewer to read the headers and understand what is happening?
5. **Sync**: Does each visual directly match what the voiceover is explaining at that exact second?

---

### Step 7 — Refine and Replace Generic Elements

If the initial draft is 70–80% accurate, **do not scrap it** (editing and prompting an existing video costs **0 extra credits**, whereas regenerating from scratch consumes another 50 credits). Use targeted refinements:

* **Replace Placeholders**: Wherever Arcade generated an abstract illustration or generic icon, swap it with a high-resolution screenshot or a recorded screen capture of the actual project in action.
* **Trim Dead Air**: Cut out unnecessary pauses or overly verbose narration.
* **Synchronize Actions**: If the voiceover mentions *"Filter by stars"*, ensure the video shows the user clicking the star filter at that precise moment.
* **Smooth Transitions**: Keep cuts simple (clean cuts or quick cross-fades). Avoid distracting 3D spinning transitions.

---

### Step 8 — Add the AOSSIE Intro and Outro

Every official AOSSIE project video must include the Aossie Intro and Outro video which will be provided
by the mentors.

---

## 4. Pre-Publishing Checklist

Before submitting your video to AOSSIE maintainers or embedding it in a pull request, verify:

- [ ] **Format**: Rendered in 16:9 aspect ratio at 1080p (`1920x1080`), 30 or 60 fps, H.264 MP4.
- [ ] **Length**: Explainer is strictly between **60 and 90 seconds** (never exceeding 120s).
- [ ] **Visual Proof**: Real product UI or terminal output is visible for at least 60% of total runtime.
- [ ] **Accuracy**: Every feature and metric shown corresponds to actual capabilities in the repository.
- [ ] **AOSSIE Intro & Outro**: Contains the official AOSSIE intro bumper and closing call-to-action end card.
- [ ] **Watermark-Free**: No third-party platform watermarks (removed prior to submission).
- [ ] **Audio Quality**: Voiceover is clear and audible; background music is subtle and does not overpower narration.
- [ ] **Subtitles**: Accurate, synchronized captions are included and easily readable.
- [ ] **Legibility**: All text, buttons, and metrics shown on screen are readable on a 13-inch laptop display.
- [ ] **File Size**: Video file is compressed (recommended under 100 MB for fast GitHub and web playback).

---
