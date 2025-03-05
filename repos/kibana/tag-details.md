<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.16.5`](#kibana8165)
-	[`kibana:8.17.3`](#kibana8173)

## `kibana:7.17.28`

```console
$ docker pull kibana@sha256:3cb1bea00e07e70d7b375cee840a9e71eb4ada9c4fac0725bfbbc01b3700ce8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.28` - linux; amd64

```console
$ docker pull kibana@sha256:d9322b59f3975a18a97887071a99946c37fdf3b89bd0a687924dcd4fdb8aaa77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.9 MB (356899770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f137710f620a39cc89a1e77514d7b6650927b1cf85907be47494974939d2a66`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 25 Feb 2025 11:58:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 25 Feb 2025 11:58:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN fc-cache -v # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
WORKDIR /usr/share/kibana
# Tue, 25 Feb 2025 11:58:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Feb 2025 11:58:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.label-schema.build-date=2025-02-19T12:12:43.403Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=e13d3db4d0479be06aa5447d35797f750b8121f3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.28 org.opencontainers.image.created=2025-02-19T12:12:43.403Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=e13d3db4d0479be06aa5447d35797f750b8121f3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.28
# Tue, 25 Feb 2025 11:58:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 25 Feb 2025 11:58:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 25 Feb 2025 11:58:14 GMT
USER kibana
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607b0dd8ab6b75c4a742eafb081571755886fb0e4012fb8ce73ba589172a1010`  
		Last Modified: Tue, 25 Feb 2025 18:30:50 GMT  
		Size: 18.2 MB (18223135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08d7cc0d73baedbe2e534346f984f88830c99a65d95cf283ab602af912bcdbf`  
		Last Modified: Tue, 25 Feb 2025 18:30:49 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be5454f317b8c10fc49b8d72673447d08d606be654f58ebcd2f26998e052a8`  
		Last Modified: Tue, 25 Feb 2025 18:30:49 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0980088f2c2cddfb0da1b38fff13cb1ba2754ffe07db51a0e2675317fced086`  
		Last Modified: Tue, 25 Feb 2025 18:30:50 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d39e3749b155a63c0a4ffaf326203573d843457100cb7c65ce66933db6c786`  
		Last Modified: Tue, 25 Feb 2025 18:30:50 GMT  
		Size: 5.3 KB (5280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c8a9856590e1126a7c83e2d8f2af6c9e24e0e85cc7e60f54f07134ab24ca3a`  
		Last Modified: Tue, 25 Feb 2025 18:30:54 GMT  
		Size: 294.5 MB (294493406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce579006d31622ad02157c3253b6eb2c6b3f820b563ec7aa23fd5cc7e395d8ae`  
		Last Modified: Tue, 25 Feb 2025 18:30:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef6bf630c03adb061f518e7df105636c23ecdf89c9314a042f301b95ec3448a`  
		Last Modified: Tue, 25 Feb 2025 18:30:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d29bd6f89838d3c12aec56f724ae0b1a34e26776f8284a14f1397f7957a5a3`  
		Last Modified: Tue, 25 Feb 2025 18:30:51 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca83f0e3cfd75d4deb4b30f8f663a07c3c3156466f5bbfee53a5043e4c40f89`  
		Last Modified: Tue, 25 Feb 2025 18:30:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b3f27f9928b8584da4f4b7d6d7411a1f1beb168a626e5701eef21dd9bd7309`  
		Last Modified: Tue, 25 Feb 2025 18:30:52 GMT  
		Size: 189.4 KB (189433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b989c9c2cf1811d314d0b1addc31926d5997bf6c27b1747aaacfb62dbc06765e`  
		Last Modified: Tue, 25 Feb 2025 18:30:52 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:0aa93301134c3ca470bdcf258ce625c075b64b97cb6624cfe801491031f0a121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3439198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a30b585f059a0e53b44ec92476cf02482f886b49378603a5fb29fcf9a242f5`

```dockerfile
```

-	Layers:
	-	`sha256:6b342596150f0cad36ac5dff1f2b6f61d8c7c0267c89ed255d7a193031c2b026`  
		Last Modified: Tue, 25 Feb 2025 18:30:50 GMT  
		Size: 3.4 MB (3394689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b29e4c3aa86a847afb7c8ba23c924d39b0bc454dea8ad58ef1f7a08abc7ced2`  
		Last Modified: Tue, 25 Feb 2025 18:30:49 GMT  
		Size: 44.5 KB (44509 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.28` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:b0c0c07d5dbc232fa1d540e933e860492ae46d921205a63c2ac307ec85168117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366651561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2fb0884aa6f011c282c9a971465db43775a701a27de68533e07cd491678a79`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 25 Feb 2025 11:58:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 25 Feb 2025 11:58:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN fc-cache -v # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
WORKDIR /usr/share/kibana
# Tue, 25 Feb 2025 11:58:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Feb 2025 11:58:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.label-schema.build-date=2025-02-19T12:12:43.403Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=e13d3db4d0479be06aa5447d35797f750b8121f3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.28 org.opencontainers.image.created=2025-02-19T12:12:43.403Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=e13d3db4d0479be06aa5447d35797f750b8121f3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.28
# Tue, 25 Feb 2025 11:58:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 25 Feb 2025 11:58:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 25 Feb 2025 11:58:14 GMT
USER kibana
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e7a5d7c8f6307b7711172e22b51ea45e4f9c6709e38655eb7dab38b7554e5`  
		Last Modified: Tue, 25 Feb 2025 23:53:26 GMT  
		Size: 17.0 MB (16977179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372f15406327e6880fb0125a096105b7498e6ca52d9ed07a8a5484ea4af95e0d`  
		Last Modified: Tue, 25 Feb 2025 23:53:25 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae58aa26445ec2def2e88e0413120d19b2b3d74e5846be0e399beb2f0423b352`  
		Last Modified: Tue, 25 Feb 2025 23:53:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c33abba5b50e698b7cc62b20f297daa442ad21576529dfa4fbb82d8f1e5841f`  
		Last Modified: Tue, 25 Feb 2025 23:53:26 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f87c01f93c9c3f7a7f488a52f5c84ca70ed3866cf9997cf054db53d3ab6f3`  
		Last Modified: Tue, 25 Feb 2025 23:53:26 GMT  
		Size: 5.3 KB (5295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fead8428e7a97912ff38b8740e60e3e6514ce0333b4df5d5dc1bc8a2873aa596`  
		Last Modified: Tue, 25 Feb 2025 23:53:41 GMT  
		Size: 307.0 MB (307034812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7630845431633d057caf2100abf7351a375ab46a4a37f6319e8b5e3840e1be21`  
		Last Modified: Tue, 25 Feb 2025 23:53:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b5be7df5423193d637accadc8088cf98cbae38da8237c2e06411aa65dbb1bd`  
		Last Modified: Tue, 25 Feb 2025 23:53:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0676e5fe1edd8957856aa6e890997215902c0cd3b908a3bb5635379c00fc6a8c`  
		Last Modified: Tue, 25 Feb 2025 23:53:27 GMT  
		Size: 4.5 KB (4500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2421a0733178f5d65e1e85c8611e34e172995196202071cd72fc553878da3b41`  
		Last Modified: Tue, 25 Feb 2025 23:53:28 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a7a6373a66421f75b6974db688e7cfab3b8b0fefdea6a283b6bd0e649d36e`  
		Last Modified: Tue, 25 Feb 2025 23:53:28 GMT  
		Size: 183.4 KB (183416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e9199b92dafe9da1d52a02fb0df804d1a907d4333365010d7bb4d4be582d31`  
		Last Modified: Tue, 25 Feb 2025 23:53:28 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:a1571c500bce002189eeb0344d25deb26f29428b1e4c58caff2e28906aae2981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3439727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298595780a1b66bdcc18b83072b1db57556ce5a33ca9363bf7b5df94fc987af0`

```dockerfile
```

-	Layers:
	-	`sha256:803cde63e7907dc30e6fa27bb16de74b5f38a00cece0015d0a3091861a9a7794`  
		Last Modified: Tue, 25 Feb 2025 23:53:25 GMT  
		Size: 3.4 MB (3394940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba153d69c988eb8e15f07725b7fb7ad798805b6439e5b2a213250c3d7c19b642`  
		Last Modified: Tue, 25 Feb 2025 23:53:25 GMT  
		Size: 44.8 KB (44787 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.16.5`

```console
$ docker pull kibana@sha256:96bb6189786c7ec27898f7e9d53bf6ce4961ab6a022ffd9d0ce8789be8a7460a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.16.5` - linux; amd64

```console
$ docker pull kibana@sha256:abac4209458844385abbd4bc82dc4d5d258792cb43e2cd5971b7f41be1fb1e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.2 MB (402169839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a914ef07c83d2b228f975dfdff712800aa26f28f1c864caa425d24c32472e1b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 04 Mar 2025 09:16:27 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 04 Mar 2025 09:16:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN fc-cache -v # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
WORKDIR /usr/share/kibana
# Tue, 04 Mar 2025 09:16:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:16:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
LABEL org.label-schema.build-date=2025-02-27T12:15:01.858Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=edec21f4bf4e4069a9ff684197348d18a3bc9a69 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.5 org.opencontainers.image.created=2025-02-27T12:15:01.858Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=edec21f4bf4e4069a9ff684197348d18a3bc9a69 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.5
# Tue, 04 Mar 2025 09:16:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 04 Mar 2025 09:16:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 04 Mar 2025 09:16:27 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a0e478c529cb0e4ae12864abdab424590cb09a386089296153c948d5030bb`  
		Last Modified: Tue, 04 Mar 2025 22:00:29 GMT  
		Size: 18.2 MB (18223214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23b0dbcdcf72d2f6c3ba5c38dcbf7232f2a048b9e2e47de2421dc430b9d0cbb`  
		Last Modified: Tue, 04 Mar 2025 22:00:34 GMT  
		Size: 339.8 MB (339763373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381f8f2efdb6dad853c42a957778f78790d16f289986ecfb9cb60ac88087b65a`  
		Last Modified: Tue, 04 Mar 2025 22:00:29 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83b6c094f3bef035299b3db08c266392c979a90e4e9aa3d6e45d79b1ad49ff2`  
		Last Modified: Tue, 04 Mar 2025 22:00:30 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7be111df559c2a00c5bae5b5d049e3043f682e57d70b987361749076522d229`  
		Last Modified: Tue, 04 Mar 2025 22:00:30 GMT  
		Size: 5.3 KB (5274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0456734a2d8458fcaaf8eca54da3c58f6e3a89d8806362702ce7932839fe26c`  
		Last Modified: Tue, 04 Mar 2025 22:00:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b67ff0d28fcd0afeba29b0eb8a40ac81c8d0433ad172b2be0123db86029a900`  
		Last Modified: Tue, 04 Mar 2025 22:00:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6893d9a737b6e05657930f3dcc30f6cf9f1ddecdc7cadfd6a45814fc21ef73`  
		Last Modified: Tue, 04 Mar 2025 22:00:31 GMT  
		Size: 4.7 KB (4709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d1b7045dd5c2ff90786d62bf914c5d8a2383db68a76143b275873484bc124e`  
		Last Modified: Tue, 04 Mar 2025 22:00:31 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90191f520c5aa0ca013cb5909ac7dd88659e8c985959bd300b45aa23f578d17`  
		Last Modified: Tue, 04 Mar 2025 22:00:32 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb152c98fd0301ae7161b6968b22cf9c1676a61a3b8eaa65802d24a7655f432`  
		Last Modified: Tue, 04 Mar 2025 22:00:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.5` - unknown; unknown

```console
$ docker pull kibana@sha256:a37c178e0ee10df43b63ee491721f3824f70e4ab2a7e60c217bb17b66263fe2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4341780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317e77b6e3c0b835d025066d4e7050cb22bcebc66bec49d0f5b7a3e6d890e176`

```dockerfile
```

-	Layers:
	-	`sha256:9e508255c2bac6ffba561ade6b74acb6b6385c47bc9f09faafeb9eed70ce74b5`  
		Last Modified: Tue, 04 Mar 2025 22:00:29 GMT  
		Size: 4.3 MB (4301100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe41063e9722245c28c12345bc19906c5b4eb34eb9ab897c3192e8a4d515ab8b`  
		Last Modified: Tue, 04 Mar 2025 22:00:29 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.16.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:5bebe49d34df5dd7750e370a20a4518b62ff61298da0fd79bb33edb29cfa6f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411922802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e548c6faf7003d969866ed3c597b4a5843e1f5a8ace160f98870c393eea89e0d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 04 Mar 2025 09:16:27 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 04 Mar 2025 09:16:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN fc-cache -v # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
WORKDIR /usr/share/kibana
# Tue, 04 Mar 2025 09:16:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:16:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
LABEL org.label-schema.build-date=2025-02-27T12:15:01.858Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=edec21f4bf4e4069a9ff684197348d18a3bc9a69 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.5 org.opencontainers.image.created=2025-02-27T12:15:01.858Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=edec21f4bf4e4069a9ff684197348d18a3bc9a69 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.5
# Tue, 04 Mar 2025 09:16:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 04 Mar 2025 09:16:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 04 Mar 2025 09:16:27 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0281bae7ea0a80b15a4a14fbd592a574ce537a44208c5a88b277ecec158814d9`  
		Last Modified: Tue, 04 Mar 2025 22:37:01 GMT  
		Size: 17.0 MB (16977400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f180b87c7525e3e38bb7dcd77fb6d755f13f59468f34d4f894edf44f6b4102`  
		Last Modified: Tue, 04 Mar 2025 22:37:08 GMT  
		Size: 352.3 MB (352305815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c802c071e40383c3036aa16bd1ac428948e88c7ec3e4c2862b8356f89e043cee`  
		Last Modified: Tue, 04 Mar 2025 22:37:01 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec3bdc59d9d42c1b8084973a0a4ce2a30c88ae6c475287e96d859498406daf4`  
		Last Modified: Tue, 04 Mar 2025 22:37:02 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a06be0e7a8563b35426d3a98c3d61d788068623163393d6c245e49f2fb5c070`  
		Last Modified: Tue, 04 Mar 2025 22:37:02 GMT  
		Size: 5.3 KB (5285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e205be285e6e2469096a85e6bca6cebe1c69b34812b91830ace415dadd93f`  
		Last Modified: Tue, 04 Mar 2025 22:37:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8f448ebaeba4cb1aca3a65cf4264961443e5f507210073acfe354ab43fb607`  
		Last Modified: Tue, 04 Mar 2025 22:37:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e3105cd746019f6306cfb7d820a836270c5c69afa295d4051fb8ce4a43e1eb`  
		Last Modified: Tue, 04 Mar 2025 22:37:03 GMT  
		Size: 4.7 KB (4710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dcd14d9e58f3b7702acb1ff6e313f508996cdf97f2b4c17b9bc67a282de2dd`  
		Last Modified: Tue, 04 Mar 2025 22:37:04 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22ac5d3be665fb368c2b164a71567a6ccb43de323f65a04524fa5886d3f4d21`  
		Last Modified: Tue, 04 Mar 2025 22:37:04 GMT  
		Size: 183.4 KB (183419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c84d44939bd54848bffd7354fc4d330bf5812d766468c146543e45c468b60f8`  
		Last Modified: Tue, 04 Mar 2025 22:37:04 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.5` - unknown; unknown

```console
$ docker pull kibana@sha256:76a825e07a20b473c43fc1218ddfb5174aa490973b22e3472299d5634be79567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4342278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8051a2b9e3757076280ea4930df6475ca126496ca0401aff18d0e383c31c5ddc`

```dockerfile
```

-	Layers:
	-	`sha256:d5179c2b1207472688f9c77c6efb0e7a23a8a124fde409516b7eaceaa2252782`  
		Last Modified: Tue, 04 Mar 2025 22:37:01 GMT  
		Size: 4.3 MB (4301351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12022062a06d97203b88eefa4f909a1d26e3d2ed5c9e993fd88d8cb8ad3c2c0`  
		Last Modified: Tue, 04 Mar 2025 22:37:01 GMT  
		Size: 40.9 KB (40927 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.3`

```console
$ docker pull kibana@sha256:1235eb45cbdf45df2c260b9be98c469f5762e9417d9d7282f97986532efae3ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.3` - linux; amd64

```console
$ docker pull kibana@sha256:4aa8251c86f812dd2f4d0d5c5a3bb23e2ee1ec0cef33f7d14cb6b0ba89d70f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403576946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dcda0c152aad17ed3700386aea80e9aecb7b3658f4f7dbeed9c411232826b6a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 04 Mar 2025 09:12:50 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 04 Mar 2025 09:12:50 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN fc-cache -v # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
WORKDIR /usr/share/kibana
# Tue, 04 Mar 2025 09:12:50 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:12:50 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
LABEL org.label-schema.build-date=2025-02-28T12:10:01.332Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=faabb4e47ac99b6f367713ef845613b7313914b8 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.3 org.opencontainers.image.created=2025-02-28T12:10:01.332Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=faabb4e47ac99b6f367713ef845613b7313914b8 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.3
# Tue, 04 Mar 2025 09:12:50 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 04 Mar 2025 09:12:50 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 04 Mar 2025 09:12:50 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd85e47cd40eb9df6340fc8554ec98bb86a8184f95b78a2b96b3ec918bd0c7b`  
		Last Modified: Tue, 04 Mar 2025 22:00:34 GMT  
		Size: 18.2 MB (18223232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25df872f0fb2c6321d89624abcc2cecbca616125289942d3e8d1ba6379bf927`  
		Last Modified: Tue, 04 Mar 2025 22:00:39 GMT  
		Size: 341.2 MB (341170431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a519ff417d63ef2b17f5b3bb0c03d1a6df3d231e9c4ddbbc0a6889a058272f8`  
		Last Modified: Tue, 04 Mar 2025 22:00:34 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761d3de8f2e28d727cc858eea05d8d07c68df4b851412da815ba96c0c45debe8`  
		Last Modified: Tue, 04 Mar 2025 22:00:34 GMT  
		Size: 16.5 MB (16460497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d03dc3cde2e16e2d1d31ab08e499178130a8aea18da4c1aa3eaa2fab722ad4`  
		Last Modified: Tue, 04 Mar 2025 22:00:34 GMT  
		Size: 5.3 KB (5281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14ee621947a1af97860321fd302d779fd964c778ba07f0337f6f1e14bdd94fe`  
		Last Modified: Tue, 04 Mar 2025 22:00:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c240f24b139fb5eebcf15d3c64d61d42f3d169514a700b4c6f5e3b89a8587b1d`  
		Last Modified: Tue, 04 Mar 2025 22:00:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4c6026801ec4ca558797d6fe84d18a2523fd1e3c448e05733cb9c320d537`  
		Last Modified: Tue, 04 Mar 2025 22:00:35 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a862b8bd1310aba8332f29c59ffac5a67d9a46a02610265dd51abbc3c19c440`  
		Last Modified: Tue, 04 Mar 2025 22:00:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f7fa2d4f466d57798e40ab3790f62e8c4c6428e9f1ee96c9740c06cd14fb1`  
		Last Modified: Tue, 04 Mar 2025 22:00:36 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d5dcb1ed91485e307c7e3ac7e61ba7c38601b2e761fa3c7a6e215f4a905355`  
		Last Modified: Tue, 04 Mar 2025 22:00:36 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.3` - unknown; unknown

```console
$ docker pull kibana@sha256:aea09540fc35cb265bde7db5e71a00455fb25ce6087e7be88cd209b26991bb58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4436460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88174f4347e34ee97f55621694b0c31fd0503b155a2ab4b12d00eb0eee06e316`

```dockerfile
```

-	Layers:
	-	`sha256:c5d36b32a22a2bed91e0e90e0d8bd30ebe68fcff3a2f41841ecf0fc03e9c0afe`  
		Last Modified: Tue, 04 Mar 2025 22:00:34 GMT  
		Size: 4.4 MB (4395780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e33f5bd13a0131617fd2c38d1a716e8c9d6d28824403bc897e0837a84a4c49c4`  
		Last Modified: Tue, 04 Mar 2025 22:00:34 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:15c5147e77284cdb8970ab0efa825a2b26ce438495d94070da3f2c9fdf14fb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.3 MB (413329054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3940fdd618cfe4131e68fb1d3189f0eee4fbfe747898bc5fe71618378bc07aa1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 04 Mar 2025 09:12:50 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 04 Mar 2025 09:12:50 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN fc-cache -v # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
WORKDIR /usr/share/kibana
# Tue, 04 Mar 2025 09:12:50 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:12:50 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
LABEL org.label-schema.build-date=2025-02-28T12:10:01.332Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=faabb4e47ac99b6f367713ef845613b7313914b8 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.3 org.opencontainers.image.created=2025-02-28T12:10:01.332Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=faabb4e47ac99b6f367713ef845613b7313914b8 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.3
# Tue, 04 Mar 2025 09:12:50 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 04 Mar 2025 09:12:50 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 04 Mar 2025 09:12:50 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0281bae7ea0a80b15a4a14fbd592a574ce537a44208c5a88b277ecec158814d9`  
		Last Modified: Tue, 04 Mar 2025 22:37:01 GMT  
		Size: 17.0 MB (16977400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edfda84c37466ea57c9371d1fb115249e1e64f9fa00e7eb3f56ebe8a58b17fd`  
		Last Modified: Tue, 04 Mar 2025 22:46:27 GMT  
		Size: 353.7 MB (353712053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0ad56a36e78b1eed72a4602693b10478ad7cbd505a616bd5ab0e94d80a94f`  
		Last Modified: Tue, 04 Mar 2025 22:46:20 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5da85babef89d9535e10178db7f2922bf52f40dacb851e2b6dde89677cdb4b`  
		Last Modified: Tue, 04 Mar 2025 22:46:21 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b54eaa0256ede1e186d114e1fd94564904071fbba32299c6da0361f765820`  
		Last Modified: Tue, 04 Mar 2025 22:46:20 GMT  
		Size: 5.3 KB (5284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70cee9f0f47f6fbc5367acd513ec145b36ac1dfe8c62d8c5f63c3c125197f60`  
		Last Modified: Tue, 04 Mar 2025 22:46:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a461f8bcbcb85461b7339df08c6f9c11da0c38970dd000f6a2a3bb029889c394`  
		Last Modified: Tue, 04 Mar 2025 22:46:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79d9eff221909f8823363912f9de19f17f04d4ce5c78689ba7c35ccf0bfd7e2`  
		Last Modified: Tue, 04 Mar 2025 22:46:22 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68edaf6ba01bd66b6d098822b4fcfe13b715e42b608ee0c29699133162a7801`  
		Last Modified: Tue, 04 Mar 2025 22:46:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f0d0f73600c8b54f6998afb969685aff0b70559f5e74c7f97c8f972fe92566`  
		Last Modified: Tue, 04 Mar 2025 22:46:22 GMT  
		Size: 183.4 KB (183419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46ba27d7a6c973bcdc22ad999a0f0c3def0263f6c6029c1c57d7df05555194f`  
		Last Modified: Tue, 04 Mar 2025 22:46:23 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.3` - unknown; unknown

```console
$ docker pull kibana@sha256:9934da1304111f9df22d712d9dec66565e4c549dd4dedbd1082d4e7f626ee65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4436958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8ea522f3b40bb2d5555797d9fd9846fdc392208ab1a23ce0717868a57c3d4d`

```dockerfile
```

-	Layers:
	-	`sha256:d3f7600383e9e1a5dcd6dedd66f601f1a04a133d5c41d852b4244ec415eea576`  
		Last Modified: Tue, 04 Mar 2025 22:46:20 GMT  
		Size: 4.4 MB (4396031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec2dc5740e0ed4f97cce20921a7137f3f6778673e5acf487c21058f99f9856b`  
		Last Modified: Tue, 04 Mar 2025 22:46:20 GMT  
		Size: 40.9 KB (40927 bytes)  
		MIME: application/vnd.in-toto+json
