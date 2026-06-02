<p align="center">
  <img src="assets/logo.png" alt="SynapSpec" width="200"/>
</p>

<h1 align="center">SynapSpec</h1>

<p align="center">
    Targeted DIA peak inspection software for quickly checking precursor and fragment peaks in raw mass spectrometry files.
</p>

<p align="center">
  <a href="https://synapspec.ai/spectralens/#docs">
    <img src="https://img.shields.io/badge/docs-spectralens-blue?style=flat-square" alt="Documentation">
  </a>
</p>

# SpectraLens

SpectraLens is designed for researchers who want to visually inspect specific precursors without running a full DIA analysis workflow. Add raw files, enter the precursor sequences you care about, and quickly review MS1/MS2 XICs, spectra, and RT-iRT calibration context.

## Documentation

User guide and download links are available at:

https://synapspec.ai/spectralens/

## Core Features

- **Targeted Precursor Inspection**: Add specific peptide sequences and charge states to inspect only the precursor signals you care about.
- **Raw File Based Analysis**: Load DIA raw files and extract targeted chromatographic evidence directly from selected files.
- **Interactive XIC Viewer**: Review MS1 precursor XICs and MS2 fragment XICs with interactive plots.
- **Spectrum Context**: Compare experimental and predicted spectra to evaluate peak evidence.
- **RT-iRT Mapping**: Use anchor precursors for retention time to iRT mapping.
- **Automatic Raw File Settings**: Instrument and analysis settings are automatically initialized from raw file metadata when available.
- **Custom Sequence Input**: Supports UniMod-style modifications, multiple sequence entry, and explicit charge notation.
- **CSV Export**: Export results for review, sharing, or downstream curation.

## Applications

### Targeted DIA Review

- Confirm whether a specific precursor is present in a raw file
- Inspect MS1 and MS2 peak shapes
- Compare fragment ion co-elution patterns
- Review uncertain identifications manually

### Method Development

- Check precursor behavior across raw files
- Validate RT windows and fragment evidence
- Inspect anchor peptides for RT-iRT calibration
- Tune extraction settings before larger-scale analysis

### Proteomics Data Curation

- Review selected peptides without re-running a full pipeline
- Export targeted inspection results
- Support manual validation of important precursor candidates

## Installation

Download the packaged desktop application for your operating system:

- **macOS**: Download the latest macOS binary
- **Windows**: Download the latest Windows binary

Linux builds are not currently available.

## Quick Start

1. Launch SpectraLens and create or select a workspace.
2. Open the **Raw Files** panel.
3. Click **Add Files** and select DIA raw files.
4. Check the blue checkbox for the raw file or files to include in analysis.
5. Click the **+** button in the precursor list toolbar to add sequences.
6. If the **+** button is not visible, collapse the **Raw Files** panel first.
7. Enter target sequences in the sequence dialog.
8. Click **Add** to add them to the precursor table.
9. Select the sequence rows you want to analyze.
10. Adjust settings if needed.
11. Click **Analyze All**.
12. Inspect the iRT-RT, Spectra, MS1 XIC, and MS2 XIC tabs.

## Precursor Input Format

Enter one sequence per line or separate multiple sequences with commas.

Examples:

```text
PEPTIDESEQ.2
PEPC(UniMod:4)TIDESEQ.3
AA[Hex(1)HexNAc(2)]DD
PEPTIDES(UniMod:21)EQ,PEPTIDEM(UniMod:35)SEQ
```

### Input Rules
Use UniMod notation for modifications, for example C(UniMod:4).
Separate multiple sequences with line breaks or commas.
Add charge state using a period followed by a number, for example .2 or .3.
If charge is omitted, SpectraLens can predict likely charge states and iRT values.

## Settings
SpectraLens automatically initializes many settings from raw file metadata when available. Users can manually adjust:

- MS1 tolerance
- MS2 tolerance
- RT extraction window
- Instrument type
- NCE
- Maximum number of fragments
- Intensity aggregation strategy

Anchor precursors are used for RT-iRT mapping.

## System Requirements
- **Operating System**: macOS or Windows
- **Input Data**: DIA raw files
- **Memory**: 16 GB RAM minimum recommended
- **Storage**: Enough local disk space for raw files, converted files, and workspace outputs

## Support

**Visit our website**: [synapspec.ai/spectralens](https://synapspec.ai/spectralens)

**Documentation**: [synapspec.ai/spectralens/#docs](https://docs.synapspec.ai)

**GitHub Discussions**: [Community support and feature requests](https://github.com/bionsight/SpectraLens/discussions)

**Bug Reports**: [Report issues](https://github.com/bionsight/SpectraLens/issues)

**Contact:** [contact@bionsight.com](contact@bionsight.com)
