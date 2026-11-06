# Reproducing this repository

Input: the Parquet files listed below, revision `fecc2c971945cacd914c63b54ee22db9149e58c9` of the `voilaj/swiss-caselaw` dataset
(`https://huggingface.co/datasets/voilaj/swiss-caselaw/resolve/fecc2c971945cacd914c63b54ee22db9149e58c9/<file>`), plus `graph/statute_references.parquet`
from the same revision, and lexifina/switzerland-law `main` for the overlay's `law_commit`.

```
python tools/build.py vd <cache with data/ and graph/> <empty folder> --today 2026-11-06
```

Needs Python 3 and `duckdb`. Gives 169,221 decision commits and one documentation commit, hash for hash.

## SHA-256 of the input files

```
d064c497b612966962639d1c40b6e3e946aee654b4e2898e80eb081d3159967b *vd_findinfo.parquet
887ce743d46df9a907fb99dabb5f68b8640fd3c75a7c74af3f33cc6f0f889700 *vd_gerichte.parquet
4a56567ce14de087ef0bf636c74adeae5a6b8fd24682a0b80a28ecdbb6806563 *vd_omni.parquet
```
