# Simulating Restaurant Reviews with LLMs
### LLMs for Economic and Social Sciences

This project explores the capabilities of various Large Language Models (LLMs). The current focus is on evaluating LLMs for review analysis tasks using zero-shot and few-shot prompting techniques.

## Project Structure

The repository is organized as follows:

-   `data_preprocessing.ipynb`: Jupyter notebook for data cleaning and preparation.
-   `gen_reviews.ipynb`: Jupyter notebook for generating synthetic review data.
-   `evaluate_reviews_zero_shot.ipynb`: Jupyter notebook for evaluating LLMs on review analysis using a zero-shot approach.
-   `evaluate_reviews_few_shot.ipynb`: Jupyter notebook for evaluating LLMs on review analysis using a few-shot approach.

## Workflow

The typical workflow for this project is as follows:

1.  **Data Preprocessing**: Run `data_preprocessing.ipynb` to clean and prepare the review data from the original dataset.
2.  **Review Generation**: Use `gen_reviews.ipynb` to generate reviews with various LLMs.
3.  **Evaluation**:
    -   Run `evaluate_reviews_zero_shot.ipynb` to perform zero-shot evaluation on the generated reviews.
    -   Run `evaluate_reviews_few_shot.ipynb` to perform few-shot evaluation on the generated reviews.

## Setup

To run the notebooks in this project, you need to have a Python environment with the necessary libraries installed. You will likely need libraries such as:

-   `pandas`
-   `numpy`
-   `jupyter`
-   `scikit-learn`
-   `requests`
-   `kagglehub`
-   `textstat`
-   `transformers`
-   `torch`
-   `sentence-transformers`
-   `umap`
-   `matplotlib`
-   `seaborn`

Please inspect the import statements in the Jupyter notebooks to identify all dependencies. You will also need to configure your LLM API endpoint in the `gen_reviews.ipynb` notebook.

## Data

The primary dataset is `data/datasets/cleaned_reviews.csv`, which is derived from [restaurant-review-dataset](https://www.kaggle.com/datasets/joebeachcapital/restaurant-reviews) from Kaggle. It contains reviews that have been preprocessed for the evaluation tasks. The `prompt_bank.csv` contains the prompts that are used to query the LLMs.

## Models Evaluated

This project evaluates the following LLMs (based on the output files):

-   Code Llama 7B (e.g., `codellama_latest`)
-   Llama 3.1 8B (e.g., `llama3.1_latest`)
-   Mistral 7B (e.g., `mistral_latest`)
-   Qwen 2.5 32B (e.g., `qwen2.5-coder_32b`)

The generated reviews are stored in the `data/zero-shot/` and `data/few-shot/` directories.

