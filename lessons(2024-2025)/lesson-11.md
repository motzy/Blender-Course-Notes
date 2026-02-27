# Lesson 11: Rigging and Weight Painting – Make Your Character Move!

## Objective

By the end of this lesson, students will:

- Understand what an Armature (skeleton) is
- Create a skeleton and add bones 
- Parent objects directly to bones
- Use Pose Mode to move a character
- Try automatic weights and basic weight painting

---

# Part 1: Build a Simple Robot (Rigid Character)

We’ll build a simple Roblox-style character using separate objects.

Create:

- Cube for body
- Cube for head
- Cube for left arm
- Cube for right arm
- Cube for left leg
- Cube for right leg

Keep every part as a separate object.

Tip:
Use <kbd>Shift</kbd> + <kbd>D</kbd> to duplicate arms and legs.

Before rigging:

Select all objects → <kbd>Ctrl</kbd> + <kbd>A</kbd> → Apply All Transforms

---

# Part 2: Add an Armature

1. Press <kbd>Shift</kbd> + <kbd>A</kbd>
2. Select **Armature**

A single bone appears.

Select the armature and:

- Go to Armature Properties
- Enable **In Front** (so bones are visible through the mesh)

Press <kbd>Tab</kbd> to enter **Edit Mode**

---

# Understanding Modes

Edit Mode = building the skeleton  
Pose Mode = moving the character

If you move bones in Edit Mode, you change their length and structure.

To pose, you MUST use Pose Mode.

---

# Part 3: Creating Bones Properly

## Create Spine and Head (Using Extrude)

Select the existing bone.

Press <kbd>E</kbd> to extrude upward.

This creates a connected head bone.

---

## Add Arm Bones Without Extruding

Instead of extruding from the spine:

Press <kbd>Shift</kbd> + <kbd>A</kbd> (while in Armature Edit Mode).

A new bone appears at the 3D cursor.

Move it with <kbd>G</kbd> to shoulder height.
Rotate with <kbd>R</kbd> if needed.

This bone is separate from the spine.

To parent it:

1. Select the arm bone
2. Shift-select the spine bone
3. Press <kbd>Ctrl</kbd> + <kbd>P</kbd>
4. Choose **Keep Offset**

Now the arm follows the spine but is not physically connected.

Duplicate it with <kbd>Shift</kbd> + <kbd>D</kbd> for the other side.

---

## Add Leg Bones

Repeat the same method:

- <kbd>Shift</kbd> + <kbd>A</kbd> to add a new bone
- Move it below the body
- Rotate it downward
- Parent to spine using **Keep Offset**
- Duplicate for the other leg

---

# Part 4: Parent Robot Parts to Bones (Rigid Method)

Now we connect each object directly to its bone.

Example: Left Arm

1. Select the left arm cube
2. Shift-select the armature
3. Press <kbd>Ctrl</kbd> + <kbd>P</kbd>
4. Choose **Bone**
5. Select the correct arm bone

Repeat for:

- Right arm
- Left leg
- Right leg
- Head
- Body (parent to spine bone)

Now each object follows exactly one bone.

---

# Part 5: Pose the Character

Select the armature.

Switch to **Pose Mode**.

Select a bone.

Press:

- <kbd>R</kbd> to rotate (most common)
- <kbd>G</kbd> only for root movement

Rotate arms and legs.

Your robot should move like an action figure.

---

# Part 6: More Advanced – Automatic Weights (Organic Example)

Now let’s try a bending character.

Create a single cube.

Go into Edit Mode and extrude:

- Arms
- Legs

Make one connected mesh.

Add an armature like before.

This time:

1. Select the mesh
2. Shift-select the armature
3. Press <kbd>Ctrl</kbd> + <kbd>P</kbd>
4. Choose **With Automatic Weights**

Switch to Pose Mode and rotate bones.

Now the mesh bends!

## Improving Bending with Subdivision

When we use Automatic Weights, the mesh needs enough geometry to bend smoothly.  
If the cube has very few faces, the arms and legs will bend in a blocky way.

### Add a Subdivision Modifier

1. Select your character mesh
2. Go to the **Modifier tab** (blue wrench icon)
3. Click **Add Modifier → Subdivision Surface**
4. Set **Levels Viewport** to 1 or 2

You should see the mesh become smoother.

### Apply the Modifier

To make the extra geometry permanent:

1. Click the small arrow on the modifier
2. Choose **Apply**

Now your character has more geometry and will bend much better when posing.

Tip:
Don’t use very high subdivision levels — it can slow Blender down.

---

# Part 7: Fixing with Weight Paint

If bending looks strange:

1. Select the mesh
2. Switch to **Weight Paint Mode**
3. Select a bone
4. Paint red where influence should be strong
5. Paint blue where it should not move

Red = strong influence  
Blue = no influence

---

# Task

Pose your character doing something fun:

- Waving
- Jumping
- Dancing
- Superhero landing

Take a screenshot.

---

## Homework

- Improve your character
- Add more bones (elbows or knees)
- Try rigging a creature