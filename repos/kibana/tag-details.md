<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.21`](#kibana71721)
-	[`kibana:8.13.4`](#kibana8134)

## `kibana:7.17.21`

```console
$ docker pull kibana@sha256:613a77917f39b93366dc523e98498b694f1fc847f6c3b2fbf074d34922d5a08e
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
$ docker pull kibana@sha256:23b7547716bc429cc0a7926b5082ff91ea4a75d017d935ac4920abe98e8b0a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.8 MB (370805735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba387265d6e38adb2886713f9a7a3038fc001b8814fa616604e93663364e7b93`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
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
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5d0d7c21ea60411e55b5523a8c2187d18bdec3a452c21708763f047bfb0ab`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 10.6 MB (10551305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18e95a4c15f82e6a2ac8d591656086912c243007fb37271b41c0b56b4acea9c`  
		Last Modified: Thu, 02 May 2024 11:35:08 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186b8a3459f0195c0081dd1a0707dda8a8c2606672c2983a5c8aaf3c94965886`  
		Last Modified: Thu, 02 May 2024 11:35:08 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fac697f917cf0cf446f4ee231c25c900de2df2e197c64cbf2fa49b9694286f`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ca2e6e15fcf3aff8c1472becdef226c9d51ab526713ff496da3141f45747`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 5.3 KB (5295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bcb8bca4cc043fd4bfc6205b461eedaf995b1460cf71fed13b2f0f30632954`  
		Last Modified: Thu, 02 May 2024 18:16:23 GMT  
		Size: 317.6 MB (317613165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39da5b2e2827144f654bf73336d9850d2300d2a2b9437b41ad3dee97c9604dd4`  
		Last Modified: Thu, 02 May 2024 18:16:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4cfb4674930155ad2ebfacb7b7169951f2eec953a345428c685825de61e087`  
		Last Modified: Thu, 02 May 2024 18:16:16 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4dbc714ecd9e6678ab65209210e4591fd58368f1ff116937d4a00320ee8ff2`  
		Last Modified: Thu, 02 May 2024 18:16:16 GMT  
		Size: 4.5 KB (4507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e18d0b90bc6c1ad4ea07492531ac202ae824660f76403adf48f1a287cdfb6fe`  
		Last Modified: Thu, 02 May 2024 18:16:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd6773c4f2bb7bc0ba0a6fa4feabda35bc679a19f306e638aedd38884a9b55`  
		Last Modified: Thu, 02 May 2024 11:35:12 GMT  
		Size: 183.4 KB (183419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c3c5e70889512b2c58eb71253584f22fde74939e396a6cc8326a195579b7a`  
		Last Modified: Thu, 02 May 2024 18:16:17 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.21` - unknown; unknown

```console
$ docker pull kibana@sha256:db1d3566d1893e8494eb9aeb829cc5f0b78c3d7eb72409244257c7d408816173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3333427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a89fcc37adad443a5a2b28fbad9831cdb334312bcac50b5025b602039122f0a`

```dockerfile
```

-	Layers:
	-	`sha256:1c77fa7af94f033c1b139605a5729b2553f8c1ad2eb66e79842b9c9d0fb3fabb`  
		Last Modified: Thu, 02 May 2024 18:16:16 GMT  
		Size: 3.3 MB (3289217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1978bc4fa56a5663e65c65073ddfcdadcd323275b5affddf6836cf5337dcba6d`  
		Last Modified: Thu, 02 May 2024 18:16:16 GMT  
		Size: 44.2 KB (44210 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.13.4`

```console
$ docker pull kibana@sha256:ce2870a222226888d93dda2d5aba865bbc8a38df51fe1a3f607537362ad392d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.13.4` - linux; amd64

```console
$ docker pull kibana@sha256:918658904074a07dc98cbc0a3e97ad8f3644a62c5a18a196cab4760a9c87cf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.5 MB (375494243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40f2a312340150aee47a796198457fc83f5e80bd27fe1a2c27a500527438c19`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 09 May 2024 12:07:29 GMT
ARG RELEASE
# Thu, 09 May 2024 12:07:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 09 May 2024 12:07:29 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 09 May 2024 12:07:29 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 12:07:29 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 09 May 2024 12:07:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN fc-cache -v # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 09 May 2024 12:07:29 GMT
WORKDIR /usr/share/kibana
# Thu, 09 May 2024 12:07:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 09 May 2024 12:07:29 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 May 2024 12:07:29 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 12:07:29 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.label-schema.build-date=2024-05-07T06:06:37.059Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f5dc24d1969f80e4aa3ced7cc375dd00554f8c0c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.4 org.opencontainers.image.created=2024-05-07T06:06:37.059Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f5dc24d1969f80e4aa3ced7cc375dd00554f8c0c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.4
# Thu, 09 May 2024 12:07:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 09 May 2024 12:07:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 09 May 2024 12:07:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b142321a1406b42d7ebee644b17ed19fc86ed0e72f5edabde4a24ded5cd57ad`  
		Last Modified: Wed, 05 Jun 2024 02:22:38 GMT  
		Size: 10.7 MB (10705130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84a47e2a11d149be94ffc2cb5ab7ee35581d6a59753335b80c3af4c2f834117`  
		Last Modified: Wed, 05 Jun 2024 02:22:37 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0633792c7346a434c08f53b9b2d6768a8a04535bee875cd8ef6c0b923f1358ae`  
		Last Modified: Wed, 05 Jun 2024 02:22:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6211d695c286fb64810b79bf05f25b333400438e8ac5fbfac72dbe80c8afc4a9`  
		Last Modified: Wed, 05 Jun 2024 02:22:38 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc4f538720a61754e0962396a1488951e8d82db745da0bd239083e4f8967383`  
		Last Modified: Wed, 05 Jun 2024 02:22:38 GMT  
		Size: 5.3 KB (5285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803ab97fbbe4352d707c600685a6f05808f748f8cec3a3f2a11fe66f7b4c29a3`  
		Last Modified: Wed, 05 Jun 2024 02:22:43 GMT  
		Size: 320.6 MB (320605349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7d73dfbe7837fba62283e6a9cbcc6ab82e8d0ab6405bd5af3f53a4fcb9435`  
		Last Modified: Wed, 05 Jun 2024 02:22:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07450b6874be23a11b58b258fd8398c987c205438f79b60b849a1c6698628a`  
		Last Modified: Wed, 05 Jun 2024 02:22:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d652eb4f1a89abe02ae3a0a3e2cb14c449ce89dc0fd5c5059213a957ff1a5278`  
		Last Modified: Wed, 05 Jun 2024 02:22:39 GMT  
		Size: 4.6 KB (4569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a398b78a855d778b616d85f945442cfb1929d755f4937d55af79293c292db9`  
		Last Modified: Wed, 05 Jun 2024 02:22:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c10b3ff45508d639830ed897b61263eeda04cb0c04a1686ac32b682d550ab`  
		Last Modified: Wed, 05 Jun 2024 02:22:40 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aedb50e7488339d715c54f0598ca59c71d42359e28b952ef415d3ba2bee37e`  
		Last Modified: Wed, 05 Jun 2024 02:22:40 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.4` - unknown; unknown

```console
$ docker pull kibana@sha256:db0d03c8263b574db686e2c4aea0aaa40671b82929b150631f00d0847d1b7ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d477e9ce85384ba7c6eb111613d45e3bfc4b57175971f2946654f9e63e3251`

```dockerfile
```

-	Layers:
	-	`sha256:b3f96ecd4d2f8029864561e9d193590c4164d429126884069c73dcb376b29cbe`  
		Last Modified: Wed, 05 Jun 2024 02:22:37 GMT  
		Size: 3.8 MB (3750713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:649596455a6ee9d0b395ec5e638186adef420f3cee0b63de17c02b7fccd134ac`  
		Last Modified: Wed, 05 Jun 2024 02:22:37 GMT  
		Size: 44.2 KB (44194 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.13.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:3eab194f1d116c1c1f5350bece3b1fc78719c5c5bd312927d9dceab29f2a11b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385953397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a012a971b782c8555b3f1810bbca08a409404eb5c01ba35c7df2e48ee3793723`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 12:07:29 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 09 May 2024 12:07:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN fc-cache -v # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 09 May 2024 12:07:29 GMT
WORKDIR /usr/share/kibana
# Thu, 09 May 2024 12:07:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 09 May 2024 12:07:29 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 09 May 2024 12:07:29 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 12:07:29 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 09 May 2024 12:07:29 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 09 May 2024 12:07:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 09 May 2024 12:07:29 GMT
LABEL org.label-schema.build-date=2024-05-07T06:06:37.059Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f5dc24d1969f80e4aa3ced7cc375dd00554f8c0c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.4 org.opencontainers.image.created=2024-05-07T06:06:37.059Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f5dc24d1969f80e4aa3ced7cc375dd00554f8c0c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.4
# Thu, 09 May 2024 12:07:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 09 May 2024 12:07:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 09 May 2024 12:07:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9025500d85a9bf329bc14d2d340eb505bfb045889254867b416ef3a7a7db67`  
		Last Modified: Wed, 08 May 2024 00:20:36 GMT  
		Size: 10.6 MB (10551265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9027e5ceb1f554ce50aba75f67d5b6e7ec51592fcaf7d09365d66e4d9b0a5429`  
		Last Modified: Wed, 08 May 2024 00:20:35 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd38fda06da71bad9ce94880d2d79562967f1e4b9f9c76fa2ec9b6b3052f5a9`  
		Last Modified: Wed, 08 May 2024 00:20:35 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8894f79c60ec5aa0c4a60ea932c1c7e82bc47e635125643035748b7cb94d6840`  
		Last Modified: Wed, 08 May 2024 00:20:36 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cce534f56a6a0a0fedf16e350b6e2b0ce91f478ccc7e011e2b42b3b7458e7f`  
		Last Modified: Wed, 08 May 2024 00:20:36 GMT  
		Size: 5.3 KB (5279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b79ba0edf57d6c8eb7df20aef6c1765c8a6f45d5e368d2a858d650392b66f`  
		Last Modified: Thu, 09 May 2024 17:21:33 GMT  
		Size: 332.8 MB (332760825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1767574bb0c0f2062c4d93b9874b3f016795ae0cbb61d57535940b9af2a3cc`  
		Last Modified: Thu, 09 May 2024 17:21:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcaa20530712ced2861ba3c40de711bdb4bea32d5e354af4b17871e497ebf1`  
		Last Modified: Thu, 09 May 2024 17:21:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc27945b58d9b2a3c5c60469eebd86e88ea4c13725266c19fc7ead867cd618f`  
		Last Modified: Thu, 09 May 2024 17:21:26 GMT  
		Size: 4.6 KB (4563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ac05d259965a877eeb837439312aa9487bc473167905ecb78c341f233351a4`  
		Last Modified: Thu, 09 May 2024 17:21:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65910ea13ff29423406a890f4a707cd41b5e291df17bbdc6e908b98e0af1dacf`  
		Last Modified: Wed, 08 May 2024 00:20:39 GMT  
		Size: 183.4 KB (183420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af15deef2148abf204baca78506de942cc60a1061de42cbab6cd6eaca27a74`  
		Last Modified: Thu, 09 May 2024 17:21:27 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.4` - unknown; unknown

```console
$ docker pull kibana@sha256:7550e93b6ba7975a80daf8956b55f001db2add5a1597ffed7cab13089dd7f0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ce70ac44448cab6e1f5e5ad28f9ddd509fef1bc977d994273161b23dda0f4`

```dockerfile
```

-	Layers:
	-	`sha256:63b5165908f6eff84fa17ec2786069f4863809fed2bb299406ad0a8951ffc0e6`  
		Last Modified: Thu, 09 May 2024 17:21:26 GMT  
		Size: 3.8 MB (3750949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402e6896e5972c60ffeab27b74e75ac80bb6a1ab1cd63b25af6d0842f5efc73b`  
		Last Modified: Thu, 09 May 2024 17:21:26 GMT  
		Size: 44.4 KB (44360 bytes)  
		MIME: application/vnd.in-toto+json
