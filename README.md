<a href="https://colab.research.google.com/github/syn73/blender-colab/blob/master/blender_render.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# Intro
This is a Python script that allows you to render Blender scene using Google Colab. You can upload the blender files using direct upload, Google Drive or URL. Frames rendered can be downloaded directly or through Google Drive. This script provides basic functionality so you may modify the script to your liking to suit your needs. Save a copy of this notebook in the File menu before proceeding. (*Note that the script may update over time.*) I discovered [this gist](https://gist.github.com/donmahallem/a05100077ec1327268f28f0b2bd8da60) from the Sheepit community in the Blender Discord server. Special thanks to [donmahallem](https://github.com/donmahallem) and the community!

Do note that:
1. You must own a Google account.
2. Hardware accelerator must be set to GPU in `Edit > Notebook settings`.
3. One notebook can only run for 12 hours unless you upgrade to Colab Pro.
4. This script is not tested fully yet.

# Setup
**Make sure to read the instructions carefully!**

Pack your blend file into a **zip archive** and put it within Google Drive. Make sure you **pack all external file** to the blend file or **make all paths** relative in order for resources to work. Note down the path of the blend file in the drive.

* `blender_version` : Version of blender used to render the scene. Only supports 2.8x
* `blend_file_path` : Path to the blend file after unpacking the zip archive. If blend file is used, this is automatically ignored.
___
* `upload_type` : Select the type of upload method.
* `drive_path_to_blend` : Path to your blend/zip file relative to the root of your Google Drive if `google_drive` is selected.
* `url_blend` : Specify the URL to the blend/zip file if `url` is selected.
___
* `animation` : Specify whether animation or still image is rendered. If **still image** is used, put the frame number in `start_frame`.
* `start_frame, end_frame` : Specify the start and end frame for animation. You may put same value such as zero for both input to set the default frame in the blend file.
___
* `download_type` : Select the type of download method.
* `output_name` : Name of the output frames, **do NOT include .blend!** (## for frame number)
* `zip_files` : Archive multiple animation frames automatically into a zip file.
* `drive_output_path` : Path to your frames/zip file in Google Drive.

After you are done, simply go to Runtime > Run All (Ctrl + F9) and upload your files or have Google Drive authorised.

## Disclaimer
The GPU used in Google Colab is specialized for data centres, neural network etc, not rendering 3D scenes. Because the computing power provided are free, the usage limits and speed of the rendering may varies. [ColabPro](https://colab.research.google.com/signup) is available for those who wanted to have more powerful GPU and longer session for rendering. See the [FAQ](https://research.google.com/colaboratory/faq.html) for more info about this platform. In some cases, it might be faster to use a renderfarm such as [Sheepit](https://www.sheepit-renderfarm.com/) (free) and [ConciergeRender](https://www.conciergerender.com/) (trial) which have parallel rendering.
