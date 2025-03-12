# ***indie*** - ***in***dependent ***d***ovetail ***i***mplants for ***e***lectrophysiology

Design files and instructions for manufacturing NP1.0, NP2.0alpha, and NP2.0 Neuropixels chronic recording enclosures. 

**Please reach out to us if you want to try this approach, we need your input.** We are actively working on the instructions and trying to find vendors that can print holders reliably.

<img src='images/description.png' width='500'>

These probe enclosures use the dovetail to secure the probes, the design is at the *current limit of the printing resolution of the SLA technology* and for that reason, it is sensitive to the material, and to the washing and curing steps. After printing, the screw hole has to be tapped using a standard 1mm thread tapper.

The NP1.0 holder weights 1.2g, the NP2.0 holder weights 0.57g. All weights include the respective probe, chassis and cap, but no headstage.

# Table of contents
- [Tools list](#tools-list)
- [Parts list (non-printed)](#parts-list-non-printed)
- [Assembly](#assembly)
  - [Printing holders](#printing-holders)
    - [General printing considerations](#general-printing-considerations)
    - [Recommended printer](#recommended-printer)
    - [Printing from STL](#printing-from-stl)
  - [Preparing the printed parts](#preparing-the-printed-parts)
  - [Preparing the probes](#preparing-the-probes)
  - [Mounting and recovering probes](#mounting-and-recovering-probes)

# Tools list

The following lab tools and supplies are required:

| Name  |  Usage      |   Vendor     | 
|-------|--------------|-------------|
| Solder station | Solder wire to probes (if using external ground) | any |
| Fine tipped forceps | Handling probes | any ([example here](https://www.amazon.com/Scientific-Labwares-Precision-Stainless-Straight/dp/B07V3JF6JD/ref=sr_1_4?keywords=fine+tip+forceps&qid=1700025665&sr=8-4)) |
| Small phillips screwdriver (M1) | Secure probe in holder | any | 
| Tap wrench | Tap the plastic holder | any
| M1 tap | Tap the plastic holder | any
| Allen wrench | secure holder to stereotax | any| 
| Stoelting surgical stereotax | stereotaxic surgery | Stoelting (we will soon make stereotax arm attachments for other manufactures)
|Standard rodent surgical toolset | rodent surgery | any| 
| Narshige grinder (optional, but recommended) | probe sharpening | Narshige
|(Optional) Metal cap holder | Hold the probes for cleaning | [IMEC](https://www.neuropixels.org/) (There are different versions for the 1.0 and 2.0 probes, get the correct one for the probes you have)
|(Optional) Thorlabs breadboard, posts and rotating post clamps | Hold probes for washing. (It can be nice to use Thorlabs parts to build a dedicated washing setup to keep surgical rigs unoccupied, but you can also just use your stereotax) | Thorlabs

# Parts list (non-printed)
The following parts are required, not including the 3D printed parts.

| Name  |  Usage      |   Vendor     | 
|-------|--------------|-------------|
| Neuropixels probe (1.0/2.0alpha/2.0) **with metal cap** | record neural activity | [IMEC](https://www.neuropixels.org/) |
| Putty | Temporarily store assembled holders | any
| M1x4 (NP2) or M1x5 (NP1) phillips head screw | secure probe to holder | any
| Bolt (M2, allen key) | stereotax holder, 1x per stereotax arm you plan to use | [Amazon](https://www.amazon.com/Machine-Assorted-Stainless-Assortment-Threaded/dp/B0DFWWFY4Q/ref=sr_1_4?crid=2UCBD7LKSA5SO&dib=eyJ2IjoiMSJ9.eNHLdrJc9lPFJbB2M1D_otWzLYXCDLBKCyQ_V31EDA7siOJkOj9CHxbrd82vGMWiKzanTB4pLcinpIn6ZhEveg10mtvRLkSY-F-6g6sw5p1VZBKMb5nrkJdZkhmVTz5aFlPg6q9OBeEWQFuS0SnWiNbBMR6pGfe90Mv7BW3MsjYeQxkkVDCqbt99_g5Bc91IAjSIfIt5EnJVr-JwgREakpEo0WQ0wsOO980k-tfUlpE.FvCf3cdy6SweoLbAyzSe15mPmmei50MwVvm74pP6g8s&dib_tag=se&keywords=230+Pcs+m2+stainless+steel+screws+nuts+assortment+kit&qid=1733427815&sprefix=230+pcs+m2+stainless+steel+screws+nuts+assortment+kit%2Caps%2C107&sr=8-4)
| Nut (M2) | stereotax holder, 1x per stereotax arm you plan to use | [Amazon](https://www.amazon.com/Machine-Assorted-Stainless-Assortment-Threaded/dp/B0DFWWFY4Q/ref=sr_1_4?crid=2UCBD7LKSA5SO&dib=eyJ2IjoiMSJ9.eNHLdrJc9lPFJbB2M1D_otWzLYXCDLBKCyQ_V31EDA7siOJkOj9CHxbrd82vGMWiKzanTB4pLcinpIn6ZhEveg10mtvRLkSY-F-6g6sw5p1VZBKMb5nrkJdZkhmVTz5aFlPg6q9OBeEWQFuS0SnWiNbBMR6pGfe90Mv7BW3MsjYeQxkkVDCqbt99_g5Bc91IAjSIfIt5EnJVr-JwgREakpEo0WQ0wsOO980k-tfUlpE.FvCf3cdy6SweoLbAyzSe15mPmmei50MwVvm74pP6g8s&dib_tag=se&keywords=230+Pcs+m2+stainless+steel+screws+nuts+assortment+kit&qid=1733427815&sprefix=230+pcs+m2+stainless+steel+screws+nuts+assortment+kit%2Caps%2C107&sr=8-4)
| Fine grit sandpaper (>1000) | Sanding down support attachment points | any
| (Optional) Kapton tape | secure probe and silver wire for soldering | ULine
| Kwik Sil | cover probes and craniotomy during surgery | WPI
|Silver Epoxy|coat grounding wire and ground screw|MG Chemicals 8331D Silver Conductive Epoxy
|  **Bare** silver wire, 0.010 in diameter | grounding, if external grounding is desired | [AM Sytems (Cat. no 782500)](https://www.a-msystems.com/p-756-bare-silver-wire.aspx?srsltid=AfmBOoob5PKCLHF8Wfljej8tYA_QrxX0-WfACrYPfjjLwrkzZmBuAf_l)

# Assembly
There are 7 total steps to using this design for your experiments: 

1. Printing the parts
2. Preparing the holder
3. Prepare the probe(s) (sharpening, soldering)
4. Mounting the probe in the holder
5. Implantation surgery
6. Probe Explantation
7. Probe cleaning

## Printing holders

**You may have to adjust the tolerances depending on the printing and washing protocol you use**, we provide scripts - iLogic - to do this programatically from **Autodesk Inventor 2025** - unfortunately backwards compatibility is not supported. You can get an academic license for Inventor if you work in an academic institution at zero cost.

**Do not implant probes without testing the tolerances.** We tipically print an array of differenet tolerance values to find out the one that fits best, then use that tolerance for all holders. 

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
### General printing considerations
We used a **FormLabs Form 3+ printer** and **GreyPro resin** to develop these protocols, please let us know if you use another printer or resin. *Clear*, and *Rigid 10k*, will NOT work (too brittle). Black V2 also worked in our hands but was not as good. Check [#2](i2) for an alternative material using a commercial vendor ( thanks @wangxuanyu0419 ).

Each version NP1.0, NP2.0 and NP2.0alpha has a folder in the repository. Print using the files in the **stl_exports** folder and using **PreForm** . 

   -  the **main chassis** is printed standing **vertically** and with the **dovetail side facing the mixer**, we tested other orientations, this was the most reliable. Do not use internal supports nor supports in the dovetail rail. This part is very sensitive to the location of the supports and printing orientation.
   - we print the *cap* (with and without headstage)  and the *stereotax holder* parts at an angle with the outer part facing the bottom, no internal supports.

### Included preform files
Under the [Releases Page](https://github.com/spkware/chronic_holder/releases/) we have provided PreForm files with these support structures already defined. We **highly recommend** printing from these files if you can. Just adjust the numbers of each part as needed, but keep the support structures. However, if you need to adjust the designs and print your own, we provide instructions below.


### Printing from STL (creating your own PreForm files)

Tested on PreForm 3.32.0. **Layer tickness 0.050mm** with **GreyPro resin**.

1. Drag the STL file(s), acknowledge *ignore* if it prompts for "issues"
2. The holder chassis needs to be **vertical**. Orient the **dovetail to the mixer side**. On the **orientation** menu: Orient Y by 90 deg, orient Z by 180 (for NP2 and NP2a; NP1 will load already facing the mixer side)
3. On the **supports** menu: remove internal supports, density 0.8, touchpoint size 0.45mm.
4. Click *Auto-generate* supports, then **edit** and remove supports that are in the dovetail. Put the support that is in the entrance of the dovetail closer to the bottom/back side.  
   - TODO: add photo of parts with supports in PreForm
5. Copy-paste after the supports are generated, as many copies as need.

Printing should take <7 h depending on how many parts are being printed. After printing, **wash for 15-20 min** depending on how clean is the isopropyl is, and let dry for at least 4 h (avoid sun light). If the parts feel "sticky" after this drying period, wash for 2 additional minutes. Cure the parts in Form **Cure with the default settings for Grey Pro**. 

## Preparing the printed parts

Once the plastic parts are printed, a few key steps need to be taken to prepare them for use.
1. First, carefully remove the plastic parts from their support structure using forceps and surgical scissors. Care must be taken to not break the small tabs that will hold the flex cable.
2. Sand the support attachment points down with a fine grit sandpaper (grit $\ge$ 1000). This only needs to be done for the main chassis part, but it is important to remove any surface irregularities from the support attachments that could affect how the chassis fits into the stereotax holder.
3. Tap the parts using a standard tap wrench with M1 tap. Be sure to apply a fair amount of forward pressure while tapping, otherwise you may strip the plastic. 
4. Blow out any plastic powder that made its way inside the chassis from the tapping process. 
5. **Test the dovetail mechanism**. Do this with a dummy or a broken probe and ensure that the probe slides along the dovetail socket before trying with a real probe.

### Stereotax arm setup
When setting up the stereotax holder attachment, remove the screw from the end of the Stoelting stereotax arm. Attach the base stereotax arm part (`stereotax_holder_part_1`) with this same screw. Then attach `stereotax_holder_part_2` to part 1 with an M2 nut/bolt. The M2 bolt is loosened and tightened in order to secure and release the chassis during implantation.

## Preparing the probes

1. Sharpen the probes, this reduces resistance when inserting and on mice is often sufficient to puncture the dura, meaning a durotomy is not needed. To sharpen, we use a Narshige grinder set to 70 and sharpen for 5 minutes. Be sure to sharpen the side that does not have the contacts. 

2. Soldering. We have found that it works best to solder the ground and reference together for each probe and then connect these all to one ground screw. The ground screw should not be next to any muscles to minimize artifacts. We have tried using internal reference (where no ground screw is used and instead the tip of the probe is ground) and recordings were lower quality. We recommend using a ground screw. After wrapping the silver wire around the ground screw, we cover it with silver epoxy to ensure solid conduction.

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



These designs are not intended for commercial use or distribution.

Please reach out for feedback.
Max Melin (mmelin@ucla.edu) and Joao Couto (couto@ucla.edu)



