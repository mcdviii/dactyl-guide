
# Table of Contents

1.  [Updated Dactyl Build Guide](#org2f1635e)
    1.  [Parts List (This is what I spent on parts)](#org1e0bc9a)
        1.  [Retailers](#org8219a0a)
    2.  [Dimensions](#org2922d44)
    3.  [Step-by-step instructions](#org8d014ea)
        1.  [Preparation](#org3502a1f)
        2.  [Circuit design](#org2047e14)
        3.  [Etching](#orgb02176e)
        4.  [Wiring](#orgf3e1b29)
        5.  [PCB Layering instructions](#orgb9d394b)
        6.  [Firmware guide](#org976be59)



<a id="org2f1635e"></a>

# Updated Dactyl Build Guide


<a id="org1e0bc9a"></a>

## Parts List (This is what I spent on parts)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Parts:</th>
<th scope="col" class="org-left">Cost in USD:</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">3D Printed Shells</td>
<td class="org-left">$40</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Key Switches</td>
<td class="org-left">~$50</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Key Caps</td>
<td class="org-left">~$50</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Pyralux (Flexible copper for PCB)</td>
<td class="org-left">$60</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>
</table>


<a id="org8219a0a"></a>

### Retailers


<a id="org2922d44"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="org8d014ea"></a>

## Step-by-step instructions


<a id="org3502a1f"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="org2047e14"></a>

### Circuit design


<a id="orgb02176e"></a>

### Etching


<a id="orgf3e1b29"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="orgb9d394b"></a>

### PCB Layering instructions


<a id="org976be59"></a>

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

