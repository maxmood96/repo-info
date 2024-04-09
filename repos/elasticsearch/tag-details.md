<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.20`](#elasticsearch71720)
-	[`elasticsearch:8.13.0`](#elasticsearch8130)

## `elasticsearch:7.17.20`

```console
$ docker pull elasticsearch@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `elasticsearch:8.13.0`

```console
$ docker pull elasticsearch@sha256:e70e2bc1f88987edac86e0b0a95f18e0e5b0b6e34eaf37074aa4aa5f6919b603
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.13.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2e06e0c83c551485faf8d49c354dbcbe5757f66fa82f27e753b36e2d3aa4b746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615312389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba1a371c8e771b1af9dc46432534d20c7d630e67e27c3a7ba4924c99454fa38`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T03:35:46.757803203Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=09df99393193b2c53d92899662a8b8b3c55b45cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T03:35:46.757803203Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=09df99393193b2c53d92899662a8b8b3c55b45cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["eswrapper"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b190db87e221cc1308d2e688ea9a83e09dda1b55ec50e9972f3dc260f0154f7`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 7.5 MB (7512513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa109031a696acdb26e523b807153d6070daaa043d16fc00fbf2bf4defab3d9d`  
		Last Modified: Tue, 26 Mar 2024 18:50:50 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08466127fcdb52493482da50e03efa0d702e3ae1a7c5d2823ae6513b9a9edd5f`  
		Last Modified: Tue, 26 Mar 2024 18:51:01 GMT  
		Size: 580.0 MB (579968400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5861b544bdb8bb365de4f07eb5ae84053d4f11ad0e955f4d7c72c9e3186d8ba1`  
		Last Modified: Tue, 26 Mar 2024 18:50:50 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d6b772957a38409db17e87e372cc3e107a3c53b7f2061c5692ab5bbd2ca838`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8288a7b93c5b6b6c37d89cebdbfad8082d65fad0dae864f472ec32b6ea7d9c`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 191.9 KB (191906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b4d3945e0f22a1f0150a19f73c269d35767c45d686dadc31a5c74763e05bbb`  
		Last Modified: Tue, 26 Mar 2024 18:50:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0122d88049315688a64c2a92b4b767e4dab2f3d874a3809f2f3db32c8549ec52`  
		Last Modified: Tue, 26 Mar 2024 18:50:52 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a2d8ae470c19a09fbd4c542d256ea179fe7644f08eb810aeb74e19aa4c582fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2eb6512b147ac967b87700dcaf456d1e8faf1f678ba6d2590a2452d082f5c69`

```dockerfile
```

-	Layers:
	-	`sha256:be8677b7c6276cb489c32d8da09c93c7ac927be31371fff2551d27cbf6f0c6fa`  
		Last Modified: Tue, 26 Mar 2024 18:50:51 GMT  
		Size: 2.6 MB (2590070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff309f0a22fe7d63df20b866644a34b82455e672f37ea622c1b72f69cadedc9`  
		Last Modified: Tue, 26 Mar 2024 18:50:50 GMT  
		Size: 37.8 KB (37757 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.13.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:223e8fa0331a01364ba1ee7d5a4ec219d047ebadc8231d570ff87fca0b1da6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.4 MB (459420510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bfb2697483e0bdc9d3c0208a4fb9f579455a75403c7be9d5945bfbad904848`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T03:35:46.757803203Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=09df99393193b2c53d92899662a8b8b3c55b45cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T03:35:46.757803203Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=09df99393193b2c53d92899662a8b8b3c55b45cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["eswrapper"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14e5e1b762bfecd88ab86a4faf77d6a3199d588e85e7407913816371679657a`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 7.3 MB (7331903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf899c8d88bb7608d07eda424716015466893306895ab7e5d094900f153bdb26`  
		Last Modified: Tue, 26 Mar 2024 18:56:00 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b9969e4f4e4faabe36f710e31bbca65b235109f03bc43a6e7dd94c9b5f5dbe`  
		Last Modified: Tue, 26 Mar 2024 18:56:11 GMT  
		Size: 425.8 MB (425803447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1079e422fd69fed0509b31ce2fc1f3693607fec5e6f46e8c15ae5cdf4e55ee2e`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46279a912b6b1e38401f4b7d596a076a4e67bbf6b313878c66c6cc9ca52942e8`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb703192bdef9a2b254da889a3c1524adce873cda1f5f1a6f63352820d2a8e2`  
		Last Modified: Tue, 26 Mar 2024 18:56:02 GMT  
		Size: 185.9 KB (185932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b83a0c8d826e0a6159aa7233c85c9ebc232b80fe0c9479fef82752e5f16b1f7`  
		Last Modified: Tue, 26 Mar 2024 18:56:02 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81667493e1e6af1edbc07bcf742326013af80e6a6824930665c5a0b14ae65150`  
		Last Modified: Tue, 26 Mar 2024 18:56:03 GMT  
		Size: 109.3 KB (109259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d7b8e95a5f259c766897378b2c2028350bf9cb3ca132445f3b2523ffe2d50008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b2569b2880376d1da7828aa0f2a8e4ab1ce781dc8f5f410b83733f391091e2`

```dockerfile
```

-	Layers:
	-	`sha256:40eb042c66842dd8ee05f2eb974a7139247f1be77e74cc218dfa24b658a5767f`  
		Last Modified: Tue, 26 Mar 2024 18:56:01 GMT  
		Size: 2.6 MB (2590303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c56700f68e57448d8b6376e76f982da10345b8301993c12963c4d32ea5e65d`  
		Last Modified: Tue, 26 Mar 2024 18:56:00 GMT  
		Size: 37.8 KB (37762 bytes)  
		MIME: application/vnd.in-toto+json
