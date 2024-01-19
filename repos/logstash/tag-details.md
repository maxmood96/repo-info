<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.16`](#logstash71716)
-	[`logstash:8.12.0`](#logstash8120)

## `logstash:7.17.16`

```console
$ docker pull logstash@sha256:fe1d1deae29a50f4debff76f3cc5c35e38e0a1ec85a969e09edffd9b6b44b884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.16` - linux; amd64

```console
$ docker pull logstash@sha256:5697365f635b36c9e1d31e7e9f2267f68f00fc4f043993f24119b56bfeae4ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.5 MB (442459266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57c02986aff5a07aefeec38cb21cdcc2fc547cf8638bb8cd3da721616a069f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Dec 2023 12:49:29 GMT
ARG RELEASE
# Tue, 12 Dec 2023 12:49:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 12:49:29 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.16-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.16 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Dec 2023 12:49:29 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
USER 1000
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.16 org.opencontainers.image.version=7.17.16 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-12-05T12:24:52+00:00 org.opencontainers.image.created=2023-12-05T12:24:52+00:00
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b06c5dca594470c89da01558ef1c3de546a60c9b4bf8179cf3c8855e2a8fe0d`  
		Last Modified: Sat, 16 Dec 2023 10:50:16 GMT  
		Size: 46.2 MB (46236266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc64dced61e148e93c0c7bc3d0fa499c02a461d2bbaa41210c75b0a827a9190`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5f9ac6c993a06ad6f4467fd99e7e1ea1bd8a1f9969197fe941f984130ba71`  
		Last Modified: Sat, 16 Dec 2023 10:50:23 GMT  
		Size: 366.9 MB (366860871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb35e856eef4d12e6be07a3e9e2c2d2ee962f716b571373ea972848c1c633d94`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d48d7debcb2279967b1bb6d73ec18fb0e4e83ff06ca7935cb8b03d26799e5`  
		Last Modified: Sat, 16 Dec 2023 10:50:15 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cd3c458bb3eef6b4aebe4144ea8284acde0f9ef48f41f21801b2442575f641`  
		Last Modified: Sat, 16 Dec 2023 10:50:15 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c371eb5570bb1f91b520ff2dbe59a2fd14bf2ff2670058acbaa3670ccb7f7f03`  
		Last Modified: Sat, 16 Dec 2023 10:50:16 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c83485e548a3c4d434ee54e21db841aa69db40cdd42044f35133f38aa86994`  
		Last Modified: Sat, 16 Dec 2023 10:50:16 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024c092c7c3ed11178281002b921000945aaaa0004f4f35718b3c6e3dd3f574c`  
		Last Modified: Sat, 16 Dec 2023 10:50:18 GMT  
		Size: 1.8 MB (1844765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfc37efa4bc959f0d2daa2f26ff99e19c3ed9fce8d6552297cc66880773d6a2`  
		Last Modified: Sat, 16 Dec 2023 10:50:17 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.16` - unknown; unknown

```console
$ docker pull logstash@sha256:2a6733630283a591b0502401da03d91b0cf899a4ba479c986ed11cb0903e52c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74c3405ded8f97331269df58cf00fc83ab26ea35bab252979961c449e142a8d`

```dockerfile
```

-	Layers:
	-	`sha256:f9311f864e03030450bad3c70ae5e3ceee348a696c6897da5adc53c4923b8b68`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 2.7 MB (2673371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971351e1ea36e7785ff28f24b50d32219498e73560afdecefae4d118cad5e303`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 32.2 KB (32169 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.16` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:dfe5734a8fca811c6ff3dfbd8ac8a599e2d3664d09f23e8bebdd4a593c67f34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.2 MB (428156580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f738760390b11e732b615d6fd436c81f368db0a87da75034bfb02810424a37`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 12 Dec 2023 12:49:29 GMT
ARG RELEASE
# Tue, 12 Dec 2023 12:49:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 12:49:29 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.16-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.16 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/logstash
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 12 Dec 2023 12:49:29 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
USER 1000
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.16 org.opencontainers.image.version=7.17.16 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-12-05T12:24:52+00:00 org.opencontainers.image.created=2023-12-05T12:24:52+00:00
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1e7d71d662fea3176db34f01e2afb22468596910909062e42889cb2be6766`  
		Last Modified: Mon, 18 Dec 2023 19:59:02 GMT  
		Size: 36.7 MB (36736504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28fe55da162ade1eb87e2a8e5383c00e22edf99c2e9c1f861f35bb42281cdd2`  
		Last Modified: Mon, 18 Dec 2023 19:59:01 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ff03f781408581c158b36cbaabb08084f15719491190e4d1a0178688ea1af`  
		Last Modified: Mon, 18 Dec 2023 20:00:06 GMT  
		Size: 363.6 MB (363595954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e6080b79db201b78a9f1499a15560bee1ead79dae310acc08d41f9290aab22`  
		Last Modified: Mon, 18 Dec 2023 19:59:56 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ec27b3e010a35ca3ae47a54c0c74d658732caf84c6dcc70d9e980170467a9e`  
		Last Modified: Mon, 18 Dec 2023 19:59:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fcb35737917972d4681a08acade07b83888badd66f22b9624ea452b1e991c3`  
		Last Modified: Mon, 18 Dec 2023 19:59:56 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515a6be9a79f59c9566f5317225e36e1bcc180fce88cc33e23982a2e059f0c`  
		Last Modified: Mon, 18 Dec 2023 19:59:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0334396271f019408d440d907d6b1d8a8d88adf9faf1a9716278ff13cc9a8b`  
		Last Modified: Mon, 18 Dec 2023 19:59:57 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e20ebe92786ad0673efda66170ca76ee31ef8b81ab4eed26aeaad5b3fbdfc`  
		Last Modified: Mon, 18 Dec 2023 19:59:57 GMT  
		Size: 1.8 MB (1844765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6463a73bcc880680060e5e7f9a12b8b4aefdfd09007be757af8cabcc2e5caf`  
		Last Modified: Mon, 18 Dec 2023 19:59:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.16` - unknown; unknown

```console
$ docker pull logstash@sha256:bea08338d34323b0e4097cff57bfb59352b4c3b672af921240c9548914497227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4bb68aedeb5395bd12ccbb27a6130d8310542a05f8cf0f87c727c1cd74c6c53`

```dockerfile
```

-	Layers:
	-	`sha256:30dbb673facae481ed3d31e45475149fc89b00e089dc3059d90bfdacf302bc09`  
		Last Modified: Mon, 18 Dec 2023 19:59:56 GMT  
		Size: 2.7 MB (2673699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92abafc051904fcf46bbdbd53611db70acb224d076124f633e8535f8903e31fd`  
		Last Modified: Mon, 18 Dec 2023 19:59:56 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.12.0`

```console
$ docker pull logstash@sha256:1f1e8eea1e24c74e0e67e7fe19b19be6637fdcd402f06afc496db51db3d19198
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `logstash:8.12.0` - linux; amd64

```console
$ docker pull logstash@sha256:93a961224d68e8139f31dd21d5ed3b18b388aa4e5b7a92a6b3afb298c97152c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.8 MB (428847253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7fc1f8688f0e42dfe5340cab60a93ca66453dea147fcb35b2ee4c54600d002`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 15:49:20 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.12.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.12.0 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
WORKDIR /usr/share/logstash
# Wed, 17 Jan 2024 15:49:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 17 Jan 2024 15:49:20 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/log4j2.properties config/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 15:49:20 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
USER 1000
# Wed, 17 Jan 2024 15:49:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.12.0 org.opencontainers.image.version=8.12.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-10T10:50:49+00:00 org.opencontainers.image.created=2024-01-10T10:50:49+00:00
# Wed, 17 Jan 2024 15:49:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae3b777ac42d37164270746a7fed119e1451acf7f00ad41b1a69f2394436788`  
		Last Modified: Thu, 18 Jan 2024 18:14:02 GMT  
		Size: 46.7 MB (46711937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92b3142091a02d379f123186cfd4916334734774af9617cc78f1de753e59004`  
		Last Modified: Thu, 18 Jan 2024 18:14:01 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59a0d1c1a7b4e89f1b18d7c41c1aa31e75ef52736492a20da42b8931527267f`  
		Last Modified: Thu, 18 Jan 2024 18:14:09 GMT  
		Size: 352.8 MB (352770291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffb0279d715abfd6b8ec55a945cb581dca147a39f864e2c5e21f3b9dc68615b`  
		Last Modified: Thu, 18 Jan 2024 18:14:01 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579b26ae566baa9696c3cbddc3716db6465ed63cc5a38fbc02a1c941e1d39619`  
		Last Modified: Thu, 18 Jan 2024 18:14:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4375ce7f00abff6d757aa2797fbe163849b296573beea47fffa58c37d8f3af6f`  
		Last Modified: Thu, 18 Jan 2024 18:14:02 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684831e4d05823043f47b494a45f6cbd6b1b41c50276fe572e27796a47f570b0`  
		Last Modified: Thu, 18 Jan 2024 18:14:03 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9b4b23c7f96fc17c140882e88cf1b495defc20a4d898e01586eba7db0f260f`  
		Last Modified: Thu, 18 Jan 2024 18:14:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6688533869056fc0ca2cc275e015444a5ed8206f1dcd91ffc62f3ecea43db59`  
		Last Modified: Thu, 18 Jan 2024 18:14:04 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb2d8abef7817a5a99e32d291f5d95edc72235b0a35f8866913d0f895736918`  
		Last Modified: Thu, 18 Jan 2024 18:14:04 GMT  
		Size: 1.8 MB (1845136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f222dc48749d926bbe98f4953522b8e5c0d78c7def5b7bbb348b80da4f3a5`  
		Last Modified: Thu, 18 Jan 2024 18:14:04 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.12.0` - unknown; unknown

```console
$ docker pull logstash@sha256:8987f316948ad87586943c33a7cd5150fd483a8656c5d8197456a492c1ed78d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2825244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea003c694caa32ba180929d164ec199dba4da4541830064f35e9a53619365722`

```dockerfile
```

-	Layers:
	-	`sha256:69a225ce532944b8fa59b0d22c99277961b24577fa160aaca29719a23eb9c826`  
		Last Modified: Thu, 18 Jan 2024 18:14:01 GMT  
		Size: 2.8 MB (2790545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0623a2051f68fcf1c451227d423699a8fe94e58b5bfe33f20402ba30f5cb6e02`  
		Last Modified: Thu, 18 Jan 2024 18:14:01 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json
