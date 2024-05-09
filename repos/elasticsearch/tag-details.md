<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.21`](#elasticsearch71721)
-	[`elasticsearch:8.13.4`](#elasticsearch8134)

## `elasticsearch:7.17.21`

```console
$ docker pull elasticsearch@sha256:689a8cc0c63295ad473fb6996c9d69cbdfc80298a5733c652c9f306388cbb78a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.21` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e5fb2883974403a49da87510384aa1ec0ba7c8eb48a6d0eda2920e8b48730531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364190795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22df66ffc7b6fe7de921641cc898ba9c657f113f430ed87cff92b1f8d664c5ec`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
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
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04870ae7d3138f7beb67084575de14a003ec4220a978399013482abc1fe5d7a`  
		Last Modified: Thu, 02 May 2024 17:53:30 GMT  
		Size: 7.5 MB (7513033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67dd2074e3bd52c8ec222bd6e254a63a7d0bf83bdd55474b051d421a3bcf26`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f43265d8bcf50ddee2a730860b14611ae24c05109e0dc9b676516cd1fc5e03c`  
		Last Modified: Thu, 02 May 2024 17:53:37 GMT  
		Size: 328.8 MB (328848437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdab0e617547cd012e92e63bfa6b78ab830abb75f86e240f6c58ee0ccf851071`  
		Last Modified: Thu, 02 May 2024 17:53:30 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542ff7db21909ac94ad4b47f18ca44457157b3daf3bc811aab52478b4711a1d3`  
		Last Modified: Thu, 02 May 2024 17:53:31 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5625417cab395cd0c2c31f67c6504b696207c292bca94023deb24524c4026024`  
		Last Modified: Thu, 02 May 2024 17:53:31 GMT  
		Size: 192.2 KB (192164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3807de2d63c833a56493d95cdcbeb6a904b43595e61e5edfcaed6550d1eaeed6`  
		Last Modified: Thu, 02 May 2024 17:53:31 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a25932a856d9ca4f770426c3d478113d7f91d71782d21b6e87a081b2ed4a13`  
		Last Modified: Thu, 02 May 2024 17:53:33 GMT  
		Size: 109.2 KB (109249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.21` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:729435778e8d73d2a06004afa78159bf3063345146ce222c3d45144eb62d84ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2350268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96526dfe6ad0a5cda7064888a8556004311a24d0e14e652dab4948c7e160b88`

```dockerfile
```

-	Layers:
	-	`sha256:480b2bddc004ee9edcd4298c17d785d3c6a99423bca7c7459e45376a91171976`  
		Last Modified: Thu, 02 May 2024 17:53:30 GMT  
		Size: 2.3 MB (2312522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9fb5ec66889064fc51e7b419d9557344ea0694fe2c8347545ab7af0d3cb4b7d`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 37.7 KB (37746 bytes)  
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

**does not exist** (yet?)
