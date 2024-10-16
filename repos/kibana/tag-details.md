<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.24`](#kibana71724)
-	[`kibana:8.15.2`](#kibana8152)

## `kibana:7.17.24`

```console
$ docker pull kibana@sha256:3147f2feede0b23056eb23b191de8ada67d49518c03a4b56c894bef7ec8e7acb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.24` - linux; amd64

```console
$ docker pull kibana@sha256:a9b1a1fc9e35b5cf12e9eaca81e775176b367a9117c3a9cd865dbb14c9d47b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349026042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a483dc876acdb68fac5411b6eb6caa8c21553bb372fed76f34217fcaac017f79`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 10 Sep 2024 08:21:14 GMT
ARG RELEASE
# Tue, 10 Sep 2024 08:21:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Sep 2024 08:21:14 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN fc-cache -v # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/kibana
# Tue, 10 Sep 2024 08:21:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.build-date=2024-09-04T11:10:43.736Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4fb3ec3c959e4c569aca4674243a2ecba9d973a7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.24 org.opencontainers.image.created=2024-09-04T11:10:43.736Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4fb3ec3c959e4c569aca4674243a2ecba9d973a7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.24
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 10 Sep 2024 08:21:14 GMT
USER kibana
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0b1010c811e3776d9820da5d7cc60a9ef4ce6a9d16285fee841627e4fb9b24`  
		Last Modified: Wed, 16 Oct 2024 16:43:06 GMT  
		Size: 10.7 MB (10723911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4f5d971c5a0e5bf184789cc0d3baac799c1133e03d80edf66324104f9e8338`  
		Last Modified: Wed, 16 Oct 2024 16:43:06 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af1bc938e10f148ba275925a9ef50cc6126b0e81573d093321d92e167b1781`  
		Last Modified: Wed, 16 Oct 2024 16:43:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be96a8f6360db4ab36edc339ed138ea533100112308601e16dfdde9bb8c59bf`  
		Last Modified: Wed, 16 Oct 2024 16:43:06 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83938464dc7fb77cb8b6be2ff248b1889165a00c90ce2f7b313cd7aa70427634`  
		Last Modified: Wed, 16 Oct 2024 16:43:07 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b73157a38e554cea31ce218a51c7e4291094e6acd6f7cd4fa9e53f9510132f`  
		Last Modified: Wed, 16 Oct 2024 16:43:14 GMT  
		Size: 294.1 MB (294118892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffb862126cf6d58fc0def051c42b0ba9e9abe679f39fcac5dc7030a153fe82e`  
		Last Modified: Wed, 16 Oct 2024 16:43:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0e85889489497e074a60ab12c88c056207f463179ff3ac05e108cf61308089`  
		Last Modified: Wed, 16 Oct 2024 16:43:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2a9ff00b24ad3e61a31ab7e13b8822f0f4b1388767deeb29d08d9a71858833`  
		Last Modified: Wed, 16 Oct 2024 16:43:08 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d88e534b322952848651ce172932a289ff60b983a713f7e1717780f62ab87`  
		Last Modified: Wed, 16 Oct 2024 16:43:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848c0a66928e762bbf42c57b2aa94665ccbefafb897c42f243cb8390c2bd1503`  
		Last Modified: Wed, 16 Oct 2024 16:43:08 GMT  
		Size: 189.4 KB (189431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7258a29428d017b7a2cc5da0de4887106fc6219d56fd683c408740c57fd1024c`  
		Last Modified: Wed, 16 Oct 2024 16:43:08 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.24` - unknown; unknown

```console
$ docker pull kibana@sha256:dfef89bc16163da6b4e87352b9c077cec755a2ee8e762a4e1769b488ebd716c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3425661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6295c2f7b7cc7a577d111e5672b18bc2239d2a92bfd0150b5031ab72ab8ca0`

```dockerfile
```

-	Layers:
	-	`sha256:322cec4696df6f9f35669193f2f3d3297b61a0e8c141aa56becaf6878fa89dba`  
		Last Modified: Wed, 16 Oct 2024 16:43:06 GMT  
		Size: 3.4 MB (3381368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b79cef8c2651b93e8139508f64de96906853cc48bced0d2cfbebe6993af68ac`  
		Last Modified: Wed, 16 Oct 2024 16:43:06 GMT  
		Size: 44.3 KB (44293 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.24` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:da9348bc579afd91261ed7b852b27747e380fe08acd7682edee7c1e9fb0a751e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359915384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845a1ea9f655d1584165c085e52fe60d77bff80f5511bf00441635040ccc375b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 10 Sep 2024 08:21:14 GMT
ARG RELEASE
# Tue, 10 Sep 2024 08:21:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Sep 2024 08:21:14 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN fc-cache -v # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/kibana
# Tue, 10 Sep 2024 08:21:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.build-date=2024-09-04T11:10:43.736Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4fb3ec3c959e4c569aca4674243a2ecba9d973a7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.24 org.opencontainers.image.created=2024-09-04T11:10:43.736Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4fb3ec3c959e4c569aca4674243a2ecba9d973a7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.24
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 10 Sep 2024 08:21:14 GMT
USER kibana
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9292fd052a4e5afdfe32d05bbde9aa9737b03f4f092222375f58aa893250f48`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 10.6 MB (10575032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe65c4e7d35e036f20c05c604524a12b7c180dcf8354448b764990a740a798`  
		Last Modified: Wed, 16 Oct 2024 03:24:58 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed698c438cb75e359246a05f0a09d8ab3744169938947a81eab7ff9c35ad192c`  
		Last Modified: Wed, 16 Oct 2024 03:24:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bf4c1f716146058b2b87961c282bbca1bc4015028244ed2a66f638d20b70c6`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1172c9a679de7f18a23a7d365c9a4ba12121e229f42af8fce85cd18a15227b`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acdea2f83a2972088d1c9554f767ba67c1b69cf8bc24dae3cbd0d906b70e6a6`  
		Last Modified: Wed, 16 Oct 2024 03:25:08 GMT  
		Size: 306.7 MB (306700783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d12cc5179408e41dcd2475ba2c45d370f03aa50de457e60ec73b2043d1a959`  
		Last Modified: Wed, 16 Oct 2024 03:25:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f278d701ed69f6232b5f2a8e83298f473e01f2ad738cd69bdeeac43d3ca99c80`  
		Last Modified: Wed, 16 Oct 2024 03:25:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1469224f7966b05b1113893821317437725aae69fbe7a75e756a674fded488`  
		Last Modified: Wed, 16 Oct 2024 03:25:00 GMT  
		Size: 4.5 KB (4500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabcd47631d11c54c0e40718d2d1abac26b328a9b63bb31992296782dd5b667`  
		Last Modified: Wed, 16 Oct 2024 03:25:01 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9065d414e85b530c093e7b87fd94b7d633affef7f2b3684d624a0befa1a3ae35`  
		Last Modified: Wed, 16 Oct 2024 03:25:01 GMT  
		Size: 183.4 KB (183416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516173a9a4882201a18b02234febd8ed3723dfacd411a46cf97c6e8a914ded9b`  
		Last Modified: Wed, 16 Oct 2024 03:25:01 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.24` - unknown; unknown

```console
$ docker pull kibana@sha256:7b93ffc8322f37dec398d052cfbf7931e27849be83de3f43e348b98606885832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee799f1951a1f11f9906ddd5c457f7338542dcd7176e0e4c865037bc4bf4929`

```dockerfile
```

-	Layers:
	-	`sha256:c0f62c8d91612386688f454684100a2ed191ae11e9f244ee6c8bf5a5a556d3b4`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 3.4 MB (3381618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0171979d3ed19b29daadd787f8d04585c0c497f47f7d4e64ad79d631a60dd807`  
		Last Modified: Wed, 16 Oct 2024 03:24:58 GMT  
		Size: 44.6 KB (44565 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.15.2`

```console
$ docker pull kibana@sha256:05ae9ce80aa93c81965cdd4bb53eafa37239f891d934a8e27a64b561f0c18c39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.2` - linux; amd64

```console
$ docker pull kibana@sha256:3a1c40276210514f2faa37bd63302e99cf3efe107353404da5b2f9cc46ddf2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393746005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51f419bd4fcdfc238e58222516afae5af8ae4c586d1f505ee08629f89064966`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 26 Sep 2024 08:08:51 GMT
ARG RELEASE
# Thu, 26 Sep 2024 08:08:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Sep 2024 08:08:51 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Sep 2024 08:08:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.build-date=2024-09-19T11:10:25.889Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5a522bfe14bc6d06c20bc337477fd53f7c538973 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.2 org.opencontainers.image.created=2024-09-19T11:10:25.889Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5a522bfe14bc6d06c20bc337477fd53f7c538973 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.2
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b92ef1a28f2065d272ff1744ed9d5bbb899ecc7786b80fc6ca82ad9ae44bf6`  
		Last Modified: Wed, 16 Oct 2024 16:20:10 GMT  
		Size: 11.0 MB (10966624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0b9eb9a887610d8e02ff3ac3d37c57b7168ffa70669a9d8bd7f06f6a05da3a`  
		Last Modified: Wed, 16 Oct 2024 16:20:15 GMT  
		Size: 338.6 MB (338596211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5128a074403dcb198a2164c0cfde3716ff674be5fd414a9fe327d64aa5db0710`  
		Last Modified: Wed, 16 Oct 2024 16:20:09 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9a0227da13f82372503ea55de30aacbf68fa2965adb802930d99fd61f2bda`  
		Last Modified: Wed, 16 Oct 2024 16:20:10 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a67af44838111720d381748250e8678b2e3336b5bdc8bf26e92b25a5a7fa17`  
		Last Modified: Wed, 16 Oct 2024 16:20:10 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be16a4e954a9f2368ba9f7de074d89c6d9473c974de78da1b0383cebb6c98655`  
		Last Modified: Wed, 16 Oct 2024 16:20:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbbe041dfcfac716e16afabb4daafcbf80d316b1daa810d599c848379a74444`  
		Last Modified: Wed, 16 Oct 2024 16:20:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dba8e700c486b094b2782dbbd3c9812a3ac749819cae56317abe1f78504c7f`  
		Last Modified: Wed, 16 Oct 2024 16:20:11 GMT  
		Size: 4.6 KB (4626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555f2935a28fda9bf329f521e7ac41084c0b6d03e1cb00776d7a19d803f40b3a`  
		Last Modified: Wed, 16 Oct 2024 16:20:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddc0a3a5765c68f18730992060d4738de923e9ce6e032a41ae2b7f72bf9d9d1`  
		Last Modified: Wed, 16 Oct 2024 16:20:12 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d77be832bf2adf92b38188d3b5bb5622851e8578d8ceaa48748e68b7402e5f4`  
		Last Modified: Wed, 16 Oct 2024 16:20:12 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.2` - unknown; unknown

```console
$ docker pull kibana@sha256:446433063586e764687f837a59f11c8f3afe4f88fdd2fc3c5b7a2dbb753f7562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd563ac1563ab9dc2eef356495be37e4b47c15f710d31283b98935e51ba2db4`

```dockerfile
```

-	Layers:
	-	`sha256:cedb6baec10447fa51d84c0e8e95bade6790d59b70ce487465d629f640188b85`  
		Last Modified: Wed, 16 Oct 2024 16:20:09 GMT  
		Size: 4.1 MB (4070754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fc9f8ac86e20bc1cd6af08fc725ce291ea319e3ca8f5af7fe56e11521444e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:09 GMT  
		Size: 40.4 KB (40426 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:000c0ae07d7ba3aa0b418cadb181ca666d51134bde1c90ca558f25106090808b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404656474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7789b6d4ced50e1f2d0bab34673c43aea38f4935504e48004a2804ee731c24d2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 26 Sep 2024 08:08:51 GMT
ARG RELEASE
# Thu, 26 Sep 2024 08:08:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Sep 2024 08:08:51 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Sep 2024 08:08:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.build-date=2024-09-19T11:10:25.889Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5a522bfe14bc6d06c20bc337477fd53f7c538973 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.2 org.opencontainers.image.created=2024-09-19T11:10:25.889Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5a522bfe14bc6d06c20bc337477fd53f7c538973 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.2
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6ba831b83cf620584ce3ad5fef753a25663549f8d119af4a0a620914f0f1de`  
		Last Modified: Wed, 16 Oct 2024 03:20:59 GMT  
		Size: 10.8 MB (10818125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1ef2f72a6b0df7a49ff43c17a7acf583e3c0afc10225dc48f11b901310be5c`  
		Last Modified: Wed, 16 Oct 2024 03:21:06 GMT  
		Size: 351.2 MB (351198857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a772ebe0d034552073d8570dd976930bcfd13f459722a9016b64db454d563a88`  
		Last Modified: Wed, 16 Oct 2024 03:20:58 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d1cc0ce12d298e18b6675fca6a7c3a19f8339db94b811a3ad18c081d6a3cb2`  
		Last Modified: Wed, 16 Oct 2024 03:20:59 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194ee217a7e14f4ba63d4c2e38153e206bd071a2c218c1707523effeaf5ef4e4`  
		Last Modified: Wed, 16 Oct 2024 03:20:59 GMT  
		Size: 5.3 KB (5276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487cc1666dc92a76189334afd98c10b91837f3a5439fbab01e1d0caa5fc5acdf`  
		Last Modified: Wed, 16 Oct 2024 03:21:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a564565898982f2f2a5e95208056e31ed879e96229169ad552fa47bcc4472d8`  
		Last Modified: Wed, 16 Oct 2024 03:21:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc1a865b6b95098da80934976cf029af15893e2f0b20ca30e70786ac726a34b`  
		Last Modified: Wed, 16 Oct 2024 03:21:00 GMT  
		Size: 4.6 KB (4623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7168c8c8ff3fde2ea26fcace03e9d5780bd359b98378cee841daa8d0a156993`  
		Last Modified: Wed, 16 Oct 2024 03:21:01 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d3dba23e4c9e0720dde328f54eb6e2c8de76bc9cff688095217054c04580ed`  
		Last Modified: Wed, 16 Oct 2024 03:21:02 GMT  
		Size: 183.4 KB (183418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68097122ab461cfe82be8f945b924ca1ab540fdbe650f830ee6339fa1bacd1b9`  
		Last Modified: Wed, 16 Oct 2024 03:21:01 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.2` - unknown; unknown

```console
$ docker pull kibana@sha256:6dfc306a8537687a0ef8f71fd9c713628519877dbb404e26dfdb2462a1ace823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4d6dc8e5816843bb2b7cede4e554054ad16990cac0553f37a7011368a10659`

```dockerfile
```

-	Layers:
	-	`sha256:8b75ef73089df04d755ed4d03d66288e6fc4aeb53c6427265eb787161ff64c4a`  
		Last Modified: Wed, 16 Oct 2024 03:20:59 GMT  
		Size: 4.1 MB (4071004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c892dc76f20da428e82b41607c9881ec0bb9b05ac0e895f7b105ba77a8b67d55`  
		Last Modified: Wed, 16 Oct 2024 03:20:58 GMT  
		Size: 40.7 KB (40668 bytes)  
		MIME: application/vnd.in-toto+json
