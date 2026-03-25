# Example – product-level decomposition of calls

## Purpose
This example translates the sample calculation sheet into retrieval-friendly text so the logic is not left only inside a table.

## Source basis
The source workbook includes a worked example with Pfizer products and the following columns: Representing Company, Product form/strength, Local Brand, Mentions, Product Details, Manufacturer, Weighted Calls, Non-Weighted Calls.

## Example narrative
One call can mention multiple products. In the worked example, the same representative company appears across multiple products, each with one mention. Product Details and Weighted Calls are split across products, while Non-Weighted Calls stays at call level and therefore can remain constant across rows before totaling.

## Sample records
- ELIQUIS FILMTABL 2.5MG: Local Brand=ELIQUIS, Mentions=1, Product Details=0.5, Manufacturer=BRISTOL-M.-SQUIBB, Weighted Calls=0.5, Non-Weighted Calls=0.5
- ELIQUIS FILMTABL 5MG: Local Brand=ELIQUIS, Mentions=1, Product Details=0.5, Manufacturer=BRISTOL-M.-SQUIBB, Weighted Calls=0.3, Non-Weighted Calls=0.5
- PREVENAR 13: Local Brand=PREVENAR 13, Mentions=1, Product Details=1, Manufacturer=PFIZER PHARMA, Weighted Calls=0.15, Non-Weighted Calls=0.5
- XELJANZ FILMTABL RET 11MG: Local Brand=XELJANZ, Mentions=1, Product Details=1, Manufacturer=PFIZER PHARMA, Weighted Calls=0.05, Non-Weighted Calls=0.5
- TOTAL: Local Brand=None, Mentions=4, Product Details=3, Manufacturer=None, Weighted Calls=1, Non-Weighted Calls=2

## Retrieval interpretation
- Use this example when users ask how Product Details, Weighted Calls, and Non-Weighted Calls can diverge at product level.
- Keep the example separate from the canonical metric definitions so examples do not replace the official definition.

## Governance note
This file is an illustrative example only. It should be linked to the canonical metric definitions for Product Details, Weighted Calls, and Non-Weighted Calls.