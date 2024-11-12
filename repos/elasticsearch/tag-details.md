<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.25`](#elasticsearch71725)
-	[`elasticsearch:8.15.3`](#elasticsearch8153)
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

## `elasticsearch:8.15.3`

```console
$ docker pull elasticsearch@sha256:54468761d3c815759843c1bdde088604c13ac0e45c626750c0a9bd0a43c0da3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2690b9545898cb1cba114eda687b60a500c071898f20265eb8ae8fdd23908ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 MB (650203462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d9686af70e3636215b50f493116f483b8692c6cb93d21a24e018d6796ea15`
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
# Thu, 17 Oct 2024 12:21:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.build-date=2024-10-09T22:08:00.328917561Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f97532e680b555c3a05e73a74c28afb666923018 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.3 org.opencontainers.image.created=2024-10-09T22:08:00.328917561Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f97532e680b555c3a05e73a74c28afb666923018 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.3
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 17 Oct 2024 12:21:47 GMT
CMD ["eswrapper"]
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4b793b4c8c52aa9f3c852bf62680d695c08768f5135c7ceee8e61ea9b6b0e2`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 7.5 MB (7523758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c906761a986525513cfd8dbdc3d9a19944fa0e13960068dc26c5cdb456721f9a`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c183ad3bd8a3e053d7acbccc66d21d4ce7f650bf269037fb1e661a4d4352f86b`  
		Last Modified: Thu, 17 Oct 2024 20:59:18 GMT  
		Size: 614.8 MB (614845210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9d54640409fcca31b61bfe6c98f0401b17e81d4675b29ad073ea450a9ce29c`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c61b4194a094fcb55a5c51ba6176068f7e2a1a3c6dfed871d8468200eb3dd6`  
		Last Modified: Thu, 17 Oct 2024 20:59:11 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d4ae1d77a296deab71413dfcf6150b0f4cff2dfd7a998a4c3ff847783cbd39`  
		Last Modified: Thu, 17 Oct 2024 20:59:11 GMT  
		Size: 191.9 KB (191904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d788479c6bf1512c9578187d54ded1affee689b2dfa6a71b29e07059445bd3`  
		Last Modified: Thu, 17 Oct 2024 20:59:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374f4ff29ffce15f4c8c6af65db8b0c8fff1dd97c74d4d5c85729a96bd447af`  
		Last Modified: Thu, 17 Oct 2024 20:59:12 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:94893219150f6abf8ee7fece463e79557647dd6c504c117f330289088d14bddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2894218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b198d41f81cf18fb9c9fb26f9d8f99f54ba5a297d0664c5c408da67bd45e5e`

```dockerfile
```

-	Layers:
	-	`sha256:2cf2ca410c9704094a5ff2f19cf445b31dcfa049702ad299505f34f98a831ba6`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 2.9 MB (2856530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cbb504a18d038974de7185911b4f9b089a17b3b833c632824ce981e1f347812`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 37.7 KB (37688 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:ef32189bb3fdcfaf3dc1f9d50444883380e26cbb3c8fc88820faf9f67d3a2228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.7 MB (493713691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfcebb5958a96d48404026e016384940f776b434fd8f33f9e5dd24723cf799fb`
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
# Thu, 17 Oct 2024 12:21:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.build-date=2024-10-09T22:08:00.328917561Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f97532e680b555c3a05e73a74c28afb666923018 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.3 org.opencontainers.image.created=2024-10-09T22:08:00.328917561Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f97532e680b555c3a05e73a74c28afb666923018 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.3
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 17 Oct 2024 12:21:47 GMT
CMD ["eswrapper"]
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6126ba20a2f4f0d9b244bc4eb31f8371a886131254f264a47d9f4c849e44ca`  
		Last Modified: Wed, 16 Oct 2024 02:46:51 GMT  
		Size: 7.3 MB (7347326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0262944513a3fde69a989ef8a782aad588b8f85f4e1a1eced030b54168819d`  
		Last Modified: Wed, 16 Oct 2024 02:46:50 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7168973486737c052342f699752a25c90e0093c8bd18174c43e9ca416f097206`  
		Last Modified: Thu, 17 Oct 2024 22:14:32 GMT  
		Size: 460.1 MB (460075484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fcba5a230599c3a61b4055ccd5d34a283ca58dc0805dea38fc7e28ae0c4a76`  
		Last Modified: Thu, 17 Oct 2024 22:14:21 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9e5ced205af77fc609cda9b41bf2893970386913cdd003abc41598bf9c780`  
		Last Modified: Thu, 17 Oct 2024 22:14:21 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bef60dc004c45d8449424e139ccf07dffb2cb295f3082648dc621da68b8b41`  
		Last Modified: Thu, 17 Oct 2024 22:14:22 GMT  
		Size: 185.9 KB (185922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ba8d2cfc8d6c8b91b7146da181ff0aba0c77f4b1dd49178eb7bcf89ca12d81`  
		Last Modified: Thu, 17 Oct 2024 22:14:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969dcaffb4e4cc846c28e70365ba9a61f5f82f9d220503213293d84755573faa`  
		Last Modified: Thu, 17 Oct 2024 22:14:23 GMT  
		Size: 115.5 KB (115541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e86771d80a201d69738ecafcb8b6b6a4c25d5870fcd4e86a384e0bb8355f06be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047b918948c954afb4fdfe2d31ed8663dad4e405eeaa0dcbe9878bb17964257`

```dockerfile
```

-	Layers:
	-	`sha256:d29d0e90666df36fa8292b72ed559aeb0fc95fc48d21f9af69ad6daac7397fd1`  
		Last Modified: Thu, 17 Oct 2024 22:14:22 GMT  
		Size: 2.9 MB (2855499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a16bf7ca56f2d6f7397a59fde7133c453807fc1cb07c4f1feb26d4202bc41f99`  
		Last Modified: Thu, 17 Oct 2024 22:14:21 GMT  
		Size: 37.9 KB (37885 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.16.0`

```console
$ docker pull elasticsearch@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
