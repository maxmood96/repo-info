<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.6`](#kibana8176)
-	[`kibana:8.18.2`](#kibana8182)
-	[`kibana:9.0.2`](#kibana902)

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

## `kibana:8.17.6`

```console
$ docker pull kibana@sha256:2389c98d286c0610e55d81ed7342b1ac46dee82e64a655f4f85f16100fdcbb2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.6` - linux; amd64

```console
$ docker pull kibana@sha256:3115ac50843f93eed70f43af2a09b4fa9e23db38f8c04c3d40585d3db2ea991a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.0 MB (396990728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f124788a2df941193efe58975f9c11bb41e5cca2c7d889f96b579eeb42025d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Tue, 06 May 2025 08:53:36 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 May 2025 08:53:36 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN fc-cache -v # buildkit
# Tue, 06 May 2025 08:53:36 GMT
WORKDIR /usr/share/kibana
# Tue, 06 May 2025 08:53:36 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 May 2025 08:53:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 08:53:36 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 May 2025 08:53:36 GMT
LABEL org.label-schema.build-date=2025-04-30T14:16:07.374Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=28847d93343b5a3adfb1bcb953866a6705ab746f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.6 org.opencontainers.image.created=2025-04-30T14:16:07.374Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=28847d93343b5a3adfb1bcb953866a6705ab746f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.6
# Tue, 06 May 2025 08:53:36 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 May 2025 08:53:36 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 May 2025 08:53:36 GMT
USER 1000
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a001e434c4436c8bff67d5c1cc60f2623028ebf558c3a5e5f7fb87816ad84390`  
		Last Modified: Fri, 09 May 2025 19:04:50 GMT  
		Size: 10.7 MB (10725868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb6c8172f42ccddb94feca5dc854fc85de5c182d6858467f38533c36a2bcb93`  
		Last Modified: Fri, 16 May 2025 14:44:23 GMT  
		Size: 342.1 MB (342082257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2468c87d0c5d74b9af18c832a57db8b83de4c63623bf5856536bed1288b4a4d`  
		Last Modified: Fri, 09 May 2025 19:04:47 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9576421bd051a1f6878ea9e26b79f42bee0b6f9715d3fb33a3e09ad8411ce41d`  
		Last Modified: Fri, 09 May 2025 19:04:50 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0707752b514431a490efcdbb31f3993c10a9be597ba86d20068688f10b3a03e3`  
		Last Modified: Fri, 09 May 2025 19:04:47 GMT  
		Size: 5.3 KB (5276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf42d675f2039095220de79b5b04cc629c8686ee500f5aaf19aca056f717616`  
		Last Modified: Fri, 09 May 2025 19:04:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ea22231532882f07501df82aab864faae27cefc235a31e61a71e25303e9b27`  
		Last Modified: Fri, 09 May 2025 19:04:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a3df13ed1f02fd58d6d4c2494f6c27fb9657986c98c4a37ca0fca761b4622`  
		Last Modified: Fri, 09 May 2025 19:04:47 GMT  
		Size: 4.7 KB (4726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de3db135547d5a546fedbc60de245429b851d75d3a801368d341fc699cb5088`  
		Last Modified: Fri, 09 May 2025 19:04:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7952248b81cded371966ff51619727f6f68c30f67ddc86d708b9f8a6b17e5366`  
		Last Modified: Fri, 09 May 2025 19:04:49 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d010667ca15d7de83c3127ee024c321d4bc40ef9a7d20383a6b1eb5d70050ff`  
		Last Modified: Fri, 09 May 2025 19:04:48 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.6` - unknown; unknown

```console
$ docker pull kibana@sha256:4c8c5ec9d32f61e30443d578e150cb7e32299c58d9a47e6950eb4dda6f3a6668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4434756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcede4dae47480b64589810e00599993befe4f44b1f6ef56cccb9635994cfab`

```dockerfile
```

-	Layers:
	-	`sha256:b49fd0c8cc7f65cad6afac882c141a84b51dd0c3252876299970a71b545c1c16`  
		Last Modified: Fri, 09 May 2025 19:03:38 GMT  
		Size: 4.4 MB (4394076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da223a365c2551508ed75eec8e4726a48ad263b2143237dd9c5a0ba3b667b766`  
		Last Modified: Fri, 09 May 2025 19:03:38 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:b0e5a6ffc316bb61cf842710d2dc628d351a2768eb3173d19e6e6de8155d4160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407691420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abbb6718ced30e9d30f7ee176dc787428d72b2b3bd2369358adcbf415cc318e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Tue, 06 May 2025 08:53:36 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 May 2025 08:53:36 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN fc-cache -v # buildkit
# Tue, 06 May 2025 08:53:36 GMT
WORKDIR /usr/share/kibana
# Tue, 06 May 2025 08:53:36 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 May 2025 08:53:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 08:53:36 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 08:53:36 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 May 2025 08:53:36 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 May 2025 08:53:36 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 May 2025 08:53:36 GMT
LABEL org.label-schema.build-date=2025-04-30T14:16:07.374Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=28847d93343b5a3adfb1bcb953866a6705ab746f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.6 org.opencontainers.image.created=2025-04-30T14:16:07.374Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=28847d93343b5a3adfb1bcb953866a6705ab746f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.6
# Tue, 06 May 2025 08:53:36 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 May 2025 08:53:36 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 May 2025 08:53:36 GMT
USER 1000
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ccd575a42dec4f47ce6b7c881155e826b5607c4ae0b24d5b1c6e251081332f`  
		Last Modified: Fri, 16 May 2025 19:42:21 GMT  
		Size: 10.6 MB (10576710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5fe48a70342ee31bc60cfc811d929541eb99d9ebb5f83a0393ef456820da69`  
		Last Modified: Fri, 16 May 2025 19:49:42 GMT  
		Size: 354.5 MB (354471260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ebad1d1e747c6255d65e2c4f893a3170b1f76241caf662a9704ef6112e6d3`  
		Last Modified: Fri, 16 May 2025 19:49:06 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a7d40cef6ccd89a205f13b4088e8e2cd70b0c4d7f3ec9447f4142339601d75`  
		Last Modified: Fri, 16 May 2025 19:49:18 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ac34c76184d343fcf8eab6d316bd6d35162bbff5c2c6a9493a33aecd871e`  
		Last Modified: Fri, 16 May 2025 19:49:11 GMT  
		Size: 5.3 KB (5280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cd2b5ea96b4241755c77ce62e808fcbf6773a8fa00973e1e50efe24497a004`  
		Last Modified: Fri, 16 May 2025 19:49:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f606e28e60b810a4974f28eaa50b9f9161b9ef2661eb814becd216c5536537a3`  
		Last Modified: Fri, 16 May 2025 19:49:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b46bdd2348534171bdb0dbde947710e4e12403856ce6e31d097f75c54a5dd6`  
		Last Modified: Fri, 16 May 2025 19:49:21 GMT  
		Size: 4.7 KB (4732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da982d9084c800d269075bc543e4b767de9498e43063bccae9a166f486ed8662`  
		Last Modified: Fri, 16 May 2025 19:49:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a842fe9e93726d5c37369f73412990e41e12d0425923bfbc792a58254973a4`  
		Last Modified: Fri, 16 May 2025 19:49:24 GMT  
		Size: 183.4 KB (183422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189be11abd167f33dee5cdb34f1abff92d1219ca5ee36f518e11143bad3dc77b`  
		Last Modified: Fri, 16 May 2025 19:49:24 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.6` - unknown; unknown

```console
$ docker pull kibana@sha256:2bad3174b3974218637431bf159462dcad32d18864503b0dec6943ece33f2784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4435254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23590d7acc0f16e77803c28ef99c391ce19868f18bdd2517fdebecb22c6d827e`

```dockerfile
```

-	Layers:
	-	`sha256:9c627e7261ec41adc9843cc3e668c9c2a633d0c313117452e9c8ee665fa67bcf`  
		Last Modified: Fri, 09 May 2025 20:24:51 GMT  
		Size: 4.4 MB (4394327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded152941e5dcc3e70e5998834cab46f97add84b44d29ea2806d7639ee9ed913`  
		Last Modified: Fri, 09 May 2025 20:24:51 GMT  
		Size: 40.9 KB (40927 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.2`

```console
$ docker pull kibana@sha256:94b2e0789bca13d1be112c53005e5136dccc5b253158fe08130ff49779d43ffa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.2` - linux; amd64

```console
$ docker pull kibana@sha256:5fc71bdab6f87b7d099e83c252241d3176f1a60a668c6352e858a873bd0e2f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.5 MB (422510950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d2f89d6cde8c8579555d0568c1d86233dad14e123b68a55452077520ac32db`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Thu, 29 May 2025 09:13:46 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 29 May 2025 09:13:46 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN fc-cache -v # buildkit
# Thu, 29 May 2025 09:13:46 GMT
WORKDIR /usr/share/kibana
# Thu, 29 May 2025 09:13:46 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 29 May 2025 09:13:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 29 May 2025 09:13:46 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 29 May 2025 09:13:46 GMT
LABEL org.label-schema.build-date=2025-05-23T11:08:08.589Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c381b5aca4e1e164e92bf39435fb80557f7d32f3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.2 org.opencontainers.image.created=2025-05-23T11:08:08.589Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c381b5aca4e1e164e92bf39435fb80557f7d32f3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.2
# Thu, 29 May 2025 09:13:46 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 29 May 2025 09:13:46 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 29 May 2025 09:13:46 GMT
USER 1000
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095aff851611716a8900e0ba06edc408030251b249c9043041698cf7c6a7dfe3`  
		Last Modified: Tue, 03 Jun 2025 13:37:10 GMT  
		Size: 18.8 MB (18847333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dc290fc07ea89ebf42ce173c1e565e8b7c0554a3c2e23475d792c8e0820caa`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 359.5 MB (359480980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325b172f5af242834b32d07b4dbd3f5062c11a72eabc780caac15bdc31bbadfe`  
		Last Modified: Tue, 03 Jun 2025 13:37:09 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbb06050436c0b1a18f61ca97991b5c49f23d1adf8e747fa96943b62b6a3b94`  
		Last Modified: Tue, 03 Jun 2025 13:37:13 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc091fd35743d112bdb53a9eae04e6557f4ca76c32a6a060d80d27f3fb28eb`  
		Last Modified: Tue, 03 Jun 2025 13:37:12 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7281a7096249a439e6095026d6c2080435a0d70cfe67d5edc8edcc02c8e555`  
		Last Modified: Tue, 03 Jun 2025 13:37:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e7e642452fe6c440ea1333714e15d24c3973b6e008bb79e3b20d404184716`  
		Last Modified: Tue, 03 Jun 2025 13:37:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b1b8a82d17a60ab21bf2cab7337bd3e71def54a40b975968689e0617721423`  
		Last Modified: Tue, 03 Jun 2025 13:37:17 GMT  
		Size: 4.8 KB (4757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dd03e46a211e99c5221f287a4b9f532557ff2f2b8301cc0f7001036c4ce102`  
		Last Modified: Tue, 03 Jun 2025 13:37:17 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe5764db9120b8644551b3d6fe2671b058439df118f0c18acbedd55563b45a5`  
		Last Modified: Tue, 03 Jun 2025 13:37:20 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf79de4f307a722fb62b0624eb681564db1d9d7f2d488a9997ae6ced99deeb5f`  
		Last Modified: Tue, 03 Jun 2025 13:37:19 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.2` - unknown; unknown

```console
$ docker pull kibana@sha256:6da6c574816559fb4daa95a8d385201e4f34bd58fcda7238672deed0874fd98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ac142630d991a41b2f192f19ef52174aa3c1d563ea7de47ef7debf9ba4c69b`

```dockerfile
```

-	Layers:
	-	`sha256:2d48681433d8c60d5cd6730d06221ee176b9554009f8af482e392227045f3459`  
		Last Modified: Thu, 05 Jun 2025 04:23:27 GMT  
		Size: 4.7 MB (4668281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe9bc4f02f5f9e855bec27ba742b3df0b8f19bde2055f1bd3d81cd96f81f8b1`  
		Last Modified: Thu, 05 Jun 2025 04:23:26 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d01b4a87cac276a9de2bcf317e43ac1b62aa96e68fbf85820d04d59cf09aa3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432068913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90ffb7c7d7a313ea56127afda5a4a9079a7ad6824cc5facf922afb888b25198`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Thu, 29 May 2025 09:13:46 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 29 May 2025 09:13:46 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN fc-cache -v # buildkit
# Thu, 29 May 2025 09:13:46 GMT
WORKDIR /usr/share/kibana
# Thu, 29 May 2025 09:13:46 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 29 May 2025 09:13:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 29 May 2025 09:13:46 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 May 2025 09:13:46 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 29 May 2025 09:13:46 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 29 May 2025 09:13:46 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 29 May 2025 09:13:46 GMT
LABEL org.label-schema.build-date=2025-05-23T11:08:08.589Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c381b5aca4e1e164e92bf39435fb80557f7d32f3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.2 org.opencontainers.image.created=2025-05-23T11:08:08.589Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c381b5aca4e1e164e92bf39435fb80557f7d32f3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.2
# Thu, 29 May 2025 09:13:46 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 29 May 2025 09:13:46 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 29 May 2025 09:13:46 GMT
USER 1000
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98e755ea1fae1c8b3be98f49b22827465a4a62cb136b35bcc8e4e4e4d273aa`  
		Last Modified: Tue, 03 Jun 2025 13:36:19 GMT  
		Size: 17.6 MB (17564933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e88bad19f9f194c59d901a96582483b1519f69672d25375b5ec2c41086543b7`  
		Last Modified: Tue, 03 Jun 2025 13:36:21 GMT  
		Size: 371.9 MB (371860503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68133a13ceb4ed7d5240fef231206876dfc2728187caa0b79611fc0ff06cd03e`  
		Last Modified: Tue, 03 Jun 2025 13:36:22 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d256b292e602a521403dd69cf1f3e00862b208832676f97188fb89c5a991458`  
		Last Modified: Tue, 03 Jun 2025 13:36:27 GMT  
		Size: 16.5 MB (16460473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7e9d9425ec9397b1f35f3c724ae044cc5a1b465693d878498db7d5602bef91`  
		Last Modified: Tue, 03 Jun 2025 13:36:28 GMT  
		Size: 5.3 KB (5287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f338bcd4efc1772379ec74ba6c423f887fa8238a30b20ff8da25e6dbc4031f3`  
		Last Modified: Tue, 03 Jun 2025 13:36:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749bca16488a4476afc1c7f5b6e75f0d013c54d69c777bca49195defe4aa74f4`  
		Last Modified: Tue, 03 Jun 2025 13:36:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea206b58478c96e030c54022b8635906edd1405ea0dc67d6a42c347c2ce5b257`  
		Last Modified: Tue, 03 Jun 2025 13:36:35 GMT  
		Size: 4.8 KB (4764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d89d73da05cf718d409df774a0715b02636f34dd77ed807e142cd990b57848`  
		Last Modified: Tue, 03 Jun 2025 13:36:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6bc784e771f8b2c6fd7ba0961bb829f9ebc9be181671871c42b2aaaf25e40d`  
		Last Modified: Tue, 03 Jun 2025 13:36:39 GMT  
		Size: 183.4 KB (183423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4fc88c29bb3107b24aae5042f22f7a2c3441646a5f47209ddd99a20f2dd60e`  
		Last Modified: Tue, 03 Jun 2025 13:36:41 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.2` - unknown; unknown

```console
$ docker pull kibana@sha256:6471809d4524e4ae316e638c5fd660f087fdf37a8229e91243657e64edce7709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4709460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba48bcc878a2cee27f7636b3e16d9c69173b830e807e6825501b05fd89c6ece0`

```dockerfile
```

-	Layers:
	-	`sha256:d682ccabe12ecca21bf6a72497eebc52300982236edd9663ccb7cb7bd4e67ace`  
		Last Modified: Thu, 05 Jun 2025 04:23:29 GMT  
		Size: 4.7 MB (4668532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f0954513b99adc3d34416d1d9301c9e15c237f5e2b41ab0d19b5de9387ee3c6`  
		Last Modified: Thu, 05 Jun 2025 04:23:28 GMT  
		Size: 40.9 KB (40928 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.2`

```console
$ docker pull kibana@sha256:3b85ce5b71155983e32aeb7958572a93e8a58139ec0b722267f8020e9a598293
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.2` - linux; amd64

```console
$ docker pull kibana@sha256:d9fc1875e012f0a4338e5c05a3b04a0bd2e66a5b7c5427cdf8fee57c31bbccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.6 MB (430612244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d6087cf95b0e52099bedd45b5ceae5d2792cddb72ea273a6a9fad43b1e1379`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL url="https://www.redhat.com"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Jun 2025 06:03:26 GMT
ENV container oci
# Thu, 05 Jun 2025 06:03:26 GMT
COPY dir:9f1e3d7980aa1b8b007cf8dcf05575fff696655332be09ae87c8f7de7f00e923 in / 
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL "build-date"="2025-06-24T16:31:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Thu, 05 Jun 2025 06:03:26 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Jun 2025 06:03:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Jun 2025 06:03:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Jun 2025 06:03:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL org.label-schema.build-date=2025-05-28T10:54:28.565Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9861b44c7eec37c4ff6b68a464579ab4cbd5611e org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.2 org.opencontainers.image.created=2025-05-28T10:54:28.565Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9861b44c7eec37c4ff6b68a464579ab4cbd5611e org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.2
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Jun 2025 06:03:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Jun 2025 06:03:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:7073092d8bcd7b6d72345cfa87d8389a33f629b3c49ff887ad3a51c6ed8dfd83`  
		Last Modified: Tue, 24 Jun 2025 18:09:29 GMT  
		Size: 39.7 MB (39650665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616ce9756d7aa41a519b1da9e57da3ff98ccea556aa19feb2d46d9f0461f3023`  
		Last Modified: Wed, 25 Jun 2025 17:57:39 GMT  
		Size: 19.4 MB (19378058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1bd3b20cbcc8adb14f109be8452b150d6583afccc2947ff4d73e94a372de3`  
		Last Modified: Wed, 25 Jun 2025 20:16:39 GMT  
		Size: 355.0 MB (355024787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af03dca2ce5e875860dd5b8625ace40357ff295b2213fee70b85d78bdf3ebe9`  
		Last Modified: Wed, 25 Jun 2025 18:00:57 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400e64ea61d4d212bd49cb07da935c8bfccaab6dab71a9c29bd0bd3afc594282`  
		Last Modified: Wed, 25 Jun 2025 20:16:47 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff9219317d9208ffef5f97267a498df28fca219e58e5ab83a09a167deb9110b`  
		Last Modified: Wed, 25 Jun 2025 18:09:36 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a459af5154fbe4977708b9a9d7e16d05e16cba923071cf0f49ff11423f26d1dd`  
		Last Modified: Wed, 25 Jun 2025 18:09:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024c2d152bc83a2e289373bec30688ab920b5fa76452e682141994a8ef3d6779`  
		Last Modified: Wed, 25 Jun 2025 18:00:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e263ae51dfbb47aa4a01127e8b076e82038f7714150d0fef9fecd593c71d6696`  
		Last Modified: Wed, 25 Jun 2025 18:00:56 GMT  
		Size: 4.7 KB (4690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f50e6fc2163a83ee2041891dcd020d88bcdbf593d11fe6101c2a38ceef433b7`  
		Last Modified: Wed, 25 Jun 2025 18:09:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c300b8477630580e93c5c056deb185846ae6dd9080a9f8752915fb617d8a1545`  
		Last Modified: Wed, 25 Jun 2025 18:10:03 GMT  
		Size: 75.1 KB (75097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e7853a7d1b4b5a59f4f2e44e3e42953476f9e12c81d33ef0adc706200c2d08`  
		Last Modified: Wed, 25 Jun 2025 18:10:16 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff5ee8aff17b62e7d76ccb7f462af9c07ca36fd923667f194c4e58adf84fa3a`  
		Last Modified: Wed, 25 Jun 2025 18:10:22 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.2` - unknown; unknown

```console
$ docker pull kibana@sha256:9a5962e926faed76f027724c5ee89fbf70646f1d754dcb243952850ba516c426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5498065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c539cfc936f125be38aa01932c9c9c2a8887a67581cb94cdc4a56e82051200`

```dockerfile
```

-	Layers:
	-	`sha256:7a61aed7c715441724c05fbb92c297e48a87df3deed7fad8a957e372cee5ebed`  
		Last Modified: Wed, 25 Jun 2025 20:11:32 GMT  
		Size: 5.5 MB (5454880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b0244e4eeab9d03ca5413d45e55f3c65f066104b9ebeff1a1d948a7ee8bea2`  
		Last Modified: Wed, 25 Jun 2025 20:11:33 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:841ef84a014690ba295ea15fcde52201ba221744f4fce98a72290e0e4ebac67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.2 MB (441168529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88135df31e567756b3ceb1bcb01c909a9920b9dee8dbb2b196d4151844e7d322`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL url="https://www.redhat.com"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Jun 2025 06:03:26 GMT
ENV container oci
# Thu, 05 Jun 2025 06:03:26 GMT
COPY dir:837c51d2245269e7540005032254a14f4d0618334b5c45ecacf5b0c7968d0657 in / 
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 06:03:26 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL "build-date"="2025-06-24T16:36:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Thu, 05 Jun 2025 06:03:26 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Jun 2025 06:03:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Jun 2025 06:03:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Jun 2025 06:03:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 06:03:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL org.label-schema.build-date=2025-05-28T10:54:28.565Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9861b44c7eec37c4ff6b68a464579ab4cbd5611e org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.2 org.opencontainers.image.created=2025-05-28T10:54:28.565Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9861b44c7eec37c4ff6b68a464579ab4cbd5611e org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.2
# Thu, 05 Jun 2025 06:03:26 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Jun 2025 06:03:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Jun 2025 06:03:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Jun 2025 06:03:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Jun 2025 06:03:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:ba92c2079b2b21a2f178ace5ca98b5ef2d5cd02901c30e48729b7afe34ecd27e`  
		Last Modified: Tue, 24 Jun 2025 18:09:22 GMT  
		Size: 37.9 MB (37864307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff6d8a12862c4f2c3be59e6fe3c174f1102ae9321884fcf10eae8c4aff0dd22`  
		Last Modified: Wed, 25 Jun 2025 19:30:32 GMT  
		Size: 19.3 MB (19321441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2ddd52bc1fd463a8ac709f2abcb31aa22e69042732725c943615b0632ea875`  
		Last Modified: Wed, 25 Jun 2025 20:16:09 GMT  
		Size: 367.4 MB (367425608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75c4b16951b7af9cbefa7b073a535acc32d62b2c9916de0a3d02a87906a2fb0`  
		Last Modified: Wed, 25 Jun 2025 19:30:26 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5f4699e620708c472666af9fb977fd799b59885a4f0b6d3eebaae225471c4a`  
		Last Modified: Wed, 25 Jun 2025 19:30:29 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f596f95919a08a8acceeeeab7b10879f04f583952a48a261fc7eaed3f0123e2e`  
		Last Modified: Wed, 25 Jun 2025 19:30:26 GMT  
		Size: 5.2 KB (5220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84888a193e57651c470407df142a4599a29d62f889542662f1583b291320aba`  
		Last Modified: Wed, 25 Jun 2025 19:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0205426ba9dc6acc17b666b4483f38b0383e3cb696de9529435db8c3f2b8f9fa`  
		Last Modified: Wed, 25 Jun 2025 19:30:26 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffc8a9394db94888819efdf51824b66e8b3ad9e1a967edb7999b16b0795b200`  
		Last Modified: Wed, 25 Jun 2025 19:30:27 GMT  
		Size: 4.7 KB (4688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6af3f8a8f420720cad8c60166fd89ecfcbaef12afadec0515bd59ef89c81ea3`  
		Last Modified: Wed, 25 Jun 2025 19:30:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da364773d147df1b2eab242e11b727ec0ea9b4a4a73c4ef5665af086c121dc4`  
		Last Modified: Wed, 25 Jun 2025 19:30:28 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14172a2d00e0dc69c211b85844dc9bb3a2eacbff7a21bdd83a0e8b8c75f7f2ac`  
		Last Modified: Wed, 25 Jun 2025 19:30:28 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b98317dc09b7b78764a0420fdec2d14d576c7f1be1d4472359a32534689aa7`  
		Last Modified: Wed, 25 Jun 2025 19:30:29 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.2` - unknown; unknown

```console
$ docker pull kibana@sha256:383539b62a2045f3f7c80670944d8dec8f96b3ff47d4ff232de0b2302713dfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5497000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508debf8750cc3ed73c47f71d0f62a03e07e2d332c1914b52be943d0f4d41a30`

```dockerfile
```

-	Layers:
	-	`sha256:baf2ee09cce79af30df311809c4352d40e265e5e3fae72889d603a844b75713a`  
		Last Modified: Wed, 25 Jun 2025 20:11:39 GMT  
		Size: 5.5 MB (5453558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09730c4c3bc155cbb0cd9ed22f685cc77ce2fa0c425843cf2fbda35768abf370`  
		Last Modified: Wed, 25 Jun 2025 20:11:40 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
