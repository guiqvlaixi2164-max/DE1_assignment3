# Web Sentiment Pipeline

## Main work

Using the boto3 library to leverage the capabilities of AWS S3, Bedrock, Translate, and Comprehend to achieve the following workflow: inputting webpage URLs, with Bedrock scraping the webpage content, Translate translating it into English, Comprehend analyzing its sentiment, and the analysis results being stored in S3. This process can be used to analyze a large number of webpages.

## Quickstart
1. Create S3 bucket: `ceu-jiaqi-2025 `
2. Configure AWS: `aws configure`
3. Create virtualenv and install: `python -m venv de_env && source de_env/bin/activate && pip install -r requirements.txt`
4. Run jupyter notebook de1assignment3_modified.ipynb
5. Results saved to `s3://ceu-jiaqi-2025/results/`
6. Run jupyter notebook interpret_results.ipynb
7. Results saved to results_summary.csv and analysis_plots/

## Files
- notebooks/: Jupyter notebooks for the whole pipeline including 
- analysis_plots/: the result visualizations of the results of sentiments of webpages

## Structure
```
DE1_assignment3/
├─ README.md
├─ requirements.txt
├─ .gitignore
├─ .env.sample               
├─ notebooks/
│  ├─ de1assignment3.ipynb
│  └─ interpret_results.ipynb
├─ analysis_plots/
│  ├─ mixed_boxplot.png
│  ├─ neutral_boxplot.png
│  ├─ Mixed_Negative_sentiment.png
│  ├─ Overall_sentiment.png
│  └─ avg_scores_by_lang.png
├─ results_json
└─ results_summary.csv

```
