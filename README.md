# hCAR-Nrf2

SILCS (Site Identification by Ligand Competitive Saturation) FragMap data supporting a project on the human Constitutive Androstane Receptor (hCAR) and the Keap1-Nrf2 pathway.

## Contents

### `LBD_hCAR/`
SILCS data for the hCAR ligand-binding domain (LBD).
- `1xvp.pdb` — receptor structure (PDB: [1XVP](https://www.rcsb.org/structure/1XVP)) used to generate the FragMaps.
- `maps/` — SILCS FragMaps computed on `1xvp.pdb`: apolar/polar functional-group free-energy maps (`*.gfe.map`), residue-type probability maps (`*.prob.map`), and an exclusion map (`*.excl.map`).
- `params.inp` — SILCS-MC docking parameters (simulation center/radius, Monte Carlo/simulated-annealing settings, and map assignments).

### `keap1/`
SILCS data for Keap1 (Kelch domain), used to probe the Keap1-Nrf2 binding site.
- `4cxt.pdb` — receptor structure (PDB: [4CXT](https://www.rcsb.org/structure/4CXT)) used to generate the FragMaps.
- `maps/` — SILCS FragMaps computed on `4cxt.pdb`.
- `params.inp` — SILCS-MC docking parameters for this site.

## Notes

- Both `params.inp` files reference maps by **absolute path** from the machines they were generated on (`/home/rgama/silcs_runs/hcar/...` for hCAR, `/home/wenbo/keap1/...` for Keap1), not by the repo-relative `maps/` folder next to them. Update the `SILCSMAP` lines to point at your local copy of `maps/` before running SILCS-MC docking from a fresh clone.
- Generated with SilcsBio 2025 (`LBD_hCAR`) / 2023 (`keap1`); see each `params.inp` header for the exact rules/parameter files used.
- The SILCS Software Suite to perform the SILCS simulations and MC docking may be obtained from SilcsBio LLC (https://silcsbio.com/)
