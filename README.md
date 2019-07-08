
# Table of Contents

1.  [Updated Dactyl Build Guide](#org0bd6be6)
    1.  [Parts List (This is what I spent on parts)](#org77ce1fc)
        1.  [Retailers](#orgc3d919a)
    2.  [Part Dimensions & Other Considerations](#orgd7f51d8)
        1.  [Key Switches](#org4cd663a)
        2.  [Key Caps](#org22bbf0b)
    3.  [Step-by-step instructions](#orga32f3f2)
        1.  [Preparation](#orged47b6d)
        2.  [Circuit design](#org3a70ffd)
        3.  [Notes on Xerox direct-print to Pyralux](#org41a6b61)
        4.  [Etching](#orgfa58449)
        5.  [Wiring](#org8560bf8)
        6.  [PCB Layering instructions](#org968141e)
        7.  [Firmware guide](#org36f3c24)



<a id="org0bd6be6"></a>

# Updated Dactyl Build Guide


<a id="org77ce1fc"></a>

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
<td class="org-left">70ct Key Switches</td>
<td class="org-right">50.00</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Rubber O-Rings for Switches</td>
<td class="org-right">7.00</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Key Caps</td>
<td class="org-right">83.00</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Pyralux (Flexible copper for PCB)</td>
<td class="org-right">30.00</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">&#xa0;</td>
<td class="org-right">total([])</td>
</tr>


<tr>
<td class="org-left">&#xa0;</td>
<td class="org-right">&#xa0;</td>
</tr>
</tbody>
</table>

-   Price considerations
    This table represents what I purchased my hartware for. YMMV.
-   You can get switch-dampening o-rings for as little as $2.00 if you're willing
    to wait for them to ship from China.
-   I splurged on my keycaps. Generally you're going to see them on Ali Express at
    around the $50-$60 price point.


<a id="orgc3d919a"></a>

### Retailers

<https://www.aliexpress.com>
<https://www.digikey.com>
<https://www.kbdfans.com>


<a id="orgd7f51d8"></a>

## Part Dimensions & Other Considerations

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Part:</th>
<th scope="col" class="org-left">Dimension or special consideration:</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Screws</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Standoffs</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Rubber feet</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>
</table>


<a id="org4cd663a"></a>

### Key Switches

-   Switch Type: It's best to use SMD (Surface Mount Device) switches. I purchased regular ones
    and ended up clipping all of the little plastic orientation pins off. Not a
    huge deal, but SMD switches are what you want
-   Cherry MX: is the premium key switch brand on the market. I highly recommend
    one of the 9 switch testers you can pick up for about $13.00. Tere are about
    3 steps in variation between no clicks to loud clicks & linear feel to tactile feel.
-   Knockoffs: I've only had experience with Gaterons. They are very much like
    Cherry MXs but have much less of a tactile feel. A good rule of thumb is to get
    the next most tactile model above whatever Cherry MX switch you prefer.


<a id="org22bbf0b"></a>

### Key Caps

1.  Profile:

    If you look at a mechanical keyboard from the side, you'll notice that the tops
    of the keys form a curve to allow for better comfort while typing. There are
    different styles available out there for this. For the Dactyl, the SA profile
    will be the best.
    
    -   OEM:
    -   SA:

2.  Material:

    You'll see two main types of material more than any others: ABS & PBT.
    
    -   ABS: The advantege of ABS is that it's more cost-effective (cheaper).
        The disadvantage is that it fades over time. If you're spending a lot on your
        keycaps and want them to last you should consider this.
    -   PBT:


<a id="orga32f3f2"></a>

## Step-by-step instructions


<a id="orged47b6d"></a>

### Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="org3a70ffd"></a>

### Circuit design


<a id="org41a6b61"></a>

### Notes on Xerox direct-print to Pyralux


<a id="orgfa58449"></a>

### Etching


<a id="org8560bf8"></a>

### Wiring

1.  TODO Prerequisites

    -   How does this work?
    -   Key matrix explanation

2.  Diode position (Row-driven vs. Column-driven )

    You will need to consider the position of the diodes depending upon how you want
    the current from your microcontroller to flow.
    For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
    allows the current to flow from the row, through the switch and out through the column.


<a id="org968141e"></a>

### PCB Layering instructions


<a id="org36f3c24"></a>

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

