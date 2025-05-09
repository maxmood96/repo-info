<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.5`](#kibana8175)
-	[`kibana:8.18.0`](#kibana8180)

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
		Last Modified: Wed, 09 Apr 2025 01:20:23 GMT  
		Size: 3.4 MB (3394739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a968912ba0d60abd66f531a258a09ebe22f75b4fee941682bf1212e2dbb3fa`  
		Last Modified: Wed, 09 Apr 2025 01:20:23 GMT  
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
		Last Modified: Wed, 09 Apr 2025 08:12:20 GMT  
		Size: 10.6 MB (10576633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1acae769c9db7fc15bd20201802ac7e10a23d935608a0fdbe1c04f4b051b17`  
		Last Modified: Wed, 09 Apr 2025 08:12:19 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289bfd26de33519e5fb64b1a0fc00e92a12dbd302ba5c929349f2c28c4cfc5ba`  
		Last Modified: Wed, 09 Apr 2025 08:12:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b21ae865a53c3ea076ac5381f0f5b36d2e3f1b67699363cb66853fd425efe3`  
		Last Modified: Wed, 09 Apr 2025 08:12:21 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daeafc0585c76c4a0b1b7e694ac8c4d58d9a011523646dd76c98a4b2d647709b`  
		Last Modified: Wed, 09 Apr 2025 08:12:20 GMT  
		Size: 5.3 KB (5279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e300d5851d0849367fd9bffde9ba6dec0bffa1bfd4860fcf3c998a1a4b6fb124`  
		Last Modified: Wed, 09 Apr 2025 08:12:29 GMT  
		Size: 307.0 MB (307034779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6646fe97b0ceb27b81a05a1f631a3d6102837b49fe14b05f9d08f67e5a2fa0b`  
		Last Modified: Wed, 09 Apr 2025 08:12:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663059830d64f58718a20357cd46fff1b0625d2a7c675327068e1424221bff9a`  
		Last Modified: Wed, 09 Apr 2025 08:12:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b88cde54938cac0fd124160dc99d956476aa7b01d63439ddbe61d4e8a8800`  
		Last Modified: Wed, 09 Apr 2025 08:12:22 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1176c4ee36b5e7806234ed28bd30c9775c7cb1f09792166680a384677da05cc4`  
		Last Modified: Wed, 09 Apr 2025 08:12:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46e31733d9faf72979d93872dc5d8ceec1ebf1e0041652e916a79c172c11cd0`  
		Last Modified: Wed, 09 Apr 2025 08:12:23 GMT  
		Size: 183.4 KB (183419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8328505486c5e27455912042380bdf45ba029a4de443a75c077d13ab2aaafc36`  
		Last Modified: Wed, 09 Apr 2025 08:12:24 GMT  
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
		Last Modified: Wed, 09 Apr 2025 08:12:20 GMT  
		Size: 3.4 MB (3394990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9133ef35b54eb2768d5644052484906f153a1dd2ae7cd37bf7286689c6312b`  
		Last Modified: Wed, 09 Apr 2025 08:12:19 GMT  
		Size: 44.8 KB (44785 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.5`

```console
$ docker pull kibana@sha256:f19d5420817860bc93843400a71e8423c64d119359f146840245c22fcc113b1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.5` - linux; amd64

```console
$ docker pull kibana@sha256:f39fa8e18a4736da6a0599613a08c120bb5a160fe0cbcb0a40002d570ca870f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 MB (396491519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05cb3e1042c22e9c5123d8adc1b36f2d700365beb362d761418766b3e87425f`
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
# Tue, 15 Apr 2025 11:26:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 15 Apr 2025 11:26:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN fc-cache -v # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
WORKDIR /usr/share/kibana
# Tue, 15 Apr 2025 11:26:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 15 Apr 2025 11:26:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
LABEL org.label-schema.build-date=2025-04-09T20:15:24.174Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=1b0d1f7623ae3403e69092138ea8905314ddd819 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.5 org.opencontainers.image.created=2025-04-09T20:15:24.174Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=1b0d1f7623ae3403e69092138ea8905314ddd819 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.5
# Tue, 15 Apr 2025 11:26:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 15 Apr 2025 11:26:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 15 Apr 2025 11:26:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eef2493b8b415f7620440191a02b3695e1499534060a1be954e3af05c87509`  
		Last Modified: Thu, 08 May 2025 17:56:35 GMT  
		Size: 10.7 MB (10725899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b739297d831af9896285d3962e4c8876d76f46970a5814397c375a758f9ab498`  
		Last Modified: Thu, 08 May 2025 17:56:56 GMT  
		Size: 341.6 MB (341583009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db87e529a7d3aa9dd6d76c3112cc74bd16d0c7997308c18a958827d92a61c2f`  
		Last Modified: Thu, 08 May 2025 17:56:35 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae0c7b9d360ba2efe812fa96d0ad5f258550964097eea120a23a8429b04c8c6`  
		Last Modified: Thu, 08 May 2025 17:56:36 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d509cc50c8c602da14518f9fb1bdc9734c3092d7c133e6ad8c585c9696a09f40`  
		Last Modified: Thu, 08 May 2025 17:56:36 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e0f9ecf53e081bfa45c9404d49865033a58b2d3323d5695360d3b1fc0c359b`  
		Last Modified: Thu, 08 May 2025 17:56:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ab6bacf1090763850de40b17b2c767818e800ae39a47b8351c9309d6937af0`  
		Last Modified: Thu, 08 May 2025 17:56:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da820c429190be5338e030c83ea99e5ab7b8a410c2e2ad5d34314b90fb3506d`  
		Last Modified: Thu, 08 May 2025 17:56:36 GMT  
		Size: 4.7 KB (4726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b44b6f9824b0f47e92a8f35e688087cf489857f8ee2640b1092637e1815ef4e`  
		Last Modified: Thu, 08 May 2025 17:56:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4942b1bdab29085d1f02c8814d3f54718aa2b19782d2d5992e4a0258232d1386`  
		Last Modified: Thu, 08 May 2025 17:56:37 GMT  
		Size: 189.4 KB (189428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3075cccd5c56004b5af4898b27151d0611a197588d947acd1b003b11f6eb53d9`  
		Last Modified: Thu, 08 May 2025 17:56:37 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.5` - unknown; unknown

```console
$ docker pull kibana@sha256:e7d0b6a725685dfb210bb3d71e320f70680e750f6678bdd4e44f6e4f1ad210d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4433478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a618d023dfbd69447719b3908a8faef01c8d940b70400221ea583bb59743469`

```dockerfile
```

-	Layers:
	-	`sha256:59b4dddcd9b95811e34ac43c24706a2d397f0edfaaf186b600a02e5d23c89b73`  
		Last Modified: Tue, 15 Apr 2025 17:58:47 GMT  
		Size: 4.4 MB (4392798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c280a36ffc815a7121d1caf7964f87e3e3c64d4f512e199a6fcf2b35386b2807`  
		Last Modified: Tue, 15 Apr 2025 17:58:47 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:53e2f3e1eba48246f13ab5617cc7ac041319f76a93346a70d0a2a1bc1c62fc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.3 MB (407343186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a024eebb4a68651c20e2cfc5e067994afac69b8efff4fdcf09b043716497eacb`
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
# Tue, 15 Apr 2025 11:26:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 15 Apr 2025 11:26:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN fc-cache -v # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
WORKDIR /usr/share/kibana
# Tue, 15 Apr 2025 11:26:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 15 Apr 2025 11:26:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 11:26:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 15 Apr 2025 11:26:34 GMT
LABEL org.label-schema.build-date=2025-04-09T20:15:24.174Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=1b0d1f7623ae3403e69092138ea8905314ddd819 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.5 org.opencontainers.image.created=2025-04-09T20:15:24.174Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=1b0d1f7623ae3403e69092138ea8905314ddd819 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.5
# Tue, 15 Apr 2025 11:26:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 15 Apr 2025 11:26:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 15 Apr 2025 11:26:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388ba6dab9a0f52eba8e0baeb884f4497b3483d4714b11c0afd7ca711ba9c98`  
		Last Modified: Thu, 08 May 2025 17:14:04 GMT  
		Size: 10.6 MB (10576615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fa0ee6b9d4aff33e210a27679516eaa8a02e199ce753aa78df6c900e6dfdf4`  
		Last Modified: Tue, 15 Apr 2025 18:18:56 GMT  
		Size: 354.1 MB (354123132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceaea4acdf1fed537460b340a54a5a6bd0c3e091f94a07a6b5d8036d56690eb`  
		Last Modified: Tue, 15 Apr 2025 18:18:48 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d2fa697075c89aaced047c9a2837f1b8efe63c03780bf15900e8e2823ed1bd`  
		Last Modified: Tue, 15 Apr 2025 18:18:49 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4438f7f3106d9d34b8e314720d29f0f57c11524065e809b02d86c321c09dbcbd`  
		Last Modified: Tue, 15 Apr 2025 18:18:49 GMT  
		Size: 5.3 KB (5285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2e80216734ba203a767bb9185f904bfa4be94bf68212f5908beacd7101fad`  
		Last Modified: Tue, 15 Apr 2025 18:18:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8985b53bb5f703cbf0cabde11edf0591bd48fe1715346988230d63868d3bb96`  
		Last Modified: Tue, 15 Apr 2025 18:18:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1902a2536e15faba1014aaeb6c07afde51463fbc1871558ba384db09d8b36351`  
		Last Modified: Tue, 15 Apr 2025 18:18:51 GMT  
		Size: 4.7 KB (4729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ead6d04778a4ec544c4af79d5df36fdb8d3362d6a343689e598cbf95c8aad`  
		Last Modified: Tue, 15 Apr 2025 18:18:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f3b99611114efca02afc36bed5bb2e6fe53703bc151131abf6eba94f0bfc6e`  
		Last Modified: Tue, 15 Apr 2025 18:18:51 GMT  
		Size: 183.4 KB (183418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fbf2a1251716ffc8fc2e6ad3e3ba66e960b83d6359ae8f6d964caa8e4323af`  
		Last Modified: Tue, 15 Apr 2025 18:18:52 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.5` - unknown; unknown

```console
$ docker pull kibana@sha256:72eb88a696221d89e61494fcb2339863c723610e6d5968a734b0f4de1fac56b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4433977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea760f900151bf9a1638a4fb45fd01ee6d336eb355b2d5c6f5e08a043fac9a7d`

```dockerfile
```

-	Layers:
	-	`sha256:9898be8a54a0f8391e1f2361a96b1ba7cb245c93e4297fcfb2cf84bad45a9c56`  
		Last Modified: Tue, 15 Apr 2025 18:18:49 GMT  
		Size: 4.4 MB (4393049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667973fee2c1c1df0a837a32e06aac3487c4f513fd3b3811db59701c58c40560`  
		Last Modified: Tue, 15 Apr 2025 18:18:48 GMT  
		Size: 40.9 KB (40928 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.0`

```console
$ docker pull kibana@sha256:04c0fc150f3a932719c0cec11de303b210baa2f63a42a8c7b4dd07f5521167e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.0` - linux; amd64

```console
$ docker pull kibana@sha256:a7ece5795fd503b45b0f11d1ee41491e3839c5c36c7043d54844f974ed8c2ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.8 MB (413763021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7840218257a244d67795dd89594d269ea536c50504249078242c7e66eda9d314`
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
# Tue, 15 Apr 2025 06:36:04 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 15 Apr 2025 06:36:04 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN fc-cache -v # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
WORKDIR /usr/share/kibana
# Tue, 15 Apr 2025 06:36:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 15 Apr 2025 06:36:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
LABEL org.label-schema.build-date=2025-04-10T11:09:30.020Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c220d2938cd718bb332afb07baaf95999eb28759 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.0 org.opencontainers.image.created=2025-04-10T11:09:30.020Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c220d2938cd718bb332afb07baaf95999eb28759 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.0
# Tue, 15 Apr 2025 06:36:04 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 15 Apr 2025 06:36:04 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 15 Apr 2025 06:36:04 GMT
USER 1000
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdf480a4370be5fc8507bb953e74d7dfa6e0a8cd3fbf9eba00d3d827a86b4c7`  
		Last Modified: Thu, 08 May 2025 17:18:40 GMT  
		Size: 10.7 MB (10725906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f038815a73cd8e69dd3c850b0bed53e4f2384213657836817f7aa1c403cb746d`  
		Last Modified: Thu, 08 May 2025 17:42:31 GMT  
		Size: 358.9 MB (358854496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0bc206e07004511eff59803807580b668eaee73831261fe478669c758a1de`  
		Last Modified: Thu, 08 May 2025 17:18:42 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b861a18e2e3b6ed54016074e58c0c04adb802460defe449df10c6157aafb6d9c`  
		Last Modified: Thu, 08 May 2025 17:18:48 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170b4e92d9c98906c9b796fb6f21f43d61e4fe54156b87689952dc0d9e61c99e`  
		Last Modified: Thu, 08 May 2025 17:18:49 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0706f45da36ae86f79aa594baaef3c7a112112d79b0f413bd520b009b21e0`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f280f28a66927f16efa6e558ce9b848e1892655c26f5db89bacedf46e8b71531`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a31ad09784c4471d89a891d78429b8eca7c253ff9694a1d5e53d867e4bf7dea`  
		Last Modified: Thu, 08 May 2025 17:18:51 GMT  
		Size: 4.7 KB (4749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e3570575f506e6bae56c1aaa58320b5e0d3f1d03e9c7657ac918545c51e607`  
		Last Modified: Thu, 08 May 2025 17:18:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e4e4da59f02ee48a8dc6d048295356ee57de8398120f96739b55c39e87d54d`  
		Last Modified: Thu, 08 May 2025 17:18:52 GMT  
		Size: 189.4 KB (189428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a20f4668f36e8443f6acb645663530a00b7b8fef99efaca1de2525ab1a9df6b`  
		Last Modified: Thu, 08 May 2025 17:18:52 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.0` - unknown; unknown

```console
$ docker pull kibana@sha256:e19836d043f88f9f86f148abb057b5ef6290af65cd0669c16f4dc83a410e2782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4670388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab2a66f0361189553cdf57eb4606caef1b2f29f18fc078bff361ef7bc5e1853`

```dockerfile
```

-	Layers:
	-	`sha256:b736d4a2608927e27b0b24c0f7bbe00ba847dd58b04157781a079a65fb6c81f8`  
		Last Modified: Wed, 16 Apr 2025 17:18:29 GMT  
		Size: 4.6 MB (4629708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8da4fd90662b17789692fc1a0951459bb20d83d084f45d947c7675aab9bdc6`  
		Last Modified: Wed, 16 Apr 2025 17:18:29 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:919bfbc4bc5d65f8b84bdecbbab34a9f8dc9a4e31ddcb32061e8e93228a080c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.6 MB (424596456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f20f775ca122fb7e7ada7af7008bc0babf33eb030e1ffd2f6642c34a568976`
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
# Tue, 15 Apr 2025 06:36:04 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 15 Apr 2025 06:36:04 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN fc-cache -v # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
WORKDIR /usr/share/kibana
# Tue, 15 Apr 2025 06:36:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 15 Apr 2025 06:36:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Apr 2025 06:36:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 15 Apr 2025 06:36:04 GMT
LABEL org.label-schema.build-date=2025-04-10T11:09:30.020Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c220d2938cd718bb332afb07baaf95999eb28759 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.0 org.opencontainers.image.created=2025-04-10T11:09:30.020Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c220d2938cd718bb332afb07baaf95999eb28759 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.0
# Tue, 15 Apr 2025 06:36:04 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 15 Apr 2025 06:36:04 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 15 Apr 2025 06:36:04 GMT
USER 1000
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388ba6dab9a0f52eba8e0baeb884f4497b3483d4714b11c0afd7ca711ba9c98`  
		Last Modified: Thu, 08 May 2025 17:14:04 GMT  
		Size: 10.6 MB (10576615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f150b2f1dcc1cec78e70c2bf14007a886335d208108b4657f2a2aa265cc37c`  
		Last Modified: Thu, 08 May 2025 17:35:54 GMT  
		Size: 371.4 MB (371376388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce93d5def7c23f5cf97b0e2118c328b9272b02f6e4efc3b0657dc396129c5f5`  
		Last Modified: Thu, 08 May 2025 17:14:00 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b01e5a369b1c0000250d76911e3ea0025f8b93ecfdeead899786da76bd69bb`  
		Last Modified: Thu, 08 May 2025 17:14:05 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bfb3aba398af0ca2477ca904444c5e6ad4bc8bbde91bb9a376e1a28de76fdd`  
		Last Modified: Thu, 08 May 2025 17:14:01 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfcedd23499fe5be3e9cf3f796c7131f0b298259303d7234c52b4660c0f451f`  
		Last Modified: Thu, 08 May 2025 17:14:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0407e1da66c8b95f38acb8219ef5f135f3863311f4072a6e904b43fc8455e`  
		Last Modified: Thu, 08 May 2025 17:14:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35698ce674d0ee30ab37020b64d48cd268c04a6713e0b3f274c4aaf32af402fb`  
		Last Modified: Thu, 08 May 2025 17:13:58 GMT  
		Size: 4.8 KB (4752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a79f39946af70ca954d73b4af7e249c59e9959d2573d4472a8a6ddc9a348f50`  
		Last Modified: Thu, 08 May 2025 17:14:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790f72551e0b3f2c63228f2143e594ecb56c09b566e59b6d0835f4fd800a6c6`  
		Last Modified: Thu, 08 May 2025 17:14:01 GMT  
		Size: 183.4 KB (183418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e1cabb70e688a8d40a68218a6fda92fe3db665aa3c546726c3ca44cb404951`  
		Last Modified: Thu, 08 May 2025 17:13:59 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.0` - unknown; unknown

```console
$ docker pull kibana@sha256:e9fc915277c7fb289945d50456b1aca813b0855eb39c35a87ae080cb42915077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4670887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f66a63d934abe8751177970ab5a37ffb4b67db73e7b41827d66a00cec171fd5`

```dockerfile
```

-	Layers:
	-	`sha256:37f725c21907f8bbfad61098756bc8c9dccb8c207a8efe8110f46eb6209d6f5d`  
		Last Modified: Wed, 16 Apr 2025 17:25:00 GMT  
		Size: 4.6 MB (4629959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed06f8c516dcbe6fe6c90f797a2fd0e8cc79808516ce78dc0e7b54f8ba0fc78`  
		Last Modified: Wed, 16 Apr 2025 17:25:00 GMT  
		Size: 40.9 KB (40928 bytes)  
		MIME: application/vnd.in-toto+json
