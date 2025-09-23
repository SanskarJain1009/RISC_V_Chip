# Day 1: 
It included-
1. Introduction to open-source simulator: 
    A general introduction is given using the block diagram linking iverilog, design and tb. 

2. Labs using iverilog and gtkwave:
    Firstly the git repo is cloned from https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git.
    ![Lab 1 Introduction](/week_1/day_1/img/Labs_Using_Iverilog_and_GTKWave/3_SKY130RTL_D1SK2_L1_Lab1_introduction_to_lab.png)

    Secondly, (this was divided in 2 parts) 
    i. inside this repo, it contained a directory which included verilog designs with respective testbenches. To showcase the simulation using iverilog, good_mux.v and tb_good_mux.v are taken as example. 
    ![Lab 2 Introduction Part 1](/week_1/day_1/img/Labs_Using_Iverilog_and_GTKWave/4_SKY130RTL_D1SK2_L2_Lab2_Introduction_iverilog_gtkwave_part1.png)
    ii. Then, the .vcd file is generated and waves are shown using gtkwave. Then the design and tb file are shown and explained. 
    ![Lab 2 Introduction Part 2](/week_1/day_1/img/Labs_Using_Iverilog_and_GTKWave/5_SKY130RTL_D1SK2_L3_Lab2_Introduction_iverilog_gtkwave_part2.png)

3. Introduction to Yosys and Logic synthesis:
    This comprised of 3 short videos discussing and introductory session for yosys and logic synthesis. The .lib file is discussed in this which is present in the cloned repo.

4. Labs using Yosys and Sky130 PDKs:
    In this part, the netlist generation is done using yosys and sky130. 
    (NOTE- The mentioned sky130 .lib file is present in lib directory and not in my_lib, maybe the video is old. And by the same name, the .lib file is present in DC_WORKSHOP)
    The generated .dot file showing the netlist generated is- ![Generated Netlist](/week_1/day_1/img/Labs_using_Yosys_and_Sky130_PDKs/9_SKY130RTL_D1SK4_L1_Lab3_Yosys_1_good_mux_Part1.png)

The generated a.out file and the good_mux_netlist.v file are attached for reference. 


