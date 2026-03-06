# Lesson 12: Animation - Blocking & Keyframes

## Objective

By the end of this lesson, students will:

- Understand what keyframes are and how animation works
- Learn the difference between blocking and polished animation
- Animate a rigged character using poses
- Use the Timeline and Dope Sheet
- Create a short character animation (wave, jump, or walk cycle)

## Materials Needed

- Blender Software
- A rigged character from Lesson 11 (or use a simple new one)

---

## Introduction – What Is Animation?

Welcome back! Last lesson, we created a skeleton (armature) and learned how to pose characters.

Today, we're going to make those poses **come to life** by animating them! 🎬

Animation is just like a flipbook:
- You draw one picture
- Then another slightly different picture
- Then another
- When you flip through them fast, it looks like movement!

In Blender, we create **keyframes** (important poses) and Blender fills in the movement between them automatically.

---

## What Are Keyframes?

**Keyframes** are like snapshots of your character at specific moments in time.

Think of it like this:
- Frame 1: Character's arm is down
- Frame 20: Character's arm is up
- Blender automatically creates the movement between Frame 1 and Frame 20!

### Keyframe Shortcuts

To create a keyframe:
- Select a bone in **Pose Mode**
- Rotate or move it with <kbd>R</kbd> or <kbd>G</kbd>
- Press <kbd>I</kbd> to insert a keyframe
- Choose **Location & Rotation** (or just **Rotation** for most poses)

You'll see a **yellow diamond** appear in the timeline at the bottom.

That's your keyframe! 🟨

---

## The Timeline and Playback

Look at the bottom of your screen. You'll see:

- **Timeline** with numbers (frames)
- **Play button** ▶️ to watch your animation
- **Current frame indicator** (blue line)

You can:
- Click and drag the blue line to scrub through time
- Press <kbd>Spacebar</kbd> to play/pause
- Change the **End Frame** to make your animation longer or shorter

Default is 250 frames. For our short animations, **60–120 frames** is plenty.

---

## Part 1: Create a Simple Wave Animation

Let's start with something simple — making your character wave!

### Step 1: Open Your Rigged Character

If you don't have one from last lesson:
1. Create a simple robot (cubes for body, arms, legs, head)
2. Add an armature with bones
3. Parent each part to a bone (or use Automatic Weights)

### Step 2: Set the First Pose (Frame 1)

1. Select your armature
2. Switch to **Pose Mode**
3. Go to **Frame 1** in the timeline
4. Pose the arm down in a neutral position
5. Select the arm bone and press <kbd>I</kbd> → **Rotation**

You just made your first keyframe! 🎉

### Step 3: Set the Second Pose (Frame 20)

1. Move to **Frame 20** in the timeline
2. Rotate the arm bone up (like waving)
3. Press <kbd>I</kbd> → **Rotation**

### Step 4: Set the Third Pose (Frame 40)

1. Move to **Frame 40**
2. Rotate the arm back down
3. Press <kbd>I</kbd> → **Rotation**

### Step 5: Play It Back!

Press <kbd>Spacebar</kbd> or click ▶️

Your character should wave! 👋

If it's too fast or slow:
- Move keyframes closer together = faster
- Move keyframes farther apart = slower

---

## Part 2: Understanding Blocking

**Blocking** is the first stage of animation where you create the main poses without worrying about smoothness.

Think of it like planning:
- Frame 1: Standing
- Frame 30: Jumping up
- Frame 60: Landing

You're not worried about perfection yet — just the key moments.

### Blocking vs. Polished Animation

| Blocking | Polished Animation |
|----------|-------------------|
| Big poses only | Smooth movement |
| Fast to create | Takes longer |
| Planning stage | Final stage |

Today, we're focusing on **blocking** because it's the foundation!

---

## Part 3: Create a Jump Animation (Guided)

Let's animate a jump! This teaches you the basics of timing and poses.

### Keyframe Plan

| Frame | Pose Description |
|-------|-----------------|
| 1     | Standing (neutral) |
| 10    | Crouch down (anticipation) |
| 20    | Jumping up (highest point) |
| 30    | Landing crouch |
| 40    | Back to standing |

### Step-by-Step

**Frame 1 – Standing:**
1. Go to Frame 1
2. Keep character in neutral pose
3. Select all bones: <kbd>A</kbd>
4. Press <kbd>I</kbd> → **Location & Rotation**

**Frame 10 – Crouch:**
1. Go to Frame 10
2. Move body down (select root bone, press <kbd>G Z</kbd>)
3. Rotate legs slightly if you have knee bones
4. Press <kbd>I</kbd> → **Location & Rotation**

**Frame 20 – Jump Up:**
1. Go to Frame 20
2. Move body way up with <kbd>G Z</kbd>
3. Rotate arms up if you want
4. Press <kbd>I</kbd> → **Location & Rotation**

**Frame 30 – Landing Crouch:**
1. Go to Frame 30
2. Copy the crouch pose from Frame 10
3. Press <kbd>I</kbd> → **Location & Rotation**

**Frame 40 – Standing:**
1. Go to Frame 40
2. Return to neutral standing pose
3. Press <kbd>I</kbd> → **Location & Rotation**

### Play It Back!

Press <kbd>Spacebar</kbd>.

You should see a jump! 🦘

---

## Part 4: Create Your Own Animation

Now it's your turn! Choose **ONE** of these:

### Option 1: Wave Animation
Make your character wave both arms in sequence.

### Option 2: Jump Animation
Improve the jump we just made by adding arm movement.

### Option 3: Dance Move
Create a simple dance move:
- Arms go left, then right
- Body rotates
- Loop it!

### Option 4: Sitting Down
Character goes from standing to sitting position.

### Requirements:
- At least **4 keyframes**
- Use **Pose Mode** only
- Duration: **60–120 frames**

Take your time and experiment! Remember: this is blocking, so don't worry if it's not perfect yet.

---

## Optional: Make Your Bones Easier to See (Bone Widgets)

Sometimes bones are hard to see or select, especially when they're inside your character. Let's make them easier to work with using **custom bone shapes** (also called widgets)!

### What Are Bone Widgets?

Instead of boring bone lines, you can use any 3D shape to represent a bone. This makes posing much easier!

Examples:
- Circles for hand controls
- Arrows for direction
- Cubes for body parts

### How to Add a Custom Bone Shape

**Step 1: Create a Simple Shape**
1. Go to **Object Mode**
2. Press <kbd>Shift</kbd> + <kbd>A</kbd> → **Mesh → UV Sphere** (or any shape you like)
3. Scale it down with <kbd>S</kbd> to make it small
4. Move it away from your character (we'll use it as a widget)

**Step 2: Assign It to a Bone**
1. Select your **armature**
2. Switch to **Pose Mode**
3. Select the bone you want to customize (like the hand bone)
4. On the right side, go to **Bone Properties** (bone icon)
5. Scroll down to **Viewport Display**
6. Under **Custom Shape**, click the picker and select your sphere

Now that bone looks like a sphere! 🎯

**Step 3: Make It Pretty (Optional)**
- You can use different shapes for different bones
- Common practice: circles/spheres for limb controls, cubes for body
- The widget shape doesn't affect the actual bone — it's just visual!

### Quick Tip
You can hide the widget objects after assigning them:
1. Select the widget shape in Object Mode
2. Press <kbd>M</kbd> → Move to a new collection called "Widgets"
3. Hide that collection by clicking the eye icon

This keeps your scene clean while still showing the custom bone shapes in Pose Mode!

---

## Optional Challenge: Loop Your Animation

Want your animation to repeat smoothly?

1. Go to your last keyframe
2. Copy the **first frame's pose**
3. Paste it at the end
4. Now it loops! 🔁

In the Timeline settings, enable **Repeat** to see it loop continuously.

---

## Tips for Good Blocking

1. **Start with big movements** (body, root bone)
2. **Then add secondary movements** (arms, head)
3. **Use reference** – act it out yourself or watch videos!
4. **Exaggerate** – bigger poses = more interesting animation
5. **Timing matters** – slow movements need more frames

---

## Common Problems and Fixes

**Problem: Character moves strangely between keyframes**
- Solution: Add more keyframes or change interpolation (we'll learn this next lesson)

**Problem: Can't see keyframes in timeline**
- Solution: Make sure you're selecting the armature, not individual objects

**Problem: Animation is too fast**
- Solution: Move keyframes farther apart in the Dope Sheet

**Problem: Wrong bone moved**
- Solution: Press <kbd>Alt</kbd>+<kbd>G</kbd> or <kbd>Alt</kbd>+<kbd>R</kbd> to reset a bone's transform

---

## Wrap-Up

Today you learned:
- ✅ What keyframes are
- ✅ How to insert keyframes with <kbd>I</kbd>
- ✅ The difference between blocking and polished animation
- ✅ How to use the Timeline
- ✅ How to create basic character animations
- ✅ (Optional) How to add custom bone shapes for easier posing

**Next lesson**, we'll polish these animations using the **Graph Editor and Dope Sheet** to make movements smoother and more natural!

---

## Homework

Choose one:

1. **Finish your animation** from class and make it at least 120 frames long
2. **Create a walk cycle** (advanced challenge):
   - Frame 1: Left leg forward
   - Frame 10: Right leg forward
   - Frame 20: Back to left leg forward
3. **Animate a character expressing emotion**:
   - Happy jump
   - Sad slouch
   - Excited wave

Bonus: Add a second character and make them interact!

---

## Quick Reference

| Action | Shortcut |
|--------|----------|
| Insert Keyframe | <kbd>I</kbd> |
| Play/Pause Animation | <kbd>Spacebar</kbd> |
| Move Keyframes | <kbd>G</kbd> (in Dope Sheet) |
| Delete Keyframe | <kbd>X</kbd> |
| Reset Rotation | <kbd>Alt</kbd>+<kbd>R</kbd> |
| Reset Location | <kbd>Alt</kbd>+<kbd>G</kbd> |

Have fun animating! 🎬
