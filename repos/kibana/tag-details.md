<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.21`](#kibana71721)
-	[`kibana:8.13.4`](#kibana8134)

## `kibana:7.17.21`

```console
$ docker pull kibana@sha256:00b785bb827cabf10be518ee03958fe233ba3a1f906ba18a6534dcc02f6c0da6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.21` - linux; amd64

```console
$ docker pull kibana@sha256:3446f43cc2641400c67ee5f741d8f7c6c2594be7c8716a3968dc47fb63ae5104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360365833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39466964d27dbc2595e40a2575f09745be4d35d5046e34ef6b6d359b7c8054f6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
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
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71775f1fd40f423435dbd21f768d0ba868750f26db366b74f20a95aae955c96a`  
		Last Modified: Thu, 02 May 2024 17:54:10 GMT  
		Size: 10.7 MB (10705170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5a3429f635f2ac1db852652eaf48c9b4cd33244d5952b423739ac5c95be204`  
		Last Modified: Thu, 02 May 2024 17:54:10 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20ecd01ab8464aaa811d2d14113d393178f12bf8825b220bf9578db9efbf2a9`  
		Last Modified: Thu, 02 May 2024 17:54:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7bd5b4e7bc89b716277ab19d8851ff4c1c1da2766d7a772a1e37ef09e020c0`  
		Last Modified: Thu, 02 May 2024 17:54:10 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9d658c9d210a10cf0056eec03de404468381589ef188e69bef68e4b7e09f08`  
		Last Modified: Thu, 02 May 2024 17:54:11 GMT  
		Size: 5.3 KB (5274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa2067b1a12366cb56ca660754ebff84735689749f4296203d5370e30ff645a`  
		Last Modified: Thu, 02 May 2024 17:54:16 GMT  
		Size: 305.5 MB (305476828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d56bbfc1c2526f01103fd0ca71af7e15ccbc522785158eb5987b6156231989`  
		Last Modified: Thu, 02 May 2024 17:54:11 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2258c9e30211b2743a8073435fd015da57205c19a85a086af77cf50a77bcdd4e`  
		Last Modified: Thu, 02 May 2024 17:54:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28bc7b9b72fa093ed5f010ba94755fd929ed631945a0cf866bf4b7573216820`  
		Last Modified: Thu, 02 May 2024 17:54:12 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37481891bc24535bec2498b97d0f69a4a2ef08565fb97353545e4985174293c8`  
		Last Modified: Thu, 02 May 2024 17:54:12 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a48e71c12feb2bd4f69a076bca84f0cc94f53707c92f84d13397cd55480fd`  
		Last Modified: Thu, 02 May 2024 17:54:13 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790e2a978a5fec87737fbc0c4bc2a7de62f67fa6b539258963420de76b6adc5d`  
		Last Modified: Thu, 02 May 2024 17:54:13 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.21` - unknown; unknown

```console
$ docker pull kibana@sha256:bb0d96a3d78a540cdb35146381d0d87b6bd260b97f16e879784dae781e0cab3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3333348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57522a8261c0b6cb4f4c12fd53fbbac1d52bb3c4108f8299cb8b298dcf9e6c7`

```dockerfile
```

-	Layers:
	-	`sha256:ad4efe939837b30dad6f29d2f55ac96f8682279087b2916a92952a697b48a9a4`  
		Last Modified: Thu, 02 May 2024 17:54:10 GMT  
		Size: 3.3 MB (3288982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5925714b001c8ce2c8c4efb7924f5041c98f29666dc3f477647ba3ffb744bd`  
		Last Modified: Thu, 02 May 2024 17:54:10 GMT  
		Size: 44.4 KB (44366 bytes)  
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
$ docker pull kibana@sha256:21a0ad710669c7b58c45c98dc4fedf094e90bd0f3662daaadfbe740ad95d527d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.13.4` - linux; amd64

```console
$ docker pull kibana@sha256:867f43755b59e99d315b77636eee4b571be3f6f5dcfe7e1664bb30e9848c774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.5 MB (375494398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3841349081b176ba0ff24f44eab8c9446125d5cf55e1ad76e07a18ee168b6bd8`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
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
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da73621b4fa09b3675e40a10a1f5ac065de4ed3194fc0b50d35ad3b46124aeec`  
		Last Modified: Thu, 09 May 2024 16:53:42 GMT  
		Size: 10.7 MB (10705158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baee0904631143d2205ccb893b55f8a5e55401b053b9670fd82093bbcbcf315`  
		Last Modified: Thu, 09 May 2024 16:53:41 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904b2227dc0a2aba2fbcede31f428801352815d75e9621b87875791d054f0da3`  
		Last Modified: Thu, 09 May 2024 16:53:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c7cfd88e1e40cccb312dbcac1669dd63bed4a89b8a402dd019ec2cc41346da`  
		Last Modified: Thu, 09 May 2024 16:53:43 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3bfd36dbb21327a6e7787e5f17ed3f058a255d22507f89df7d24c7a3fd1e19`  
		Last Modified: Thu, 09 May 2024 16:53:43 GMT  
		Size: 5.3 KB (5281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0328104ab0d30375473151f51654d96f670f0da001392d349f382e5ed458bcae`  
		Last Modified: Thu, 09 May 2024 16:53:50 GMT  
		Size: 320.6 MB (320605350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54153adb390a3d56fcf55d998b8fab5321bce027ace8d20565aeb3d57820620`  
		Last Modified: Thu, 09 May 2024 16:53:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557f3a4c13277299b682dec567a6d607e3325206973748517117d702eab1cea`  
		Last Modified: Thu, 09 May 2024 16:53:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dcedb2bb9251da20f2b4cf23f9f8bca14ecfd565f8599684dc1926449ece40`  
		Last Modified: Thu, 09 May 2024 16:53:44 GMT  
		Size: 4.6 KB (4561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd70a2df6b35f397d0a15fe8f5c7e192faa0d60e7b062d87f4425f955b509b`  
		Last Modified: Thu, 09 May 2024 16:53:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b939aa9da44c3e3d7f8911a54cd482647d5b942c0e73b3943743f8b041cee5`  
		Last Modified: Thu, 09 May 2024 16:53:46 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eced73f704b7a8eb9f2c224ad76094cb65a91944d7c2ccddfd2479ab3069e5a7`  
		Last Modified: Thu, 09 May 2024 16:53:45 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.4` - unknown; unknown

```console
$ docker pull kibana@sha256:1369729e969481e75df31a88f8eeb5563a54eec636b71437668101cacac4bdf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb41f8d9aacf41d31b8dbdce402ef55f2d923b85b32e40d0aea30aebe4c5914`

```dockerfile
```

-	Layers:
	-	`sha256:a67672720103074ceae6bb837140f9384b6cb631cd9918470ac800a042c177da`  
		Last Modified: Thu, 09 May 2024 16:53:42 GMT  
		Size: 3.8 MB (3750714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65a9846afeca3d81db75f09f8b2319290a5577016fd99e3384c10b82e4ef51e5`  
		Last Modified: Thu, 09 May 2024 16:53:42 GMT  
		Size: 44.4 KB (44356 bytes)  
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
