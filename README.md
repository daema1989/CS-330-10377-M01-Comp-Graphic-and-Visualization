# CS-330-10377-M01-Comp-Graphic-and-Visualization
8-2
How do I approach designing software?
What new design skills has your work on the project helped you to craft?
What design process did you follow for your project work?
How could tactics from your design approach be applied in future work?
How do I approach developing programs?
What new development strategies did you use while working on your 3D scene?
How did iteration factor into your development?
How has your approach to developing code evolved throughout the milestones, which led you to the project’s completion?
How can computer science help me in reaching my goals?
How do computational graphics and visualizations give you new knowledge and skills that can be applied in your future educational pathway?
How do computational graphics and visualizations give you new knowledge and skills that can be applied in your future professional pathway?

My process now looks like:

Define the purpose

What problem is this software solving?

For the 3D scene: “Show realistic lighting behavior (ambient, diffuse, specular) in a believable environment.”

Identify the core features

For the scene: camera, objects, materials, and lighting types.

For an app: inputs, outputs, main actions.

Model the system before coding

I break the work into objects/components and their responsibilities.

Example: A Light class shouldn’t also manage camera movement. A Mesh shouldn’t also compute shading logic. That separation makes everything easier to maintain.

Choose constraints early

Performance limits, platform, libraries, deadlines.

In graphics, that meant using OpenGL-style transforms and simple meshes instead of, say, simulating global illumination.

Sketch / prototype

I block in rough versions first instead of trying to make it perfect the first time. Gray cubes first, polished materials later.

The big point: I don’t just “start coding.” I design a plan that balances visuals, performance, and complexity.

2. What new design skills has your work on the project helped you to craft?

Three big ones:

Scene composition / visual hierarchy
I learned to think in terms of what the viewer’s eye should be drawn to. Light placement, camera angle, and material contrast are design tools, not just technical settings. That’s very close to UI/UX thinking: guide attention on purpose.

Modular system design
I got better at structuring code into reusable components (camera module, lighting module, object/mesh module). That’s core software architecture.

Lighting as a design element
I stopped thinking “a light is just a light” and started thinking “this light creates mood, defines material, communicates time of day.” That’s visual storytelling, and it’s a design skill.

3. What design process did you follow for your project work?

What I followed was basically an iterative design loop:

Concept

Write down or sketch what the world should feel like (e.g. a desk lit by a warm lamp and cooler window light).

Asset planning

List objects I actually need: desk, lamp, mug, etc.

Decide which ones get higher detail and which can stay simple.

Prototype layout

Place low-detail geometry in the scene so I can test proportions, camera framing, and scale.

Lighting pass

Add ambient + directional + point lights and tune brightness/colors until the look matches the concept.

Refinement

Add material properties (shininess, roughness).

Fix weird shadows, fix clipping, adjust camera.

Review against requirements

Check: did I demonstrate diffuse and specular lighting? Are transformations (translate/rotate/scale) applied correctly? Is the camera controllable or at least sensibly placed?

So: plan → block in → light → refine → validate.

That same loop is how professional teams work, just with fancier tools.

4. How could tactics from your design approach be applied in future work?

A few tactics carry forward anywhere in software:

Blocking first, detail later
Start with a working version and then layer in polish. This prevents you from wasting time perfecting something that might get cut.

Modular thinking
When you design each part to have one clear job, you can reuse it in future projects. For example, a camera controller from this project could be reused in any later visualization or game prototype.

Lighting = communication
In non-graphics software, “lighting” is basically “feedback.” You learn to think: how do I guide the user’s focus? In dashboards, that might be contrast or motion instead of literal light, but it’s the same mental habit.

Constant validation against requirements
You don’t wait until the end to ask “does this actually do what it’s supposed to do?” You check during every iteration.

5. How do I approach developing programs?

My development approach now is more disciplined than “code until it runs.”

I follow this cycle:

Break the problem into components

Example: rendering, input, math/transformations, scene data.

Write minimal code for one component at a time

Get the camera working before worrying about glossy reflections.

Test continuously

Run early, run often. If something goes wrong, I know which change caused it because I didn’t batch 20 changes at once.

Refactor as I go

When something starts feeling hacked-together, I stop and clean it into functions/classes so it doesn’t snowball into chaos.

Use iteration instead of “final build” mentality

I assume I’ll improve it, not nail it on the first attempt. That reduces pressure and weirdly makes me faster.

6. What new development strategies did you use while working on your 3D scene?

These were huge:

Transform pipeline discipline
I had to understand and apply model → world → view → projection transformations in the correct order. Before this project, matrices felt abstract. Now they’re practical tools to position objects, aim cameras, and create perspective.

Shading math in code
Instead of just saying “the lamp looks shiny,” I had to implement/specify how specular highlights are calculated (view vector, normal vector, light vector, shininess exponent). That pushed me toward math-driven problem solving.

Incremental builds
I didn’t try to add every object plus final lighting plus camera movement at once. I would add one feature, confirm it worked, then move on.

Debugging visually
I learned to debug with my eyes. If the scene was completely black, that meant maybe normals were wrong or the light intensity was zero. That’s different from normal console debugging and it’s a new kind of intuition.

7. How did iteration factor into your development?

Iteration was basically the backbone.

Visual tuning:
I’d place a light, render, realize it blew out the highlight on the mug, dial it back, move it 10 degrees, render again. That is iteration.

Code cleanup:
Early versions were kind of hardcoded (“put light at (x,y,z)”). Later iterations turned those into variables, structs/classes, and reusable functions.

Performance sanity:
If something tanked performance, I simplified geometry or reduced how many lights contributed to specular. So iteration also kept the scene efficient.

Meeting rubric / requirements:
Each pass got me closer to what the milestone required — not just “cool image,” but “prove I understand ambient vs diffuse vs specular, prove I can transform objects, prove I can manage a scene.” Iteration let me tighten each requirement without rebuilding from scratch.

In short: I didn’t treat the project as a single submission. I treated it as evolving versions.

8. How has your approach to developing code evolved throughout the milestones, which led you to the project’s completion?

Early on:

I was mostly focused on “just make something appear on screen.”

My code was more procedural and very direct (do X, then Y, then Z in one long function).

By the end:

I was thinking in terms of systems and responsibilities.

Camera logic belongs in one place.

Lighting data belongs in another.

Scene objects get their own transforms and materials.

Other evolution points:

I became less afraid of math. Matrices, dot products, normals — all of that turned from scary theory into routine tools.

I started planning changes instead of randomly poking at values.

I built with reuse in mind. Now if I wanted a new scene, I wouldn’t start from zero; I already have pieces.

So, I shifted from “make it work” to “make it structured, explainable, and reusable.”

9. How can computer science help me in reaching my goals?

Computer science gives you leverage.

Problem solving mindset:
You learn how to take something vague (“make it look realistic”) and break it into solvable subproblems (“calculate surface normal,” “define light color,” “compute reflection intensity”). That’s useful in any field.

Automation:
If a task is repetitive, CS lets you script it, visualize it, or simulate it so you don’t waste human time.

Communication power:
You can present ideas in a convincing, data-backed, visual way: dashboards, visualizations, simulations, projections. That matters in school, work, budgeting, even explaining something to leadership.

Career flexibility:
Graphics, data, scripting tools, UI development, testing — these are all marketable niches. Each new skill you stack makes you harder to replace.

10. How do computational graphics and visualizations give you new knowledge and skills that can be applied in your future educational pathway?

In school settings:

Improved spatial reasoning
You learn how objects move and rotate in 3D space. That skill transfers directly to physics classes, engineering-style classes, game development courses, robotics kinematics, etc.

Math confidence
Working with matrices, vectors, normals, lighting equations forces you to actually use linear algebra and geometry. So when those topics show up later in other courses, it’s not abstract anymore — you’ve already used them to make something real.

Scientific communication
Visualizations help explain complex ideas quickly. If you can render or plot it, you can teach it. Being able to illustrate concepts gives you an advantage in presentations, labs, discussions, and capstones.

Project planning / milestone discipline
Graphics projects tend to expose bugs fast and publicly (“wow, the entire scene is purple”). That pressure trains you to iterate, document progress, and defend design decisions — all skills professors expect in upper-level work.

11. How do computational graphics and visualizations give you new knowledge and skills that can be applied in your future professional pathway?

Professionally:

You learn to think in systems
A rendered scene is not one thing — it’s geometry + materials + lighting + camera + math + performance budget. That systems thinking is valuable in software engineering, security, data work, and even operations.

You get better at visual storytelling
Whether you’re showing a 3D prototype, a simulation result, or a dashboard, you’re telling a story with visuals. People in leadership respond to clarity. If you can control where their attention goes, you can influence decisions.

Performance awareness
Graphics teaches you to care about memory usage, frame rate, draw calls — basically, “can this run in real time?” That mindset maps to writing efficient code anywhere (mobile apps, embedded systems, backend services under load).

Reusability and modularity
You practiced building reusable components (camera controller, lighting model, transformation pipeline). Industry wants developers who don’t hardcode everything, but instead build libraries and engines that can be used again.

Communication between technical and non-technical people
You can show a picture or animation instead of making someone read 3 pages of text. That’s a career cheat code.
