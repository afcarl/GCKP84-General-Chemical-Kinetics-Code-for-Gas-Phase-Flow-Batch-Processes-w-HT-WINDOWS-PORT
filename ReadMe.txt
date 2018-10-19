
====================================================================================================================
GCKP86: General Chemical Kinetics Code for Gas-Phase Flow Batch Processes with Heat-Transfer Effects: (WINDOWS-PORT)
====================================================================================================================

Program Capabilities:

A general chemical kinetics code for complex, homogeneous ideal-gas reactions is described. The code is designed for flexibility, convenience, and speed of computation in treating a variety of reaction conditions. These conditions include (1) general reaction in a batch system or one-dimensional frictionless flow; (2) computation in a well-stirred (highly back mixed) reactor; (3) reaction behind a shock wave; (4) ignition and combustion reactions in a batch or flowing system; and (5) nozzle expansion reactions.


1. Pre-Requisits/Reference: (https://ntrs.nasa.gov/search.jsp?R=19840024376)

2. Documentation: (https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/19840024376.pdf)

3. Example problems located in "./examples/":


4. INPUT FILE #1: "./thermo.inp".

======================================
START: Input File: "thermo.inp"
======================================
   300.000  1000.000  5000.000                                                  
AR                L 5/66AR 1.00 0.00 0.00 0.G   300.000  5000.000     39.94800 1
 0.25000000E 01     0.00000000     0.00000000     0.00000000     0.00000000    2
-0.74537502E 03 0.43660006E 01 0.25000000E 01     0.00000000     0.00000000    3
     0.00000000     0.00000000-0.74537498E 03 0.43660006E 01     0.00000000    4
BR                J 6/74BR 1.   0.   0.   0.G   300.000  5000.000    79.909    1
 0.20843207E 01 0.71949483E-03-0.27419924E-06 0.42422650E-10-0.23791570E-14    2
 0.12858837E 05 0.90838003E 01 0.24611551E 01 0.33319275E-03-0.10080655E-05    3
 0.12262126E-08-0.44283510E-12 0.12711920E 05 0.69494733E 01                   4

... <content removed> ...

H2O(L)            J 3/79H  2.O  1.   0.   0.L   273.150   500.000     18.01520 1
 0.28630800E 02-0.20260986E 00 0.78529479E-03-0.13653020E-05 0.91326966E-09    2
-0.38579539E 05-0.11895046E 03 0.28630800E 02-0.20260986E 00 0.78529479E-03    3
-0.13653020E-05 0.91326966E-09-0.38579539E 05-0.11895046E 03     0.00000000    4
XE                L 4/70XE  10   00   00   0G   300.000  5000.000    131.290   1
 0.25000000E 01 0.             0.             0.             0.                2
-0.74537501E 03 0.61512740E 01 0.25000000E 01 0.             0.                3
 0.             0.            -0.74537499E 03 0.61512742E 01                   4
END                                                                             
======================================
END: Input File: "thermo.inp"
======================================


5. INPUT FILE #2: "./examples/example_*.inp".

5a. "Example_1.inp":  BROMINE DISSOCIATION IN A SHOCK TUBE                        CASE 1
5b. "Example_2.inp":  HYD - AIR TEST WITH HEAT TRANSFER          STOICH           CASE 2
5c. "Example_3.inp":  HYD - AIR TEST WITH HEAT TRANSFER       FULL MECH           CASE 3
5d. "Example_4.inp":  HYD - OXYGEN CASE WITH HEAT TRANSFER                        CASE 4
5e. "Example_5.inp":  CH4 - AIR RICH MECH. BATCH RXN WITH OTTO CYCLE HEAT LOSS    CASE 5
5f. "Example_6.inp":  METHANE  AIR  TEST CASE  LEAN MECHANISM                     CASE 6
5g. "Example_7.inp":  CH4 - AIR WITH AREA PROFILE OF CASE 6                       CASE 7
5h. "Example_8.inp":  METHANOL - AIR  COMBUSTION                                  CASE 8
5i. "Example_9.inp":  C3H8 - AIR WELL-STIRRED REACTOR +  ROCKET EXPANSION PROB.   CASE 9
5j. "Example_10.inp": HIGH TEMPERATURE AIR IONIZATION                             CASE 10
5k. "Example_11.inp": HIGH PRESSURE H2  -  CO REACTION                            CASE 11
5l. "Example_12.inp": HYDROGEN - OXYGEN LOW TEMP PHOTOLYTIC IGNITION              CASE 12
5m. "Example_13.inp": ETHANE PYROLYSIS     DUNKER TEST  CASE A                    CASE 13
5n. "Example_14.inp": FORMALDEHYDE OXIDATION     DUNKER TEST  CASE B              CASE 14
5o. "Example_15.inp": YETTER ET AL'S WET CO OXIDATION REDUCED MECH                CASE 15
5p. "Example_16.inp": KRAMER ET AL'S WET CO OXIDATION COMPLETE MECHANISM          CASE 16
5q. "Example_17.inp": HYDROGEN COMB. IN PURE AIR,  MACH =3.00 AND P=3.10 ATM.     CASE 17
5r. "Example_18.inp": BENZENE - OXYGEN - AR SHOCK IGNITION                        CASE 18


6. INPUT FILE #3: "./transport.inp".

======================================
START: Input File: "transport.inp"
======================================
 H2             0.687200E 00  -0.617320E 00  -0.111490E 03   0.577240E 00   VISC
 H2             0.116129E 01   0.469043E 03  -0.551496E 05  -0.149041E 01   COND
 CH3OH          0.641455E 00  -0.211775E 03   0.125265E 05   0.150983E 01   VISC
 CH3OH          0.793792E 00  -0.487550E 03   0.322097E 05   0.646522E 00   COND

... <content removed> ...

 CO2            0.440370E 00  -0.288400E 03   0.193120E 05   0.324659E 01   VISC
 CO2            0.603518E 00  -0.438483E 03   0.322949E 05   0.134023E 01   COND
 O2             0.659260E 00   0.941422E 00  -0.711780E 04   0.164432E 01   VISC
 O2             0.478050E 00  -0.452958E 03   0.579015E 05   0.228192E 01   COND
LAST                                                                            
======================================
END: Input File: "transport.inp"
======================================


5. Operation: Run "./bin/gckp86.exe"


6. OUTPUT FILE: "./results/gckp86_example_*.out".

6a. "gckp86_example_1.out":  BROMINE DISSOCIATION IN A SHOCK TUBE                        CASE 1
6b. "gckp86_example_2.out":  HYD - AIR TEST WITH HEAT TRANSFER          STOICH           CASE 2
6c. "gckp86_example_3.out":  HYD - AIR TEST WITH HEAT TRANSFER       FULL MECH           CASE 3
6d. "gckp86_example_4.out":  HYD - OXYGEN CASE WITH HEAT TRANSFER                        CASE 4
6e. "gckp86_example_5.out":  CH4 - AIR RICH MECH. BATCH RXN WITH OTTO CYCLE HEAT LOSS    CASE 5
6f. "gckp86_example_6.out":  METHANE  AIR  TEST CASE  LEAN MECHANISM                     CASE 6
6g. "gckp86_example_7.out":  CH4 - AIR WITH AREA PROFILE OF CASE 6                       CASE 7
6h. "gckp86_example_8.out":  METHANOL - AIR  COMBUSTION                                  CASE 8
6i. "gckp86_example_9.out":  C3H8 - AIR WELL-STIRRED REACTOR +  ROCKET EXPANSION PROB.   CASE 9
6j. "gckp86_example_10.out": HIGH TEMPERATURE AIR IONIZATION                             CASE 10
6k. "gckp86_example_11.out": HIGH PRESSURE H2  -  CO REACTION                            CASE 11
6l. "gckp86_example_12.out": HYDROGEN - OXYGEN LOW TEMP PHOTOLYTIC IGNITION              CASE 12
6m. "gckp86_example_13.out": ETHANE PYROLYSIS     DUNKER TEST  CASE A                    CASE 13
6n. "gckp86_example_14.out": FORMALDEHYDE OXIDATION     DUNKER TEST  CASE B              CASE 14
6o. "gckp86_example_15.out": YETTER ET AL'S WET CO OXIDATION REDUCED MECH                CASE 15
6p. "gckp86_example_16.out": KRAMER ET AL'S WET CO OXIDATION COMPLETE MECHANISM          CASE 16
6q. "gckp86_example_17.out": HYDROGEN COMB. IN PURE AIR,  MACH =3.00 AND P=3.10 ATM.     CASE 17
6r. "gckp86_example_18.out": BENZENE - OXYGEN - AR SHOCK IGNITION                        CASE 18

