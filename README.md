
# Table of Contents

1.  [Updated Dactyl Build Guide](#org13190fa)
    1.  [Parts List (This is what I spent on parts)](#org0a3b0ef)
        1.  [Retailers](#org1c8a102)
    2.  [Dimensions](#orgd3d017c)
    3.  [Step-by-step instructions](#org44fce0d)
        1.  [Preparation](#org6126562)
        2.  [Circuit design](#org22e0d27)
        3.  [Etching](#org4c8ceb9)
        4.  [Wiring](#orgac923f7)
        5.  [PCB Layering instructions](#org8ac8352)
        6.  [Firmware guide](#orgeb822c9)



<a id="org13190fa"></a>

# Updated Dactyl Build Guide


<a id="org0a3b0ef"></a>

## Parts List (This is what I spent on parts)

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Parts:</th>
<th scope="col" class="org-right">Cost in USD:</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">3D Printed Shells</td>
<td class="org-right">400000</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Key Switches</td>
<td class="org-right">500000</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Key Caps</td>
<td class="org-right">500000</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Pyralux (Flexible copper for PCB)</td>
<td class="org-right">600000</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Total:</td>
<td class="org-right">total([])</td>
</tr>
</tbody>
</table>


<a id="org1c8a102"></a>

### Retailers


<a id="orgd3d017c"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="org44fce0d"></a>

## Step-by-step instructions


<a id="org6126562"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="org22e0d27"></a>

### Circuit design


<a id="org4c8ceb9"></a>

### Etching


<a id="orgac923f7"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="org8ac8352"></a>

### PCB Layering instructions


<a id="orgeb822c9"></a>

### Firmware guide

1.  config.qmk.fm

    -   Under board, choose 'handwired/dactyl'.
    -   Change defaults as necessary.
    -   Click on 'COMPILE'.
    -   Once finished, download the .hex file by clicking 'FIRMWARE'. (Consider saving the keymap.json file for future reference.)
    -   For MacOS & Windows, use the qmk-toolbox application to flash the Teensy 2.0. Follow gui instructions.
    -   For GNU+Linux, use your package manager to search for the teensy-loader-cli
        (or some variation therof) command-line tool. Use the following syntax to
        flash your chosen hex file: `$ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex\=`

