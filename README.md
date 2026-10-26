# SynthDetect

Course project for *Deep Generative Models for Visual Data* (HIT).
We test whether synthetic images generated with Stable Diffusion improve light fine-tuning of existing Hugging Face object detection models, measured on real images only. Full requirements: [PRD.md](PRD.md).

## Structure

| Path | Purpose |
|---|---|
| `config.yaml` | All parameters: domain, models, conditions, amounts, seed |
| `objects_table.csv` | Object types: appearance, cause, size, how to generate |
| `notebooks/00_environment_check.ipynb` | Checks GPU, packages, Drive, generation and detection |
| `notebooks/01_generate.ipynb` | Generate synthetic images |
| `notebooks/02_validate.ipynb` | Realism checks |
| `notebooks/03_finetune.ipynb` | Fine-tune detection models |
| `notebooks/04_results.ipynb` | Results table and plots |

Images, checkpoints and models are stored in Google Drive (`drive_root` in `config.yaml`), never in Git. Drive holds three folders, each created when first needed: `real`, `synthetic`, `results`.

## Getting started

1. Open [`00_environment_check.ipynb` in Colab](https://colab.research.google.com/github/AlmogSchwartzberg/genai-temp-project-name/blob/main/notebooks/00_environment_check.ipynb).
2. Runtime > Change runtime type > **T4 GPU**.
3. Runtime > Run all. The last cell prints a pass/fail summary.

## Workflow

Each team member works on their own branch and opens a PR to `main`. Keep each notebook in its own file to avoid merge conflicts. To run a notebook from a branch, set `BRANCH` in its first cell.
