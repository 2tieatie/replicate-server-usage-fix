**# replicate-server-usage-fix**
Tried to connect server hosted on Replicate to LangChain and can not do it? Here is the fix.

1. Go to the:
```venv\Lib\site-packages\langchain\llms\replicate.py```
Replace existing file with fixed.

2. Set the environment variable with replicate server path:
```os.environ['REPLICATE_SERVER_PATH'] = "replicate_username/server_name"```

3. Set `use_server=True` in `Replicate()` definition:
```llm = Replicate(
    model="model_name",
    use_server=True
 )```

Here we go!

Fixed with 🐍❤️. 
