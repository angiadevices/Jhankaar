# Jhankaar

झंकार | Jhankaar: The sound of chimes or percussion / The name of a popular series of remix cassettes in India in the 90s.

Update 16/11/25:

- From Toadstool Tech on the schematic, "The way the input detect probe is designed to work is that the GPIO send out a binary signal that is detected by the MCU when nothing is connected to the jack.
The way this works uses the switch pin on the standard mono thonkiconn jack.
The switch pin is connected to the output of the input detect GPIO, which then connects to the input of the ADC if nothing is plugged in.
When a cable is inserted though, this breaks that normalled connection and CV is received as normal.
So your INPUT_DETECT net should connect to the "Ring" of your jack instead of the tip.
There's actually a Kicad footprint for this normalled jack, called "AudioJack2_Switch" I think, which better repreents it, since you're not using a TRS stereo jack." </br>
- Replacing the W25Q128JVSIQ for W25Q32JVSSIQ did something! Able to navigate with the Mode button with LEDs now reflecting the changes in mode. Still no audio output yet, and most other I/O still seems to do nothing with preliminary testing.

Original:

An inexact hardware clone of the ['Ectocore' Eurorack module by Toadstool Tech and Infinite Digits](https://github.com/schollz/_core), Jhankaar currently stands as an incomplete project, the troubleshooting of which may currently be out of my capability/circumstances. [As the original schematics are provided under CC-BY-SA license](https://github.com/schollz/_core/blob/main/schematics/ectocore_v1.0.1.pdf), so too are the files in this repository.

The following hardware bugs have been confirmed to exist in this particular iteration of the files:
- R7 needs to be 10k, **NOT** 0R
- U22 10V shunt needs to be **flipped** (it is used for generating -10V in this circuit)

However, **fixing those changes on prototypes have not made the module functional.** They have gotten this design to the point of having power as and where expected, and flashing the module with the Ectocore firmware successfully, but actually turning on the module still results in a big pile of nothing.

I am hoping that members of the vibrant open-source synth DIY community more knowledgable than I can see mistakes here that I can't, and that this can serve as the basis for a triumphant encore of the Ectocore.
