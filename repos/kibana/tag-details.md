<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.24`](#kibana71724)
-	[`kibana:8.15.2`](#kibana8152)

## `kibana:7.17.24`

```console
$ docker pull kibana@sha256:f712c6a5f7de029bc1f1c86d2bd13fa14122805f158ef4afae9265b00625ef04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.24` - linux; amd64

```console
$ docker pull kibana@sha256:f435c39a34e8a226883d02d37dde6dd37e54244e8c2f6d0ce566f6ae086140ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349007818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ef11c6f92f6a6470d0e9728f24bc081c1d6b999a9c07b73b75e2ecef45ce2e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05446250c1c1feba0ab37c2662e695aa5a13cd1717daefb3451b38991369f904`  
		Last Modified: Tue, 10 Sep 2024 21:59:02 GMT  
		Size: 10.7 MB (10704965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7987d168c820e5806df5762fba7fa81b9ad9c52e5c876be3006b472ba61ced8`  
		Last Modified: Tue, 10 Sep 2024 21:59:02 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f651379d019fb5c577f16194ef6d627617996d4a0a0e0e439c570090830a9f`  
		Last Modified: Tue, 10 Sep 2024 21:59:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e7cff6a301a3ac90c6e818ac52e1553797e690301d1f008bee1e70d553b26b`  
		Last Modified: Tue, 10 Sep 2024 21:59:02 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb374ae9c58475c61259a068bb3f30a2492aeed8c3a6ae9b3524f3c4be547d7`  
		Last Modified: Tue, 10 Sep 2024 21:59:03 GMT  
		Size: 5.3 KB (5294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2030ea58b7433e7d70e355a70fd99641fa65d4bcb05ffc378a72493b8ea22e4`  
		Last Modified: Tue, 10 Sep 2024 21:59:07 GMT  
		Size: 294.1 MB (294118888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876d38aedcf85a9cbd53b2ef26767b8290bf9c7172f113506565ea5840c5ea73`  
		Last Modified: Tue, 10 Sep 2024 21:59:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d63827f3465c7fa52597e5f1a20cd4540d7cf428a31f570f64fed6fde85025`  
		Last Modified: Tue, 10 Sep 2024 21:59:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb5ef78da471bf093a3af8260df5e80a792aaf59dcd7d4085289510d3ea6c9f`  
		Last Modified: Tue, 10 Sep 2024 21:59:04 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ff32294afe7087f966dcd4bd3389f9afcca21cf38610ee52256532738e2b1c`  
		Last Modified: Tue, 10 Sep 2024 21:59:04 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa672d84e1bbc969529ad01975b0173ee4467078939a31c546defd4225c1ec`  
		Last Modified: Tue, 10 Sep 2024 21:59:04 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa23501b43c6d790d5fc8818a21dd44d6cab1671ea3ef6489d727ee003be6047`  
		Last Modified: Tue, 10 Sep 2024 21:59:05 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.24` - unknown; unknown

```console
$ docker pull kibana@sha256:054f08d0fcee0d446ea591c47c8c20ee1291a9cc8b546ba510f7f42c67990c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72da2b5bb2d31c184e47e4287d58f8c070daf92fe289a9ac4f8ac0f1f2bbb570`

```dockerfile
```

-	Layers:
	-	`sha256:0869e8351b7a558b878efbec4887cbf96f7dd2ca51e9c25e8cb98ffa768fb62a`  
		Last Modified: Tue, 10 Sep 2024 21:59:02 GMT  
		Size: 3.4 MB (3375465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00534530b352f5c3f2c838667e22cd6b83332b76c3f65f8e010cf75d93e065e`  
		Last Modified: Tue, 10 Sep 2024 21:59:02 GMT  
		Size: 44.3 KB (44255 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.24` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:0a8547c36294e7c96c99f669b744b1fdbe289fe5decabb3dfe30e5a70e5cbb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359892485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7741f0c82c68a32307e862f28f150ec1d7712b176585cc63c0999c75c7e1460`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
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
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a91294367125b4ffc56c10c3166acbbe8213b599ff913557f7aec2f252f214`  
		Last Modified: Tue, 10 Sep 2024 22:03:49 GMT  
		Size: 10.6 MB (10551752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c519a1b07c27a81688f260a0453b4c84e08eb1c959a25533e110806038af5a`  
		Last Modified: Tue, 10 Sep 2024 22:03:48 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c46ca6ee39abd94e32b65782a9781b2955ce75bd525bd4f1e6beece453b76`  
		Last Modified: Tue, 10 Sep 2024 22:03:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f8aec75b3af208c0282e2e75beb404acfbaf1e5300189a7612a40231af10b1`  
		Last Modified: Tue, 10 Sep 2024 22:03:49 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e58d33f50b3cc446d8c93d7677934ebb4143bde662c607e946013d81334fe91`  
		Last Modified: Tue, 10 Sep 2024 22:03:49 GMT  
		Size: 5.3 KB (5303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74de1c48b17ba81854f64f75f86077eb5cba4da46731ee2e3c70789b46776dc8`  
		Last Modified: Tue, 10 Sep 2024 22:03:56 GMT  
		Size: 306.7 MB (306700734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc780ccd71d2fcee0f64c9c06e2c54c770c2c7dfc13c9657cf2b9ce88db28f53`  
		Last Modified: Tue, 10 Sep 2024 22:03:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ab22f7e54c7e1ac3457f67f35d3a0d23bb878ded1df94c1be78c015033adaa`  
		Last Modified: Tue, 10 Sep 2024 22:03:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade0fc51b5f640c3db68f90b9253d60a6d8d9682a1a7264fecbabc2b8af3e46c`  
		Last Modified: Tue, 10 Sep 2024 22:03:50 GMT  
		Size: 4.5 KB (4507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d36f55818419aff6793a5d38d5264e7a2b80e0d8db9ad5e7d4d1ebb3751b8`  
		Last Modified: Tue, 10 Sep 2024 22:03:51 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e628db239b5246826842e37476d8d812d13db2f342be0f86300e3d80af01ee9b`  
		Last Modified: Tue, 10 Sep 2024 22:03:51 GMT  
		Size: 183.4 KB (183421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904f1963d55f9596d0d85af56c00cd85125e8610ce2e3ce551db4615fb00403d`  
		Last Modified: Tue, 10 Sep 2024 22:03:51 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.24` - unknown; unknown

```console
$ docker pull kibana@sha256:5d634ce42215302c35e754e40029ed436345a8ab4e7ab9256d639be4e3331ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3420234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8deb4f77303da5f432ecf0c10483b10f1165ab215c82c70d1f673518eac932`

```dockerfile
```

-	Layers:
	-	`sha256:cceeaf919ead74b8d24c6226d2f15e4d105d3cbda8917258a992cc4177fd8fd9`  
		Last Modified: Tue, 10 Sep 2024 22:03:49 GMT  
		Size: 3.4 MB (3375715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff532fd8667ac6b30999b72fa7f80bf6feb590e800c7a297f9e8b5c1c5a4cd03`  
		Last Modified: Tue, 10 Sep 2024 22:03:48 GMT  
		Size: 44.5 KB (44519 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.15.2`

```console
$ docker pull kibana@sha256:68fa7c301798aa532e10e345ceb929bd6dadf86269acf49ea76b4c82774eb9af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.2` - linux; amd64

```console
$ docker pull kibana@sha256:ff4a63e7d12b0d0a91b14b2a195cd7c2712725096984704394dd5de623b6fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.2 MB (394161223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bd4992060ddbcf29b26a7749d3d1a442e6166b91cde62a261b068db8e707cd`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a357bd168d994da231e9367f606ba576c346e415cef3f6403c998b565c655c1`  
		Last Modified: Thu, 26 Sep 2024 23:00:01 GMT  
		Size: 11.4 MB (11380994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e55e6d464157b9c96e0acd028c1a1468eaabca93086448ee34fe96b67840d2f`  
		Last Modified: Thu, 26 Sep 2024 23:00:06 GMT  
		Size: 338.6 MB (338596338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398abcec699fcb6f0e88e15381d2bdf0339b7f4d59517e67f54aaf1fb94f3a7a`  
		Last Modified: Thu, 26 Sep 2024 23:00:01 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede32880c29763a19566e4aa5bd0ae5100fcf0455deaf265b3472f02696fdcf2`  
		Last Modified: Thu, 26 Sep 2024 23:00:01 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33c8f71f01711bc60f7ab7e369b9e0ce2fece83c78f2dea6e0841981da84f5`  
		Last Modified: Thu, 26 Sep 2024 23:00:01 GMT  
		Size: 5.3 KB (5277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9cb0cf3d0c0be973e128c269decc2d0ed2904a6c2328245792161173985162`  
		Last Modified: Thu, 26 Sep 2024 23:00:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285f98109ec3a115249e420603f1aa5412b49a763de3a3c122399394383a9272`  
		Last Modified: Thu, 26 Sep 2024 23:00:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c35c35103d3021c35bbe12dbfc94275f696b2b961c4a318b941e59b94c97c3`  
		Last Modified: Thu, 26 Sep 2024 23:00:02 GMT  
		Size: 4.6 KB (4627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1853178023ad16a7a3ccf29d64946c7ee540e2c39ad4d9ce301d0466b921bc5`  
		Last Modified: Thu, 26 Sep 2024 23:00:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2e9238142ee5b53963fd174c6febd228793ce0e435d73fc2b007293759fb2`  
		Last Modified: Thu, 26 Sep 2024 23:00:03 GMT  
		Size: 189.4 KB (189433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d11c418a4bb8a7080442c9d32a46ae40a03d00279aa0a16f8c38bb931dde45`  
		Last Modified: Thu, 26 Sep 2024 23:00:03 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.2` - unknown; unknown

```console
$ docker pull kibana@sha256:bd79953fc188a9d3cb3786d7565cc7bb587b549cbef205571a19280b58361225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9b8630fb70881fcfae3b3fd08fac225d3af7f06273051820c53a8dbe416c21`

```dockerfile
```

-	Layers:
	-	`sha256:2f482a3ac98a40319a66a3de9386235f58195bf9f0b601415624c1699b507cbd`  
		Last Modified: Thu, 26 Sep 2024 23:00:01 GMT  
		Size: 4.1 MB (4070754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1844fb682b2d1557191a9c0a6f87273af9c67ced94e1bee5ee4dbccda7531694`  
		Last Modified: Thu, 26 Sep 2024 23:00:01 GMT  
		Size: 40.4 KB (40387 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:ed9dfd7fdd3a953158a25cc9d45e2eeed6efb2583976456048e97f03746399c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.1 MB (405063123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa0a57ff7ac56ffd4121fe66f0e5f020410b0a48eb40678ec639bb76ebf2531`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
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
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13daad5aa0fe6527e178dd03f0b7d35eb9068b22b15c211e021fe07b88ea72d5`  
		Last Modified: Fri, 27 Sep 2024 01:09:36 GMT  
		Size: 11.2 MB (11224363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9257f8acae0c2785ae75c90eb8b275696bce69a84e3602efd8341b2a5a8585`  
		Last Modified: Fri, 27 Sep 2024 01:09:43 GMT  
		Size: 351.2 MB (351198857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d6fab02fd53ccd65e9136b113ce59890fc2a283be65f2313b53fc218aa8850`  
		Last Modified: Fri, 27 Sep 2024 01:09:36 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f89e5e7728e504049111db65ab096bba6c8dbc8f334bb81d0542bdfc8d9ba1`  
		Last Modified: Fri, 27 Sep 2024 01:09:37 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8a2416e0c66ac32b23230fa091c52dee84405df378bcff2af30ea4c94cba56`  
		Last Modified: Fri, 27 Sep 2024 01:09:37 GMT  
		Size: 5.3 KB (5284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180805e49097bc30d703373143bba32a965deb604b4db98ead16e3b80e67b547`  
		Last Modified: Fri, 27 Sep 2024 01:09:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0a8b635b4300470767778e13901ab73dbc09b7a3f5d1d42a66799206cfccab`  
		Last Modified: Fri, 27 Sep 2024 01:09:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944f96952008139ce587305c9eea16ceb7488c40b18303ea8f3f81afbe8b62e1`  
		Last Modified: Fri, 27 Sep 2024 01:09:38 GMT  
		Size: 4.6 KB (4629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683dd9f47291ac42574b5d9fb758b234beda5deceb992c915308053f9ee4265d`  
		Last Modified: Fri, 27 Sep 2024 01:09:39 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1b07c0fb5390c03df2491d0f49e5ece1d125abff141ed5cc8330e42f69b370`  
		Last Modified: Fri, 27 Sep 2024 01:09:39 GMT  
		Size: 183.4 KB (183421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7e31e50418a9c35d36491416af9f96b3ecf41088cdb7ad9fcd932929d3182`  
		Last Modified: Fri, 27 Sep 2024 01:09:39 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.2` - unknown; unknown

```console
$ docker pull kibana@sha256:8e701594a7d4c9b0cda01ef2772754f235b6748cd2611b3547028fe2a37d634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bd24ca329b4e50b0979c86ea7455039c5b26deb5e76e2cd32ee10091215cc7`

```dockerfile
```

-	Layers:
	-	`sha256:d4b10c59863831cf79d91a0c408d050eb7615075e9bd6f1850dfa6d0a3920888`  
		Last Modified: Fri, 27 Sep 2024 01:09:36 GMT  
		Size: 4.1 MB (4071004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:711ef2acd27ffb5b0b9a60c2642553533dfbb5169240693c474e59ec97a5880e`  
		Last Modified: Fri, 27 Sep 2024 01:09:36 GMT  
		Size: 40.7 KB (40653 bytes)  
		MIME: application/vnd.in-toto+json
