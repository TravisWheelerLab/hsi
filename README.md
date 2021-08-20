# hsi

A featherweight package for indexing biological sequence files and extracting
subsequences.

## Usage

The package consists of three tools, described below.

**sindex**

Generates an .hsi index for a FASTA-formatted biological sequence file.

**sstat**

Outputs metadata about an indexed sequence file, including number
of sequences, total residues, and per-sequence residue counts.

**sfetch**

Extracts a (sub)sequence from an indexed file.

## Build

We use CMake, so the usual incantations will work...

```
cmake .
make
```

Executables will end up in the `build/` directory.
