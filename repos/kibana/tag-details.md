<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.21`](#kibana71721)
-	[`kibana:8.14.0`](#kibana8140)

## `kibana:7.17.21`

```console
$ docker pull kibana@sha256:014bf4b7b88ae4aabbfbafc7542be1498b4672883bcf9bdc3581d433d030a75c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.21` - linux; amd64

```console
$ docker pull kibana@sha256:7e8044dd46b780b3d1a359c582a08ac2c4fc79cd7bb9a1aa65b689c0ec600ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360365633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ba65263d34f5368264e4683b060668547dcaf8f4381baf60f70631f7c82d1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 02 May 2024 09:08:49 GMT
ARG RELEASE
# Thu, 02 May 2024 09:08:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 May 2024 09:08:49 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 May 2024 09:08:49 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN fc-cache -v # buildkit
# Thu, 02 May 2024 09:08:49 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/kibana
# Thu, 02 May 2024 09:08:49 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.build-date=2024-04-25T11:06:50.254Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=34995fdf7c8c448c6fc99cd0a5e50c88479ff59f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.21 org.opencontainers.image.created=2024-04-25T11:06:50.254Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=34995fdf7c8c448c6fc99cd0a5e50c88479ff59f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.21
# Thu, 02 May 2024 09:08:49 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 02 May 2024 09:08:49 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 02 May 2024 09:08:49 GMT
USER kibana
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312aa48f7b4ee91f171ee09811c2fe1f37e2068886935d44d2b41766b6e122b1`  
		Last Modified: Wed, 05 Jun 2024 02:21:41 GMT  
		Size: 10.7 MB (10705104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c050d99f3658f9e3a3299edf30c7e904640a1ca0d4923f1d43414d08a043c07e`  
		Last Modified: Wed, 05 Jun 2024 02:21:41 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5753f5ee37255cb9e15be25a6b23458cf9b37cca12f4be0b2f138be87ab091`  
		Last Modified: Wed, 05 Jun 2024 02:21:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b208f0413e5f38f4299bd84c92ddadab75b815322e919e781a374eba25063b1`  
		Last Modified: Wed, 05 Jun 2024 02:21:41 GMT  
		Size: 16.5 MB (16460474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e667b621110cf3cde76a356ddd831ef6c5977596fb567ef1f27fa669194a1721`  
		Last Modified: Wed, 05 Jun 2024 02:21:42 GMT  
		Size: 5.3 KB (5283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a84a86ff950923e674f30cd46fd1a0acab7505067f3ab03ad3985725ca6acbd`  
		Last Modified: Wed, 05 Jun 2024 02:21:47 GMT  
		Size: 305.5 MB (305476839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55491e307fca45936c7b4aacf92dd897e117129cd9173c9a8cc37b48ecc5afdd`  
		Last Modified: Wed, 05 Jun 2024 02:21:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed3ce3887f1951054883994ed051a27640fc515ad377d7e522e7863194dc801`  
		Last Modified: Wed, 05 Jun 2024 02:21:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79273b67f96ce2159bf0b1ac8eac0d576a5f34690beb661279a4751604192a4`  
		Last Modified: Wed, 05 Jun 2024 02:21:43 GMT  
		Size: 4.5 KB (4509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76247bf50a213f4f971700eb03080567b726cf7608d4d7703125aa70d65b523`  
		Last Modified: Wed, 05 Jun 2024 02:21:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8502542d4aa6fce490bb0f0329ac69ab079b3a635e8029458ad69755a12fe1f9`  
		Last Modified: Wed, 05 Jun 2024 02:21:43 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ad10cdcb41af1f939d375510f6cac9f81e23c09dac9f6fb0c080f578eaa176`  
		Last Modified: Wed, 05 Jun 2024 02:21:44 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.21` - unknown; unknown

```console
$ docker pull kibana@sha256:194078a414084becebabfdf9a6fb3250f9f3ca2df919f421cfce723d63cefe5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3333187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955c937f9af852640a7247a5e240aefb07e2f6d2b0234b1623bb9f3e41b6e6c6`

```dockerfile
```

-	Layers:
	-	`sha256:39ed7b6544bb9635285db35caeaa2bbf64ad83fa1d0db1b0a58b6c25935768cf`  
		Last Modified: Wed, 05 Jun 2024 02:21:41 GMT  
		Size: 3.3 MB (3288981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e09daea39aaf27c1559a7b66aed08dcb26d6b61f84bd0c6248b09f39970828a`  
		Last Modified: Wed, 05 Jun 2024 02:21:41 GMT  
		Size: 44.2 KB (44206 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.21` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:49253056f15a799dc966ac949d0289943a0a5171577c0abc18c2de198b66fd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.8 MB (370803718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89fbc555e735f0f2908e1992a58b703365dabd961f7b5f61fea4dc511524dac`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 02 May 2024 09:08:49 GMT
ARG RELEASE
# Thu, 02 May 2024 09:08:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 May 2024 09:08:49 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 May 2024 09:08:49 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN fc-cache -v # buildkit
# Thu, 02 May 2024 09:08:49 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/kibana
# Thu, 02 May 2024 09:08:49 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.build-date=2024-04-25T11:06:50.254Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=34995fdf7c8c448c6fc99cd0a5e50c88479ff59f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.21 org.opencontainers.image.created=2024-04-25T11:06:50.254Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=34995fdf7c8c448c6fc99cd0a5e50c88479ff59f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.21
# Thu, 02 May 2024 09:08:49 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 02 May 2024 09:08:49 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 02 May 2024 09:08:49 GMT
USER kibana
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dd30ab58335cfc64b8644d22d1edf54b10726a5dd7eb89ff73ee78013860a`  
		Last Modified: Wed, 05 Jun 2024 16:01:43 GMT  
		Size: 10.6 MB (10550719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395764de8c16ca9fdf511b85693276262681625012db63283350548fb437524d`  
		Last Modified: Wed, 05 Jun 2024 16:01:43 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3687c8f64db803aba5cbbdd491fb195b22f7771198fced7b8167373e2ba0d617`  
		Last Modified: Wed, 05 Jun 2024 16:01:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab0c1d5f43e5ebd3d0f4cdff9ceb5aefa40137e177b9517e2383c2ec0c82f99`  
		Last Modified: Wed, 05 Jun 2024 16:01:44 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409b485e7538528aec5d9dd7a45870c294c0784478c9884441494df4431da66f`  
		Last Modified: Wed, 05 Jun 2024 16:01:44 GMT  
		Size: 5.3 KB (5286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035a14431d5d04080d0b6cb2e546aca3a4f8df1a95f2c6c69782df52c21f6ea`  
		Last Modified: Wed, 05 Jun 2024 16:05:55 GMT  
		Size: 317.6 MB (317613283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adcbf784db434d6c8ef63bc3f592db8bb02bb676f2ea209c590cf8eb1d0ae18`  
		Last Modified: Wed, 05 Jun 2024 16:05:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2426871a4244a2fcdf1db29c49e7e6ce20ccb8dc75ecdde3d44054bbd4f00e96`  
		Last Modified: Wed, 05 Jun 2024 16:05:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d69e4285de2c51f56510ac1c171e6885665dbbf5d3eba0561e288f4aaac063`  
		Last Modified: Wed, 05 Jun 2024 16:05:48 GMT  
		Size: 4.5 KB (4507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eeb94877d3d6136da0703451df22a18f2323beab455f613aca61649d0803f32`  
		Last Modified: Wed, 05 Jun 2024 16:05:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9857a80288b1e7330fd7d3c833a9aa1df38c9a722a52796dee4a4835ef22b9`  
		Last Modified: Wed, 05 Jun 2024 16:01:47 GMT  
		Size: 183.4 KB (183420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1ef622469d1f4789169f87e4867349e6a7d83043b41b1c299d3a79ea8056b0`  
		Last Modified: Wed, 05 Jun 2024 16:05:49 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.21` - unknown; unknown

```console
$ docker pull kibana@sha256:c9df29f18e9cedb2f8e0819d724eb0511de63b1dad58adcdfe1d867e7e40a117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3333702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8492c8160bc3be782ae3ddc789ed2540a536be95178015768e2c813b23868bc7`

```dockerfile
```

-	Layers:
	-	`sha256:053387176c0eec57e92bab6f1c44d2946b98b63c493687fac104c55172ce0812`  
		Last Modified: Wed, 05 Jun 2024 16:05:48 GMT  
		Size: 3.3 MB (3289231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d1b81f01547b8bcdebbbafa3d67c0ab5830e6c5d2b08ec66e014548ab046a3`  
		Last Modified: Wed, 05 Jun 2024 16:05:48 GMT  
		Size: 44.5 KB (44471 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.14.0`

**does not exist** (yet?)
