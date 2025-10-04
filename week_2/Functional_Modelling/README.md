# Functional_Modelling

Practice functional modelling of the BabySoC using simulation tools (Icarus Verilog & GTKWave). 

### Part 2 – Labs (Hands-on Functional Modelling) 

After following the instructions provided in the PDF (cloning, compiling, simulate and generate .vcd waveform files), the obtained `pre_synth_sim.vcd` file is attached. The simulated waveform is also attached.

![pre_synth_sim](/week_2/Functional_Modelling/img/pre_synth_sim_1.png)

### Signals in the Simulation

- **CLK**:
  - Input clock signal of the `RVMYTH` core.
  - Originally comes from the PLL.

- **reset**:
  - Input reset signal of the `RVMYTH` core.
  - Originally comes from an external source.

- **RV_TO_DAC[9:0]**:
  - 10-bit output port `[9:0]` of the `RVMYTH` core.
  - Derived from `RVMYTH` register #17.

- **OUT (real datatype)**:
  - Output wire of type `real` from the DAC module.
  - Can simulate analog values.
  - Originally comes from the DAC.

- **OUT**:
  - Output signal of the `VSDBabySoC` module.
  - Comes from the DAC.
  - Due to simulation restrictions, it behaves like a digital signal (not the correct analog behavior).

![pre_synth_sim](/week_2/Functional_Modelling/img/pre_synth_sim_2.png)

In the image shown above, the signals are the same. The only difference is the OUT in the last, which is the output of the `VSDBabySoC` but it is shown as an analog step wave.
