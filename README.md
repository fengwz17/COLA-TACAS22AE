# COLA: a complementation and determinization library for Büchi automata
Cola includes complement algorithms for unambiguous nondeterministic Büchi automata (UNBA) and limit deterministic Büchi automata (LDBA), as well as a determinization algorithm for LDBAs.
Cola has been built on top of [Seminator](https://github.com/mklokocka/seminator).

### Special instructions for artifact evaluation
* The GitHub repo [COLA](https://github.com/fengwz17/COLA) is under developing and much different from the version in this artifact submission. Here we provided the version we used in the experiments of the submission paper.

### List of algorithms
* Complementing UNBA: the [slice-based algorithm](https://arxiv.org/abs/2005.09125v2)

* Determinizing LDBA: in submission

### Requirements
* [Spot](https://spot.lrde.epita.fr/)

### Compilation
```
autoreconf -i
```
```
./configure
```
```
make
```
```
sudo ldconfig
```
Then you will get an executable file named **cola** .

### Determinization
Input an LDBA named "filename", and run ```./cola --determinize=parity filename```, then you will get an equivalent deterministic parity automaton (DPA) on standard output!
To output the DPA to a file, use ```./cola --determinize=parity filename -o out_filename```
