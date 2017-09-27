# Ambisonic Toolkit Matrices

A set of (real) matrix files for use by matrix mixing encoders and decoders.

### Features

*  Channel Order: Gerzon / Furse-Malham, aka, Classic first-order (FOA)
*  Normalization: MaxN, aka, Classic first-order (FOA)

The ATK's fixed matrices are designed to support a variety of useful
_encoding_ and _decoding_ strategies. Encoding means, converting from some other
signal format, e.g., _monophonic_ or _stereophonic_, to Ambisonic B-format.
Decoding means converting from Ambisonic B-format.


#### Encoders

*   Omni - Omnidirectional encoding (monophonic). E.g., pressure only.
    In a well aligned, dampend studio environment, this usually sounds "in the head", while in concert hall listening usually appears as omnipresent.

*   Quad - Quadraphonic encoding. The quadraphonic signal is encoded
    as four planewaves arriving at `[ 45, 135, -135, -45 ]` degrees.

*   5.0 - 5.0 encoding. The 5.0 signal is encoded as five planewaves
    arriving at `[ 0, 30, 110, -110, -30 ]` degrees.

*   7.0 - 7.0 encoding. The 7.0 signal is encoded as seven planewaves
    arriving at `[ 0, 30, 90, 135, -135, -90, -30 ]` degrees.

*   A to B - A-format to B-format encoding. Encodes to a variety of
    tetrahedral orientations and W channel weights. The A-format encoder is often used in conjunction with the B-format to A-format decoder to form signal processing networks which preserve the spatial encoding. On its own, is often used to author immersive, periphonic (3D) decorrelated soundfields.

*   HOA1 - First order
    [Ambisonic format exchange](https://en.wikipedia.org/wiki/Ambisonic_data_exchange_formats) encoding. Encodes a variety of formats to traditional B-format. Encoding means encoding from one Ambisonic channel componenent orderding and normalisation to that of traditional B-format. In other words, from some standard scheme to __Gerzon__ (aka __Furse-Malham__) ordering with __MaxN__ normalisation.


#### Transformers
*   Mirror - Mirroring across the _origin_ and each of the _coordinate axes_.


#### Decoders
*   5.0 - [Bruce Wiggins'](http://www.brucewiggins.co.uk/?page_id=78)
    optimised ITU 5.0 decoders. Three kinds are available:
    *  _Focused_ returns a focused, but front weighted image.
    *  _Equal_ equalises the angles across the image.
    *  _Four_ is similar to _Equal_, but doesn't use the centre speaker.


*   B to A - B-format to A-format decoding. Decodes to a variety of
    tetrahedral orientations and W channel weights. The B-format to A-format decoder is primarily intended to be used in conjuction with the A-format to B-format encoder. Though the use of BtoA/AtoB decoder/encoder pairs, signal processing networks can be constructed which preserve the spatial encoding found in the original input B-format signal.

*   HOA1 - First order [Ambisonic format
    exchange](https://en.wikipedia.org/wiki/Ambisonic_data_exchange_formats) decoding. Decodes traditional B-format to a variety of formats. Decoding means decoding from traditional B-format to another Ambisonic channel componenent orderding and normalisation. In other words, from __Gerzon__ (aka __Furse-Malham__) ordering with __MaxN__ normalisation to some other standard scheme.

    __Note:__ You should have received a license notice with these matrices.
    Please see the included _Third Party Notices_ for further details on the
    Wiggins contribution.


---
### Matrix formats

Each matrix is provided in several formats:

***.yml***

A [YAML](http://yaml.org/) file containing the matrix along with verbose metadata. Refer to [flu-dec.yml](FOA/decoders/BtoA/flu-dec.yml) for an example.

***.txt***

A text file containing the matrix, with one row per line, and cell values separated by spaces. Refer to [flu-dec.txt](FOA/decoders/BtoA/flu-dec.txt) for an example.

***.mosl.txt***

A text file containing one cell value per line. The first two values gives the dimension of the matrix as number of rows and number of columns. Empty lines can be used for improved readability. Comment lines can be added, starting with `//`. Inline comments are also supported. Refer to [flu-dec.mosl.txt](FOA/decoders/BtoA/flu-dec.mosl.txt) for an example.


---
## Using Matrices with Reaper

The matrices are included as part of the [ATK for Reaper](http://ambisonictoolkit.github.io/download/reaper/) install, and there is no need to download and install the matrices separately.


## Using Matrices with SuperCollider

Install [ATK for SuperCollider](http://ambisonictoolkit.github.io/download/supercollider/). Launch SuperCollider3, and run the following code:


```
ATK Matrix Installation
(
// Create ATK support directory
// Place unzipped matrices in the directory opened  

Atk.createUserSupportDir;
Atk.openUserSupportDir;
)
```

If ATK for SuperCollider has been correctly installed, the above code will open the ATK's user support directory. Place the downloaded matrices here.

If you use ATK for Reaper as well as ATK for SuperCollider on Mac OSX, the matrices are shared between the two programs, and they will reside in the same location. We do not expect this to cause any problems.

---

## Feedback and Bug Reports

Known issues are logged at [GitHub](https://github.com/ambisonictoolkit/atk-matrices/issues).

If you experience problems or have questions pertaining to the ATK Matrices,
please create an issue in the
[ATK-Matrices issue tracker](https://github.com/ambisonictoolkit/atk-matrices/issues).

If you use the matrices for an artistic project, please
[let us know](mailto:info[at]ambisonictoolkit.net). We [plan on](https://github.com/ambisonictoolkit/ambisonictoolkit.github.io/issues/9)
adding a gallery of example artistic and creative projects that make use of the
Ambisonic Toolkit.

If you wish to use the matrices as part of a technical or software project, we'd
[like to know](mailto:info[at]ambisonictoolkit.net) about that too. We're
[planning](https://github.com/ambisonictoolkit/ambisonictoolkit.github.io/issues/10)
to link to other projects making use of Ambisonic Toolkit assets.

### List of Changes

Version 1.0.0
*   Initial release

## Credits

The matrix files distributed with the Ambisonic Toolkit are licensed
under a Creative Commons Attribution-Share Alike 3.0 Unported [(CC BY-SA 3.0)](http://creativecommons.org/licenses/by-sa/3.0/) License and
are copyright the Ambisonic Toolkit Community and Joseph Anderson, 2017.

* J Anderson : [[e-mail]](mailto:j.anderson[at]ambisonictoolkit.net)
