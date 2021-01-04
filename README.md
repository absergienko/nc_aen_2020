# nc_aen_2020
This project contains codebooks for noncoherent transmission obtained using autoencoder network

These results are presented in the following paper:

Alexander B. Sergienko, Polina V. Apalina, "Codebook Design for Noncoherent Communications Using Autoencoders," Proc. 2021 IEEE Conference of Russian Young Researchers in Electrical and Electronic Engineering (EIConRus), Saint Petersburg and Moscow, Russia, 2021.

The codebooks are presented in two formats: as MATLAB data files (`*.mat`, folder `MAT`) and as ASCII files (`*.txt`, folder `ASCII`)

File names have the following form: `cb_n*_k*`

The number after "n" shows the number of samples in the codebook signals.

The number after "k" shows the number of bits that can be transmitted using this codebook (i.e., the codebook contains `2^k` signals)

For example, the file `cb_n5_k8.txt` contains the codebook with `2^8=256` signals consisting of `n=5` samples.

Every `.MAT` file contains a single variable with the name `ssc`. This variable is a 2D complex-valued array with `2^k` rows and `n` columns. Every row of this array represents one signal from the codebook.

Every `.TXT` file contains an ASCII table of floating-point numbers with `2^k` rows and `2*n` columns. Every row of the table represents one signal from the codebook. The 

first `n` columns contain real parts of the signal samples, remaining `n` columns contain imaginary parts of the signal samples. 

The ASCII folder also contains the file `read_codebook_from_ascii_file.m` - MATLAB function for reading a codebook from these ASCII files.
