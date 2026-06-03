# Berliner Schule Sequencer (BSS)

An algorithmic MIDI sequencer that runs directly in the browser. It generates melodic patterns inspired by the **Berliner Schule** style of electronic music, balancing repetition with subtle organic evolution.

## Core Functionality

The tool is designed as a sequence generator. While it includes a basic internal synth for monitoring and previewing patterns, its primary purpose is to generate MIDI data. The actual sound design and final music production are intended to take place within a **Digital Audio Workstation (DAW)** or with external hardware via the MIDI export function.

The tool uses a Pseudo-Random Number Generator (PRNG) to create sequences based on musical constraints. Users can either generate random patterns or use fixed seeds to recreate specific results.

### Composition Modes
- **Classic**: A "Random Walk" within the selected scale, creating fluid and grounded melodies.
- **Klaus Schulze**: Focuses on sparse, long-held notes and drones for a meditative atmosphere.
- **Offbeat Anchor**: Locks specific steps (usually offbeats) to a fixed pedal point while the rest of the melody varies.
- **Arpeggiator**: Cycles through chord tones; these can be mutated over time to evolve the rhythmic pattern.
- **Motivic**: Generates a 4-note "DNA motif" and applies classical transformations (Inversion, Retrograde).

### Harmonic Palette (Scales)
The mood of the sequence is determined by the selected scale:
- **Dorian**: Sophisticated, slightly melancholic but open.
- **Phrygian**: Dark, tense, and exotic; typical for "dark cosmic" sounds.
- **Aeolian (Natural Minor)**: Classic sad or dramatic tone.
- **Mixolydian**: Brighter, more dominant and open.
- **Minor/Major Pentatonic**: Simplified scales that always sound harmonious and fluid.

### Evolutionary Export (🧬)
Beyond standard MIDI loops, the sequencer features an evolutionary chain generator. This mimics the drift of vintage modular systems by mutating a sequence over several blocks:
- **Mutation**: Controls how much each block differs from the previous one.
- **Drift**: Adds probability for sudden octave jumps.
- **Grip**: Determines how strongly the evolution adheres to the original theme.
- **Root Shift**: Allows for harmonic progressions (e.g., Cycle of Fifths, Modal shifts) between blocks.

## Installation & Usage

No installation is required.
1. Download or clone the repository.
2. Open `berliner-schule-sequencer.html` in any modern web browser.

## Operation Guide

### Parameter Behavior
- **Live Parameters (Green Labels)**: These affect the playback engine in real-time (e.g., BPM, Swing). Changes are audible immediately.
- **Generative Parameters (Amber Labels)**: These define the blueprint of the sequence. Changing these values triggers an automatic regeneration of the pattern upon releasing the slider or changing the selection. The "↻ Generate" button can also be used to manually trigger a new seed.

### Key Settings
- **Timing & Rhythm**: Adjust BPM, Swing, and Steps per Beat (resolution).
- **Phrase & Notes**:
    - `Scale & Root`: Defines the harmonic palette.
    - `Steps`: Length of one musical idea before it repeats.
    - `Density`: Probability of a note occurring on any given step.
    - `Interval`: Limits the "jump" between consecutive notes to control melodic smoothness.
- **Variation**: Controls how much each repeat of a phrase differs from the original, preventing robotic repetition.

### Visual Legend
- **Blue cell**: Standard generated note.
- **Pink cell**: Anchor note (fixed pitch).
- **Dark/empty cell**: A rest.
- **Semi-transparent blue**: A tie (held note).
- **Blue height bar**: Relative pitch indicator.

## License
MIT License © 2026 Reiner Prokein
