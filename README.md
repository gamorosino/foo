<h1 align="center">foo</h1>

<p align="center">
  Utility that copies a mask image unchanged so the output carries the brain and dwi datatype tags.
</p>

<p align="center">
  <a href="https://github.com/brainlife/abcd-spec"><img src="https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg" alt="ABCD Spec v1.1"></a>
  <a href="https://doi.org/10.25663/brainlife.app.923"><img src="https://img.shields.io/badge/Brainlife-brainlife.app.923-blue.svg" alt="Run on brainlife.io"></a>
</p>

## At a glance

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Utility that copies a mask image unchanged so the output carries the brain and dwi datatype tags.**

Copies the input files unchanged to the output (no image processing is done, the main script only copies files with jq and cp). Use it to relabel a dataset with the datatype tag shown on the output when the processing it reflects was done elsewhere. Do not use it to actually process data.

| | |
|---|---|
| **Inputs** | `neuro/mask` |
| **Outputs** | `neuro/mask` |
| **Resources** | 8 CPUs · 1 h walltime |
| **Run it** | [doi.org/10.25663/brainlife.app.923](https://doi.org/10.25663/brainlife.app.923) |

#### Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `mask` | `neuro/mask` | yes | Mask image (NIfTI). |

#### Outputs

| Output | Datatype | Description |
|---|---|---|
| `mask` | `neuro/mask` | The same mask, copied unchanged and tagged brain and dwi. |

<!-- brainlife-app:end -->

## Versions on brainlife.io

This repository hosts several Apps, each built from its own branch.

| App | Branch | Run it | Status |
|---|---|---|---|
| app-set-datatype_tag-brain-dwi | [`main`](https://github.com/gamorosino/foo/tree/main) | [doi:10.25663/brainlife.app.923](https://doi.org/10.25663/brainlife.app.923) | current |
| app-set-dwi-datatype_tag-preprocessed | [`main`](https://github.com/gamorosino/foo/tree/main) | [doi:10.25663/brainlife.app.909](https://doi.org/10.25663/brainlife.app.909) | available |
| app-set-datatype_tag-debiased | [`main`](https://github.com/gamorosino/foo/tree/main) | [doi:10.25663/brainlife.app.847](https://doi.org/10.25663/brainlife.app.847) | available |
| app-set-datatype_tag-preprocessed | [`main`](https://github.com/gamorosino/foo/tree/main) | [doi:10.25663/brainlife.app.846](https://doi.org/10.25663/brainlife.app.846) | available |

## Running the App

### On brainlife.io

Open the App at [doi.org/10.25663/brainlife.app.923](https://doi.org/10.25663/brainlife.app.923), choose `neuro/mask` from your project and press **Execute**. The results are saved to your project as `neuro/mask`.

### Locally

You need [`jq`](https://jqlang.github.io/jq/).

1. Clone this repository and check out the App's branch (`git checkout main`).
2. Create `config.json` with the paths to your inputs and the parameters:

   ```json
   {
       "mask": "/path/to/mask/mask"
   }
   ```

3. Run `./main`.

## Citing

If you use this App, please cite it, the software it builds on and brainlife.io:

- app-set-datatype_tag-brain-dwi. brainlife.io App. [doi:10.25663/brainlife.app.923](https://doi.org/10.25663/brainlife.app.923)
- Hayashi S, Caron BA, Heinsfeld AS, et al. brainlife.io: a decentralized and open-source cloud platform to support neuroscience research. *Nature Methods* 21:809–813 (2024). [doi:10.1038/s41592-024-02237-2](https://doi.org/10.1038/s41592-024-02237-2)
- Avesani P, McPherson B, Hayashi S, et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. *Scientific Data* 6:69 (2019). [doi:10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

## Authors

Maintained by [@gamorosino](https://github.com/gamorosino).
