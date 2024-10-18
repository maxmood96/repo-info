<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.24`](#kibana71724)
-	[`kibana:8.15.3`](#kibana8153)

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

## `kibana:8.15.3`

```console
$ docker pull kibana@sha256:47824ff5ca06578c8de76ab9b38b655b5d12550d413393cb626b66efdbf24617
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.3` - linux; amd64

```console
$ docker pull kibana@sha256:36a568fa4917d5b7bbf9f542de45ac4224b1e2dfa239ddfb0512602549d908ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394758461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e79e6b434938854674a4ac367f2e08d8ef489152a7a0e60fa023d8cb57474c9`
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
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN fc-cache -v # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/kibana
# Thu, 17 Oct 2024 12:21:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.build-date=2024-10-09T11:11:49.786Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3933429968aafb1ba31319fc38649d0f974044bf org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.3 org.opencontainers.image.created=2024-10-09T11:11:49.786Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3933429968aafb1ba31319fc38649d0f974044bf org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.3
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 17 Oct 2024 12:21:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e81878edc4fac5cec441a43d55d42a4ccda5f061205c121fc4806d01d95877`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 11.0 MB (10966616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2312b8c1d8c6c295daae8801c856bbc9b0c27a80133f5004d467ea0351eea946`  
		Last Modified: Thu, 17 Oct 2024 21:00:53 GMT  
		Size: 339.6 MB (339608695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86e1486e58baf6985b65ce10f332493c50d5bd307ad22a81b264bde6c97855f`  
		Last Modified: Thu, 17 Oct 2024 21:00:44 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042420ce6076b22215500cd72e65b7f9fd3e99d77f564209379821b4de4048c1`  
		Last Modified: Thu, 17 Oct 2024 21:00:46 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bca47f98c76ebfc15952de4cafd4504bb69312e94d8b284cd94d9720a0d737f`  
		Last Modified: Thu, 17 Oct 2024 21:00:46 GMT  
		Size: 5.3 KB (5274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d84a8a04346d1d0bf8c478a3ac35cf80e96fdee3738b154bf3506f61ab24988`  
		Last Modified: Thu, 17 Oct 2024 21:00:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f20def6164ce76efac95afb410323a0a66d330d86d7c02c5f651a92dbe7206`  
		Last Modified: Thu, 17 Oct 2024 21:00:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e373104978a531f777adb63d24a126bc369d5700bd7474fba3962904b5a12569`  
		Last Modified: Thu, 17 Oct 2024 21:00:47 GMT  
		Size: 4.6 KB (4625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bbb965b9c197734fb6626e5b9d1714b4bcf6978f33dfd2e998d1722cd39480`  
		Last Modified: Thu, 17 Oct 2024 21:00:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c325d52041107a5e71b22b4aec6ebc45fb4781664785c955f36e6167777f40`  
		Last Modified: Thu, 17 Oct 2024 21:00:48 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906d54432ff1d9fa69551f460ac8d6bb74b0cd352a0598329c98a66588304bba`  
		Last Modified: Thu, 17 Oct 2024 21:00:48 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.3` - unknown; unknown

```console
$ docker pull kibana@sha256:2db1e594ec8332860c9e2499c44c4fdf07562db7d6e04b24ee4c0375f4bf77f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69ced5ac5c204ace914bf4b33739fe49c2b8b28341048696cac2381b26cb327`

```dockerfile
```

-	Layers:
	-	`sha256:612a809daf52ccb82d52289f1ea32ffbc36f91b74263e50aa40d6c235431bad3`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 4.1 MB (4070903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de951ebc07571c3da9af40a247b641c44bbcbff680cae6aed81d707512cdf6a`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 40.4 KB (40425 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e2e2e6f9ed8902087e0592730a7c6edc94148a4f977d9df9189c1f9925f57727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.8 MB (405821992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e436961c293225cddc2793b96d9e46a070fbdfa3f8ece9b0f110335f7fdd6`
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
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN fc-cache -v # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/kibana
# Thu, 17 Oct 2024 12:21:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.build-date=2024-10-09T11:11:49.786Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3933429968aafb1ba31319fc38649d0f974044bf org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.3 org.opencontainers.image.created=2024-10-09T11:11:49.786Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3933429968aafb1ba31319fc38649d0f974044bf org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.3
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 17 Oct 2024 12:21:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 17 Oct 2024 12:21:47 GMT
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
	-	`sha256:80ee6d8e35c71b9d4909022afbad37efb7d48f1f6b1ca819347270106f5106b6`  
		Last Modified: Thu, 17 Oct 2024 22:20:54 GMT  
		Size: 352.4 MB (352364368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff30b920890a2c495f379f559e7064243ab5398065c95db39cae562ef8e97b1d`  
		Last Modified: Thu, 17 Oct 2024 22:20:46 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c12a1fabb536688d5956b33b5a0593e172990d62beefd0b3171bbda3f2bd88c`  
		Last Modified: Thu, 17 Oct 2024 22:20:47 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b75b292032195705ebb38ddb4930e1a69ee95aac385a79400d427d30aaa86c`  
		Last Modified: Thu, 17 Oct 2024 22:20:46 GMT  
		Size: 5.3 KB (5281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f56cdecc00fd6f6b663514cf57e1c8b5d4ef7ba3bfd56d301235fabaa31e7c`  
		Last Modified: Thu, 17 Oct 2024 22:20:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7a7e5d863dcf9d0e36c8576f063cb52f382a80c3ae67475f75e672d3fa6858`  
		Last Modified: Thu, 17 Oct 2024 22:20:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1e14346d69ba3c49fd2a23443c75f2935c0f96795a6971bfb7b83ff1629702`  
		Last Modified: Thu, 17 Oct 2024 22:20:48 GMT  
		Size: 4.6 KB (4623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869cd104df7f51d5115842c750f0a10beee0a2621b08f44e37161340336c95c8`  
		Last Modified: Thu, 17 Oct 2024 22:20:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af00746a9670a0545c6c46c2ffe66a53dee088167099f7e64a8bde7536ad23f`  
		Last Modified: Thu, 17 Oct 2024 22:20:48 GMT  
		Size: 183.4 KB (183415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5038d92764f308df1f22dcd158bca835dfb5f364a810cdabd9c2cde631fc2a0b`  
		Last Modified: Thu, 17 Oct 2024 22:20:49 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.3` - unknown; unknown

```console
$ docker pull kibana@sha256:8d82ccf652591320627593027c061950e5cbbc5d08ccf2d5aad8b90013489c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5c05e4a1ae1c86831c41d4adde2bc3a2284edc5db19162fa530d0ca5903598`

```dockerfile
```

-	Layers:
	-	`sha256:93ebb2f405d78ae1e481a0e3fd67cf24c6c9aec60e2fb0f2c365182bd2f91826`  
		Last Modified: Thu, 17 Oct 2024 22:20:47 GMT  
		Size: 4.1 MB (4071153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3660dc8315cc9f2ad6de2053f9eaf3ac6a826ecea7aede54f175303c30ebd2`  
		Last Modified: Thu, 17 Oct 2024 22:20:46 GMT  
		Size: 40.7 KB (40667 bytes)  
		MIME: application/vnd.in-toto+json
