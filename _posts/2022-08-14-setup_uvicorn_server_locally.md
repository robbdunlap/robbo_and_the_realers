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
uvicorn your_apps_name_here:app --host 0.0.0.0    
```

You can also change the port by adding the port flag and the desired port, for example:
```bash
uvicorn your_apps_name_here:app --host 0.0.0.0 --port 5000
``` 

See the [Uvicorn documentation](https://www.uvicorn.org/settings/) for more information. 

**Disclaimer** This assumes that you are behind a firewall that will not allow access to that address/port. If you don't know this for sure then don't use this method.
