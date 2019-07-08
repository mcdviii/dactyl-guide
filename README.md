
# Table of Contents

1.  [Updated Dactyl Build Guide](#org5f8c3a0)
    1.  [Parts List (This is what I spent on parts)](#org594edd3)
        1.  [Retailers](#orgdfca223)
    2.  [Dimensions](#org5f72b21)
    3.  [Step-by-step instructions](#org42b7f58)
        1.  [Preparation](#org1bfc9b6)
        2.  [Circuit design](#orgcd52d01)
        3.  [Etching](#org1b003bb)
        4.  [Wiring](#org8e32a28)
        5.  [PCB Layering instructions](#org4073b22)
        6.  [Firmware guide](#org1ee831b)



<a id="org5f8c3a0"></a>

# Updated Dactyl Build Guide


<a id="org594edd3"></a>

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


<a id="orgdfca223"></a>

### Retailers


<a id="org5f72b21"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="org42b7f58"></a>

## Step-by-step instructions


<a id="org1bfc9b6"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="orgcd52d01"></a>

### Circuit design


<a id="org1b003bb"></a>

### Etching


<a id="org8e32a28"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="org4073b22"></a>

### PCB Layering instructions


<a id="org1ee831b"></a>

### Firmware guide

1.  config.qmk.fm

    -   Under board, choose 'handwired/dactyl'.
    -   Change defaults as necessary.
    -   Click on 'COMPILE'.
    -   Once finished, download the .hex file by clicking 'FIRMWARE'. (Consider saving the keymap.json file for future reference.)
    -   For MacOS & Windows, use the qmk-toolbox application to flash the Teensy 2.0. Follow gui instructions.
    -   For GNU+Linux, use your package manager to search for the teensy-loader-cli
        (or some variation therof) command-line tool. Use the following syntax to
        flash your chosen hex file: `$ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex`

