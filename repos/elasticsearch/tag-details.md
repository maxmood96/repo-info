<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.25`](#elasticsearch71725)
-	[`elasticsearch:8.15.4`](#elasticsearch8154)
-	[`elasticsearch:8.16.1`](#elasticsearch8161)

## `elasticsearch:7.17.25`

```console
$ docker pull elasticsearch@sha256:fefc137c094d047462b4a7374cae078a280865faae35892bd44a3d1aaaafb37e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.25` - linux; amd64

```console
$ docker pull elasticsearch@sha256:119a420ed401d7126cae80985aa1e55e60fd8e8900ea144dfbbaa2017e81451e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 MB (362820029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402d32ac1e34b86c554773af4d31b0039688023946271b7d0acb45f52b23da20`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 22 Oct 2024 09:34:17 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 22 Oct 2024 09:34:17 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 22 Oct 2024 09:34:17 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Oct 2024 09:34:17 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 22 Oct 2024 09:34:17 GMT
LABEL org.label-schema.build-date=2024-10-16T22:06:36.904732810Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f9b6b57d1d0f76e2d14291c04fb50abeb642cfbf org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.25 org.opencontainers.image.created=2024-10-16T22:06:36.904732810Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f9b6b57d1d0f76e2d14291c04fb50abeb642cfbf org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.25
# Tue, 22 Oct 2024 09:34:17 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 09:34:17 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f861c07b7ad3bf20b9dea0d7eb473d14686423539d89ef7170ed97ee38ac3a7`  
		Last Modified: Tue, 22 Oct 2024 17:59:04 GMT  
		Size: 7.5 MB (7523717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bc8332bb4138bd9aaf4f7dca339e0336ca9a2b6048070b1c5ec3be3f77607a`  
		Last Modified: Tue, 22 Oct 2024 17:59:04 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dcbd05b4b47f61f399ce868687869c7cce3cfd6957c110d5c3c8ece5ae7683`  
		Last Modified: Tue, 22 Oct 2024 17:59:08 GMT  
		Size: 327.5 MB (327461305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d9c850a37143d78ee4a7403a38493738ed4b5f611c57238e6999dc48968869`  
		Last Modified: Tue, 22 Oct 2024 17:59:04 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee328141628db704c0eb8f0808569b6df52229e75179355fb8de95e8182f21e8`  
		Last Modified: Tue, 22 Oct 2024 17:59:05 GMT  
		Size: 2.0 KB (1975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7293e6052e13a27563ee6a9986513020a3fe3e2c5cef910ba294e238a1838d`  
		Last Modified: Tue, 22 Oct 2024 17:59:05 GMT  
		Size: 192.2 KB (192163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3c3a415ffd5a7ce3c243c2ab4730cad57c92cbfb3af03532a38d3df91f55bf`  
		Last Modified: Tue, 22 Oct 2024 17:59:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1b4585eb98651cb9fd978d783477bc61e29fbdad8e5471560a3bd6eb3d2a7e`  
		Last Modified: Tue, 22 Oct 2024 17:59:05 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.25` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9cf47c7c9663d329726abd40bcd2f962a9bae34b97baabcc43bec762692d3da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52d75cd0f366492bac1ce207e3e35340aa2024af89770e760259ef276b9f0bb`

```dockerfile
```

-	Layers:
	-	`sha256:4f85b622541c1c873036cdec779d881645f98a1278f5925bf5bb4f5a127e40a3`  
		Last Modified: Tue, 22 Oct 2024 17:59:04 GMT  
		Size: 2.6 MB (2554580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281ec2fe91753d74cace7857bdec63bb0baa7179389dd1d845f50f75136b2f1c`  
		Last Modified: Tue, 22 Oct 2024 17:59:04 GMT  
		Size: 37.9 KB (37887 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.25` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:cdb8040f503130b19cda007ff97c1453ff5b547c132ed23b905eba62b326d043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358758876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1e286e4ee0ffd0199da672f1a673bf38f5dfb8515817f96912d4b83f0e06c2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 22 Oct 2024 09:34:17 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 22 Oct 2024 09:34:17 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 22 Oct 2024 09:34:17 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Oct 2024 09:34:17 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 22 Oct 2024 09:34:17 GMT
LABEL org.label-schema.build-date=2024-10-16T22:06:36.904732810Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f9b6b57d1d0f76e2d14291c04fb50abeb642cfbf org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.25 org.opencontainers.image.created=2024-10-16T22:06:36.904732810Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f9b6b57d1d0f76e2d14291c04fb50abeb642cfbf org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.25
# Tue, 22 Oct 2024 09:34:17 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 09:34:17 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c218d3b24c46787c192804f137c43a06fe522c75a5bd8d582c80857c36103`  
		Last Modified: Wed, 16 Oct 2024 02:48:36 GMT  
		Size: 7.3 MB (7347306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3088df8074d66943a171b0017f5118ea1384d714af989d1812a08dc889231ad`  
		Last Modified: Wed, 16 Oct 2024 02:48:35 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa231d00900f7ff5fb258367b1b1c4d456f4a5aa30372ae349c2cf50455eed5`  
		Last Modified: Tue, 22 Oct 2024 17:59:33 GMT  
		Size: 325.1 MB (325120173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de595b58700f13651cf1d467db992cff905291d1d9985394f4ef13fec070d52b`  
		Last Modified: Tue, 22 Oct 2024 17:59:26 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a7c29a05f1f96177fb74c54497e6c2661c9888c4bb0a226e367eafd62ea5bb`  
		Last Modified: Tue, 22 Oct 2024 17:59:26 GMT  
		Size: 2.0 KB (1980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d10133e4fd63cc4ffbf6285b14e6c1b636e7591abbbb6fb32f7dcc8f2a3f4c`  
		Last Modified: Tue, 22 Oct 2024 17:59:26 GMT  
		Size: 186.2 KB (186187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4974b8ed96bf0d249e2fc153f30d1503affbf4733a9365ffc3fdfdd151f88bd`  
		Last Modified: Tue, 22 Oct 2024 17:59:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ce7a819f9b80eaf5053066f72f6b9d9354c75e253234a4f2c8983fd2915357`  
		Last Modified: Tue, 22 Oct 2024 17:59:27 GMT  
		Size: 115.5 KB (115541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.25` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:504edbd13b9c5f8f4dc617a3ae60139c9bbee4b6fe930fedb969b3cdf396987c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10628ed1ae142c8cb3171d218a34b4ba3ecec73d2c56b4b84f8553a1bed2d997`

```dockerfile
```

-	Layers:
	-	`sha256:cb89a69e332c54ece4944c34fc5223390b59538d3294b858f4420d73b1f6173f`  
		Last Modified: Tue, 22 Oct 2024 17:59:26 GMT  
		Size: 2.6 MB (2553549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff80201f47ef124478f7c25a33e65ec7b48a3565b23e5d1103000a23af257d94`  
		Last Modified: Tue, 22 Oct 2024 17:59:26 GMT  
		Size: 38.1 KB (38090 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.15.4`

```console
$ docker pull elasticsearch@sha256:a3a9e33bd3518d97c549ab737989395fe36ddd455dec21e18f247901bd0cf81e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:3cd4c48a4f954a687025ad7ac20856897ba4ddf7ac4c96fc95d813bd69caf946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.8 MB (650758576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960d9b5837b8b89481b3cf3cee2f7e026abf2ee75595bca88740c2d02ad585a2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2024 16:58:33 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 16:58:33 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 16:58:33 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Nov 2024 16:58:33 GMT
LABEL org.label-schema.build-date=2024-11-07T09:35:45.535387784Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ec7e3608de63c104724277ebfa8dc7b84685f48 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.4 org.opencontainers.image.created=2024-11-07T09:35:45.535387784Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ec7e3608de63c104724277ebfa8dc7b84685f48 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.4
# Tue, 12 Nov 2024 16:58:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Nov 2024 16:58:33 GMT
CMD ["eswrapper"]
# Tue, 12 Nov 2024 16:58:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81a9d8ec85ae991d7087271d03b2a5f2b308eb2fe853f79c8fe21d5f6295438`  
		Last Modified: Mon, 18 Nov 2024 23:08:12 GMT  
		Size: 7.5 MB (7523730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e948f06feab591790251d994f12b0473478b3d8f5fa55bb63ad4290c9da6dff7`  
		Last Modified: Mon, 18 Nov 2024 23:08:12 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91ed54f1546c75dddce011510317783b5d9c04bc8d65d82940d34ae8bd49682`  
		Last Modified: Mon, 18 Nov 2024 23:08:22 GMT  
		Size: 615.4 MB (615400342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38be2ad6624497ab4c1f525f14dd0ee0a9fef5ad9b309fb7783ac7781e351fb9`  
		Last Modified: Mon, 18 Nov 2024 23:08:12 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a985bfcdde3b3ee1078174a3eb3e42bc44225a6627398826c500ecc0ecbf54a8`  
		Last Modified: Mon, 18 Nov 2024 23:08:13 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6ab82fe44d97964855932ed417fc65e47c911d00d7ededfef27ec984b1d627`  
		Last Modified: Mon, 18 Nov 2024 23:08:13 GMT  
		Size: 191.9 KB (191910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70237b2bade0432d0c4cf15b322bb2c34341e3ab462f0ea562ad740b387a3cb2`  
		Last Modified: Mon, 18 Nov 2024 23:08:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7115a95f623ca85f70e36c90243122574ba31ad1a73c6b1b0ec0a4df38c481`  
		Last Modified: Mon, 18 Nov 2024 23:08:13 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1c0b11ecd217457b11c0d4ebea67a56e7bb29c005e66f89f5047941d1ffc501e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed763636d22a052df380d18a6ecfeb9eaab32de7dc6b4d3e341a6c1e602d2a7`

```dockerfile
```

-	Layers:
	-	`sha256:687d10b64471c94a42d1103b44e02d8ccda50bc6283f2c5d651b3eaae7f9bb00`  
		Last Modified: Mon, 18 Nov 2024 23:08:12 GMT  
		Size: 2.9 MB (2943183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:245c35a14627968bc86ed3c1e6399edf65d0fab4988130e923aae004a4abb55c`  
		Last Modified: Mon, 18 Nov 2024 23:08:12 GMT  
		Size: 37.9 KB (37904 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b1e1a125fe9f9af7918f1fe9ee00dbd9fe37a1b693c08432fa7b7c5f8a34285a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.3 MB (494258263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1b221e0b564008da303b7315398ca767f67cce0030c35fc902496be9d381e0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2024 16:58:33 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 16:58:33 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 16:58:33 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Nov 2024 16:58:33 GMT
LABEL org.label-schema.build-date=2024-11-07T09:35:45.535387784Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ec7e3608de63c104724277ebfa8dc7b84685f48 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.4 org.opencontainers.image.created=2024-11-07T09:35:45.535387784Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ec7e3608de63c104724277ebfa8dc7b84685f48 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.4
# Tue, 12 Nov 2024 16:58:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Nov 2024 16:58:33 GMT
CMD ["eswrapper"]
# Tue, 12 Nov 2024 16:58:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc895cb5cb5d3a3b7efd1d4f6dd7593c12321fdd7383704697e5b0213f17500f`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 7.3 MB (7347302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0fd9ad867422b2a6f093d60c1244d5e391ff43a794fcead8d76939b9621c2b`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 4.3 KB (4323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caed71613a34b334e906d3050841cb179ab7f6f08629ed4524816291f2ea26c`  
		Last Modified: Mon, 18 Nov 2024 23:42:27 GMT  
		Size: 460.6 MB (460620089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6de4a0eb1e4b5b9e2f3dcbceef46d71060da379d2a652493b2cb19800b1d8c`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49264330d18df9e059477e1d5e96960d0e107d34a76b277d1906c2208d383327`  
		Last Modified: Mon, 18 Nov 2024 23:42:18 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dba4836f3360debd72698431eaaffd857aa70b4f21a45a77422bb56793484e2`  
		Last Modified: Mon, 18 Nov 2024 23:42:18 GMT  
		Size: 185.9 KB (185923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a809358639310e36fc9a723da34b9732b39badb9494dcd0ce5ea4f6abb01b4`  
		Last Modified: Mon, 18 Nov 2024 23:42:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a742b17f9effb73a6ce8c12f53bc9b6a5cf22335c86864cbf9c7dc4fda380`  
		Last Modified: Mon, 18 Nov 2024 23:42:19 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1887585e57b5db435a2658c3faea65a8cb986ffe32153612936bafa2e39e63bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26fa50376b2ca57f8ffd368ca2cfcd07e9bef21f28f90ca2f8a40101f3e29b2`

```dockerfile
```

-	Layers:
	-	`sha256:89624d9d8e41b0516f59f994d069a9a191030c3d1c2d5a3ab7431a67c030f2ac`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 2.9 MB (2942152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d177e8796d77b7b12011bb7436e43e0d3cb02b49a8a1e350b744526a268d340`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 38.1 KB (38107 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.16.1`

```console
$ docker pull elasticsearch@sha256:e5ee5f8dacbf18fa3ab59a098cc7d4d69f73e61637eb45f1c029e74b1cb200a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.16.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d6878475f25bfea020573cf0dd94aab8e80688b0c55cdc97c40264e72026d301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.4 MB (676423233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bd8c11e2e7ead52c0200d6d7f2007874ab776e7fa62b643b97574f7ba81caf`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 14:43:56 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
ENV SHELL=/bin/bash
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.build-date=2024-11-19T16:00:31.793213192Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ffe992aa682c1968b5df375b5095b3a21f122bf3 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.1 org.opencontainers.image.created=2024-11-19T16:00:31.793213192Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=ffe992aa682c1968b5df375b5095b3a21f122bf3 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.1
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 21 Nov 2024 14:43:56 GMT
CMD ["eswrapper"]
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5284e56853e59c3cd65ac4e5b6d29b741218254ce00ecabadc6a5eb8d8f6d3`  
		Last Modified: Fri, 22 Nov 2024 22:29:28 GMT  
		Size: 7.5 MB (7523664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a83fbdc57cf00c7f01c43f754f830df5b73f1a77366102076ea8a9284198015`  
		Last Modified: Fri, 22 Nov 2024 22:29:27 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d795c858d6ef5fb843aadf47e0318946eeb41a0a397a1d794d3ae0a93d923760`  
		Last Modified: Fri, 22 Nov 2024 22:29:42 GMT  
		Size: 641.1 MB (641065067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7794733e5c4a80ba044fd99afc2d62f52a5dae1ebe0f7fe57e96484d3ca076`  
		Last Modified: Fri, 22 Nov 2024 22:29:27 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d6e0f319b04d0a3318a454bf25afcd76944c4749741e4476fb69a2d3040a19`  
		Last Modified: Fri, 22 Nov 2024 22:29:28 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7c37b51a32bf0b8e165d91d854b1f85b5399bcbaa75fd0cf9c98aaf4721b92`  
		Last Modified: Fri, 22 Nov 2024 22:29:28 GMT  
		Size: 191.9 KB (191906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645b8ddcf26d3c0d93e43847141c3636ec72a57b66d6252a00f85f7e86b51d09`  
		Last Modified: Fri, 22 Nov 2024 22:29:29 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2575b34d7a7f0ec4b501f9c799c476149509608887cfc755210de7dca534bf8`  
		Last Modified: Fri, 22 Nov 2024 22:29:29 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ea02471241e54ba89702f0406a62e87c831b5d5ab427a7ef0eae1f7fb0ba92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c820c2b026c460a9050d6393541cadcd24f6dfc1640f7b65a0592c9bb2c3701`

```dockerfile
```

-	Layers:
	-	`sha256:3d25a57a6bbe13e63b553893d2bf891eb8a291e8eecd0333f23d3633a93ec981`  
		Last Modified: Fri, 22 Nov 2024 22:29:28 GMT  
		Size: 3.0 MB (3010092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3535b4f150516e9e3eac975145056a6eb7394412250343d60805bbab67f085`  
		Last Modified: Fri, 22 Nov 2024 22:29:27 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.16.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c5ea110d0a644fbfaaf44ab1d16612e510b2f977afc333aa261d981a8af12784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.8 MB (519769532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93690647f924d1bd03be51543f091f0ed5974e8fcc88d0a395790f18cf15949`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 14:43:56 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
ENV SHELL=/bin/bash
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.build-date=2024-11-19T16:00:31.793213192Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ffe992aa682c1968b5df375b5095b3a21f122bf3 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.1 org.opencontainers.image.created=2024-11-19T16:00:31.793213192Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=ffe992aa682c1968b5df375b5095b3a21f122bf3 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.1
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 21 Nov 2024 14:43:56 GMT
CMD ["eswrapper"]
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc895cb5cb5d3a3b7efd1d4f6dd7593c12321fdd7383704697e5b0213f17500f`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 7.3 MB (7347302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0fd9ad867422b2a6f093d60c1244d5e391ff43a794fcead8d76939b9621c2b`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 4.3 KB (4323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8e0ffee7c9e89363344a4ab50b7d78708cae11dabe1981c00b3e003900a968`  
		Last Modified: Fri, 22 Nov 2024 22:32:24 GMT  
		Size: 486.1 MB (486131338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d733871a0031e03ac68a7da4aae2768e49f71feef31dfea8faf1a2a4a6070387`  
		Last Modified: Fri, 22 Nov 2024 22:32:12 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ae58363b94c788801a49d22f9bc7ff2a1da18ea26f7a0cad5ef16ebc43254`  
		Last Modified: Fri, 22 Nov 2024 22:32:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab6cd2208d6b34cd383cf0abf386d0b11111364b366a9b27b7170c2c4f896b5`  
		Last Modified: Fri, 22 Nov 2024 22:32:12 GMT  
		Size: 185.9 KB (185931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41882eb00176e59a60b809b82d542bb6c249ecb1752b41f1f99c5863560bda9`  
		Last Modified: Fri, 22 Nov 2024 22:32:13 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e2352a9791a655c09b873870a3c4221d3698bdb508c8b3022119193076dfde`  
		Last Modified: Fri, 22 Nov 2024 22:32:13 GMT  
		Size: 115.5 KB (115540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:efbabd1f8b3cc9d0f859f2f2ae80945acef88c380643d8089973445a5b3b6426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b2448ac2c9e7530e5782134c8b5de6833987a232b07c9622d539364f824e5`

```dockerfile
```

-	Layers:
	-	`sha256:8b4dd864061e48de71db7b5e7ecca413a72761d1e4e5d591c603c1bee5124baa`  
		Last Modified: Fri, 22 Nov 2024 22:32:13 GMT  
		Size: 3.0 MB (3009061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2cc87c4980f775b182acff18d977d534f38e4ed9dbd15b2f4b8c75db5131c8`  
		Last Modified: Fri, 22 Nov 2024 22:32:12 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json
