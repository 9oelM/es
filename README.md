# Scraper
## Setup
0. Make sure you are using `python3.6+` and a decent `pip`
    ```bash
    python3 --version
    pip install --upgrade pip
    ```

1. Install `pipenv` and install packages
    ```bash
    pip install pipenv
    pipenv install 
    ```

2. Install node lts
    ```bash
    nvm install stable
    ```

3. Install `serverless` globally and install python requirements plugin
    ```bash
    npm install -g serverless
    serverless sls plugin install -n serverless-python-requirements
    ```

4. Install npm packages
    ```bash
    npm install 
    ```

## Deploy 
```
pipenv run pip freeze > requirements.txt && sls deploy
```

## Must read (warning)
`requirements.txt` is essential for `serverless-python-requirements` to work. You can delete it, but you must produce it again before you deploy!
