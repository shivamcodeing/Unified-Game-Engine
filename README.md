# Unified Game Engine (UGE)

![UGE Logo](assets/uge-logo.png)

> **Unity-style ease of use** + **Godot-level lightweight performance** + **Unreal-style power** + **Blender-like modeling ambitions**

---

## 🚀 Vision
UGE aims to combine the best of modern game engines:
- **Unity-style ease of use**: GameObject + AddComponent workflow, beginner-friendly.
- **Godot-level lightweight performance**: Runs on 10-20 year old low-end PCs (integrated GPUs, 4GB RAM, dual-core CPUs like Intel Core 2 Duo / i5-3230M).
- **Unreal-style power**: Blueprint visual scripting, Animation Blueprint state machines.
- **Blender-like modeling ambitions**: Long-term goal (deprioritized; glTF/OBJ import first).

---

## 🎯 Target Audience
- **Beginners to advanced users**
- **2D and 3D game development**
- **Easy-to-use inbuilt code editor**

---

## 🛠️ Tech Stack
| Category          | Technology               |
|-------------------|--------------------------|
| **Language**      | C++17                    |
| **Renderer**      | OpenGL 3.3 Core Profile  |
| **Windowing**     | GLFW                     |
| **OpenGL Loader** | GLEW                     |
| **Math**          | GLM (header-only)        |
| **Scripting**     | Lua (sol2, header-only)  |
| **Physics**       | Bullet (3D) + Box2D (2D) |
| **Editor UI**     | Dear ImGui                |
| **Visual Scripting** | imnodes (node editor) |
| **Architecture**  | Custom ECS               |
| **Build System**  | CMake                    |
| **Platforms**     | Windows (MSYS2/MinGW), Linux (Zorin OS/Ubuntu) |

---

## 📦 Already Built (v0.1 + v0.2)
- **Core**: `Window.h/.cpp` (GLFW + OpenGL 3.3 context)
- **ECS**:
  - `Entity.h` (Entity = `uint32_t`)
  - `Registry.h` (CreateEntity, AddComponent, GetComponent, HasComponent, RemoveComponent, View, DestroyEntity)
  - `Components/Transform.h` (Position/Rotation/Scale)
  - `Components/ScriptComponent.h` (ScriptPath, Loaded, LastWriteTime)
- **Scripting**:
  - `ScriptEngine.h/.cpp` (sol2 state, Lua bindings for Transform/Vec3, hot-reload)
- **Main**: `main.cpp` (60Hz fixed-timestep game loop, demo entity with Transform + ScriptComponent)
- **Build**: `CMakeLists.txt` (system GLFW/GLEW/GLM/Lua5.4 via pkg-config, vendored sol2)

---

## 📁 Repository Structure