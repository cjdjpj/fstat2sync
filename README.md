# fstat2sync

Simple utility to convert [FSTAT files](https://doi.org/10.1111/j.1471-8286.2004.00828.x) to sync ([synchronized pileup files](https://doi.org/10.1093%2Fbioinformatics%2Fbtr589)).

Caveats:
1. No chromosomal/genetic structure data (marked NA).
2. "Reference allele" is assumed to be allele with highest frequency

## Usage
```bash
cd fstat2sync
cargo build --release
./target/release/fstat2sync -f <input.fstat> -o <output.sync>
```
Both file formats are tab/whitespace separated formats that encode pool-seq data.
