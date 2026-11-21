# Lesson 4: Shapes Everywhere – Build-a-Bot! 🤖

## Objective

Build a **robot** out of basic shapes (cubes, cylinders, spheres). Students practise **move / rotate / scale**, learn to **duplicate** and **parent** (glue objects together), then add **materials**, a **light** and a **pose**.

> 🧑‍🏫 **Teacher note** – There are no exact measurements on purpose. Build it by eye, together with the class, and let every robot turn out different. Last year's robots are in `examples/lesson-04/` for inspiration (show them *after* the kids have had a go, or every robot will look the same).

---

## Part 0: Quick Recap (5–10 minutes) 🔁

Ask the class, let them shout answers, demo as they answer.

**Lesson 1 – Basics**
- The big middle window is the **viewport**; the list on the top right is the **outliner**.
- <kbd>Shift</kbd>+<kbd>A</kbd> adds a new object (Mesh → Cube, Cylinder, Sphere…). *(Or the **Add** menu in the viewport header.)*
- <kbd>G</kbd> = **move**, <kbd>R</kbd> = **rotate**, <kbd>S</kbd> = **scale**. Press <kbd>X</kbd>, <kbd>Y</kbd> or <kbd>Z</kbd> afterwards to lock to one direction. *(Or click the **Move / Rotate / Scale** tools in the toolbar on the left and drag the coloured handles. 🔴 X, 🟢 Y, 🔵 Z.)*
- Middle mouse = orbit, <kbd>Shift</kbd> + middle mouse = pan, scroll = zoom. *(Or drag the **navigation gizmo** at the top right of the viewport: ball = orbit, ✋ = pan, 🔍 = zoom.)*
- Exact numbers live in the **N panel** → **Item** tab. *(Press <kbd>N</kbd>, or **View → Sidebar**, or click the tiny arrow at the top right of the viewport.)*

**Lesson 2 – Lights & Animation**
- Light types: **Point** (lightbulb), **Sun**, **Area** (softbox), **Spot** (torch).
- **Keyframes** (<kbd>I</kbd>) store a value at one moment in time. *(Or right-click a value → **Insert Keyframe**.)*
- Viewport shading: Wireframe, Solid, Material Preview, Rendered.

**Lesson 3 – Materials**
- Materials live in the **Material tab** (the checkered sphere icon).
- **Principled BSDF**: Base Color, Metallic, Roughness, Emission.
- Use **Material Preview** to see colours in the viewport.

Can lead into the next part by identifying what basic shapes everyday objects are ("a traffic cone", "a can of soup", "a die") and let the kids say which basic shape it is. Then flip it: "What's a *robot* made of?" → *shapes!* That's today.

---

## Part 1: New Tricks (5 minutes) 🧰

Start a **General** project, **save it** (<kbd>Ctrl</kbd>+<kbd>S</kbd> or **File → Save**) as `robot_yourname.blend`, and remind kids to save after every stage.

Every shortcut has a mouse route too, so show both and let kids pick:

| Trick | Keyboard | Mouse / menu |
|-------|----------|--------------|
| **Duplicate** | <kbd>Shift</kbd>+<kbd>D</kbd>, then right-click to drop it in place | **Object → Duplicate Objects**, then right-click to drop it in place |
| **Rename** | <kbd>F2</kbd> | Double-click the name in the Outliner |
| **Undo** | <kbd>Ctrl</kbd>+<kbd>Z</kbd> | **Edit → Undo** |
| **Select several** | <kbd>Shift</kbd>+click in the viewport | <kbd>Ctrl</kbd>+click names in the Outliner, or the **Select Box** tool and drag a box |
| **Parent (glue)** | Click the **children**, add the **parent last**, then <kbd>Ctrl</kbd>+<kbd>P</kbd> → **Object** | Same selection, then **Object → Parent → Object** |
| **Reset 3D cursor** | <kbd>Shift</kbd>+<kbd>C</kbd> | **Object → Snap → Cursor to World Origin** |
| **Front view** | <kbd>Numpad 1</kbd> | **View → Viewpoint → Front**, or click the **-Y** circle on the gizmo |

🧠 **Parenting memory trick:** *"Kids first, parent last."* The **child** follows everything the **parent** does.

> 💡 Front view (a straight-on, flat look) makes it much easier to line parts up. Use it a lot!

---

## Part 2: Build the Robot 🔧

> 🧑‍🏫 **Teacher note** – Do each stage live on the projector (about 3–5 minutes each), then give kids a moment to copy it. Build by eye: "make it a bit wider", "a bit shorter". Check every few stages that everyone is keeping up, and let kids add their own twists.

**Build order: body → head → neck → face and antenna → arms → legs → feet**

### 1. Body 📦
- Use the **default cube**. **Stretch** it taller (<kbd>S</kbd> then <kbd>Z</kbd>) so it looks like a chunky torso. *(Or the **Scale** tool and drag the 🔵 blue box.)*
- Rename it `Body`.
- 🎯 *Mini-challenge:* swap the cube for a cylinder for a barrel-shaped robot!

### 2. Head 🧠
- Add another **cube**, **shrink** it, and **move** it on top of the body.

### 3. Neck 🔩
- Add a small **cylinder**, **squash** it short, and place it between the head and the body.
- *(If the neck is hidden, move the head up a little.)*

### 4. Face and antenna 👀📡
- **Eyes:** two **cylinders** or spheres on the front of the head. Rotate cylinders 90° so the flat end faces us (like camera lenses). Make one, **duplicate** it, move the copy across.
- **Mouth:** a thin, wide **cube**.
- **Antenna:** a thin **cylinder** with a small **sphere** on top.

> 🧭 The **front** of the default view faces the **-Y** side. Use front view (<kbd>Numpad 1</kbd>) and the face should point at you.

🏁 *Checkpoint:* head, face and antenna on a body. High-five your neighbour! ✋ *(No arms yet, so it looks a bit like a vending machine 😄)*

### 5. Arms 💪 (the important bit!)

Build **one arm** out of **rectangular boxes (stretched cubes)** with **spheres as joints**:

> 🔵 shoulder → ▭ upper arm → 🔵 elbow → ▭ forearm → 🔵 hand

Place the shoulder at the side of the body, then build the arm hanging down from it.

#### 😬 The problem
Select the **upper arm** and **rotate** it. It spins around its **middle** and flies off the shoulder! Every object rotates around a little orange dot called its **origin**.

> 🧑‍🏫 Let them discover this and groan. Then say: *"Let's fix it like real engineers – by gluing the pieces together."* Undo (<kbd>Ctrl</kbd>+<kbd>Z</kbd>) before continuing.

#### ✅ The fix: parenting
Work from the hand towards the shoulder:
1. **Elbow group:** forearm + hand (children), **elbow last** (parent) → **Parent → Object**.
2. **Shoulder group:** upper arm + elbow (children), **shoulder last** (parent) → **Parent → Object**.

The Outliner now shows a family tree. 🎉 **Test it:** rotate the **shoulder** and the whole arm swings. Rotate the **elbow** and only the forearm and hand bend!

> ⚠️ Don't **scale** a parent after parenting (it squashes everything glued to it). Move and rotate are fine.

#### 🐑 Clone the arm
1. In the Outliner, **right-click the shoulder → Select Hierarchy** (selects the whole arm). *(Make sure the arm isn't posed yet.)*
2. **Duplicate** it and right-click to drop it in place.
3. Click only the **new shoulder** and move it to the other side of the body. (In the N panel, make its **X location** the negative of the first one.)

### 6. Legs 🦿
- Same trick as the arms, only shorter: a **box** for each leg, plus (optional) a **sphere** for the hip and knee joint.
- Build **one**, then **duplicate** it and move the copy to the other side.
- *Tip:* parent each leg's pieces to its hip joint so legs can swing too.

### 7. Feet 👟
- A flat, wide **cube** at the bottom of each leg. Build one, **duplicate**, move across.
- Stand the robot on the floor. If feet float or sink, check from the **front view**.

> 🎨 **Don't add colours yet!** Duplicating and copy/pasting treat materials differently, which gets confusing. We colour the robot in Part 3, once all the copying is done.

### ✨ Extras (fast finishers)
Cone nose, ear-muffs, backpack, chest buttons, rocket boots, a second antenna, spiky shoulders, a tail…

---

## Part 3: Make It Shine ✨

### Materials (reminder from Lesson 3)

> ⚠️ **Add materials LAST, after all the building and duplicating is finished!**
> Copies of an object bring a material along, and **how** you copy decides what happens:
> - **Duplicate** (<kbd>Shift</kbd>+<kbd>D</kbd>) → the copy **shares** the original's material. Change the colour on one and **all** of them change.
> - **Copy / Paste** (<kbd>Ctrl</kbd>+<kbd>C</kbd> then <kbd>Ctrl</kbd>+<kbd>V</kbd>, or **Object → Copy Objects / Paste Objects**) → the copy gets its **own separate** material (`Material.001`…). Change the colour on one and the other stays the same.
>
> Kids mix these two up all the time, so colours start changing (or *not* changing) when they don't expect it. The simple fix: **build first, colour at the end.** 🎨
> 🧑‍🏫 Say this out loud *before* the kids start colouring, and again if someone says "my hands turned blue too!" or "my other arm didn't change!"

We want a few materials shared by many parts, **not** 25 separate paint jobs. First, make the material:

1. Click the **Body** → **Material tab** (the checkered sphere icon) → **New**.
2. Rename it `Robot Body`, and pick a colour (try **Metallic** 1, **Roughness** 0.3).

Now give it to the other parts. Pick whichever way you like:

#### Way 1: All at once (fastest) ⚡
1. Select all the parts that should match (head, neck, upper arms, forearms, legs…), then click the **Body last** so it's the active one (brightest outline).
2. **Object → Link/Transfer Data → Link Materials** (or <kbd>Ctrl</kbd>+<kbd>L</kbd>).
3. Done! Every selected part now uses `Robot Body`. Change the colour once and **all** of them update.

#### Way 2: One by one 🐢 (slower, but easy to understand)
1. Click a part (for example the **Head**) and open the **Material tab**.
2. Click the **Browse Material** button (the little sphere icon to the left of the material name). A list of materials appears.
3. Pick `Robot Body`. Repeat for each part.

> 🚫 **Don't press "New" on every part!** That makes a brand-new material (`Material.001`, `Material.002`…) for each one, just like copy/paste does. Pick the **existing** material from the Browse list instead. Otherwise changing the colour later won't update all the parts.
> *(Want a part that's a different colour from its copy? Select it, click the **duplicate** icon next to the material name to give it its own copy, then change the colour. That's how a Rainbow Bot is made!)*

Make two more materials the same way (create it on one part, then share it):
- **Robot Joint**: a contrasting colour for the spheres (shoulders, elbows, hands, knees) and feet.
- **Robot Glow**: for the eyes and antenna ball. Use **Emission** (colour + **Strength** about 5) so they light up.

### Light (reminder from Lesson 2)
- **Add → Light → Area** (or Point), place it in front and above the robot.
- Try a **coloured light** (blue or orange). Switch to **Rendered** view (top right of the viewport, 4th sphere icon) and watch the eyes glow.

### Strike a pose! 🕺
**Rotate** the shoulders, elbows, head and legs: 🙋 wave, 💪 flex, 🕺 dance, 🛑 "stop!".

---

## Part 4: Optional Challenges 🏆

| Level | Challenge |
|-------|-----------|
| ⭐ | **Rainbow Bot:** a different colour for every part. |
| ⭐ | **Robot Sidekick:** select everything (<kbd>A</kbd>, or **Select → All**), **duplicate**, and **scale** the copy down for a mini-robot. |
| ⭐⭐ | **Not Only Boxes:** a sphere head and a cylinder body. Cuter? |
| ⭐⭐⭐ | **Robot Waves Hello:** keyframe the shoulder rotation (frame 1 down, frame 20 up, frame 40 down). Insert with <kbd>I</kbd> or right-click the value → **Insert Keyframe**. Play with <kbd>Space</kbd> or the **▶** button in the Timeline. |
| ⭐⭐⭐ | **Everything glued:** parent the head, face, antenna and limbs to the body so the whole robot moves as one. |

---

## Part 5: Wrap-Up – Robot Parade! 🎬 (5 minutes)

Each student shows their robot and tells the class its **name** and **special power**. 🎤

Ask:
- What's the difference between **move**, **rotate** and **scale**?
- What happens to the *children* when you rotate the *parent*?
- Why **duplicate** instead of building everything twice?

---

## 🧑‍🏫 Teacher Cheat Sheet

**Rough timing (about 90 minutes):** recap 10 → new tricks 5 → stages 1–4 (body to antenna) 20 → arms and parenting 25 → legs and feet 10 → materials, light, pose 15 → parade 5.

| Problem | Fix |
|---------|-----|
| "My shape appeared somewhere weird." | Reset the 3D cursor (<kbd>Shift</kbd>+<kbd>C</kbd>, or **Object → Snap → Cursor to World Origin**). |
| "I changed the wrong thing." | Undo (<kbd>Ctrl</kbd>+<kbd>Z</kbd> or **Edit → Undo**), then click the object **in the Outliner**. |
| "The arm doesn't follow the shoulder." | The parent wasn't selected **last**. Undo and redo the parenting. |
| "Everything squashed when I scaled." | Scaled a parent. Undo and scale the child instead. |
| "The face is on the back." | Front is **-Y**. Move the face to the other side, or rotate the head 180°. |
| "I can't see the colours." | Switch to **Material Preview**. |
| "The eyes don't glow." | Check **Emission** strength and use **Rendered** view. |
| "I lost my robot!" | **View → Frame All** (or <kbd>Home</kbd> with the mouse over the viewport). |

---

## Homework

- Make a **variation of your robot**: new colours, a different head, extra gadgets.
- **Bonus:** build a robot **pet** (dog, cat or bird) with the same tricks.
- Bring a **screenshot** of your favourite robot to show next lesson!
