---
layout: page
title: Setup Uvicorn to Serve an API within Your Local Network
permalink: 
---

If you want to expose an API endpoint inside your local network during development work you can use Uvicorn. The normal method of launching an App using Uvicorn is:
```bash
uvicorn your_apps_name_here:app --reload
```

This defaults to serving it only on that machine at default location http://127.0.0.1:8000/. To set it up sot that it serves the page at your computer's IP address launch it with this command instead:
```bash
uvicorn your_apps_name_here:app --reload --host 0.0.0.0    
```

You can also change the port by adding the port flag and the desired port, for example:
```bash
uvicorn your_apps_name_here:app --reload --host 0.0.0.0 --port 5000
``` 

Alternatively, you can launch the Uvicorn server programmatically from with your Python code by adding Uvicorn to your import statements and then adding the Uvicorn commands to the __name__="__main__" statement:

```python
if __name__ == "__main__":
    uvicorn.run("your_apps_name_here:app", host="0.0.0.0", port=8000, log_level="info")
```

Then you launch the app from Python:

```bash
$ python your_apps_name_here.py
```

<br>
See the [Uvicorn documentation](https://www.uvicorn.org/settings/) for more information. 

<br>
**Disclaimer** This assumes that you are behind a firewall that will not allow access to that address/port. If you don't know this for sure then don't use this method.
<br>
<br>
Thanks to João Pedro's article on [Towards Data Science](https://towardsdatascience.com/building-a-text-preprocessing-microservice-with-fastapi-ca7912050ba) for getting me started with Uvicorn.
