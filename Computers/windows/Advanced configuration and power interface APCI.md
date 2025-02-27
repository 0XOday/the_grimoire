Advanced Configuration and Power Interface (ACPI) modes are power states that a computer can enter to save power. The six ACPI power states are: 

    S0: The run state, where the computer is fully functional 

S1: The suspend state, where the CPU is suspended but retains its contexts 
S2: A sleep state where the CPU is not powered but RAM is still being refreshed 
S3: A deeper sleep mode where the processor does not need to keep its cache coherent 
S4: A sleep state where contexts are saved to disk 
S5: The soft-off state, where all activity stops and all contexts are lost 

ACPI also has global system states, called G-states, which define the power state of the entire system. The G0 state is the working state, and the G1 state is the sleeping state. 
ACPI can also manage the power state of individual devices. For example, ACPI tables can encode information about devices that share a power line. 
