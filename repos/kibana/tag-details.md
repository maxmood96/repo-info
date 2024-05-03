<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.21`](#kibana71721)
-	[`kibana:8.13.0`](#kibana8130)

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

## `kibana:8.13.0`

```console
$ docker pull kibana@sha256:d713b80cdb02c0dd484de9bbbac2312e7dab98f09a25b6adbbfa30841649b828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.13.0` - linux; amd64

```console
$ docker pull kibana@sha256:d43324e676cbd2d2178a29057223bde6013dfee55d09d4ddba17e9013e78a6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.1 MB (375053138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c1f896185badaecfa762da47458d0a32f331944b16e7d985e9300b31ad9807`
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
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
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
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9270f90453da34504c79124531d40b33decfcb048adc94ff1819d8570d7f72`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 10.7 MB (10705183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ee893e59a1a2d7fee8d90f81f61106159bc44e98327014963b7736bef51b92`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae1b253504a71c4529f6b2e7c1d5fcf256146fd64f282238c82c4b5ae998823`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeee51ecc63805a655f2ab121c976279751ce4472b50560b299fe84aee5dac1b`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2500363d16446137ed52467eae89732ac2ba2ef4f35740d9fbeb31fb76efbca`  
		Last Modified: Thu, 02 May 2024 00:54:40 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cb78aa516972699c3403452c24911660ce4c70b170093e660a9356af09455c`  
		Last Modified: Thu, 02 May 2024 00:54:44 GMT  
		Size: 320.2 MB (320164065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f065f373ad833ce464887751cf63c6b5d93ef1c4bc616ca70bdebcbb6fb5af97`  
		Last Modified: Thu, 02 May 2024 00:54:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fbb338f026b9e8e7b987fce14b56690a496894ff8777430684f6b8bcb748f5`  
		Last Modified: Thu, 02 May 2024 00:54:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f21d8fb616536b5c54722ba30fed6d5f02b7085ff7294987a7e0ca1c7fd80`  
		Last Modified: Thu, 02 May 2024 00:54:41 GMT  
		Size: 4.6 KB (4563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7499fcd7ec800bb3cd3cc4072492a6639d91a7f6ee3a2027127c0e5ffe13b65d`  
		Last Modified: Thu, 02 May 2024 00:54:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd916f8c3f7f388d2bd0444c3d92a2e88d80d6ed7bac2583fa9a2dc26ee641b6`  
		Last Modified: Thu, 02 May 2024 00:54:41 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c5146376b1e2cabcb6d6298abd9bf983b472e29b0f5962a77092c2936a33d`  
		Last Modified: Thu, 02 May 2024 00:54:41 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:c782351cef46b06a4dbfd40a76d825a75a7f929dddbcaeea8c13b0a98555a81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465541209b81d0c3e557ee48adca5bccda750eed990876c97086518fa6c57b5`

```dockerfile
```

-	Layers:
	-	`sha256:63babf3416dc9d0d0ba89165b5228055bd7b66edf93a650d21f1b928b1673644`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 3.7 MB (3749657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f500da12478a9dcff4a04969877344e3db799d8f543f98f4b9640cd8d717002`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 44.4 KB (44356 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.13.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9dfc2e86ca0e4a7528ef632844456774bf787f9870036017e235ada77408c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385487015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0fe852981d370c7eb7db96c5990336fb44c723062458b5b6e86a49d8db9b2c`
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
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
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
	-	`sha256:e5c55329d5b58905918d9c2d6aa17a2d52e864271b6e89b77dd6aa95b7102f72`  
		Last Modified: Thu, 02 May 2024 11:35:17 GMT  
		Size: 332.3 MB (332294389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed089e73d0dfc0bdc9b35ae240b644b4b8c2e5a5054eeaba1c951f4056442c57`  
		Last Modified: Thu, 02 May 2024 11:35:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3e6ae72d42eb86957f8cb3e4f57276a82bf37cc1899bdac8ba07ae88971340`  
		Last Modified: Thu, 02 May 2024 11:35:10 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b1007d14653d31f4c62bc30f0d8004be33697d5d67efc67fd0a37941c857b`  
		Last Modified: Thu, 02 May 2024 11:35:11 GMT  
		Size: 4.6 KB (4565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a75345761143d942361dd5e6fc02d1c5b23c41ea7ae81671b7db90517974b`  
		Last Modified: Thu, 02 May 2024 11:35:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd6773c4f2bb7bc0ba0a6fa4feabda35bc679a19f306e638aedd38884a9b55`  
		Last Modified: Thu, 02 May 2024 11:35:12 GMT  
		Size: 183.4 KB (183419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7011dcb4f45a13db5835a2caadac9c2a860e1f2f4dc467e68b892c1b35d13a61`  
		Last Modified: Thu, 02 May 2024 11:35:12 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:12b10d082822f3225367a549b65c7b6f99034a845f789d30bd376b6c66f40050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8a5866c3c54fb0f8d64be40e18bbb6060348b50616faa3b6e93b9107296912`

```dockerfile
```

-	Layers:
	-	`sha256:22ba0cfeb662c7bf269170a6c4f87242d1346f8c74ea8de706f002d84470947d`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 3.7 MB (3749892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44e66ceb8c4bb894e0859e6b8077d4c0a19d76eb6eec07bce0237b1e78b775e`  
		Last Modified: Thu, 02 May 2024 11:35:08 GMT  
		Size: 44.2 KB (44199 bytes)  
		MIME: application/vnd.in-toto+json
