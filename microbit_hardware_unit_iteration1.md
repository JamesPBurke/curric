# Micro:bit Hardware Unit, Iteration 1

**Course:** Engineering Design  
**Teacher:** James Patrick Burke  
**Audience:** High school engineering students with basic prior exposure to Micro:bit programming  
**Unit Arc:** From beginner physical computing with simple switches to a functional foam-bodied Micro:bit car  
**Status:** First iteration draft for refinement and expansion

---

## 1. Unit vision

This unit is a hands-on bridge from introductory Micro:bit coding to genuine systems engineering. Students move from writing code that responds to simple physical input, to integrating code, structure, wiring, motion, and fabrication in a final car project. The first project is deliberately constrained and fast: students design a switch from low-cost materials and use it to trigger outputs. The final project is slower and messier in the best way: students design, carve, wire, assemble, and program a foam-bodied vehicle whose movement is controlled by a Micro:bit and servo-based drivetrain.

The instructional idea is simple: **begin with reliable signal flow, then scale to controlled motion, then scale to integrated design.**

---

## 2. Big goals

By the end of the unit, students should be able to:

- explain the function of Micro:bit GPIO pins, power, and ground
- build and troubleshoot a simple input/output hardware circuit
- read and write MakeCode programs that respond to external input
- distinguish between power for logic/control and power for motors
- safely wire and test a servo-controlled mechanism
- design a physical chassis/body that houses electronic components
- iterate on a prototype using evidence from testing
- document engineering decisions and tradeoffs

---

## 3. Unit structure

### Project 1: Switch + signal mini-project
Students create a homemade switch using foil/cardboard or similar conductive-contact materials. The switch controls one or more outputs: the Micro:bit LED matrix, an external LED, or a simple signaling behavior.

**Purpose:**
- establish confidence with pins, circuits, and event-driven logic
- normalize troubleshooting
- create a shared baseline before motion and fabrication complexity arrive

### Project 2: Foam car final
Students design and build a car body from pink foam insulation and integrate a Micro:bit as the controller. A likely first iteration uses yellow continuous-rotation servos for drivetrain motion; blue positional servos may be added if steering is feasible.

**Purpose:**
- integrate mechanics, electronics, fabrication, and code
- emphasize iteration, testing, and constraints
- produce a tangible capstone with visible engineering tradeoffs

---

## 4. Recommended first-iteration design constraints

Because this is the **first full iteration** of the unit, the project should be constrained to preserve sanity.

### Recommended minimum viable final car
Students must produce a car that:
- has a carved foam body or foam chassis/body shell
- securely mounts a Micro:bit
- uses at least one motorized drive system under Micro:bit control
- can move intentionally on the floor
- includes a safe and sensible wiring layout
- includes a brief design log and reflection

### Strong recommendation for Iteration 1
Use **yellow continuous-rotation servos for propulsion** and treat **steering as optional extension work**.

Why:
- it reduces mechanical complexity
- it keeps the build within a realistic school timeline
- it lowers the number of failure points
- it lets students succeed on motion before introducing more advanced steering geometry

### Optional extension
If materials and time allow, advanced groups may:
- add a blue positional servo for steering
- add a bumper switch
- add simple autonomous or semi-autonomous behavior
- complete a timed obstacle/course challenge

---

## 5. Scope and sequence

## Week 1: Launch physical computing and review Micro:bit pins
**Focus:** What changes when code leaves the screen?

**Goals:**
- review Micro:bit basics already learned
- identify P0, P1, P2, 3V, and GND
- understand open/closed circuits and basic signal flow
- begin switch design

**Teacher moves:**
- demo Micro:bit pin usage and show common wiring errors
- model a very simple input → output system
- explicitly teach the difference between signal and power
- establish norms for testing one change at a time

**Student work:**
- annotate a Micro:bit pin diagram
- sketch a switch mechanism
- test conductive materials
- build a first rough switch prototype

**Deliverables:**
- labeled pin reference sheet
- first switch sketch
- prototype notes

---

## Week 2: Build and code the switch project
**Focus:** Reliable input

**Goals:**
- connect a handmade switch to the Micro:bit
- write code that detects the switch state
- trigger a visible output
- troubleshoot unreliable contact

**Student work:**
- construct switch from cardboard, foil, tape, and leads
- connect to GPIO and ground
- create MakeCode program for pressed/not-pressed behavior
- test repeatedly and revise design

**Possible outputs:**
- external LED turns on when switch closes
- matrix icon changes when switch closes
- blinking signal pattern when activated

**Deliverables:**
- functioning switch prototype
- screenshot/export of MakeCode program
- quick troubleshooting log

---

## Week 3: Refine switch and introduce engineering quality criteria
**Focus:** Stability, usability, and evidence

**Goals:**
- improve switch durability and reliability
- compare designs using criteria
- prepare students for design constraints in the car project

**Quality criteria for the switch:**
- activates consistently
- does not short accidentally
- survives repeated use
- is understandable to another user
- has reasonably neat wiring

**Student work:**
- run repeated trials
- revise design based on failures
- present switch and explain how it works

**Deliverables:**
- revised switch
- peer feedback form
- short reflection: what made the design more reliable?

---

## Week 4: Introduce the foam car project and plan the build
**Focus:** Systems design before carving

**Goals:**
- define the final car challenge
- identify required subsystems
- draft body/chassis plans before cutting foam

**Subsystems to teach explicitly:**
- controller (Micro:bit)
- drivetrain (servo(s), wheels, axle method)
- structure (foam body/chassis)
- power (battery pack, servo power, shared ground)
- code (movement logic)

**Student work:**
- analyze sample builds and constraints
- sketch top/side views of car
- decide where components will mount
- estimate dimensions and carve plan

**Deliverables:**
- car design sheet
- component layout sketch
- bill of materials per team

---

## Week 5: Servo control and safe power
**Focus:** Make things move without frying the board

**Goals:**
- understand positional vs continuous servos
- learn safe servo wiring
- test servo control with the Micro:bit before full assembly

**Critical safety idea:**
Do **not** assume servos should be powered from the Micro:bit directly in classroom builds. A separate battery supply for servos is the safer default, with **common ground** shared between the Micro:bit and motor power system.

**Student work:**
- identify servo type
- wire one servo safely
- test movement code in MakeCode
- calibrate stop/forward/reverse behavior for continuous servos

**Deliverables:**
- working servo test rig
- short wiring diagram
- calibration notes

---

## Week 6: Car fabrication and mechanical assembly
**Focus:** Build the body and mount components

**Goals:**
- glue and carve pink foam insulation into workable car bodies
- mount wheels, servo(s), battery pack, and Micro:bit
- revise structure to reduce wobble and wiring strain

**Student work:**
- cut, glue, measure, and carve foam
- create openings/channels for wiring and hardware
- mount drivetrain and test basic rolling motion
- iterate on body shape without sacrificing function

**Deliverables:**
- carved body/chassis
- mounted components
- first rolling/mechanical test

---

## Week 7: Integration and test cycles
**Focus:** Whole system debugging

**Goals:**
- combine code, structure, and wiring into a working car
- identify failures systematically
- document changes based on evidence

**Debugging categories to use with students:**
- code problem
- wiring problem
- power problem
- mechanical friction/alignment problem
- body design problem

**Student work:**
- run floor tests
- record failures and fixes
- tune motion and reliability
- prepare a simple showcase/demo

**Deliverables:**
- testing log
- revised code
- functioning car or documented partial prototype

---

## Week 8: Showcase, reflection, and revision
**Focus:** Demonstration and engineering reasoning

**Goals:**
- demonstrate car performance
- explain design decisions and tradeoffs
- reflect on what made systems succeed or fail

**Possible showcase formats:**
- straight-line challenge
- short obstacle path
- design expo with demo stations
- judged categories: reliability, craftsmanship, iteration, creativity

**Deliverables:**
- final car demonstration
- engineering reflection
- design portfolio or slide summary

---

## 6. Suggested daily lesson arc for most build days

1. **Do Now / retrieval** — one short question about pins, wiring, code, or design tradeoffs  
2. **Mini lesson / demo** — 8 to 15 minutes  
3. **Guided build/test window**  
4. **Checkpoint conference** with teacher  
5. **Exit ticket** documenting progress, failures, and next step

This keeps the unit from dissolving into unstructured tool time, which, while popular, is often educationally thin. Irrelevant excitement is not progress.

---

## 7. Equipment and materials list

## Core electronics per team
- 1 Micro:bit
- USB cable for programming
- battery pack for Micro:bit
- crocodile/alligator clip leads and/or jumper wires
- breakout board or edge-connector adapter if available
- breadboard (recommended)
- LEDs
- resistors for LED circuits
- electrical tape or masking tape

## Switch project materials
- cardboard
- aluminum foil
- scissors
- glue or tape
- paper fasteners / brads (optional)
- binder clips or clothespins (optional for mechanism experiments)

## Car project materials
- pink foam insulation board or blocks
- hot glue or foam-safe adhesive
- craft knives / foam cutters under appropriate safety procedures
- rulers and measuring tools
- skewers, dowels, rods, or axle material
- wheels (pre-made, 3D printed, repurposed, or kit-based)
- servo horns and mounting screws if included
- zip ties, rubber bands, tape, or brackets for mounting

## Motors and power
- yellow continuous-rotation servos (recommended base build)
- blue positional servos (optional extension or steering)
- separate battery pack for servos/motor system
- spare batteries

## Classroom support items
- labeled bins for hardware
- backup Micro:bits and leads
- printed wiring references
- troubleshooting checklists
- charging/storage routine

---

## 8. Instructional risks and mitigation

### Risk 1: Students destroy momentum because hardware is unreliable
**Mitigation:**
- begin with a tiny successful circuit
- require testing in stages
- provide known-good demo rigs
- keep a few teacher-validated parts on hand

### Risk 2: Servo power/wiring confusion causes frustration or damage
**Mitigation:**
- teach a single standard wiring pattern
- insist on common ground explanation
- explicitly prohibit unsafe power shortcuts
- use color-coded diagrams

### Risk 3: Car body fabrication consumes all the time
**Mitigation:**
- constrain size
- provide design templates or dimensional caps
- require a planning sketch before cutting
- allow “functional ugly first, aesthetic better later” as a build norm

### Risk 4: Some teams stall in open-endedness
**Mitigation:**
- offer checkpoint deadlines
- provide a minimum viable build target
- maintain extension tiers for faster groups

---

## 9. Assessment model

## Formative assessment
- pin identification checks
- code reviews
- wiring conferences
- test logs
- exit tickets
- peer critique

## Summative assessment categories
Suggested rubric categories:
- **Functionality** — does the switch/car work reliably?
- **Engineering process** — evidence of iteration and troubleshooting
- **Code quality** — logic, readability, appropriate use of inputs/outputs
- **Build quality** — structure, wiring management, mounting, craftsmanship
- **Explanation/reflection** — can students explain why their system works or fails?

## Suggested weighting
- Switch mini-project: 20–25%
- Car final build: 45–55%
- Design notebook / log / reflection: 20–25%

---

## 10. Recommended teacher-created support documents

To make this unit truly runnable, the following should be created next:

1. detailed lesson plans by day  
2. student-facing project sheets  
3. materials checklist by team  
4. wiring diagrams  
5. troubleshooting guide  
6. MakeCode starter examples  
7. car design planning worksheet  
8. rubric set for switch and car  
9. slide deck outline for each week  
10. parent/admin-safe summary of the final project

---

## 11. External resources worth using in Iteration 1

These are promising references for teacher prep and student support.

### Official / high-value references
- **Micro:bit pins overview**: https://makecode.microbit.org/device/pins  
  Useful for teaching P0/P1/P2, 3V, GND, and GPIO basics.

- **MakeCode servo reference**: https://makecode.microbit.org/reference/servos  
  Useful for showing servo functions such as set angle, run, stop, and pulse behavior.

- **Micro:bit support article on using a servo**: https://support.microbit.org/support/solutions/articles/19000101864-using-a-servo-with-the-micro-bit  
  Particularly valuable for the warning about servo power requirements, separate power, and common ground.

### Switch / physical computing examples
- **Simple switch example**: https://sites.google.com/holmdelschools.org/rokeefestechhub/tech-resources/microbit/sensors/simple-switch  
  Teacher-facing example using cardboard/foil switch construction.

- **Teach Computing / Raspberry Pi physical computing connections lessons**:  
  https://teachcomputing.org/curriculum/key-stage-4/physical-computing/connections  
  Useful as a conceptual lesson reference for GPIO, LEDs, and switches.

### Video resources to vet for classroom use
These appear relevant, though they should be previewed before assigning to students.
- **Programming a Servo with the micro:bit and MakeCode**  
  https://www.youtube.com/watch?v=ijRBim2ydFs4
- **Behind the MakeCode Hardware - Servo Motors with micro:bit**  
  https://www.youtube.com/watch?v=okxooamdAP4
- **Control a Servo - BBC micro:bit Code in 60 Seconds**  
  https://www.youtube.com/watch?v=2wTInw8uhCQ
- **PLTW CSIM 2.2 - Using a Continuous Servo with your Micro:bit**  
  https://www.youtube.com/watch?v=SEZffxJDn9U

### Important note on resource use
For student-facing use, prefer:
- official Micro:bit resources
- short videos under 5 minutes for just-in-time troubleshooting
- teacher-vetted examples instead of sending students into random search chaos

---

## 12. Recommended next deliverables for a fully built curriculum package

The most valuable next documents to produce are:

1. **unit overview handout** for students  
2. **full scope-and-sequence calendar** by class meeting  
3. **switch project guide** with materials, steps, photos, and code starter  
4. **servo lab** for safe wiring and calibration  
5. **foam car project guide** with milestones  
6. **teacher troubleshooting guide**  
7. **rubrics**  
8. **slide deck content outline**

---

## 13. Recommendation to James

For Iteration 1, do **not** try to build the perfect robotics curriculum in one pass. Build the first version around:
- one reliable switch task
- one reliable servo lab
- one constrained car build
- heavy use of troubleshooting logs and checkpoints

That will give you usable classroom reality instead of theoretical elegance. The latter is seductive. The former survives June.
