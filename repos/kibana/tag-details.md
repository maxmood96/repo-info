<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.8`](#kibana8178)
-	[`kibana:8.18.3`](#kibana8183)
-	[`kibana:9.0.3`](#kibana903)

## `kibana:7.17.28`

```console
$ docker pull kibana@sha256:b2550601444212c0f4be0973009f5cd238434a68f76449f611c1c5d59589427b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.28` - linux; amd64

```console
$ docker pull kibana@sha256:300ba6a84a9fd4b966afd9c94cba7ed407248cfaa8eb8b4a2b0be9a89cf08a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349401887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814f8b0c22b101593becf57c3488a028123cbf6ca520f4ea0e30af24865f08bd`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 25 Feb 2025 11:58:14 GMT
ARG RELEASE
# Tue, 25 Feb 2025 11:58:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Feb 2025 11:58:14 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Feb 2025 11:58:14 GMT
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
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ea456835084ef3b2a83ca41b1c067b32ddb750d7e316b44e22cbc2653e8f1d`  
		Last Modified: Fri, 09 May 2025 00:15:13 GMT  
		Size: 10.7 MB (10725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c9817efc0a2eb6e3ff008c789b87d7501d369492126b875ea9848e9be43979`  
		Last Modified: Fri, 09 May 2025 00:15:12 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357d3e9a90f4743bace292564a50825dc3c5cf58abcf51c6f11991b827e849f4`  
		Last Modified: Fri, 09 May 2025 00:15:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0501e9c0b84dcc25fcd1fc075bf596c575c374d42c4163af4ab294894a3fcf56`  
		Last Modified: Fri, 09 May 2025 00:15:14 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e1bbff07da50d015c339e76757d5525bb9b327b744a2c25d8108a9637265c`  
		Last Modified: Fri, 09 May 2025 00:15:13 GMT  
		Size: 5.3 KB (5299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f91260925ca5ca55382d2a6645e5c3357b749b61972fc7ebfa16e30ecce908`  
		Last Modified: Fri, 09 May 2025 00:15:42 GMT  
		Size: 294.5 MB (294493406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e7c4853810a90b40f861caa0e10973ff539f6140127a00039fdb9c53ccf1d9`  
		Last Modified: Fri, 09 May 2025 00:15:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bde9374be7f7403d62304b82425d7fd00ef33fb5750447d4754087d07d87c8c`  
		Last Modified: Fri, 09 May 2025 00:15:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c9e27e22d6c4fc57e1701034dc34ac7ec224e260ac31cc421660fa5760bfa2`  
		Last Modified: Fri, 09 May 2025 00:15:15 GMT  
		Size: 4.5 KB (4501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c1873d13033612c9c0c18d33dc984e1b79d82ab1d09f0be505bdca193a3a1d`  
		Last Modified: Fri, 09 May 2025 00:15:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ec2c24e65a384564091f48529373c3eb804015485c26b9d48e951947c5e869`  
		Last Modified: Fri, 09 May 2025 00:15:16 GMT  
		Size: 189.4 KB (189428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9579d7a2d933fc43b65370dc8622c069b4cf339780945521bb1ec694950567`  
		Last Modified: Fri, 09 May 2025 00:15:16 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:f8845a6a35867cd21220b0697de6bc231c32b60a7bfe83dcd83a77854187feea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3439248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8439cd5daea15ab443158ee8df35d882b1509386f85e9cfa79d5399875a03e62`

```dockerfile
```

-	Layers:
	-	`sha256:8ed085192e217de59f734d574dab589511735854559f744ed7183af409ffeffc`  
		Last Modified: Sun, 08 Jun 2025 12:37:11 GMT  
		Size: 3.4 MB (3394739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a968912ba0d60abd66f531a258a09ebe22f75b4fee941682bf1212e2dbb3fa`  
		Last Modified: Sun, 08 Jun 2025 12:37:10 GMT  
		Size: 44.5 KB (44509 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.28` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:fbce756dc34f75e793ed8e8aebe06a7fa4aaff0dcad9419b1b7bdb63521ed277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360254817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e45f194352f19ea8d8cf50780673d894555da714165b5e48ecf692422e06b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 25 Feb 2025 11:58:14 GMT
ARG RELEASE
# Tue, 25 Feb 2025 11:58:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Feb 2025 11:58:14 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 Feb 2025 11:58:14 GMT
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7bff26d1b003bf34f4bc0abf75ef21464e528abe1f4646cc4f7dd87317a031`  
		Last Modified: Fri, 09 May 2025 02:20:33 GMT  
		Size: 10.6 MB (10576633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1acae769c9db7fc15bd20201802ac7e10a23d935608a0fdbe1c04f4b051b17`  
		Last Modified: Fri, 09 May 2025 02:20:26 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289bfd26de33519e5fb64b1a0fc00e92a12dbd302ba5c929349f2c28c4cfc5ba`  
		Last Modified: Fri, 09 May 2025 02:20:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b21ae865a53c3ea076ac5381f0f5b36d2e3f1b67699363cb66853fd425efe3`  
		Last Modified: Fri, 09 May 2025 02:20:36 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daeafc0585c76c4a0b1b7e694ac8c4d58d9a011523646dd76c98a4b2d647709b`  
		Last Modified: Fri, 09 May 2025 02:20:27 GMT  
		Size: 5.3 KB (5279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e300d5851d0849367fd9bffde9ba6dec0bffa1bfd4860fcf3c998a1a4b6fb124`  
		Last Modified: Fri, 09 May 2025 02:20:48 GMT  
		Size: 307.0 MB (307034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6646fe97b0ceb27b81a05a1f631a3d6102837b49fe14b05f9d08f67e5a2fa0b`  
		Last Modified: Fri, 09 May 2025 02:20:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663059830d64f58718a20357cd46fff1b0625d2a7c675327068e1424221bff9a`  
		Last Modified: Fri, 09 May 2025 02:20:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b88cde54938cac0fd124160dc99d956476aa7b01d63439ddbe61d4e8a8800`  
		Last Modified: Fri, 09 May 2025 02:20:27 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1176c4ee36b5e7806234ed28bd30c9775c7cb1f09792166680a384677da05cc4`  
		Last Modified: Fri, 09 May 2025 02:20:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46e31733d9faf72979d93872dc5d8ceec1ebf1e0041652e916a79c172c11cd0`  
		Last Modified: Fri, 09 May 2025 02:20:28 GMT  
		Size: 183.4 KB (183419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8328505486c5e27455912042380bdf45ba029a4de443a75c077d13ab2aaafc36`  
		Last Modified: Fri, 09 May 2025 02:20:27 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:dc13195b74f792d01fd18154be31bb6f5ed0a1099a3eb7fc6f4d41a1602b7589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3439775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebe7098b8c1d303ab49a782f283450981080ae0ed54f09344a42efed499b45b`

```dockerfile
```

-	Layers:
	-	`sha256:37ceaf5df551589cde529ff61fb6b3dd97ed58ca89d3d2a7938f4c1d49a356a9`  
		Last Modified: Sun, 08 Jun 2025 12:37:02 GMT  
		Size: 3.4 MB (3394990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9133ef35b54eb2768d5644052484906f153a1dd2ae7cd37bf7286689c6312b`  
		Last Modified: Sun, 08 Jun 2025 12:37:00 GMT  
		Size: 44.8 KB (44785 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.8`

```console
$ docker pull kibana@sha256:6689f87e7c5df5f1e1e65c9abc4f22f1a61a1817178af83691ddcabf9c6b9589
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.8` - linux; amd64

```console
$ docker pull kibana@sha256:c3c4182042e1c6f6ccbb83f54af852fc5c3e74b717af52bafcbdf0933d2c830e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.9 MB (404948859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83242e76eee0505750419f3d3d75fcfe90b935f4024c22d3e6b160edce3ba6f5`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 09:50:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 24 Jun 2025 09:50:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
RUN fc-cache -v # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
WORKDIR /usr/share/kibana
# Tue, 24 Jun 2025 09:50:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 09:50:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 09:50:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
LABEL org.label-schema.build-date=2025-06-18T18:17:14.465Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9ac86ca77adb4dc5793e20f76695563f0be31f0a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.8 org.opencontainers.image.created=2025-06-18T18:17:14.465Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9ac86ca77adb4dc5793e20f76695563f0be31f0a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.8
# Tue, 24 Jun 2025 09:50:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 24 Jun 2025 09:50:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 24 Jun 2025 09:50:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266f44b10fadf09b01b95f68ae64db72d9c06bad64bb35060b44ddd089dfbd36`  
		Last Modified: Thu, 10 Jul 2025 21:48:03 GMT  
		Size: 11.2 MB (11160936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b619a05ebcb2daf42a84daf5a8de2f094b605160c90d01cc6b59159c7524d6b`  
		Last Modified: Thu, 10 Jul 2025 23:16:50 GMT  
		Size: 347.4 MB (347425920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9af8d32915c7b76b627987f41a32ac05d4d7d6eec82a9013b0de99c4dc8cf9`  
		Last Modified: Thu, 10 Jul 2025 21:48:02 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf82ef33b1677428d033fce613aa879eb3b31bb5b2e2c0e323cfaacc21b0e69`  
		Last Modified: Thu, 10 Jul 2025 21:48:03 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474ec89ec0e2b98b4f3352361b4f08e096ff1c61c775574110a64ae85784c18`  
		Last Modified: Thu, 10 Jul 2025 21:48:02 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d464359539dad65c26464210483dd069fef9d0aad9f2150a118098149c0dcfe9`  
		Last Modified: Thu, 10 Jul 2025 21:48:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a2a7e50a632a2830fb57e8322723664a1552e46b2f173da6e99a2c0260d8e`  
		Last Modified: Thu, 10 Jul 2025 21:48:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dd89d4a793be6658ff8cfd5a302a72fcda377eeac27451eeee18062899774d`  
		Last Modified: Thu, 10 Jul 2025 21:48:02 GMT  
		Size: 4.7 KB (4730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87ab581d2e85f039a1fb96a4f3ec8ba0672b6b473c4bf97b90f10f122bb4e83`  
		Last Modified: Thu, 10 Jul 2025 21:48:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8355dccde498424b6106371362ffa0a1293766900cee8048c0c57c8b5be32e5c`  
		Last Modified: Thu, 10 Jul 2025 21:48:02 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6919769550758e4e876cd17d23bc520b4f843b1f91939c13f5f0a373b69c7ee`  
		Last Modified: Thu, 10 Jul 2025 21:48:02 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.8` - unknown; unknown

```console
$ docker pull kibana@sha256:311bd0e1b6f9011762caf9056acf8e94620d76f02d40fc3cf026be265dc054bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b980c3c6963c3fd417c356569feb512049842859396d90918c69e4471f740f`

```dockerfile
```

-	Layers:
	-	`sha256:e5742ddf7e6a13361be4c087ebfe91c75a60c41ddb71fbb7b5f2f2cb901fddcb`  
		Last Modified: Thu, 10 Jul 2025 23:11:23 GMT  
		Size: 4.5 MB (4518509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f04df5dbe1808ad2a27af9a9ccb6d7610eb2cc647463e1637d3f0967eb221d8`  
		Last Modified: Thu, 10 Jul 2025 23:11:24 GMT  
		Size: 40.7 KB (40739 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:2bb0bae7022f637129365335dbc64a40cfe9879a6939a285060d6228569f3d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.2 MB (417217780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ee3248aa77d2e1baadb6557fc9bd8b1f55013bc7bbc92878615aeef817e414`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 09:50:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 24 Jun 2025 09:50:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
RUN fc-cache -v # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
WORKDIR /usr/share/kibana
# Tue, 24 Jun 2025 09:50:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 09:50:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 09:50:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 24 Jun 2025 09:50:26 GMT
LABEL org.label-schema.build-date=2025-06-18T18:17:14.465Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9ac86ca77adb4dc5793e20f76695563f0be31f0a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.8 org.opencontainers.image.created=2025-06-18T18:17:14.465Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9ac86ca77adb4dc5793e20f76695563f0be31f0a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.8
# Tue, 24 Jun 2025 09:50:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 24 Jun 2025 09:50:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 24 Jun 2025 09:50:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ea964ce3d2024cd7d3eccac8714552b9f2efd0309b18f7a4c34c529fbf4d0b`  
		Last Modified: Thu, 10 Jul 2025 21:58:47 GMT  
		Size: 11.3 MB (11257662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189d86cc656b1c22d6aaf392f642ebb686220a8156f4f86c2cbe27a02d7d59d9`  
		Last Modified: Thu, 10 Jul 2025 23:15:56 GMT  
		Size: 360.5 MB (360464362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97902083dcee61e242ab1b3bec32f24ebd6e3315c22ccd475f26f2ddda64c711`  
		Last Modified: Thu, 10 Jul 2025 21:58:46 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0083c89b3667311a859597e3f1e08e785dc6b372067f56b30bc8863206a916c6`  
		Last Modified: Thu, 10 Jul 2025 21:58:48 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003785845a453a5298fb57ec947f882e7e70d0d22f815a387eb1589c4b695285`  
		Last Modified: Thu, 10 Jul 2025 21:58:46 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038a9808b7d62563c5194bea533ef8c808227ecba43f5bc83b98fec408fe6519`  
		Last Modified: Thu, 10 Jul 2025 21:58:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff89b94c6d64428eb827ba283d640bb515baab641cbfa1836aa9f03517edb6f0`  
		Last Modified: Thu, 10 Jul 2025 21:58:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1757e8464fdfd7b358b1c80e5bf5fc5181d457b6a6c5e0a68f7d0d92d2ea4428`  
		Last Modified: Thu, 10 Jul 2025 21:58:47 GMT  
		Size: 4.7 KB (4729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58cec76ef259708344815b3bcf9c12f47d5d3001c0baa0428011a7d1fac56e7`  
		Last Modified: Thu, 10 Jul 2025 21:58:46 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7876826dba72932bf87215a1f19a95df845a4d8cb7a5f5315c4d5daad4cac1db`  
		Last Modified: Thu, 10 Jul 2025 21:58:46 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4e7dc167da3b0f1bd497f3c4c1cd8777dafcd6a84074e97faab20a9f1d61d7`  
		Last Modified: Thu, 10 Jul 2025 21:58:47 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.8` - unknown; unknown

```console
$ docker pull kibana@sha256:6bb8bba43746a8c566f17a3ddf09938a2283838631465a64bcae1581ec7db20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4560560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6464a9635700cf7ee433b764b2cd5250041de87cd21ddb99ba852dcc6b9947e7`

```dockerfile
```

-	Layers:
	-	`sha256:aa3b66a86646e2993a69307cb07a729b433d21ac9b3504bc0ff50806db06f87f`  
		Last Modified: Thu, 10 Jul 2025 23:11:29 GMT  
		Size: 4.5 MB (4519573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c609f9e316d7218a1dc98302c52acd6a31dd6623b0e8e555bdc702bee0695311`  
		Last Modified: Thu, 10 Jul 2025 23:11:30 GMT  
		Size: 41.0 KB (40987 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.3`

```console
$ docker pull kibana@sha256:73ea36190c6ba43a2e7add47dd4715684efba697bac4936f644c4c16801544a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.3` - linux; amd64

```console
$ docker pull kibana@sha256:318697de51bcf795c75276af18b59157b2bb33715f7884ac213e55c4f16b4190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424235134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101b6f9fd04bd8df6e9a339098dc79410473005e76923d04a13bcd6013e48aaf`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 10:05:53 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 24 Jun 2025 10:05:53 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN fc-cache -v # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
WORKDIR /usr/share/kibana
# Tue, 24 Jun 2025 10:05:53 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 10:05:53 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
LABEL org.label-schema.build-date=2025-06-18T18:13:59.370Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=70e0ee45ae6f2e5cd35b7af4822d86ffa877ad9c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.3 org.opencontainers.image.created=2025-06-18T18:13:59.370Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=70e0ee45ae6f2e5cd35b7af4822d86ffa877ad9c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.3
# Tue, 24 Jun 2025 10:05:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 24 Jun 2025 10:05:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 24 Jun 2025 10:05:53 GMT
USER 1000
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34adf07c2e235fb6bf1a033c4e7b579243eb34019c7ffe51984feac75857515c`  
		Last Modified: Thu, 10 Jul 2025 21:48:46 GMT  
		Size: 11.2 MB (11160838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462a9ca625322f219e69243ee9ff0f9d313c4acae3b74bbb380841e3fb94632a`  
		Last Modified: Thu, 10 Jul 2025 23:18:24 GMT  
		Size: 366.7 MB (366712282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce00f5d5d6bee7c99b67f6283586014e00a8c2c375dfd1a72cc0ca76ca4ed875`  
		Last Modified: Thu, 10 Jul 2025 21:48:45 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80248e1fcd0a2ad288829a982748744d92e61845ecec0720513316bff2899aa6`  
		Last Modified: Thu, 10 Jul 2025 21:48:46 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb2796b449c81a75a3fc43f7332c63183329e698d53cf63ba191b545abc07c7`  
		Last Modified: Thu, 10 Jul 2025 21:48:45 GMT  
		Size: 5.2 KB (5238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405431b319204497391e0585e74f42ecf424900b510896cfe5c91a6f1b95277a`  
		Last Modified: Thu, 10 Jul 2025 21:48:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56634f2128aefc45d20643dc5d2169737ddd9e216aa9b978d1458562dbed0656`  
		Last Modified: Thu, 10 Jul 2025 21:48:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7ea3540cc0433e005dff905179d051e5484f2499e0b62360f0f5ad8bbbdeec`  
		Last Modified: Thu, 10 Jul 2025 21:48:45 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aead48d98d84493ba327f8ffdff99649606b56649481626d1ad8b9f1a48d3bb8`  
		Last Modified: Thu, 10 Jul 2025 21:48:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df2c59cd071288d28eabe65e2c69699c1edab9c377f544eaf52d9e9df44dc9`  
		Last Modified: Thu, 10 Jul 2025 21:48:45 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a753821cbc3a6ff305e7adfbd70c8d94a0cea7a2c52050b45bc0881162f9248`  
		Last Modified: Thu, 10 Jul 2025 21:48:45 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.3` - unknown; unknown

```console
$ docker pull kibana@sha256:c8a59da8b1a8fb9327c2f5cc4b41454642ea695706c401cfcbe51c2d9cc45ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4810496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74737c042b61ef3fb1c7b3f54511f96fd0c1b46b78ec139c0f0e922e2bd0b17b`

```dockerfile
```

-	Layers:
	-	`sha256:0001d47eddd4c6de94111602b64b98bbebcd6c2b58e7b38f40b3d7df91d961de`  
		Last Modified: Thu, 10 Jul 2025 23:11:33 GMT  
		Size: 4.8 MB (4769757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff50dd20e583ccdae81c732db7be23e186eaf85ba0ce45a0db1115f768e9242e`  
		Last Modified: Thu, 10 Jul 2025 23:11:33 GMT  
		Size: 40.7 KB (40739 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:13dffd824a715912c38c15048c22f765dcd0aa7a661f10643cf1a5d83eabf5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.5 MB (436505136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3accff34c558adde2515bd41576f24488983e27366d47fe02ab9675ffcae6ee7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 10:05:53 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 24 Jun 2025 10:05:53 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN fc-cache -v # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
WORKDIR /usr/share/kibana
# Tue, 24 Jun 2025 10:05:53 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 10:05:53 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 10:05:53 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 24 Jun 2025 10:05:53 GMT
LABEL org.label-schema.build-date=2025-06-18T18:13:59.370Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=70e0ee45ae6f2e5cd35b7af4822d86ffa877ad9c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.3 org.opencontainers.image.created=2025-06-18T18:13:59.370Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=70e0ee45ae6f2e5cd35b7af4822d86ffa877ad9c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.3
# Tue, 24 Jun 2025 10:05:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 24 Jun 2025 10:05:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 24 Jun 2025 10:05:53 GMT
USER 1000
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ea964ce3d2024cd7d3eccac8714552b9f2efd0309b18f7a4c34c529fbf4d0b`  
		Last Modified: Thu, 10 Jul 2025 21:58:47 GMT  
		Size: 11.3 MB (11257662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ef8bf05b534bb08cf2267808a20814a67a8c5e91cd5664a0016e501b53c8ea`  
		Last Modified: Thu, 10 Jul 2025 23:17:38 GMT  
		Size: 379.8 MB (379751687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6634adc41061856a794cb11712b3418adcc54e3038b4e11531deb330312b3399`  
		Last Modified: Thu, 10 Jul 2025 22:06:02 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a6b598d8502f89f9fac3f28752565cd48a3fa4204a775cb89235a58978472f`  
		Last Modified: Thu, 10 Jul 2025 22:06:05 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616eb8f528d341ee79cfbe50348f4fa7fad8538f4d00aaee8f670d5954138d34`  
		Last Modified: Thu, 10 Jul 2025 22:06:03 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71f1258faa3009f8d384217caa8f93cf4b91a6ff845715bf8d7ed1525005ca3`  
		Last Modified: Thu, 10 Jul 2025 22:06:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16721d72e890bad6138bd64c8c653e90c6f967f9f517bab2f55a460d3a2d6898`  
		Last Modified: Thu, 10 Jul 2025 22:06:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dddc47cb6eea4ddb6b4551f7b3518f219f3da4c553075babfad557f712538c`  
		Last Modified: Thu, 10 Jul 2025 22:06:03 GMT  
		Size: 4.8 KB (4764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888ab6249b9de8ca2862740c6d0865bb166ad6bce21a9e835d6c636435e369c3`  
		Last Modified: Thu, 10 Jul 2025 22:06:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987bc0145035df21797c41bfa81fa1b1f5cd78f1f026fd678a67625bb39d5efe`  
		Last Modified: Thu, 10 Jul 2025 22:06:03 GMT  
		Size: 158.0 KB (157998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98de5d8bfbd686c6b899bffcc05fdb92dd13d99b99775bfbb38ad04293281af9`  
		Last Modified: Thu, 10 Jul 2025 22:06:03 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.3` - unknown; unknown

```console
$ docker pull kibana@sha256:92a7ab5e8aadc0d2f3a9f7bfe6960cd6075c86a503f307d158507ff46d9a9385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4811807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c628afa8db5d8922990b522f91cc3072f89351516c2f9baae05b6fd87d2689b`

```dockerfile
```

-	Layers:
	-	`sha256:420617a482ac89d8ea6206999edbfc2800c052c01999cb20f914029fc4cb8b2f`  
		Last Modified: Thu, 10 Jul 2025 23:11:38 GMT  
		Size: 4.8 MB (4770821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add93233f71ff75b849a48ce91e5249090bffbc557e23628fd8c8ac3d7167bdc`  
		Last Modified: Thu, 10 Jul 2025 23:11:39 GMT  
		Size: 41.0 KB (40986 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.3`

```console
$ docker pull kibana@sha256:f50917ac0ed94408f7482f28bb42837dc6620c113bb132d5490d899547fb5133
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.3` - linux; amd64

```console
$ docker pull kibana@sha256:92daf18f0c528ff5a8f6042a21608ed0ff7c5b30a6fc1bf28cf01b9910aca70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.2 MB (438239744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fdcae9c6499246363ebddf909491966907bd9606a21461e0371cc66052c948`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL url="https://www.redhat.com"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 24 Jun 2025 11:03:26 GMT
ENV container oci
# Tue, 24 Jun 2025 11:03:26 GMT
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Tue, 24 Jun 2025 11:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 24 Jun 2025 11:03:26 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 11:03:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Tue, 24 Jun 2025 11:03:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 24 Jun 2025 11:03:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN fc-cache -v # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
WORKDIR /usr/share/kibana
# Tue, 24 Jun 2025 11:03:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 11:03:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL org.label-schema.build-date=2025-06-18T20:29:08.844Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3b8379b249b9b5ab0c3c2ee245cd7d62ad93ab4d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.3 org.opencontainers.image.created=2025-06-18T20:29:08.844Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3b8379b249b9b5ab0c3c2ee245cd7d62ad93ab4d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.3
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 24 Jun 2025 11:03:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 24 Jun 2025 11:03:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 24 Jun 2025 11:03:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d618e8313815b5c4ee6fce1690fb89c5f33f1ac94436a3cbe0219d89ceeb3`  
		Last Modified: Thu, 10 Jul 2025 21:48:11 GMT  
		Size: 19.4 MB (19386293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2490b78562eb3f8df47d5bab3a121ad92ca4d1ec35443510fc02a35a2e60ec0`  
		Last Modified: Thu, 10 Jul 2025 23:19:39 GMT  
		Size: 362.6 MB (362643889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10e7740dfa08452fa0d1bf7c96d97bb0b9afa1d617d71061492c1f8bb8b1177`  
		Last Modified: Thu, 10 Jul 2025 21:48:09 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b990175128544eb9efab25b069be55be94869d0f52c22d0c182c7c9824d501fd`  
		Last Modified: Thu, 10 Jul 2025 21:48:12 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e29d725bccf6dd5addc6e94096ee71192d9e6bd91695f9214f9b5c6172845c`  
		Last Modified: Thu, 10 Jul 2025 21:48:10 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c5898ee3089e52c39789cdc698e332c0bef09c97853c5a346db49795f812ad`  
		Last Modified: Thu, 10 Jul 2025 21:48:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a14ebd1397ad5648b78585ceda06db8288763378804effa00648badfdd28a9a`  
		Last Modified: Thu, 10 Jul 2025 21:48:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244429ea3a91a45135822dd8dd694700cc7962abce9c05141581d5af22ebf8ad`  
		Last Modified: Thu, 10 Jul 2025 21:48:10 GMT  
		Size: 4.7 KB (4688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505da2ba412a15bab18a2396a90a12747d6b00a5ed5c0093529aa4e2e5038a94`  
		Last Modified: Thu, 10 Jul 2025 21:48:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77d21f5ca7a438930815cfef918fb6e2ba830d7a90255c7b04d1bd32a4abf7`  
		Last Modified: Thu, 10 Jul 2025 21:48:11 GMT  
		Size: 75.1 KB (75097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c0662cc146737b2109b7a5f374ae724a1d4604885792390e24c6994fb40dd9`  
		Last Modified: Thu, 10 Jul 2025 21:48:10 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78b7bc860d1898c9b9b761aa046135851fe95cc03a4cd9aecf7c946987e10ba`  
		Last Modified: Thu, 10 Jul 2025 21:48:09 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.3` - unknown; unknown

```console
$ docker pull kibana@sha256:4dda5bc3d7cd64010cfc003ea23e2920fb22e3c60b996071f0e098c0981b646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5512905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c98012232888bbe784a6afc750d57ab94dcc00218661f359708fafe2765b61`

```dockerfile
```

-	Layers:
	-	`sha256:f6e2aa6537091d5fda680b0d4063a781607a40e1b9cfcb97d471935cb6446aed`  
		Last Modified: Thu, 10 Jul 2025 23:11:41 GMT  
		Size: 5.5 MB (5469721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f39aa6544754b1c3bd1c6c53c84d88414073f1d626f796b11d0a088653c3ad6d`  
		Last Modified: Thu, 10 Jul 2025 23:11:42 GMT  
		Size: 43.2 KB (43184 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e16125e3e715d8dfa5fffb050f63ad52c5c2be088392e83e9de54bc914433996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.4 MB (449441503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e732947d5a7711c83f8482a09b23803fdb78ab5df1882d37a54b6180e971c3a1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL url="https://www.redhat.com"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 24 Jun 2025 11:03:26 GMT
ENV container oci
# Tue, 24 Jun 2025 11:03:26 GMT
COPY dir:4a26990fc6a982252bab47a280479ef21eaa9fb0686b5810bf75da5fc5af7d4f in /    
# Tue, 24 Jun 2025 11:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Tue, 24 Jun 2025 11:03:26 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 11:03:26 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL "build-date"="2025-06-30T12:36:52" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Tue, 24 Jun 2025 11:03:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 24 Jun 2025 11:03:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN fc-cache -v # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
WORKDIR /usr/share/kibana
# Tue, 24 Jun 2025 11:03:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 24 Jun 2025 11:03:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jun 2025 11:03:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL org.label-schema.build-date=2025-06-18T20:29:08.844Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3b8379b249b9b5ab0c3c2ee245cd7d62ad93ab4d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.3 org.opencontainers.image.created=2025-06-18T20:29:08.844Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3b8379b249b9b5ab0c3c2ee245cd7d62ad93ab4d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.3
# Tue, 24 Jun 2025 11:03:26 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 24 Jun 2025 11:03:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 24 Jun 2025 11:03:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 24 Jun 2025 11:03:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 24 Jun 2025 11:03:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:ffb6dfc9a5fd85e709e0a3428084894621f9e001746e51a54875b13ff103e464`  
		Last Modified: Mon, 30 Jun 2025 14:20:11 GMT  
		Size: 37.9 MB (37864356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab4c98c7b7104fa6bb986aaf2e91b7a0c141c63f25b5493d5cb5cc893161b6`  
		Last Modified: Wed, 02 Jul 2025 18:55:02 GMT  
		Size: 19.3 MB (19315841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6cfce160033e8a14063df1efdbca1c17852e3500612c4a296e5784be3fb31b`  
		Last Modified: Thu, 10 Jul 2025 23:19:00 GMT  
		Size: 375.7 MB (375704098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a75def3c3a0123876450b96686dc7c7760a65d702887f3974c1a40ee335046`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de82a55ebb2b89f280a5d50185fc1c7782cf038cd81aa55a002e776efbac00f`  
		Last Modified: Thu, 10 Jul 2025 22:13:06 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f33638e05305d4f2cb328750f27c3f15c0ede74044da511536247fcedccf4`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64b3792124e6b42137024d7448b4bbd9b5a883d607cd16a024dc5469e51cb7`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2253854adb8f96ef5be1f7dc3c77d654ce613bb6a28d59aec71083ba5ab1ae5`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648758e963b3b13948e4ec17933a4367909a4aedda94304c2ff0728ee62eef7`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 4.7 KB (4690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbf9fc8106f9f42f1d1a7def295e48a7959c73d4ad9ca2b9048ac9daa7e04b9`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9053d4269575e6fe5ed9b3b92e2a850dd0b38d7823231e1ddbfc1723abcc038`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 74.0 KB (73984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fc8820b99ac50a0d2c2895951ffc4795288da98f68b7f81d410c65c47634a9`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8519502f76cbd639d3a1abb90848eaeccbd992c481b40c5cf97206ff94def5b1`  
		Last Modified: Thu, 10 Jul 2025 22:13:06 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.3` - unknown; unknown

```console
$ docker pull kibana@sha256:3df00fa39902d9b3aeae52e33a39bda1cbdc71189430ac014c9a38013bd0efba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fcfa29ec0ecded548f638bbb7f0af19871e11ccce66ce613ec8468f7e15559`

```dockerfile
```

-	Layers:
	-	`sha256:f6f586b9cf4df057e242b5822f112f5f2bb31acd9cc35427b36c58fb26eb7e94`  
		Last Modified: Thu, 10 Jul 2025 23:11:47 GMT  
		Size: 5.5 MB (5468383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e277549547fae266a2f73444f36657ae55afd664446055164657cfd54480af3d`  
		Last Modified: Thu, 10 Jul 2025 23:11:48 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
