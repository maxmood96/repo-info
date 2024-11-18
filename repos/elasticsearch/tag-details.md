<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.25`](#elasticsearch71725)
-	[`elasticsearch:8.15.4`](#elasticsearch8154)
-	[`elasticsearch:8.16.0`](#elasticsearch8160)

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
$ docker pull elasticsearch@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `elasticsearch:8.16.0`

```console
$ docker pull elasticsearch@sha256:a411f7c17549209c5839b69f929de00bd91f1e2dcf08b65d5f41b122eae17f5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.16.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b834a33c1ef3d886e1a9c145fc63d17a83cf30b51af43bfa54c7d0bd42cb463a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.0 MB (675985020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e5d31650746ae2305bad980cb3ead660bf3dcd484089466c74fa12cdb8a859`
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
# Tue, 12 Nov 2024 13:42:14 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 13:42:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Nov 2024 13:42:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 13:42:14 GMT
ENV SHELL=/bin/bash
# Tue, 12 Nov 2024 13:42:14 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Nov 2024 13:42:14 GMT
LABEL org.label-schema.build-date=2024-11-08T10:05:56.292914697Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=12ff76a92922609df4aba61a368e7adf65589749 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.0 org.opencontainers.image.created=2024-11-08T10:05:56.292914697Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=12ff76a92922609df4aba61a368e7adf65589749 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.0
# Tue, 12 Nov 2024 13:42:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Nov 2024 13:42:14 GMT
CMD ["eswrapper"]
# Tue, 12 Nov 2024 13:42:14 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513e444d93a4089577889417b23c4d9a6cc4e558844cf2fbe23bdc5c22137`  
		Last Modified: Tue, 12 Nov 2024 20:12:55 GMT  
		Size: 7.5 MB (7523647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0ce1fe2eb3b921b94a90c473649ec50ce489796f4352619a842f3739208ea5`  
		Last Modified: Tue, 12 Nov 2024 20:12:55 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13af542526725f8e48aa9ea066ae7f8eab7503ab9364f7907f8303b67b26234`  
		Last Modified: Tue, 12 Nov 2024 20:13:08 GMT  
		Size: 640.6 MB (640626861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca940e27983ae665e4f8a97fb62aeee5b6f0103212c0c6e9a34b1d1be93cc3d`  
		Last Modified: Tue, 12 Nov 2024 20:12:55 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90036ae70e51447a1fd6d4a4931dec21f2d6868de54971e39d2ea043b76b006d`  
		Last Modified: Tue, 12 Nov 2024 20:12:56 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a78b7f7b9e3a06e33deb0d55d3ca59946526889e55e8be07f9ec5af8b4c90e4`  
		Last Modified: Tue, 12 Nov 2024 20:12:56 GMT  
		Size: 191.9 KB (191906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1261f6d994e5035b14440e7091f33b9cdd28e7cad0dc9fea45876f737889298a`  
		Last Modified: Tue, 12 Nov 2024 20:12:56 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd1cd2739df3214ee189bb42b7d1aa1fa3af42c9240d30d4957ed8345597b8a`  
		Last Modified: Tue, 12 Nov 2024 20:12:57 GMT  
		Size: 115.5 KB (115538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8fd4b3c535e6120b882a126ef9260e8df9808052197d5e1b124ad390fe46e1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f848e32d1d98f788a4547e5c323caf4ac894ed45cc9903688d34f0a7696f107c`

```dockerfile
```

-	Layers:
	-	`sha256:2cf35790db805ae71965b8ed25a73e075991944a8b91a8abc53c2ee6749ad816`  
		Last Modified: Tue, 12 Nov 2024 20:12:55 GMT  
		Size: 3.0 MB (3010672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede9cc774970dd170e5ff013c6b853899b7f781d209dea7e4ab050d2d213180d`  
		Last Modified: Tue, 12 Nov 2024 20:12:55 GMT  
		Size: 38.2 KB (38205 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.16.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c4d9c369220bcb5339dfd8060790dbed1a6bbd5ee6efcc5e8d57c880dd09bbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.3 MB (519338785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81d18714ce1620ef072d1729e568eb693fabbb0db878725cde333756d64c87b`
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
# Tue, 12 Nov 2024 13:42:14 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 13:42:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Nov 2024 13:42:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 13:42:14 GMT
ENV SHELL=/bin/bash
# Tue, 12 Nov 2024 13:42:14 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Nov 2024 13:42:14 GMT
LABEL org.label-schema.build-date=2024-11-08T10:05:56.292914697Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=12ff76a92922609df4aba61a368e7adf65589749 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.0 org.opencontainers.image.created=2024-11-08T10:05:56.292914697Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=12ff76a92922609df4aba61a368e7adf65589749 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.0
# Tue, 12 Nov 2024 13:42:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Nov 2024 13:42:14 GMT
CMD ["eswrapper"]
# Tue, 12 Nov 2024 13:42:14 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473eb5b4772c762dec6ce4ecbcf8e16d63678f3cc7feee193c72f2bff27fb064`  
		Last Modified: Wed, 13 Nov 2024 03:14:14 GMT  
		Size: 7.3 MB (7347330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd134931ff62b520f550b12c5c0e27bd5c52e0f7e15d81ae1c190ed27edfa901`  
		Last Modified: Wed, 13 Nov 2024 03:14:13 GMT  
		Size: 4.3 KB (4326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0405857d0d750a6a40e48332bd2a4c2c171abe2112dbfd8ae32ab3d487c1726`  
		Last Modified: Wed, 13 Nov 2024 03:14:27 GMT  
		Size: 485.7 MB (485700598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d949094aaeb759f0a71160eb46828c55e3f348f082466444005973728cd7c37`  
		Last Modified: Wed, 13 Nov 2024 03:14:13 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e31900ae5305e31dc150e6316afaa2f98229acce4296c67197b0e17cb0535c2`  
		Last Modified: Wed, 13 Nov 2024 03:14:14 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243eea34a3f5c9854f2019e1118a7264928805cfa48e2d689f6c4d1724eefb8d`  
		Last Modified: Wed, 13 Nov 2024 03:14:15 GMT  
		Size: 185.9 KB (185918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70edfb86b1ae9874ab791da046e2cb1fe50ccfc321072bbf6ab4aba309b594b2`  
		Last Modified: Wed, 13 Nov 2024 03:14:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c3ebe1632ae2d55f596acfae481f8d9efafee90aa5b5fb2455971ef4a8488a`  
		Last Modified: Wed, 13 Nov 2024 03:14:15 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:16cb8b7c0dacb996a9ec0ddecb8a1688cb5c5561ff826f84347ef3807ae52758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb242f70c790716c89d013ed509f7db01e007e640383f9a8fa8854f19b475d7b`

```dockerfile
```

-	Layers:
	-	`sha256:5bbd766ea0f68d6ddc8dff2880ddcd834b2a244582e214c6ca95f03a49198895`  
		Last Modified: Wed, 13 Nov 2024 03:14:14 GMT  
		Size: 3.0 MB (3009641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35880c968289fee1bf42c6a0c85075beb2f019d072e5bbf65c14ce51d4e607eb`  
		Last Modified: Wed, 13 Nov 2024 03:14:13 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json
