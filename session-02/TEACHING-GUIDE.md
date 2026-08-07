# Session 2 Teaching Guide

## Theme

Arrays and engineering visualization through a one-dimensional straight-fin model.

## Duration

90 minutes.

## Learning objectives

Students will be able to create NumPy arrays, perform vectorized calculations, visualize several engineering cases, apply professional figure conventions, and support a design statement with plotted evidence.

## Suggested flow

| Time | Activity |
|---:|---|
| 0–10 min | Reconnect Session 1 functions to array-based calculations |
| 10–25 min | Build arrays and inspect shape, size, indexing, and units |
| 25–40 min | Vectorize the analytical fin-temperature equation |
| 40–55 min | Create and improve a single engineering plot |
| 55–70 min | Run a convection-coefficient parameter sweep |
| 70–82 min | Produce and export the final publication-ready figure |
| 82–90 min | Interpret results and complete the exit ticket |

## Model used

For an adiabatic-tip straight rectangular fin,

\[
T(x)=T_\infty+(T_b-T_\infty)\frac{\cosh[m(L-x)]}{\cosh(mL)},
\qquad
m=\sqrt{\frac{hP}{kA_c}}.
\]

Default values: length 0.10 m, width 0.025 m, thickness 0.002 m, conductivity 205 W/(m·K), base temperature 100 °C, ambient temperature 25 °C, and convection coefficient 25 W/(m²·K).

## Teaching prompts

- What does the array shape tell us physically?
- Why is vectorization a better fit than evaluating one position at a time?
- Which plot elements carry engineering meaning rather than visual decoration?
- What happens to the temperature profile when `h` increases, and why?
- Can a beautiful figure still communicate a physically misleading result?

## Common difficulties

- Mixing millimeters and meters.
- Using `math.cosh` instead of `numpy.cosh` for arrays.
- Omitting units from axis labels.
- Comparing cases without a legend or without holding other parameters constant.
- Claiming that a larger temperature means better performance without defining the performance objective.

## Assessment

The completed figure should include multiple `h` cases, readable line styles, labeled axes with units, a legend, a light grid, constrained layout, and a 300-dpi export. The written conclusion should connect the curve behavior to increased convection from the fin.

## Extension

Ask advanced students to calculate fin efficiency or compare aluminum with steel while keeping geometry and boundary conditions fixed.
