
## Delivery
- **app/Dockerfile**: To generate an application image
- **k8s/deployment.yaml**: To deploy image to Kubernetes
- Other necessary code

## Input/Output

When you execute this command:
```bash
curl --location --request POST 'http://127.0.0.1:9527/translation' \
--header 'Content-Type: application/json' \
--data-raw '{
    "payload": {
        "fromLang": "en",
        "records": [
            {
                "id": "123",
                "text": "Life is like a box of chocolates."
            }
        ],
        "toLang": "ja"
    }
}'
```

Should return:
```bash
{
   "result":[
      {
         "id":"123",
         "text":"人生はチョコレートの箱のようなものだ。"
      }
   ]
}
```

