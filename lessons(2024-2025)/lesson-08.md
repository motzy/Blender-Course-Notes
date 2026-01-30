# Lesson 8: Wrap It and Paint It - UVs & Textures

## Objective
By the end of this 1.5 hour class, students will:
- Learn what UVs are in a simple way
- Unwrap a small model (lego brick, robot part or toy)
- Apply an image texture and do a small, fun texture paint (sticker or color patch)
- Save their painted texture and render a final image

## Materials Needed
- Blender (same version used in previous lessons)
- A simple model from an earlier lesson (lego brick, robot head, snowman part) or a new simple model
- A few example textures (wood, plastic, sticker) — instructor provides or students use one from their computer
- Pen/tablet optional for painting, mouse is fine
- Projector / screen for instructor demo

---

## Simple Explanation (for students)
- 3D model = shape. A texture = picture we wrap around the shape.
- UVs are like cutting and flattening a paper model so we can glue a picture onto it. UV Editor shows that flattened paper.
- We don't need perfect UVs today — just enough so the texture looks okay.

---

## Instructor Demo — Step-by-step (live, with projector)

1. Open the student's model or a demo file.
2. Switch to Layout or UV Editing workspace (top bar).
   - Left: 3D Viewport. Right: UV Editor.
3. Enter Edit Mode (Tab) and select the whole object (A).
4. Mark seams (simple rule):
   - Think where you'd cut paper to flatten the model.
   - Select edges, right-click → Mark Seam.
   - For a lego brick: mark around the base and along the sides so top and sides become islands.
   - Tip: fewer seams = more stretching. Add seams where hidden or on edges.
5. Unwrap:
   - With faces selected, press U → choose "Unwrap".
   - If model is simple, try U → "Smart UV Project" for a quick result.
6. Look in the UV Editor:
   - You should see islands (flattened pieces).
   - If islands overlap, show how to select, move and rotate them.

(Keep language simple; show one or two examples only.)

---

## Applying an Image Texture (10–15 min)

1. Switch to the Shading workspace.
2. Select the object, go to the Material tab.
3. In Shader Editor:
   - Add → Texture → Image Texture.
   - Click "Open" and choose an image (plastic, wood, sticker).
   - Connect Color output → Base Color of Principled BSDF.
4. Return to UV Edting, switch the viewport to Material Preview or Rendered to see the texture.
5. Demonstrate how editing the UVs impacts how the texture is projected onto the object.
6. Try different UV unwraps.

---

## Texture Paint — Make a Sticker or Color Patch (15–20 min)

1. In the UV Editor, create a new image if you want to paint onto a fresh texture:
   - Image → New → give a name (e.g., brick_sticker), 1024×1024 is fine.
2. In the Shader Editor, select that image in the Image Texture node (so Blender paints into this image).
3. Switch the main window to Texture Paint mode.
4. Use the brush to paint a small sticker, eyes, or color stripe:
   - Pick a brush color and size.
   - Paint directly on the model in the 3D Viewport.
5. Save the painted image: in the Image menu of the UV Editor → Save As… (important — otherwise paint will be lost).

Tips:
- Use low strength and larger brush for soft patches.
- For precise details, zoom in and reduce brush size.

---

## Homework
- Finish texturing one of your earlier models:
  - Use one photo texture (e.g., wood or plastic) and paint over it or combine multiple textures.

Have fun — encourage creative stickers and colors so students stay excited while learning UVs!
