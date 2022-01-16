# 4runner-alarm-wiring
Replacing a deprecated Directed Viper 5901 alarm with a Viper 4806V.
Both models include remote start and integrate into the vehicle CAN bus security system.

## Manuals
Note; Relevant pages and techniques are highlighted in their respective PDFs

[4806V Install Guide (single page)](4806-one-page-install-guide.pdf)  
[4806V Install Manual](4806V-install-manual.pdf)  
[4806V Owners Manual](4806V-owners-manual.pdf)  

[5901 Install Manual](5901-install-manual.pdf)  

[ADS-AL Security System Manual](ADS-AL(TB)-install-guide.pdf)  

[As-installed notes](as-installed-notes.pdf)  
 
## 4806V Wiring

| H1 | Main Harness White 6 pin       | Color         | Function                 | Connected? |
|----|-------------------------------:|---------------|--------------------------|------------|
|    | 1                              | red           | 12v constant             | TRUE       |
|    | 2                              | black         | gnd                      | TRUE       |
|    | 3                              | brown         | horn out                 | TRUE       |
|    | 4                              | white/brown   | parking light isolation  | TRUE       |
|    | 5                              | white         | parking light out        | TRUE       |
|    | 6                              | orange        | sink when armed out      | TRUE       |
|    |                                |               |                          |            |
| H2 | Aux Shutdown harness 24 pin    | Color         | Function                 | Connected? |
|    | 1                              | pink/white    | ign2/flex relay out      | FALSE      |
|    | 2                              | blue/white    | 2nd status               | TRUE       |
|    | 3                              | red/white     | trunk release out        | TRUE       |
|    | 4                              | black/yellow  | dome light out           | TRUE       |
|    | 5                              | dark blue     | status out               | FALSE      |
|    | 6                              | white/black   | aux 3 out                | TRUE       |
|    | 7                              | white/violet  | aux 1 out                | TRUE       |
|    | 8                              | orange/black  | aux 4 out                | FALSE      |
|    | 9                              | gray          | hood pin in              | TRUE       |
|    | 10                             | blue          | factory horn in          | FALSE      |
|    | 11                             | white/black   | activation in            | FALSE      |
|    | 12                             | violet/white  | tach in                  | TRUE       |
|    | 13                             | black/white   | parking brake in         | TRUE       |
|    | 14                             | green/black   | factory alarm disarm out | TRUE       |
|    | 15                             | green         | door input               | TRUE       |
|    | 16                             | NC            | nc                       | FALSE      |
|    | 17                             | pink          | ign 1 out                | FALSE      |
|    | 18                             | violet        | door input               | TRUE       |
|    | 19                             | violet/black  | aux 2 out                | TRUE       |
|    | 20                             | brown         | brake shutdown input     | FALSE      |
|    | 21                             | violet/yellow | starter out              | FALSE      |
|    | 22                             | gray/black    | diesel start in          | FALSE      |
|    | 23                             | orange        | accesory out             | TRUE       |
|    | 24                             | green/white   | factory alarm arm out    | TRUE       |
|    |                                |               |                          |            |
| H3 | Remote start white 8 pin heavy | Color         | Function                 | Connected? |
|    | 1                              | red/black     | starter in               | TRUE       |
|    | 2                              | pink/black    | flex relay in            | TRUE       |
|    | 3                              | pink/white    | flex relay out           | TRUE       |
|    | 4                              | red           | fused 12v in             | FALSE      |
|    | 5                              | violet        | starter out              | TRUE       |
|    | 6                              | orange        | accesory out             | TRUE       |
|    | 7                              | red/white     | 12v ignition 2           | TRUE       |
|    | 8                              | pink          | ignition 1 IO            | TRUE       |
|    |                                |               | .                        |            |
| H4 | Door lock 3 pin                | Color         | Function                 | Connected? |
|    | 1                              | Blue          | Unlock out               | TRUE       |
|    | 2                              | nc            | NC                       | TRUE       |
|    | 3                              | green         | Lock out                 | TRUE       |
|    |                                |               |                          |            |
| H5 | D2d Harness red 4 pin          | Color         | Function                 | Connected? |
|    | 1                              | blue          | d2d tx                   | FALSE      |
|    | 2                              | black         | gnd                      | FALSE      |
|    | 3                              | green         | d2d rx                   | FALSE      |
|    | 4                              | red           | 12v                      | FALSE      |
|    |                                |               |                          |            |
| H6 | bitwrited black 3 pin          | Color         | Function                 | Connected? |
|    | 1                              | red           | 12v                      | FALSE      |
|    | 2                              | orange        | tx rx                    | FALSE      |
|    | 3                              | black         | 12v                      | FALSE      |

## 5901 Wiring

| H1 | Primary harness 12 pin     | Color             | Function                  | Connect to |
|----|---------------------------:|-------------------|---------------------------|------------|
|    | 1                          | red/white         | trunk release out         | H2-3       |
|    | 2                          | red               | 12v constant in           | H1-1       |
|    | 3                          | brown             | siren out                 |            |
|    | 4                          | white/brown       | light flash isolation out | H1-4       |
|    | 5                          | black             | gnd                       | H1-2       |
|    | 6                          | violet            | door trigger in +         | H2-18      |
|    | 7                          | blue              | trunk pin in              |            |
|    | 8                          | green             | door trigger in -         | H2-15      |
|    | 9                          | black/white       | dome light out            | H2-4       |
|    | 10                         | white/blue        | remote start activation   | ?          |
|    | 11                         | white             | parking light out         | H1-5       |
|    | 12                         | orange            | sink when armed out       | H1-6       |
|    |                            |                   |                           |            |
| H2 | Aux harness 8 pin          | Color             | Function                  | Connect to |
|    | 1                          | light green/black | factory alarm disarm out  | H2-14      |
|    | 2                          | light green/white | factory alarm arm out     | H2-24      |
|    | 3                          | white/violet      | aux 1 out                 | H2-7       |
|    | 4                          | violet/black      | aux 2 out                 | H2-19      |
|    | 5                          | white/black       | aux 3 out                 | H2-6       |
|    | 6                          | light blue        | 2nd unlock out            |            |
|    | 7                          | gray/black        | diesel start              |            |
|    | 8                          | brown/black       | horn honk                 | H1-3       |
|    |                            |                   |                           |            |
| H3 | Heavy Guage 10 pin         | Color             | Function                  | Connect to |
|    | 1                          | pink              | ign 1 io                  | H3-8       |
|    | 2                          | red/white         | ign 2 in                  | H3-7       |
|    | 3                          | orange            | acc out                   | H3-6       |
|    | 4                          | violet            | starter output            | H3-5       |
|    | 5                          | green             | starter input             | H3-1       |
|    | 6                          | red               | ign1 input                |            |
|    | 7                          | pink/white        | ign2 out                  | H3-3       |
|    | 8                          | pink/black        | flex relay input          |            |
|    | 9                          | red/black         | accesory starter input    |            |
|    | 10                         | nc                | nc                        |            |
|    |                            |                   |                           |            |
| H? | Remote start input 5 pin   | Color             | Function                  | Connect to |
|    | 1                          | Black/white       | nss                       | GND?       |
|    | 2                          | violet/white      | tach in                   | H2-12      |
|    | 3                          | brown             | brake shutdown in         | H2-13      |
|    | 4                          | gray              | hood pin                  | H2-9       |
|    | 5                          | blue/white        | 2nd status in             | H2-2       |
|    |                            |                   |                           |            |
| H? | Remote start aux out 5 pin | Color             | Function                  | Connect to |
|    | 1                          | pink/white        | flex relay out            | H3-2       |
|    | 2                          | orange            | acc out -                 | H2-23      |
|    | 3                          | violet            | starter out               |            |
|    | 4                          | pink              | ign 1 out                 |            |
|    | 5                          | blue              | status out                |            |
|    |                            |                   |                           |            |
| H? | Door lock 3 pin            | Color             | Function                  | Connect to |
|    | 1                          | blue              | unlock out                | H4-1       |
|    | 2                          | nc                | nc                        | H4-2       |
|    | 3                          | green             | lock                      | H4-3       |

