# LLM Next-Item Recommendation

A five-day proof-of-concept project that applies LLM-generated shopping intentions to rerank next-item recommendations on the Amazon Reviews 2023 All Beauty dataset.

## Project idea

The system combines a sequential recommender with semantic intention matching:

1. A recommendation model generates candidate products.
2. A small LLM infers the user's current shopping intention from recent interactions.
3. Product intentions are generated from product metadata.
4. Semantic similarity is used to rerank candidate products.

## Day 1 status

- Download Amazon Reviews 2023 All Beauty interactions and metadata.
- Audit and clean the data.
- Apply iterative k-core filtering.
- Create temporal train, validation, and test splits.
- Export processed Parquet files and a RecBole `.inter` file.

## Repository structure

```text
llm-next-item-recommendation/
├── README.md
├── requirements-day1.txt
└── notebooks/
    └── 01_data_preprocessing.ipynb
```

## Run Day 1 notebook

1. Open Google Colab.
2. Upload `notebooks/01_data_preprocessing.ipynb`.
3. Run each cell from top to bottom.
4. Store generated data in Google Drive.

## Day 1 dependencies

```bash
pip install -r requirements-day1.txt
```

## Dataset

Amazon Reviews 2023 — All Beauty, published by McAuley Lab.

## Notes

Large raw and processed datasets are not committed to GitHub. The notebook downloads the official files and recreates the preprocessing outputs.
