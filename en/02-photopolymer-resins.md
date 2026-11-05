# Photopolymer resins

**English** | [中文](../zh/02-光敏树脂.md)

A printing resin is a liquid that turns solid when light starts a chemical reaction in it. Knowing roughly what is inside explains most of what happens during printing and post-processing.

> **Key points**
> - A resin is mostly oligomers and monomers, plus a photoinitiator that starts curing when light hits it.
> - Cured resin is a thermoset: it cannot be re-melted.
> - A part straight off the printer is a "green part"; post-cure with light and/or heat gives its final properties.
> - Elastomeric resins are rubbery and measured on Shore A; rigid resins on Shore D.

---

## What is in a resin

| Ingredient | Role |
|---|---|
| Oligomers | Short polymer chains that form the backbone of the cured material and decide most of its properties, for example rigid or rubbery |
| Monomers (reactive diluents) | Small molecules that thin the resin so it flows, and join the network when cured |
| Photoinitiator | Absorbs light of the printer's wavelength (commonly around 385 or 405 nm) and starts the reaction |
| Light absorber | Limits how deep the light reaches, so each layer cures only to its intended thickness and fine details stay sharp |
| Pigments and additives | Colour, stability and other adjustments |

## Why it hardens

When the photoinitiator absorbs light, it creates reactive species that link the oligomers and monomers into a three-dimensional network. Once linked, the chains cannot slide past each other or melt again. This makes cured resin a **thermoset**: unlike a thermoplastic such as TPU, it cannot be re-melted and re-shaped.

Oxygen in the air slows this reaction at the surface. That is why a freshly printed part can feel slightly tacky even when its inside is cured.

## Green parts and post-cure

A part straight off the printer is a **green part**: it has its final shape but is not fully cured, so it is weaker and may still be tacky. Post-curing finishes the reaction:

| Method | How it works |
|---|---|
| Light post-cure | The cleaned part is exposed to light in a curing unit, often while warm |
| Thermal post-cure | Some resins, including many production elastomers, are **dual-cure**: light sets the shape during printing, and a second chemistry is completed by baking the part in an oven. The final properties only appear after this bake |

Skipping or shortening post-cure usually leaves a part softer, weaker and less stable over time than its data sheet suggests. Always follow the resin maker's curing instructions.

## Rigid vs elastomeric resins

| | Rigid resins | Elastomeric resins |
|---|---|---|
| Typical use | Models, housings, dental and jewellery work | Cushioning, seals, grips, footwear lattices |
| Feel | Hard, often brittle | Rubbery; returns to shape after bending |
| Usual hardness scale | Shore D | Shore A |
| Printing | Generally easier | Softer green parts and stickier resin make supports, peeling and cleaning harder |

Elastomeric resins are often based on polyurethane chemistry. In footwear they are usually used in a fairly firm grade, with softness coming from the lattice geometry rather than from a very soft material.

## Ageing

Cured resins can yellow, stiffen or become more brittle with long exposure to UV light and heat. Elastomer parts kept in strong sun for long periods may change feel over time. How much depends on the formulation.

---

## Further reading

- Materials used in printed footwear, and what happens at end of life: [printfootlab.com/materials](https://printfootlab.com/materials)
