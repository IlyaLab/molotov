This project is a C++ reimplementation of Motif Locator.  Please see [documentation](BuildingAndUsing.md) for more details.

**Molotov** is an implementation of the algorithm sketched out in Gert Thijs' PhD thesis, [Probabilistic Methods to Search for Regulatory Elements in Sets of Coregulated Genes (Thijs 2003)](ftp://ftp.esat.kuleuven.ac.be/sista/thijs/reports/phd.pdf).

Its sole purpose is to linearly scan an input genomic sequence searching for motifs with a high probabilistic signal relative to an input consensus matrix. In this sense, the algorithm is similar to a synonym matcher for any given data set, with the bonus of providing location-based information and a score proportional to the amount of signal provided by each candidate match.

For further algorithmic considerations, please consult the paper.


---


For more information, please contact [codefor@systemsbiology.org](mailto:codefor@systemsbiology.org).

