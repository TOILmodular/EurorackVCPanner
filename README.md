# EurorackVCPanner
## General
A voltage-controlled 2-channel panning Eurorack module, based on the design from YUSYNTH.

You can check this [Youtube video](https://youtu.be/wUGyGTA9OOM) to see the module in action.

## Module Build and PCBs
If you want to build the module yourself, I uploaded the schematic, the BOM and the Gerber files for the PCB.

The PCB designs are purely through-hole.

There are two different versions for the control board, an "original" and a "Thonk" version.
Reason is that for my own module, I am using specific potentiometers - 16K4 series from Supertech Electronics - and 3.5mm jack sockets - MJ-355 from Marushin - available at my local electronics shop.

However, since most DIY projects for Eurorack modules out there are using potentiometers from ALPHA and so-called THONKICONN jacks, as they are provided by Thonk in the UK, I also created a version with footprints for those components.
Choose the one you need.

Please note, that there is also a difference in the front panel components between the different versions.
The "original" version has an additional stereo jack output for connecting to a 3.5mm head phone, while the "Thonk" version only has the separate mono output jacks for the two channels.

The reason is simply that I did not find any stereo type of the THONKICONN jacks.

I created the Gerber files with the online tool EasyEDA and ordered it at JLCPCB.
I cannot guarantee, if this set of zipped Gerber files works also for other providers, like e.g. PCBWay. I have not tried that. But I saw online, that others did it.

If you want to know about my DIY building process, take a look at those two YouTube videos:
- [How I design PCBs for my Eurorack Synth Modules](https://youtu.be/pXtuV9Pv-m4)
- [Eurorack Module Synth - Building an Electric Druid Wavetable Oscillator Module](https://youtu.be/ECpdo4HfqLg)

## Panel Layout (two versions)
I added the information about hole coordinates for the front panels in the folder PanelLayout, referring to the component layout in the Gerber files. The layout differs between the two PCB versions due to the stereo output jack only available in the "original" version.

## Calibration
The two trimmers are used to adjust the midrange for the paning for each channel.
Each trimmer (left/right on the board) belongs to one channel (accordingly, as the component layout is symmetric, left and right).

The procedure for each channel is the following:
1. Use a voltmeter and adjust the trimmer in order to measure -4V on the wiper pad of the trimmer.
2. Send a triangle wave (1kHz) with an amplitude of 10Vpp (-5V/+5V) on the input of the channel.
3. Set the pan level pot entirely counter-clockwise, and the pan pot to 12 o'clock.
4. Connect a dual channel oscilloscope at the outputs A and B. You should obtain the triangle with equal amplitude on both channels, then turn the pan pot from clockwise to counter-clockwise position. You should observe the disappearing of the triangle on one side and the increase in amplitude on the other side.
5. Adjust the trimmer, so that when the pan pot is at 12 o'clock, the amplitude of the two triangle waves is roughly half of that can be measured for one wave when the pan pot is set to clockwise or counter-clockwise positions. (If you don't have an oscilloscope by ear using hadphones, check for an even balance at 12 o'clock, then verify that the panning effect acts as expected when rotating the pan pot).

## Additional Information about specific Components
If you want to use the Gerber files for having PCB manufactured, please note the following information about components used.

- On the control board, you will find electrolytic capacitors with a rectangle next to them. Since these capacitors are too tall for standing upright on the board with the main board on top of it, those capacitors need to be mounted in a rectangular position. The rectangle shows the position for each bent-over capacitor.

![VCPanner](https://user-images.githubusercontent.com/97026614/208285201-dfbbc868-3e67-439f-993b-360eb0bb05e7.jpeg)

![VCPannerFront](https://user-images.githubusercontent.com/97026614/208285485-5868b83e-366f-40ce-acf1-905e7239262e.jpeg)

![VCPannerSide](https://user-images.githubusercontent.com/97026614/208285495-b5506d2f-b3a5-4faa-b05f-4f2914710ab7.jpeg)

![VCPannerBack](https://user-images.githubusercontent.com/97026614/208285500-fb965954-ad8f-43df-86e7-0887a7a944d3.jpeg)

<img width="389" alt="VCPanner_PCB_Main_Back_Thonk" src="https://user-images.githubusercontent.com/97026614/208284757-2657470f-5ccf-44d8-b783-eee1ba2389bf.png">

<img width="389" alt="VCPanner_PCB_Main_Front_Thonk" src="https://user-images.githubusercontent.com/97026614/208284758-f55b4fe3-2c1e-49f0-a35d-8ce1be8cc83e.png">

<img width="389" alt="VCPanner_PCB_Ctrl_Front_Thonk" src="https://user-images.githubusercontent.com/97026614/208284753-1e3e428a-b3fb-4bca-9c43-79683ca24706.png">

<img width="389" alt="VCPanner_PCB_Ctrl_Back_Thonk" src="https://user-images.githubusercontent.com/97026614/208284749-c599325a-299f-4a56-8f6b-a072ba5d1d33.png">
