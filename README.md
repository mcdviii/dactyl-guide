
# Table of Contents

1.  [Updated Dactyl Build Guide](#orgd94b6e6)
    1.  [Parts List (This is what I spent on parts)](#orgada80f7)
        1.  [Retailers](#org77de59a)
    2.  [Dimensions](#org5e0b960)
    3.  [Step-by-step instructions](#org6b8fdec)
        1.  [Preparation](#org39574c5)
        2.  [Circuit design](#orgc491d32)
        3.  [Etching](#orgd622f82)
        4.  [Wiring](#org7203a6a)
        5.  [PCB Layering instructions](#org457844c)
        6.  [Firmware guide](#orge0237da)



<a id="orgd94b6e6"></a>

# Updated Dactyl Build Guide


<a id="orgada80f7"></a>

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


<a id="org77de59a"></a>

### Retailers


<a id="org5e0b960"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="org6b8fdec"></a>

## Step-by-step instructions


<a id="org39574c5"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="orgc491d32"></a>

### Circuit design


<a id="orgd622f82"></a>

### Etching


<a id="org7203a6a"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="org457844c"></a>

### PCB Layering instructions


<a id="orge0237da"></a>

### Firmware guide

1.  config.qmk.fm

    -   Under board, choose 'handwired/dactyl'.
    -   Change defaults as necessary.
    -   Click on 'COMPILE'.
    -   Once finished, download the .hex file by clicking 'FIRMWARE'. (Consider saving the keymap.json file for future reference.)
    -   For MacOS & Windows, use the qmk-toolbox application to flash the Teensy 2.0. Follow gui instructions.
    -   For GNU+Linux, use your package manager to search for the teensy-loader-cli
        (or some variation therof) command-line tool. Use the following syntax to
<<<<<<< HEAD
        flash your chosen hex file: `$ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex\`
=======
        flash your chosen hex file: `$ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex`
>>>>>>> origin/master

