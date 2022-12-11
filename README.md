
First of all, it is stated that the code of this warehouse is referenced from [this warehouse](https://github.com/acheong08/ChatGPT). I just provide an example here.

<br>

## how to use
-  Log in to openai and get the token, you can [click here](https://github.com/acheong08/ChatGPT/wiki/Setup) to view the details.


- Install the following packages:
    ```bash
    pip3 install revChatGPT --upgrade
    ```

- Then run the following code:
    ```bash
    python chatgpt.py
    ```

## 
Of course, you can also use to build your own system, just like the following code:
```python
from revChatGPT.revChatGPT import Chatbot

# For the config please go here:
# https://github.com/acheong08/ChatGPT/wiki/Setup
config = {"session_token": ""}

def text2text(text):
    chatbot = Chatbot(config, conversation_id=None)
    response = chatbot.get_chat_response(text, output="text")
    result_text = response["message"]
    print("chatgpt: {}\n".format(result_text))
    return result_text

text = "hello world!"
result_text = text2text(text)
print(result_text)
```

