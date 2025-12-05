# Project Demo - How to run simulation (PLCSIM)

1. Open Siemens TIA Portal and load the project file.
2. Open PLCSIM and connect to the simulated PLC (ensure correct PLC version).
3. Load the compiled block into PLCSIM and start simulation mode.
4. Test Cases:
   - Test Case 1: Normal Start
     - Set PB_Start = 1
     - Verify OUT_MainContactor = 1 and OUT_PumpA_Run starts
   - Test Case 2: Sequence Pump B
     - Start Pump B manually or via sequence; verify OUT_PumpB_Run
   - Test Case 3: Single Pump Fault (Pump A)
     - Activate FLT_PumpA input
     - Verify OUT_PumpA_Run stops and OUT_StandbyPump_Run starts
     - Verify OUT_AlarmLamp blinks
   - Test Case 4: Dual Pump Fault
     - Activate FLT_PumpA and FLT_PumpB simultaneously
     - Verify FLT_TwoPumpFault is set
     - Verify OUT_MainContactor is stopped and alarm is active
5. Record results and screenshots for README.
