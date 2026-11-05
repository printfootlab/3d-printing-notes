# Testing elastomer materials

**English** | [中文](../zh/05-弹性体测试.md)

Data sheets for flexible printing materials list results from a handful of standard tests. Knowing what each test measures makes it easier to compare materials, and to tell which numbers matter for a given part.

The standards named below are ASTM methods. ISO publishes equivalent methods for most of them, but results from different standards are not always directly comparable.

> **Key points**
> - Shore hardness (ASTM D2240) describes the material, not how soft a lattice part feels.
> - Tensile, tear and compression set tests show toughness and recovery.
> - For cushioning, compression set and rebound resilience matter most.
> - Check print orientation and cure conditions before comparing data sheets.

---

## Tests at a glance

| Test | Standard | What it measures | Why it matters for lattice parts |
|---|---|---|---|
| Shore hardness | ASTM D2240 | Indenter depth, read on a 0–100 scale | Describes the material only |
| Tensile strength and elongation | ASTM D412 | Stress and stretch at break | High elongation helps thin struts survive repeated bending |
| Tear strength | ASTM D624 | Force needed to tear a sample | Hints at resistance to cracks starting at nodes and edges |
| Compression set | ASTM D395 | Share of a compression that does not recover | Lower is better; one of the most relevant numbers for cushioning |
| Rebound resilience | Several methods | Energy returned by a dropped weight or pendulum | High feels springy; low feels damped |

## Hardness: Shore durometer (ASTM D2240)

A spring-loaded indenter is pressed into the material and the depth it reaches is read on a 0–100 scale.

- **Shore A** is used for soft and medium rubbers and most elastomers.
- **Shore D** is used for harder plastics.
- The scales overlap: a very hard Shore A material and a soft Shore D material can feel similar.

Hardness describes the **material**, not the part. A lattice printed from a fairly firm elastomer can feel much softer than a solid block of the same material, because the softness comes from the geometry.

## Tensile strength and elongation (ASTM D412)

A dog-bone shaped sample is pulled until it breaks.

- **Tensile strength** is the stress at break.
- **Elongation at break** is how far it stretched, as a percentage of its original length.
- Some data sheets also give the stress at a set stretch (for example 100%), sometimes called a modulus.

## Tear strength (ASTM D624)

A shaped or pre-cut sample is pulled to see how much force it takes to tear.

## Compression set (ASTM D395)

A sample is squeezed by a fixed amount, held for a set time and temperature, then released. Compression set is the share of the squeeze that does not recover. A **lower** value means better spring-back, though a lattice's recovery also depends on its design.

## Rebound resilience

A weight or pendulum is dropped onto the material and the energy that comes back is measured. High resilience feels springy and lively; low resilience feels damped.

## Reading data sheets with care

- **How samples were made.** Printed samples may be tested in one orientation only, and properties can differ between orientations.
- **Cure conditions.** Results usually assume the full recommended post-cure.
- **Material is not the part.** How a finished lattice feels and lasts also depends on cell design, and must be tested on the part itself.

---

## Further reading

- How printed lattice slides compare with EVA foam slides: [printfootlab.com/guides/3d-printed-vs-eva-foam-slides](https://printfootlab.com/guides/3d-printed-vs-eva-foam-slides)
