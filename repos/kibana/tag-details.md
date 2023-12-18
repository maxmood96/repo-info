<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.16`](#kibana71716)
-	[`kibana:8.11.2`](#kibana8112)
-	[`kibana:8.11.3`](#kibana8113)

## `kibana:7.17.16`

```console
$ docker pull kibana@sha256:47926ffa4915bd40c51a82604930afec0ea9c3dbc04630ffe9be03d59bf817cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.16` - linux; amd64

```console
$ docker pull kibana@sha256:9128162448025f388414c36d37cd4f02b6ee5b9b2c46f7b522c457985a134101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.4 MB (356384197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ebfdd8ec8b9d878e1d00d2d7dd202c4dcf655cc0b2f432ca0305e0da25f0c7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Dec 2023 12:49:29 GMT
ARG RELEASE
# Tue, 12 Dec 2023 12:49:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 12:49:29 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Dec 2023 12:49:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.build-date=2023-12-08T12:07:39.833Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5838d16e60eb684b785702c80ff41e59d344fe1f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.16 org.opencontainers.image.created=2023-12-08T12:07:39.833Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5838d16e60eb684b785702c80ff41e59d344fe1f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.16
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Dec 2023 12:49:29 GMT
USER kibana
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d560b9e6f5f02566742923e8ff5b77a6b3a567c262946322ff300a405d8e10a3`  
		Last Modified: Sat, 16 Dec 2023 10:50:53 GMT  
		Size: 10.5 MB (10530599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9590e1b10b3d48fd1a67031832e2b55b85c3c2d661aefe69d99f50f380e3322`  
		Last Modified: Sat, 16 Dec 2023 10:50:52 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facf15002fc127b82f0e037b7e1b0442d8aad2c5368ff4728975a7c2b004adc0`  
		Last Modified: Sat, 16 Dec 2023 10:50:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868eaeda2e4748a3edc384999c7e080d512dd9ea6ca722140c0dc1b49d9122c1`  
		Last Modified: Sat, 16 Dec 2023 10:50:54 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f77f0366e324711d634a02883e69cad0af9b3c96e62fbbb2aa94a9bc2215521`  
		Last Modified: Sat, 16 Dec 2023 10:50:54 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6db9085d891d5c631e3acb9b18e3878731c660c51b786b8c9de657969e69eb`  
		Last Modified: Sat, 16 Dec 2023 10:51:02 GMT  
		Size: 301.7 MB (301668667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e8a3c8313c3f08c608362db5ff0f12f058920fa85d259298882edd4424e1db`  
		Last Modified: Sat, 16 Dec 2023 10:50:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141b4666c662c2dc1462588e6a0d484a0f90367f85a60422c8d80506bb497275`  
		Last Modified: Sat, 16 Dec 2023 10:50:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c841eeb902cdfed83e48c9f423d3a79554c2a37936e1ab337c66fc1b29b31d`  
		Last Modified: Sat, 16 Dec 2023 10:50:55 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a684f7ab43924af0881fdb5c8624c09e977257582634f7765831c707fe3862d0`  
		Last Modified: Sat, 16 Dec 2023 10:50:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338d4654e26f66e55cf6a692603b79fd84008a7c16ab1e448e8b4bd51f6d6277`  
		Last Modified: Sat, 16 Dec 2023 10:50:56 GMT  
		Size: 189.4 KB (189404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82d3397a0599053d10d876173051f3b34adec4bac19d9b3f7516fc954422670`  
		Last Modified: Sat, 16 Dec 2023 10:50:56 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.16` - unknown; unknown

```console
$ docker pull kibana@sha256:8ec46201c6fa4a02674eee134729242f0d9c1d9ab93fdb6a7205eb445b9554e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da029303c8170847cc907456142ae4aca90e9f250a603c1eb348fdd2dff385b5`

```dockerfile
```

-	Layers:
	-	`sha256:285f978d3404a186152201b70f8d2f7f0e4396969e1a3c7551c9caaa2796b246`  
		Last Modified: Sat, 16 Dec 2023 10:50:53 GMT  
		Size: 3.0 MB (3033311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b92ee8f017b52df3e4a1cf17e7eb9cb2871cf638b07cfa495340ba9671a832`  
		Last Modified: Sat, 16 Dec 2023 10:50:53 GMT  
		Size: 44.4 KB (44362 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.16` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:a13f6bc2d200a9b4aa3a781aad7353d8ff233a7d0151f67c2301fdb81b1ee0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (367027222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e5d9f12b881ac451619a8351639e34fc975dfa182499724110fefdeb977972`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Dec 2023 12:49:29 GMT
ARG RELEASE
# Tue, 12 Dec 2023 12:49:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 12:49:29 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 12:49:29 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Dec 2023 12:49:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Dec 2023 12:49:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 12:49:29 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 12:49:29 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Dec 2023 12:49:29 GMT
LABEL org.label-schema.build-date=2023-12-08T12:07:39.833Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5838d16e60eb684b785702c80ff41e59d344fe1f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.16 org.opencontainers.image.created=2023-12-08T12:07:39.833Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5838d16e60eb684b785702c80ff41e59d344fe1f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.16
# Tue, 12 Dec 2023 12:49:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Dec 2023 12:49:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Dec 2023 12:49:29 GMT
USER kibana
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b33c1a27bbb4c31c43eb167ae3df748361fefa96bbfa0dec48c68a4c1e33ca1`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 10.4 MB (10396649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98059de69b424d043bad0fbc3aa68baae6367fabf5f63704de018bfe92e97239`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae0f05ad9a7ff1532ceaf39932fb0b9a88a8de625669867c4f1e74135770c4d`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c897b19d6be892715b84b17db2bce8870bb544cd8aaa14b5d69487582a2542`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 16.5 MB (16460497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e8ede858fed3dc2c66c8f0b11d0b7b977202fc35ee37a2c50784b2b716f601`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691cc7d9617e86d3da6690bd3667b184e535b5b8d048bd7130c787c4b0323287`  
		Last Modified: Mon, 18 Dec 2023 19:58:43 GMT  
		Size: 314.0 MB (313990045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29be76c9e51c929c68a52ff4969d9bd70e14aea30d8f37b54a3978693d650b98`  
		Last Modified: Mon, 18 Dec 2023 19:58:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27e77577fa567e2c060b8acd4f9027dae20229a532a90d57e83d00c57c15fc4`  
		Last Modified: Mon, 18 Dec 2023 19:58:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cf1139dc5a8ba3b59aef0ad95c952aafe32fdb31a3c9ebfd71b355fcd4445f`  
		Last Modified: Mon, 18 Dec 2023 19:58:36 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f460194b70535a5c1330449a9b5c01bd0ee11898f8da223db9320cec973ee2`  
		Last Modified: Mon, 18 Dec 2023 19:58:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec71c63e4e93a26c161397366b453e569e598b46b8508c9fa90cdc32767563`  
		Last Modified: Mon, 18 Dec 2023 19:57:34 GMT  
		Size: 183.4 KB (183409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab8892e134071fe33e0cdaf171c5ced2a24ed083f343c7d0b72feb484428cad`  
		Last Modified: Mon, 18 Dec 2023 19:58:38 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.16` - unknown; unknown

```console
$ docker pull kibana@sha256:c68c5d650943190b4fd2e5e87f24991849445b61ff81c7fd8df071e0a8f3549d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c58678509f40d84e5793f23c9c42f85a373c1b155121067a3946617dca16afa`

```dockerfile
```

-	Layers:
	-	`sha256:6c00afdd1a8b5404216703687379067d0323238ae540d08d7df0f2180296ae46`  
		Last Modified: Mon, 18 Dec 2023 19:58:36 GMT  
		Size: 3.0 MB (3033652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8251be2aadaf762c17b81f900ea86d56943296c13426db5e42769657baa41235`  
		Last Modified: Mon, 18 Dec 2023 19:58:36 GMT  
		Size: 44.2 KB (44206 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.11.2`

```console
$ docker pull kibana@sha256:63c1e68a5d1de0822254669b6d9edbc4780c2827c4286dd36e7aa8e9bfa717d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.11.2` - linux; amd64

```console
$ docker pull kibana@sha256:71d6ff5095b5ee8a95428bf16ea32f50cece38c63c41ba6196aa2c37884ad21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368865401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d87083b6877f3c9a0d29f051c330f1915094584ce7850535ba38488c13b4530`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 07 Dec 2023 12:34:16 GMT
ARG RELEASE
# Thu, 07 Dec 2023 12:34:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 07 Dec 2023 12:34:16 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 12:34:16 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 07 Dec 2023 12:34:16 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN fc-cache -v # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
WORKDIR /usr/share/kibana
# Thu, 07 Dec 2023 12:34:16 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Dec 2023 12:34:16 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.label-schema.build-date=2023-12-05T12:05:54.257Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=92746356b61c3e3ac62b6d7045727f8d737fa4b5 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.11.2 org.opencontainers.image.created=2023-12-05T12:05:54.257Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=92746356b61c3e3ac62b6d7045727f8d737fa4b5 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.2
# Thu, 07 Dec 2023 12:34:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 07 Dec 2023 12:34:16 GMT
USER kibana
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd3e2179f6c16f3046ba2f535e440ca4b3ca9e5914fda4bcc837231e2f6b42b`  
		Last Modified: Sat, 16 Dec 2023 10:51:37 GMT  
		Size: 10.5 MB (10530632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd32dcdeb4304dcea0936f74db19b409c175acf29c7948cee1701379a920b077`  
		Last Modified: Sat, 16 Dec 2023 10:51:17 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f07e394bd2569127212ef3b2c77ec52165b6cdd4d9ba795e7b3654c278d1ac`  
		Last Modified: Sat, 16 Dec 2023 10:51:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3684e3f2c49365477054bc85e8b6a9e08d214731878f0dee8f5565752fd013`  
		Last Modified: Sat, 16 Dec 2023 10:51:18 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2974a7dadec56e69c284e16d71ed41f0bc6a51548073f764154b6fc5d6a19f7b`  
		Last Modified: Sat, 16 Dec 2023 10:51:37 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfc58658730fb8cd81f8b773233271e78b4750898c9d86b6210d7c76dbc012b`  
		Last Modified: Sat, 16 Dec 2023 10:51:42 GMT  
		Size: 314.1 MB (314149804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d592fedb04540a84a92fe4e250bf9eda58bdb9527ccb58af1a0cd54dfb829`  
		Last Modified: Sat, 16 Dec 2023 10:51:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46938b99931d272ce68b2167fb5d37db335410935f44eea23f5adac8a1dede24`  
		Last Modified: Sat, 16 Dec 2023 10:51:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc22452aef9f904907c8839f76546b28c0d06df6854ab077776bcdd55ae4f7`  
		Last Modified: Sat, 16 Dec 2023 10:51:38 GMT  
		Size: 4.6 KB (4553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa4fc03deb6164693ebd38a7de03a4670b7efd2ef0b0cd76f3feb951c4725c`  
		Last Modified: Sat, 16 Dec 2023 10:51:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7890af4f0998bfa039806d4d7c6587a8c7ef7d3fdacb1a241db9fa11cd5bc7`  
		Last Modified: Sat, 16 Dec 2023 10:51:20 GMT  
		Size: 189.4 KB (189405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922f309876588623af2adf81c49831f358182a1df5c43ea9d0a5eaf75e9d97be`  
		Last Modified: Sat, 16 Dec 2023 10:51:38 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.11.2` - unknown; unknown

```console
$ docker pull kibana@sha256:db6ce478c0609f67763378a7afb4a0971c026f40380a20fccbdb6ccb66c0ddb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3481554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5141069f17a5d791c3a4789c1bbb7d127acf0c40b904b36f3b2d63764176a14`

```dockerfile
```

-	Layers:
	-	`sha256:79f2d9524d89b415c32049b960e447645e6c669424be3705cf48b3456e98c8b5`  
		Last Modified: Sat, 16 Dec 2023 10:51:37 GMT  
		Size: 3.4 MB (3437198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71eb042e9a80c71b46fe9214b48caa6f535cd5d49a226bd97824f7da4a91cfea`  
		Last Modified: Sat, 16 Dec 2023 10:51:37 GMT  
		Size: 44.4 KB (44356 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.11.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1870bd9b72b074b7d44437a35805d96bbafd7bc11770707063c5477b3908b152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379685079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61891ff6e12ef769c244dbae0a9c33983f6e76b5c3747e27ee3079ac67769923`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 07 Dec 2023 12:34:16 GMT
ARG RELEASE
# Thu, 07 Dec 2023 12:34:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 07 Dec 2023 12:34:16 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 12:34:16 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 07 Dec 2023 12:34:16 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN fc-cache -v # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
WORKDIR /usr/share/kibana
# Thu, 07 Dec 2023 12:34:16 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 07 Dec 2023 12:34:16 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 12:34:16 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 07 Dec 2023 12:34:16 GMT
LABEL org.label-schema.build-date=2023-12-05T12:05:54.257Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=92746356b61c3e3ac62b6d7045727f8d737fa4b5 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.11.2 org.opencontainers.image.created=2023-12-05T12:05:54.257Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=92746356b61c3e3ac62b6d7045727f8d737fa4b5 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.2
# Thu, 07 Dec 2023 12:34:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 07 Dec 2023 12:34:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 07 Dec 2023 12:34:16 GMT
USER kibana
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b33c1a27bbb4c31c43eb167ae3df748361fefa96bbfa0dec48c68a4c1e33ca1`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 10.4 MB (10396649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98059de69b424d043bad0fbc3aa68baae6367fabf5f63704de018bfe92e97239`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae0f05ad9a7ff1532ceaf39932fb0b9a88a8de625669867c4f1e74135770c4d`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c897b19d6be892715b84b17db2bce8870bb544cd8aaa14b5d69487582a2542`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 16.5 MB (16460497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e8ede858fed3dc2c66c8f0b11d0b7b977202fc35ee37a2c50784b2b716f601`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4f24bb3249181638687a53d8fc527c81b083667f56541fa919388690bb773`  
		Last Modified: Mon, 18 Dec 2023 19:58:13 GMT  
		Size: 326.6 MB (326647850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc65b3aaa6f322501278035f178028374180348d85c2594fb24060d37477e428`  
		Last Modified: Mon, 18 Dec 2023 19:58:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abc92afe46005fb43a0e25931e991d8718e957569b8b00c77a0b3bd63c99d25`  
		Last Modified: Mon, 18 Dec 2023 19:58:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac185be6da4efc4fc25bb7e9684af4f9555fbf698d8786acc25e617f1137565`  
		Last Modified: Mon, 18 Dec 2023 19:58:07 GMT  
		Size: 4.6 KB (4556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838a1ce3be7f8cb72b216fd9ed60089046c3d3b95c14ff573a8d3fb04ed2fed2`  
		Last Modified: Mon, 18 Dec 2023 19:58:08 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec71c63e4e93a26c161397366b453e569e598b46b8508c9fa90cdc32767563`  
		Last Modified: Mon, 18 Dec 2023 19:57:34 GMT  
		Size: 183.4 KB (183409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbc5572c58fa6cf11f1e7adbad77597da628c0a3719b3ad8bf0a0e41e742cd9`  
		Last Modified: Mon, 18 Dec 2023 19:58:08 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.11.2` - unknown; unknown

```console
$ docker pull kibana@sha256:7fdade0be3d49a6701c6f7e804c604b4234a4b3ce540227a36c8b73583d3876f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3481738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019e48d9d42fe70bc1b28033cbf84ca89d3bd0034cb7cdc51233e37a1f8389b4`

```dockerfile
```

-	Layers:
	-	`sha256:558301f9da2cc49044b0736894ccc3ad4a46787f9b8b19b2c7b8b44697f2c9cf`  
		Last Modified: Mon, 18 Dec 2023 19:58:07 GMT  
		Size: 3.4 MB (3437539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf517cea95f66d355dd94f0177c46455671e114e688d1a1549657b848bce639`  
		Last Modified: Mon, 18 Dec 2023 19:58:06 GMT  
		Size: 44.2 KB (44199 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.11.3`

```console
$ docker pull kibana@sha256:7566abb216186144689647539896afe581528a399ca7d7ae5a17f234fd09f3d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.11.3` - linux; amd64

```console
$ docker pull kibana@sha256:1d1ad24a560582d0426a5cfd2b33db395529e4b54e98fa2e15328b302d8ef407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368866244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb428a138a34448f6c06b73dec9605e2bf28bcb96b18a2caa6e63d13f63f925f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Dec 2023 13:07:20 GMT
ARG RELEASE
# Tue, 12 Dec 2023 13:07:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 13:07:20 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 13:07:20 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Dec 2023 13:07:20 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Dec 2023 13:07:20 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 13:07:20 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.label-schema.build-date=2023-12-08T16:30:01.542Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=cc11667953f4734af414e8d8977b8d9dda5698ef org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.11.3 org.opencontainers.image.created=2023-12-08T16:30:01.542Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=cc11667953f4734af414e8d8977b8d9dda5698ef org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.3
# Tue, 12 Dec 2023 13:07:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Dec 2023 13:07:20 GMT
USER kibana
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0418024c03fca4007ba56628d4865287339daf4d5a031d6d9cc18ef392ad9782`  
		Last Modified: Sat, 16 Dec 2023 10:51:18 GMT  
		Size: 10.5 MB (10530706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd32dcdeb4304dcea0936f74db19b409c175acf29c7948cee1701379a920b077`  
		Last Modified: Sat, 16 Dec 2023 10:51:17 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f07e394bd2569127212ef3b2c77ec52165b6cdd4d9ba795e7b3654c278d1ac`  
		Last Modified: Sat, 16 Dec 2023 10:51:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3684e3f2c49365477054bc85e8b6a9e08d214731878f0dee8f5565752fd013`  
		Last Modified: Sat, 16 Dec 2023 10:51:18 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ae62ea6ae8dd0e633c305cb494333c3e3ca942f5e119dd548b1d8608dde483`  
		Last Modified: Sat, 16 Dec 2023 10:51:18 GMT  
		Size: 5.3 KB (5271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620aa23185782526532da38038cfa0cecd7438fc409c2a7114d9d164aa2941a`  
		Last Modified: Sat, 16 Dec 2023 10:51:25 GMT  
		Size: 314.2 MB (314150581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2020c591cdc1beff764a315a566683da9e04b2d1610f4a1fd3ef3159bbe7b9ae`  
		Last Modified: Sat, 16 Dec 2023 10:51:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aa68441835d44bef3f98bd8d51626ac48f8fbcb21772f3a55fe5f7e6dda9bb`  
		Last Modified: Sat, 16 Dec 2023 10:51:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b0f8e814e135bd99f611e6d1fd91cc90150fe932b3f161b69af034472313a9`  
		Last Modified: Sat, 16 Dec 2023 10:51:19 GMT  
		Size: 4.6 KB (4552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c925bd65584abe120e9f52e8a90901899fc51439cbe0dd10f8ca96cafcbc2391`  
		Last Modified: Sat, 16 Dec 2023 10:51:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7890af4f0998bfa039806d4d7c6587a8c7ef7d3fdacb1a241db9fa11cd5bc7`  
		Last Modified: Sat, 16 Dec 2023 10:51:20 GMT  
		Size: 189.4 KB (189405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b389a78fe71b7f92663682af72cb1ad76956429069d43028358061b13a02f49c`  
		Last Modified: Sat, 16 Dec 2023 10:51:20 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.11.3` - unknown; unknown

```console
$ docker pull kibana@sha256:b5ea16f586cf1ff3c86d3dd7182eb19575f7cc0dd4538f0167ae59357fbb7a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a5ab9a390a91b55dff7f3adbc52bdf25430d43c328f4e50688c336f23e70fb`

```dockerfile
```

-	Layers:
	-	`sha256:8e6a55ce251526db717b98b6dc6ee818f5006af449ea7334d77b54c9c9096f94`  
		Last Modified: Sat, 16 Dec 2023 10:51:17 GMT  
		Size: 3.4 MB (3436123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53eef0fcc84072d11f4e461aad44e6dcbbd05073dbdc5fafc523aa4ecec0cb6`  
		Last Modified: Sat, 16 Dec 2023 10:51:17 GMT  
		Size: 44.4 KB (44356 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.11.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:f563d805062623c410cd8ff575f8f0aed8d9e17ac80a24119ccea3f73aca54de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379683317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4218885ae6cae45ee8b5004914638c903e042b57e3c03709e458f6bfbdc88`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Dec 2023 13:07:20 GMT
ARG RELEASE
# Tue, 12 Dec 2023 13:07:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 12 Dec 2023 13:07:20 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["/bin/bash"]
# Tue, 12 Dec 2023 13:07:20 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Dec 2023 13:07:20 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Dec 2023 13:07:20 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Dec 2023 13:07:20 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 13:07:20 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Dec 2023 13:07:20 GMT
LABEL org.label-schema.build-date=2023-12-08T16:30:01.542Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=cc11667953f4734af414e8d8977b8d9dda5698ef org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.11.3 org.opencontainers.image.created=2023-12-08T16:30:01.542Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=cc11667953f4734af414e8d8977b8d9dda5698ef org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.3
# Tue, 12 Dec 2023 13:07:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Dec 2023 13:07:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Dec 2023 13:07:20 GMT
USER kibana
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b33c1a27bbb4c31c43eb167ae3df748361fefa96bbfa0dec48c68a4c1e33ca1`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 10.4 MB (10396649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98059de69b424d043bad0fbc3aa68baae6367fabf5f63704de018bfe92e97239`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae0f05ad9a7ff1532ceaf39932fb0b9a88a8de625669867c4f1e74135770c4d`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c897b19d6be892715b84b17db2bce8870bb544cd8aaa14b5d69487582a2542`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 16.5 MB (16460497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e8ede858fed3dc2c66c8f0b11d0b7b977202fc35ee37a2c50784b2b716f601`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293183d89e8d29564418afa5dec4d0c1d7da720b0f182878e0615fa2c1995ca3`  
		Last Modified: Mon, 18 Dec 2023 19:57:46 GMT  
		Size: 326.6 MB (326646094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd0dedde44ab29410a464a520f3f8fb3cb16a7b3e0e1eefbc771d69aee1989`  
		Last Modified: Mon, 18 Dec 2023 19:57:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93a684cd6adf25c2d5097e2fffde88f232af9379181c1527062edfcf4681a0b`  
		Last Modified: Mon, 18 Dec 2023 19:57:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5f0e3c8d3a970dafd42fd5216c9474747d8e0ed39e77807cd10fbeadb0e391`  
		Last Modified: Mon, 18 Dec 2023 19:57:33 GMT  
		Size: 4.6 KB (4553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0d6fc5632046e728529047463a98d1e05a26ded1cc9e609df5c475529c5f6a`  
		Last Modified: Mon, 18 Dec 2023 19:57:34 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec71c63e4e93a26c161397366b453e569e598b46b8508c9fa90cdc32767563`  
		Last Modified: Mon, 18 Dec 2023 19:57:34 GMT  
		Size: 183.4 KB (183409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c1de9f1fe6e5d20b5e9c28405853d7ee601d0df74422de325b0be441b00942`  
		Last Modified: Mon, 18 Dec 2023 19:57:35 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.11.3` - unknown; unknown

```console
$ docker pull kibana@sha256:9afe40e98ff81e546901d947db252680b91a7bf7f247bbe3c4cc68103f8f5089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38b6243e7df804792bc7ff6cb6039fd698a6f12875791c093d553ca698d297f`

```dockerfile
```

-	Layers:
	-	`sha256:b743a09a7c719620fc991ed89af5da5cf955502fa6f1e35e6fc0052adbc2006d`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 3.4 MB (3436464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:831f325ad7246dea5293b1588587afb5fc85e2f6888846f03f2fa563bc485dcd`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 44.2 KB (44199 bytes)  
		MIME: application/vnd.in-toto+json
