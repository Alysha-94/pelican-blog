Title: Python http server
Date: 2019-07-10 12:00pm
Category: Python
Tags: python
Summary: Using python http server for local development.

Python3 has a built-in http server that is very simple to set up with `python -m http.server`.

A port number can also be specified with `python -m http.server 8001`

If no port number is set it will be served on the default port 8000.

I have been using this to run a basic server and preview my changes on my Pelican blog.

After running `make html` to generate the output folder:
```
cd output
python -m http.server
Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...
```
Now the server has started and the site can be viewed on http://localhost:8000/

Note: For Python 2 `SimpleHTTPServer` must be used instead.