 # clk period = 20ns 

### syntesis stats
```

19. Printing statistics.

=== tt_um_yappingnoises_TCPU16 ===

        +----------Local Count, excluding submodules.
        |        +-Local Area, excluding submodules.
        |        | 
      499        - wires
      534        - wire bits
      111        - public wires
      146        - public wire bits
        8        - ports
       43        - port bits
      515 1.56E+04 cells
       13  228.301   gf180mcu_fd_sc_mcu7t5v0__and2_1
        3   65.856   gf180mcu_fd_sc_mcu7t5v0__and3_1
        1   21.952   gf180mcu_fd_sc_mcu7t5v0__aoi211_1
       24  421.478   gf180mcu_fd_sc_mcu7t5v0__aoi21_1
       11  265.619   gf180mcu_fd_sc_mcu7t5v0__aoi221_1
        3    59.27   gf180mcu_fd_sc_mcu7t5v0__aoi22_1
       24  316.109   gf180mcu_fd_sc_mcu7t5v0__buf_1
       25   219.52   gf180mcu_fd_sc_mcu7t5v0__clkinv_1
       97 6.18E+03   gf180mcu_fd_sc_mcu7t5v0__dffq_1
       98 3.23E+03   gf180mcu_fd_sc_mcu7t5v0__mux2_2
       16 1.12E+03   gf180mcu_fd_sc_mcu7t5v0__mux4_1
       54  592.704   gf180mcu_fd_sc_mcu7t5v0__nand2_1
       11   169.03   gf180mcu_fd_sc_mcu7t5v0__nand3_1
        3    59.27   gf180mcu_fd_sc_mcu7t5v0__nand4_1
       32  421.478   gf180mcu_fd_sc_mcu7t5v0__nor2_1
        6   105.37   gf180mcu_fd_sc_mcu7t5v0__nor3_1
        5   109.76   gf180mcu_fd_sc_mcu7t5v0__nor4_1
       15   329.28   gf180mcu_fd_sc_mcu7t5v0__oai211_1
       33  579.533   gf180mcu_fd_sc_mcu7t5v0__oai21_1
        1   26.342   gf180mcu_fd_sc_mcu7t5v0__oai221_1
        1   21.952   gf180mcu_fd_sc_mcu7t5v0__oai22_1
        4   96.589   gf180mcu_fd_sc_mcu7t5v0__oai31_1
        8  140.493   gf180mcu_fd_sc_mcu7t5v0__or2_1
        2   52.685   gf180mcu_fd_sc_mcu7t5v0__or4_1
        1    8.781   gf180mcu_fd_sc_mcu7t5v0__tiel
        7  199.763   gf180mcu_fd_sc_mcu7t5v0__xnor2_1
       14  368.794   gf180mcu_fd_sc_mcu7t5v0__xor2_1
        3  151.469   gf180mcu_fd_sc_mcu7t5v0__xor3_1

   Chip area for module '\tt_um_yappingnoises_TCPU16': 15557.382400
     of which used for sequential elements: 6175.097600 (39.69%)


```

### sta logs 
```

=== Summary
logs/15_sta_max_ff.log:worst slack max 7.29
logs/15_sta_max_ff.log:worst slack min 0.16
logs/15_sta_max_ss.log:worst slack max -24.12
logs/15_sta_max_ss.log:worst slack min 1.29
logs/15_sta_max_tt.log:worst slack max -2.04
logs/15_sta_max_tt.log:worst slack min 0.50
logs/15_sta_min_ff.log:worst slack max 7.87
logs/15_sta_min_ff.log:worst slack min 0.16
logs/15_sta_min_ss.log:worst slack max -22.51
logs/15_sta_min_ss.log:worst slack min 1.29
logs/15_sta_min_tt.log:worst slack max -1.12
logs/15_sta_min_tt.log:worst slack min 0.50
logs/15_sta_nom_ff.log:worst slack max 7.60
logs/15_sta_nom_ff.log:worst slack min 0.16
logs/15_sta_nom_ss.log:worst slack max -23.22
logs/15_sta_nom_ss.log:worst slack min 1.29
logs/15_sta_nom_tt.log:worst slack max -1.50
logs/15_sta_nom_tt.log:worst slack min 0.50
Worstcase IR drop: 7.36e-04 V
Worstcase IR drop: 6.85e-04 V
```

sta fails at ss corner. 

rerunning at period 100ns 

# clock period = 100ns 

```
=== Summary
logs/15_sta_max_ff.log:worst slack max 86.86
logs/15_sta_max_ff.log:worst slack min 0.16
logs/15_sta_max_ss.log:worst slack max 53.99
logs/15_sta_max_ss.log:worst slack min 1.29
logs/15_sta_max_tt.log:worst slack max 77.12
logs/15_sta_max_tt.log:worst slack min 0.50
logs/15_sta_min_ff.log:worst slack max 87.39
logs/15_sta_min_ff.log:worst slack min 0.16
logs/15_sta_min_ss.log:worst slack max 55.64
logs/15_sta_min_ss.log:worst slack min 1.29
logs/15_sta_min_tt.log:worst slack max 78.01
logs/15_sta_min_tt.log:worst slack min 0.50
logs/15_sta_nom_ff.log:worst slack max 87.15
logs/15_sta_nom_ff.log:worst slack min 0.16
logs/15_sta_nom_ss.log:worst slack max 54.89
logs/15_sta_nom_ss.log:worst slack min 1.29
logs/15_sta_nom_tt.log:worst slack max 77.61
logs/15_sta_nom_tt.log:worst slack min 0.50
Worstcase IR drop: 1.45e-04 V
Worstcase IR drop: 1.37e-04 V
```

STA analysis passes at 100 ns or 10 MHz 



# Slew and cap violations

There are max slew and max cap violations. On investigation into individual liberty files and sdc files, the max fanout is defined as 10 in .sdc file as `set_max_fanout 10.0000 [current_design]`. but in the some of the corners, the max fanouts are going beyond that limit. 

```
set_max_transition 3.0000 [current_design]

set_max_capacitance 0.2000 [current_design]

set_max_fanout 10.0000 [current_design]
```

for one of the corners , you can observe the fact that the fanout, and slew is getting violated
```
Startpoint: ui_in[6] (input port clocked by clk)
Endpoint: _845_ (rising edge-triggered flip-flop clocked by clk)
Path Group: clk
Path Type: max

Fanout         Cap        Slew       Delay        Time   Description
---------------------------------------------------------------------------------------------
                                  0.000000    0.000000   clock clk (rise edge)
                                  0.000000    0.000000   clock network delay (propagated)
                                 20.000000   20.000000 v input external delay
     1    0.005594    0.103737    0.044112   20.044113 v ui_in[6] (in)
                                                         ui_in[6] (net)
                      0.103737    0.000000   20.044113 v input8/I (gf180mcu_fd_sc_mcu7t5v0__dlyb_1)
     8    0.057898    0.889915    2.121856   22.165970 v input8/Z (gf180mcu_fd_sc_mcu7t5v0__dlyb_1)
                                                         net8 (net)
                      0.889927    0.002267   22.168236 v _479_/I0 (gf180mcu_fd_sc_mcu7t5v0__mux2_2)
     1    0.004569    0.173607    0.717680   22.885916 v _479_/Z (gf180mcu_fd_sc_mcu7t5v0__mux2_2)
                                                         _049_ (net)
                      0.173607    0.000099   22.886015 v _845_/D (gf180mcu_fd_sc_mcu7t5v0__dffq_1)
                                             22.886015   data arrival time

                                100.000000  100.000000   clock clk (rise edge)
                                  0.000000  100.000000   clock source latency
     1    0.035338    0.252839    0.118078  100.118073 ^ clk (in)
                                                         clk (net)
                      0.252845    0.000000  100.118073 ^ clkbuf_0_clk/I (gf180mcu_fd_sc_mcu7t5v0__clkbuf_16)
    16    0.209926    0.366962    0.479140  100.597214 ^ clkbuf_0_clk/Z (gf180mcu_fd_sc_mcu7t5v0__clkbuf_16)
                                                         clknet_0_clk (net)
                      0.366980    0.003652  100.600868 ^ clkbuf_4_2_0_clk/I (gf180mcu_fd_sc_mcu7t5v0__clkbuf_8)
     7    0.030929    0.173094    0.367550  100.968414 ^ clkbuf_4_2_0_clk/Z (gf180mcu_fd_sc_mcu7t5v0__clkbuf_8)
                                                         clknet_4_2_0_clk (net)
                      0.173094    0.000703  100.969124 ^ _845_/CLK (gf180mcu_fd_sc_mcu7t5v0__dffq_1)
                                 -0.250000  100.719124   clock uncertainty
                                  0.000000  100.719124   clock reconvergence pessimism
                                 -0.383399  100.335724   library setup time
                                            100.335724   data required time
---------------------------------------------------------------------------------------------
                                            100.335724   data required time
                                            -22.886015   data arrival time
---------------------------------------------------------------------------------------------
                                             77.449707   slack (MET)
```

### Potential fixes for these violations?

- People on tiny tapeout discord mentioned adding `"RUN_POST_GRT_DESIGN_REPAIR": 1` to the config.json and this seemed to have removed some of the slew violations. although, there are still 2 corners with slew violations, and none of the max cap violations have been resolved. 
