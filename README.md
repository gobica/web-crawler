# Web Crawler

YOu are going to need: 
	- installed Python 
	- installed Anaconda
	- installed Docker

Web Crawler runs on Linux Ubuntu OS. 

For running Web Crawler run commands: 


conda create -n wier python=3.6
conda activate wier
conda install nb_conda
pip install beautifulsoup4
pip install json
pip install ultimate_sitemap_parser


For running database with Docker: 


docker run --name postgresql-wier -e POSTGRES_PASSWORD=SecretPassword -e POSTGRES_USER=user -v $PWD/pgdata:/var/lib/postgresql/data -v $PWD/init-scripts:/docker-entrypoint-initdb.d -p 5432:5432 -d postgres:9

Run web crawler with 

python fetch-data-frontier.py.
