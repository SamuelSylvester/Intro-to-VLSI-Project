Due to the behavior of this specific compound gate, I was able to setup the simulation to do the best case rising and falling edge in the same simulation, as well as the worst case rising and falling edge. 

Ensure you are using spectre simulator (my software defaults to hspiceD).

The simulation best_cases is setup to do the best cases (contamination delay). You can load the state bestCaseTransient in ADE L to run the simulation for the schematic, and the state bestCaseExtracted for the simulation of the layout. All 4 inputs are shown, as well as the output, regardless of if the inputs change. This is to ensure that the proper state transitions are being shown.
The best case rising edge is from (A=1,B=0,C=0,D=0) to (A=0,B=0,C=0,D=0).
The best case falling edge is from (A=0,B=0,C=0,D=0) to (A=1,B=1,C=0,D=0).

The simulation best_cases is setup to do the worst cases (propagation delay). You can load the state worstCaseTransient in ADE L to run the simulation for the schematic, and the state worstCaseExtracted for the simulation of the layout.  All 4 inputs are shown, as well as the output, regardless of if the inputs change. This is to ensure that the proper state transitions are being shown.
The worst case rising edge is from (A=0,B=0,C=0,D=1) to (A=0,B=0,C=1,D=1).
The worst case falling edge is from (A=0,B=0,C=1,D=1) to (A=0,B=0,C=0,D=1).