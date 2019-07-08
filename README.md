
# Table of Contents

1.  [Updated Dactyl Build Guide](#org6e0df76)
    1.  [Parts List (This is what I spent on parts)](#org4e6c1ee)
        1.  [Retailers](#orgfbfddd7)
    2.  [Dimensions](#org833d8cf)
    3.  [Step-by-step instructions](#org106a232)
        1.  [Preparation](#org6c49199)
        2.  [Circuit design](#org653064e)
        3.  [Etching](#org45ac46a)
        4.  [Wiring](#org12494c4)
        5.  [PCB Layering instructions](#orgbd2ee03)
        6.  [Firmware guide](#orgf42ce46)



<a id="org6e0df76"></a>

# Updated Dactyl Build Guide


<a id="org4e6c1ee"></a>

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


<a id="orgfbfddd7"></a>

### Retailers


<a id="org833d8cf"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="org106a232"></a>

## Step-by-step instructions


<a id="org6c49199"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="org653064e"></a>

### Circuit design


<a id="org45ac46a"></a>

### Etching


<a id="org12494c4"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="orgbd2ee03"></a>

### PCB Layering instructions


<a id="orgf42ce46"></a>

### Firmware guide

1.  config.qmk.fm

    -   Under board, choose 'handwired/dactyl'.
    -   Change defaults as necessary.
    -   Click on 'COMPILE'.
    -   Once finished, download the .hex file by clicking 'FIRMWARE'. (Consider saving the keymap.json file for future reference.)
    -   For MacOS & Windows, use the qmk-toolbox application to flash the Teensy 2.0. Follow gui instructions.
    -   For GNU+Linux, use your package manager to search for the teensy-loader-cli
        (or some variation therof) command-line tool. Use the following syntax to
        flash your chosen hex file: `$ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex'

