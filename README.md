
# Table of Contents

1.  [Updated Dactyl Build Guide](#org362b649)
    1.  [Parts List (This is what I spent on parts)](#org446a215)
        1.  [Retailers](#org8b805f2)
    2.  [Dimensions](#org53867d1)
    3.  [Step-by-step instructions](#orgdfe8133)
        1.  [Preparation](#org03c8a72)
        2.  [Circuit design](#orga654458)
        3.  [Etching](#org6848cb5)
        4.  [Wiring](#orgf051b6e)
        5.  [PCB Layering instructions](#org61f4e8c)
        6.  [Firmware guide](#org5ba9dbb)



<a id="org362b649"></a>

# Updated Dactyl Build Guide


<a id="org446a215"></a>

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


<a id="org8b805f2"></a>

### Retailers


<a id="org53867d1"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="orgdfe8133"></a>

## Step-by-step instructions


<a id="org03c8a72"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="orga654458"></a>

### Circuit design


<a id="org6848cb5"></a>

### Etching


<a id="orgf051b6e"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="org61f4e8c"></a>

### PCB Layering instructions


<a id="org5ba9dbb"></a>

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

