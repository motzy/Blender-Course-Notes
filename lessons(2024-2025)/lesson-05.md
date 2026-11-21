# Lesson 5: Let's Stretch and Cut – Modelling a Castle Tower 🏰

## Objective

Go beyond whole shapes: enter **Edit Mode**, select **vertices / edges / faces**, and reshape a mesh with **Extrude**, **Inset** and **Loop Cut**. Build a castle tower. Learn which tools to **avoid**, and how to keep a model **connected** and **low-poly**.

> 🧑‍🏫 Examples in `examples/lesson-05/`: a castle tower (`blender class 5.blend`) and a tank (`blender class 5_2/5_3.blend`), both built from a single cylinder or cube.

---

## Recap (5 min) 🔁

- Lesson 4: shapes, **move / rotate / scale**, **duplicate**, **parenting**, **materials last**.
- Whole shapes are limiting. Today we change the **shape itself**.
- Quick question: "How would you make a door in a cube without a second cube?"

---

## Part 1: Edit Mode Basics (10 min) ✏️

| Action | Keyboard | Mouse / menu |
|--------|----------|--------------|
| **Enter / leave Edit Mode** | <kbd>Tab</kbd> | **Mode dropdown** at the top left of the viewport |
| **Vertex / Edge / Face select** | <kbd>1</kbd> / <kbd>2</kbd> / <kbd>3</kbd> | Three icons in the viewport header |
| **Select all / none** | <kbd>A</kbd> / <kbd>Alt</kbd>+<kbd>A</kbd> | **Select** menu |
| **Add to selection** | <kbd>Shift</kbd>+click | Same |
| **Select a whole ring (loop)** | <kbd>Alt</kbd>+click an edge | **Select → Select Loops** |
| **See through the model** | <kbd>Alt</kbd>+<kbd>Z</kbd> (X-ray) | X-ray button in the viewport header |
| **Move / Rotate / Scale** | <kbd>G</kbd> / <kbd>R</kbd> / <kbd>S</kbd> (+ <kbd>X</kbd> <kbd>Y</kbd> <kbd>Z</kbd>) | Toolbar tools + handles |
| **Show triangle/face counts** | n/a | **Overlays dropdown → Statistics** |

### The three modelling tools

| Tool | Keyboard | Mouse / menu | Use it for |
|------|----------|--------------|-----------|
| **Extrude** | <kbd>E</kbd> | Toolbar **Extrude Region**, or **Face → Extrude Faces** | Pull a face out (towers, arms, roofs) or push it in (doors, windows). **Connected** geometry! |
| **Inset** | <kbd>I</kbd> | Toolbar **Inset Faces**, or **Face → Inset Faces** | A smaller face inside a face. Perfect before extruding. |
| **Loop Cut** | <kbd>Ctrl</kbd>+<kbd>R</kbd>, scroll wheel = more cuts, click, then drag or right-click to centre | Toolbar **Loop Cut** | A ring of new edges, **only** where you need detail. |

> 💡 Extrude / Inset / Loop Cut all end with moving the mouse then clicking. **Right-click or <kbd>Esc</kbd> = place it but don't move.**

---

## Part 2: The Golden Rules 🏅

1. **Keep it connected.** One mesh, no floating pieces. Make new parts by **extruding**, not by adding loose shapes.
2. **Keep it low-poly.** Fewer faces = easier to edit. Check the Statistics overlay often.
3. **Only add geometry where you need it.** Need a door? Inset and extrude *one* face. Don't cut the whole model.
4. **Undo is your friend** (<kbd>Ctrl</kbd>+<kbd>Z</kbd> or **Edit → Undo**). Save often.

### ⚠️ Tools to stay away from (for now)

| Don't use | Why it bites | Do this instead |
|-----------|-------------|-----------------|
| **Subdivide** (right-click → **Subdivide**, **Edge → Subdivide**) | Multiplies faces **4× each click**. A cube becomes a heavy mesh in seconds, and nothing is shaped any better. | **Loop Cut** exactly where needed. |
| **Delete → Vertices / Edges** (<kbd>X</kbd>) | Leaves **holes** and broken faces. | Delete → **Faces** to remove a face on purpose, or **Dissolve** to remove edges/vertices cleanly. |
| **Extrude, then right-click / <kbd>Esc</kbd> to "cancel"** | The copy is **left behind in the same spot**: invisible duplicate faces. | Extrude, **click** to confirm; or undo (<kbd>Ctrl</kbd>+<kbd>Z</kbd>) if you change your mind. |
| **<kbd>Shift</kbd>+<kbd>D</kbd> in Edit Mode** | Creates a **disconnected** island. | Extrude instead. |
| **Adding new shapes while in Edit Mode** | They join the mesh as loose, unconnected pieces. | Leave Edit Mode (<kbd>Tab</kbd>), add the object, then place it in Object Mode. |
| **Loop Cut with lots of cuts / Bevel with many segments** | Quickly makes thousands of faces. | One or two cuts. |
| **Knife, Bisect, Remesh, Decimate** | Messy geometry, hard to fix. | Not today. |
| **Proportional Editing (<kbd>O</kbd>)** | When on, moving one vertex drags its neighbours. "Why is everything moving?!" | Turn it **off** (the circle icon in the header). |

> 🧑‍🏫 Tip: say these out loud as you go, and ask kids to **show you the Statistics** if something looks slow.

---

## Part 3: Build a Castle Tower 🏰 (guided)

> 🧑‍🏫 Build live, let kids copy. **No numbers**: do it by eye.

1. **Tower body:** start with a **cylinder** (**Add → Mesh → Cylinder**). Before doing anything else, open the **Add Cylinder** panel at the bottom left and set **Vertices to 12** (default of 32 is far too many).
2. **Go to Edit Mode** (<kbd>Tab</kbd>) and **face select** (<kbd>3</kbd>).
3. **Stretch it tall:** select the **top face**, **Extrude** (<kbd>E</kbd>) up, **click**. Or just scale the whole object up in Object Mode.
4. **Flared base:** **Loop Cut** a ring near the **bottom**. Select the bottom ring (<kbd>Alt</kbd>+click) and **scale** (<kbd>S</kbd>) it wider.
5. **Battlements:** select the **top face**, **Inset** (<kbd>I</kbd>) a little to make a rim. **Extrude** the rim up slightly, click. Then select **every other** rim face (<kbd>Shift</kbd>+click) and **Extrude** them up again for the "teeth".
6. **Door and windows:** select one side face, **Inset**, then **Extrude** *inward* (<kbd>E</kbd> then drag in, or type a negative number).
7. **Roof:** **Tab** out to Object Mode, add a **Cone** (set **Vertices to 12**), and move / scale it onto the tower.
8. **Colour last** (materials from Lesson 4!).

✅ Check **Statistics**: the whole tower should be a few hundred faces at most.

### 🏆 Challenges

| Level | Challenge |
|-------|-----------|
| ⭐ | **Add a second tower** or a wall between two towers. |
| ⭐⭐ | **Castle gate:** inset and extrude a big arch-shaped door. |
| ⭐⭐ | **Tank:** start with a cube, extrude out a turret and a long barrel, inset hatches. (See `blender class 5_2.blend` and `blender class 5_3.blend`.) |
| ⭐⭐⭐ | **Your own building** (house, lighthouse, spaceship). Same tools, same rules! |

---

## 🧑‍🏫 Quick Fixes

| Problem | Fix |
|---------|-----|
| "I can't select the back." | **X-ray** (<kbd>Alt</kbd>+<kbd>Z</kbd>). |
| "Everything moves when I move one vertex." | **Proportional Editing** is on (<kbd>O</kbd>). |
| "My face looks weird or dark." | Probably duplicate geometry from a cancelled extrude. Undo until it's gone. |
| "I have a hole in my model." | A face was deleted. Select the surrounding edge loop and press <kbd>F</kbd> (**Face → Make Edge/Face**). |
| "My model is slow / has too many faces." | Check **Statistics**. Undo back before Subdivide or too many loop cuts. |
| "My cylinder has hundreds of vertices." | Delete it and re-add it, and lower **Vertices** in the **Add** panel. |

---

## Homework

- Finish your castle or building. Add **at least one** feature built with Extrude, Inset **and** Loop Cut.
- Bring in a **screenshot** with the **Statistics** overlay showing.
