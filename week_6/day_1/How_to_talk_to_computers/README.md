# How to talk to computers: 
It included-
1. Introduction to QFN-48 Package, chip, pads, core, die and IPs:
    Basic introduction to package and chip design. How chip actually looks after fabrication. Foundary IPs and macros are shown. The images below explain it better.
    ![Chip_Pad](/week_6/day_1/How_to_talk_to_computers/img/Chip_Pad.png)
    ![Inside_Chip](/week_6/day_1/How_to_talk_to_computers/img/Inside_Chip.png)
    
2. Introduction to RISC-V:
    A basic introduction was given on how from RISC-V Archtecture to Implementation (picorv32 cpu core was taken as an example) to Layout (qflow) is the RTL to GDSII Flow. The image below shows this.
    ![Intro_to_RISCV](/week_6/day_1/How_to_talk_to_computers/img/Intro_to_RISCV.png)
    
3. From Software Applications to Hardware
    This focuses on how from software to execution is translated. The flow goes like-
    Application Software -> System Software (OS, Compiler, Assembler) ->  Hardware
    The images below shows this flow and the example.
    ![Software_Application_to_Hardware](/week_6/day_1/How_to_talk_to_computers/img/Software_Application_to_Hardware.png)
    ![Software_Application_to_Hardware_Example](/week_6/day_1/How_to_talk_to_computers/img/Software_Application_to_Hardware_Example.png)
    
    The instructions obtained after compilation gives instructions which are human understandable and act as abstract interface between any programming language and the hardware. This is Abstract Interface (Instruction Set Architecture) or Architecture of the computer.
    The image below describes the ISA and the flow from ISA->RTL->Layout.
    ![Abstract_Interface_ISA](/week_6/day_1/How_to_talk_to_computers/img/Abstract_Interface_ISA.png)
    ![ISA_RTL_to_Hardware](/week_6/day_1/How_to_talk_to_computers/img/ISA_RTL_to_Hardware.png)
    
