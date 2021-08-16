# Web Crawler
Goal of this project is to build a standalone crawler that will crawl only .gov.si web sites. The crawler will roughly consist of the following components:

- HTTP downloader and renderer: To retrieve and render a web page.
- Data extractor: Minimal functionalities to extract images and hyperlinks.
- Duplicate detector: To detect already parsed pages.
- URL frontier: A list of URLs waiting to be parsed.
- Datastore: To store the data and additional metadata used by the crawler.

# How to run web crawler?
Web Crawler runs on Linux Ubuntu OS. 

You are going to need to install: 
- Python 3.6
-  Anaconda
-  Docker

For running Web Crawler run commands: 

```
conda create -n wier python=3.6
conda activate wier
conda install nb_conda
pip install beautifulsoup4
pip install json
pip install ultimate_sitemap_parser
```

For running database with Docker run command: 

```
docker run --name postgresql-wier -e POSTGRES_PASSWORD=SecretPassword -e POSTGRES_USER=user -v $PWD/pgdata:/var/lib/postgresql/data -v $PWD/init-scripts:/docker-entrypoint-initdb.d -p 5432:5432 -d postgres:9
```
Run web crawler with ```python fetch-data-frontier.py.```
