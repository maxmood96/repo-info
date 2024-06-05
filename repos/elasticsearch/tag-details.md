<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.21`](#elasticsearch71721)
-	[`elasticsearch:8.13.4`](#elasticsearch8134)

## `elasticsearch:7.17.21`

```console
$ docker pull elasticsearch@sha256:0e75a50aa18fa99207f1e44188b6b0f01598c8648b59572461d94efdea99ed36
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
$ docker pull elasticsearch@sha256:86010c81c9c354490cb8f371d17d084a0f8ca49a513ccb411fc2f85ec58a50ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360373456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0de4e6db2bf9606eda83e75322a0dc9561d9bbc025e94de46c9481cd55ec41e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
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
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a4e6de708014028e39a2d00fb33cee6da7a73dc8a169d0d933ea2c62eb0246`  
		Last Modified: Thu, 02 May 2024 11:28:12 GMT  
		Size: 7.3 MB (7332784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3fe6a2d06dafb21c2c940739605cd63f9a633890fa0d2dc23db4794d6d8283`  
		Last Modified: Thu, 02 May 2024 11:28:12 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929601c3ac41ed3a21d9afa569a842fc072bec2a45d7b59d8d3f639c5561fd60`  
		Last Modified: Thu, 02 May 2024 18:12:43 GMT  
		Size: 326.8 MB (326753886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e80c34bee30248d0947f60bd05d19ec9771018d21346d9184dd07778206bc4`  
		Last Modified: Thu, 02 May 2024 18:12:37 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ee74cb2deee8f76d44928a8abea8d8078ae6c62eb7af988a91a2be5f42a82`  
		Last Modified: Thu, 02 May 2024 18:12:37 GMT  
		Size: 2.0 KB (1982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf94012634477fa90b475b305513884b86100a1dd8025a2caebc5b0cf39d65`  
		Last Modified: Thu, 02 May 2024 18:12:37 GMT  
		Size: 186.2 KB (186188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8e1b2828bcbeef4ddb4506a217b17d3b4cedc21905a0edb7419b32f141057f`  
		Last Modified: Thu, 02 May 2024 18:12:38 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7bd19109256a688349a27e827b0a99d88f669466b36b50fb53fecbf7d4d548`  
		Last Modified: Thu, 02 May 2024 18:12:38 GMT  
		Size: 109.3 KB (109257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.21` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a1ddef4161c21cd9829a078fd13776a7747896abed1ba075fdf1c907ed0cf1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2350328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111fabf643a1bd41cebb0c31680591668c6f2e2111a9f95db3ddc85a91024faa`

```dockerfile
```

-	Layers:
	-	`sha256:d0b55c0bd9dedd18e0c76d412c280a24d1be95915e15c94f400010844ae1736c`  
		Last Modified: Thu, 02 May 2024 18:12:37 GMT  
		Size: 2.3 MB (2312739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3629670ffebb97734294b4086a19de63769206db2af8cc39def2900b73c4450`  
		Last Modified: Thu, 02 May 2024 18:12:37 GMT  
		Size: 37.6 KB (37589 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.13.4`

```console
$ docker pull elasticsearch@sha256:80f417b2b368f6cb6f89ee80656eb1c40adfff1c962c5155bca4f938cb2425c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.13.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f83ab3f949e2089877fef62f6a1fd6a796d4ec29e218898eeab262d8017b08b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616908316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a981d1bf256a0367a18292f03bfcd98e517a5dd346c70b9179a4df1f80f7a0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 09 May 2024 12:07:29 GMT
ARG RELEASE
# Thu, 09 May 2024 12:07:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 09 May 2024 12:07:29 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 09 May 2024 12:07:29 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 12:07:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 09 May 2024 12:07:29 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 May 2024 12:07:29 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 09 May 2024 12:07:29 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 09 May 2024 12:07:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 12:07:29 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 09 May 2024 12:07:29 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.label-schema.build-date=2024-05-06T22:04:45.107454559Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=da95df118650b55a500dcc181889ac35c6d8da7c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.13.4 org.opencontainers.image.created=2024-05-06T22:04:45.107454559Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=da95df118650b55a500dcc181889ac35c6d8da7c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.4
# Thu, 09 May 2024 12:07:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 09 May 2024 12:07:29 GMT
CMD ["eswrapper"]
# Thu, 09 May 2024 12:07:29 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6f4f283cda290401e2f27b06e079c2f04f0a384650d5bbe17073c5707c0b90`  
		Last Modified: Wed, 05 Jun 2024 02:21:35 GMT  
		Size: 7.5 MB (7512978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d81a403f9faad52695304290bba14f5bfd0b8e146a5188e6a2746def3acd2`  
		Last Modified: Wed, 05 Jun 2024 02:21:35 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19b2e6591a46b270e9681c2ba28dfc5bc35c0ea825d27f819bd089569eae241`  
		Last Modified: Wed, 05 Jun 2024 02:21:44 GMT  
		Size: 581.6 MB (581566413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b675dfbabbe2a5ecbb4e5e013ede075ec4c564c4463943eff04cd2ab7aa456`  
		Last Modified: Wed, 05 Jun 2024 02:21:35 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433074ee92b37d13088563df740e7c5d9e83481c70953d7a6bcadce552604151`  
		Last Modified: Wed, 05 Jun 2024 02:21:36 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c051b58b47a4b723cea415e0a2c11d107bce43a1adef9e9e173537fc35c5fa1c`  
		Last Modified: Wed, 05 Jun 2024 02:21:36 GMT  
		Size: 191.9 KB (191903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd51018461ead4d7d2eb327096d27ee84dc92b45eecddb9a9be65286cb2595e9`  
		Last Modified: Wed, 05 Jun 2024 02:21:36 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d3a991fadf2e8d43eeb2b916ceba37a173e6b68fa987ad9fa46bbe1bbabced`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 109.2 KB (109250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:82aadcb2f189eb85b42876ea4d6c5b89d63f923be748a2ba5e40716306755de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b56dadecf54c84f300e80c95ff1261c30190153f3697a7d3059b1d711c549ee`

```dockerfile
```

-	Layers:
	-	`sha256:3dfa0f306ae654428b74d3dd4149b907850e97e837d666f79ef88c9adf741dbd`  
		Last Modified: Wed, 05 Jun 2024 02:21:35 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ee1d35d0284d7214641efe74905f95a4a1e8443d8c6b17dbc6c30b5ba3f746`  
		Last Modified: Wed, 05 Jun 2024 02:21:35 GMT  
		Size: 37.6 KB (37601 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.13.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:241ed4d9eedd427471f8e0dd3bd8694dee830b8feac390dd9036095f98a1ab69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.2 MB (461234440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4783a81daa8d19154b224cc4533be9858e74a4d0792783c92210bd819c69462`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 12:07:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 09 May 2024 12:07:29 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 May 2024 12:07:29 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 09 May 2024 12:07:29 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 09 May 2024 12:07:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 12:07:29 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 09 May 2024 12:07:29 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.label-schema.build-date=2024-05-06T22:04:45.107454559Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=da95df118650b55a500dcc181889ac35c6d8da7c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.13.4 org.opencontainers.image.created=2024-05-06T22:04:45.107454559Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=da95df118650b55a500dcc181889ac35c6d8da7c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.4
# Thu, 09 May 2024 12:07:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 09 May 2024 12:07:29 GMT
CMD ["eswrapper"]
# Thu, 09 May 2024 12:07:29 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d4d91fa2417e3167384fb4fae4d9eec0a8592c69ceaa015a2ff0e163a947e9`  
		Last Modified: Tue, 07 May 2024 23:04:25 GMT  
		Size: 7.3 MB (7332755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab22f96f93bcde90ca98ea85963134c247652a358b4335008cf44b97c80128c4`  
		Last Modified: Tue, 07 May 2024 23:04:25 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb857268b821048083e1947d016ddafab2d433d0f1b1697182131e4b66bc0b9`  
		Last Modified: Thu, 09 May 2024 17:15:52 GMT  
		Size: 427.6 MB (427615412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c8ee5e01cb9b95dae9821d4ddc807399b81ede039e71c058c60c630760f285`  
		Last Modified: Thu, 09 May 2024 17:15:43 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bd45399b7d22f4764f9e523c49d9925d845d9a5d89e833b9be10045e5968c3`  
		Last Modified: Thu, 09 May 2024 17:15:43 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a306294629ed99490b6764192d15f7418b9a56ff1ce2390699558239a38c1273`  
		Last Modified: Thu, 09 May 2024 17:15:43 GMT  
		Size: 185.9 KB (185926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911c3136651ea5efd0d29ecb25061f95a7a2cdaaa2a99823b78cd73fb31a3c9b`  
		Last Modified: Thu, 09 May 2024 17:15:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47143f0a5b2884052be81b50285a207cc65c81ae9047ff132e9521fcf2868e67`  
		Last Modified: Thu, 09 May 2024 17:15:44 GMT  
		Size: 109.3 KB (109258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.13.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:75e5014eedc623483cc15068cea453dbbeea07ab689ed714fcf66546063a02cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1580882c342eb04a834b36f4e1b239c0931532c8281e9705f6952d9a9f34dbcd`

```dockerfile
```

-	Layers:
	-	`sha256:65103e74931c6ab620958f305ce9374461f3f0dac4bc815e2d72b143866dc9da`  
		Last Modified: Thu, 09 May 2024 17:15:43 GMT  
		Size: 2.6 MB (2591352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5702906e5fe9e6bb18e3a057cf7e9ea4cc57bcfafece73f2ef517f714f9b22cc`  
		Last Modified: Thu, 09 May 2024 17:15:43 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json
