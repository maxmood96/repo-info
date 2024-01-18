<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.16`](#kibana71716)
-	[`kibana:8.11.4`](#kibana8114)

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

## `kibana:8.11.4`

```console
$ docker pull kibana@sha256:e8343544e5fd84a825bdb701e3a61f292f1850f634e1000a6ae1714b60d0fcd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.11.4` - linux; amd64

```console
$ docker pull kibana@sha256:bee82991bff3fda023ca0eb67d81f360f8080ec26c8f6e66dc5b599c398923a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369251752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabe686256c3ba558a7ec49e3e88181b7f0ed7c25c11fdf03bfa251bca22b372`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Thu, 11 Jan 2024 09:47:01 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 11 Jan 2024 09:47:01 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN fc-cache -v # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
WORKDIR /usr/share/kibana
# Thu, 11 Jan 2024 09:47:01 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jan 2024 09:47:01 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
LABEL org.label-schema.build-date=2024-01-08T03:01:07.195Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4e90188951eb2dce4f4a0d45ba1a0b9ae9efe19d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.11.4 org.opencontainers.image.created=2024-01-08T03:01:07.195Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4e90188951eb2dce4f4a0d45ba1a0b9ae9efe19d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.4
# Thu, 11 Jan 2024 09:47:01 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 11 Jan 2024 09:47:01 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 11 Jan 2024 09:47:01 GMT
USER kibana
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a30ad03f8d1d3a11299aac0e8029a67655e6ce7fc59bd4a883f867eaba09929`  
		Last Modified: Wed, 17 Jan 2024 22:45:59 GMT  
		Size: 10.9 MB (10914374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c0dbc29fdfa76889e4095be8b3f6f93c78bb6623532110cce5324cfcd10754`  
		Last Modified: Wed, 17 Jan 2024 22:45:58 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e230da9fd1916515902c31d427665195d616f5410e5d11ea0e2984231ecbbef`  
		Last Modified: Wed, 17 Jan 2024 22:45:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1018f2d9e110592ae28f0fed68883483fd07cdec68335428807d6f1889f5513a`  
		Last Modified: Wed, 17 Jan 2024 22:45:58 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943ff029538cba290d1435620e4ccda2314a27b1c3f0f46824a7fb1c5e7d7aac`  
		Last Modified: Wed, 17 Jan 2024 22:45:59 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af61bf19a41c3165f2c4d9f2cf473b8b4ba44f8aa04be1e3d44da767389108b6`  
		Last Modified: Wed, 17 Jan 2024 22:46:05 GMT  
		Size: 314.2 MB (314152405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210010c5e1605ec85c808a563f0e83f6c480a6984de36729980af8578a534084`  
		Last Modified: Wed, 17 Jan 2024 22:46:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c003f432a76d2a1578c0f23892a18cc581d5ad48a7c252ff099d2545f956d9a`  
		Last Modified: Wed, 17 Jan 2024 22:46:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d577e2a0cb661e984b4ea96ee341b7422e0587066654169effcd1e389e129b`  
		Last Modified: Wed, 17 Jan 2024 22:46:00 GMT  
		Size: 4.6 KB (4555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2bcae9b4033d6cd427010a84736390bb5387ae937de82c6f508810749e362d`  
		Last Modified: Wed, 17 Jan 2024 22:46:01 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b90a9d3ec8fc63b15ea2699b2a415f57e13d736625ffa94b9a3b58d0cbac09`  
		Last Modified: Wed, 17 Jan 2024 22:46:01 GMT  
		Size: 189.4 KB (189405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414a15d417aa835c42e0cd7c216b1d74845d8545b1941b0186bd8a7ededa1a7`  
		Last Modified: Wed, 17 Jan 2024 22:46:01 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.11.4` - unknown; unknown

```console
$ docker pull kibana@sha256:01222b55a8af2a5837386442f59d4e7bc542a9384f0df6c0aad2421bd1f77e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0ed3d91156243b5b6fc8bab2967af7a406e0ce33a75ea8f00b5261b792a008`

```dockerfile
```

-	Layers:
	-	`sha256:1545701aa3db037c2af9a24ee74111b8d67493da146269470d8cb754d48f4ec4`  
		Last Modified: Wed, 17 Jan 2024 22:45:58 GMT  
		Size: 3.4 MB (3436123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42f3fdc0622b95d9577c9c322f812f5e4f85ce5433d055a7974733b168a0683`  
		Last Modified: Wed, 17 Jan 2024 22:45:58 GMT  
		Size: 44.4 KB (44356 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.11.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:714ade86a7788d952abd3f129f268a682f2c2da87b1f200510ff37e14d699021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379680623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de34f4670baa83640d3f07d267d79dc557b94605c6f14c23eff9b3d5c58e854`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Jan 2024 09:47:01 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 11 Jan 2024 09:47:01 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN fc-cache -v # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
WORKDIR /usr/share/kibana
# Thu, 11 Jan 2024 09:47:01 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jan 2024 09:47:01 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 09:47:01 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 11 Jan 2024 09:47:01 GMT
LABEL org.label-schema.build-date=2024-01-08T03:01:07.195Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4e90188951eb2dce4f4a0d45ba1a0b9ae9efe19d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.11.4 org.opencontainers.image.created=2024-01-08T03:01:07.195Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4e90188951eb2dce4f4a0d45ba1a0b9ae9efe19d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.4
# Thu, 11 Jan 2024 09:47:01 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 11 Jan 2024 09:47:01 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 11 Jan 2024 09:47:01 GMT
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
	-	`sha256:fc0518eab78c875dac7143b94a346c52c3acae77c23b83cb89e839fcce49a2af`  
		Last Modified: Thu, 18 Jan 2024 10:32:20 GMT  
		Size: 326.6 MB (326643393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433ce7eca1045a6f5448877319e86390d32673e0171c62a3194e8b513430bfc1`  
		Last Modified: Thu, 18 Jan 2024 10:32:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56dad308720c4afa377aefd79600bfaa7d2053e5f54478e132177fd36c55a65`  
		Last Modified: Thu, 18 Jan 2024 10:32:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876e628cf00246329b4ece9df804549464aa7201503a373b531199cc778474f5`  
		Last Modified: Thu, 18 Jan 2024 10:32:12 GMT  
		Size: 4.6 KB (4555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c43ddac69c9af815178f2197008668968ecac8c370468f2fc35fe334f52b6f`  
		Last Modified: Thu, 18 Jan 2024 10:32:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec71c63e4e93a26c161397366b453e569e598b46b8508c9fa90cdc32767563`  
		Last Modified: Mon, 18 Dec 2023 19:57:34 GMT  
		Size: 183.4 KB (183409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80ee00ef3a069c21d1dab1b188d2467de7459d635727c875c5908a6eb3e6abc`  
		Last Modified: Thu, 18 Jan 2024 10:32:13 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.11.4` - unknown; unknown

```console
$ docker pull kibana@sha256:99baaed2f0b95b29e983a78829b9a6412249d22d0a3c5d2d1422cff15b9fabb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776048d8374de13059c39965c263cff89885a0b24cadbd977f1933ad76d60d8e`

```dockerfile
```

-	Layers:
	-	`sha256:192d996e70a26ad65e939635c1416bc4bc60ee8214bb5b084d25f5598fab0e0e`  
		Last Modified: Thu, 18 Jan 2024 10:32:12 GMT  
		Size: 3.4 MB (3436464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f89c5d7690206e133caf126da14414b7bfe158af7f9bc51bff8fc3bcb1f74`  
		Last Modified: Thu, 18 Jan 2024 10:32:11 GMT  
		Size: 44.4 KB (44360 bytes)  
		MIME: application/vnd.in-toto+json
