
# Table of Contents

1.  [Updated Dactyl Build Guide](#orgd0b9c57)
    1.  [Parts List (This is what I spent on parts)](#orgba7d88f)
        1.  [Retailers](#orgd01169f)
    2.  [Dimensions](#org3e4dd9f)
    3.  [Step-by-step instructions](#org667310f)
        1.  [Preparation](#org4ca9604)
        2.  [Circuit design](#org4a568b1)
        3.  [Etching](#org0f42c42)
        4.  [Wiring](#orgbb15c34)
        5.  [PCB Layering instructions](#orgbea05a3)
        6.  [Firmware guide](#orgcd026aa)



<a id="orgd0b9c57"></a>

# Updated Dactyl Build Guide


<a id="orgba7d88f"></a>

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


<a id="orgd01169f"></a>

### Retailers


<a id="org3e4dd9f"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="org667310f"></a>

## Step-by-step instructions


<a id="org4ca9604"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="org4a568b1"></a>

### Circuit design


<a id="org0f42c42"></a>

### Etching


<a id="orgbb15c34"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="orgbea05a3"></a>

### PCB Layering instructions


<a id="orgcd026aa"></a>

### Firmware guide

1.  config.qmk.fm

    -   Under board, choose 'handwired/dactyl'.
    -   Change defaults as necessary.
    -   Click on 'COMPILE'.
    -   Once finished, download the .hex file by clicking 'FIRMWARE'. (Consider saving the keymap.json file for future reference.)
    -   For MacOS & Windows, use the qmk-toolbox application to flash the Teensy 2.0. Follow gui instructions.
    -   For GNU+Linux, use your package manager to search for the teensy-loader-cli
        (or some variation therof) command-line tool. Use the following syntax to
        flash your chosen hex file: \`$ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex\`

