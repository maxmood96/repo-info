<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.24`](#kibana71724)
-	[`kibana:8.15.1`](#kibana8151)

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

## `kibana:8.15.1`

```console
$ docker pull kibana@sha256:826304508019ce346f35a6817b1e730c18efe2b5882bf12daec477060c98010e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.1` - linux; amd64

```console
$ docker pull kibana@sha256:426b9e373557bf62e6885aa98782505025d41f20100b069a310c75939d2926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393742062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0dde5a104ccd67354bd7538f97937b9942963e46d52dec64a90d8cf924284a`
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
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Sep 2024 16:37:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T12:15:21.436Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T12:15:21.436Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fdb71e81f1aab48fe4befba210ca076bee27c9ca7a9c74036983fe07eb77f5`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 10.9 MB (10945277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f38bcb526e838da90ffc8bdce23188725f29cabdc81b94a4dd49711ccfa18bf`  
		Last Modified: Thu, 05 Sep 2024 22:05:43 GMT  
		Size: 338.6 MB (338612904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb7acd1efc4f4ea7280b7bb2d31b715da2a447e03f9bb6b5a89fcd61030dfb1`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846f1629c72a6eb06ecccd8fdb1ec09e93b90a05b26bafbc4f29ca6727276c21`  
		Last Modified: Thu, 05 Sep 2024 22:05:34 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce6b9672912b161e80b737151de4a4cc5edb1f61e51103e03737f8c00f393c5`  
		Last Modified: Thu, 05 Sep 2024 22:05:34 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34aab2c6e0fba6241730b041de8a36e1c1c535a5051e2dce9b016de3374a02b2`  
		Last Modified: Thu, 05 Sep 2024 22:05:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f81ccb102c8fa5e7d5bcf38f08c1b25667c82b13952aa2cf520c387febbe2cb`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208be2ce3fe324c3b60ca9a08c42d48dbbb347b8176815fd750de341949530a8`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 4.6 KB (4627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8519ba4305d25228c6d62a46bf92f529f35e43c323b284aded34f190b0dff4e8`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53aaa438adccd4389f3be76872845d7319ab2dbc8935c53eba1c994cb1ab66`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 189.4 KB (189430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c108aac256f036478ad3e192075be59e27990d0fdc8ca93803bcfc10b6090681`  
		Last Modified: Thu, 05 Sep 2024 22:05:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.1` - unknown; unknown

```console
$ docker pull kibana@sha256:8cf439d59109dbab0a84c1b2eb1429a3a689fa731e26953a5f6a711bb8182cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4103967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb8dd79606ee06e81ead98b0723dd86a4bdb203c5c3d1b9908a2997fd7ff254`

```dockerfile
```

-	Layers:
	-	`sha256:2220ecce9ce8bd7409c827767dd36c3c279905ac8d4f4af20449dfb5f160d03f`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 4.1 MB (4063579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef92ee7d97b53f99ff9d9a72abeadbe370c71dfab34187f6457adfa4b8f83b42`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 40.4 KB (40388 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:0723e618fbb73c4e4fb85dd8db1b94031aaf96d39954e6e66d7a7ce82b32f74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.6 MB (404648844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec167ad0e8d996730439ac291a9114b03863932e5908f69735fb0bf73faf7def`
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
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Sep 2024 16:37:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T12:15:21.436Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T12:15:21.436Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdedf750a744afb7e0b04b26877aee1247d6f9ea65ba56552f24a1e9924a4a8f`  
		Last Modified: Sat, 17 Aug 2024 02:58:25 GMT  
		Size: 10.8 MB (10797079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d67bbe7b6b7cf2f5aa1b7074695ee58bdfbb78703ae71443d4a2399b2772950`  
		Last Modified: Thu, 05 Sep 2024 22:19:44 GMT  
		Size: 351.2 MB (351211846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad594e431daa16b323ee60eaa4a41bb2712e36d6abb364a2241d98d9f3d6ccb`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a6c171b38d01f72d4ea8f5248aca5bfc24c14358e647a9919026bd3e04021`  
		Last Modified: Thu, 05 Sep 2024 22:19:37 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca544c9570d1048f3e9bbd6be835c61deb7bc868a4e6906859644370737c530b`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 5.3 KB (5298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd8aae931d61ddfff3a278853ab881df32709bdf8dc383cbe3959e5eb1d1da4`  
		Last Modified: Thu, 05 Sep 2024 22:19:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb61633fd72db7111f7b16095a54e20aaf28c97ec71bc98706055df82c800771`  
		Last Modified: Thu, 05 Sep 2024 22:19:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603599a53019ffbb9514220fdf858648d0c35bf7a55db356819c3f0d590d5c92`  
		Last Modified: Thu, 05 Sep 2024 22:19:38 GMT  
		Size: 4.6 KB (4629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf6ba2a0bb454ff9eef46c7bd1c4f9b6ae0acd28cdb12ed6983c6de8177248a`  
		Last Modified: Thu, 05 Sep 2024 22:19:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08571e2eb63d047e75cd36fd4f48645ff2899d5c6da2df30093e30e748a9d76`  
		Last Modified: Thu, 05 Sep 2024 22:19:38 GMT  
		Size: 183.4 KB (183421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f24bc4a7595e6c6fe9e52b3f6d21d7efd3126096fe17475da1a23c631c6cb`  
		Last Modified: Thu, 05 Sep 2024 22:19:39 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.1` - unknown; unknown

```console
$ docker pull kibana@sha256:fccf0bf0652985000c9ada30b61f1ec3e0de4327c272e9e38943aeaea0a9f891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4104481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c261549449f8b65a1e1338bb85124133f418caa2728ccc4d3870a73107f67483`

```dockerfile
```

-	Layers:
	-	`sha256:cd2717e09601bc29b2b62d5caf5bb9cc2cbc39df3d3060788924df14f0c7a859`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 4.1 MB (4063829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cecb08a450809924cae3019c818a66407f573cf16955ac96992a8093f2f03a6`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 40.7 KB (40652 bytes)  
		MIME: application/vnd.in-toto+json
