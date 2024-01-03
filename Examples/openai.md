---
layout: page
title: Open AI
nav_order: 4.1
---

> messages obj

> shape of messages

> then chatGPT

## Mirror
This app mirrors user input by responding back with the same text:
```py
from sarya import Sarya, UI
 
sarya = Sarya("SECRET")

@sarya("@name-of-your-app")
def app(messages):
    return UI.Text(messages[0]["content"]) # incoming messages

sarya.run()
```
