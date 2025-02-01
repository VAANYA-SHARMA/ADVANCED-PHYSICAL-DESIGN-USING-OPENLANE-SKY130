# ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130
This is a workshop which is about ASIC design using OPEN source tools.
## Advanced Physical Design- OpenLANE\Sky130
![Screenshot 2024-03-19 195759](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/9e3eb63d-d8ec-4051-96e3-3a3a06a7a540)
<br>

Course -  Advanced Physical Design Using OpenLANE/SKY130 offered by VSDIAT
<br> Author - VAANYA SHARMA
## <br> *WORKSHOP DAY WISE CONTENT* 
Contents -:
* [SKY130 Day 1: Inception of OpenSource EDA, OpenLANE and SKY130 PDK](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#sky130-day-1-inception-of-opensource-eda-openlane-and-sky130-pdk)
    - [How to Talk to Computers](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-how-to-talk-to-computers)
        + [Introduction to QFN - 48 package, chip, pads, core, die and IPs](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-introduction-to-qfn---48-package-chip-pads-core-die-and-ips)
        + [Introduction to RISC V](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#---introduction-to-risc-v)
        + [From Software Applications to Hardware](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#--from-software-applications-to-hardware)
    - [SoC Design and OpenLANE](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-soc-design-and-openlane)
        + [Introduction to Components of Opensource Digital ASIC Design](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-introduction-to-all-components-of-opensource-digital-asic-design)
        + [Simplified RTL to GDS flow](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-simplified-rtl-to-gdsii-flow)
        + [Introduction to OpenLANE and Strive Chipsets](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-introduction-to-openlane-and-strive-chipsets)
        + [Introduction to OpenLANE detailed ASIC Design Flow](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-introduction-to-openlane-detailed-asic-design-flow)
    - [Get Familiar to Opensource EDA tools](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-get-familiar-to-open-source-eda-tools)
        + [OpenLANE Directory Structure in Detail](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-openlane-directory-structure-in-detail)
        + [Design Preparation Step](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-design-preparation-step)
        + [Review Files After Design Prep and Run Synthesis](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-review-files-after-design-prep-and-run-synthesis)
        + [Steps to Characterise Synthesis Results](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%201.md#-steps-to-characterise-synthesis-results)        
* [SKY130 Day 2: Good vs Bad Floorplan and Introduction to Library Cells](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#sky130-day-2-good-vs-bad-floorplan-and-introduction-to-library-cells)
    - [Chip Floor Planning Considerations](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#-chip-floor-planning-considerations)
        + [Utilisation Factor and Aspect Ratio](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#-utilisation-factor-and-aspect-ratio)
        + [Concept of Pre-Placed Cells](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#-concept-of-pre-placed-cells)
        + [De-Coupling Capacitors](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#-de-coupling-capacitors)
        + [Power Planning](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#-power-planning)
        + [Pin Placement and Logical Cell Placement Blockage](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#-pin-placement-and-logical-cell-placement-blockage)
        + [Steps to Run Floorplan Using OpenLANE](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#steps-to-run-floorplan-using-openlane)
     - [Library Binding and Placement](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#-library-binding-and-placement)
        + [Netlist Binding and Initial Place Design](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#netlist-binding-and-initial-place-design)
        + [Optimise Placement Using Estimated Wire-Length and Capacitance](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/1eafddd3d74d3fbdf351d03f7e8ff2a5138b4b6c/DAY%202.md#optimize-placement-using-estimated-wire-length-and-capacitance)
      
    - [Cell Design and Characterization Flow](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/edit/main/DAY%202.md#-cell-design-and-characterization-flows)
        + [Cell Design Flow](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/edit/main/DAY%202.md#cell-design-flow)
       
* [SKY130 DAY 3: Design Library Cell Using Magic Layout and NGSPICE characterisation](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/0018c9048084024be815bf951f795ee8fda2f840/DAY%203.md#day-3---design-and-characterize-one-library-cell-using-magic-layout-tool-and-ngspice)
     - [Labs for CMOS Inverter NGSPICE Simulations](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/0018c9048084024be815bf951f795ee8fda2f840/DAY%203.md#--labs-for-cmos-inverter-ngspice-simulations)
        
     - [Inception of Layout Â CMOS Fabrication Process](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/0018c9048084024be815bf951f795ee8fda2f840/DAY%203.md#-inception-of-layout--cmos-fabrication-process)
        
     - [SKY130 Tech File Labs](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/0018c9048084024be815bf951f795ee8fda2f840/DAY%203.md#sky130-tech-file-labs)
        + [Lab Steps To Create Final SPICE deck using SKY130 tech](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/0018c9048084024be815bf951f795ee8fda2f840/DAY%203.md#lab-steps-to-create-final-spice-deck-using-sky130-tech)
        
* [SKY130 DAY 4 : Pre-Layout Timing Analysis and Importance of Good Clock Tree](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/5d527c41a8b6b1779b01dd9a197950fff26883ac/DAY%204.md#day-4----pre-layout-timing-analysis-and-importance-of-good-clock-tree)
     - [Timing Modelling Using Delay Tables](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/5d527c41a8b6b1779b01dd9a197950fff26883ac/DAY%204.md#-timing-modelling-using-delay-tables)
        + [Lab Steps To Convert Grid Information Into Track Information](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%204.md#-lab-steps-to-convert-grid-info-to-track-info)
        + [Lab Steps to Convert Magic Layout to STD Cell LEF](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%204.md#-lab-steps-to-convert-magic-layout-to-std-cell-lef)
      
          
* [SKY130 DAY 5: Final Steps For RTL2GDS Using TritonRoute and OpenSTA](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%205.md#day-5---final-steps-to-rtl2gds-using-tritonroute-and-opensta)
    
     - [Power Distribution Network and Routing](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%205.md#pdn-and-routing)
        + [Lab Steps To Build Power Distribution Network](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/DAY%205.md#labs-to-build-pdn)



