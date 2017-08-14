# The nodezoo microservice demonstration architecture

This is a repository in the microservice demonstration system for
the [Tao of Microservices](//bit.ly/rmtaomicro) book (chapter 9). This
code is live at [nodezoo.com](//nodezoo.com).

This system shows you how to construct a full microservice
architecture. It is MIT licensed so that you can cut-and-paste to
build your own system with minimal effort. The system consists of
multiple repositories, and runs ten or so microservices in production
([Kubernetes](//kubernetes.io)), staging ([Docker](//docker.com)), and
development ([fuge](//github.com/apparatus/fuge)) modes.

## Nodezoo

The nodezoo system is a little search engine
for [Node.js](//nodejs.org) modules, using
the [npm module registry](//npmjs.com) (among others) as an external
data source.


## Getting started

Follow these instructions to get a demonstration nodezoo system up and
running.

1. Checkout this repository.
  ```
  $ git clone https://github.com/nodezoo/tao.git
  ```

2. Checkout all the microservice repositories.
  ```
  $ ./tao/clone-all.sh`
  ```
  
3. Install all the modules.
  ```
  $ ./tao/npm-install.sh`
  ```

4. Install and run a [development instance of ElasticSearch](https://www.elastic.co/guide/en/elasticsearch/reference/5.5/_installation.html).
  
5. Start up the system by running the local development environment
  using ([fuge](//github.com/apparatus/fuge)).
  ```
  $ cd system
  $ ./node_modules/.bin/fuge shell fuge/fuge.yml
  ```

6. Index a few modules, by visiting the _info_ page in your browser.
  * [http://localhost:8000/info/express](http://localhost:8000/info/express)
  * [http://localhost:8000/info/hapi](http://localhost:8000/info/hapi)
  * [http://localhost:8000/info/seneca](http://localhost:8000/info/seneca)

7. Search for modules.
  * [http://localhost:8000/#q=express](http://localhost:8000/#q=express)


## List of repositories

* [nodezoo-system](//github.com/nodezoo/nodezoo-system)
* [nodezoo-repl](//github.com/nodezoo/nodezoo-repl)
* [nodezoo-web](//github.com/nodezoo/nodezoo-web)
* [nodezoo-search](//github.com/nodezoo/nodezoo-search)
* [nodezoo-info](//github.com/nodezoo/nodezoo-info)
* [nodezoo-npm](//github.com/nodezoo/nodezoo-npm)
* [nodezoo-github](//github.com/nodezoo/nodezoo-github)
* [nodezoo-suggest](//github.com/nodezoo/nodezoo-suggest)



