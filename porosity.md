# Undergraduate Research – Composite Materials and Structures Lab (CMSL)

## Project Overview

This research investigates the development of a modular hybrid ceramic–polymer thermal protection system (TPS) for hypersonic vehicles. The project combines a porous ceramic substrate with a phenolic resin ablative layer to provide thermal insulation, mechanical integrity, and active gas-blowing protection under extreme aerodynamic heating conditions.

Inspired by SpaceX's modular heat shield architecture, the design employs interconnected hexagonal tiles that can be assembled into a flexible "fabric" capable of protecting large surface areas. The modular approach enables damaged tiles to be replaced individually while maintaining overall system performance.

My work focuses on designing functionally graded porous ceramic structures with vascular channels that can be manufactured using additive manufacturing techniques and subsequently infused with phenolic resin. These structures are intended to provide both passive insulation and active ablative cooling during atmospheric reentry and hypersonic flight.

## Research Objectives

- Develop a modular hexagonal thermal protection tile architecture.
- Generate functionally graded porous geometries using Python.
- Export three-dimensional models as STL files for additive manufacturing.
- Fabricate porous ceramic structures and impregnate them with phenolic resin.
- Compare performance against conventional thermal protection systems.
- Evaluate thermal resistance through torch testing.

## Geometry Development

<script type="module"
src="https://ajax.googleapis.com/ajax/libs/model-viewer/4.1.0/model-viewer.min.js">
</script>

<model-viewer
src="/hex_tile.glb"
camera-controls
auto-rotate
shadow-intensity="1"
style="width:100%; height:500px;">
</model-viewer>

A custom Python program was developed to generate the internal porous architecture and export the geometry directly as STL files for manufacturing. The structure contains a porosity gradient designed to mimic the thermal requirements experienced during hypersonic flight.

The hot surface possesses approximately 41% porosity, providing large interconnected channels that promote gas transport and reduce heat transfer. The cold surface contains approximately 5% porosity, producing a denser ceramic structure with improved mechanical strength and thermal insulation.

The pore gradient enables the structure to combine high-temperature resistance with structural rigidity while facilitating the release of pyrolysis gases generated during resin decomposition.

### Current Status

- ✅ Python geometry generation completed
- ✅ STL file generation completed
- 🔄 Ceramic additive manufacturing in progress
- ⏳ Resin impregnation
- ⏳ Torch testing
- ⏳ Comparison with existing TPS materials

## Manufacturing Process

The porous ceramic structures are fabricated using ceramic additive manufacturing. After printing, the green body undergoes washing and drying before thermal debinding removes the organic matrix. High-temperature sintering densifies the alumina particles and produces a mechanically robust porous ceramic.

Following sintering, the ceramic structure is vacuum impregnated with phenolic resin containing chopped silicon carbide fibers. After curing, the resulting material forms a hybrid ceramic–polymer ablative composite capable of withstanding severe thermal environments.

<div style="text-align:center;">
  <img src="/manufacturing-process.png" style="max-width:100%;">
</div>

**Figure 1.** Manufacturing sequence used to produce the hybrid ceramic-polymer ablative composite. Ceramic structures are printed, washed, thermally debound, sintered, and finally infused with phenolic resin containing chopped silicon carbide fibers. The resulting composite combines the mechanical strength of porous alumina with the ablative characteristics of phenolic materials.

## Thermal Protection Mechanism

The proposed TPS architecture consists of an active ablative layer supported by a porous ceramic substrate. During hypersonic heating, the phenolic resin decomposes and releases pyrolysis gases that form a protective boundary layer above the surface. This gas blowing effect reduces convective heating and delays thermal penetration into the structure.

As the surface chars and recedes, the porous ceramic provides mechanical support and maintains structural integrity. The combination of gas-blowing, thermal insulation, and high compressive strength enables the system to survive severe aerodynamic environments.

<div style="text-align:center;">
  <img src="/tps-concept.png" style="max-width:100%;">
</div>

**Figure 2.** Conceptual operation of the hybrid ceramic–polymer thermal protection system. The ablative layer dissipates heat through pyrolysis and gas release while the porous ceramic substrate provides thermal insulation and structural support. The synergistic interaction between these mechanisms improves resistance to oxidation, recession, and mechanical spallation.

## Experimental Validation

After fabrication, specimens will be subjected to torch testing to evaluate thermal performance. The temperature response and structural behavior of the hybrid composite will be compared with conventional thermal protection materials to determine the effectiveness of the functionally graded architecture.

## Future Work

- Fabrication of modular hexagonal tiles.
- Experimental torch testing.
- Comparison against state-of-the-art TPS materials.
- Investigation of larger tile arrays forming a heat shield "fabric."
- Optimization of pore architecture and channel connectivity.
- Integration with machine learning and PINN-based thermal models.
