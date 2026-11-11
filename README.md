# Bertwin Kurisinkal Shine

Mechanical engineer working on CFD, FEA and the fast models built on top of them.
M.Sc. Advanced Manufacturing at TU Chemnitz, now at the thesis stage. Based in Chemnitz, Germany.

[Portfolio](https://bertwinkurisinkalshine-portfolio.netlify.app) · [LinkedIn](https://www.linkedin.com/in/bertwin-kurisinkal-shine)

---

### Current work

Reference CFD data and a reduced-order model for a Czochralski silicon melt.
I ran 33 cases in ANSYS Fluent across three parameter sweeps. Each case had to pass a check against its own boundary conditions before it went into the dataset. A POD + RBF surrogate trained on these cases rebuilds a full velocity, pressure or temperature field in about 0.1 ms.

### Selected repositories

| Repository | What it is | Key result |
|---|---|---|
| [CZ_Surrogate_App](https://github.com/bertwinshine/CZ_Surrogate_App) | POD + RBF surrogate of the CZ melt, as a Streamlit app | ~0.1 ms per field; leave-one-out error below 2 % of field range |
| [CZ_Silicon_Melt_CFD_Dataset](https://github.com/bertwinshine/CZ_Silicon_Melt_CFD_Dataset) | 33 Fluent cases on one 8181-node mesh, three sweeps | Meridional flow reverses between 6 and 7 rpm crystal rotation |
| [freecad-mcp-showcase](https://github.com/bertwinshine/freecad-mcp-showcase) | MCP server that lets Claude build parts live in FreeCAD | Gears and printed boats, checked by hand calculation and ANSYS |
| [ansys-cylinder-validated](https://github.com/bertwinshine/ansys-cylinder-validated) | Thick-walled pressure vessel in ANSYS, compared with the Lamé solution | 0.05 % mean stress error |

### CAD and simulation projects

These are written up on the [portfolio](https://bertwinkurisinkalshine-portfolio.netlify.app) with models, results and videos:

- **HELIOS-25 planetary gearbox:** coaxial e-axle reducer, 24.84:1, 30,000 rpm input, with bearing life analysis (SolidWorks 2025)
- **EV battery bracket:** AlSi10Mg die-cast bracket; static, modal, random vibration and fatigue analysis; about 51 % lighter after topology optimisation
- **Serpentine cold plate:** 2.8 kW power-electronics module in ANSYS Fluent, four operating points
- **Battery module CHT:** 8-cell cylindrical pack with a cold plate, conjugate heat transfer
- **E-machine stator and rotor dynamics:** modal, harmonic response with eccentricity, Campbell diagram (ANSYS)

### Tools

**Simulation:** ANSYS Fluent, ANSYS Mechanical
**CAD:** SolidWorks (CSWA), PTC Creo, Siemens NX, Fusion 360, FreeCAD
**Code:** Python for pre- and post-processing and reduced-order models (NumPy, pandas, SciPy, Streamlit)

### How I work

Before I trust a simulation result, I check it against something independent: an analytical solution, a finer mesh, or a mass and energy balance. Each repo says what was checked and where the model stops working. Where AI tools helped write the code, the README says so.

<details>
<summary>Education</summary>

- **M.Sc. Advanced Manufacturing**, Technische Universität Chemnitz, since 2023
- **B.Sc. Mechanical Engineering**, Riga Technical University, Latvia

</details>

Open to Master's thesis positions and simulation engineering roles in Germany.
