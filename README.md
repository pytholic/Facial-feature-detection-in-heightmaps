# MarsTool
## For help
```
E:\skia_projects\Facial-feature-detection-in-heightmaps\MarsTool>Marstool.exe --help
```
```
E:\skia_projects\Facial-feature-detection-in-heightmaps\MarsTool>Marstool.exe meshgen --help
```

## To generate volume
```
Y:\MarsTool>MarsTool.exe meshgen -M -C --no-mesh-out Y:\original\asmc\HeadSample
```
```
Y:\MarsTool>MarsTool.exe meshgen -M -C --no-mesh-out Y:\original\asmc\HeadSample -O Y:\original\asmc\HeadSample
```

## My use case

**Generate Volume**
```
Y:\MarsTool>MarsTool.exe meshgen -M -C --no-mesh-out {input CT path} -O {output volume path}
```

**Generate heightmap**
* Uses volume generated in last step
```
Y:\MarsTool>MarsTool.exe depth -i 1 -d A {input volume path}
```
## MarsTool Updated
Use the command as follows with newer version of `MarsTool`. Updated version has *rescaling* function.
Example:
```
Y:\marstool.exe heightmap -r E:\skia_projects\Facial-feature-detection-in-heightmaps\data\data_volume\1.2.392.200036.9116.2.6.1.37.2417546703.1627868041.834669.mask.vol E:\skia_projects\Facial-feature-detection-in-heightmaps\data\data_volume
```

## Batch Operation
Use the **looping notebook** provided in the `Scripts` folder for batch operation. It will automatically loop through all the patients to generate `volume` files and corresponding `heightmaps`.

# Installation
```console
pip install mediapipe
```

# Usage
Follow `main.py` or `main_loop.py` to predict on your data. The notebook contains all the `preprocessing` functions and different output results including *landmarks, contour prediction and face mesh tesselation*.

# Resources
* Useful [link](https://www.youtube.com/watch?v=Yg6bFRnOSbs).
* [MediaPipe FaceMesh](https://google.github.io/mediapipe/solutions/face_mesh.html)