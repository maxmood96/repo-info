<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.16.6`](#kibana8166)
-	[`kibana:8.17.4`](#kibana8174)

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

## `kibana:8.16.6`

```console
$ docker pull kibana@sha256:099060d7188ce4a63d52a1d43899ceb9bd24bfec6d0855390b1e69bbfdc6115e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.16.6` - linux; amd64

```console
$ docker pull kibana@sha256:2406ff5744bf6c325ea8fba43efccad60a04acf0a3723a5fe5ff3fd8a1e71e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.9 MB (394888396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e6460efc17db008e5a56c40c83d97219e7d5c7ae57fd8c1937bbe6ec3ac4d7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 25 Mar 2025 08:54:09 GMT
ARG RELEASE
# Tue, 25 Mar 2025 08:54:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Mar 2025 08:54:09 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN fc-cache -v # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/kibana
# Tue, 25 Mar 2025 08:54:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.build-date=2025-03-20T11:10:41.087Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=39969cb4b1ab957faf1e78d25d83ec04192ddc21 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.6 org.opencontainers.image.created=2025-03-20T11:10:41.087Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=39969cb4b1ab957faf1e78d25d83ec04192ddc21 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.6
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5fcb54725bcc66217a044cabc67d309ebc07f5b3761242820db1729aaf9042`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 10.7 MB (10725848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7b2843daed8653e710921c3a089135c76ea6f3e40689e5aa786f35cd36ff7`  
		Last Modified: Wed, 09 Apr 2025 01:21:24 GMT  
		Size: 340.0 MB (339979976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f95bbe0763949f2a3f2cc2727ffb5d76e58e1f83468bbc8de1485a2b7402bb`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2fcb034d141c8e4162a1069df0f0bf7d78126eb8f372352fb0128edcbc9ef`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455ee5029c3a8be9f9db1ab09fc134eebdc08417c20b4bd142fc8b8e5f6cd880`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 5.3 KB (5275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0352cd7e09a3cdbc495fcf8a9ea1f97d25d45ca1716ff9085256a4dfc18ab4`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7fdfa04504f5dac47ff0bbd9aec62b5f1ca140c98112accc1003042c1d4750`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ca14aa0bdd02b1bee1c16ee35274fcdcd449f59c69a7c845969f78213ed22a`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc2dda21747e0f24eb8899101c98ef5308da0b0c03d4261d948cc05eeafd3a`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4906035e91e1c2cd24349bba98a0aaca7b0c76b9ababf89c516f7ea68a722f4e`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 189.4 KB (189428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1073bd005f968a5e6a27a563107ce59275075ba0e6a3eb26f1e397c2a26980f`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.6` - unknown; unknown

```console
$ docker pull kibana@sha256:f24062e4200766490937d9e643854d86c87c58c0c9bd8ad1c9da4c8be65983dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed16f695a6f55c53698cabb5d626f06211bbe68f1cad347a285ceb6af02b71c2`

```dockerfile
```

-	Layers:
	-	`sha256:2740d294c0c09b344cd1d51ff8d067479c0d0c3115fdadbf578f8d5efea9a249`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 4.3 MB (4302623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21417a4396fa27c6f1b46659e467a7b424814e8594d77dc64ad7b92f465e2ac8`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.16.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:4ba9cefa9549bf63450d3f5da3faaafaa315182a282fb6fcbc06eb49237f4000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.1 MB (412125519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a12334a36a75bdae33216ed82a497c2adcbc7e446dfe28417b2e1c9849e85f`
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
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN fc-cache -v # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/kibana
# Tue, 25 Mar 2025 08:54:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.build-date=2025-03-20T11:10:41.087Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=39969cb4b1ab957faf1e78d25d83ec04192ddc21 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.6 org.opencontainers.image.created=2025-03-20T11:10:41.087Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=39969cb4b1ab957faf1e78d25d83ec04192ddc21 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.6
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2b1e4f4f088bcb90a93113df565d844d0587dfed04db3f04692a54a907d4e9`  
		Last Modified: Tue, 25 Mar 2025 19:51:51 GMT  
		Size: 17.0 MB (16977305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31a8341abafddddf25cc0b5c8c06e6373048359b6fa165221a652b3d163701c`  
		Last Modified: Tue, 25 Mar 2025 19:51:58 GMT  
		Size: 352.5 MB (352508631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8709a3e9f82c089e9101384fa8b9b9bf3d2a85a7829fbb5f0fcc238124c919`  
		Last Modified: Tue, 25 Mar 2025 19:51:50 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d80251cd657f4cfd8a417f163a56a7c266932132967448f0404e74435350cc`  
		Last Modified: Tue, 25 Mar 2025 19:51:52 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368cc8d6d6ec0cdc299cf0619bc37efaa08accbf4572351ba13018e2f254f927`  
		Last Modified: Tue, 25 Mar 2025 19:51:52 GMT  
		Size: 5.3 KB (5276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e46aef1336a3b873708d2a1a18fa7aea2061e9a6d8c86d17abb6af043f50c8a`  
		Last Modified: Tue, 25 Mar 2025 19:51:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c329bf66610c984603e1b9d8e614863d33025b44488ccb566857849ec1277`  
		Last Modified: Tue, 25 Mar 2025 19:51:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16193d3d2247f44a99cfcdc5ff0039bb524a8e88751b23cc8947b48c8442419a`  
		Last Modified: Tue, 25 Mar 2025 19:51:53 GMT  
		Size: 4.7 KB (4708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00ee8ff81ca6b6aafa28b777ec986a4c4614814248dced42158bdbeb6f0a865`  
		Last Modified: Tue, 25 Mar 2025 19:51:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc517c7b6fcc113e4498122cf90fbbb9b7bd039cd74dccfd3617612ca6e034`  
		Last Modified: Tue, 25 Mar 2025 19:51:54 GMT  
		Size: 183.4 KB (183418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefc21b43cb3909989ddb97cb033f87f49e8dd18ba6223e5f2fd685e089a14d7`  
		Last Modified: Tue, 25 Mar 2025 19:51:54 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.6` - unknown; unknown

```console
$ docker pull kibana@sha256:7b147b12a0e0651c247c0c474b2831340cb1ec25c6946bef5db233ba0400b51a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08fecfe9b8e0924d9a22eb6556a2c0dea2fa55f813ce5e18138e9fe64f27941`

```dockerfile
```

-	Layers:
	-	`sha256:a0d5df669ab26e5ee83b6ed11512e8cbfc3b871edde57fa7ff3a6efc64bc5bf8`  
		Last Modified: Tue, 25 Mar 2025 19:51:51 GMT  
		Size: 4.3 MB (4302824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd93c6b633b4c59fcffcdb0b2cd3539f50d46e9d6ca8903f56e72ae562148b36`  
		Last Modified: Tue, 25 Mar 2025 19:51:51 GMT  
		Size: 40.9 KB (40928 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.4`

```console
$ docker pull kibana@sha256:54abdc26575477890b1b39f326777c44987d4df49e62604fb797b09a66ddd11e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.4` - linux; amd64

```console
$ docker pull kibana@sha256:f728ba6ae7e6b32aa91966fc6082c8c55a3f02c59d5f578030da76f9e80e5203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 MB (396262379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8c15e6ca2ce9cc98319ca5fa7365273242e97cb84f09cd3794f48dd1928aee`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 25 Mar 2025 09:28:57 GMT
ARG RELEASE
# Tue, 25 Mar 2025 09:28:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Mar 2025 09:28:57 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Mar 2025 09:28:57 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN fc-cache -v # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/kibana
# Tue, 25 Mar 2025 09:28:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.build-date=2025-03-20T11:10:44.572Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=57a32881bd4c7055491b10f3c957e7dcef2f1bf0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.4 org.opencontainers.image.created=2025-03-20T11:10:44.572Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=57a32881bd4c7055491b10f3c957e7dcef2f1bf0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.4
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 25 Mar 2025 09:28:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fcc5639d78eb058fe6d40b706191fa8991891cae5e6f952e955041f87ed412`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 10.7 MB (10725875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212bfae0699802674286ffe487a55b796665beb5de923749889f4b85db51095a`  
		Last Modified: Wed, 09 Apr 2025 01:21:25 GMT  
		Size: 341.4 MB (341353910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037b33c45a54ae7a976ee96632dc2c6e3cfdaa1085469a478e32672d074a806f`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000b5def795427d5c34e86989ec3452643bf86401b04dfc78fc518a87ddbd90e`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f990529fef711a617c86ef900630d7ec511c0ae102ebcdbb5a15ff4132e7b2`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fd28d0a7fe6fe5d11db816b6e4837b64f4c6d53b8ca65225336866fc2a1410`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a16d1476adc17df2dd9753b75de2a388f2cff69605d52785a602c0dd03a07b3`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472f074a5fa945eda17aa7c39b7463e3dc4e48431125443e4cfd4ec15d56b628`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 4.7 KB (4715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bf1317c5ab40cd08331d4a711f0286129eb83a4bf9d023e893e972183ee0e9`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f79b96fbd938fe2ce1e7dc6ed7e40da24f5d4466d218b6ce0e8b5b95e288011`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 189.4 KB (189428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810f5e6df1a1fcdee8e449872d75e5008f0e3d81d81fabfff299206ef8f66662`  
		Last Modified: Wed, 09 Apr 2025 01:21:22 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.4` - unknown; unknown

```console
$ docker pull kibana@sha256:c0f19aa1fceaa0fe36e6048f6408ec176d4817e93a1622cd8c626ec2be03f7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4433494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639e40514d3457a5e9412a124ce28d7d384b42712b8e864fb92fa2a58c24f424`

```dockerfile
```

-	Layers:
	-	`sha256:657e8a378b7c37e258cfb87bfef0dd772de887ebd9db96dbe5b062f41f5f7eb7`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 4.4 MB (4392815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6998cc510bac8063b9b5924ec11bbf7f0d8373326baa1427187cbfd6f5ea8454`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 40.7 KB (40679 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:c328dd35e729a53921b3fb34fb67f9c9fc4ba161fc8d2fdc09148c60fb1cfd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.5 MB (413490992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fa3b6c996917722fe20205d28ae0e6a9995258dc53e6755d13eff01e18fef`
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
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN fc-cache -v # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/kibana
# Tue, 25 Mar 2025 09:28:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.build-date=2025-03-20T11:10:44.572Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=57a32881bd4c7055491b10f3c957e7dcef2f1bf0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.4 org.opencontainers.image.created=2025-03-20T11:10:44.572Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=57a32881bd4c7055491b10f3c957e7dcef2f1bf0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.4
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 25 Mar 2025 09:28:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2b1e4f4f088bcb90a93113df565d844d0587dfed04db3f04692a54a907d4e9`  
		Last Modified: Tue, 25 Mar 2025 19:51:51 GMT  
		Size: 17.0 MB (16977305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c389e34b758259dae4a1236017cc38352074eb76999dad4da5d0b483bd85485d`  
		Last Modified: Tue, 25 Mar 2025 20:04:10 GMT  
		Size: 353.9 MB (353874088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879b7a78c243c6ff003b7b5f3be14f441ed4f12143949e35b353b34f01f7b672`  
		Last Modified: Tue, 25 Mar 2025 20:04:02 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6418951c659f7bed6e4ceba222393f2ac120b84bb1f0b194488b94eaa1a54b0c`  
		Last Modified: Tue, 25 Mar 2025 20:04:03 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a87a1e9f220c9ba27d969f3980d48628bd774c240d0978dc79b5e1507a52609`  
		Last Modified: Tue, 25 Mar 2025 20:04:02 GMT  
		Size: 5.3 KB (5294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b2f24d0833e7d32c724a527a865195041f895cce3037446a1c62d9d6b4ddc`  
		Last Modified: Tue, 25 Mar 2025 20:04:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78be47bda60a61adf7ded91d0affbf9ba4ac7ab6662b6b496dfd3ba90b082fd`  
		Last Modified: Tue, 25 Mar 2025 20:04:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab13deb25b0fe94a4fb74d9af0b611a0a0bb4d44017330f33b3bdd30da780d5`  
		Last Modified: Tue, 25 Mar 2025 20:04:04 GMT  
		Size: 4.7 KB (4715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6660616ae2cdd3d00002bd5ed55af61ecc3f30afac5aad426e3650ddb3c80f`  
		Last Modified: Tue, 25 Mar 2025 20:04:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4650844d506f23c2e4bb5f871641127c2d39a5c1ededbc5a16c0d0df03ae5d3a`  
		Last Modified: Tue, 25 Mar 2025 20:04:05 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f199b47aab07daa9ae5c22466a29d6d0ce4a8cbcb4df8202cde30419f7262ee`  
		Last Modified: Tue, 25 Mar 2025 20:04:05 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.4` - unknown; unknown

```console
$ docker pull kibana@sha256:6eaa5fae8d61c5cd531ba76d96c8f9c16b08c6acc06cb6d453980b0fb7b4c223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4433944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af94a591dd83466d1c3ba5614bef914f14e3aeed0642d59afc0488a97a1978ab`

```dockerfile
```

-	Layers:
	-	`sha256:15b42c9bd7eabd77cd7f0aa6734c0c004483c9925c89b8a4bd921fa5032f97b2`  
		Last Modified: Tue, 25 Mar 2025 20:04:02 GMT  
		Size: 4.4 MB (4393016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a769ee030446fe21ba9c9e79b26d1a22fa179561db2f795b49c98e0ccc324e`  
		Last Modified: Tue, 25 Mar 2025 20:04:02 GMT  
		Size: 40.9 KB (40928 bytes)  
		MIME: application/vnd.in-toto+json
