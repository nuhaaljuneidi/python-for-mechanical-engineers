# Session 1 Teaching Guide

## Python Foundations for Engineering Calculations

**Audience:** Mixed undergraduate and graduate students  
**Duration:** 2.5–3 hours  
**Mode:** Live coding + guided practice + engineering challenge

## Learning outcomes

By the end of the session, students can:

1. Use variables, operators, and formatted output in an engineering calculation.
2. Distinguish scalars from arrays and select an appropriate data structure.
3. Write reusable functions with units documented.
4. Apply conditional logic to check whether a result is physically meaningful.
5. Solve introductory thermal and fluid-system calculations in Python.
6. Communicate a result with its value, unit, assumptions, and validity check.

## Suggested timing

| Time | Activity |
|---|---|
| 0:00–0:15 | Colab orientation and the engineering-computation workflow |
| 0:15–0:40 | Variables, units, arithmetic, and formatted output |
| 0:40–1:05 | Example 1: heating water and checking energy units |
| 1:05–1:25 | Functions and input validation |
| 1:25–1:35 | Break |
| 1:35–2:00 | Example 2: Reynolds number and flow regime |
| 2:00–2:25 | Example 3: thermal resistance network |
| 2:25–2:50 | Student design challenge |
| 2:50–3:00 | Exit ticket and preview of Session 2 |

## Teaching strategy for a mixed cohort

- All students complete the core cells.
- Undergraduate beginners use the hints in the notebook.
- Students with prior coding experience complete the **Graduate/Advanced Extension** cells.
- Pair students by engineering reasoning, not only programming experience.
- Require every reported result to include a unit and one physical reasonableness statement.

## Formative assessment

- Checkpoint 1: Correct energy calculation and conversion to kWh.
- Checkpoint 2: A function that returns both Reynolds number and flow regime.
- Checkpoint 3: Correct overall heat-transfer coefficient from series resistances.
- Exit ticket: Explain one advantage of a function over copying an equation.

## Instructor preparation

1. Open both notebooks in Colab before class.
2. Run **Runtime → Run all** in the solution notebook.
3. Keep the solution notebook private until students submit the challenge.
4. Ask students to save a copy to their own Google Drive.

## Common misconceptions

- Treating °C as K in expressions involving absolute temperature.
- Mixing J and kJ or W and kW.
- Assuming Python automatically understands units.
- Using `^` for exponentiation instead of `**`.
- Reporting a numerical answer without checking magnitude or assumptions.

## Exit ticket prompt

In three sentences: state one calculation you automated, one error check you added, and one mechanical-engineering problem you would like to solve with Python.
