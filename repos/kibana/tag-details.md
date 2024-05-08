<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.21`](#kibana71721)
-	[`kibana:8.13.3`](#kibana8133)

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

## `kibana:8.13.3`

```console
$ docker pull kibana@sha256:86ad1df55642cf3863c059b8bfb3128c064c5aebf48201da89580317a8630a8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.13.3` - linux; amd64

```console
$ docker pull kibana@sha256:d5b3d6cae6021b489168bd38b643ee85e5d188fbf105a0a88a3db5f5de6a70d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.5 MB (375497431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23ae10d6842f6586358dc2bb129742bec45d5ef15f529855a3c8eb7424355d5`
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
# Thu, 02 May 2024 17:24:52 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 02 May 2024 17:24:52 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN fc-cache -v # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 02 May 2024 17:24:52 GMT
WORKDIR /usr/share/kibana
# Thu, 02 May 2024 17:24:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 02 May 2024 17:24:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 17:24:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 17:24:52 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 02 May 2024 17:24:52 GMT
LABEL org.label-schema.build-date=2024-04-30T02:06:44.402Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=003e4a42946390c2eb93dfb3586498ce7520a530 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.3 org.opencontainers.image.created=2024-04-30T02:06:44.402Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=003e4a42946390c2eb93dfb3586498ce7520a530 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.3
# Thu, 02 May 2024 17:24:52 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 02 May 2024 17:24:52 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 02 May 2024 17:24:52 GMT
USER 1000
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ef69d85b58295510421513b4a3842edefa6037f7334f14cc9d650540cd04b2`  
		Last Modified: Tue, 07 May 2024 21:55:00 GMT  
		Size: 10.7 MB (10705198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dc2ff646eab29507d270d39d111af45a3748bf0d809c8c3fe75af7550c14a6`  
		Last Modified: Tue, 07 May 2024 21:55:00 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a369ff0f0c51ca283c1a39a92436d005a4a974ffa4954ec13d836f0824bcc4b0`  
		Last Modified: Tue, 07 May 2024 21:55:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f541e20163f45cd026d6ef4b163401ea645593cc0ae961f81976cf5b0ac9ee0`  
		Last Modified: Tue, 07 May 2024 21:55:00 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264a5c39e1b90804dc45eadb367ab74be946d184cc388ed51da8b4de99c843fc`  
		Last Modified: Tue, 07 May 2024 21:55:01 GMT  
		Size: 5.3 KB (5292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21204cf5283b4a4a273830fdbb1800e99a51642f387bfc5b822d030577e12075`  
		Last Modified: Tue, 07 May 2024 21:55:06 GMT  
		Size: 320.6 MB (320608323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6477f3dee952b05d7154a2fbbc7468f670368deec41080a082e5c7b9c085a820`  
		Last Modified: Tue, 07 May 2024 21:55:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbde6dc9a9013661d0645831f3fabb0c5ee68dee0ccb4ddf9dd56ee7fd4c1c0e`  
		Last Modified: Tue, 07 May 2024 21:55:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ab68e31c764aac43b2d0df34d134742aaa4239215a5f468abfceeb57efd166`  
		Last Modified: Tue, 07 May 2024 21:55:02 GMT  
		Size: 4.6 KB (4562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a5148f0c8efcba8a3e2936ad159a3ac56c4fcc08c26b06fbfb35b500294ead`  
		Last Modified: Tue, 07 May 2024 21:55:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304c4d84c240c6c5171da60247dd6998ee67ce597b618896ad745de856eec9e2`  
		Last Modified: Tue, 07 May 2024 21:55:03 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c30f31313b8b85822222ca0834821d5358245e480d4511b34189eb482e9e0d`  
		Last Modified: Tue, 07 May 2024 21:55:03 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.3` - unknown; unknown

```console
$ docker pull kibana@sha256:38c46df24eec48037c6168dcf9d7134d83b13bf9964639b1141611275b64e255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befad0f18c7eba354fbc74a4d141b1a8b8f42e0188c0a8df8a674ed627c0fa0e`

```dockerfile
```

-	Layers:
	-	`sha256:7fe1b75137ee7f87fa26d4330bfdc7c8199b1d30dee2036dc02ea7526a9bb907`  
		Last Modified: Tue, 07 May 2024 21:55:00 GMT  
		Size: 3.8 MB (3750714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ea39bdf298ce2ce967e78595d91f0c6f30ca105332fa4a652eca4908c50ce57`  
		Last Modified: Tue, 07 May 2024 21:55:00 GMT  
		Size: 44.4 KB (44356 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.13.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:cd2b7405cdac50da59f8d49993799b2a91426dfcb01297ed34a88e4841b7c4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385953269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1653fcaa643b9f6d97f26384761475446dcc42fce3327d54a47bd30c906e686`
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
# Thu, 02 May 2024 17:24:52 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 02 May 2024 17:24:52 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN fc-cache -v # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 02 May 2024 17:24:52 GMT
WORKDIR /usr/share/kibana
# Thu, 02 May 2024 17:24:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 02 May 2024 17:24:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 17:24:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 17:24:52 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 02 May 2024 17:24:52 GMT
LABEL org.label-schema.build-date=2024-04-30T02:06:44.402Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=003e4a42946390c2eb93dfb3586498ce7520a530 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.3 org.opencontainers.image.created=2024-04-30T02:06:44.402Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=003e4a42946390c2eb93dfb3586498ce7520a530 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.3
# Thu, 02 May 2024 17:24:52 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 02 May 2024 17:24:52 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 02 May 2024 17:24:52 GMT
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
	-	`sha256:16cb888382ac58320cf5d4fc615a079724601f12c0c100e12c591bf766ebc9f9`  
		Last Modified: Wed, 08 May 2024 00:20:44 GMT  
		Size: 332.8 MB (332760693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf7b11ffbd0c7b4a8f795f3971afbc914b5c229742e9242de03c96a59af9e4`  
		Last Modified: Wed, 08 May 2024 00:20:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c26e8ac59608ccb6e3f66a4d6e387983243b08b76acf87896d1b56f9d6ff47b`  
		Last Modified: Wed, 08 May 2024 00:20:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ec61eb44407f9e3e0f21eb1910ef426fb060f977f4fad52f900a66be8abd4a`  
		Last Modified: Wed, 08 May 2024 00:20:38 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63704d49e5753aad5f665a9afc0221fb753de4f77ccac08d77170a001ffefee4`  
		Last Modified: Wed, 08 May 2024 00:20:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65910ea13ff29423406a890f4a707cd41b5e291df17bbdc6e908b98e0af1dacf`  
		Last Modified: Wed, 08 May 2024 00:20:39 GMT  
		Size: 183.4 KB (183420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e35205baa3d3898ff1938e3227c076e0009714f9a889eec112f5db21b68356`  
		Last Modified: Wed, 08 May 2024 00:20:39 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.3` - unknown; unknown

```console
$ docker pull kibana@sha256:9b13f2deeadcc722469b1d621290bfe45eda992bdbe6aab8734af134d7067893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f31e0aca49dde19b6861dbd77c6131b2c4c122ef37051c9641fa9073bfba7b`

```dockerfile
```

-	Layers:
	-	`sha256:73b42b377a5d4c92e81c35e1ace71a6158b8c0a16f4405bc0e8843738409827f`  
		Last Modified: Wed, 08 May 2024 00:20:36 GMT  
		Size: 3.8 MB (3750949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc38c0fa2df8f0264306f2d141ced0f729e234677fad1f63ba5d53c7081de89`  
		Last Modified: Wed, 08 May 2024 00:20:35 GMT  
		Size: 44.2 KB (44199 bytes)  
		MIME: application/vnd.in-toto+json
