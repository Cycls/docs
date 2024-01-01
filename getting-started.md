---
layout: default
title: Getting started
nav_order: 2
description: "..."
permalink: /getting-started
---

#  Getting started

Sarya is a python framework for building, and publishing AI applications. It provides everything you need to transform your project into beautiful UI across multiple platforms. 

in order to get started make sure you get your `SECRET-KEY` from the developer platform at [platform.sarya.com](https://platform.sarya.com).

### 1. Install

```sh
pip install sarya
```

### 2. Initiate Sarya Client

make the `Sarya` client with your key:

```py
from sarya import Sarya, UI

sarya = Sarya("sk-...")
```

### 3. Add the Entry Point
A main function works as the entry point of your app. Designate your main function with a name `@app.app("@my-app")`. in this example we just send "Hello World!" for each user request.
```py
@sarya.name("@my-app")
def ai():
    return UI.Text("Hello World!")
```

### 4. Run the Server
Your app is published with `run()` so that Sarya calls to it with each relevant request:
```py
sarya.run()
```

### 5. Hello World! 👋
The full example:
```py
from sarya import Sarya, UI

sarya = Sarya("sk-...")

@sarya.name("@my-app")
def ai():
    return UI.Text("Hello World!")

sarya.run()
```

### 6. Extra: Mirror 🪞
Here is another app that just replies back to user what they wrote, basically a mirror:
```py
from sarya import Sarya, UI
 
sarya = Sarya("sk-...")

@sarya.name("@my-app")
def ai(messages):
    return UI.Text(messages[0]["content"]) # incoming messages

sarya.run()
```
