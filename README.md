# fstat2sync

Simple utility to convert [FSTAT files](https://doi.org/10.1111/j.1471-8286.2004.00828.x) to sync ([synchronized pileup files](https://doi.org/10.1093%2Fbioinformatics%2Fbtr589)).

Caveats:
1. Only supports 4 alleles (simulating sequence reads A/T/C/G)
2. No chromosomal/genetic structure data included in sync (marked NA)
3. "Reference allele" is assumed to be allele with highest frequency

## Usage
```bash
cd fstat2sync
cargo build --release
./target/release/fstat2sync -f <input.fstat> -o <output.sync>
```
Both file formats are tab/whitespace separated formats.
The synchronized pileup format is used to represent pool-seq data.
This conversion is useful if we want to treat FSTAT as pseudo-poolseq data, for example when outputted by the forward simulation program quantiNemo2.
