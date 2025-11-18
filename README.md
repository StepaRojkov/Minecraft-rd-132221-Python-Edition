📦 Minecraft-rd-132221-Python-Edition
A full open-source port of Minecraft RubyDung (RD 132221) written in Python using PyOpenGL and Pygame.

This project is an accurate yet extensible reconstruction of one of the earliest Minecraft versions (RubyDung, build RD 132221), rewritten entirely in Python with PyOpenGL, Pygame, and custom rendering modules.

The goal of the project is to provide the community with an open, understandable, and fully moddable foundation for experimentation, education, and building new ideas based on the earliest Minecraft prototype.
<img width="1023" height="766" alt="Снимок экрана 2025-11-19 000820" src="https://github.com/user-attachments/assets/4e0c244a-7b98-48e8-bdd2-0ab98b43db89" />

✨ Features

• Fully functional RD 132221-style block rendering
• Block tesselation (Tesselator)
• Chunk rendering via OpenGL display lists
• Implemented frustum culling
• Level system with saving/loading via level.dat
• Player physics with AABB collisions
• Accurate 3D DDA raycast for block selection
• Breaking and placing blocks (LMB/RMB)
• Simple dynamic lighting (bright/dark block simulation)
• Easily moddable and extendable codebase

🎮 Controls

Movement — W A S D or Arrow keys
Jump — Space
Break block — Left Mouse Button
Place block — Right Mouse Button
Respawn player — R
Save world — S
Exit — ESC

🧱 Architecture Overview

rubydung.py
• Main game loop, OpenGL initialization, input handling, raycasting, rendering.

Level / Chunk
• Stores block data
• Regenerates chunks when needed
• Saves and loads the level.dat file

Tile
• Renders block geometry (top, bottom, sides)

Player
• Position and rotation
• AABB collision system
• Jumping, movement, gravity

Tesselator
• A minimal wrapper around OpenGL glBegin/glEnd (like early Minecraft)

Frustum
• Determines which chunks are visible → rendering optimization

🔧 Configuration & Modding

This project is intentionally simple and flexible:

• Want new block types? — extend Tile.
• Want world generation? — modify Level.__init__.
• Want shaders? — rewrite rendering in LevelRenderer.
• Want multiplayer? — implement a server subsystem.

The codebase can also be ported to ModernGL or moderngl-window with minimal effort.

📄 License

This project is released under the MIT license, allowing:

• use
• modification
• redistribution
• commercial use

❤️ Why This Project Exists

RubyDung is a small but historic version of Minecraft.
It’s perfect for studying engines, 3D graphics, tesselation, optimization, and understanding legacy OpenGL.

This project recreates and expands that version so anyone can:

• explore early Minecraft architecture
• build experiments on top of it
• modify the engine freely
• learn OpenGL and Python through a real working example

🧭 Planned Improvements (TODO)

• ModernGL backend
• Proper 16×16 textures from RD 132211
• Custom block selection mechanics
• World generation system
• GUI / main menu
• Flight mode
• Possible WASM/Browser port via Pyodide

🤝 Contribute

PRs, forks, and ideas are welcome.
I’ll be happy if this project becomes a foundation for your own experiments.
