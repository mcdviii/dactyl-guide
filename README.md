
# Table of Contents

1.  [Updated Dactyl Build Guide](#org8855fa5)
    1.  [Parts List (This is what I spent on parts)](#org6bec38e)
        1.  [Retailers](#org9b6622e)
    2.  [Dimensions](#org77d35b5)
    3.  [Step-by-step instructions](#orga1ce90c)
        1.  [Preparation](#org7575549)
        2.  [Circuit design](#orgddc8e5f)
        3.  [Notes on Xerox direct-print to Pyralux](#org1aca48f)
        4.  [Etching](#org1656a59)
        5.  [Wiring](#orgd5ef5df)
        6.  [PCB Layering instructions](#org2a6f247)
        7.  [Firmware guide](#org95cb5cb)



<a id="org8855fa5"></a>

# Updated Dactyl Build Guide


<a id="org6bec38e"></a>

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


<a id="org9b6622e"></a>

### Retailers


<a id="org77d35b5"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="orga1ce90c"></a>

## Step-by-step instructions


<a id="org7575549"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="orgddc8e5f"></a>

### Circuit design


<a id="org1aca48f"></a>

### Notes on Xerox direct-print to Pyralux


<a id="org1656a59"></a>

### Etching


<a id="orgd5ef5df"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="org2a6f247"></a>

### PCB Layering instructions


<a id="org95cb5cb"></a>

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

