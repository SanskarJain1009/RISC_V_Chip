# Day 5: Optimization in synthesis
It included-

1. If-Case constructs-
    
    The danger/caution with 'if' construct is the incompleteness and poor coding style which results in to the Inferred Latch, which is if not desired is considered bad. 
    This Inferred Latch is sometime desired, for eg. in a design of counter. 

    The danger/caution with 'case' construct also results in to the Inferred Latch, which is if not desired considered bad. To avoid this, code 'case' with default. 
    Writing default does not mean that you won't get any latch, if there is partial assignment done, then it is still possible to get latches. To avoid this, assign all the outputs in all the segments of case. And one more caveat: there shouldn't be any overlapping case.
    
2. Labs on "Incomplete If Case"-
    The incomp_if.v design is used to demonstrate the incomplete if statement. Although it is a mux design but it is realized in D-Flip Flop (inferred as latch because of incompleteness). The simulated waveform and synthesized netlist is attached below.
     ![incomp_if_wave](/week_1/day_5/img/Labs_On_Incomplete_if_case/incomp_if_wave.png)
     ![synthesized_incomp_if](/week_1/day_5/img/Labs_On_Incomplete_if_case/synthesized_incomp_if.png)
     
     The design incomp_if2.v is also taken as example to demonstrate the incompleteness. This design containes if and else if statement but not the else statement. The simulated waveform and synthesized netlist is attached below. This design is also incomplete and result in an inferred latch situation.
     ![incomp_if2_wave](/week_1/day_5/img/Labs_On_Incomplete_if_case/incomp_if2_wave.png)
     ![synthesized_incomp_if2](/week_1/day_5/img/Labs_On_Incomplete_if_case/synthesized_incomp_if2.png)
     
3. Labs on "Incomplete overlapping Case"-
    For this lab, we used 4 designs comp_case.v, incomp_case.v, partial_case_assign.v and bad_case.v, the simulated wave and synthesized designs for each of them is attached below respectively. There were few erros in the tb_partial_case_assign.v file, I made the required changes and attached the correct tb_partial_case_assign.v also.
    
    comp_case.v- In this design, there is no latch inferred as it is a complete design with good coding style.
    
    ![comp_case_wave](/week_1/day_5/img/Labs_on_Incomplete_overlapping_Case/comp_case_wave.png)
    ![synthesized_comp_case](/week_1/day_5/img/Labs_on_Incomplete_overlapping_Case/synthesized_comp_case.png)
    
    incomp_case.v- In this design, there is latch inferred. 
    
    ![incomp_case_wave](/week_1/day_5/img/Labs_on_Incomplete_overlapping_Case/incomp_case_wave.png)
    ![synthesized_incomp_case](/week_1/day_5/img/Labs_on_Incomplete_overlapping_Case/synthesized_incomp_case.png)
    
    partial_case_assign.v-
    
    ![partial_case_assign_wave](/week_1/day_5/img/Labs_on_Incomplete_overlapping_Case/partial_case_assign_wave.png)
    ![synthesized_partial_case_assign](/week_1/day_5/img/Labs_on_Incomplete_overlapping_Case/synthesized_partial_case_assign.png)
    
    bad_case.v-
    
    ![bad_case_wave](/week_1/day_5/img/Labs_on_Incomplete_overlapping_Case/bad_case_wave.png)
    ![synthesized_bad_case](/week_1/day_5/img/Labs_on_Incomplete_overlapping_Case/synthesized_bad_case.png)
    
    There is synthesis simulation mismatch in this design.

4. for loop and for generate-
        Verilog includes, for loop and generate construct. 'for loop' is used inside the always block and the 'generate' is used outside the always block. 'generate' is used to instantiate the hardware. 
        Inside for loop, blocking assignment use becomes most meaningful. 

5. Labs on "for loop" and "for generate"


