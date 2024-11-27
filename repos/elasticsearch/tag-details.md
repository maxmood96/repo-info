<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.25`](#elasticsearch71725)
-	[`elasticsearch:8.15.5`](#elasticsearch8155)
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

## `elasticsearch:8.15.5`

```console
$ docker pull elasticsearch@sha256:82d39a05c027480938d5d405d7ddd933f221effcd1d8a33356f0dd0212640df9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:c7dd133ad77ec2a6ceb03a0daaa9c8556626a3e4f245daed0b62c7ecb4be3df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.1 MB (651068006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e983a5cfa41874a2c248b3a50dbdf98449b066c5e665987fd6b32b8126bf47d9`
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
# Tue, 26 Nov 2024 10:47:54 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.build-date=2024-11-21T22:06:13.985834967Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b10896bcfe167cce44a84ba2771d101fb596d40d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.5 org.opencontainers.image.created=2024-11-21T22:06:13.985834967Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b10896bcfe167cce44a84ba2771d101fb596d40d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.5
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 10:47:54 GMT
CMD ["eswrapper"]
# Tue, 26 Nov 2024 10:47:54 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e9ebd97e160eb4ce1e1ae6b499f9a23847d73bf8e939e9d49db8c3f152543f`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 7.5 MB (7523702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de1bd8f314146b8d61ebc77b9d96d5847ae8ffe47f00bf1b365250369111787`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6d6fb462c845d40fe4bf5da328c37cf7481f768157705a029199e7a1f20d8`  
		Last Modified: Tue, 26 Nov 2024 18:27:25 GMT  
		Size: 615.7 MB (615709821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62ec68f75a4abbc9ac5a9b50f78dd02eeb337e73332348519a7221fef91ed3`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0e24c5da73d95c4adabbad02355182ccd146391907a48e21fd5fcf80a0582`  
		Last Modified: Tue, 26 Nov 2024 18:27:18 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7e76321b94ba543b31a032524a201b8daef69416391cacec8cd8a599031b94`  
		Last Modified: Tue, 26 Nov 2024 18:27:18 GMT  
		Size: 191.9 KB (191900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a014a471a9ee7cb8aab4075e3676dbfe772c2468c93541a3e28b2e615b028a7e`  
		Last Modified: Tue, 26 Nov 2024 18:27:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e040db56d40fa9c7caa905995fef4f8d023ca3c903e5104cbd8a09c483845889`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
		Size: 115.5 KB (115526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5e9f9f12d35a34aa50ee434f5d40510ff4861f23d0136650d94c44823b60a702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fd65a763bde738696a996fd48c4fd6d7e5bcada69490b64a66772df1fe50e5`

```dockerfile
```

-	Layers:
	-	`sha256:c5e9a25ee347f755ad92b22c3734859abe4e5e2ce827b0940f03a16aad9cbe95`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 2.9 MB (2942603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478de23964428271c6cec2d24ae2f96f1f2ae3a7d8141f0d1029742d1e08a022`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 37.9 KB (37904 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:90185845d8ccb9810ca11aeee110891bfceba201743e81c1037bc1c08fd213ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.6 MB (494571156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4ce1c00571537453baa36c31ed176d2ed6663b0d6b5e49d05e6cd311796892`
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
# Tue, 26 Nov 2024 10:47:54 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.build-date=2024-11-21T22:06:13.985834967Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b10896bcfe167cce44a84ba2771d101fb596d40d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.5 org.opencontainers.image.created=2024-11-21T22:06:13.985834967Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b10896bcfe167cce44a84ba2771d101fb596d40d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.5
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 10:47:54 GMT
CMD ["eswrapper"]
# Tue, 26 Nov 2024 10:47:54 GMT
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
	-	`sha256:e27e0a18ea97478d6e587e29fb7c78dbc38a803df994cf3e40e7cd5f5337513e`  
		Last Modified: Tue, 26 Nov 2024 18:27:30 GMT  
		Size: 460.9 MB (460932961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e8b0295b66bd4377e566365cd4cccae2f01fe242146b2689e46248a7019446`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7b9aebe61c0e9a2a65cad568d558c8aaddf1bdac36ccc18949d6a4e0501268`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aec644b5f803bbcc2363566a14fca3c8fdeafdcb92c1939e2df10c606d9e0b8`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
		Size: 185.9 KB (185932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc677c48115ee2c98ea5bbaf7f298835d26762fb37751573ba1024b2d2310395`  
		Last Modified: Tue, 26 Nov 2024 18:27:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c67805f190df50f59464637a503648ea576025c97a671a6e291cf228e1cc550`  
		Last Modified: Tue, 26 Nov 2024 18:27:20 GMT  
		Size: 115.5 KB (115539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:510ee99bb6b79ad2933523626725c896e05206e929f7e02e86869dfff050b154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2979679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c84c91bb2b60b3266bd20927b18512e2ea3fc3d73664daae3a6b2de2466e6`

```dockerfile
```

-	Layers:
	-	`sha256:12ed4c4366f33da22956372ac9e4ebbfd7058d9d71bec62469d1a3e89ccc6c8d`  
		Last Modified: Tue, 26 Nov 2024 18:27:20 GMT  
		Size: 2.9 MB (2941572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886c2fcd5499eff2aaf0c4e2f8ecd8c1d92b72bb39398dfbac59cb830f1b99fa`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
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
