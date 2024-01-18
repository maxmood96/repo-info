<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.16`](#logstash71716)
-	[`logstash:8.11.4`](#logstash8114)

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

## `logstash:8.11.4`

```console
$ docker pull logstash@sha256:13430f55f82887cf5f5b9d06cf9e17321f90294f9def72f4974cc3b0832c95e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.11.4` - linux; amd64

```console
$ docker pull logstash@sha256:35c935ed16cfc6804e1ae0c9294e60c9b964c84e6dc02c6eda8f71ee75a0e34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.7 MB (428729372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1afd84f3dac225a7b0a4fad06be494a38121fae4ff38dfebc44e9edd5a58cb`
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
# Thu, 11 Jan 2024 09:47:01 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.11.4-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.4 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
WORKDIR /usr/share/logstash
# Thu, 11 Jan 2024 09:47:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jan 2024 09:47:01 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 11 Jan 2024 09:47:01 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
USER 1000
# Thu, 11 Jan 2024 09:47:01 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 11 Jan 2024 09:47:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.4 org.opencontainers.image.version=8.11.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-05T16:53:43+00:00 org.opencontainers.image.created=2024-01-05T16:53:43+00:00
# Thu, 11 Jan 2024 09:47:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b722aefd1f164e6b347fff2bc1aac27b9bf2b18bd28b8fdc1b3c39f5bec9ac3`  
		Last Modified: Wed, 17 Jan 2024 22:44:22 GMT  
		Size: 46.7 MB (46707088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636eae443b81bd95faee147ed299356cc2ec738df3e3a4ddd85c45b4aed0c52`  
		Last Modified: Wed, 17 Jan 2024 22:44:21 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f56af6460452845207a8dcb63ffd5c57af826a8aa8f551f4aa6afe4ae143b`  
		Last Modified: Wed, 17 Jan 2024 22:44:27 GMT  
		Size: 352.7 MB (352657454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0685933a22416f7d9925e9f7914e3a904f64d50352372404aef9908399b61a2f`  
		Last Modified: Wed, 17 Jan 2024 22:44:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e807ada9ac22ed0b5c4e06ebdcd204459d60fe5ff889ecbb055df87cfa86dd52`  
		Last Modified: Wed, 17 Jan 2024 22:44:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bad7b9d26d6a1535903f04d65f686a56b4f36ad17e9ea848a877bdae0bf0b8f`  
		Last Modified: Wed, 17 Jan 2024 22:44:22 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0434a75447bdd1ddb5c3a2d61dc242eabef26740fa9c969b0067d051f9a2dc6`  
		Last Modified: Wed, 17 Jan 2024 22:44:23 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b79b827fc4532854322a99cb7ebc0a748942e4fd4b3bfb2fef6092f8093e4f`  
		Last Modified: Wed, 17 Jan 2024 22:44:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9d85f4cb3152074917278d5deed67ec07ed2bdeb022aa0828d468ec74505e`  
		Last Modified: Wed, 17 Jan 2024 22:44:23 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a51610fb6a35c42831a5b4a02886c2a8dadb4db857c96e1eac1c32cf88769d`  
		Last Modified: Wed, 17 Jan 2024 22:44:24 GMT  
		Size: 1.8 MB (1844951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f062abae65d729765fb63274acad0167f409ef2c95b2eecbae413fb49944cd`  
		Last Modified: Wed, 17 Jan 2024 22:44:24 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.11.4` - unknown; unknown

```console
$ docker pull logstash@sha256:c83cdd491a1fb3f7739473e02e883ee86f22eaf5e99620e923179e83358721c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2825122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b78bc1c9788c71beca89774a95673187781db3cdf16e9610c390a9bac6c6999`

```dockerfile
```

-	Layers:
	-	`sha256:388fe9f02af975bea9f6e56203e35e7abef1b82b6f104f43efbbcf916804cc1c`  
		Last Modified: Wed, 17 Jan 2024 22:44:22 GMT  
		Size: 2.8 MB (2790423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7ace750ae8b7d1997e2e0a217390391403dc26e50400e575d2b6762cc146bc`  
		Last Modified: Wed, 17 Jan 2024 22:44:21 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.11.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:9f0c01ad721e5669da54cafbb4368cb0f66fe3c9b35d0b0fa6b2dd7558bf4ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416037822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06252cf4bf4fc7b8313cbf52791cb2635540f666f2cb7149e2388a4aac5f78ce`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Jan 2024 09:47:01 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.11.4-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.4 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
WORKDIR /usr/share/logstash
# Thu, 11 Jan 2024 09:47:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jan 2024 09:47:01 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 11 Jan 2024 09:47:01 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
USER 1000
# Thu, 11 Jan 2024 09:47:01 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 11 Jan 2024 09:47:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.4 org.opencontainers.image.version=8.11.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-05T16:53:43+00:00 org.opencontainers.image.created=2024-01-05T16:53:43+00:00
# Thu, 11 Jan 2024 09:47:01 GMT
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
	-	`sha256:11dc1e82525aec1935911693d97d599f5f6bc36aab9eca62b08121ab7fe830aa`  
		Last Modified: Thu, 18 Jan 2024 10:34:55 GMT  
		Size: 351.5 MB (351474484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960430f10c6b30209099d6467eb811e3491b9192426d2bab5f0bae841d0a9e71`  
		Last Modified: Thu, 18 Jan 2024 10:34:46 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b7e35da91ad8a387fcac2d5796f3761307aa18debe59937bbd0192e169bb1f`  
		Last Modified: Thu, 18 Jan 2024 10:34:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804cff081de8b01a6de09e441d91a7a8a423223d25619882dad173630b4cbdc`  
		Last Modified: Thu, 18 Jan 2024 10:34:46 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e17e46afa9ec5aaba463d295af536913d22bdbf5d9d9bee1c278e5722a5d15`  
		Last Modified: Thu, 18 Jan 2024 10:34:47 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357aa2ef341df4b6676c9acfddd2ab5686ac42489f1ac602a8865b146fc40361`  
		Last Modified: Thu, 18 Jan 2024 10:34:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33e83a400d6d50ee3417b0978d66e84ec3ee10c26f1f9400b756025e28917d0`  
		Last Modified: Thu, 18 Jan 2024 10:34:47 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78d0ada97c1383dd6c5fbd7c021bed70178351e32998b255c252e415df17c7e`  
		Last Modified: Thu, 18 Jan 2024 10:34:49 GMT  
		Size: 1.8 MB (1844950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bc8001737b550fe6c5492575f2ddd9e13dc89f55ed0fd2951c4c69834a2a53`  
		Last Modified: Thu, 18 Jan 2024 10:34:48 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.11.4` - unknown; unknown

```console
$ docker pull logstash@sha256:458a7d91d02a9a762ebc806146d92956a5a8e446dd58745ebcec6dda023f97b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2825291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445aee6e6635598ea482e042a3146c8384c58060cfc63c81e34181089eac4346`

```dockerfile
```

-	Layers:
	-	`sha256:acf0edd0ecf7d315af186b6c6299dacadd574ef8af4322d255bad898f154a2cf`  
		Last Modified: Thu, 18 Jan 2024 10:34:47 GMT  
		Size: 2.8 MB (2790749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d2146cd7f0d3a268b7d9aa9ac4f64572e9c63c3b295d408228fd99cea234640`  
		Last Modified: Thu, 18 Jan 2024 10:34:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json
