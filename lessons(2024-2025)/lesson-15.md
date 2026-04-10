
# Lesson 15: Your Own World - Personal Project & Final Render

## Objective
Students will use this lesson to work on, finish, or polish their own personal 3D scene. By the end of the session, every student will have produced at least one final render they can be proud of and take home.

## Materials Needed
- Blender Software
- Computer with appropriate specifications
- Any work-in-progress `.blend` files from previous lessons

---

## Part 1: Personal Project Time

This is **your** lesson. You can:

- **Continue** a scene or model you started in a previous lesson
- **Start something new** — a character, a landscape, a room, a spaceship, anything you want!
- **Combine** things you've built across different lessons into one scene

### Ideas if you're not sure where to start:
- A cosy bedroom or treehouse
- A futuristic city street
- An alien planet landscape
- A robot character doing something cool
- Your favourite game or movie scene recreated in 3D

> **Tip:** Don't try to make everything perfect. Focus on *one* thing that makes your scene interesting — a great character, a cool prop, or an interesting environment.

---

## Part 2: Getting Your Scene Render-Ready

Before you render, take 5 minutes to check these things:

### 1. Set Up Your Camera
- Press **Numpad 0** to look through the camera
- Move the camera so it frames your scene nicely
- Use **View → Align Active Camera to View** (Ctrl + Alt + Numpad 0) to match your current view

### 2. Check Your Lighting
- Make sure your scene has at least one light source
- If it looks too dark, add a **Point Light** or **Sun Light** (Shift + A → Light)
- You can also use the **World** panel to set a background colour or brightness

### 3. Set Your Render Resolution
- Go to **Properties → Output** (the printer icon)
- A good default is **1920 × 1080** (Full HD)
- For a quick preview render, try **1280 × 720**

### 4. Choose Your Render Engine
- Go to **Properties → Render** (the camera icon)
- **EEVEE** is fast — great for a quick result
- **Cycles** looks more realistic but takes longer — use it if you have time

---

## Part 3: Rendering Your Scene

### Preview Render (quick check)
- Press **F12** to render a single frame
- The render will appear in the Image Editor window
- Press **Escape** to cancel if it's taking too long

### Saving Your Render
- In the render window, go to **Image → Save As** (Alt + S)
- Save as a **PNG** file — this keeps the best quality
- Name it something like `my-scene-final.png`

### Rendering an Animation (optional — if you have keyframes!)
If your scene has animation, you can render it out as a video instead of a single image.

**Before you start — set your output format:**
- Go to **Properties → Output** (the printer icon)
- Under **Output**, choose a folder to save the frames (e.g. your Desktop)
- Change the file format to **FFmpeg Video**
- Under **Encoding**, set the container to **MPEG-4** and the codec to **H.264** — this gives you a standard `.mp4` file

**Set your frame range:**
- At the bottom of the screen, check the **Start Frame** and **End Frame** in the timeline
- A 3-second animation at 24fps = frames 1–72. Keep it short to save time!

**Render the animation:**
- Go to **Render → Render Animation** (or press **Ctrl + F12**)
- Blender will render each frame one by one — this takes a while, so start it early
- The finished video file will be saved to the folder you chose

> **Warning:** Animation rendering can take a long time. Use **EEVEE** (not Cycles) to keep it fast. A 3–5 second clip is plenty for a first animation render!

---

## Conclusion

Today you showed off everything you've learned across this course — modelling, materials, lighting, animation, and more. Your render is yours to keep!

### Share your work:
- Show your render to the group at the end of the session
- Tell everyone: *what is your scene, and what are you most proud of in it?*

## Homework
- Keep working on your scene at home if you want to
- Try tweaking the lighting or camera angle and render again — see how different it looks!
- If you want to go further, check out the **Optional Bonus Lessons** on physics simulations, advanced lighting, and compositing
