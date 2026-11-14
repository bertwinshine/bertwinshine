# Bertwin Kurisinkal Shine

Mechanical engineer working on CFD, FEA and the fast models built on top of them.
M.Sc. Advanced Manufacturing at TU Chemnitz, now at the thesis stage. Based in Chemnitz, Germany.

[Portfolio](https://bertwinkurisinkalshine-portfolio.netlify.app) · [LinkedIn](https://www.linkedin.com/in/bertwin-kurisinkal-shine)

---

### Current work

**CFD reference data for a Czochralski silicon melt.** The second version of the dataset varies crystal rotation, crucible rotation and hot-wall temperature together over a Sobol design: 265 ANSYS Fluent runs, all converged to 1e-6 with a closed heat balance. 254 reached a steady solution; the 11 that did not are listed with the reason. A mesh study (GCI over coarse, base and fine meshes) and 43 hold-out cases come with it. Converging to 1e-6 also showed that some cases in my first dataset, which stopped at Fluent's default 1e-3, only looked steady. The Zenodo release is next.

The first version (33 cases in three one-parameter sweeps) and a POD + RBF surrogate trained on it are still online. The surrogate rebuilds a full velocity, pressure or temperature field in about 0.1 ms.

**Prompt-to-CAD with FreeCAD and MCP.** An MCP server that connects Claude to a running FreeCAD session, plus an engineering knowledge base, so a plain-English brief becomes a checked CAD model. I check the results with hand calculations and ANSYS. A 19-case benchmark compares the assistant with and without the knowledge base. I'm now working on the security side (file access limits, job logging, a safe mode without free code execution) before releasing the source.

### Selected repositories

| Repository | What it is | Key result |
|---|---|---|
| [CZ-Dataset-Doe](https://github.com/bertwinshine/CZ-Dataset-Doe) | 265 Fluent cases over a Sobol design of all three parameters, converged to 1e-6, with mesh study and hold-out set | 254 steady cases kept; base mesh within 1 % of the fine mesh |
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
