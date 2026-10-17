# AVD
AERO60002 - Aerospace Vehicle Design. Year 3 group project.

# Current Sizing
Weight:

    W_0 = 290408.102 kg 
    W_f = 108629.073 kg 
    We = 126299.029 kg 
    W_pax = 14850.000 kg 
    W_crew = 630.000 kg 
    W_cargo = 40000.000 kg 

Fuselage:

     Total length is 67.161 m, 
    with cabin length 26.497 m, 
    Upper cargo length 19.438 m, 
    upper total length is 45.935 m 
    Lower cargo length is 47.202 m 
    with 1.268 m rest space. 
    D_outer and D_inner: 5.834 m and 5.478 m 
    with 7 inch wall stickness 
    Current Cargo density = 160 kg/m^3

T/W and W/Sref:
    
    AR = 9.0 
    wing span b = 64.929 m 
    Sref = 468.415 m^2. 
    b / L_Fuslage = 0.967. 
    Wing Loading = 6082.010. 
    Thrust to weight ratio = 0.298.

Time of mission:

                 Segment                     Duration_min    Cumulative_min
    ______________________________________________________________________________

    {'0-1 Taxi & Takeoff'              }           15               15    
    {'1-2 Climb & Accelerate'          }           25               40    
    {'2-3 Main Cruise (5500 nmi)'      }       701.64           741.64    
    {'3-4 Initial Descent'             }           25           766.64    
    ______________________________________________________________________________
    {'4-5 Missed Approach + Climb'     }           25           791.64    
    {'5-6 Cruise to Alternate (370 km)'}       32.521           824.16    
    {'6-7 Loiter at 5000 ft'           }           45           869.16    
    {'7-8 Final Descent'               }           20           889.16    
    {'8-9 Landing & Taxi'              }           10           899.16    
    Considered mission time = 12.78 hours
    Total mission time = 14 h 51 min
Engine Selection:

Trent xwb-97

Wing Selection:

# Mass EASA Standard
Easy Access Rules for Air Operations (EASA, current): https://www.easa.europa.eu/en/document-library/easy-access-rules/online-publications/easy-access-rules-air-operations

EASA Annex to ED Decision 2014/015/R, Part-CAT (PDF): https://www.easa.europa.eu/sites/default/files/dfu/Annex%20to%20ED%20Decision%202014-015-R%20-%20Part-CAT_0.pdf
# Cabin and fuselage sizing
Roskam, Airplane Design Part 3, 2002

Torenbeek, Synthesis of Subsonic Airplane Design, 1982

# Wetted Area Analysis in Airplane Design
https://www.scribd.com/document/897371895/Wetted-and-Projected-Area-Relationships-in-Commercial-Airplane-Design

### Install Aerospace toolbox for wing desgin!!!
