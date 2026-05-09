## Changelog

### v1.1
- Edge clearance, pulley-to-plate clearance, and divider plate thickness are now user-editable inputs (previously hardcoded)
- Nominal inner gap displayed as a computed output
- Removed "12ga" label from plate thickness for generality

### v1.0
- Initial release
- Auto-optimizer finds common belt/pulley face sizes across all selected conveyor widths
- Uniform and Edge + Inner belt modes
- Belt and pulley face widths rounded to nearest 0.005" for manufacturing
- Edge belt < inner belt constraint (Edge + Inner mode)
- Per-conveyor breakdown with actual gap values and deviation badges
- Cross-section diagrams with pulley face, belt, plate, and clearance visualization
- Configurable: pulley face−belt width difference, min belt width, max belts per conveyor, max gap deviation
- Supports conveyor widths: 16, 18, 22, 24, 28, 30, 37, 43, 49, 61.5"
- Standalone single-file deployment (React via CDN, no build step)
