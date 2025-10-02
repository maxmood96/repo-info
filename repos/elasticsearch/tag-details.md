<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.7`](#elasticsearch8187)
-	[`elasticsearch:8.19.4`](#elasticsearch8194)
-	[`elasticsearch:9.0.7`](#elasticsearch907)
-	[`elasticsearch:9.1.4`](#elasticsearch914)

## `elasticsearch:8.17.10`

```console
$ docker pull elasticsearch@sha256:8f67ac52551ded038189abf3c6d2e99e762471b47594df3d57cf4b7fe19fa334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2a1b28ba53061e0943a06ffe1930ecfee92b90fbeaaa249cf064f3ee73b0ecc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.4 MB (679358283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02860478f7aaf0f993fead2f057ed364c11289edeb665c70c7bc7722d15e6b8c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ebd38a500f2fe5024ec7a31c21d02379a758a0646282bca76ad155208cb472`  
		Last Modified: Thu, 02 Oct 2025 05:05:05 GMT  
		Size: 6.9 MB (6893762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7afcc9426d341dfb32f78b0ed8a4a584fc489dd3defa3bf75e0c45f4acc85c`  
		Last Modified: Thu, 02 Oct 2025 05:05:02 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7246d3930d58778334ee5f57ab62d59369261dab2c0bed761d3e8bb7ebb6484a`  
		Last Modified: Thu, 02 Oct 2025 05:18:21 GMT  
		Size: 642.4 MB (642446819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c94b9062df367b8a2c931023ac97ae9f3372e7915ed79d5d8f89cc27ca419f`  
		Last Modified: Thu, 02 Oct 2025 05:05:02 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ff2881eced0b29df619fb62156d7d7632070bb2b290e7324de483efddab5a5`  
		Last Modified: Thu, 02 Oct 2025 05:05:03 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad21e81ebe763124e174c54aad8256edbe2ba8de54c5ee19612aac6b0f070e1`  
		Last Modified: Thu, 02 Oct 2025 05:05:03 GMT  
		Size: 163.9 KB (163936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4112aedce0fb927cd619b23a9f894c4b4bf1706c794cd7535d8719612031c24b`  
		Last Modified: Thu, 02 Oct 2025 05:05:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c35b7a0cf3fd8e2ffb2e1cbdee35be0c8dd41013774330c229b265319f5d535`  
		Last Modified: Thu, 02 Oct 2025 05:05:03 GMT  
		Size: 115.5 KB (115540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:524a7551617228c14f1accd3700cafb9d38aaf0028cb5114a764b5143cce5a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f94704c5148694e584b0d332e36f93663a34692b63153448226347eb9231a8d`

```dockerfile
```

-	Layers:
	-	`sha256:b40745cfda1b1e15a1ea5deb59449924c75cd793b29568c565314134bc9ac906`  
		Last Modified: Thu, 02 Oct 2025 06:25:18 GMT  
		Size: 3.2 MB (3164785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e81910b24c65f2d23d1826f1493176c5204a26ca227447e23a46df073829fa0`  
		Last Modified: Thu, 02 Oct 2025 06:25:19 GMT  
		Size: 38.4 KB (38396 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:8ccc721242c7e6e21043b1aacb0b3208fc128e384ff4aa3670442006d3aed764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.4 MB (523379141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8a779e36f750522751773ace431d09f5b9803974c9891aa28e2894ab1fbdab`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f4998ecdc7422150cbcf37116ccb6d2b92c6754470e9e6c59dfbd71ed78cb2`  
		Last Modified: Thu, 02 Oct 2025 01:20:03 GMT  
		Size: 6.7 MB (6712723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729a1b4130c206e65e8c3bafccb5d560af995976c88c95cbbef66754766fdcd2`  
		Last Modified: Thu, 02 Oct 2025 01:20:03 GMT  
		Size: 3.5 KB (3523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf98a78d7a29e8236d3c5d2e4f8df893e321babc5de3c1d024ec273c34aeafe`  
		Last Modified: Thu, 02 Oct 2025 03:28:21 GMT  
		Size: 487.5 MB (487514152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec09b1dfb27f0a271564b23ac2b16c7ffb7583b5223e9adc16b3d23d00a0195`  
		Last Modified: Thu, 02 Oct 2025 01:20:03 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88bdae5fbb785cc8f7660f63716ae0c8784b1530c1e90efdfb32848e564943`  
		Last Modified: Thu, 02 Oct 2025 01:20:03 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994af5ad32d30b14d208553d44759eff66ccafacbf1b32e22003c81a3acf619d`  
		Last Modified: Thu, 02 Oct 2025 01:20:04 GMT  
		Size: 160.4 KB (160365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c620b56563574e2679dd79ca12585a4b08fce7f6783157185aeec7afc3297c7`  
		Last Modified: Thu, 02 Oct 2025 01:20:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0c6a1bf6619bc2be0d76661ca42a4b4d79c13ce56c0a041c2b9e68a5d46e3`  
		Last Modified: Thu, 02 Oct 2025 01:20:04 GMT  
		Size: 115.5 KB (115545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5745637d36b73596515d802cdb172d1fb4c33833162dfe916cba2f45baf89d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa081de98bfe6bfb332be98be117b3acfce907b84a0426f5fe4ae4d80b97066`

```dockerfile
```

-	Layers:
	-	`sha256:8de8067855769e5dcad12d8e4550b4b7efbc0abe312693023acbc973e3d979da`  
		Last Modified: Thu, 02 Oct 2025 03:25:20 GMT  
		Size: 3.2 MB (3164569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:864fb2203f1b5f737372fdc650abb29c99d25e1e6acacfaaf95ddc0a5496ffc1`  
		Last Modified: Thu, 02 Oct 2025 03:25:21 GMT  
		Size: 38.6 KB (38598 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.7`

```console
$ docker pull elasticsearch@sha256:c77b0f094643c2127d9ff7b2c0fedf0852c66aa190ff830ab169fff67f9625b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e0623eaa49a7c2aae702a4c7f1dbf5c5c93f0d136d76bea7acdbd62172e8417e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.0 MB (690977792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7fa774d59e5106760a081a9493102c8fecf4e6063faf9978df3c93ab2dd40b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
ARG RELEASE
# Tue, 16 Sep 2025 08:32:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Sep 2025 08:32:12 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:04:56.853519418Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T22:04:56.853519418Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b88e968374672e43b1a426b80b07c9dfff2eb650f74b2adacda79a9af0f879`  
		Last Modified: Thu, 02 Oct 2025 05:05:04 GMT  
		Size: 6.9 MB (6893769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b784063840c56ebf2ef86d3dac44e57214cbb82f5b31ee51c7334fb34f50e789`  
		Last Modified: Thu, 02 Oct 2025 05:05:03 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26e34be4b1fbf437b496134937120b9a4072167157ed55d85060452e6ed4e7b`  
		Last Modified: Thu, 02 Oct 2025 06:26:07 GMT  
		Size: 654.1 MB (654066339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b832ee954d0f8c630274674b91b47645475056ea3211aece2faf031861004`  
		Last Modified: Thu, 02 Oct 2025 05:05:03 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134f8fb92aeef9c0a1f7a1e7c246a39252736ba5605b7670109878050afd889b`  
		Last Modified: Thu, 02 Oct 2025 05:05:04 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cd39fce4b6ddcaf8d23f031173768d4f587c559fb1957ccc4563dbde903656`  
		Last Modified: Thu, 02 Oct 2025 05:05:04 GMT  
		Size: 163.9 KB (163929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad7bfd61287620cf0fb61f0b96b97c914193b04ea5579b6b13fc98543e9b371`  
		Last Modified: Thu, 02 Oct 2025 05:05:03 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae90bd926baee02209323feae701234e65537a9a012d2b8d0fdc1efa83c3868f`  
		Last Modified: Thu, 02 Oct 2025 05:05:03 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2b781beff157211e268cd9a055aa9e234855863aae50aebd9da54c9b26d35463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ba03e827c72690bde585dd930dc13aeb3118cff792ed3b6ba7a9fa354ecc0c`

```dockerfile
```

-	Layers:
	-	`sha256:5f730bcbc5cdc981b6d481a9e5ed0b8ae04c92ba2289efdec9905011bb1b130c`  
		Last Modified: Thu, 02 Oct 2025 06:25:22 GMT  
		Size: 3.2 MB (3192742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8537b2c7756ed37e0c9daa47ec73579922a25040035c7401d20884b289c1a8`  
		Last Modified: Thu, 02 Oct 2025 06:25:23 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:fb99415e0c47865160655a0cc3aeef79f417b7d3c0ea2471fdffa8a2750313b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.2 MB (533206256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657455d4df2a1243b833b1bb19606e4607f58194366a9e62570a61c5b43ff6ab`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
ARG RELEASE
# Tue, 16 Sep 2025 08:32:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Sep 2025 08:32:12 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:04:56.853519418Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T22:04:56.853519418Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23c1f9d02276c78128d106edba5f0458fe7cb201ec2c82085d3419a83c2b9b6`  
		Last Modified: Thu, 02 Oct 2025 01:20:05 GMT  
		Size: 6.7 MB (6712709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c919b29861578812510e4f7b23405b2ba7be5957a4d9793bf82364d3ab73a5c`  
		Last Modified: Thu, 02 Oct 2025 01:20:04 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2918d1915826c5df8543aeb56c4a1140110f39bbe28a60a80243513e78ee686d`  
		Last Modified: Thu, 02 Oct 2025 02:28:08 GMT  
		Size: 497.3 MB (497341288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9380bb6a3c4dd95cec602cb79408e12cdcc71e5e280bf59999d4001f235356`  
		Last Modified: Thu, 02 Oct 2025 01:20:04 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908ff19878db11bb1853ed2be9a463f66a6b4ba884c0bce84277637541a53eac`  
		Last Modified: Thu, 02 Oct 2025 01:20:04 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b86910ddb106b2773fcb6ae89a805050b8b90a864c70b81f92630bbfdcf14af`  
		Last Modified: Thu, 02 Oct 2025 01:20:04 GMT  
		Size: 160.4 KB (160364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59723965f29c8704b674fc2ca02c305d8b31d231b5605aca7deaffc5bbcee4a7`  
		Last Modified: Thu, 02 Oct 2025 01:20:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3df87333cb7e40a3330668e09651062b13ae076313222cd6ebbb462412e0f2`  
		Last Modified: Thu, 02 Oct 2025 01:20:05 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:da532feb8a9e8f59a3b5389abb2b337ba3091b770c9a8fa367fbb3038aed2d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc6a7d90a250f0bc0b5465acf94294ac7a56e0d59ae3c0f95621fec9051556d`

```dockerfile
```

-	Layers:
	-	`sha256:bdf3b1813e429922f457251186060507a71627e92c7c43e5ae20ace9e5476d29`  
		Last Modified: Thu, 02 Oct 2025 03:25:26 GMT  
		Size: 3.2 MB (3193155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59061bc355c0318db2fd331258835c0466d8ef591a62ad9e7ae72a0dc730f45e`  
		Last Modified: Thu, 02 Oct 2025 03:25:27 GMT  
		Size: 38.6 KB (38591 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.4`

```console
$ docker pull elasticsearch@sha256:5b2a4763ba7fa7a3495989733973a231e5061434d0d695373b0f702857428399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:8192b42434c6edd8180f41f20fa9b5557ff3e678e9c8ea8aa2a803e9364dfda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.8 MB (697814621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac41c93b217c7ae78d2173d9204b847409aff77ffd8c3d45e0c90e4719718227`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:07:26 GMT
ARG RELEASE
# Thu, 18 Sep 2025 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Sep 2025 08:07:26 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T22:06:03.940754111Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T22:06:03.940754111Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6f50a06c83dd14479a1d4e10d739e24a2fa9afaeb0e8a434df257198d64d3f`  
		Last Modified: Thu, 02 Oct 2025 05:05:07 GMT  
		Size: 6.9 MB (6893762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bff929743e86aff0f685608bfc0935f1bbf6a14706eef52afc2495eb903ad88`  
		Last Modified: Thu, 02 Oct 2025 05:05:07 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a816122bd76ae5ab439b0d451ebae7a9e6eb51f4452b4363cf2af4408c5fadc5`  
		Last Modified: Thu, 02 Oct 2025 06:26:31 GMT  
		Size: 660.9 MB (660903165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acbe10ec4875d9bcc10ad9cee3bb019bce2601c3b2c3de2a5e4bfa50c9e7ee2`  
		Last Modified: Thu, 02 Oct 2025 05:05:07 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7297ffd77060c10b5aac616a1805384fa4458386b3f5187787a8e206f7c2901b`  
		Last Modified: Thu, 02 Oct 2025 05:05:07 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e372943618076c3eece60a5009ba49ec4d5a8fde5db153e47826e8b57c523a14`  
		Last Modified: Thu, 02 Oct 2025 05:05:07 GMT  
		Size: 163.9 KB (163933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437b2d9c1f7d5c3d6863e61aca89cb700bd95572ddc4091363e5e72b0f24f212`  
		Last Modified: Thu, 02 Oct 2025 05:05:07 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cbc9fda1ad67bc2047df4bd1024acd378fd2c55bc7d365023fab6c6cd86073`  
		Last Modified: Thu, 02 Oct 2025 05:05:07 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:deea63485e48eb570211afb825a09b427bb0644c52be21537513c49c81c077fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289dd93c484f0878f368b72fa139f79dd8980de3fd0cdadbfd26a4fbfc1ccf51`

```dockerfile
```

-	Layers:
	-	`sha256:abc8c2c3c23b49c848455a078be1ee8793f718da8e6433c7122f28063a57b71f`  
		Last Modified: Thu, 02 Oct 2025 06:25:28 GMT  
		Size: 3.2 MB (3214203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18fa34d98154825555fa462fc53495dc65943efd1f412f20052920a5887c82ee`  
		Last Modified: Thu, 02 Oct 2025 06:25:29 GMT  
		Size: 36.9 KB (36882 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:50646f6ca8c43d73f45e8562fad05eb606892afe15b772a1f52636fcf5caf3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540020264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be590863a796e21f62aad5491b4203cdbdfe9ca259b9a71f857931b0bc9a3f78`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:07:26 GMT
ARG RELEASE
# Thu, 18 Sep 2025 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Sep 2025 08:07:26 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T22:06:03.940754111Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T22:06:03.940754111Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c7e059c03a8006e04684ad8c2fcb8ccffd28d058810e1db4816d2a15401cf`  
		Last Modified: Thu, 02 Oct 2025 01:20:07 GMT  
		Size: 6.7 MB (6712746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdf67020d4a09ee24282b8b57c750bd5f6bdc89c1bcec3ef90da26e3210cc62`  
		Last Modified: Thu, 02 Oct 2025 01:20:08 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412b58146b0e4b4de10cefebea16455bbb2dadab2f6291777ee173179bde7636`  
		Last Modified: Thu, 02 Oct 2025 03:30:15 GMT  
		Size: 504.2 MB (504155266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6fbde0711d4818559c364df35f248f648e394f8228833b3f5797848911a883`  
		Last Modified: Thu, 02 Oct 2025 01:20:08 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f652fe4c7b1d8dfbe4c137f1b0f5cf59dd95b6e1d028077438083a3b1480903d`  
		Last Modified: Thu, 02 Oct 2025 01:20:09 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b390b3f231ac16d5ba25d3e590e3199feb820db9d22d96e802a97aaf7bcef16c`  
		Last Modified: Thu, 02 Oct 2025 01:20:09 GMT  
		Size: 160.4 KB (160360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0439a4e8df708589e482701078fdaecce5ba1da07a5d2f833d50eeab7401fa04`  
		Last Modified: Thu, 02 Oct 2025 01:20:10 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b156164a2d570249fd2335babf949bec6e11f669d5de3fff6eb0a058746f58aa`  
		Last Modified: Thu, 02 Oct 2025 01:20:09 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:47146ce209f9a54b0a35a4711074b6b2f5e79f94977aabf191a4e3b8e63ca9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0969c057aa1901c71d77f0012eab44f564d606fb49967131200153db1662183f`

```dockerfile
```

-	Layers:
	-	`sha256:6690b848d3dce01904ccea8ec48fb5e8b35d74e374d1904d3ccd77df6ace4fe5`  
		Last Modified: Thu, 02 Oct 2025 03:25:32 GMT  
		Size: 3.2 MB (3214616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636212dc03ba8ac4617fb46043feb7fc9b6ea62e8593649c8566c3d5b3cdc427`  
		Last Modified: Thu, 02 Oct 2025 03:25:32 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.7`

```console
$ docker pull elasticsearch@sha256:f4867391fd4d5e2bc2ea3a9fd2ff2f5708cdc5bb77b89690fc94971bc79604e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6f19b3b1ed72178a53d58af887bbd82a273dd0923d36d4b352ec7ee134998a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700687946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44e666fb7450c1220f3e0f183a1d1df6c4b7acbc8b12592941e947a2649a1f9`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:06:39.784049935Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:06:39.784049935Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921a1386559fdc3fad77d74fb02ed2865aecf66a84924c19c3e389b64bcf0004`  
		Last Modified: Fri, 19 Sep 2025 21:18:12 GMT  
		Size: 4.3 MB (4282655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8f21a40e62169849c1353a79265ebb38aa131f0f39a036db85ff4f60730e3`  
		Last Modified: Fri, 19 Sep 2025 21:18:12 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f9d0ab21bb483ac1a1a7ea236bf5198391e3ee863f49417e0f83decddfd741`  
		Last Modified: Fri, 19 Sep 2025 21:18:14 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ac2c0ef7803bc42f70553280c374bc42163af9d822e9a36bc9b1637b03a88b`  
		Last Modified: Fri, 19 Sep 2025 21:19:16 GMT  
		Size: 656.7 MB (656666520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68d712d0902dd8181bb529ce9c6c6e99851214e3634e490f9dc40e0633e3b97`  
		Last Modified: Fri, 19 Sep 2025 21:18:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71b899601cb75af4c33ab76c01bc7bf478f78ad63fdce7aef76a7b59fa283ba`  
		Last Modified: Fri, 19 Sep 2025 21:18:14 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01928d41737432ffafdb2e3e52fbd3df19b16c1cfc483e72a5c7116d4241cf3f`  
		Last Modified: Fri, 19 Sep 2025 21:18:14 GMT  
		Size: 75.7 KB (75745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0692bc25115149e5c143120bdfda15d1b49018c01a8b2c87f6e2311bb9f5f04`  
		Last Modified: Fri, 19 Sep 2025 21:18:12 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a961174e11a976d37323665c2f769d606a57036bce8b648bc4a21ccb9e4bc077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2064511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0c0816e7a6a9c75b8ce73712ad5e150b3cb496114fe7a9aefb33e098588a55`

```dockerfile
```

-	Layers:
	-	`sha256:642e9aee8d770fd5e6b65263e50a18fe48ae33a639110bf1dd39360e7737d01c`  
		Last Modified: Fri, 19 Sep 2025 21:25:23 GMT  
		Size: 2.0 MB (2030673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d37b1f3fd940cfc3f5079e0fd9de8a6aab5d71846b6521b6bea19d893670ba`  
		Last Modified: Fri, 19 Sep 2025 21:25:24 GMT  
		Size: 33.8 KB (33838 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:6ac4fe8dacd40f955d100887e587c2cb3f1250597a256e7955f5d725c4fa98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.2 MB (539213471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379d2e7c290ccd328e9ec3708ce55544ff066bae52280b8495eaae7e28254c52`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:06:39.784049935Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:06:39.784049935Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7f33888e5b67a259be391c604710b80055e9ee4740d87827669461eff488ed`  
		Last Modified: Fri, 19 Sep 2025 20:47:19 GMT  
		Size: 4.3 MB (4290411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44665faa46e15431143ad527dee58442c70b6a199f3d70fa6cfdd19555f4c3f7`  
		Last Modified: Fri, 19 Sep 2025 20:47:19 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9026ec73c64fc604d51d7ee555e0bd42289f45e46bdb8ef3d37b0235571eac26`  
		Last Modified: Fri, 19 Sep 2025 20:47:20 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de94affd03766b67d7d33114e082b1680cf292cc3ecca83f12220d7cdd028c7a`  
		Last Modified: Fri, 19 Sep 2025 21:27:36 GMT  
		Size: 496.9 MB (496933925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e90d3c05d113e0894e5b0f8112e152b018d856bc631a149901b1e31f6ae6b62`  
		Last Modified: Fri, 19 Sep 2025 20:47:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974c4edbe8315a6a1d1811dabe0b33f9dd7dfcbdbe80c29cd628c31278ac7074`  
		Last Modified: Fri, 19 Sep 2025 20:47:20 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3150cd8d4c07e95118b02b572152e572dd3d4ec5db419f2494e15851f65d2d`  
		Last Modified: Fri, 19 Sep 2025 20:47:20 GMT  
		Size: 74.6 KB (74638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9e48bb4e2f3e8a74ec32d43666b1e3726846af93c3c6fb85c5005c22ce5a91`  
		Last Modified: Fri, 19 Sep 2025 20:47:21 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:545a8af37843a4daa1f14eddbcb39eacd7f7e471102f7c9e9a166b018e081e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b49bb00571f1214c9212acd2bd9eff7882e4e7f563b26dd6b79c2c699ab677`

```dockerfile
```

-	Layers:
	-	`sha256:e6e0fcfd5cfbf77751175d53d07847bdfbb971f305b5c01409a98a4ed77a9386`  
		Last Modified: Fri, 19 Sep 2025 21:25:28 GMT  
		Size: 2.0 MB (2031237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bdc2aef5686efe1720e69f0f8e10d201e36139c95552e9d830a2dd63dbf2090`  
		Last Modified: Fri, 19 Sep 2025 21:25:29 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.4`

```console
$ docker pull elasticsearch@sha256:0605584123a5e577e7da05215d80ed81473d3ad041abca686918c1295c90a549
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9ab0d100892dd17873a683604e4105503401a918597d098ce25d2a02930d5e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.7 MB (715689399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8a06e4e4ee7c44b27bbb4690ccf9ae84b3291458b3dac99d7631c02cb423d6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T22:05:19.073893347Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T22:05:19.073893347Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1a049251b7bfa5ec400dc3fa47c63b05267537f7f1a41c9633f5356eb803c`  
		Last Modified: Fri, 19 Sep 2025 20:47:58 GMT  
		Size: 4.3 MB (4282663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67584a0c265f1847753e5c88807f48f0190eab56669704ac0f99b3556a1d3890`  
		Last Modified: Fri, 19 Sep 2025 20:47:58 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fa5866cd62a62efe0dbe88b8a8b30ecf18da1ff6de0cf49e837ecf7a70eb7`  
		Last Modified: Fri, 19 Sep 2025 20:47:58 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dc5f5c65e20827de29bc8b5e80743030409d311d09e692ab74bae724146949`  
		Last Modified: Fri, 19 Sep 2025 21:31:05 GMT  
		Size: 671.7 MB (671667958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f4e7406b96d8da6d8e4fd21b0c5bfb156b8e8092106090054197fc462a5daa`  
		Last Modified: Fri, 19 Sep 2025 20:48:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d08a248b7e26b34a988dc91c69efe9882bc524952511f3a5cbbb5cfa17d271`  
		Last Modified: Fri, 19 Sep 2025 20:48:00 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cd5ffcea4cbc9ff463993762fee2d7da83652600f0d076b14af66e67a9a9e8`  
		Last Modified: Fri, 19 Sep 2025 20:48:01 GMT  
		Size: 75.8 KB (75750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da272f21b2bda95ec69a27a1cbc3d9f6d26599742edde2112a28b0d5d328b3c5`  
		Last Modified: Fri, 19 Sep 2025 20:48:01 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:7fd6988713d6f6159d94851faf897fd0bd5b1c29a0d85a04f76117e54bf2e920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1128f7474abd594bad5ef5e7db8f0a392f146cf2188053373483b0d29f7c`

```dockerfile
```

-	Layers:
	-	`sha256:525a02d1c3e6c21ca3801ff6bbbeb203935006bc4e69fe9c5e2385dc51dc8d41`  
		Last Modified: Fri, 19 Sep 2025 21:25:31 GMT  
		Size: 2.1 MB (2084168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2b8e9415e0703854541acd56aeee7dd8b12bc821719be14eaf1c3676888ff0`  
		Last Modified: Fri, 19 Sep 2025 21:25:32 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:64d8d37090f7f755c859c2a71b5b85dfb46523b4681d405204a57db2c14f30ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.2 MB (554221710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472111600f599a75eeab4e0b395922cae7fe8c37a476e53ff6f86e952a38c2f5`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T22:05:19.073893347Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T22:05:19.073893347Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf90545866d98bf757816c7957357bc6af3aff9b9881ed49577604b60b126a46`  
		Last Modified: Fri, 19 Sep 2025 20:46:50 GMT  
		Size: 4.3 MB (4290406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a538d136ff0dc21a69fc99fd813f309c3754d677fc597357999e96a121245e`  
		Last Modified: Fri, 19 Sep 2025 20:46:50 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8939d2f98f6f413ea8258b723655c5bd272944ea53024ebe8e33327488907`  
		Last Modified: Fri, 19 Sep 2025 20:46:50 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6b546893a06f0a4b4e925b46e9599f7206308a0c97bee33c67ba78477051e1`  
		Last Modified: Fri, 19 Sep 2025 21:18:57 GMT  
		Size: 511.9 MB (511942164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6f7a202c88ac0503f308f5804971d6889c02b804ff2a6f302276c2a8145558`  
		Last Modified: Fri, 19 Sep 2025 20:46:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da98f427c4e32c35fb03ca07d24a7dd4962af2758382759244d20f25354fbac`  
		Last Modified: Fri, 19 Sep 2025 20:46:51 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc7f1906f6fa6ffb8d7822e1b2b2e363abed7fe5cc2ae9287989c437073794e`  
		Last Modified: Fri, 19 Sep 2025 20:46:51 GMT  
		Size: 74.6 KB (74640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c1f4b224ad74619ffe45595974199eb60aeedea56fab58225613684f60315d`  
		Last Modified: Fri, 19 Sep 2025 20:46:51 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4d49e663e92803971c0724b252b778f0eb0934da67591a71898e14b852170dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ea701c1e08ce19c3d8dcd00cb0af5629fc63d5518fbe6639f2f85eaa274b66`

```dockerfile
```

-	Layers:
	-	`sha256:088f41e56cd0625302cc63303562cb5c3665f4ad3df13a699c016be0971db6fc`  
		Last Modified: Fri, 19 Sep 2025 21:25:37 GMT  
		Size: 2.1 MB (2084732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27579a45dfe6710f32edd05a496bb0b0eb181cd3eef796cd9633d38eacb35918`  
		Last Modified: Fri, 19 Sep 2025 21:25:37 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
