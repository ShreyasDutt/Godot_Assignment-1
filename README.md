# Godot Landscape Generator with Mesh and Noise

This project demonstrates how to generate a 3D terrain in the Godot Engine using the `FastNoiseLite` module to create Perlin noise-based heightmaps. It generates a landscape by manipulating a mesh through vertex-based noise and displays the terrain in real-time. You can adjust the size and characteristics of the terrain through exported properties.

## Features

- **Perlin Noise-Based Terrain:** The terrain is generated using Perlin noise, creating realistic, smooth hills and valleys.
- **Dynamic Mesh Generation:** The mesh is generated dynamically based on the given dimensions (x and z sizes).
- **Real-Time Updates:** The terrain can be regenerated in real-time by toggling the update flag in the editor.
- **Vertex Visualization:** Optionally, vertices can be visualized with small spheres to better understand how the terrain is built.
- **Customizable Parameters:**
  - `xSize`: Controls the width of the terrain.
  - `zSize`: Controls the depth of the terrain.
  - `frequency`: Adjusts the noise scale to control the roughness of the terrain.

## Getting Started

- Basic understanding of noise, FastnoiseLite, Textures and Godot.

### Prerequisites

- **Godot Engine:** Make sure you have Godot Engine installed (preferably version 4.0 or higher).
- **FastNoiseLite:** This project makes use of the `FastNoiseLite` plugin that should be enabled or included in the project.

### Setup

1. Clone or download the project files.
2. Open the project in Godot.
3. Adjust the `xSize` and `zSize` properties in the inspector to set the dimensions of the terrain.
4. Optionally, toggle the `update` flag to regenerate the terrain dynamically while the game is running.

### Code Overview

- **`generate_terrain()`**: This function uses `FastNoiseLite` to generate 2D Perlin noise for terrain height. It then adds vertices and triangles to a mesh using the `SurfaceTool`.
  
- **`draw_sphere()`**: This helper function is used to visualize the vertices by placing small spheres at each vertex position.

- **`_process()`**: This checks the `update` flag and regenerates the terrain in real-time when toggled.

### Example Usage

1. Set the `xSize` and `zSize` to define the size of the terrain.
2. Adjust the `frequency` value within the `generate_terrain()` method to control the roughness or smoothness of the terrain.
3. Run the project to generate a mesh-based landscape based on the Perlin noise.

### Customization

- Modify the noise type by adjusting the `noise_type` of `FastNoiseLite` for different effects (e.g., Simplex noise).
- For this project we have used Perlin noise, use of any other noise is also possible.
- Experiment with different scaling factors and noise frequencies to produce varied terrain styles.

### Screenshots
- Editor View
- ![image](https://github.com/user-attachments/assets/e412ed63-9508-4f85-b3a1-ac296ed84a02)
- Run time view
- ![image](https://github.com/user-attachments/assets/1593678e-51af-4acc-839b-1bac82058465)

Camera views can be changed according to the need.

