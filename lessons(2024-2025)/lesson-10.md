# Lesson 10: Working with Curves – Create Roads, Rollercoasters, and Neon Lights!

## Objective

By the end of this lesson, students will:

- Understand what curves are in Blender
- Learn how to create and edit curves
- Turn curves into 3D objects
- Create a fun project like a rollercoaster, neon sign, or slide
- (Optional) Try drawing in 3D using Grease Pencil

## Materials Needed

- Blender Software

---

## Introduction

So far, we’ve been building everything using shapes like cubes and spheres.

Today, we’re going to use something different called **curves**.

Curves are like **lines you can bend and shape**, and then turn into 3D objects!

Artists use curves to make:

- Roads
- Rollercoasters
- Neon lights
- Pipes and tubes
- Hair and tentacles

Let’s try it!

---

## Adding a Curve

To add a curve:

1. Press <kbd>Shift</kbd> + <kbd>A</kbd>
2. Select **Curve**
3. Click **Bezier Curve**

You will see a line appear in your scene.

This line has **points** you can move.

---

## Editing the Curve

To change its shape:

1. Select the curve
2. Press <kbd>Tab</kbd> to enter **Edit Mode**

You will see points.

You can:

- Press <kbd>G</kbd> to move points
- Press <kbd>R</kbd> to rotate
- Press <kbd>S</kbd> to scale

Try moving the points to create a crazy shape!

**Task:**
Make your curve into a zig-zag or wave shape.

---

## Adding More Points

To make more complex shapes:

1. In Edit Mode
2. Click a point
3. Press <kbd>E</kbd> to **Extrude**

This adds a new point!

**Task:**
Add at least 3 new points.

---

## Turning the Curve into a 3D Tube

Right now, the curve is flat. Let’s make it 3D!

1. Select the curve
2. Go to the **Object Data Properties tab**
   (green curve icon on the right)
3. Find **Geometry**
4. Increase **Bevel Depth**

Your curve becomes a tube!

🎉 You made a pipe!

---

## Advanced Task: Create a Rollercoaster Track (Array + Curve)

Now we’ll make a real rollercoaster track by repeating an object along a curve. This is how artists create tracks, roads, and fences!

---

### Step 1: Create the Curve Path

1. Press <kbd>Shift</kbd> + <kbd>A</kbd> → **Curve → Bezier Curve**
2. Press <kbd>Tab</kbd> for **Edit Mode**
3. Use:
   - <kbd>G</kbd> to move points
   - <kbd>E</kbd> to extrude new points

Create a rollercoaster shape.

---

### Step 2: Create One Track Piece

1. Press <kbd>Shift</kbd> + <kbd>A</kbd> → **Mesh → Cube**
2. Scale it with <kbd>S</kbd> into a small rectangle

Press <kbd>Ctrl</kbd> + <kbd>A</kbd> → **Apply Scale**

---

### Step 3: Add Array Modifier

1. Select the cube
2. Go to the **Modifier tab** (blue wrench)
3. Click **Add Modifier → Array**
4. Increase **Count** to **20–50**

---

### Step 4: Make it Follow the Curve

1. Click **Add Modifier → Curve**
2. In **Object**, select your curve

Your track will now follow the curve!

If it looks wrong, change **Deform Axis** to X, Y, or Z.

---

## Task

Create one of the following using this technique:

- Rollercoaster
- Train track
- Fence
- Snake body
- Robot tail

---

## Optional: Draw in 3D with Grease Pencil

Grease Pencil lets you draw directly in 3D!

To try it:

1. Press <kbd>Shift</kbd> + <kbd>A</kbd>
2. Select **Grease Pencil**
3. Click **Blank**
4. Switch to **Draw Mode**

Now draw!

You can draw:

- Characters
- Shapes
- Scribbles in 3D space

---

## Optional Challenge: Neon Light

Create a neon light:

1. Create a curve
2. Shape it into:
    - Your name
    - A lightning bolt
    - A symbol

3. Add Bevel Depth
4. Add a bright material
5. Turn on **Emission**

Now it glows!

---

## Homework

Create something using curves:

Ideas:

- A race track
- A snake
- Your name in neon
- A rollercoaster

Bonus:
Add materials and lighting!
