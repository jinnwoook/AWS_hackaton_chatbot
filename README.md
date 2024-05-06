# AWS_hackaton_chatbot
복지왕 서비스 chatbot service


# aws_hackaton_alab


## :wrench: Modification of README.md is in progress :wrench:  

## How to run
Only tested on python=3.10  
If you don't have streamlit package  
```
pip install steamlit
```
**Running app.py with streamlit**
```
streamlit run app.py
```


### notes  
requirements.txt is not updated yet.  
You need to create new OPENAI API key and apply it to code.  

## Todo List  
- [ ] Adapt json config
- [ ] Link AWS EC2 and S3 bucket
- [ ] Move faiss index, csv file, etc. from EC2 to S3
- [ ] Apply inference part to lambda function
- [ ] Remove inference part from main page of chatbot code

## Example of "awsconfig.json"
```ruby
{
    "API_KEY": {
        "OPENAI": "<your_openai_api_key>"
    },
    "AWS": {
        "S3PATH" : "s3://your-bucket-name"
    },
    "MODEL": {
        "NAME": "gpt-3.5-turbo",
        "TEMPERATURE": 0.7,
        "MAX_TOKENS": 100,
        "TOP_P": 1.0,
        "FREQUENCY_PENALTY": 0.0,
        "PRESENCE_PENALTY": 0.0
    },
    "FAISS": {
        "INDEX_PATH": "",
        "FILENAME": ""
    }
}
```
