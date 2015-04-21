# hello.docker.els

A quick experiment to provision [ElasticSearch](https://registry.hub.docker.com/_/elasticsearch/) using vagrant and docker.

## Prerequisites

You should have installed

- [VirtualBox](https://www.virtualbox.org/) (v4.3.26)
- [vagrant](https://www.vagrantup.com/) (v1.7.2)

## Proxy configuration

When working in a proxy environment, be sure to 

- install the [vagrant-proxyconf](https://github.com/tmatilai/vagrant-proxyconf) plugin,
- configure proxy settings in `$HOME/.vagrant.d/Vagrantfile` and
- include `/var/run/docker.sock` in your no-proxy settings as suggested in [vagrant-proxyconf/issues/97](https://github.com/tmatilai/vagrant-proxyconf/issues/97#issuecomment-88661401)

## How to use

Just go `vagrant up` and after vagrant and docker have done their magic you should be able to access a running elasticsearch instance at [http://localhost:9200](http://localhost:9200)

	{
	  "status" : 200,
	  "name" : "Kleinstocks",
	  "cluster_name" : "elasticsearch",
	  "version" : {
	    "number" : "1.4.4",
	    "build_hash" : "c88f77ffc81301dfa9dfd81ca2232f09588bd512",
	    "build_timestamp" : "2015-02-19T13:05:36Z",
	    "build_snapshot" : false,
	    "lucene_version" : "4.10.3"
	  },
	  "tagline" : "You Know, for Search"
	}

