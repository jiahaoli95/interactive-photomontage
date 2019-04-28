# Interactive Digital Photomontage

This is a very simple python Implementation of [Interactive Digital Photomontage](https://grail.cs.washington.edu/projects/photomontage/photomontage.pdf).
This implementation only supports "Designated image" data penalty and "colors" interaction penalty, as dicussed in Section 3 of the paper.

The code for poisson blending is largely borrowed from [this](https://github.com/PPPW/poisson-image-editing) repo.

![GUI](/gui.png)

## Denpendencies

The code is in Python 3. The GUI is written in tkinter, which should be shipped with most python distribution.

[PyMaxflow](https://github.com/pmneila/PyMaxflow) and cv2 are required.
