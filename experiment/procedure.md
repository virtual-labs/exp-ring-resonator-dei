## Procedure

1. Click the **Concept** tab to read the basic theory of the ring resonator and its comparison with the linear λ/2 resonator.
2. Click the **Theory** tab to note down the resonant frequency, Q-factor, and equivalent circuit formulas.
3. Click the **Why 50 Ω?** tab (optional) to understand why 50 Ω is used as the standard reference impedance.
4. select the **Design & Simulation** tab. The **Design Parameters** panel appears on the left, and the **Simulation** panel appears on the right. The graphs initially contain placeholders; they are generated only when **Run S-Parameters** is clicked.
  
5. **Set the design parameters.** Enter or retain the default values in the **Input parameters** section. 
   Use the available material presets, if needed. Ensure that the entered values are valid; the simulator highlights invalid inputs and disables the Run button until they are corrected.

6. **Observe the live design results.** Examine the **Calculated parameters** and **Performance** tiles. Note the ideal fundamental frequency **f₁**, coupled resonant frequency **fres**, characteristic impedance **Z₀**, gap capacitance **Cgap**, unloaded quality factor **Qu**, external quality factor **Qext**, loaded quality factor **QL**, bandwidth **BW** and insertion loss. These estimates update when the design inputs change.

7. **Inspect the ring geometry.** In the right panel, select **Live Geometry**. Observe the top view of the ring, substrate, feed lines and coupling gaps. Change one design parameter, such as **R** or **g**, and examine the resulting geometry and calculated values. Restore the intended design before proceeding.

8. **Choose a frequency sweep.** The default sweep is **0.5 to 6 GHz** with **201 points**. To examine the fundamental resonance more clearly, click **Focus on Resonance**. This automatically sets the start and stop frequencies around the current **fres** (approximately **±5 bandwidths**) and uses sufficient sampling for a detailed view. *This button changes the sweep settings but does not run the simulation.*

9. **Run the simulation.** Click **Run S-Parameters**. After the run completes, study the generated **S₂₁ / S₁₁ Magnitude** and **S₁₁ Phase** graphs. Identify the resonance near **fres**, read the resonance marker, and observe the shaded analytical **−3 dB bandwidth** region. Use the **dB / VSWR** switch to inspect the VSWR plot. If any design input or sweep setting is modified, click **Run S-Parameters** again to refresh the graphs.

10. **Examine additional response plots.** Scroll down to view the **Smith Chart**, **Group Delay (of S₂₁)**, and **|V(z)| Standing Wave at resonance** plots. Observe the frequency-dependent reflection response, the group-delay peak near resonance, and the standing-wave distribution of the fundamental (**n = 1**) mode.

11. **Explore the field distribution.** Return to the simulation panel and select **Field Distribution**. Use **Electric field (E)** and **Magnetic field (H)** to compare the two qualitative visualizations. Move the operating-frequency slider from below **fres**, through **fres**, to above **fres**, and observe the changes in field amplitude and phase. Click **Play** to animate one RF cycle; use **Pause**, **Speed**, **Field vectors**, **Field intensity**, and **Reset** as required. Also observe the cross-section and phase/stored-energy displays.

12. **Inspect the equivalent circuit.** Select **Equivalent Circuit**. Identify the two coupling capacitors and the parallel **R–L–C** resonator model. Compare the displayed **Cgap**, **Rp**, **Leq**, **Ceq**, **f₁** and **fres** values with the calculated results.

13. **Record the results.** Return to the completed plots and the **Results Summary**. Record the required quantities in an observation table. Repeat the simulation after changing **one parameter at a time** (for example, radius, coupling gap or substrate permittivity), using **Focus on Resonance** and **Run S-Parameters** for each new design. Compare how resonance frequency, coupling, loaded Q, bandwidth and insertion loss change. Use **Reset** in the Design Parameters panel to restore the original design.

## Observation Table

| Trial | R (mm) | g (mm) | εr | f₁ (GHz) | fres (GHz) | Z₀ (Ω) | QL | BW (MHz) | Insertion loss (dB) |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 1 — Default design | | | | | | | | | |
| 2 — Changed radius | | | | | | | | | |
| 3 — Changed gap | | | | | | | | | |
| 4 — Changed permittivity | | | | | | | | | |

## Notes for Students

- **f₁** is the ideal/unperturbed fundamental ring resonance; **fres** is the resonance estimated with coupling-gap loading. The two values need not be equal.
- Use **Focus on Resonance** before running when the default frequency sweep gives a narrow, poorly sampled peak.
- Changing a parameter updates the live design quantities, **not** the previously generated graphs. Press **Run S-Parameters** again after every change.
- The plotted S-parameter response models the **fundamental n = 1 resonance only**. Higher resonances are not simulated.
- The field views are **qualitative illustrations**, and the circuit and coupling results are **analytical estimates**. This virtual simulation is intended for learning, not for full-wave electromagnetic validation or production design.
