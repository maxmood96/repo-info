<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.21`](#elasticsearch71721)
-	[`elasticsearch:8.14.0`](#elasticsearch8140)

## `elasticsearch:7.17.21`

```console
$ docker pull elasticsearch@sha256:57365c7934a18d54176886829e6619dfb7d9a87be7bffb542ae97b4c127d09fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.21` - linux; amd64

```console
$ docker pull elasticsearch@sha256:ea13bd417c3a6238f92e3c31cf2095de749e3379c0fecc6adc800a01ea904cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364191193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cec81adb5065f04be1bcc9d5508fbe2d1800ddc3289e634f67654de5f8da104`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 02 May 2024 09:08:49 GMT
ARG RELEASE
# Thu, 02 May 2024 09:08:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 May 2024 09:08:49 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 May 2024 09:08:49 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 02 May 2024 09:08:49 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 02 May 2024 09:08:49 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 02 May 2024 09:08:49 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.build-date=2024-04-26T04:36:26.745220156Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d38e4b028f4a9784bb74de339ac1b877e2dbea6f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.21 org.opencontainers.image.created=2024-04-26T04:36:26.745220156Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d38e4b028f4a9784bb74de339ac1b877e2dbea6f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.21
# Thu, 02 May 2024 09:08:49 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 02 May 2024 09:08:49 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32a029835fb81d9c6c74103e294e5888d082b0d295ea3f0169773fa727c493a`  
		Last Modified: Wed, 05 Jun 2024 02:21:23 GMT  
		Size: 7.5 MB (7513038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5c1a78bf8450694e592a5c3819e4c3be500991a92b117134d9943d548f5861`  
		Last Modified: Wed, 05 Jun 2024 02:21:23 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988e39b822856e856942cfd5f7fa9b6caa55d5714dbbe2180c93ca460071f4ed`  
		Last Modified: Wed, 05 Jun 2024 02:21:28 GMT  
		Size: 328.8 MB (328848702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56df7a513d806bbd21f6be11224cefedddfa3e64b4ebe560c47e15877da564b`  
		Last Modified: Wed, 05 Jun 2024 02:21:23 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f2b9393eac9009f194bc2bcb4b2f31d8cb6d6fe24d5cb94d71604539a90578`  
		Last Modified: Wed, 05 Jun 2024 02:21:24 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526f908f3466dbec0eeed516811a443a65aec4b85b8e5e5e78ebc24787b129f4`  
		Last Modified: Wed, 05 Jun 2024 02:21:24 GMT  
		Size: 192.2 KB (192168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867e5327f4a4da0353a4f01ba651e5339639f24321a890014bc71ffff147c0d4`  
		Last Modified: Wed, 05 Jun 2024 02:21:24 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf1e26c4d4cb11d63e6986c053cac0657606d7c6ed76c8efb08cac3591ef7c6`  
		Last Modified: Wed, 05 Jun 2024 02:21:24 GMT  
		Size: 109.2 KB (109248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.21` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a03ad2fc39d343c00ec2598473ed2bc22030bfe05acc69cd1d252a09fdc88c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2350106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd2d6ade4e5ecac3c5c6f8b3dcbcba7a0ba743c2f36e815f8e91f27d05eb678`

```dockerfile
```

-	Layers:
	-	`sha256:7edf483e119c5a4bd99c4d154169a79408a3ce3a6281a9d560eab41b7dc3bcff`  
		Last Modified: Wed, 05 Jun 2024 02:21:23 GMT  
		Size: 2.3 MB (2312521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20cdd43a76de59decbb9ab64da4b6d90351f197753f2d696b83c4937bdc70f33`  
		Last Modified: Wed, 05 Jun 2024 02:21:23 GMT  
		Size: 37.6 KB (37585 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.21` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d471faff6d2edc36703646ba88c8bcc2a32f6e01a1bb683db1adf9b63cdcdf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360371515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c86489da2ccd7fb2fd52634f39df4f91393e648148e9b23559b46998e3ff484`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 02 May 2024 09:08:49 GMT
ARG RELEASE
# Thu, 02 May 2024 09:08:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 May 2024 09:08:49 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 May 2024 09:08:49 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 02 May 2024 09:08:49 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 02 May 2024 09:08:49 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 02 May 2024 09:08:49 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.build-date=2024-04-26T04:36:26.745220156Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d38e4b028f4a9784bb74de339ac1b877e2dbea6f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.21 org.opencontainers.image.created=2024-04-26T04:36:26.745220156Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d38e4b028f4a9784bb74de339ac1b877e2dbea6f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.21
# Thu, 02 May 2024 09:08:49 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 02 May 2024 09:08:49 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b1fd8f908356040db6d18b5ecfcbcc3827b850649a748aaf4572907ae307aa`  
		Last Modified: Wed, 05 Jun 2024 14:31:52 GMT  
		Size: 7.3 MB (7332205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4867208bc43d949659aef9fec85dbfcce32ab469974fe29a4262b930a7e82e65`  
		Last Modified: Wed, 05 Jun 2024 14:31:51 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87bbb9c38b1948782392b1043d708f5db8b891ec5682228c9523e7a672814d`  
		Last Modified: Wed, 05 Jun 2024 14:31:59 GMT  
		Size: 326.8 MB (326753818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154d4972bca8016e8446f1eee9aec05da93cc846699f54161c210f1976e05750`  
		Last Modified: Wed, 05 Jun 2024 14:31:52 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31e5f9e89cc444b2dbb390f202d28d0ddb2d38db4b88c1b23c7b5e7cb9ebcdd`  
		Last Modified: Wed, 05 Jun 2024 14:31:53 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546e8c8ec25d6b5a1586ee7da27a2faa8f6f18465c879963f0298adc34c0d543`  
		Last Modified: Wed, 05 Jun 2024 14:31:53 GMT  
		Size: 186.2 KB (186184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dfc78ce4bf4a30e56c78a6f1a651b210b60f8f5ec2e3655289990d32cc4933`  
		Last Modified: Wed, 05 Jun 2024 14:31:53 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab5aa7c3f88063458d8eb2d3f0855e1a8d6c19bcb71700bd4401bbe05134f80`  
		Last Modified: Wed, 05 Jun 2024 14:31:54 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.21` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a2534695addae9a631d363ae8259c883d17b4a3bfe6e3aa75d1833030a9f7fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2350603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1cb06bb70016afca2c879e5ca51e65be6523ad51840e3ff4cde5049b0772b4`

```dockerfile
```

-	Layers:
	-	`sha256:efe283d2278e0c6254afc8583314ff7df5460579036305d8df7b9e9ba3642a33`  
		Last Modified: Wed, 05 Jun 2024 14:31:52 GMT  
		Size: 2.3 MB (2312753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8bfe0e8b5ff03f3ed5418cf4e1e9835481507542a362aa559cf878f17ea57a`  
		Last Modified: Wed, 05 Jun 2024 14:31:51 GMT  
		Size: 37.9 KB (37850 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.14.0`

```console
$ docker pull elasticsearch@sha256:dfd92a2938094bdd0fc4203796d7ad3426b72b19b4a29d8b26bb032510c5bed6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.14.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:59dc31be98d446d8f97e4eb9aca610b257053b2ddac4d65d69d44458da300bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.6 MB (629641892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b37a9c2297b9fc852d491c642760abf33f98511b03afb42f6b607cd1af056c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 11:38:24 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 05 Jun 2024 11:38:24 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 05 Jun 2024 11:38:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 11:38:24 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 05 Jun 2024 11:38:24 GMT
LABEL org.label-schema.build-date=2024-06-03T10:05:49.073003402Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=8d96bbe3bf5fed931f3119733895458eab75dca9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.14.0 org.opencontainers.image.created=2024-06-03T10:05:49.073003402Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=8d96bbe3bf5fed931f3119733895458eab75dca9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.0
# Wed, 05 Jun 2024 11:38:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 11:38:24 GMT
CMD ["eswrapper"]
# Wed, 05 Jun 2024 11:38:24 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e973f09d07c77f02434f176f85ee256943aaf21887542ae33ac9f1ac72c7e07c`  
		Last Modified: Wed, 05 Jun 2024 18:57:16 GMT  
		Size: 7.5 MB (7512979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57a18efe3eccb876c2bb04816d7502ff5e59cdd0b18b0c4426ef9350e1cb8f8`  
		Last Modified: Wed, 05 Jun 2024 18:57:15 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c969eb7c4f3a5dae4fafdc21ca41eedcf4c4514bd1ae2a13706f4c3e5ea02bb2`  
		Last Modified: Wed, 05 Jun 2024 18:57:29 GMT  
		Size: 594.3 MB (594299975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d914c6582e649788da2866cb34c8b7cdfdb74d8f934c994299977ec7865935`  
		Last Modified: Wed, 05 Jun 2024 18:57:15 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da5c8ce053baf11a9d0a2bb9cb5012123998ae934fc6b49d5f3c9341cd8dfc2`  
		Last Modified: Wed, 05 Jun 2024 18:57:16 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3122e6c648de427ded5ae77696a75789d0089bd2bea9b15e6506e65deb35e8`  
		Last Modified: Wed, 05 Jun 2024 18:57:17 GMT  
		Size: 191.9 KB (191907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbadf98d55dcec493e6d2f16f860cd94ff9603499621f9c01db5e70fd621fa92`  
		Last Modified: Wed, 05 Jun 2024 18:57:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23747add1b8ab8cdf7c1a4f0c932d1b06cdb883e063a53b80c6b9a39fffc76e`  
		Last Modified: Wed, 05 Jun 2024 18:57:17 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.14.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a4ddbfb63cd52bb2f2fd8dd27371fe5bd656d62826fb242e4a84ccff49b90f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594ee2a91756cf9a46a0f649e1023c05864985c09b1c28452333099d31cc5303`

```dockerfile
```

-	Layers:
	-	`sha256:8a9bc60c19632fdce49ad7c937d80c18e8b0951297b8dc81b0ac1d68a0672137`  
		Last Modified: Wed, 05 Jun 2024 18:57:15 GMT  
		Size: 2.6 MB (2594252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d69eda4d2df9e8c60da74789e5a570fa01c51d925f8c40fbced8b6907cbf241`  
		Last Modified: Wed, 05 Jun 2024 18:57:15 GMT  
		Size: 37.6 KB (37601 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.14.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:7206552c7bea5b6e45764164a4b9e6ead92281b01533d9935b57846bf83157f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.7 MB (473742964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09d896b2d2489cff8b635e0945d1c4a9a13c7bda516d7c0e1484ed9e78f3e4e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 11:38:24 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 05 Jun 2024 11:38:24 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 05 Jun 2024 11:38:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 11:38:24 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 05 Jun 2024 11:38:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 05 Jun 2024 11:38:24 GMT
LABEL org.label-schema.build-date=2024-06-03T10:05:49.073003402Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=8d96bbe3bf5fed931f3119733895458eab75dca9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.14.0 org.opencontainers.image.created=2024-06-03T10:05:49.073003402Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=8d96bbe3bf5fed931f3119733895458eab75dca9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.0
# Wed, 05 Jun 2024 11:38:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 11:38:24 GMT
CMD ["eswrapper"]
# Wed, 05 Jun 2024 11:38:24 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcd3919ca9443ebe08b9d6b1619712e6c335e861b504fb6fa7e2c80b842a762`  
		Last Modified: Wed, 05 Jun 2024 14:30:26 GMT  
		Size: 7.3 MB (7332155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e4d6200dcda45f2e4ce2ccd29d253abc848a359ea2abb4ea2e66e2c280d39f`  
		Last Modified: Wed, 05 Jun 2024 14:30:25 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86edbb7929ba8573867a90142f10935142141c6b37f5e7276ac99ea98838f60a`  
		Last Modified: Wed, 05 Jun 2024 19:09:55 GMT  
		Size: 440.1 MB (440125822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc02a90da51427c4ea11fb8db246ea42f1ad8a2fc8a623d785fd152c7ab1056`  
		Last Modified: Wed, 05 Jun 2024 19:09:43 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a378d0a3ff5ad126ccec909aad29c255dddcea0134770bb131c72ec6e905d8a`  
		Last Modified: Wed, 05 Jun 2024 19:09:42 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba8320dd285065ab377ba6ebd286868277c4e3136c2744b7dab0d45168f36c1`  
		Last Modified: Wed, 05 Jun 2024 19:09:43 GMT  
		Size: 185.9 KB (185922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1c38945de85afe6f8e3a1c16c92190dc11c6c5eb8607571a72bc0b4503526`  
		Last Modified: Wed, 05 Jun 2024 19:09:43 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59a367be5e7287780251f6096a853164ee50578809577101be9f6e7783cc393`  
		Last Modified: Wed, 05 Jun 2024 19:09:44 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.14.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:069300de24b53f1a552974eb74cf92367b6bc6340b667223722d3355c1b43f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1211d4b43b3fe6a6167590627cc62d87e03bf5b15fb19d602ee5db5e5308862`

```dockerfile
```

-	Layers:
	-	`sha256:d7068f0639ae081381d194cf83885fbe9f7220690055664cedead5a590037903`  
		Last Modified: Wed, 05 Jun 2024 19:09:43 GMT  
		Size: 2.6 MB (2594476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7cf217280a6c2c8cd98d99a193f35ec4eeb94271c307f0b6ed792cb444e2523`  
		Last Modified: Wed, 05 Jun 2024 19:09:42 GMT  
		Size: 37.9 KB (37866 bytes)  
		MIME: application/vnd.in-toto+json
