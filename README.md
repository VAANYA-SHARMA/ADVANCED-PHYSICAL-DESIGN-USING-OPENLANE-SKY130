# ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130
This is a workshop which is about ASIC design using OPEN source tools.
## Advanced Physical Design- OpenLANE\Sky130
![Screenshot 2024-03-19 195759](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/9e3eb63d-d8ec-4051-96e3-3a3a06a7a540)
<br>

Course -  Advanced Physical Design Using OpenLANE/SKY130 offered by VSDIAT
<br> Author - VAANYA SHARMA

<br> ## <br> *WORKSHOP DAY WISE CONTENT* 
Contents -:
* [SKY130 Day 1: Inception of OpenSource EDA, OpenLANE and SKY130 PDK](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#sky130-day-1-inception-of-opensource-eda-openlane-and-sky130-pdk)
    - [How to Talk to Computers](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-how-to-talk-to-computers)
        + [Introduction to QFN - 48 package, chip, pads, core, die and IPs](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-introduction-to-qfn---48-package-chip-pads-core-die-and-ips)
        + [Introduction to RISC V]()
        + [From Software Applications to Hardware](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#from-software-applications-to-hardware)
    - [SoC Design and OpenLANE](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#soc-design-and-openlane)
        + [Introduction to Components of Opensource Digital ASIC Design](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#introduction-to-components-of-opensource-digital-asic-design)
        + [Simplified RTL to GDS flow](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#simplified-rtl-to-gds-flow)
        + [Introduction to OpenLANE and Strive Chipsets](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#introduction-to-openlane-and-strive-chipsets)
        + [Introduction to OpenLANE detailed ASIC Design Flow](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#introduction-to-openlane-detailed-asic-design-flow)
    - [Get Familiar to Opensource EDA tools](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#get-familiar-to-opensource-eda-tools)
        + [OpenLANE Directory Structure in Detail](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#openlane-directory-structure-in-detail)
        + [Design Preparation Step](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#design-preparation-step)
        + [Review Files After Design Prep and Run Synthesis](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#review-files-after-design-prep-and-run-synthesis)
        + [Steps to Characterise Synthesis Results](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%201.md#steps-to-charecterise-synthesis-results)        
* [SKY130 Day 2: Good vs Bad Floorplan and Introduction to Library Cells](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#sky130-day-2-good-vs-bad-floorplan-and-introduction-to-library-cells)
    - [Chip Floor Planning Considerations](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#chip-floor-planning-considerations)
        + [Utilisation Factor and Aspect Ratio](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#utilisation-factor-and-aspect-ratio)
        + [Concept of Pre-Placed Cells](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#concept-of-pre-placed-cells)
        + [De-Coupling Capacitors](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#de-coupling-capacitors)
        + [Power Planning](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#power-planning)
        + [Pin Placement and Logical Cell Placement Blockage](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#pin-placement-and-logical-cell-placement-blockage)
        + [Steps to Run Floorplan Using OpenLANE](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#steps-to-run-floorplan-using-openlane)
        + [Review Floorplan Files and Steps to Review Floorplan](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#review-floorplan-files-and-steps-to-review-floorplan)
        + [Review Floorplan Layout in Magic](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#review-floorplan-layout-in-magic)
     - [Library Binding and Placement](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#library-binding-and-placement)
        + [Netlist Binding and Initial Place Design](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#netlist-binding-and-initial-place-design)
        + [Optimise Placement Using Estimated Wire-Length and Capacitance](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#optimise-placement-using-estimated-wire-length-and-capacitance)
        + [Final Placement Optimization](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#final-placement-optimization)
        + [Need for Libraries and Characterisation](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#need-for-libraries-and-characterisation)
        + [Congestion Aware Placement Using RePLACE](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#congestion-aware-placement-using-replace)
    - [Cell Design and Characterisation Flows](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#cell-design-and-characterisation-flows)
        + [Inputs for Cell Design Flow](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#inputs-for-cell-design-flow-and-circuit-and-layout-design-step)
        + [Circuit Design Step](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#inputs-for-cell-design-flow-and-circuit-and-layout-design-step)
        + [Layout Design Step](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#inputs-for-cell-design-flow-and-circuit-and-layout-design-step)
        + [Typical Characterisation Flow](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#typical-characterisation-flow)
     - [General Timing Characterisation Parameters](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#general-timing-characterisation-parameters)
        + [Timing Threshhold Definitions](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#timing-threshhold-definitions)
        + [Propogation Delay and Transition Time](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%202.md#propogation-delay-and-transition-time)     
* [SKY130 DAY 3: Design Library Cell Using Magic Layout and NGSPICE characterisation](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#sky130-day-3-design-library-cell-using-magic-layout-and-ngspice-characterisation)
     - [Labs for CMOS Inverter NGSPICE Simulations](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#labs-for-cmos-inverter-ngspice-simulations)
        + [IO Placer Revision](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#io-placer-revision)
        + [SPICE Deck Creation For CMOS Inverter](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#spice-deck-creation-for-cmos-inverter)
        + [SPICE Simulation Lab for CMOS Inverter](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#spice-simulation-lab-for-cmos-inverter)
        + [Switching Threshhold Vm](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#switching-threshhold-vm)
        + [Static and Dynamic Simulation of CMOS Inverter](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#static-and-dynamic-simulation-of-cmos-inverter)
        + [Lab Steps to GitClone VSDSTD Cell Design](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-steps-to-gitclone-vsdstd-cell-design)
     - [Inception of Layout Â CMOS Fabrication Process](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#inception-of-layout-%C3%A2-cmos-fabrication-process)
        + [Create Active Regions](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#create-active-regions)
        + [Formation of N and P well](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#formation-of-n-and-p-well)
        + [Formation of Gate Terminal](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#formation-of-gate-terminal)
        + [Lightly Doped Drain [LDD] Formation](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lightly-doped-drain-ldd-formation)
        + [Source Â Drain Formation](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#source-%C3%A2-drain-formation)
        + [Local Interconnect Formation](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#local-interconnect-formation)
        + [Higher Level Metal Formation](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#higher-level-metal-formation)
        + [Lab Introduction to SKY130 Basic Layers Layout and LEF using Inverter](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-introduction-to-sky130-basic-layers-layout-and-lef-using-inverter)
        + [Lab Steps to Create STD Cell Layout and Extract SPICE Netlist](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-steps-to-create-std-cell-layout-and-extract-spice-netlist)
     - [SKY130 Tech File Labs](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#sky130-tech-file-labs)
        + [Lab Steps To Create Final SPICE deck using SKY130 tech](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-steps-to-create-final-spice-deak-using-sky130-tech)
        + [Lab Steps to Characterise Inverter using SKY130 Model Files](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-steps-to-characterise-inverter-using-sky130-model-files)
        + [Lab Introduction to SKY130 PDKs And Steps to Download Labs](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-introduction-to-sky130-pdks-and-steps-to-download-labs)
        + [Lab Introduction to Magic Tool Options and DRC Rules](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-introduction-to-magic-tool-options-and-drc-rules)
        + [Lab Introduction to Magic and Steps to Load SKY130 Tech Rules](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-introduction-to-magic-and-steps-to-load-sky130-tech-rules)
        + [Lab Excercise to Fix **poly.9** error in SKY130 Tech-File](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-excercise-to-fix-poly9-error-in-sky130-tech-file)
        + [Lab Excercise to Implement Poly-Resistor Spacing to Diff and Tap](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%203.md#lab-excercise-to-implement-poly-resistor-spacing-to-diff-and-tap)
* [SKY130 DAY 4 : Pre-Layout Timing Analysis and Importance of Good Clock Tree](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#sky130-day-4--pre-layout-timing-analysis-and-importance-of-good-clock-tree)
     - [Timing Modelling Using Delay Tables](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#timing-modelling-using-delay-tables)
        + [Lab Steps To Convert Grid Information Into Track Information](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-convert-grid-information-into-track-information)
        + [Lab Steps to Convert Magic Layout to STD Cell LEF](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-convert-magic-layout-to-std-cell-lef)
        + [Introduction of Timing **libs** and Steps To Include New Cell in Synthesis](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#introduction-of-timing-libs-and-steps-to-include-new-cell-in-synthesis)
        + [Delay Tables](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#delay-tables)
        + [Lab Steps To Configure Synthesis Settings to Fix Slack and Include VSDINV](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-configure-synthesis-settings-to-fix-slack-and-include-vsdinv)
     - [Timing Analysis With Ideal Clocks Using Open STA](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#timing-analysis-with-ideal-clocks-using-open-sta)
        + [Setup Timing Analysis And Introduction to Flip-Flop Setup Time](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#setup-timing-analysis-and-introduction-to-flip-flop-setup-time)
        + [Introduction to Clock Jitter and Uncertainty](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#introduction-to-clock-jitter-and-uncertainty)
        + [Lab Steps to Configure OpenSTA for Post-Synth Timings Analysis](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-configure-opensta-for-post-synth-timings-analysis)
        + [Lab Steps to Optimize Synthesis to Reduce Setup Violations](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-optimize-synthesis-to-reduce-setup-violations)
        + [Lab Steps to do Basic Timing ECO](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-do-basic-timing-eco)
     - [Clock Tree Synthesis TritonCTS and Signal Integrity](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#clock-tree-synthesis-tritoncts-and-signal-integrity)
        + [Clock Tree Routing and Buffering Using H-Tree Algorithm](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#clock-tree-routing-and-buffering-using-h-tree-algorithm)
        + [Crosswalk and Clock Net Shielding](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#crosswalk-and-clock-net-shielding)
        + [Lab Steps to run CTS using TritonCTS](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-run-cts-using-tritoncts)
        + [Lab Steps to Verify CTS Runs](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-verify-cts-runs)
     - [Timing Analysis  With Real Clocks Using Open STA](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#timing-analysis--with-real-clocks-using-open-sta)
        + [Setup Timing Analysis Using Real Clocks](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#setup-timing-analysis-using-real-clocks)
        + [Lab Steps to Analyse Timing With Real Clocks Using OpenSTA](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#setup-timing-analysis-using-real-clocks)
        + [Lab Steps to Excecute OpenSTA With Right Timing Libraries and CTS Assignment](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-excecute-opensta-with-right-timing-libraries-and-cts-assignment)
        + [Lab Steps to Observe Impact of Bigger CTS Buffers On Setup And Hold Timing](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%204.md#lab-steps-to-observe-impact-of-bigger-cts-buffers-on-setup-and-hold-timing)
* [SKY130 DAY 5: Final Steps For RTL2GDS Using TritonRoute and OpenSTA](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#sky130-day-5-final-steps-for-rtl2gds-using-tritonroute-and-opensta)
     - [Routing and Design Check [DRC]](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#routing-and-design-check-drc)
        + [Introduction to Maze Routing and Lee's Algorithm](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#introduction-to-maze-routing-and-lees-algorithm)
        + [Lee's Algorithm Conclusion](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#lees-algorithm-conclusion)
        + [Design Rule Check](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#design-rule-check)
     - [Power Distribution Network and Routing](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#power-distribution-network-and-routing)
        + [Lab Steps To Build Power Distribution Network](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#lab-steps-to-build-power-distribution-network)
        + [Lab Steps From Power Straps To STD Cell Power](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#lab-steps-from-power-straps-to-std-cell-power)
        + [Basics of Global and Detail Routing and Configure TritonRoute](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#basics-of-global-and-detail-routing-and-configure-tritonroute)
     - [TritonRoute Features](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#tritonroute-features)
        + [TritonRoute Feature 1 - Honors Pre-processed Route Guides](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#tritonroute-feature-1---honors-pre-processed-route-guides)
        + [TritonRoute Feature 2 & 3 - Inter-Guide Connectivity and Intra & Inter Layer Routing](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#tritonroute-feature-2--3---inter-guide-connectivity-and-intra--inter-layer-routing)
        + [TritonRoute Method To Handle Connectivity](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#tritonroute-method-to-handle-connectivity)
        + [Routing Topology Algorithm and Final Files List Post Route](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/DAY%205.md#routing-topology-algorithm-and-final-files-list-post-route)
* [Bibliography and Acknowledgements](https://github.com/ojasvi-shah/Advanced-Physical-Design-Using-OpenLANE--Ojasvi-Shah/blob/main/Bibliography%20and%20Acknowledgements.md)

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
####### Normal Text (Not a heading, just plain text)

This is normal text without any `#`.

**Bold Text**  
*Italic Text*  
~~Strikethrough~~  
[Clickable Link](https://example.com)



