# Day 4: GLS, blocking vs non-blocking and Synthesis-Simulation mismatch
It included-
1. GLS, Synthesis-Simulation mismatch and Blocking/Non-blocking statements-
    Introduction is given about Gate Level Synthesis (GLS) and it's necessity. In these introduction videos, only the functionally aware Gate Level Verilog Models are discussed and not Timing Aware. The below displayed image gives the glimpse of introductory session for GLS. 
    ![GLS_Concept_And_Flow](/week_1/day_4/img/GLS_Synthesis_Simulation_mismatch_and_Blocking_Non_blocking_statements/GLSConceptsAndFlowUsingIverilog.png)
    
    The reason for doing the functional aware GLS is because of Synthesis Simulation Mismatch.
    The following can be the reasons for Synthesis Simulation Mismatch-
    i. Missing Sensitivity List.
    ii. Blocking vs Non-Blocking Assignment.
    iii. Non-standard Verilog Coding. 

2. Labs on GLS and Synthesis-Simulation Mismatch-
    First, the GLS is shown using the example ternary_operator_mux.v design. The rtl simulated result, then the generated netlist design and the GLS result is attached below respectively and the .vcd file along with the generated netlist verilog design is also attached in the day_4 folder.
    ![ternary_operator_mux_wave](/week_1/day_4/img/Labs_on_GLS_and_Synthesis_Simulation_Mismatch/ternary_operator_mux_wave.png)
    ![synthesized_ternary_operator_mux_wave](/week_1/day_4/img/Labs_on_GLS_and_Synthesis_Simulation_Mismatch/synthesized_ternary_operator_mux.png)
    ![gls_synthesized_ternary_operator_mux](/week_1/day_4/img/Labs_on_GLS_and_Synthesis_Simulation_Mismatch/GLS_synthesized_ternary_operator_mux.png)
    
    Then, the bad_mux.v is taken is example. There is synthesis simulation mismatch in this bad_mux.v design.The simulated wave, generated netlist and GLS are attached below.
    ![bad_mux_wave](/week_1/day_4/img/Labs_on_GLS_and_Synthesis_Simulation_Mismatch/bad_mux_wave.png)
    ![synthesized_bad_mux](/week_1/day_4/img/Labs_on_GLS_and_Synthesis_Simulation_Mismatch/synthesized_bad_mux.png)
    ![synthesized_bad_mux](/week_1/day_4/img/Labs_on_GLS_and_Synthesis_Simulation_Mismatch/GLS_bad_mux_wave.png)
    
3. Labs on synth-sim mismatch for blocking statement-
    The aim is to create the logic :   (A|B)&C    : The intermediate point is 'x' here.
    The blocking_cavet.v design is taken as example. In this design 'x' will act as a flopped output in simulation. 
    It is found that due to blocking assignment there is synthesis simulation mismatch in the design. The generated wave for simulation, the synthesized netlist and the GLS wave is attached below. 
    ![bad_mux_wave](/week_1/day_4/img/Labs_on_synth_sim_mismatch_for_blocking_statement/blocking_cavet_wave.png)
    ![synthesized_bad_mux](/week_1/day_4/img/Labs_on_synth_sim_mismatch_for_blocking_statement/synthesized_blocking_caveat.png)
    ![synthesized_bad_mux](/week_1/day_4/img/Labs_on_synth_sim_mismatch_for_blocking_statement/GLS_blocking_caveat_wave.png)
     
