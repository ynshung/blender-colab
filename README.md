<a href="https://colab.research.google.com/github/syn73/blender-colab/blob/master/blender_render.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# Intro
This is a Python script that allows you to render Blender 2.8x scene using Google Colaboratory.
You can upload the blender files using direct upload, Google Drive or URL while rendered frames can be downloaded directly or through Google Drive.
This script provides basic functionality so you may modify the script to your liking to suit your needs.
This script is adapted from this [gist](https://gist.github.com/donmahallem/a05100077ec1327268f28f0b2bd8da60). Special thanks to [donmahallem](https://github.com/donmahallem) and the Sheepit Discord community (for discovery of this gist)!

A few notes:
1. You must own a Google account.
2. One notebook can only run for maximum time of 12 hours (24 hours for Google Colab Pro) but not guaranteed.
3. EEVEE rendering is not supported in virtual machine.
4. This script is not tested fully yet. Expect some errors.
5. Do note that your access to GPU may be limited or blocked if you render for many hours.
6. This script is intended for those who have no access to high-end GPU for rendering. Please use responsibly!

## Disclaimer
Google Colab is specialized for data centres, neural network etc, not rendering 3D scenes. Because the computing power provided are free, the usage limits, idle timeouts and speed of the rendering may varies. [ColabPro](https://colab.research.google.com/signup) is available for those who wanted to have more powerful GPU and longer session for rendering. See the [FAQ](https://research.google.com/colaboratory/faq.html) for more info. In some cases, it might be faster to use a renderfarm such as [Sheepit](https://www.sheepit-renderfarm.com/) (free) and [ConciergeRender](https://www.conciergerender.com/) (paid w/ trial) which support parallel rendering.
