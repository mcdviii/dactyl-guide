
# Table of Contents

1.  [Updated Dactyl Build Guide](#org71bf6ed)
    1.  [Parts List (This is what I spent on parts)](#orgc31fcf1)
        1.  [Retailers](#orgb3d3162)
    2.  [Dimensions](#org38a5b97)
    3.  [Step-by-step instructions](#orgd31e664)
        1.  [Preparation](#org76ec012)
        2.  [Circuit design](#orge3907b9)
        3.  [Etching](#orgbe395ee)
        4.  [Wiring](#org06fd733)
        5.  [PCB Layering instructions](#orgba996cb)
        6.  [Firmware guide](#org69b4875)



<a id="org71bf6ed"></a>

# Updated Dactyl Build Guide


<a id="orgc31fcf1"></a>

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


<a id="orgb3d3162"></a>

### Retailers


<a id="org38a5b97"></a>

## Dimensions

-   Screws
-   Standoffs
-   Rubber feet


<a id="orgd31e664"></a>

## Step-by-step instructions


<a id="org76ec012"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="orge3907b9"></a>

### Circuit design


<a id="orgbe395ee"></a>

### Etching


<a id="org06fd733"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    
    Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="orgba996cb"></a>

### PCB Layering instructions


<a id="org69b4875"></a>

### Firmware guide

1.  config.qmk.fm

    -   Under board, choose 'handwired/dactyl'.
    -   Change defaults as necessary.
    -   Click on 'COMPILE'.
    -   Once finised, download the .hex file by clicking 'FIRMWARE'. (Consider saving the keymap.json file for future reference.)
    -   For MacOS & Windows, use the qmk-toolbox application to flash the Teensy 2.0.
    -   Follow gui instructions.
    -   For GNU+Linux, use your package manager to search for the teensy-loader-cli
        (or some variation therof) command-line tool. Use the following syntax to
        flash your chosen hex file: \`$ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex'

