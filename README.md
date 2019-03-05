### twitographer -- a parallelized web crawler to traverse the twitter graph
--------

**this is a tiny script that uses [miyakogi's python port](https://github.com/miyakogi/pyppeteer) of [google's puppeteer headless browser](https://github.com/GoogleChrome/puppeteer) to traverse the twitter graph, logging the friends of each account.**

i wrote this for a big data analysis project to infer twitter communities from aggregated social relationships.

add your twitter username and password to `credentials.py` before running.

twitographer determines the number of processes to spawn via:
```python
from credentials import creds
if len(creds) <= multiprocessing.cpu_count():
   num_processes = len(creds)
else:
   num_processes = multiprocessing.cpu_count()
```
### installation

(requires python >= 3.0, redis >= 1.0.0)

-------
###### matthew jack <{username}@uiowa.edu>
