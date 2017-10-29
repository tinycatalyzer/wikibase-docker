## Install Instructions

#### 1) Install Docker (community edition)

https://docs.docker.com/engine/installation/

#### 2) Install Docker Compose

https://docs.docker.com/compose/install/

#### 3) Clone this repository

```
git clone https://github.com/addshore/wikibase-docker.git
```

#### 4) Start the containers

```
docker-composer up --build
```

## Access Instructions

**Host access**

Access the following hosts:
 - [Wikibase @ http://localhost:8181](http://localhost:8181)
 - [Query Service UI @ http://localhost:8282](http://localhost:8282)
 - [Query Service Backend (Behind a proxy) @ http://localhost:8989/bigdata/](http://localhost:8989/bigdata/)
 - [Query Service Backend (Direct) @ http://localhost:8999/bigdata/](http://localhost:8999/bigdata/)

**Exporting data**

Get a JSON dump from wikibase:

```docker-compose exec wikibase php ./extensions/Wikibase/repo/maintenance/dumpJson.php```

Get an RDF dump from wikibase:

```docker-compose exec wikibase php ./extensions/Wikibase/repo/maintenance/dumpRdf.php```

## Troubleshooting

* [I am on linux and I don't want to run docker as root](https://askubuntu.com/questions/477551/how-can-i-use-docker-without-sudo#477554)