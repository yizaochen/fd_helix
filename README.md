# fd_helix - A Tool for Building Helical Structures from Fiber Diffraction Data

**fd_helix** is a C program designed to construct various helical structures from fiber diffraction data, primarily producing double-stranded Watson-Crick helices in PDB format. This code is especially useful for computational structural biologists who wish to generate helices of different types for modeling and simulation purposes.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Input Parameters](#input-parameters)
- [Example](#example)
- [References](#references)
- [License](#license)

## Overview

This repository provides a modern, user-friendly tutorial and implementation of **fd_helix**, originally developed by David A. Case. The tool can generate helical structures for a variety of types, such as:

- Right-handed A-RNA (Arnott)
- Right-handed A-PRIME RNA (Arnott)
- Right-handed B-DNA (Langridge)
- Right-handed B-DNA (Arnott)
- Left-handed B-DNA (Sasisekharan)
- Right-handed A-DNA (Arnott)

The helix axis is aligned along the z-axis, and outputs are written in PDB format.

## Features

- Generates double-stranded Watson-Crick helices
- Supports multiple helix types for both DNA and RNA
- Outputs data in PDB format for easy visualization and further analysis

## Installation

To compile the code, you need a C compiler such as `gcc`. Use the following command:

```bash
gcc -o fd_helix fd_helix.c -lm
```

## Usage

The program takes two primary inputs:

1. **helix_type**: A string indicating the desired helix type (e.g., "arna", "abdna").
2. **sequence**: A one-letter nucleotide sequence (e.g., "CGCGAAUUGC"). The complementary strand will be automatically generated.

Run the program from the command line as follows:

```bash
./fd_helix <helix_type> <sequence>
```

### Input Parameters

- **helix_type**: One of the following options:

  - `arna`: Right-handed A-RNA
  - `aprna`: Right-handed A-PRIME RNA
  - `lbdna`: Right-handed B-DNA (Langridge)
  - `abdna`: Right-handed B-DNA (Arnott)
  - `sbdna`: Left-handed B-DNA
  - `adna`: Right-handed A-DNA

- **sequence**: A one-letter sequence of nucleotides (e.g., "CGCGAAUUGC").

### Example

To generate a B-DNA helix from the sequence "ACGTACGT", use:

```bash
./fd_helix abdna ACGTACGT
```

The output will be in PDB format and printed to `stdout`.

## References

The helix structures are based on published fiber diffraction data. Key references include:

1. Arnott, S., et al. J. Mol. Biol. (1973) 81:107-122.
2. Arnott, S., et al. Nature (1980) 283:743-745.
3. Lakshimanarayanan, A.V., et al. Biochim. Biophys. Acta (1970) 204:49-53.
4. Fuller, W., et al. J. Mol. Biol. (1965) 12:60.
5. Arnott, S., et al. Handbook of Biochemistry and Molecular Biology, CRC Press, 1976.

## License

This project is licensed under the BSD 3-Clause License. See the [LICENSE](LICENSE) file for the full license text.

The original code by David A. Case (2018) is distributed under a permissive open-source license, and any modifications or redistribution must comply with the following conditions:

- Redistributions of the source code must retain the original copyright notice, license conditions, and disclaimer.
- The original license text is included in the source code for reference.

By combining these terms, the repository acknowledges and respects the original licensing requirements while providing clarity for future users and contributors.

## Acknowledgments

Special thanks to David A. Case for the original implementation of **fd_helix** and to all contributors to this field of computational structural biology.
