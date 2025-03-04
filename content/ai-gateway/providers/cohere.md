---
title: Cohere
pcx_content_type: get-started
---

# Cohere
[Cohere](https://cohere.com/) build AI models designed to solve real-world business challenges.

## Endpoint

`https://gateway.ai.cloudflare.com/v1/{account_id}/{gateway_id}/cohere`

## URL structure

When making requests to [Cohere](https://cohere.com/), replace `https://api.cohere.ai/v1` in the URL you’re currently using with `https://gateway.ai.cloudflare.com/v1/{account_id}/{gateway_id}/cohere`.

## Examples

```bash
---
header: Request
---

curl https://gateway.ai.cloudflare.com/v1/{account_id}/{gateway_id}/cohere/v1/chat \
  --header 'Authorization: Token {cohere_api_token}' \
  --header 'Content-Type: application/json' \
  --data '{
  "chat_history": [
    {"role": "USER", "message": "Who discovered gravity?"},
    {"role": "CHATBOT", "message": "The man who is widely credited with discovering gravity is Sir Isaac Newton"}
  ],
  "message": "What year was he born?",
  "connectors": [{"id": "web-search"}]
}'
```

If using the [`cohere-python-sdk`](https://github.com/cohere-ai/cohere-python), set your endpoint like this:

```python
---
filename: main.py
---
import cohere
import os

co = cohere.Client(
  api_key= os.getenv('API_KEY'),
  base_url="https://gateway.ai.cloudflare.com/v1/{account_id}/{gateway_id}/cohere/v1",
)

chat = co.chat(
  message="hello world!",
  model="command-r-plus"
)

print(chat)
```