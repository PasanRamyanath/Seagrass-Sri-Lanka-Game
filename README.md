# Seagrass Sri Lanka Game

Dive into the vibrant underwater world of Sri Lanka in this immersive game, exploring lush seagrass meadows, colorful corals, and diverse marine life including turtles, fishes, and octopuses. Experience the beauty of the ocean while engaging with a realistic and dynamic environment that brings the sea to life.

## Instructions for playing
- Use `W`, `A`, `S`, `D` to move, and right-click + mouse to look around.
- Use `Shift` + move to sprint.
- When you get close to trash, a **Press `E` to collect trash** prompt will appear.
- Collect as much trash as possible within **150 seconds**.

**Play online:** https://pasanramyanath.github.io/Seagrass-Sri-Lanka-Game/

<!-- Screenshot gallery: 3 images per row, no captions -->
<table>
	<tr>
		<td><img src="screenshots/Screenshot (12).png" alt="" width="300"/></td>
		<td><img src="screenshots/Screenshot (13).png" alt="" width="300"/></td>
		<td><img src="screenshots/Screenshot (14).png" alt="" width="300"/></td>
	</tr>
	<tr>
		<td><img src="screenshots/Screenshot (15).png" alt="" width="300"/></td>
		<td><img src="screenshots/Screenshot (16).png" alt="" width="300"/></td>
		<td><img src="screenshots/Screenshot (17).png" alt="" width="300"/></td>
	</tr>
	<tr>
		<td><img src="screenshots/Screenshot (18).png" alt="" width="300"/></td>
		<td><img src="screenshots/Screenshot (63).png" alt="" width="300"/></td>
		<td><img src="screenshots/Screenshot (64).png" alt="" width="300"/></td>
	</tr>
	<tr>
		<td><img src="screenshots/Screenshot (65).png" alt="" width="300"/></td>
		<td><img src="screenshots/Screenshot (66).png" alt="" width="300"/></td>
		<td><img src="screenshots/Screenshot (67).png" alt="" width="300"/></td>
	</tr>
	<tr>
		<td><img src="screenshots/Screenshot (68).png" alt="" width="300"/></td>
		<td></td>
		<td></td>
	</tr>
</table>

Short Unity/WebGL game showcase built with the Unity game engine using C# and Blender for 3D assets.

**Play**
- **Local (quick):** open `index.html` in your browser (some browsers require a local server for WebGL builds).
- **Local (recommended):** run a simple HTTP server in the build folder. Example using Python (PowerShell):

```powershell
cd "Build"
python -m http.server 8000
# then open http://localhost:8000 in a browser
```

**Project Structure**
- `index.html`: entry point for the WebGL build.
- `Build/`: Unity WebGL build files (loader, framework, data).
- `Cover Image/`: cover art and related images.
- `TemplateData/` and `style.css`: webpage assets.

**Made With**
- **Engine:** Unity (WebGL build)
- **Languages:** C# (game logic)
- **3D Modeling:** Blender (assets and low-poly models)

**Key Features**
- Randomized object spawning/launching around a center point to create dynamic scenes.
- Performance-focused: LOD (Level of Detail) usage, batching, object pooling, and other optimizations.

**Optimization Techniques Used**
- **LOD (Level of Detail):** simplified meshes for distant objects to reduce draw cost.
- **Object Pooling:** reuse frequently spawned objects instead of creating/destroying them repeatedly.
- **Static & Dynamic Batching:** reduce draw calls where applicable.
- **Occlusion & Frustum Culling:** rely on Unity culling to avoid rendering unseen objects.
- **Low-poly assets from Blender:** models optimized in Blender for fewer vertices/triangles.
- **Texture Atlases & Compression:** combine textures and compress where possible to reduce memory and draw overhead.
- **Random Launching Around Center:** objects are spawned and given random velocities/rotations around a configurable center point; consider limiting active objects and using pooling to keep CPU/GPU usage stable.

**Controls**
- Controls depend on the build/scene — typically mouse for camera look and keyboard for basic interactions. See in-game UI for specifics.

**Development Notes**
- The Unity project source is not included in this build folder. To re-open the project in Unity, open the Unity project directory (if available) in the Unity Editor compatible with the project version used to build WebGL.
- If you plan to modify spawning or optimization behavior, look for scripts that control spawn centers, object pools, LOD groups, and performance settings.

**Suggestions / Next Steps**
- Add the full Unity project to the repository (or a separate branch) so contributors can edit scenes and scripts.
- Include sample screenshots or a short GIF in `Cover Image/` and reference them from this README.
- Provide a small `CONTRIBUTING.md` with build steps and Unity editor version used.

**License & Credits**
- See `LICENSE` in repository root for license details.
- Assets created by project author using Blender and other free/third-party assets as noted by the author.
