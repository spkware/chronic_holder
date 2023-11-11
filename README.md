# chronic_holder

Design files and instructions for manufacturing NP1.0, NP2.0alpha, and NP2.0 Neuropixels chronic recording enclosures.

**Please reach out to us if you want to try this approach, we need your input.** We are actively working on the instructions and trying to find vendors that can print holders reliably.

<img src='images/description.png' width='500'>

These probe enclosures use the dovetail to secure the probes, the design is at the *current limit of the printing resolution of the SLA technology* and for that reason, it is sensitive to the material, and to the washing and curing steps. After printing, the screw hole has to be taped using a standard 1mm taper.

The NP 1.0 holder weights 1.2g, the NP2.0 holder weights 0.57g. All weights include the respective probe, chassis and cap without headstage.

## Printing holders

**You may have to adjust the tolerances depending on the printing and washing protocol you use**, we provide scripts - iLogic - to do this programatically from **Autodesk Inventor**. You can get an academic license for Inventor if you work in an academic institution at zero cost.

**Do not implant probes without testing the tolerances.** We tipically print an array of differenet tolerance values to find out the one that fits best, then use that tolerance for all holders. 

We used a **FormLabs Form 3+ printer** and **GreyPro resin** to develop these protocols, please let us know if you use another printer or resin. *Clear*, and *Rigid 10k*, will NOT work (too brittle). Black V2 also worked in our hands but was not as good.

Each version NP1.0, NP2.0 and NP2.0alpha has a folder in the repository. Print using the files in the **stl_exports** folder and using **PreForm** (we will provide files to print directly in the future; for now feel free to reachout to us for these files).

   -  the **main chassis** is printed standing **vertically** and with the **dovetail side facing the mixer**, we tested other orientations, this was the most reliable. Do not use internal supports nor supports in the dovetail rail. This part is very sensitive to the location of the supports and printing orientation.
   - we print the *cap* (with and without headstage)  and the *stereotax holder* parts at an angle with the outer part facing the bottom, no internal supports.

###Recommended printer

| name  |  usage      |   vendor     | cost estimate | 
|-------|--------------|-------------|---------------|
|  [Form 3+](https://formlabs.com/store/3d-printers/form-3-basic-package-without-service/#/package/)| SLA printer  | Formlabs | around 3k (2023) |
| Form Wash | wash parts | Formlabs | around 650 (2023) |
| Form Cure | cure parts | Formlabs | around 750 (2023) |
| [Resin tank]() | 3d printer tank (needs to be replaced from time to time) | Formlabs | around 150 (2023) |
| [Grey Pro resin](https://formlabs.com/store/materials/grey-pro-resin/) | resin to print the holders (needs to be replaced from time to time) | Formlabs | around 200 (2023) |
| [Isopropyl 99%](https://support.formlabs.com/s/article/Isopropyl-Alcohol-IPA) | wash parts | multiple vendors | 150 per gallon |


Read the printer instructions for tricks on how to print, wash and cure. Washing times depend on how clean the isopropyl is and strongly affect the tolerances.

### Print from STL

Tested on PreForm 3.30.0. **Layer tickness 0.050mm** with **GreyPro resin**.

1. Drag the STL file(s), acknowledge *ignore* if it prompts for "issues"
2. The holder needs to be **vertical**. Orient the **dovetail to the mixer side**. On the **orientation** menu: Orient Y by 90 deg, orient Z by 180 (for NP2 and NP2a; NP1 will load already facing the mixer side)
3. On the **supports** menu: remove internal supports, density 0.8, touchpoint size 0.45mm.
4. Click *Auto-generate* supports, then **edit** and remove supports that are in the dovetail. Put the support that is in the entrance of the dovetail closer to the bottom/back side.  
5. Copy-paste after the supports are generated, as many copies as need.

Printing should take 7 h depending on how many parts are being printed. After printing, **wash for 15-20 min** depending on how clean is the isopropyl and let dry for at least 4 h (avoid sun light). If it is sticky after washing, give it 2 more minutes. Cure the parts in Form **Cure with the default settings for Grey Pro**. 

## Mounting probes

Slide the probe in the chassis and screw tightly. 


## Tools list

The following lab tools are required to assemble and implant a probe holder.

- solder station
- forceps (for probe handling)
- small phillips screwdriver
- hex key (TODO: add size)
- putty to hold probes when not in use (link)
- Kopf surgical stereotax (we will soon make stereotax arm attachments for other manufactures) TODO: more stereotax details?
- Standard rodent surgical tool set
- Thorlabs posts and connectors are helpful for washing probes, but using the sterotax is also fine if not needed for other surgeries
- The Imec acute recording post (the one that's meant to go with the dovetail) is also helpful for washing the probes
- Tap Wrench
- Size M1 tap

If 3D printing parts in-house:
- 

## Parts list (non-printed)
The following parts are required to assemble and implante one probe holder. (requirements are the same for all probe versions).
- 1x Neuropixels 1.0/2.0/2.0alpha probe (with metal cap. Metal caps (dovetails) can also be glued on in house, but alignment may not be as good.)
- 1x set screw (TODO: M1x3 or M1x4?)
- 1x nut (TODO: details for stereotax nut)
- 1x bolt (TODO: details for stereotax stereotax bolt)
- silver wire (TODO: link)
- Kapton tape (thin, for soldering ground wire)





