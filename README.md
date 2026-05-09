# Link to Tool

https://beboobeep.github.io/Strip_Belt_Merge_Design_Tools/

# Strip Belt Conveyor Optimizer

Finds common belt and pulley face widths that work across multiple conveyor widths using a rigid stack-up. Frame width is computed from the physical dimensions — it is always equal to or wider than the nominal conveyor width, never smaller.

## How It Works

You define the pulley geometry and constraints. The tool sweeps all valid belt/PF combos in 0.005" increments and checks every selected conveyor width. For each combo, it finds the belt count per conveyor that produces the smallest frame oversize. Results are ranked by smallest worst-case oversize.

Belt and pulley face widths are the **same on every conveyor** — only the belt count changes. The actual frame width varies per conveyor based on the stack-up.

### Stack-Up

```
Frame width = 2×boss + 2×edgePF + N×innerPF + (N+1)×(boss + plate + boss)
```

Where N = inner belt count. The boss mounts to the surface of the plate/channel and provides minimum clearance between the pulley face and the metal.

## Inputs

**Geometry**
- **Bearing Boss Length** — spacer between pulley face and plate/channel, mounts to surface of the metal
- **Divider Plate Thickness** — thickness of the plate between pulleys
- Inner gap (boss + plate + boss) is computed from these

**Parameters**
- **Belt Mode** — Uniform (all belts identical) or Edge + Inner (edge belts narrower)
- **Pulley Face − Belt Width** — belt tracking space on the pulley
- **Min Belt Width** — floor for belt width search
- **Max Belts Per Conveyor** — upper limit on belt count
- **Max Frame Oversize** — how much wider than nominal the frame can be (frame is never undersized)

**Conveyor Widths** — toggle which nominal widths to include

## Reading the Results

Each result card shows the belt/PF widths, worst oversize across all conveyors, and belt counts.

Click to expand:
- **Table** — nominal width, actual frame width, and oversize per conveyor
- **Cross-sections** — visual layout (blue = edge, amber = inner, purple = boss, gray = plate)
- **Stack-up formula** — with the actual values for that combo
