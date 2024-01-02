---
layout: default
title: Getting started
nav_order: 2
description: "..."
permalink: /getting-started
---

##  Getting started

Sarya is a python framework for building, and publishing AI applications. It provides everything you need to transform your project into beautiful UI across multiple platforms. 

<br/><br/>
In order to get started make sure you sign-up and get your `SECRET-KEY` from the developer platform at [platform.sarya.com](https://platform.sarya.com).
### 1. Install

```sh
pip install sarya
```

### 2. Initiate Sarya Client

make the `Sarya` client with your key:

```py
from sarya import Sarya, UI

sarya = Sarya("SECRET")
```

### 3. Add the Entry Point
Define the entry point of your application with a `@sarya("@my-app")`. In this example, the function responds with "Hello World!" to each user request.
```py
@sarya("@my-app")
def ai():
    return UI.Text("Hello World!")
```

### 4. Hello World! 👋
The full example:
```py
from sarya import Sarya, UI

sarya = Sarya("SECRET")

@sarya.name("@my-app")
def ai():
    return UI.Text("Hello World!")
```
