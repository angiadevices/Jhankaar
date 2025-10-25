# Jhankaar

झंकार|Jhankaar: The sound of chimes or percussion/The name of a popular series of remix cassettes in India in the 90s.

An inexact hardware clone of the 'Ectocore' Eurorack module by Toadstool Tech and Infinite Digits, Jhankaar currently stands as an incomplete project, the troubleshooting of which may currently be out of my capability/circumstances. As the original schematics are provided under CC-BY-SA license (https://github.com/schollz/_core/blob/main/schematics/ectocore_v1.0.1.pdf), so too are the files in this repository.

The following hardware bugs have been confirmed to exist in this particular iteration of the files:
- R7 needs to be 10k, **NOT** 0R
- U22 10V shunt needs to be **flipped** (it is used for generating -10V in this circuit)

However, **fixing those changes on prototypes have not made the module functional.** They have gotten this design to the point of having power as and where expected, and flashing the module with the Ectocore firmware successfully, but actually turning on the module still results in a big pile of nothing.

I am hoping that members of the vibrant open-source synth DIY community more knowledgable than I can see mistakes here that I can't, and that this can serve as the basis for a triumphant encore of the Ectocore.
