# Unity Project Standard

## Images

Please images under `Documentation~/images/`

## Use avif for animated images

### Rules
* Please use the relative path to the documentation. 
* Do not use the global path such as "https://". 
* Do not use github upload media
* Use this line to include the images. 

```<img width="300" src="Documentation~/images/01fish.avif" >```.


### Convert video to animated avif
Use this command line to convert the files 

```
ffmpeg -i 02rekfish.mp4 -c:v libsvtav1  -crf 20 02rekfish.avif
```
where 
The valid CRF value range is 0-63, with the default being 50. Lower values correspond to higher quality and greater file size. 

```
ffmpeg -i 01fish.avif -vcodec libwebp  -lossless 0 -loop 0 -preset picture -an -vsync 0 -s 600:600 output.webp
```

## Video 
Please place videos under `Documentation~/videos/`

### Rules
* Use mp4 only when showing movie with sounds. If movie without background sound, use animated images instead. 

* Use this line to include the images.

```<img width="300" src="Documentation~/videos/01fish.mp4" >```

## Unity Package Structure
```
<package-root>
  ├── package.json
  ├── README.md
  ├── CHANGELOG.md
  ├── LICENSE.md
  ├── Third Party Notices.md
  ├── Assets
  │   └── Scenes
  │   └── Materials
  ├── Editor
  │   ├── <company-name>.<package-name>.Editor.asmdef
  │   └── EditorExample.cs
  ├── Runtime
  │   ├── <company-name>.<package-name>.asmdef
  │   ├── Plugins
  │   │   ├── iOS
  │   │   ├── macOS
  │   └── RuntimeExample.cs
  ├── Tests
  │   ├── Editor
  │   │   ├── <company-name>.<package-name>.Editor.Tests.asmdef
  │   │   └── EditorExampleTest.cs
  │   └── Runtime
  │        ├── <company-name>.<package-name>.Tests.asmdef
  │        └── RuntimeExampleTest.cs
  ├── Samples~
  │        ├── SampleFolder1
  │        ├── SampleFolder2
  │        └── ...
  ├── Sources~
  │        ├── SampleFolder1
  │        ├── SampleFolder2
  │        └── ...
  └── Documentation~
       ├── images
       |   └── image.avif
       ├── videos
       |   └── video.mp4
       ├── index.md
       └── get-started.md
```


## Reality

```
<repo-root>
  ├── Assets
  └── Packages
      └── com.holoi.reality.mofa
```

## GitHub

### Main HoloKit account 

https://github.com/holokit/holokit-sdk
https://github.com/holokit/holokit-app
https://github.com/holokit/holokit-app-library
https://github.com/holokit/holokit-multiplayer-template
https://github.com/holokit/holokit-reality-template

Forum: 
https://github.com/orgs/holokit/discussions




