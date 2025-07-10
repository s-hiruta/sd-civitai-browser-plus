## How to Add Flux.1 and Flux.1 D Filtering to CivitAI Browser+
Follow these steps to add Flux.1 S and Flux.1 D filtering capabilities to your CivitAI Browser+ extension:

In your Civitai Browser+ extension scripts folder likely in `extensions\sd-civitai-browser-plus\scripts`, find `civitai_gui.py`, this will be the file we edit.

Step 1: Update the Base Model Options
In `civitai_gui.py`, find the `base_filter` definition and update it to include Flux options:

```python
base_filter = gr.Dropdown(label='Base model:', multiselect=True, choices=["SD 1.4","SD 1.5","SD 1.5 LCM","SD 2.0","SD 2.0 768","SD 2.1","SD 2.1 768","SD 2.1 Unclip","SDXL 0.9","SDXL 1.0","SDXL 1.0 LCM","SDXL Distilled","SDXL Turbo","SDXL Lightning","Stable Cascade","Pony","SVD","SVD XT","Playground v2","PixArt a", "Flux.1 S", "Flux.1 D","Other"], value=None, type="value", elem_id="centerText")
```

Step 2: Test the Changes
Save `civitai_gui.py` file.
Restart your Stable Diffusion WebUI.
In the CivitAI Browser+ tab, try selecting "Flux.1 S" and/or "Flux.1 D" in the base model filter.
Verify that the correct models are being displayed based on your selection.
These changes will allow you to filter for Flux.1 S and/or Flux.1 D models individually or together, while maintaining the functionality for other base models.