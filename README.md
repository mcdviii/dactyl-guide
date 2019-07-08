
# Table of Contents

1.  [Organize & Commit Personal Work to Github](#org3046c3c)
    1.  [PCB Design](#org4180db2)
    2.  [Take Dimensions for standoffs, screws & rubber feet](#orgbfd446b)
    3.  [Step-by-step instructions](#org0081745)
        1.  [Updated parts list](#org12d3ee4)
        2.  [Heatshrink standoffs](#org948bc2c)
        3.  [PCB Layering instructions](#org80cd78f)
        4.  [Diode position](#org4ffd7b6)
        5.  [Firmware guide](#orge0d7714)



<a id="org3046c3c"></a>

# Organize & Commit Personal Work to Github


<a id="org4180db2"></a>

## PCB Design


<a id="orgbfd446b"></a>

## Take Dimensions for standoffs, screws & rubber feet


<a id="org0081745"></a>

## Step-by-step instructions


<a id="org12d3ee4"></a>

### Updated parts list


<a id="org948bc2c"></a>

### Heatshrink standoffs


<a id="org80cd78f"></a>

### PCB Layering instructions


<a id="org4ffd7b6"></a>

### Diode position

For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
allows the current to flow from the row, through the switch and out through the column.


<a id="orge0d7714"></a>

### Firmware guide

1.  config.qmk.fm

    Under board, choose 'handwired/dactyl'.
    Change defaults as necessary.
    Click on 'COMPILE'.
    Once finised, download the .hex file by clicking 'FIRMWARE'.
    
    -   Consider saving the keymap.json file for future reference.
    
    For MacOS & Windows, use the qmk-toolbox application to flash the Teensy 2.0.
    Follow gui instructions.
    For GNU+Linux, use your package manager to search for the teensy-loader-cli (or
    some variation therof) command-line tool. Use the following syntax to flash your
    chosen hex file:
    
    -   $ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex

