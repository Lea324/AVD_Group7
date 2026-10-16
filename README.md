# AVD
AERO60002 - Aerospace Vehicle Design. Year 3 group project.

# Current Sizing
Weight:

    W_0 = 356073.207 kg 
    W_f = 147618.894 kg 
    We = 152974.313 kg 
    W_pax = 14850.000 kg 
    W_crew = 630.000 kg 
    W_cargo = 40000.000 kg 

Fuselage:

    Total length is 62.411 m, 
    with cabin length 20.298 m, 
    Upper cargo length 19.995 m, 
    upper total length is 40.292 m 
    Lower cargo length is 42.451 m 
    with 2.159 m rest space. 
    D_outer and D_inner: 5.834 m and 5.478 m 
    with 7 inch wall stickness
    Current Cargo density = 160 kg/m^3

T/W and W/Sref:
    
    AR = 7.5 
    wing span b = 64.097 m 
    Sref = 547.783 m^2. 
    L_Fuslage/ b = 1.027. 
    Wing Loading = 6376.754. 
    Thrust to weight ratio = 0.332.With selected CL_max_setting = 1.2
    wing span b = 63.57 m. 
Time of mission:

                  Segment                   Duration_min    Cumulative_min
    _________________________________________________________________________
    {'0-1 Taxi & Takeoff'              }           15               15    
    {'1-2 Climb & Accelerate'          }           25               40    
    {'2-3 Main Cruise (5500 nmi)'      }       701.64           741.64    
    {'3-4 Initial Descent'             }           25           766.64  
    _________________________________________________________________________  
    {'4-5 Missed Approach + Climb'     }           25           791.64    
    {'5-6 Cruise to Alternate (370 km)'}       23.988           815.63    
    {'6-7 Loiter at 5000 ft'           }           45           860.63    
    {'7-8 Final Descent'               }           20           880.63    
    {'8-9 Landing & Taxi'              }           10           890.63    

    Considered mission time = 12.78 hours
    Total mission time = 14 h 51 min
Engine Selection:

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
