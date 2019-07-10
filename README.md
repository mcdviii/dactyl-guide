
# Table of Contents

1.  [Parts List](#org9b2e26a)
    1.  [Retailers](#orgc56983e)
2.  [Part Dimensions & Other Considerations](#org2c2a70a)
    1.  [Key Switches](#orgd1565c9)
    2.  [Key Caps](#orgfe6465e)
        1.  [Profile:](#orgc58df15)
        2.  [Material:](#orgc55aed2)
3.  [Step-by-step instructions](#org02adc32)
    1.  [Preparation](#org09cc69a)
    2.  [Circuit design](#org86230cd)
    3.  [Notes on Xerox direct-print to Pyralux](#orgc05cd47)
    4.  [Etching](#org248e197)
    5.  [Wiring](#org4ee8049)
        1.  [Prerequisites](#org9aee5b9)
        2.  [Diode position (Row-driven vs. Column-driven )](#org606ade1)
    6.  [PCB Layering instructions](#org05cecf8)
    7.  [Firmware guide](#org0026bf4)
        1.  [config.qmk.fm](#org530d143)



<a id="org9b2e26a"></a>

# Parts List

Things you'll need.

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
<td class="org-right">100.00</td>
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
<td class="org-right">2.00</td>
</tr>
</tbody>

<tbody>
<tr>
<td class="org-left">Key Caps</td>
<td class="org-right">50.00</td>
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
<td class="org-left">Total</td>
<td class="org-right">232.</td>
</tr>
</tbody>
</table>

-   Costs provided are approximations.
    This table represents what I purchased my hartware for. YMMV.
-   You can get switch-dampening o-rings for as little as $2.00 if you're willing
    to wait for them to ship from China.
-   I splurged on my keycaps. Generally you're going to see them on Ali Express at
    around the $50-$60 price point.


<a id="orgc56983e"></a>

## Retailers

-   <https://www.aliexpress.com>
-   <https://www.digikey.com>
-   <https://kbdfans.com>


<a id="org2c2a70a"></a>

# Part Dimensions & Other Considerations

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


<a id="orgd1565c9"></a>

## Key Switches

-   Switch Type: It's best to use SMD (Surface Mount Device) switches. I purchased regular ones
    and ended up clipping all of the little plastic orientation pins off. Not a
    huge deal, but SMD switches are what you want
-   Cherry MX: is the premium key switch brand on the market. I highly recommend
    one of the 9 switch testers you can pick up for about $13.00. Tere are about
    3 steps in variation between no clicks to loud clicks & linear feel to tactile feel.
-   Knockoffs: I've only had experience with Gaterons. They are very much like
    Cherry MXs but have much less of a tactile feel. A good rule of thumb is to get
    the next most tactile model above whatever Cherry MX switch you prefer.


<a id="orgfe6465e"></a>

## Key Caps


<a id="orgc58df15"></a>

### Profile:

If you look at a mechanical keyboard from the side, you'll notice that the tops
of the keys form a curve to allow for better comfort while typing. There are
different styles available out there for this. For the Dactyl, the SA profile
will be the best.

-   OEM:
-   SA:


<a id="orgc55aed2"></a>

### Material:

You'll see two main types of material more than any others: ABS & PBT.

-   ABS: The advantege of ABS is that it's more cost-effective (cheaper).
    The disadvantage is that it fades over time. If you're spending a lot on your
    keycaps and want them to last you should consider this.
-   PBT:


<a id="org02adc32"></a>

# Step-by-step instructions


<a id="org09cc69a"></a>

## Preparation

Use soldering iron to push countersunk screws into plastic shell.
Before wiring, be sure to heatshrink the standoffs to prevent shorts. I found 1/8"
heatshrink tubing works best.


<a id="org86230cd"></a>

## Circuit design


<a id="orgc05cd47"></a>

## Notes on Xerox direct-print to Pyralux


<a id="org248e197"></a>

## Etching


<a id="org4ee8049"></a>

## Wiring


<a id="org9aee5b9"></a>

### TODO Prerequisites

-   How does this work?
-   Key matrix explanation


<a id="org606ade1"></a>

### Diode position (Row-driven vs. Column-driven )

You will need to consider the position of the diodes depending upon how you want
the current from your microcontroller to flow.
For a row-driven keyboard, the cathode ends of the diodes should face away from the switch pin. This
allows the current to flow from the row, through the switch and out through the column.


<a id="org05cecf8"></a>

## PCB Layering instructions


<a id="org0026bf4"></a>

## Firmware guide


<a id="org530d143"></a>

### config.qmk.fm

-   Under board, choose 'handwired/dactyl'.
-   Change defaults as necessary.
-   Click on 'COMPILE'.
-   Once finished, download the .hex file by clicking 'FIRMWARE'. (Consider saving the keymap.json file for future reference.)
-   For MacOS & Windows, use the qmk-toolbox application to flash the Teensy 2.0. Follow gui instructions.
-   For GNU+Linux, use your package manager to search for the teensy-loader-cli
    (or some variation therof) command-line tool. Use the following syntax to
    flash your chosen hex file: `$ teensy-loader-cli -mmcu=atmega32u4 -wv path/to/file.hex`

