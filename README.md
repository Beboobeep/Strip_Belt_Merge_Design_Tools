# Link to Tool

https://beboobeep.github.io/Strip_Belt_Merge_Design_Tools/

# Strip Belt Conveyor Optimizer

Finds common belt and pulley face widths that work across multiple conveyor widths. Belt/PF dims are rounded to the nearest 0.005" for manufacturing. Clearance gaps absorb the geometric remainder per conveyor.

## How It Works

You define the conveyor geometry (clearances, plate thickness) and constraints (min belt width, max belts, max gap deviation). The tool sweeps all valid belt/PF combos in 0.005" steps and checks every selected conveyor width. Results are ranked by smallest gap deviation from nominal.

Each result uses the **same belt and pulley face widths** on every conveyor — only the belt count changes. The clearance gaps (edge-to-wall and pulley-to-plate) flex slightly at the 4th decimal to make it fit.

## Inputs

**Geometry (top section)**
- **Edge Pulley → Wall** — clearance from edge pulley face to side channel
- **Pulley Face → Plate** — clearance from pulley face to divider plate, each side
- **Divider Plate Thickness** — thickness of the plate between pulleys
- Nominal inner gap is computed from these three values

**Parameters**
- **Belt Mode** — Uniform (all belts identical) or Edge + Inner (edge belts narrower than inner)
- **Pulley Face − Belt Width** — how much wider the pulley face is than the belt
- **Min Belt Width** — floor for belt width search
- **Max Belts Per Conveyor** — upper limit on belt count
- **Max Gap Deviation** — how far each clearance can deviate from nominal before a combo is rejected

**Conveyor Widths** — toggle on/off which widths to include in the search

## Reading the Results

Each result card shows:
- Belt and pulley face widths (common across all conveyors)
- Worst gap deviation across all conveyors
- Belt counts per conveyor

Click a card to expand:
- **Table** — per-conveyor actual edge gap, pulley-to-plate gap, and inner gap with deviation from nominal
- **Cross-sections** — visual layout showing belt (filled), pulley face (outline), plates (gray), and edge clearance (red tint)
