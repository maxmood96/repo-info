<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.8`](#elasticsearch8188)
-	[`elasticsearch:8.19.5`](#elasticsearch8195)
-	[`elasticsearch:9.0.8`](#elasticsearch908)
-	[`elasticsearch:9.1.5`](#elasticsearch915)

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

## `elasticsearch:8.18.8`

```console
$ docker pull elasticsearch@sha256:c811f8cd1cc7227427f194bbe5adb0484320467a9b6da98fb1f4c7d762731d1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:018ad99c1fbd12ef3823b33e0f69df9751d9a57cfa1e085c26a4ffe02cafb0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.8 MB (701820247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32f25f440c620d60830eaaf8caeef9359865e8f1dc09ff9308b1bb73094100a`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ce27949be5aa3487f0dd75b0bfa1221335059400745b32e9a3cc5943ae7459`  
		Last Modified: Mon, 06 Oct 2025 21:00:11 GMT  
		Size: 6.9 MB (6893790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412008eab324f139f667b318f8ca94bcfc4f262bff7cd9e20dface0a052a8387`  
		Last Modified: Mon, 06 Oct 2025 20:47:16 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d1bea405125413cfc5423123c50a126b10a22785c69ac07b1f618630e8a399`  
		Last Modified: Mon, 06 Oct 2025 21:00:41 GMT  
		Size: 664.9 MB (664908770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6750d4fc7057ae1e3ae6ae8d7ffe72867623d3fafc51caecdad3c45ea964421`  
		Last Modified: Mon, 06 Oct 2025 20:47:21 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d0bba16a0ff4e3dc23da958e5b522e7fb1223587af4272c2b1b9eaba725593`  
		Last Modified: Mon, 06 Oct 2025 20:47:24 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b247b051063db9c134fd99e554a1e13ad4febd70a5d0266eba6dc748e146a262`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 163.9 KB (163934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92cf6f63d9d4d236b4ef3d36c3b55e64a64893b6c1ce38f0fcd606670c3bf08`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a7f7e05334e3e8b8db1c8adafe176954e59f93a98054ca9c567cfaf49bdde9`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:23aaf4ea536c5e1e09557e9c80df783223c9a1bba7e27afa3481a0f2818f12fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61244150d7ade43a63783af3bcd8330f45d17a44ffe16b130123fda124fe4a08`

```dockerfile
```

-	Layers:
	-	`sha256:1ccc182d3e8a506bb3cc18304d1efc46bd60de87e6b5621273e763316fb3e531`  
		Last Modified: Mon, 06 Oct 2025 21:01:12 GMT  
		Size: 3.2 MB (3192944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48fa735aea63b52ff1dec33529be72f93195e38288df66136838c1d963b10974`  
		Last Modified: Mon, 06 Oct 2025 21:01:14 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:01f646c7a5ebbaca775650131502181a9ffc07554f0056882fc61873235df402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.9 MB (543868308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8487a2e99c5b3cb9a36b41c0dc54d63f3dd0c40d1a4416c03e554abe0bab1c30`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b0986566ec7b91d9eccc4e1c8f1fed0f0daf2cdef42f42ce4eb3266b0b5cf7`  
		Last Modified: Mon, 06 Oct 2025 20:36:12 GMT  
		Size: 6.7 MB (6712815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8fcdcc367f87f35257bbe964488aaf762a77c551af76b82efc787862c78c6e`  
		Last Modified: Mon, 06 Oct 2025 21:13:50 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4a30b9e539c2fb030799ce2e9c61083381eeece4f813791055ffd3f5b822c5`  
		Last Modified: Mon, 06 Oct 2025 20:36:21 GMT  
		Size: 508.0 MB (508003223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb6e1560025749f99ba54aea20e7da2c5d86fc53b2d4e4c0f4f1b751353753e`  
		Last Modified: Mon, 06 Oct 2025 21:13:54 GMT  
		Size: 9.1 KB (9107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6fb70a37403c72df00e133472ef0422852bc885a67b8c3f09e12e9235a9782`  
		Last Modified: Mon, 06 Oct 2025 21:13:58 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adea0defbe5a9ec4fdbcf3e1a4e31e22f02b24faa58487c8b56610cb33101ad3`  
		Last Modified: Mon, 06 Oct 2025 21:14:02 GMT  
		Size: 160.4 KB (160372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5f0306c320658e97f27cc80411bb30f20d4c225de34b624e42135e3e35a297`  
		Last Modified: Mon, 06 Oct 2025 21:14:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1be7e3459979fd87fe911eb6b907db1456a8e078c1c81bbff171bc59529400b`  
		Last Modified: Mon, 06 Oct 2025 21:14:07 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:75fddd680d512de2e874b4a8fd0355f5d825a83120c8420997a40a8ac9d3ef62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ea3b4135d57d5095a1f947581cbfa6df79a85b8528e666c556bf24ff77cf39`

```dockerfile
```

-	Layers:
	-	`sha256:61ab0e2036b722dfee73acd1de56b74dcb222ad171717db9418c865eb1c0998e`  
		Last Modified: Mon, 06 Oct 2025 21:25:27 GMT  
		Size: 3.2 MB (3193357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a1f43c19955ccb5b543e99ea96796384bc6de40dae6fcc362681a6985689c7`  
		Last Modified: Mon, 06 Oct 2025 21:25:28 GMT  
		Size: 38.6 KB (38590 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.5`

```console
$ docker pull elasticsearch@sha256:a6246cb990f1ae0a17bcd3088336deec1f3f40e52dccb9abc8a3d0492649725e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9d4a35587739c534a444524f916ca0cde0d73e951284a633b828cb7bfe573980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.7 MB (708747818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f97a887fae64f31d3dc8179fe1b791155217c1478fcb82ff4c4342ca21a4bf`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.build-date=2025-10-03T16:35:50.165700789Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d6dd0417f05cd69706f4f103c69bbb8b7688db9c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.5 org.opencontainers.image.created=2025-10-03T16:35:50.165700789Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d6dd0417f05cd69706f4f103c69bbb8b7688db9c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.5
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:09 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ff68572a641b4ccdc527f59ba8888d1854ba7d38f8c8ff8e06ee3e1ed443cb`  
		Last Modified: Mon, 06 Oct 2025 20:38:05 GMT  
		Size: 6.9 MB (6893731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea03ce29c0b315a102119efeb674341a6ad91f7a253255480c8d955ad7b4d9f2`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0d83dfa089f4dc89c3af2353ad5e05c21b552c80440feac81c6df2a9d32024`  
		Last Modified: Mon, 06 Oct 2025 21:02:16 GMT  
		Size: 671.8 MB (671836406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb82fa2a1091a1e761e254b2aaa6ce873166376cc2380057d016322d396df91`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faae685f1ebe7812df521bd56817cbd27e6d89c67086615d09dab983a100912`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddec3d123c9e72f6d779e4fddb3b3f94d57c72050399c60920c52924103a7aa`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 163.9 KB (163929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbccca08f630aba54117321a074f37fefd440aafc49c969b5fbb87ed365b682d`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5aa444804d4506c40ea6f48490c51cc6f54b86fe603bdd132e4ce1a795dc0b`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ca7d483a0fdfca37f0299e89e80beadc69ce5673ae6558d8da27b2a80819c6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845d6be0282ffee3d3aef2c5284883c5186829e03cd64a4a2d7536abeaf45bcb`

```dockerfile
```

-	Layers:
	-	`sha256:dc67cbdb6924436412d6bf08b6d57b87ce7b48f60cf6122398c531a5c8918873`  
		Last Modified: Mon, 06 Oct 2025 21:02:42 GMT  
		Size: 3.2 MB (3215149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050efb114e02a02fa7c7fb8b65df760cb98846ad9bc15a721ede2d9d50a1ba40`  
		Last Modified: Mon, 06 Oct 2025 21:02:44 GMT  
		Size: 36.9 KB (36883 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:5577b324092b4b51152bdf0b42fe0deeefb8eba5f218b0e5e5bb20783cbf513d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.8 MB (550764781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bc1b6e29e75e40949decf283110538113951ea147624fdea3e8f9548006e9f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.build-date=2025-10-03T16:35:50.165700789Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d6dd0417f05cd69706f4f103c69bbb8b7688db9c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.5 org.opencontainers.image.created=2025-10-03T16:35:50.165700789Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d6dd0417f05cd69706f4f103c69bbb8b7688db9c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.5
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:09 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1390c7c0038dc343eb088de985af51039820218b0e72076bbce0ec1ec6076b32`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 6.7 MB (6712860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186829b5fa1060dd3c4a550ccab15d0b4a068c4e6a8601db7c5459e471ca022`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 3.5 KB (3524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbb399381a45877db6347bbdbc648c0fb0851c9d49b205a6eb64e127d061d9f`  
		Last Modified: Mon, 06 Oct 2025 21:26:37 GMT  
		Size: 514.9 MB (514899668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3431b3ed3c7fb20806285c093af9b6ae5eb5cbd0d46d852570209913982f1570`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39adc4e20daac0a019bcd7e76c390aad5445769aea7c9ff68eef7cdf0b82c09b`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813119ee0e9ec48a14a334638e9b047711602d6ce978c18daf9ced1a16e3c61f`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 160.4 KB (160363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9bbe27ed8b97be70176ec5b07e37827bebc7b4a650ae3b40dbb05714605292`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05512691d8ba674fd68dd959f66473cd39f787caf0ac9ba3c490811bea7213e7`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0aa0ed0fc595c5c4a7a00d2528adb2e92e0d720afdc513bd78f25f41f8c5248a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca1f636d72a2926b8767e2af407e49f71334d9590aedc25867f2de4e9aad9dc`

```dockerfile
```

-	Layers:
	-	`sha256:9fbfe61563db8e30661a0c349150a1bfd05416dc183210ac7b9b30fadab76b64`  
		Last Modified: Mon, 06 Oct 2025 21:25:36 GMT  
		Size: 3.2 MB (3215562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:802919f7a8fadecaf56632c3cc74cf38301f17ce558045d34b8e3ef953a1cb57`  
		Last Modified: Mon, 06 Oct 2025 21:25:36 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.8`

```console
$ docker pull elasticsearch@sha256:10c1b6e8c7f1d67fd3f59ff58974d7f51a4e2ad5cbf5b6331944af1d84cb505e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e84f011a779b43eba0673bbdbb04142b74f1b52c95c9806ce7f977c3e876b129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **711.5 MB (711487330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1629a74612aa2d8013691f36f2aff7b7abc5de5cc764ef989abbb1e56db0a4f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-10-02T22:06:15.098088583Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=936f7cf370e0d7952bb71a98629284c3c0e0d00e org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-10-02T22:06:15.098088583Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=936f7cf370e0d7952bb71a98629284c3c0e0d00e org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.8 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 06 Oct 2025 11:09:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fc658d731fd5ecfa349d08a752957d755e5371316fc45fce407060e7fa304b`  
		Last Modified: Mon, 06 Oct 2025 20:38:08 GMT  
		Size: 4.3 MB (4282682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e98ba0d90869fd987fc1bd20dbba39bd537fa44b692521bf6e0e038bd9d775`  
		Last Modified: Mon, 06 Oct 2025 20:38:04 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdf885783cb360426460961f2b03c146d6408170cf1ad26cbcb0686806a111f`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ae56d1185f48fdd817d7abf6ccd77a0f8209e95ff72d16a42d0c33b0c3176e`  
		Last Modified: Mon, 06 Oct 2025 20:39:25 GMT  
		Size: 667.5 MB (667465874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfdd52c490d1dbbf9206e55f3881b60eca71d1ff1142eb7f0392cc35673ad4`  
		Last Modified: Mon, 06 Oct 2025 20:38:04 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb5e8750d84389739533b1f68430b6cb120ed33471689c4095a1622e945f705`  
		Last Modified: Mon, 06 Oct 2025 20:38:04 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77918d87f5e152d8ee7f0b7f88f6052824fd1efb4edcc832caed9f5295bec869`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 75.7 KB (75747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77da23aa1bc99b0f1c9c47a9a0e7ec7d7fe69f438937b2a922af43cad395edd1`  
		Last Modified: Mon, 06 Oct 2025 20:38:04 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:295b81d57aebf0cfc8533f4097d52caf27cdd8c610aa243ae370947d6492f6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2064714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bfcd792f045a35bc2ddea20c57a4f89127d565eef641b07444510c27dba7b6`

```dockerfile
```

-	Layers:
	-	`sha256:70e50279ac8388599645acaa4ea0095c7d12f736a45458ce02f7f118c4e12171`  
		Last Modified: Mon, 06 Oct 2025 21:25:43 GMT  
		Size: 2.0 MB (2030875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fcc6bafd5ad96fa13000504697dcb735a26e89cee9dc8e05ffb1ef2d166cccb`  
		Last Modified: Mon, 06 Oct 2025 21:25:44 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:a97ebcf6c52a4de8ee9d7665a08f3e9de18ce00169b4a601f78b5e63de61ba24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.8 MB (549844238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2046b0f6e0bc2127f3bbcb37afda917898b314b78efd754eaee4b2470a955ceb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:39:52 GMT
ENV container oci
# Thu, 18 Sep 2025 08:39:53 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:39:53 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:39:53 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:39:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-10-02T22:06:15.098088583Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=936f7cf370e0d7952bb71a98629284c3c0e0d00e org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-10-02T22:06:15.098088583Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=936f7cf370e0d7952bb71a98629284c3c0e0d00e org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.8 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 06 Oct 2025 11:09:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e26d1d6c963b9bd5f5ec7369e0de0caf7b29cd13272492992164f34361fdc79`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 4.3 MB (4290426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb7ab32f844c3493d8595fa519d27e2759905c753c43d625f7dbc2b5e01dad`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1670271ac78b9194c208b0680b732b7cf4400d701f279fd29a48f734db91112c`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31086c4e2e931ebd53aaec71d78aeec858fd600b710563e5a248b3dc9864be1f`  
		Last Modified: Mon, 06 Oct 2025 20:38:09 GMT  
		Size: 507.6 MB (507564674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b6bb0c931e9a06d18b3faa24b10a463bcfa4a1d2d147f7996c6eca05bac48`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0380e8037b6ee5492ab7984b984d7176c5d310a0c5f5d86e44eefc5096b758ad`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b119279a9fbc40cd7f8ccce757892646c0b46d9e9474596e22013b43a173be3a`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 74.6 KB (74640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000f69b721f915859e9127dd51e85d49bb983c13947c78996f6a30f6b4154c19`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3e4d8ebfe7b26ad0dd79a855e46be6438a5fffb1bd4984d0aeb04529f25d9854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e34c55420388ac81d10bd0d093a0cdb3d586734867a8f464ce0ae2635dea01`

```dockerfile
```

-	Layers:
	-	`sha256:fd3586109919c368f6d4ae5b372f3679d16c5ac2316553d791a4b1d28b7d7c51`  
		Last Modified: Mon, 06 Oct 2025 21:25:48 GMT  
		Size: 2.0 MB (2031439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b557b1e6b2451fca6bef04836b29e49f4ea35da0cacf11865df1e3a4e23ffa6`  
		Last Modified: Mon, 06 Oct 2025 21:25:49 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.5`

```console
$ docker pull elasticsearch@sha256:9dac882b67afe5161f8988a7ede0e9890145182af83e4e1d4d10631c2f66656f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:48a0f013e919d797200acd3c5d7facb3d489c4614c2ab9d456f989cef76d2a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.5 MB (726504246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5900781248258881a2094b9c28c8b0606ebbcdb359f180210ca7ddf3a8e2205`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-10-02T22:07:12.966975992Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=90ee222e7e0136dd8ddbb34015538f3a00c129b7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-10-02T22:07:12.966975992Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=90ee222e7e0136dd8ddbb34015538f3a00c129b7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.5 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 06 Oct 2025 11:10:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdea4eec579b41823ef978d3f5da47e9dae60b707384126cc1128dbd9764712`  
		Last Modified: Mon, 06 Oct 2025 20:38:12 GMT  
		Size: 4.3 MB (4282696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339edb92a604f6908fb6322b31e498f6172b261a97c08b1441730410462e247`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d620359daf50e58cadd9cbd15f270ce60fb8a2381bb39f462e4c842ce39883d2`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ef9c90b6ad55b4b23a821436c7ba00f039e7ef485f07a606069e04cf0d848d`  
		Last Modified: Mon, 06 Oct 2025 21:01:48 GMT  
		Size: 682.5 MB (682482776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dc577f8ffce967e49c5b8119a0478b43b8522a46bc1bf5c3a044beca253f29`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7778cc196d0768fadd4c1df8f6a18a89e4dbc10b08c4639d4538bdbff736621`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595f1c606af50b141c38bbed779a6a4b07dbb5d381f8dc3a998a73d1a2bb8879`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 75.7 KB (75748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a6236f9f211860c4211fcdf347b1bf19b59f3ac63caf094d85a52e98e0e733`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f2ddf67caf83745ac45816f17ef32ed403c9f111a27a350fbbafde2f7dcd0215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980bb0289041640ddea3671e04049e3d11dc2679ee45b90bafc998663bb34806`

```dockerfile
```

-	Layers:
	-	`sha256:bbfe038b5ba7f3f48dc79f1a8855f2d4b9e5d9a1cd68fd62e02c94613a1603bc`  
		Last Modified: Mon, 06 Oct 2025 21:25:49 GMT  
		Size: 2.1 MB (2084370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7ed610b47be9e80dee8a67fc83588f1d459ef89e13c372e1089d2f0b57b307e`  
		Last Modified: Mon, 06 Oct 2025 21:25:50 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:994b0df97532976bcb792ab9471c0971bb7ee3f8e84cb9e203820c4f5b0cead8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.9 MB (564853172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9f1d7872553d47050dece25ccb6675a48aff433e33a2744f376cee65f4fea`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:39:52 GMT
ENV container oci
# Thu, 18 Sep 2025 08:39:53 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:39:53 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:39:53 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:39:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-10-02T22:07:12.966975992Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=90ee222e7e0136dd8ddbb34015538f3a00c129b7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-10-02T22:07:12.966975992Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=90ee222e7e0136dd8ddbb34015538f3a00c129b7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.5 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 06 Oct 2025 11:10:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19c1fd3d9b1295fdd3aa416ab6b1007024fdbdab2f681d7b4682d83b24c785a`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 4.3 MB (4290407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c50c99bb08a6f967e286e846adeea0081cf55f0bfa88953f59b002e55c37590`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365b2bbeca84ead5e03dabfd8f2c8464e6e45be63e0a5bf4e6efa95bf522d209`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9f340da037d629ace04734836c7b76ff8ad738c547811b30de9b07b04f7a8`  
		Last Modified: Mon, 06 Oct 2025 20:36:53 GMT  
		Size: 522.6 MB (522573629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965b34874474d405cb5d3be5d25c79ddd72395f9dec06562301ea799e70834b`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a0fc2739dd1190aa3d7762ca2f1b71b02da7bb0e44883cb9ba435b500e2122`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1481df50a8806d47a5eddfba00fe03fa6efee6dc4c9666d7bc47fec4d6d068a7`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 74.6 KB (74636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8f591acc134f6c243ba9ba1a440602530eedde77dcf6e2bdba81be90da17a`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:aef7ecd2705179a2a4d29f5bad9a0c0694b15f60444ca77d9c43905f944bad76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f0c43928aa3389c8de1389ba87a9d5b723c58b7866880324473adc4b62c917`

```dockerfile
```

-	Layers:
	-	`sha256:a257381b5fa69b96cc2ed3045c04c72fceb065a01158367fc324fd3d7ef2586d`  
		Last Modified: Mon, 06 Oct 2025 21:25:59 GMT  
		Size: 2.1 MB (2084934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6c16a55591ae4b5099a665c159a4a05f100f28dbbffc8d628144543209ea0a`  
		Last Modified: Mon, 06 Oct 2025 21:26:00 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
