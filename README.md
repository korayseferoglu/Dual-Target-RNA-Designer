# Dual-Target RNA Designer: A Hybrid saRNA/siRNA Discovery Engine

## Project Overview
The Dual-Target RNA Designer is a specialized computational tool developed to identify multi-functional RNA candidates capable of simultaneously modulating two distinct genetic targets. By integrating molecular biology principles with algorithmic efficiency, the tool discovers sequences that can act as a Small Activating RNA (saRNA) for one gene and a Small Interfering RNA (siRNA) for another.

## Core Biological Logic
The engine utilizes a Private scoring and filtering architecture to ensure high-efficiency molecular candidates:

* **Thermodynamic Modeling**: Binding affinity is calculated using the Nearest-Neighbor thermodynamic model. 
* **Parameter Integration**: The algorithm applies specific parameters ($nnParams$) for every dinucleotide pair to determine the Gibbs Free Energy ($\Delta G$) of the interaction.
* **Rational Design Integration**: The tool incorporates Reynolds and Ui-Tei rational design rules to rank candidates based on sequence stability and asymmetry.
* **RISC Loading Optimization**: A mandatory "Strict A/T Rich 3' End" filter can be toggled to ensure the preferential loading of the guide strand into the RISC complex.

## Key Features

* **Dual-Sequence Sliding Window**: The backend independently performs a k-mer sliding window analysis across two distinct DNA/mRNA sequences to find mathematical intersections.
* **Advanced Sequence Filtering**:
    * **GC Content Control**: Restricts candidates to a user-defined range (e.g., 35% - 65%) to optimize AGO2 protein compatibility.
    * **Homopolymer Rules**: Automatically eliminates sequences containing GGGG (toxicity risk) and AAAAA/CCCCC (slippage risk).
    * **Homopolymer Penalties**: Sequences containing UUUU (termination signal risk) receive significant score deductions.
* **Structure Visualization**: Features a built-in "Molecular Duplex Viewer" that displays the predicted sense (passenger) and antisense (guide) alignment.
* **Industrial Export Capabilities**: Supports professional R&D workflows with direct exports to FASTA (for synthesis), CSV (for data analysis), and PDF (for academic reporting).

## Technical Implementation
This platform is a high-performance, client-side web application built with:

* **Vanilla JavaScript Engine**: Optimized for rapid string manipulation and thermodynamic calculations without server-side latency.
* **Client-Side Data Handling**: Utilizes jsPDF and autoTable for secure, offline data reporting.
* **Responsive Scientific UI**: A professional interface designed for high-resolution data comparison and sequence management.

## Scientific Disclaimer
This tool was independently engineered to demonstrate the feasibility of multi-targeted RNA therapeutics. The biological algorithms and scoring logic were developed by the author, while AI-augmented coding techniques were utilized to optimize software deployment and frontend performance.
