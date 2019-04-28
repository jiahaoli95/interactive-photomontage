# Interactive Digital Photomontage

This is a very simple python Implementation of [Interactive Digital Photomontage](https://grail.cs.washington.edu/projects/photomontage/photomontage.pdf).
This implementation only supports "Designated image" data penalty and "colors" interaction penalty, as dicussed in Section 3 of the paper.

The code for poisson blending is largely borrowed from [this](https://github.com/PPPW/poisson-image-editing) repo.

![GUI](/gui.png)

## Denpendencies

The code is in Python 3. The GUI is written in tkinter, which should be shipped with most python distribution.

[PyMaxflow](https://github.com/pmneila/PyMaxflow) and cv2 are required.

## Usage

The usage is very simple. First put the source images in `source_imgs` directory (only `.jpg` and `.jpeg` are supported). Then in the command line, run `python main.py`, the window as above should appear.

The image on the left is the current composite image. The image in the middle is one of the source images. You can click "Next image" to switch to next source image. The map on the right is the label map which indicates which part of the composite comes from which source image.

This implementation blends current composite image with one source image at a time. The only thing you need to do is to draw a few strokes on the composite image and source image respectively, which indicate which parts of the composite and source image you want to preserve. Then click the "Run" button and wait for a few seconds. The new composite image will be generated on the left, along with the label map on the right. These two images are saved in the `output_imgs` directory.
