# chronic_holder

Design files and instructions for manufacturing NP1.0, NP2.0alpha, and NP2.0 Neuropixels chronic recording enclosures.

**Please reach out to us if you want to try this approach, we need your input.** We are actively working on the instructions and trying to find vendors that can print holders reliably.

<img src='images/description.png' width='500'>

These probe enclosures use the dovetail to secure the probes, the design is at the *current limit of the printing resolution of the SLA technology* and for that reason, it is sensitive to the material, and to the washing and curing steps. After printing, the screw hole has to be tapped using a standard 1mm thread tapper.

The NP1.0 holder weights 1.2g, the NP2.0 holder weights 0.57g. All weights include the respective probe, chassis and cap, but no headstage.

# Table of contents
- [Assembly](#assembly)
  - [Preparing the printed parts](#preparing-the-printed-parts)
  - [Preparing the probes](#preparing-the-probes)
  - [Mounting and recovering probes](#mounting-and-recovering-probes)
  - [Printing holders](#printing-holders)
    - [General printing considerations](#general-printing-considerations)
    - [Recommended printer](#recommended-printer)
    - [Printing from STL](#printing-from-stl)
- [Tools list](#tools-list)
- [Parts list (non-printed)](#parts-list-non-printed)

# Assembly
There are 7 total steps to using this design for your experiments. Documentation is still being added but we will eventually cover them all here. 

1. Printing the parts
2. Preparing the holder
3. Prepare the probe(s) (sharpening, soldering)
4. Mounting the probe in the holder
5. Implantation surgery
6. Probe Explantation
7. Probe cleaning

## Preparing the printed parts

Here we describe how to tap printed parts, check the **printing holders** section for how to get the parts printed.

## Preparing the probes

Sharpening probes makes that there is less resistance when driving probes during insertion and can prevent the need for duroctomies.

Soldering the ground and reference wires are an essential part of preparation to reduce noise. Neuropixels probes are less prone to noise than others because the digitization occurs at the probe. Here we discuss the optimal grounding strategies for using the multiple probes chronically. Some of this knowledge is guided by discussions with *Bill Karsh* (main developer of SpikeGLX) and *Jan Putzeys* (main developper of the acquisition system).

There are many ways of connecting multiple probes and ground to the animal that work, here we present one of them. The probes have 2 soldering points, the **ground** and the **reference**. Ideally we connect the ground **from one of the probes** to the animal (screw in the skull) to ground the animal. The reference from each probe can then be connected together and to a screw in the animal.

Technically, the best configuration separates the ground from the reference, we don't always do this and often connect the ground from one of the probes to the reference of all probes and attach that to a ground screw that is touching the *dura*.

When implanting many probes one can consider using the tip of the probe as reference. NP2.0 allow connecting the tip of 2 probes as reference (2 per headstage).When implanting less than 4 probes we often use the external reference as ground.  

## Mounting and recovering probes

The design uses the "metal cap" (aka dovetail) to guide and secure the probe (through a screw in the rear of the holder). **To use this implant design, we recommend you order the probes denoted "with metal cap" on the IMEC website.** If you already have probes without the metal cap and want to use this design, you can have the metal dovetail machined yourself and then glue it to the probe. We will provide the design files for that part and instructions on how to glue it soon.

To mount probes, insert the probe with the shank first throught the dovetail, drive it all the way with the help of forceps.

**Critical:**
   - The probe should not be wiggling when it reaches the bottom of the holder. The fit should be snug (if the probe wiggles side to side when you move the flex, the dovetail tolerance is too large).
   - Secure the probe with an M1 screw. We will post pictures of how to tap the holder and secure the probe (this should be done before trying to mount the probe in the holder.)
   - Lift the flex, the probe metal cap should be flat in the rail (if the probe is not sitting flat in the dovetail, the tolerance is a bit too large.)


To "recover" do the oposite:
   - release the screw
   - use your thumb in the back of the holder
   - pull the probe by the flex, up the rail until the shank is entirely out,
   - either slide the cap out or rotate the probe down 45 degrees to break the rails.

![picture](images/mounting_recovering.gif)

## Printing holders

**You may have to adjust the tolerances depending on the printing and washing protocol you use**, we provide scripts - iLogic - to do this programatically from **Autodesk Inventor**. You can get an academic license for Inventor if you work in an academic institution at zero cost.

**Do not implant probes without testing the tolerances.** We tipically print an array of differenet tolerance values to find out the one that fits best, then use that tolerance for all holders. 

### General printing considerations
We used a **FormLabs Form 3+ printer** and **GreyPro resin** to develop these protocols, please let us know if you use another printer or resin. *Clear*, and *Rigid 10k*, will NOT work (too brittle). Black V2 also worked in our hands but was not as good. Check [#2](i2) for an alternative material using a commercial vendor ( thanks @wangxuanyu0419 ).

Each version NP1.0, NP2.0 and NP2.0alpha has a folder in the repository. Print using the files in the **stl_exports** folder and using **PreForm** (we will provide files to print directly in the future; for now feel free to reachout to us for these files).

   -  the **main chassis** is printed standing **vertically** and with the **dovetail side facing the mixer**, we tested other orientations, this was the most reliable. Do not use internal supports nor supports in the dovetail rail. This part is very sensitive to the location of the supports and printing orientation.
   - we print the *cap* (with and without headstage)  and the *stereotax holder* parts at an angle with the outer part facing the bottom, no internal supports.

### Recommended printer

| name  |  usage      |   vendor     | cost estimate | 
|-------|--------------|-------------|---------------|
|  [Form 3+](https://formlabs.com/store/3d-printers/form-3-basic-package-without-service/#/package/)| SLA printer  | Formlabs | around 3k (2023) |
| Form Wash | wash parts | Formlabs | around 650 (2023) |
| Form Cure | cure parts | Formlabs | around 750 (2023) |
| [Resin tank]() | 3d printer tank (needs to be replaced from time to time) | Formlabs | around 150 (2023) |
| [Grey Pro resin](https://formlabs.com/store/materials/grey-pro-resin/) | resin to print the holders (needs to be replaced from time to time) | Formlabs | around 200 (2023) |
| [Isopropyl 99%](https://support.formlabs.com/s/article/Isopropyl-Alcohol-IPA) | wash parts | multiple vendors | 150 per gallon |


Read the printer instructions for tricks on how to print, wash and cure. Washing times depend on how clean the isopropyl is and strongly affect the tolerances.

### Printing from STL

Tested on PreForm 3.32.0. **Layer tickness 0.050mm** with **GreyPro resin**.

1. Drag the STL file(s), acknowledge *ignore* if it prompts for "issues"
2. The holder chassis needs to be **vertical**. Orient the **dovetail to the mixer side**. On the **orientation** menu: Orient Y by 90 deg, orient Z by 180 (for NP2 and NP2a; NP1 will load already facing the mixer side)
3. On the **supports** menu: remove internal supports, density 0.8, touchpoint size 0.45mm.
4. Click *Auto-generate* supports, then **edit** and remove supports that are in the dovetail. Put the support that is in the entrance of the dovetail closer to the bottom/back side.  
   - TODO: add photo of parts with supports in PreForm
5. Copy-paste after the supports are generated, as many copies as need.

Printing should take <7 h depending on how many parts are being printed. After printing, **wash for 15-20 min** depending on how clean is the isopropyl is, and let dry for at least 4 h (avoid sun light). If the parts feel "sticky" after this drying period, wash for 2 additional minutes. Cure the parts in Form **Cure with the default settings for Grey Pro**. 


# Tools list

The following lab tools are required to assemble and implant a probe holder: 

| name  |  usage      |   vendor     | 
|-------|--------------|-------------|
| Solder station | Solder wire to probes (if using external ground) | any |
| Fine tipped forceps | Handling probes | any ([example here](https://www.amazon.com/Scientific-Labwares-Precision-Stainless-Straight/dp/B07V3JF6JD/ref=sr_1_4?keywords=fine+tip+forceps&qid=1700025665&sr=8-4)) |
| Small phillips screwdriver (M1) | Secure probe in holder | any | 
| Tap wrench | Tap the plastic holder | any
| M1 tap | Tap the plastic holder | any
| Hex key (todo, add size) | secure holder to stereotax | any| 
| Putty | Temporarily store assembled holders | todo: link
| Kopf surgical stereotax | stereotaxic surgery | Kopf (we will soon make stereotax arm attachments for other manufactures)
|Standard rodent surgical toolset | rodent surgery | any| 
|(Optional) Metal cap holder | Hold the probes for cleaning | [IMEC](https://www.neuropixels.org/) (There are different versions for the 1.0 and 2.0 probes, get the correct one for the probes you have)
|(Optional) Thorlabs breadboard, posts and rotating post clamps | Hold probes for washing. (It can be nice to use Thorlabs parts to build a dedicated washing setup to keep surgical rigs unoccupied, but you can also just use your stereotax) | Thorlabs




# Additional parts list (non-printed)
The following parts are also required to assemble and implant one probe, not including the 3D printed parts.

| name  |  usage      |   vendor     | 
|-------|--------------|-------------|
| Neuropixels probe (1.0/2.0alpha/2.0) **with metal cap** | record neural activity | [IMEC](https://www.neuropixels.org/) |
| M1x4 (NP2) or M1x5 (NP1) phillips head screw | secure probe to holder | any
| Nut (TODO, add size) | stereotax holder | any
| Bolt (TODO, add size) | stereotax holder | any
| (Optional) Kapton tape | secure probe and silver wire for soldering | TODO
| (Optional) Silver wire | grounding, if external grounding is desired | TODO

These designs are not intended for commercial use or distribution.

Please reach out for feedback.
Max Melin (mmelin@ucla.edu) and Joao Couto (couto@ucla.edu)




