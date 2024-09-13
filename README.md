**This fork has been made to merge in pending Pull Requests, and formatting changes will break compatibility. [Original repository](https://github.com/BlafKing/sd-civitai-browser-plus)**

![CivitAI Browser-05+](https://github.com/BlafKing/sd-civitai-browser-plus/assets/9644716/95afcc41-56f0-4398-8779-51cb2a9e2f55)

---
### Extension for [Automatic1111's Stable Diffusion Web UI](https://github.com/AUTOMATIC1111/stable-diffusion-webui)


<h1>Features 🚀</h1>
<h3>Browse all models from CivitAI 🧩</h3>

* Explore a wide range of models at your fingertips.

<h3>Check for updates and installed models 🔄</h3>

* Easily spot new updates and identify already installed models while browsing.
* Ability to scan all installed models for available updates.

<h3>Download any Model, any version, and any file 📥</h3>

* Get the specific model version and file you need hassle-free.
* Download queue to avoid waiting for finished downloads.

<h3>Automatically assign tags to installed models 🏷️</h3>

* Assign tags by scanning all installed models for automatic use in image generation.

<h3>Quick Model Info Access 📊</h3>

* A button for each model card in txt2img and img2img to load it into the extension.
* A button under each image in model info to send its generation info to txt2img.

<h3>High-speed downloads with Aria2 🚄</h3>

* Maximize your bandwidth for lightning-fast downloads.

<h3>Sleek and Intuitive User Interface 🖌️</h3>

* Enjoy a clutter-free, user-friendly interface, designed to enhance your experience.

<h3>Actively maintained with feature requests welcome 🛠️</h3>

* Feel free to send me your feature requests, and I'll do my best to implement them!

<h1></h1>

<details>
<summary><h1>Known Issues 🐛</h1></summary>

<h3>Unable to download / Frozen download:</h3>

**If you're experiencing issues with broken or frozen downloads, there are two possible solutions you can try:**

1. **Revert to the old download method**:
   A solution could be to disable the "Download models using Aria2" feature.  
This will switch back to the old download method, which may resolve the issue.

   ![Revert to old download method](https://github.com/BlafKing/sd-civitai-browser-plus/assets/9644716/982b0ebb-0cac-4053-8060-285533e0e176)

2. **Disable Async DNS for Aria2**:
   If you're using a DNS manager program like PortMaster, try turning on the "Disable Async DNS for Aria2" option.

   ![Disable Async DNS for Aria2](https://github.com/BlafKing/sd-civitai-browser-plus/assets/9644716/3cf7fab3-0df5-4995-9543-d9824b7931ff)

These settings can be found under the "Settings" tab in Web-UI and then under the "CivitAI Browser+" tile.

</details>

<h1></h1>

# How to install 📘

<h3>Automatic Installation:</h3>

![HowTo](https://github.com/BlafKing/sd-civitai-browser-plus/assets/9644716/91a8f636-0fd5-4964-8fb4-830a5c22254a)


<h3>Manual Installation:</h3>

1. Download the latest version from this site and unpack the .zip  
![2023-09-25 13_06_31](https://github.com/BlafKing/sd-civitai-browser-plus/assets/9644716/12e46c6b-74b5-4ed5-bf55-cb76c5f75c62)

2. Navigate to your extensions folder (Your SD folder/webui/extensions)
3. Place the unpacked folder inside the extensions folder
4. Restart SD-WebUI

# Preview 👀

https://github.com/BlafKing/sd-civitai-browser-plus/assets/9644716/44c5c7a0-4854-4043-bfbb-f32fa9df5a74


# Star History 🌟

<a href="https://star-history.com/#BlafKing/sd-civitai-browser-plus&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=BlafKing/sd-civitai-browser-plus&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=BlafKing/sd-civitai-browser-plus&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=BlafKing/sd-civitai-browser-plus&type=Date" />
  </picture>
</a>

# Changelog 📋

<h3>v3.5.4</h3>

* Feature: Added support for DoRA (Requires SD-WebUI v1.9)
* Bug fix: No longer rescans models that were previously not found on CivitAI
* Bug fix: Fixed placement of HTML & api_info files when custom images location was used.
* Bug fix: Fixed incorrect json naming.

---
<h3>v1.0</h3>

* Feature: 'Refresh' now reloads the current page unless any options have been changed.
* Feature: Made the page refresh after a download and made it load during one.
* Feature: Orange glow for any outdated installed packages.
* Feature: 'Delete old version after download' option.
* Feature: Ability to manually fill in a page number to load the corresponding page.
* Cleanup: Removed new folder option.
* Cleanup: Made the glow around frames always visible without hovering.
* Pulled fork from: [SignalFlagZ's Fork](https://github.com/SignalFlagZ/sd-civitai-browser) [v1.1.0](https://github.com/SignalFlagZ/sd-civitai-browser/releases/tag/1.1.0)
