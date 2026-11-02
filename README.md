# PLC Set and Reset Operation

## Project Overview

This project demonstrates the **Set and Reset (S/R) operation** in Programmable Logic Controller (PLC) ladder logic. It is a beginner-level PLC simulation project created to understand how an output can be latched ON by a Set instruction and switched OFF by a Reset instruction.

## Objective

- Understand Set (S) and Reset (R) instructions in ladder logic.
- Practise assigning PLC input and output variables.
- Observe how a latched output behaves in a simulator.
- Build a foundation for motor control and other industrial automation sequences.

## Ladder Logic

The program contains two rungs:

1. **Set rung:** `Start_Button` is used as the condition for the Set (`S`) instruction.
2. **Reset rung:** `Reset_Button` is used as the condition for the Reset (`R`) instruction.

Conceptually:

```text
Rung 1:  --[ Start_Button ]----------------(S) Output

Rung 2:  --[ Reset_Button ]----------------(R) Output
```

The exact variable mapping and instruction behavior depend on the PLC software and project configuration.

## How It Works

1. Start the PLC simulator and connect the debugger.
2. Activate `Start_Button`.
3. The Set instruction sets the output state to ON.
4. Release `Start_Button`; the output should remain ON if the simulator's Set instruction is retentive.
5. Activate `Reset_Button`.
6. The Reset instruction clears the output state to OFF.

**Important:** If both commands are active at the same time, the result can depend on the PLC's instruction semantics and rung execution order. Test this condition in the simulator before using the logic in a real system.

## Tools and Environment

- PLC ladder-logic editor and simulator (as shown in the project screenshot)
- Ladder Diagram (LD)
- Online debugging / variable monitoring

> Add the exact software name and version here if you want the project environment documented precisely.

## Testing Checklist

- [ ] Simulator starts and the debugger connects.
- [ ] Activating `Start_Button` sets the output ON.
- [ ] Releasing `Start_Button` leaves the output ON.
- [ ] Activating `Reset_Button` clears the output.
- [ ] Test simultaneous Set and Reset commands.
- [ ] Confirm the output's initial state after restarting the simulator.

## What I Learned

- How Set and Reset instructions differ from ordinary output-coil logic.
- How a PLC can retain an output state after the initiating condition is released.
- How to monitor program execution using a simulator and debugger.
- How to structure a simple ladder-logic project for later automation exercises.

## Possible Improvements

- Add a status indicator for the output.
- Add an interlock so Set and Reset commands cannot conflict.
- Extend the project to a motor Start/Stop circuit.
- Add emergency-stop and overload conditions in a properly designed, safety-aware example.
- Include screenshots or a short recording showing the ON and OFF states.

## Safety Note

This is an educational simulation. A real machine or motor circuit needs a suitable risk assessment, correctly selected hardware, and appropriate safety-rated devices. Standard PLC logic alone should not be treated as a substitute for a safety circuit.

## Project Screenshot

Add your screenshot to the repository (for example, in a folder named `images`) and update the path below:

```markdown
![PLC Set and Reset ladder logic](images/set-reset-ladder.png)
```

## Author

**Rahaman Sheikh**

Beginner PLC and industrial automation learning project.
