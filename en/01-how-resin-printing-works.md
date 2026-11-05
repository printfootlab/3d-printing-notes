# How resin 3D printing works

**English** | [中文](../zh/01-树脂打印原理.md)

Resin printing, also called vat photopolymerization, builds a part from a liquid resin that hardens when it is exposed to light. Each layer is a thin slice of the part, cured on top of the previous one. The main variants differ in how the light is delivered.

> **Key points**
> - Resin printing cures a liquid resin layer by layer with light.
> - SLA uses a laser; DLP and LCD expose a whole layer at once; continuous printing (CLIP / DLS) skips the separate peel step.
> - Layer thickness, exposure, pixel size, supports and orientation decide print quality.
> - Whole-layer exposure makes resin printing well suited to fine lattices.

---

## The four common light sources

| Process | How each layer is exposed | Notes |
|---|---|---|
| SLA (stereolithography) | A laser traces the layer point by point | The original process; layer time grows with the area of the layer |
| DLP (digital light processing) | A projector exposes the whole layer at once | Layer time does not depend on how much of the layer is filled |
| LCD / MSLA | An LCD screen masks a light source, exposing the whole layer at once | Similar to DLP; common in desktop printers |
| Continuous printing (e.g. CLIP / DLS) | A projector exposes through an oxygen-permeable window, so the part is pulled up continuously instead of layer by layer | Faster, with fewer layer lines; used for many production elastomer parts |

DLP and LCD are both "whole layer" processes. For a lattice this matters: every layer is full of small, separate islands of material. A laser has to visit each island, while a projector cures them all in one exposure.

## A print, step by step

1. **Slice.** Software cuts the 3D model into layers, typically tens of micrometres thick, and turns each layer into an image.
2. **Expose.** The build platform sits just above the floor of the vat, leaving one layer of resin between them. Light through the transparent floor cures that layer onto the platform.
3. **Separate.** The platform lifts so the fresh layer peels off the vat floor, and new resin flows in underneath.
4. **Repeat** until the part is complete. The part hangs upside down from the platform.

Most desktop and many industrial printers work bottom-up like this. Peeling each layer off the vat floor pulls on the part, which is one reason supports and orientation matter.

## What controls quality

| Factor | Effect |
|---|---|
| Layer thickness | Thinner layers give smoother sides and finer detail, but take longer |
| Exposure time | Too little and thin features do not form or fall off; too much and light bleeds past the edges, closing small holes. In a lattice, overexposure shows up as partly filled cells |
| Pixel size (XY resolution) | Sets the smallest strut or gap the printer can draw. A strut only a few pixels wide is fragile and may not print reliably |
| Supports | Overhangs and the first layers need supports to resist the peel force. Lattices are often partly self-supporting, because each cell holds up the next |
| Orientation | Tilting a part changes where supports go, how large each layer is and where layer lines fall. A footbed printed flat has very large layers and high peel force; printed upright, each layer is small but the print is tall |

## Why resin suits fine lattices

Resin printing can draw small, smooth features, so it can produce lattices with small cells and thin struts that are hard to make by other methods.

- **FDM (filament):** limited by nozzle width and by bridging between struts.
- **SLS, MJF (powder bed):** can also make fine lattices, but unfused powder must be cleared from every cell.
- **Resin:** has its own clean-up problem, liquid resin trapped in the lattice. See [04 Post-processing](04-post-processing-resin-parts.md).

---

## Further reading

- How printed slides are made, from design to inspection: [printfootlab.com/guides/how-3d-printed-slides-are-made](https://printfootlab.com/guides/how-3d-printed-slides-are-made?src=gh-01)
