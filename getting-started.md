---
layout: default
title: Getting started
nav_order: 2
description: "..."
permalink: /getting-started
---

##  Getting started

Sarya is a python framework for building, and publishing AI applications. It simplifies the process of publishing your projects with user-friendly interfaces across multiple platforms.

<br/><br/>
In order to get started make sure you sign-up and get your `SECRET` key from the developer platform at [platform.sarya.com](https://platform.sarya.com).
### Install

```sh
pip install sarya
```

### Define sarya client

make the `Sarya` client with your key:

```py
from sarya import Sarya, UI

sarya = Sarya("SECRET")
```

### Add entry-point to your app
Add the entry-point of your application with a `@sarya("@name-of-your-app")`:
```py
@sarya("@name-of-your-app")
def app():
    return UI.Text("Hello World!")
```
In this example, the function responds with "Hello World!" to each user request.

### Publish the app
Publish your app by adding `run` at the end of your file:
```py
sarya.run()
```

### Hello World!
The full code:
```py
from sarya import Sarya, UI

sarya = Sarya("SECRET")

@sarya("@name-of-your-app")
def app():
    return UI.Text("Hello World!")

sarya.run()
```
