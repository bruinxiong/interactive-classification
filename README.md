# Interactive Classification for Deep Learning Interpretation

We have designed and developed an interactive system that allows users to experiment with deep learning image classifiers and explore their robustness and sensitivity.
Selected areas of an image can be removed in real time with classical computer vision inpainting algorithms, allowing users to ask a variety of "what if" questions by experimentally modifying images and seeing how the deep learning model reacts.
The system also computes class activation maps for any selected class, which highlight the important semantic regions of an image the model uses for classification.
The system runs fully in browser using Tensorflow.js, React, and SqueezeNet. An advanced inpainting version is also available using a server running the PatchMatch algorithm from the [GIMP Resynthesizer plugin](https://github.com/bootchk/resynthesizer).

<!-- VIDEO LINK -->

***

## Installation

Download or clone this repository:

```bash
git clone https://github.com/poloclub/interactive-classification.git
```

Within the cloned repo, install the required packages with yarn:

```bash
yarn

```

## Usage

To run, type:

```bash
yarn start

```

## Advanced Inpainting

The following steps are needed to set up PatchMatch inpainting:

1. Clone the [Resynthesizer](https://github.com/bootchk/resynthesizer) repository and follow the instructions for building the project
2. Find the `libresynthesizer.a` shared library in the `lib` folder and copy it to the `inpaint` folder in this repository
3. Run `gcc resynth.c -L. -lresynthesizer -lm -lglib-2.0 -o prog` (may have to install glib2.0 first) to generate the prog executable
4. You can now run `inpaint_server.py` and PatchMatch will be used as the inpainting algorithm.

## License

MIT License. See [`LICENSE.md`](LICENSE.md).


## Contact

For questions or support [open an issue][issues].

[issues]: https://github.com/poloclub/interactive-classification/issues
