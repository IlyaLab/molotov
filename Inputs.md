## Input parameters ##

Users will require a series of files as input for Molotov.  These are, in order of their appearance on command line:

  * _Sequence File:_ a FASTA sequence containing genomic data. For each probability matrix that follows, this sequence will be linearly scanned for scored matches.
  * _Background File:_ a precomputed INCLUSive background model, currently of version 1.0. This should contain one horizontal vector of data (0th-order model), one vertical vector of data (1st-order model), and a background matrix (2nd-order model) for processing.
  * _Threshold File:_ a listing of consensus motif positional weight matrices and their expected threshold values for significance. This file will always be used as the determinant of which matrices to use, even when filtering is not enabled.
  * _Matrix Library:_ the directory containing all of the motif positional weight matrices indicated by the given threshold file. Absolute and relative paths are both accepted in the context of your platform's path specification.

Three switches are also provided for convenience:

  * _-quiet:_ disables all status messages printed to stdout. Errors and warnings will still be printed to stderr, however.
  * _-filter:_ enables filtering based on the values defined by our threshold file. This mode enables speculative filtering based on the historical maximum scores observed within a given sequence file. This means that, early in processing, several results will be output with small values as the tool builds its maximum value. This is expected behavior, and any results of this nature should simply be filtered out as a post-processing step. The entire purpose of filtering is thus to limit the output to a small set for post-processing. More on this later.
  * _-reverse:_ compute _only_ the reverse strand by walking the [reverse complement](http://en.wikipedia.org/wiki/Complementarity_(molecular_biology)) of the given sequence file. In this way, both the positive and negative strands of an input genomic sequence can be computed through two separate runs of the tool, assuming no imperfections in sequencing.