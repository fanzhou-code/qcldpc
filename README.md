### QC-LDPC code prototype matrices for 2-level Construction D' lattices

This package contains three DAT files for QC-LDPC code prototype matrix with block length n = 2304, 5016, 10008 respectively. Each DAT file consists of a line indicating code length and two 12-by-24 prototype matrices. 


For more details about how to build a Construction D' lattice using QC-LDPC parity-check matrices and the encoding and decoding algorithms to be used in power-constrained channels, see my paper [arXiv:2102.04741 [cs.IT]](https://arxiv.org/abs/2102.04741). You are requested to cite the paper if you publish an academic paper basd on these codes. See LICENSE for more information.

-

Nested QC-LDPC codes *C*<sub>0</sub> and *C*<sub>1</sub> are used to build 2-level Construction D' lattices. The parity-check matrices **H**<sub>0</sub> and **H**<sub>1</sub> can be obtained as follows.

- The parity-check matrix **H**<sub>0</sub> of the first-level code *C*<sub>0</sub> is generated using the two 12-by-24 prototype matrices. Convert each prototype matrix to a binary matrix by replacing an entry using a Z-by-Z matrix where Z = n / 24. This is done as follows. The element -1 represents a zero matrix. The element 0 represents an indentity matrix **I**. And a positive element indicates the shift amount of a right-shift cyclic-permutation matrix. The sum of the two binary matrices is **H**<sub>0</sub> which has only one double-circulant.


- The parity-check matrix **H**<sub>1</sub> of the second-level code *C*<sub>1</sub> is built by two block rows. The first block row is the sum of the block rows of **H**<sub>0</sub> in sets {5,7,9,11} while the second block row is the sum of the block rows of H<sub>0</sub> in sets {6,8,10,12}.

The parity-check matrices **H**<sub>0</sub> and **H**<sub>1</sub> are of girth 8. These QC-LDPC codes are not designed for achieving optimal coding properties, but for easily building a triangular matrix for a Construction D' lattice that is to be used in power-constrained channels thus the encoding and indexing are also straightforward. The QC-LDPC code parity-check matrices are used for decoding.




