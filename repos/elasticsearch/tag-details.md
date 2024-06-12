<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.21`](#elasticsearch71721)
-	[`elasticsearch:8.14.1`](#elasticsearch8141)

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

## `elasticsearch:8.14.1`

```console
$ docker pull elasticsearch@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
