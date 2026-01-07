# LLMs for Economic and Social Sciences (llms4ess-project)

This project explores the capabilities of various Large Language Models (LLMs) for tasks in the economic and social sciences. The current focus is on evaluating LLMs for review analysis tasks using zero-shot and few-shot prompting techniques.

## Project Structure

The repository is organized as follows:

-   `data_preprocessing.ipynb`: Jupyter notebook for data cleaning and preparation.
-   `gen_reviews.ipynb`: Jupyter notebook for generating synthetic review data.
-   `evaluate_reviews_zero_shot.ipynb`: Jupyter notebook for evaluating LLMs on review analysis using a zero-shot approach.
-   `evaluate_reviews_few_shot.ipynb`: Jupyter notebook for evaluating LLMs on review analysis using a few-shot approach.
-   `data/`: Contains all data-related files.
    -   `data/datasets/`: Raw and processed datasets.
        -   `cleaned_reviews.csv`: The main dataset of cleaned reviews.
        -   `holdout.csv`: A holdout set for final evaluation.
        -   `prompt_bank.csv`: A collection of prompts used for evaluation.
    -   `data/zero-shot/`: Stores the output of the zero-shot evaluations for different models.
    -   `data/few-shot/`: Stores the output of the few-shot evaluations for different models.
-   `README.md`: This file.

## Workflow

The typical workflow for this project is as follows:

1.  **Data Preprocessing**: Run `data_preprocessing.ipynb` to clean and prepare the review data from the original dataset.
2.  **Review Generation (Optional)**: If synthetic data is needed, use `gen_reviews.ipynb` to generate reviews with various LLMs.
3.  **Evaluation**:
    -   Run `evaluate_reviews_zero_shot.ipynb` to perform zero-shot evaluation on the generated reviews.
    -   Run `evaluate_reviews_few_shot.ipynb` to perform few-shot evaluation on the generated reviews.
4.  **Analysis**: The evaluation notebooks will save their results as JSON files in the `data/zero-shot` and `data/few-shot` directories. These results can be further analyzed to compare model performance.

## Setup

To run the notebooks in this project, you need to have a Python environment with the necessary libraries installed. While a `requirements.txt` is not provided, you will likely need libraries such as:

-   `pandas`
-   `numpy`
-   `jupyter`
-   `scikit-learn`
-   `requests`
-   `kagglehub`

Please inspect the import statements in the Jupyter notebooks to identify all dependencies. You will also need to configure your LLM API endpoint in the `gen_reviews.ipynb` notebook.

## Data

The primary dataset is `data/datasets/cleaned_reviews.csv`, which is derived from a restaurant review dataset. It contains reviews that have been preprocessed for the evaluation tasks. The `prompt_bank.csv` contains the prompts that are used to query the LLMs.

## Models Evaluated

This project evaluates the following LLMs (based on the output files):

-   Code Llama (e.g., `codellama_latest`)
-   Llama 3.1 (e.g., `llama3.1_latest`)
-   Mistral (e.g., `mistral_latest`)
-   Qwen 2.5 (e.g., `qwen2.5-coder_32b`)

The results of these evaluations are stored in the `data/zero-shot/` and `data/few-shot/` directories.

