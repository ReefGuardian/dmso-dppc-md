# Project plan

Version: 0.1, initialized 2026-09-25  
Status: working plan accepted for organization; numerical simulation protocol not yet finalized.

## Questions

1. With modern Martini 3, how do 0, 6, and 12 mol% DMSO change area per lipid, bilayer thickness, and DMSO distribution in a DPPC membrane?
2. Do self-assembled and INSANE-built membranes give consistent equilibrated results under matched conditions?
3. How do those trends compare with the 2006 coarse-grained study?

The two construction routes use the same selected force field. INSANE constructs coordinates; it does not supply a competing physical model.

## Stages

| Stage | Work | Evidence needed before moving on |
| --- | --- | --- |
| 0. Organize | Establish the private repository and notebook | Repository URL, initial commit, parameter sources, and next step recorded |
| 1. Learn locally | Prepare an approximately 50-DPPC, DMSO-free training system; run an appropriately short test and visualize it | Actual software output, input files, successful preprocessing/run evidence, and a viewable structure; duration and builder still to be specified |
| 2. Establish the control | Prepare and equilibrate 512-DPPC systems at 323 K and 1 bar using each construction route | Verified topology, composition, box, orientation, leaflet populations, and stable membrane measurements |
| 3. Add DMSO | Prepare the selected 0/6/12 mol% comparison from equilibrated DMSO-free membranes | Documented mixture calculation and actual solvent counts for every system |
| 4. Collect research data | Use CIRCE for the longer simulations and independent repeats | Validated settings, selected repeat count, actual run versions, equilibration window, and sufficient sampling |
| 5. Analyze | Compare means and uncertainty within/between routes and with historical results | Reproducible analysis scripts, definitions, plots, and limitations |
| 6. Consider extension | Revisit the 2007 atomistic study after the coarse-grained work is established | A separate plan for that model and its conditions |

No long run is requested by the repository-setup task. Do not populate the notebook with simulated results that have not been produced.

## Preparation comparison

Experiment 1: self-assembled DPPC.  
Experiment 2: INSANE-built DPPC.

The selected first workflow is to form and equilibrate pure DPPC membranes, then prepare DMSO mixtures from those membranes. Studying DMSO's effect on assembly itself would be a separate question.

Match lipid identity and count, solvent composition, physical conditions, force-field files, production settings, and analysis definitions between routes. Verify actual leaflet populations. An asymmetric self-assembled membrane and a symmetric constructed membrane would introduce another difference into the comparison.

Check that the builder's molecule names, bead counts, and bead ordering match the selected Martini 3 topologies. Record the builder command and version; the name INSANE alone does not establish that a structure is compatible with a particular topology release.

Following the official tutorial, assembly and an established planar bilayer can require different pressure-coupling geometries. Record preparation settings separately from production settings. An INSANE-built membrane still needs minimization and equilibration.

## Analysis

Primary measurement: area per lipid.

Supporting measurements: bilayer thickness, DMSO density/distribution, and membrane integrity. Water penetration and pores are exploratory observations. A pore is not guaranteed at the selected concentrations, and these structural measurements alone do not constitute a quantitative permeability measurement.

For a flat, intact membrane in the xy plane:
- Projected area per lipid in a leaflet = Lx × Ly / actual lipid count in that leaflet.
- Dividing by 256 is appropriate only when that leaflet actually contains 256 lipids.
- Record thickness by a stated definition, initially the separation of phosphate-density peaks.

Independent repeats and an uncertainty method are required for the research comparison; their number and implementation remain to be selected. Use time blocks or another justified approach that accounts for correlated trajectory frames. Repeats of self-assembly should also address variability in the construction process.

## Duration and time conventions

The 800 ns production value is retained as an initial planning target, not as proof of adequate sampling. The 100 ns practice duration remains a proposal. A 50-lipid system does not itself specify how long the training run should last.

Report GROMACS simulation time explicitly. The 2004 model used a factor-of-four effective-time convention; the exact convention of the 2006 reported durations still needs clarification before comparing kinetic times. Do not apply a universal factor of four to Martini 3.

## Historical comparison

The 2006 paper used 512 DPPC at 323 K and 1 bar with an older coarse-grained model and a special D1/D2 DMSO representation. Its supplement describes introducing DMSO by replacing water particles around an existing bilayer.

The 2007 paper used an atomistic/united-atom approach with different conditions, including 128 DPPC and 350 K. Those settings are not inputs to the current Martini project.

## Current open decisions

- Exact training builder, box, hydration, relaxation protocol, and duration.
- Compatible temperature/pressure-control update settings for the installed GROMACS.
- Final solvent counts and how hydration is held consistent across mixtures.
- Equilibration criteria, independent-repeat count, random seeds, sampling windows, and uncertainty calculation.
- Actual GROMACS and INSANE versions on each execution machine.
- CIRCE partition, resources, storage paths, and backup location.
- Final output frequency, sufficient for the selected analyses.
