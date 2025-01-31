## Day 3 - Design and characterize one library cell using Magic Layout tool and ngspice
### <br>  Labs for CMOS inverter ngspice simulations
 
Now we will doing some spice simulations on some MOSFETS. But first we need to create a spice deck. A spice deck is a connectivity information of a netlist. So we need to create for PMOS And NMOS as well. We need to define the following things for creating this spice deck.....

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/6722add4-f2e0-4c68-88c6-526f670b1f0c)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

The connectivity information of PMOS.

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/75e9eac4-0354-419f-8509-3a27294d9833)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

The connectivity information of NMOS.

![Screenshot 2024-03-30 002823](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/4f142434-8d47-44af-a6ed-927d88ce5c38)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

The connectivity information of CLOAD(capacitor load).

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/79060827-7836-4c3f-938f-b980ff80c5bd)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM


The connectivity information of VDD.

![Screenshot 2024-03-30 003047](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/0f5d5ee5-e00e-4e2b-8458-55365507b29f)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now we will git clone a repository which has the .magic file. The github repository [github repository](https://github.com/nickson-jose/vsdstdcelldesign#standard-cell-design-and-characterization-using-openlane-flow)

Then gitclone the repository link through:-

![Screenshot 2024-03-30 131247](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/c5ec9e1b-0612-429d-b1f7-3312df5c71e2)

Now after copying go to openlane directory in terminal........
<br>Put git clone command and then paste the URL.

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/50c1aa1e-2ace-489b-97d8-b26ab34938d0)

This will create a folder of the same name as the repository. 
![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/9b5f0854-2ec4-44dd-9960-1ffaa385ad2d)

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/c91a7451-2ad2-439e-a78a-cb41d1b12718)

Now lets look at what is there inside this..

![Screenshot 2024-03-30 135241](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/90f7486d-56ab-4418-bd61-7a16dffd25c1)

Now if you look at the repository and the terminal, they have the same files.

Now we will go to magic with our cloned file. 

![Screenshot 2024-03-30 152739](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/2710d3b9-24bd-4d66-a1cc-aeaa38207f4b)

![Screenshot 2024-03-30 152759](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/dad500ad-72b3-49e5-95c3-f9ac597289a2)



## <br> Inception of Layout – CMOS fabrication process

16 MASK CMOS PROCESS

1. Selecting a Substrate
<br>  A substrate is something onto which you fabricate your design. The one we will be choosing will be a p-type. Out of all the qualities of the substrate, we will be mainly focusing on resistivity and doping level. The main focus for our doping level will be that the Substrate doping should be less than well doping.

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/4e054482-3f94-49b9-9314-f045aa33065d)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

2. Creating active region for transistors.
<br>  These are the regions where actually you see the pmos and nmos transistors. So basically we will be creating some bucket kind of in the substrate, where we will create pmos and nmos. First we will create some isolation between the pockets so they don't interfere in eachother's working. So for this you can deposit layers. First, a 40 nm SiO <sub>2</sub>. Then, 80 nm Si<sub>3</sub>N<sub>4</sub> and a 1um photoresist.  
There is a term Mask. The layout particularly in the fabrication term is known as mask. The layouts that we see in custom design are converted to these masks. 
<br> Now the areas where we donot want any chemical reactions to happen, we will place the masks over there. Then we will the expose the areas not covered to UV light. Then we will wash or remove the area which was not covered.

![Screenshot 2024-03-28 230516](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/eaf51411-8cf1-425c-9319-e6e174ad5e4b)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

![Screenshot 2024-03-28 230525](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/70deb806-dd10-42b6-adab-c3ff55025342)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Then you remove this mask layer. Now if you do any reactions or depositions, the area under the photoresist won't be effected. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/9b437569-8972-4852-b62f-e064674226d6)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now we will also remove the layer of 80 nm Si<sub>3</sub>N<sub>4</sub> that was exposed to UV light and the photoresist as well. The remaining layer of Si<sub>3</sub>N<sub>4</sub> will also act as a good layer of protection as well. 

![Screenshot 2024-03-29 091448](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/ffdedb54-c277-4b16-977e-12124c980023)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

When we will put this substrate in a very hi temperature furnace, the area of SiO <sub>2</sub> that is not covered by Si<sub>3</sub>N<sub>4</sub> will grow and the area that was covered won't grow. Let us see how. So first we need to place this in an oxidation furnace. It looks something like this.....

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/86106984-fcce-447d-991f-6db2b3777fbc)
<br> SOURCE OF THE IMAGE- THE WEB PAGE OF IIT KANPUR. 
<BR> THE LINK- (https://www.iitk.ac.in/dordold/index.php?option=com_content&view=category&layout=blog&id=186&Itemid=205#:~:text=Oxidation%20Furnace&text=Thermal%20oxidation%20is%20a%20simple,filler%20material%20in%20gaps%20etc).


THIS WOULD NOW LOOK SOMETHING LIKE BELOW.........

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/352132d4-2f1f-4e4e-9ff4-f10c3687b267)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

The grown part is referred to field oxide or the bird's beak. And the process is known as "LOCOS"(Local Oxidation of Silicon.). 


![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/9b2bb907-4f36-4eab-9fcb-df72e2e3e120)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Si<sub>3</sub>N<sub>4</sub> will be stripped using hot phosphoric acid. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/27250d7e-7b42-4b6c-b7b8-48c177530030)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now, let me define the regions. The well kind of regions that were protected regions are the active regions. And the grown part is the isolated region, which won't allow one transistor to interfere in other transistor's working. 

3. Creating N-well and P-well. 
<br> Now the N-well will be used for the fabrication of PMOS transistors and the P-well will be used for NMOS transistors. In this also, one area needs to be protected as both the wells cannot be formed at the same time. The process to be followed now is pretty similar to the one followed earlier. First put a layer of photoresist, and then the mask upon the area you want to protect. Expose to UV light. Wash off the exposed area. Remove the mask. And now for making a P-well in the exposed area, we will use Boron. Boron is a P-type substance. To diffuse Boron into the well, we would use the process namely Ion implant.

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/ee97d44b-1083-4bcb-9450-677afb126e43)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

<br> You follow the same steps for N-well as well. But in place of Boron you use Phosphurous as it is an N-type substance. 

![Screenshot 2024-03-29 095933](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/b3fba42f-d639-476a-8668-8844de6c164e)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

![Screenshot 2024-03-29 100125](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/ed522c49-f405-4aa6-b027-eeac85f7a847)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

![Screenshot 2024-03-29 100145](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/ef433249-5875-4781-9c44-be7788037501)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

These wells are also known as the twin tubs. Now we need to diffuse the well, so that it covers almost half of the substrate. This will decide the depth of the wells. So for this we will be putting this into a high temperature furnace.  

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/40937700-52fa-4c2b-a397-da16f605463a)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM


4. Formation of Gate

Gate as we see now, is the most important termianl of the transistors beacause you control the threshold voltage(turning on voltage of the transistor) from here. So the fabrication of gate terminal becomes really important. 

![Screenshot 2024-03-29 110459](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/f2c6eb80-51fa-422a-b6b3-b45961398e2b)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/e1857037-d872-4624-927f-f87cd33e506c)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM


So, we need to control the oxide capacitance and doping concentration.
<br> First let us control doping capacitance. Now, we will follow the same steps as before. Now we will be using the mask4, and as the name suggests for this CMOS process we will be using total of 16 masks. And for this we will be using boron but with lesser force. We will maintain the dose of boron in such a manner, so that we have the required doping concentration. And this doping concentration depends upon the threshold voltage seen in the above images. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/a06c31c2-ed88-482a-8f71-a165f6ede0f8)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now using mask 5 we will be following same process for NMOS but again using phosphorous or we can also use arsenic.  

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/9fc26e48-d3a2-42c4-bbd0-96610c630481)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

As we have been implementing many layers an P & N type substances, So our oxide is being damaged multiple times. So we will repair this layer.

First we etch the original damaged oxide layer using dilute hydrofluoric solution. Then we regrow this layer to give high quality oxide.  
<br> ![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/730dccb6-a8d9-4e6d-bbf8-251a99118eea)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now we will deposit a layer of 0.4 um polysilicon layer. 
![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/fb12fc0f-9531-46ab-93b8-57777177978d)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Then we ion implant any N-type substance either phosphurous or arsenic for low gate resistence.

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/716ca0e7-879e-4a48-bc48-c36354ab867e)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now using photoresist and mask 6, we will make something like below. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/26dd0251-2c9c-4366-91d1-000d46a36636)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now we can remove the mask and etch away the polysilicon layer that was not covered by photoresist. And then remove the photoresist layer.

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/0ea48563-dcb0-42b3-8ae0-e51c66a9336d)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

5. Lightly Doped Drain formation

We need to create LDD of two types, P- and N-. First we will put a layer of photoresist then mask7 and expose the other side to UV light. Then remove the mask. And as firstly we have exposed the P well to UV light. So we tend to make a NMOS there. So we would use phosphorous for ion implant. So for this we will be choosing the force and the dosage very carefully, so the n- implant does not penetrate fully into the well and hovers at the top. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/53e09902-8d39-4c4f-abb3-6d54f3aa387d)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

But why is it n- and not n+ ?? It is so, because if p or n type has "-" as after them, it means it is lightly doped.


Same process for PMOS. But with Boron. 

![Screenshot 2024-03-29 130424](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/09a8fe90-641f-491e-94ab-74c3e7f5836f)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now somehow we have to protect the implants so in the further processes nothing gets into them. So we will put some spacers over there. So first deposit a thick layer of either SiO <sub>2</sub> or Si<sub>3</sub>N<sub>4</sub>. So we will do Plasma anisotropic etching. In this all of the layer is etched but the substance near the side walls remains.  

![Screenshot 2024-03-29 132323](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/5443e6cb-7545-4645-b07d-8ae29389c08c)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

6. Source and Drain formation.

Now add a thin layer of screen oxide. The purpose of adding it is to avoid the effect of channeling. The effect of channeling is when we do alot of ion implant and when the vector velocity of the crystaline structure of our P substrate matches with the velocity of the ions. When this happens, the ions might go deep into the substrate without even hitting any of the silicon atoms. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/d5f9729d-2f8a-453b-a0cd-269afc1469fd)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now again thesame process. Photoresistor, Mask 9, other side's exposure to UV light, Ion implant of arsenic.

![Screenshot 2024-03-29 134206](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/1fc364ef-f0eb-485d-a657-782a11efc25c)

Same for the otherside. Ion implant with Boron. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/a680b85d-500c-4723-ad76-0d86f23a1196)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now we will do High Temperature Annealinng.
![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/eb7571dc-4472-4f08-a03c-7c3474cb1ffb)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

7. Steps to form contacts and interconnects(local) 

So contacts are really important because, that is the only thing that is accessible to an user. It is a medium through which you can control the electrical characteristics of your transistors.   

So to start with, we will first etch the thin oxide layer that we had put in the earlier steps. Then, deposit titanium on wafer surface, using sputtering. But what is sputtering?? It is a process in which we take the metal, which in this example is titanium and hit argon gas at it. And this will make the atoms of the titanium sputter and enter into the substrate.    

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/f8930305-c0ae-425c-8442-d52e6c5d1c39)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM


![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/4e2ef4a8-3eca-444c-b2a6-944161b4f6a7)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/775101e8-9a99-4fd5-a863-b56bc645f4b5)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Apart from the above result for the N<sub>2</sub> being an ambient there is another result. That is TiN that is used only for local comunication.  

So now, If you look at the previous image you will able to see a dark blue layer which is in the area where there are no thick layers. That layer is TiSi<sub>2</sub>. And the light blue layer above every structure is TiN.


Now we need to decide which contacts to bring to the next level. As some connections can be made internally and there is no need of taking them above. 

Now we will put the layers of photoresist and mask 11 on the areas which we want to reach above. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/436b90f8-e747-480b-893f-d1d412f7b405)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Then remove the mask and etch off the extra TiN using RCA cleaning. RCA cleaning is done a solution known as RCA only. Its solutes vary from use to use. In this it would consist of:- 
<br> 1. De-ionized water (H<sub>2</sub>O), 5 parts
<br> 2. Ammonium hydroxide (NH<sub>4</sub>OH), 1 part
<br> 3. Hydrogen peroxide (H<sub>2</sub>O<sub>2</sub>O), 1 part

It would look ssomething like below- 
<br>![Screenshot 2024-03-29 173223](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/ac10b124-11bb-4ee9-ae70-a18310fdf3c9)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now we remove the photoresist layer. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/00101cc3-cf73-4591-a111-2bee45ef3553)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM


8. Higher level metal formation.

Now if we see surface topogaraphy of this state of the substrate is not suitable for further ados. 

So for this we will deposit a thick layer of SiO <sub>2</sub>. And this is a specific  SiO <sub>2</sub> doped with phosphorous or boron (known as phosphosiicate glass or borophosphosilicate glass) depsited on wafer surface.

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/c441258f-c33d-447a-8406-87a3c1d96236)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now, we will use the Chemical Mechanical Polishing technique for planarizing wafer surface. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/46b26ebe-736a-40a3-80aa-2de1822cd001)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Now we will follow some more processes and form the below kind of substrate.

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/2a3f77a1-8b7b-48f1-808b-e97053e13807)
<br> SOURCE OF THE IMAGE- VSDIAT PLATFORM

Labs -

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/738658ea-111f-42b7-82e2-26f06f00c364)

So this is the layout for our inverter that we got in the previous labs. In this are two transistors PMOS and NMOS. 

![image](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/2cdd3ecc-4fc9-4666-bae5-5ece858a7a26)

And the red line is polysilicon. In the repository mentioned, the steps of making an inverter from scratch are also given.

<br> ![Screenshot 2025-01-31 224516](https://github.com/user-attachments/assets/affb5e3c-bfa5-4f05-8fd4-bb1bbce1da34)
<br> {IMAGE CREDITS: DEEPTHY SANTHAKUMAR, TAKEN FROM OJASVI SHAH'S REPOSITORY}

![image](https://github.com/user-attachments/assets/725a4a1a-7c6b-4f3a-96b6-1bf419ed9542)

![Screenshot 2025-01-31 230544](https://github.com/user-attachments/assets/dd2534d6-6b8b-4f42-8e0e-00fa3ec34174)<br> ![image](https://github.com/user-attachments/assets/eb349111-b98b-4be1-90a9-fe448a4484b0) <br> ![image](https://github.com/user-attachments/assets/aa3664c8-81c2-458b-84e9-4d1005142f92)


## SKY130 TECH FILE LABS
### LAB STEPS TO CREATE FINAL SPICE DECK USING SKY130 TECH

<BR> ![image](https://github.com/user-attachments/assets/53cf8e0e-e603-45a2-bb4d-6234116c52cd)
<BR> ![image](https://github.com/user-attachments/assets/212645cc-948b-4037-8de3-ddfc993dbcbe)

<br> ![image](https://github.com/user-attachments/assets/ec8f9ce3-a4a2-4362-946d-c5c175b05fcc)



### LAB STEPS TO CREATE FINAL SPICE DECK USING SKY130 TECH
 





