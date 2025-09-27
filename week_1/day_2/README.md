# Day 2: 
It included-
1. Introduction to timing .libs:
    This gave the introductory sessions on .lib file. Functioning and grasping the idea and understanding for liberty file is showcased. PVT (Process, Voltage and Temperature) parameters are also explained. The 'and_or' and 'and' cells are used to demonstrated to showcase the idea of naming and how the the different size affects PVT parameters.
    
2. Hierarchical vs Flat Synthesis:
    From the verilog_files, multiple_modules.v is chosen as example. 
    Note- Stacked PMOS is bad, as it has poor mobility and achieving the required logic speed large area pmos is required. 
    synth -top for submodules is explained. For simplicity, when same submodule is instantiated multiple times and for the divide and conquer apporach (synthesizing the submodules to their best designs and moving forward by stitching these modules together to the completion of whole design).
    I tried using both options hierarchy and flatten option but the output displayed using show command is same. Although this is the case but I got what's the difference and need for both of them.
    ![multiple_modules](/week_1/day_2/img/Introduction_to_timing_lib/multiple_modules.png)
    ![multiple_modules_flatten](/week_1/day_2/img/Introduction_to_timing_lib/multiple_modules_flatten.png)
    ![sub_module1](/week_1/day_2/img/Introduction_to_timing_lib/sub_module1.png)
    
3. Various Flop Coding Styles and optimization:
    Flip flops are needed to avoid glitches. Sync and Async flip flop styles is explained thoroughly with the example of sync, async and sync-async reset and set.
    The iverilog is used to simulate the design for the example taken are dff_asyncres.v, dff_asyncset.v dff_syncres.v.
    The respective output wave simulation is as follows:
    ![asyncres](/week_1/day_2/img/Various_Flop_Coding_Styles_and_Optimization/dff_asyncres.png)
    ![asyncset](/week_1/day_2/img/Various_Flop_Coding_Styles_and_Optimization/dff_asyncset.png)
    ![syncres](/week_1/day_2/img/Various_Flop_Coding_Styles_and_Optimization/dff_syncres.png)
    
    The previously dff designs mentioned are than synthesized, the design obtained was slightly different but the boolean logic is same as intended. 
    The designs obtained are as follows:
    ![synthesized_asyncres](/week_1/day_2/img/Various_Flop_Coding_Styles_and_Optimization/synthesized_dff_asyncres.png)
    ![synthesized_asyncset](/week_1/day_2/img/Various_Flop_Coding_Styles_and_Optimization/synthesized_dff_async_set.png)
    ![synthesized_syncres](/week_1/day_2/img/Various_Flop_Coding_Styles_and_Optimization/synthesized_dff_syncres.png)

    Optimisations are done and demonstrated using the example mult_2.v (multiplication of 3 bit input by 2) ad mult_8.v (multiplication of a 3 bit input by 9) verilog designs.
    With mult_2.v, it was found that it is a special case as it doesn't require any hardware. In this case, keeping the signal same and appending an extra by ground is sufficient to realise the design, i,e. it does not require abc command in yosys, wires are sufficient for it's design. 
    ![synthesized_mul2](/week_1/day_2/img/Various_Flop_Coding_Styles_and_Optimization/synthesized_mul2.png)
    ![abc_liberty_command_output_mul2](/week_1/day_2/img/Various_Flop_Coding_Styles_and_Optimization/abc_liberty_command_output_mul2.png)
    
    The output becomes input 'a' concatenated with 0.
    
    With mult_8.v, it is also a special case. It is synthesized and the output is concatenation of input 'a' with itself. This special case is due to the input bit size, i.e, 3 and the multiplication factor of 9. 
    ![synthesized_mul2](/week_1/day_2/img/Various_Flop_Coding_Styles_and_Optimization/synthesized_mul8.png)
    
    The generated netlist for both these examples is attached for review. 
    These optimisations shows a glimpse of how a hardware design can be written in efficient ways which preserves hardware resources.
    
    

