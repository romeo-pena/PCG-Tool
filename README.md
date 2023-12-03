# PCG-Tool
This Unity Program is the PCG Tool used in the research titled "Exploring the use of Procedural Content Generation of 3D urban scenes for 2D Semantic Segmentation". This repository lacks the Assets folder as it is big in size. To obtain the Assets folder, please contact the owner at romeomanuel.pena@gmail.com. This project uses other assets and packages however such as [Fantastic City Generator](https://assetstore.unity.com/packages/3d/environments/urban/fantastic-city-generator-157625 "Fantastic City Generator"). Additionally, this porject utilizes the [Unity Perception](https://github.com/Unity-Technologies/com.unity.perception "Unity Perception") package to capture images of the Unity Scene. 

Access Link for Assets folder: https://drive.google.com/file/d/14M5nLgQ8C2__VQHXHzA0z4JirWRzIpas/view?usp=sharing 

## Requirements
1. Unity Editor with Editor version 2020.2.0f1
2. NuGet installed in Unity

## How to change scene parameters:
- Make sure the Assets folder and Library folder in the directory and run the project in Unity Editor using 2020.2.0f1 version of Unity Editor
- To change the scene environment structure, go to `Window > Custom City Generator`. Once there you will be prompted with a window that will ask you how big you want the structure to be, and to generate buildings and cars.
- To change the runtime textures, go to `Assets > cartextures`/`Assets > buidingtextures`/`Assets > roadtextures` in the project navigator window, and change/add/delete the PNG files found in those directories
- To change the scene illumination colors and properties, look at the scene gameobjects and change the `Directional Light` object properties. This is the same for other scene rendering capabilites which is found in the `Global Volume` gameobject. Changing the values found in the `Global Volume` also changes how the scene colors are rendered
- To change the car models used in the scene, navigate to `Assets > Fantastic City Generator > Traffic System` in the project navigator and inspect the `Traffic System` object. Change the profebs found in the `la Cars` section of the object depending on the cars you want to use in the scene. Then press again the `Add Traffic System` button on the Custom City Generator window.

## Dataset Capture
1. The project is setup to already do dataset capture upon pressing the play button on the top section of the Unity Editor.
2. The files are saved in a default directory based on the local machines root files.
3. Additionally, you may change the number of images captured in the dataset by changing the `Total Iterations` and `Frames per Iteration` properties of the `CitySimulation` gameobject. The number of images produced when pressing the play button is `Total Iterations` x `Frames per Iteration`. For example we can have 50 `Total Iterations` and 60 `Frames per Iteration`, which gives us a total of 3000 images. 
