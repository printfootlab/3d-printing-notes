# Designing lattices for 3D printing

**English** | [中文](../zh/03-晶格设计.md)

A lattice is a structure made by repeating a small cell through a volume. With the same material, a lattice can make a part lighter, softer or more breathable than a solid part.

> **Key points**
> - A lattice repeats a unit cell; cell size, strut thickness and relative density set its behaviour.
> - Strut-based cells are simple; surface-based TPMS cells such as the gyroid spread stress and drain well.
> - Graded, conformal and Voronoi lattices let one part be firm in one zone and soft in another.
> - Keep cells open and connected so resin can drain.

---

## Unit cells

The repeating piece is the **unit cell**. It is described by three values:

| Parameter | Meaning |
|---|---|
| Cell size | The width of one cell |
| Strut or wall thickness | How thick the material inside the cell is |
| Relative density | The share of the cell's volume that is solid. Thicker struts or smaller cells raise it |

For the same material, relative density and cell type together set most of the mechanical behaviour.

## Two families of cells

**Strut-based (beam) lattices** are built from straight rods joined at nodes: cubic, body-centred cubic, octet truss, honeycomb-style cells and so on. They are easy to describe and inspect. Depending on how the struts are arranged:

| Type | How it carries load | Behaviour |
|---|---|---|
| Bending-dominated | Struts mainly bend | Softer, more cushioning |
| Stretch-dominated | Struts are mainly pulled or pushed along their length | Stiffer and stronger |

Cushioning parts usually use bending-dominated cells.

**Surface-based lattices** are made from smooth, continuous walls. The best known are **TPMS** (triply periodic minimal surfaces) such as the gyroid, Schwarz P and Schwarz D (diamond). They have no sharp nodes, which spreads stress more evenly, and all their channels are connected, which helps resin drain and air flow.

## The gyroid as an equation

TPMS lattices are usually generated from a formula rather than drawn by hand. The gyroid is approximated by:

```
sin(x)·cos(y) + sin(y)·cos(z) + sin(z)·cos(x) = 0
```

Points where the expression equals zero form the surface. To make a printable wall, software keeps all points where the expression lies between −t and +t; a larger t gives a thicker wall. Scaling x, y and z sets the cell size.

## Graded, conformal and Voronoi lattices

A real part rarely uses one uniform lattice:

| Type | How it works |
|---|---|
| Graded | Cell size or thickness changes gradually, for example firmer under the heel and softer under the arch |
| Conformal | The cell grid bends to follow a curved shape, so cells are not cut off awkwardly at the surface |
| Voronoi (stochastic) | Irregular cells generated from scattered points; changing how densely the points are placed is an easy way to grade the structure |

## From design to a printable file

Lattices contain huge numbers of small features, which strains traditional CAD:

| Approach / format | Notes |
|---|---|
| Implicit modelling | Describes the lattice as a mathematical field (like the gyroid equation) and only turns it into a mesh at the end. Many specialist lattice tools work this way |
| STL | Stores triangles only. A full lattice footbed can produce very large STL files |
| 3MF | A newer format that is more compact and can carry more information about the part |

## Design checklist

- **Minimum feature size.** Struts and walls must be thick enough for the printer's resolution and strong enough to survive cleaning.
- **Open, connected cells.** Closed pockets trap liquid resin (or unfused powder) that cannot be cleaned out.
- **Drainage paths.** In resin printing, every cell needs a way for resin to run out. See [04 Post-processing](04-post-processing-resin-parts.md).
- **Skins and edges.** A thin solid skin where the lattice meets the outside makes edges smoother and stronger, but blocks airflow and drainage there.

---

## Further reading

- How cell size, strut thickness and cell shape change cushioning and airflow in footwear: [printfootlab.com/lattice-basics](https://printfootlab.com/lattice-basics)
