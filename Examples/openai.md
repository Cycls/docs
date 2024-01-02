---
layout: page
title: Open AI
nav_order: 4.1
---

## Mirror
This app mirrors user input by responding back with the same text:
```py
from sarya import Sarya, UI
 
sarya = Sarya("SECRET")

@sarya("@my-app")
def ai(messages):
    return UI.Text(messages[0]["content"]) # incoming messages
```
