![EPFL Center for Imaging logo](https://imaging.epfl.ch/resources/logo-for-gitlab.svg)
# nD Image Visualization with Open-Source Tools

![screenshot](assets/itkwidgets_screenshot.png)

This repository contains a few demo notebooks for creating interactive 3D visualizations using Python. 

- [↗️ PyVista Example](./pyvista_demo.ipynb)

- [↗️ Itkwidgets Example](./itkwidgets_demo.ipynb)

- [↗️ Dash VTK Example](./dash_demo.ipynb)

## Setup & Installation

Install the Python requirements:

```
pip install -r requirements.txt
```

Start jupyter lab from the terminal:

```
jupyter lab
```

## List of 3D image visualization tools

In addition to Jupyter notebook tools, many other 3D rendering software packages exist. Here are a few that we recommend (in alphabetical order):


- [Dash VTK](https://dash.plotly.com/vtk/intro)
- [Fiji - 3D viewer](https://imagej.net/plugins/3d-viewer/)
- [Fiji - Volume viewer](https://imagej.net/plugins/volume-viewer)
- [Itkwidgets](https://itkwidgets.readthedocs.io/en/latest/)
- [K3D](https://k3d-jupyter.org/index.html)
- [Napari](https://napari.org/stable/)
- [Neuroglancer](https://github.com/google/neuroglancer)
- [Paraview](https://www.paraview.org/)
- [PyVista](https://pyvista.org/)
- [stackview](https://github.com/haesleinhuepf/stackview)
- [tif2blender](https://github.com/oanegros/MicroscopyNodes)
- [vedo](https://vedo.embl.es/)
- [Viv](https://github.com/hms-dbmi/viv?tab=readme-ov-file)
- [Vizarr](https://github.com/hms-dbmi/vizarr)

## Which tool for which use case?

### Features

| Software | 3D+time | Multichannel | Large data | Volume rendering | Projections (mip) | Isosurface / meshes | Glyphs | Intuitive | Scriptable |
|----------|-------- | ------------ | ---------- | ---------------- | ----------------- | ------------------- | ------ | --------- | ---------- |
| Fiji Volume Viewer | - | - | - | ✅ | ✅ | - | - | ✅ | - |
| Fiji 3D Viewer     | ✅ | ✅ | - | ✅ | - | ✅ | - | ✅ | - |
| Napari             | ✅ | ✅ | ✔️ | ✔️ | ✅ | ✅ | ✅ | ✅ | ✅ |
| PyVista            | - | ✔️ | ✔️ | ✅ | - | ✅ | ✅ | ✔️ | ✅ |
| Neuroglancer       | ✅ | ✅ | ✅ | ✔️ | ✔️ | ✅ | ✔️ | - | ✔️ |
| Paraview           | ✅ | ✔️ | ✔️ | ✅ | - | ✅ | ✅ | - | ✔️ |

✅ Yes ✔️ Sort of

### Pros and cons

**Fiji Volume Viewer**

- ✅ Ideal for Fiji users
- ✅ Good control over the 3D rendering
- 🔴 No glyphs or overlays (masks, points, vectors...)
- 🔴 4D (3D+time or multichannel) not supported (?)
- 🔴 Not controllable programmatically

**Napari**

- ✅ Ideal for nD: 3D+time, multichannel
- ✅ Ideal for overlays: masks, points, vectors...
- ✅ Controllable programmatically
- 🔴 No fine control over the transfer function

**PyVista**

- ✅ Ideal for reproducible visualizations in Python
- ✅ Good control over the 3D rendering
- ✅ Desktop or web-based
- 🔴 Not as interactive as other tools

**Neuroglancer**

- ✅ Ideal for Zarr and large images
- ✅ Visualizations can be shared simply with a URL
- 🔴 Not as intuitive as other tools