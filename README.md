# Story2Comic — Story to Comic Generator

This project converts short stories (1-3 paragraphs) into black-and-white manga-style comic pages.

## Features

- Story parsing using spaCy
- Character dictionary with attributes and reference portraits
- Reference portrait generation (Stable Diffusion text2img)
- Panel generation (text2img by default; img2img / ControlNet optional)
- Speech bubble rendering using Pillow
- Page assembly into grid layout

## Quick start

1. Create & activate virtualenv

Windows PowerShell:

python -m venv venv
.\venv\Scripts\Activate.ps1

2. Install packages

pip install -r requirements.txt
python -m spacy download en_core_web_sm

3. Run example

Outputs will be saved to `outputs/comics/`.

## Notes

- For consistent character appearance across panels, use the `--mode enhanced` flag (ControlNet + reference images) if you have a capable GPU.
- If VRAM is limited, use `--mode baseline` (img2img chaining) and smaller image sizes.
