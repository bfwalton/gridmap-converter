# GridMap Converter

A Godot 4 editor plugin that provides conversion utilities between GridMap, MeshInstance3D, and MultiMeshInstance3D nodes.

## Features

- **Convert GridMap to Scene** - Convert a GridMap node to individual MeshInstance3D nodes or optimized MultiMeshInstance3D nodes
- **Convert Node to MultiMesh** - Combine multiple MeshInstance3D nodes into efficient MultiMeshInstance3D instances
- **Convert MultiMesh to GridMap** - Convert MultiMeshInstance3D nodes back to a GridMap with auto-generated MeshLibrary

## Installation

1. Download or clone this repository into your Godot project's `addons` folder
2. The folder structure should look like: `res://addons/gridmap-converter/`
3. Enable the plugin in **Project > Project Settings > Plugins > GridMap Converter**

## Usage

### Convert GridMap to Scene

1. Select a GridMap node in the scene tree
2. Click the **"Convert GridMap to Scene"** button in the toolbar
3. Check **"Use MultiMesh"** to combine identical meshes into MultiMeshInstance3D nodes (more efficient)

This creates:
- Individual MeshInstance3D nodes (one per cell), OR
- MultiMeshInstance3D nodes (one per unique mesh type)

Collision shapes are preserved from the original GridMap's MeshLibrary.

### Convert Node to MultiMesh

1. Select a node containing MeshInstance3D children
2. Click the **"Convert Node to MultiMesh"** button
3. Optionally check **"Separate Children"** to preserve non-mesh child nodes

This combines identical meshes into MultiMeshInstance3D instances, reducing draw calls and improving performance.

### Convert MultiMesh to GridMap

1. Select a node containing MultiMeshInstance3D children
2. Click the **"Convert MultiMesh to GridMap"** button

This creates a new GridMap with an auto-generated MeshLibrary containing all unique meshes.

## Requirements

- Godot 4.x

## License

This plugin is provided as-is for use in your projects.
