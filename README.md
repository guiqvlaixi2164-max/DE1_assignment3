# Web Sentiment Pipeline

## Quickstart
1. Create S3 bucket: `ceu-jiaqi-2025 `
2. Configure AWS: `aws configure`
3. Create virtualenv and install: `python -m venv de_env && source de_env/bin/activate && pip install -r requirements.txt`
4. Run notebook or `python app.py <url1> <url2>`
5. Results saved to `s3://ceu-jiaqi-2025/results/`

## Files
- notebooks/: Jupyter notebook
- pipeline/: reusable modules
- Dockerfile: reproducible environment

## Structure
```
web-sentiment-pipeline/
├─ README.md
├─ requirements.txt
├─ requirements-lock.txt
├─ .gitignore
├─ .env.sample
├─ app.py                
├─ notebooks/
│  └─ s3-bedrock-pipeline.ipynb
├─ pipeline/
│  ├─ fetcher.py
│  ├─ bedrock_client.py
│  ├─ translate_client.py
│  ├─ comprehend_client.py
│  └─ s3_store.py
├─ tests/
│  └─ test_pipeline.py
├─ Dockerfile
└─ .github/
   └─ workflows/
       └─ ci.yml

```
