# Needham-Schroeder Symmetric Key Protocol Automated Analysis

GitHub repository for the security analysis of the Needham-Schroeder Symmetric Key protocol using the Tamarin Prover. All the findings are meant only to confirm the flaws already identified within the literature, as the content if this work was intended as an introductory tutorial to the use of the Tamarin Prover.
This repository contains all the necessary files, including the Tamarin Prover code and a detailed article explaining the theoretical background behind the analysis.

## Table of Contents

- [Introduction](#introduction)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Usage](#usage)
- [Article](#article)
- [License](#license)

## Introduction

The Needham-Schroeder Symmetric Key protocol is a well-known cryptographic protocol designed for secure communication between two parties using symmetric key encryption. This repository leverages the Tamarin Prover, a state-of-the-art tool for the formal verification of security protocols, to verify the main security properties protocol.

## Repository Structure

The repository is organized as follows:

```
.
├── article
│   ├── Needham-Schroeder-Analysis.pdf
│   └── src
├── tamarin
│   ├── NS.sphty
│   ├── NS_fixed.sphty
│   ├── XD3H.sphty
│   └── README.md
├── README.md
├── CITATION.cff
└── LICENSE
```

- `article/`: Contains the detailed article introducing Tamarin and explaining the analysis. Also contains the source code to compile the article.
- `tamarin/`: Contains the Tamarin Prover code and a README specific to the Tamarin files.
- `README.md`: This README file.
- `CITATION.cff`: Metadata to correctly cite this work.
- `LICENSE`: The license under which this project is distributed.

## Getting Started

To get started with analyzing the Needham-Schroeder Symmetric Key protocol using the Tamarin Prover, follow the steps below.

### Prerequisites

Ensure you have the following installed on your system:

- [Tamarin Prover](https://tamarin-prover.github.io)
- [LaTeX](https://www.latex-project.org) (optional, for building the article)

### Usage

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/dambrosidenis/Needham-Schroeder-Tamarin.git
   cd Needham-Schroeder-Tamarin
   ```

2. **Navigate to the Tamarin Directory:**

   ```bash
   cd tamarin
   ```

3. **Run the Tamarin Prover:**

   ```bash
   tamarin-prover [file].spthy
   ```

## Article

The detailed article explaining the analysis can be found in the `article/` directory:

- [Needham-Schroeder-Analysis.pdf](article/Needham-Schroeder-Analysis.pdf)

The article provides an introduction to the Tamarin Prover, an in-depth explanation of the Needham-Schroeder Symmetric Key protocol, the methodology used for the analysis, and the results of the verification. The source files for the article are available at [article/src/](article/src/)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
