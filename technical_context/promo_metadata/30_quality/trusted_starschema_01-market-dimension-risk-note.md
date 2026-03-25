# d_reconstructed_markets — Risk Note

## Why this note exists
The final assessment identifies `d_reconstructed_markets` as the only real dimensional blocker.

## Risk
- duplicate `MARKET_ID` keys exist as exact duplicates
- all fact rows depend on duplicated market keys
- a naive 1:* semantic join would multiply rows

## Use policy
- do not present this table as a standard clean dimension until deduplicated
- prefer a canonical one-row-per-`MARKET_ID` view for semantic and RAG relationship guidance
