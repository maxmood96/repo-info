<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.20`](#kibana71720)
-	[`kibana:8.13.0`](#kibana8130)

## `kibana:7.17.20`

```console
$ docker pull kibana@sha256:5769055ac4a396d43f9819aee002fdcc7d8830d5cf3062ca605f922100a2db87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.20` - linux; amd64

```console
$ docker pull kibana@sha256:ce6da794d6308a4fd3e243c009eb908a1e9d5fa0f1333cfd3a1c24c4f2dd1872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360565069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991143f55922404e284474926c59a0b3164c5dbe641b7c101bcc052ee53e29df`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN fc-cache -v # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/kibana
# Tue, 09 Apr 2024 08:24:48 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.build-date=2024-04-08T11:05:28.782Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=03253d4922979c94747a2f108370c00ad99df6d1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.20 org.opencontainers.image.created=2024-04-08T11:05:28.782Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=03253d4922979c94747a2f108370c00ad99df6d1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.20
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 09 Apr 2024 08:24:48 GMT
USER kibana
```

-	Layers:
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ca70d9a06f149f64aa7897bdfb51e9459dea15a8c1b007f85e558195e0647f`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 11.6 MB (11580838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77c1b6650f92cc71b6eacb401802a10759fdfb51471d788458b3255125dc786`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2a1ad44b2c94a2fc92f075f9d2901821664e5f98cf6b7721477d6397b4858c`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6951d00fb782b3dbd8a896caf9d3822c05fa2c6ed3fc98f72a5bba23b40d2acd`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c9420d44314b322e4dc9798f36daea84cb7b01a22468408bcbdd18055748a6`  
		Last Modified: Tue, 16 Apr 2024 04:26:54 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045e0c38010acd3ca9fb388f3408aa7a57dfb6036cb418d297fa7fdd6a76f594`  
		Last Modified: Tue, 16 Apr 2024 04:26:57 GMT  
		Size: 304.8 MB (304800212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d0db2b355eaabce0bcf181af1a27054504fd335df45abdb01abe8a288279d5`  
		Last Modified: Tue, 16 Apr 2024 04:26:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2687ff44196c3f3e7717b4787718af27d687a53d2de50c60fd98c4eaec5e0330`  
		Last Modified: Tue, 16 Apr 2024 04:26:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdadaf31762092ca5161250a7e50aebe1cce7f4fc81c1a87aa64bcfa07d9b18`  
		Last Modified: Tue, 16 Apr 2024 04:26:55 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4867cbfe45bd25e5076bc5e0040c61b8ebd031cb158290292e0114e26a0264`  
		Last Modified: Tue, 16 Apr 2024 04:26:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258a9654aca7392d8e8b72889f1bed3a448f2e08b13e21ecda4f545aaac323d6`  
		Last Modified: Tue, 16 Apr 2024 04:26:55 GMT  
		Size: 189.4 KB (189433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2eeb64cf73caaeee19af103e3de695247431e21907679193866df17f084924`  
		Last Modified: Tue, 16 Apr 2024 04:26:55 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.20` - unknown; unknown

```console
$ docker pull kibana@sha256:e76421cc82b3ae539b5cbc28b93bfc72ec4f23d6a8127e978e7a5fdfa4a9f349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3334265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac5b495e87b47c51e19ba7c404aaa407049304062b5a52b435822f145efbdd9`

```dockerfile
```

-	Layers:
	-	`sha256:672c66cc280f0e9d99ae0219311fbb34a432114698fd812399051980ca70aa72`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 3.3 MB (3289902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce4a9c6de2de008dc5e43c5fdbfaf7fcb3426f722c1fbc5bbdadba7c83fede8`  
		Last Modified: Tue, 16 Apr 2024 04:26:53 GMT  
		Size: 44.4 KB (44363 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.20` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:f44905602d1269b4364d6da6a61f88eded38af0ae3edc9ff2cb0a059f3bee938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369944795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b87c9a600ca8e021802abae5e06e55f12cb05e743e101a364e883cb70ee6e6a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN fc-cache -v # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/kibana
# Tue, 09 Apr 2024 08:24:48 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.build-date=2024-04-08T11:05:28.782Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=03253d4922979c94747a2f108370c00ad99df6d1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.20 org.opencontainers.image.created=2024-04-08T11:05:28.782Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=03253d4922979c94747a2f108370c00ad99df6d1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.20
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 09 Apr 2024 08:24:48 GMT
USER kibana
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f996b4573625d24d01984a19a4fbc3549230b9b88cb16a28419abf638dc28a7c`  
		Last Modified: Tue, 26 Mar 2024 19:02:10 GMT  
		Size: 10.4 MB (10396734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0cdce6d48fa7a32e359c918adeb38713806797f9c3ea633f26446660b123f6`  
		Last Modified: Tue, 26 Mar 2024 19:02:10 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b426958853de33e4305c56fe7ed2cf52f0a0d1858b2f73d7fc60e9a52ee28c`  
		Last Modified: Tue, 26 Mar 2024 19:02:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1c43c65e14dd2c61241503b8df1e3fff0476ca449d938947da7be5ac98be13`  
		Last Modified: Tue, 26 Mar 2024 19:02:10 GMT  
		Size: 16.5 MB (16460478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28686ecbbafc1644c10d33b11ca70ff6914226cd1cc97d451b69200b9a649377`  
		Last Modified: Tue, 26 Mar 2024 19:02:11 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31212b1b002fde92e7ece4c564a272d368091d7d7ba2410813777c726a3694df`  
		Last Modified: Tue, 09 Apr 2024 18:56:42 GMT  
		Size: 316.9 MB (316907906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5450ea7fa55e119ace7f722b8d71f0e654f19d5b3563b9bf08bf8f0ee8399d8a`  
		Last Modified: Tue, 09 Apr 2024 18:56:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b54eeaac9b562ca95283e58a0cdfda98ea5980047b74b4cbae7798134496598`  
		Last Modified: Tue, 09 Apr 2024 18:56:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5d8bd9f5678ffb20390b5e8b79ec37abb1e14de7459978f236b459d8f25067`  
		Last Modified: Tue, 09 Apr 2024 18:56:36 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0957dddbd5422f6990c7b9659433599d4545a8ca58174e5b4d780f1e04151`  
		Last Modified: Tue, 09 Apr 2024 18:56:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6db0af78670da9998bf582dc3c55f49cfb70b0d3933ad24821310721fbbb5a6`  
		Last Modified: Tue, 26 Mar 2024 19:02:13 GMT  
		Size: 183.4 KB (183424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48039c511a70b90c5226e0c1617ca648f716a62092e79b179638d62aa42c5336`  
		Last Modified: Tue, 09 Apr 2024 18:56:37 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.20` - unknown; unknown

```console
$ docker pull kibana@sha256:4910a5fa96164b13118b392383f310d7aa58cffb290de3ab44e17e2967a5e4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3334428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc5e1f879c5969005260485ec983fc261f515d3d3bd88a66f4fb92e37a9d9c7`

```dockerfile
```

-	Layers:
	-	`sha256:6e1e880740eedf5be8afce93dcc1e9dcd3a25aef442b4c5ed8c84f15efe40f8b`  
		Last Modified: Tue, 09 Apr 2024 18:56:36 GMT  
		Size: 3.3 MB (3290061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b074acf0dcd1487f1416da758a034da997023c3faf41bbd9b0c15d9119a11cf`  
		Last Modified: Tue, 09 Apr 2024 18:56:35 GMT  
		Size: 44.4 KB (44367 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.13.0`

```console
$ docker pull kibana@sha256:dbcb82bcce5fb83cb1d82663b0079adc9f79604616cf102cf16bd4b3a36a7a75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.13.0` - linux; amd64

```console
$ docker pull kibana@sha256:d49bb88a231b7bb7acf9dc92b915325480a428ddaeeb7f355f76b126dc2acde7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.9 MB (375929068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eea0db0a4b07327315fda2b327125aa5f9a9252c437602de5650a59420a921d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN fc-cache -v # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/kibana
# Tue, 26 Mar 2024 13:49:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T04:07:01.866Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T04:07:01.866Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5a3edb2abd7826997997d1309ee9753ef1a565c28ee79291dba4eede9b78c5`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 11.6 MB (11580885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58960dff290233a2836d157ff6f1b983101305e6d7982bff6e12b5834f9a56f7`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95e25456d28a79011c942ce50b2ccb944e03e3d69bf243ae1badbae95bdb2b8`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d883d1421fe9ceebaf897a17aa2b603e5c58d5ead4cb8f0ce05d9b7770f7c`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8a479d4ff521ad53ada831352f253a819d92165aa0351a0fbc6c5f62f0de83`  
		Last Modified: Tue, 16 Apr 2024 04:28:16 GMT  
		Size: 5.3 KB (5292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1874e163cf879e2403037506626abf5a7822d917459bf6cb1b24868899b8ee51`  
		Last Modified: Tue, 16 Apr 2024 04:28:20 GMT  
		Size: 320.2 MB (320164088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818464c02fe5350ac16cb2d8361cdd2dfc899c6f5bab6b1f9d86dda99642581d`  
		Last Modified: Tue, 16 Apr 2024 04:28:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a218d9d98aecfe34699161be1d56ca6f7a4e777e7443a06ae656822a79aaeba`  
		Last Modified: Tue, 16 Apr 2024 04:28:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ffa6ce416ba36cc665d6ffde3b7d46b4e81d1035446fa2b7f76c57d7f566aa`  
		Last Modified: Tue, 16 Apr 2024 04:28:17 GMT  
		Size: 4.6 KB (4563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d1e5de15cdaad966db7af0071e0256721cfdbf8c00cda0bf9ade3be26ef94e`  
		Last Modified: Tue, 16 Apr 2024 04:28:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876b6997c43ab71b120aebbf60609d7fc5c285d9fee48def60bddd31837759f0`  
		Last Modified: Tue, 16 Apr 2024 04:28:17 GMT  
		Size: 189.4 KB (189429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec46a661a3e774666f0c4e9ace78e8be9e6c85e655de883f0a1dc96767223f6`  
		Last Modified: Tue, 16 Apr 2024 04:28:18 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:8e9cd8741f34357b945237a0c5268814fa133fe2b3b6e83475c8e5ea7fb5e80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3793944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5291d7fcbfe5147b9f701fb62fc0ae6293074456b4a90ab68c6316914d40930`

```dockerfile
```

-	Layers:
	-	`sha256:4186065a74691cd194a93a16cda7067c0fe1626ca1126baa5aaa0f8aface2190`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 3.7 MB (3749593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7811e12a23aeeb3118cbd8137c8c273251ba69d8598938f00382830f11748d91`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 44.4 KB (44351 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.13.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:8b54942d4997c97cfc721357e6303ed96ed9fd674f71d7ce0bce41ebc9e6f749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 MB (385331334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0db7ebb4793ed4d8987c973cf9a281bafde8299a036b3a7493886d7924c789`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN fc-cache -v # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/kibana
# Tue, 26 Mar 2024 13:49:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T04:07:01.866Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T04:07:01.866Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f996b4573625d24d01984a19a4fbc3549230b9b88cb16a28419abf638dc28a7c`  
		Last Modified: Tue, 26 Mar 2024 19:02:10 GMT  
		Size: 10.4 MB (10396734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0cdce6d48fa7a32e359c918adeb38713806797f9c3ea633f26446660b123f6`  
		Last Modified: Tue, 26 Mar 2024 19:02:10 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b426958853de33e4305c56fe7ed2cf52f0a0d1858b2f73d7fc60e9a52ee28c`  
		Last Modified: Tue, 26 Mar 2024 19:02:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1c43c65e14dd2c61241503b8df1e3fff0476ca449d938947da7be5ac98be13`  
		Last Modified: Tue, 26 Mar 2024 19:02:10 GMT  
		Size: 16.5 MB (16460478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28686ecbbafc1644c10d33b11ca70ff6914226cd1cc97d451b69200b9a649377`  
		Last Modified: Tue, 26 Mar 2024 19:02:11 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794fdd1666c7ebcfdbfc2c1bb19ac394ace72eac8fea3dcda296f815b46453dd`  
		Last Modified: Tue, 26 Mar 2024 19:02:21 GMT  
		Size: 332.3 MB (332294382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ec837a6bcb6bb29c207eaf9cd73d861678e83afa19399f7add7618abee72b0`  
		Last Modified: Tue, 26 Mar 2024 19:02:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce5da19c23702b31f35ba8280bf3af7a0b5efa14818f4e47ad600ae29518d72`  
		Last Modified: Tue, 26 Mar 2024 19:02:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4e6984716cbc66249a512fc152e2839b9c02160940548ebbfa4e8dfe489697`  
		Last Modified: Tue, 26 Mar 2024 19:02:12 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2d2971571d8a891bdb613fa389b294c741a6ed62caca9b2ddfd0b605904fa`  
		Last Modified: Tue, 26 Mar 2024 19:02:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6db0af78670da9998bf582dc3c55f49cfb70b0d3933ad24821310721fbbb5a6`  
		Last Modified: Tue, 26 Mar 2024 19:02:13 GMT  
		Size: 183.4 KB (183424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75af7fb69941467a81cb6bf0e7bf8a68473dcca41ef2049dbeb23420463f824e`  
		Last Modified: Tue, 26 Mar 2024 19:02:13 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:3aafd2613ed1c77c0764c330899dfd15bce88d905a9adea85bb6cc2d7b1bd96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3793947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb57493acb433734a75f05edfabf4796a7b3af11b7d1f2e518d4e1906c472d8`

```dockerfile
```

-	Layers:
	-	`sha256:7b236e20ef5c4eacb64f519c0da4ee365cb94526670bdbfb4c02bac818f3537f`  
		Last Modified: Tue, 26 Mar 2024 19:02:10 GMT  
		Size: 3.7 MB (3749752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc95e07c3dfd0222704527f8e1af71e7ed5a2654942aabd58bd0a1398e345e5d`  
		Last Modified: Tue, 26 Mar 2024 19:02:09 GMT  
		Size: 44.2 KB (44195 bytes)  
		MIME: application/vnd.in-toto+json
