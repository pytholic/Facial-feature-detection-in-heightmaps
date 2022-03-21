## Example Commands
### For help
```
E:\skia_projects\Facial-feature-detection-in-heightmaps\MarsTool>Marstool.exe --help
```
```
E:\skia_projects\Facial-feature-detection-in-heightmaps\MarsTool>Marstool.exe meshgen --help
```

### To generate volume
```
Y:\MarsTool>MarsTool.exe meshgen -M -C --no-mesh-out Y:\original\asmc\HeadSample
```
```
Y:\MarsTool>MarsTool.exe meshgen -M -C --no-mesh-out Y:\original\asmc\HeadSample -O Y:\original\asmc\HeadSample
```

### My use case

**Generate Volume**
```
Y:\MarsTool>MarsTool.exe meshgen -M -C --no-mesh-out Z:\original\asmc\2021\11143712_KIM_SANGJOON -O E:\skia_projects\Facial-feature-detection-in-heightmaps\data
```

**Generate heightmap**
* Uses volume generated in last step
```
Y:\MarsTool>MarsTool.exe depth -i 1 -d A E:\skia_projects\Facial-feature-detection-in-heightmaps\data\1.3.12.2.1107.5.1.4.66417.30000021090323410187400018283.mask.vol
```

## Batch Operation
Use the **looping notebook** provided in the `MarsTool` folder for batch operation. It will automatically loop through all the patients to generate `volume` files and corresponding `heightmaps`.