# AR SPATIAL MASTER GUIDE
> **TECHNOLOGY:** <model-viewer> (Google) & WebXR
> **COMPATIBILITY:** iOS (QuickLook) & Android (SceneViewer)

## How to use Augmented Reality

1. **Asset Preparation:**
   - You need a `.glb` or `.gltf` 3D model.
   - Place it in `public/assets/`.

2. **Code Implementation:**
   - The system has already injected the `<script>` for model-viewer.
   - To show the AR object, add this HTML where you want the trigger:

   ```html
   <model-viewer 
      src="./assets/my-model.glb" 
      ios-src="./assets/my-model.usdz"
      ar 
      ar-modes="webxr scene-viewer quick-look" 
      camera-controls 
      shadow-intensity="1"
      style="width: 100%; height: 500px;"
   >
      <button slot="ar-button" style="background-color: white; border-radius: 4px; border: none; position: absolute; top: 16px; right: 16px; padding: 10px;">
          Activate AR View
      </button>
   </model-viewer>
   ```

3. **Testing:**
   - AR requires HTTPS. Use Vercel/Netlify to test on mobile.
