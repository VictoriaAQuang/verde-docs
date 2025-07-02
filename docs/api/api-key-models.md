# Using Your API Key to View Your Available Models

After obtaining your API Key from your course/team, you can obtain a detailed list of available models using curl:

```
curl -s -L "https://llm-api.cyverse.ai/v1/models" -H "Authorization: Bearer $OPENAI_API_KEY" -H 'Content-Type: application/json'
```

Alternatively, you can use `jq` or python's json module to view the output in a more human readable format.

Option 1: If you have `jq` installed:
```
curl -s -L "https://llm-api.cyverse.ai/v1/models" -H "Authorization: Bearer $OPENAI_API_KEY" -H 'Content-Type: application/json'|jq
```

Option 2: If you have python's json module installed:
```
curl -s -L "https://llm-api.cyverse.ai/v1/models" -H "Authorization: Bearer $OPENAI_API_KEY" |python -m json.tool
```

