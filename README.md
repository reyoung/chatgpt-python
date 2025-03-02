<p align="center">
    <a href="https://pypi.python.org/pypi/chatgpt/"><img alt="PyPi" src="https://img.shields.io/pypi/v/chatgpt.svg?style=flat-square"></a>
    <a href="https://github.com/labteral/chatgpt-python/blob/master/LICENSE"><img alt="License" src="https://img.shields.io/github/license/labteral/chatgpt-python.svg?style=flat-square"></a>
</p>

<h3 align="center">
    <b>ChatGPT Python SDK</b>
</h3>

<p align="center">
    <a href="https://www.buymeacoffee.com/brunneis" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="35px"></a>
</p>

## Install or update
```bash
pip install -U chatgpt
```


## Create a file with your credentials
> :warning: &nbsp; Please, update the library. Note the change in the config file.

Create the file `config.json` in your working directory: 

```json
{
    "email": "email@example.org",
    "password": "xxx"
}
```


## Usage
### CLI
You can launch the CLI with:
```bash
chatgpt
```
or
```bash
python -m chatgpt
```

These are the available commands:
- `reset`: forget the context of the current conversation.
- `clear`: clear the terminal.
- `exit`: exit the CLI.

### SDK
```python
from chatgpt import Conversation

conversation = Conversation()
print(
    conversation.chat(
        "We are going to start a conversation. "
        "I will speak English and you will speak Portuguese."
    )
)
print(conversation.chat("What's the color of the sky?"))

# The AI will forget it was speaking Portuguese
conversation.reset()
print(conversation.chat("What's the color of the sun?"))
```
