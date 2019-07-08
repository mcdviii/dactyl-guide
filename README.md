
# Table of Contents

1.  [Updated Dactyl Build Guide](#orgecd9f79)
    1.  [Parts List (This is what I spent on parts)](#org7b01345)
        1.  [Retailers](#org2734fde)
    2.  [Dimensions](#org0b907c5)
    3.  [Step-by-step instructions](#orgf40a8c6)
        1.  [Preparation](#org481380b)
        2.  [Circuit design](#org4f69011)
        3.  [Etching](#org5adb96f)
        4.  [Wiring](#orgff64ab8)
        5.  [PCB Layering instructions](#orgd2044b0)
        6.  [Firmware guide](#org033196a)



<a id="orgecd9f79"></a>

# Updated Dactyl Build Guide


<a id="org7b01345"></a>

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


<a id="org2734fde"></a>

### Retailers


<a id="org0b907c5"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="orgf40a8c6"></a>

## Step-by-step instructions


<a id="org481380b"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="org4f69011"></a>

### Circuit design


<a id="org5adb96f"></a>

### Etching


<a id="orgff64ab8"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="orgd2044b0"></a>

### PCB Layering instructions


<a id="org033196a"></a>

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

