
# Table of Contents

1.  [Updated Dactyl Build Guide](#orgdbd4573)
    1.  [Parts List (This is what I spent on parts)](#orga74040e)
        1.  [Retailers](#org99c2dc2)
    2.  [Dimensions](#org88d7543)
    3.  [Step-by-step instructions](#org69fec58)
        1.  [Preparation](#orgb80e1c9)
        2.  [Circuit design](#org77f6e1d)
        3.  [Etching](#orge02fa3c)
        4.  [Wiring](#orga452625)
        5.  [PCB Layering instructions](#org34b5bcb)
        6.  [Firmware guide](#org677e7f2)



<a id="orgdbd4573"></a>

# Updated Dactyl Build Guide


<a id="orga74040e"></a>

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


<a id="org99c2dc2"></a>

### Retailers


<a id="org88d7543"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="org69fec58"></a>

## Step-by-step instructions


<a id="orgb80e1c9"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="org77f6e1d"></a>

### Circuit design


<a id="orge02fa3c"></a>

### Etching


<a id="orga452625"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="org34b5bcb"></a>

### PCB Layering instructions


<a id="org677e7f2"></a>

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

