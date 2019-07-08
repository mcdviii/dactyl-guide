
# Table of Contents

1.  [Updated Dactyl Build Guide](#org47d23c6)
    1.  [Parts List (This is what I spent on parts)](#orgacc8fa1)
        1.  [Retailers](#org9427fbf)
    2.  [Dimensions](#org26c9e26)
    3.  [Step-by-step instructions](#orgc50efc4)
        1.  [Preparation](#org27c9d63)
        2.  [Circuit design](#org55a78dc)
        3.  [Etching](#orgeca5332)
        4.  [Wiring](#org4511828)
        5.  [PCB Layering instructions](#org8a7c506)
        6.  [Firmware guide](#org26c8ff9)



<a id="org47d23c6"></a>

# Updated Dactyl Build Guide


<a id="orgacc8fa1"></a>

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


<a id="org9427fbf"></a>

### Retailers


<a id="org26c9e26"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="orgc50efc4"></a>

## Step-by-step instructions


<a id="org27c9d63"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="org55a78dc"></a>

### Circuit design


<a id="orgeca5332"></a>

### Etching


<a id="org4511828"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="org8a7c506"></a>

### PCB Layering instructions


<a id="org26c8ff9"></a>

### Firmware guide

1.  config.qmk.fm

    -   Under board, choose 'handwired/dactyl'.
    -   Change defaults as necessary.
    -   Click on 'COMPILE'.
    -   Once finised, download the .hex file by clicking 'FIRMWARE'. (Consider saving the keymap.json file for future reference.)
    -   For MacOS & Windows, use the qmk-toolbox application to flash the Teensy 2.0. Follow gui instructions.
    -   For GNU+Linux, use your package manager to search for the teensy-loader-cli
        (or some variation therof) command-line tool. Use the following syntax to
        flash your chosen hex file: '$ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex'

