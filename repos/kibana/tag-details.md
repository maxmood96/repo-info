<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.6`](#kibana8176)
-	[`kibana:8.18.1`](#kibana8181)
-	[`kibana:9.0.1`](#kibana901)

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
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ea456835084ef3b2a83ca41b1c067b32ddb750d7e316b44e22cbc2653e8f1d`  
		Last Modified: Wed, 09 Apr 2025 01:20:23 GMT  
		Size: 10.7 MB (10725898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c9817efc0a2eb6e3ff008c789b87d7501d369492126b875ea9848e9be43979`  
		Last Modified: Wed, 09 Apr 2025 01:20:23 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357d3e9a90f4743bace292564a50825dc3c5cf58abcf51c6f11991b827e849f4`  
		Last Modified: Wed, 09 Apr 2025 01:20:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0501e9c0b84dcc25fcd1fc075bf596c575c374d42c4163af4ab294894a3fcf56`  
		Last Modified: Wed, 09 Apr 2025 01:20:24 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e1bbff07da50d015c339e76757d5525bb9b327b744a2c25d8108a9637265c`  
		Last Modified: Wed, 09 Apr 2025 01:20:24 GMT  
		Size: 5.3 KB (5299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f91260925ca5ca55382d2a6645e5c3357b749b61972fc7ebfa16e30ecce908`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 294.5 MB (294493406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e7c4853810a90b40f861caa0e10973ff539f6140127a00039fdb9c53ccf1d9`  
		Last Modified: Wed, 09 Apr 2025 01:20:24 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bde9374be7f7403d62304b82425d7fd00ef33fb5750447d4754087d07d87c8c`  
		Last Modified: Wed, 09 Apr 2025 01:20:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c9e27e22d6c4fc57e1701034dc34ac7ec224e260ac31cc421660fa5760bfa2`  
		Last Modified: Wed, 09 Apr 2025 01:20:25 GMT  
		Size: 4.5 KB (4501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c1873d13033612c9c0c18d33dc984e1b79d82ab1d09f0be505bdca193a3a1d`  
		Last Modified: Wed, 09 Apr 2025 01:20:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ec2c24e65a384564091f48529373c3eb804015485c26b9d48e951947c5e869`  
		Last Modified: Wed, 09 Apr 2025 01:20:26 GMT  
		Size: 189.4 KB (189428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9579d7a2d933fc43b65370dc8622c069b4cf339780945521bb1ec694950567`  
		Last Modified: Wed, 09 Apr 2025 01:20:26 GMT  
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
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a001e434c4436c8bff67d5c1cc60f2623028ebf558c3a5e5f7fb87816ad84390`  
		Last Modified: Fri, 09 May 2025 19:03:38 GMT  
		Size: 10.7 MB (10725868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb6c8172f42ccddb94feca5dc854fc85de5c182d6858467f38533c36a2bcb93`  
		Last Modified: Fri, 09 May 2025 19:03:43 GMT  
		Size: 342.1 MB (342082257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2468c87d0c5d74b9af18c832a57db8b83de4c63623bf5856536bed1288b4a4d`  
		Last Modified: Fri, 09 May 2025 19:03:38 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9576421bd051a1f6878ea9e26b79f42bee0b6f9715d3fb33a3e09ad8411ce41d`  
		Last Modified: Fri, 09 May 2025 19:03:38 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0707752b514431a490efcdbb31f3993c10a9be597ba86d20068688f10b3a03e3`  
		Last Modified: Fri, 09 May 2025 19:03:38 GMT  
		Size: 5.3 KB (5276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf42d675f2039095220de79b5b04cc629c8686ee500f5aaf19aca056f717616`  
		Last Modified: Fri, 09 May 2025 19:03:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ea22231532882f07501df82aab864faae27cefc235a31e61a71e25303e9b27`  
		Last Modified: Fri, 09 May 2025 19:03:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a3df13ed1f02fd58d6d4c2494f6c27fb9657986c98c4a37ca0fca761b4622`  
		Last Modified: Fri, 09 May 2025 19:03:39 GMT  
		Size: 4.7 KB (4726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de3db135547d5a546fedbc60de245429b851d75d3a801368d341fc699cb5088`  
		Last Modified: Fri, 09 May 2025 19:03:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7952248b81cded371966ff51619727f6f68c30f67ddc86d708b9f8a6b17e5366`  
		Last Modified: Fri, 09 May 2025 19:03:40 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d010667ca15d7de83c3127ee024c321d4bc40ef9a7d20383a6b1eb5d70050ff`  
		Last Modified: Fri, 09 May 2025 19:03:40 GMT  
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
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ccd575a42dec4f47ce6b7c881155e826b5607c4ae0b24d5b1c6e251081332f`  
		Last Modified: Fri, 09 May 2025 20:24:51 GMT  
		Size: 10.6 MB (10576710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5fe48a70342ee31bc60cfc811d929541eb99d9ebb5f83a0393ef456820da69`  
		Last Modified: Fri, 09 May 2025 20:24:59 GMT  
		Size: 354.5 MB (354471260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ebad1d1e747c6255d65e2c4f893a3170b1f76241caf662a9704ef6112e6d3`  
		Last Modified: Fri, 09 May 2025 20:24:51 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a7d40cef6ccd89a205f13b4088e8e2cd70b0c4d7f3ec9447f4142339601d75`  
		Last Modified: Fri, 09 May 2025 20:24:52 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7865ac34c76184d343fcf8eab6d316bd6d35162bbff5c2c6a9493a33aecd871e`  
		Last Modified: Fri, 09 May 2025 20:24:52 GMT  
		Size: 5.3 KB (5280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cd2b5ea96b4241755c77ce62e808fcbf6773a8fa00973e1e50efe24497a004`  
		Last Modified: Fri, 09 May 2025 20:24:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f606e28e60b810a4974f28eaa50b9f9161b9ef2661eb814becd216c5536537a3`  
		Last Modified: Fri, 09 May 2025 20:24:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b46bdd2348534171bdb0dbde947710e4e12403856ce6e31d097f75c54a5dd6`  
		Last Modified: Fri, 09 May 2025 20:24:53 GMT  
		Size: 4.7 KB (4732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da982d9084c800d269075bc543e4b767de9498e43063bccae9a166f486ed8662`  
		Last Modified: Fri, 09 May 2025 20:24:54 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a842fe9e93726d5c37369f73412990e41e12d0425923bfbc792a58254973a4`  
		Last Modified: Fri, 09 May 2025 20:24:54 GMT  
		Size: 183.4 KB (183422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189be11abd167f33dee5cdb34f1abff92d1219ca5ee36f518e11143bad3dc77b`  
		Last Modified: Fri, 09 May 2025 20:24:54 GMT  
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

## `kibana:8.18.1`

```console
$ docker pull kibana@sha256:fdef03ed0ae377b05d2d2fcc9eee96cc04c4f54e1dd2dfddd530c8fdd462adda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.1` - linux; amd64

```console
$ docker pull kibana@sha256:d86614412ebc445d64a6b1153dc9ffbfd2c181ebf5803b6e83d5bf344fa5c538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414235124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a86f1b9093b813fff2a663cfe6acce14ed12f153deb30319edfaa8d3069d54`
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
# Tue, 06 May 2025 09:07:22 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 May 2025 09:07:22 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN fc-cache -v # buildkit
# Tue, 06 May 2025 09:07:22 GMT
WORKDIR /usr/share/kibana
# Tue, 06 May 2025 09:07:22 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 May 2025 09:07:22 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 09:07:22 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 May 2025 09:07:22 GMT
LABEL org.label-schema.build-date=2025-04-30T11:08:13.935Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d095a26b905eabe7a75cb980b65aea0ad319b8fe org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.1 org.opencontainers.image.created=2025-04-30T11:08:13.935Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d095a26b905eabe7a75cb980b65aea0ad319b8fe org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.1
# Tue, 06 May 2025 09:07:22 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 May 2025 09:07:22 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 May 2025 09:07:22 GMT
USER 1000
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d265a169a8d4a2327ca827962fa07434eb451ce2d9cd42e1120437dd12964a`  
		Last Modified: Fri, 09 May 2025 19:03:45 GMT  
		Size: 10.7 MB (10725933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e7173d8ea5962211c94bff17eceed2ad0f4f982174666a46d2d5a7a4814a58`  
		Last Modified: Fri, 09 May 2025 19:03:50 GMT  
		Size: 359.3 MB (359326551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e465d3f97530b1c87a01f591864fb817b064aa649e33eaa241937946fb1feaf`  
		Last Modified: Fri, 09 May 2025 19:03:44 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73839d42b12fec79a1d2d1ecf89a14b4f3509180e27543cda9177174e7199bd`  
		Last Modified: Fri, 09 May 2025 19:03:45 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a3f949c940f3fbc10fb2161ce075b7e7835d5bb70b991c43d82b8958054107`  
		Last Modified: Fri, 09 May 2025 19:03:45 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e348283ae679ca194aa41431f783cfa4b0f5dabb343e06ec4b71c140bca689`  
		Last Modified: Fri, 09 May 2025 19:03:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca421abc2a4b9bc5d87010751f438fbfea034d48a3420f62e9802c27bbf0ef3`  
		Last Modified: Fri, 09 May 2025 19:03:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a747d3ecf015fd605ca649e7206cc3440428600c62b20ceafc2a97e607e552a2`  
		Last Modified: Fri, 09 May 2025 19:03:46 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7333da274fd8727cfb6f31e547088cea7a9fdf26a30a116948445da8f6fb1b`  
		Last Modified: Fri, 09 May 2025 19:03:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccb9e3179114c3b065cf22c1e393bde7854da6ae7cf0943a6221d8fcfa39191`  
		Last Modified: Fri, 09 May 2025 19:03:47 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013cb8ea06645f5e56058cf6d37459472dc613136d77dd43327f35eb4eadd721`  
		Last Modified: Fri, 09 May 2025 19:03:47 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.1` - unknown; unknown

```console
$ docker pull kibana@sha256:dad648d5015ce149b7780265e53ac62f0cb048e45bd941eb1a5b19c4ca67f0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4671666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec41ae85dbef1e5d7a31b6daaa601049bef84a77c7fcc576435c5cf6a02e666`

```dockerfile
```

-	Layers:
	-	`sha256:a3b326991a810d4b82fda96fa611714046ea7a1e9faa22dbaa1d7df556c7807c`  
		Last Modified: Fri, 09 May 2025 19:03:45 GMT  
		Size: 4.6 MB (4630986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941479945ad51c9dc59367b9412d69331d676aa37ac2317c80a9f77ce5cf0200`  
		Last Modified: Fri, 09 May 2025 19:03:44 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:2e61307eac80ce551137014eecd6838e9f0fbc712f1c56bad6af6b360681faf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 MB (424933736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c7bcbb9cecdcadfcd994002092e98989778ca981706cfb45cfbf2587881e12`
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
# Tue, 06 May 2025 09:07:22 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 May 2025 09:07:22 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN fc-cache -v # buildkit
# Tue, 06 May 2025 09:07:22 GMT
WORKDIR /usr/share/kibana
# Tue, 06 May 2025 09:07:22 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 May 2025 09:07:22 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 May 2025 09:07:22 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 09:07:22 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 May 2025 09:07:22 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 May 2025 09:07:22 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 May 2025 09:07:22 GMT
LABEL org.label-schema.build-date=2025-04-30T11:08:13.935Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d095a26b905eabe7a75cb980b65aea0ad319b8fe org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.1 org.opencontainers.image.created=2025-04-30T11:08:13.935Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d095a26b905eabe7a75cb980b65aea0ad319b8fe org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.1
# Tue, 06 May 2025 09:07:22 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 May 2025 09:07:22 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 May 2025 09:07:22 GMT
USER 1000
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ccd575a42dec4f47ce6b7c881155e826b5607c4ae0b24d5b1c6e251081332f`  
		Last Modified: Fri, 09 May 2025 20:24:51 GMT  
		Size: 10.6 MB (10576710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d559b2cd65176bf5fc999f3913b2cd5146a9a0398393e8c20ef267b8f97ada`  
		Last Modified: Fri, 09 May 2025 20:32:21 GMT  
		Size: 371.7 MB (371713551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef7de236030881d19280385fdc5329cf4f3cf63584c52a381632a7e71cfb579`  
		Last Modified: Fri, 09 May 2025 20:32:13 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ef28e4235c529d1bcd0b9bb8186a03bf3dc18c5473b9b074aff6e549ecd1cc`  
		Last Modified: Fri, 09 May 2025 20:32:14 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d3a7c266b09df01bbad1f12b3970e069b70617bf3c50394dbb03309c71762c`  
		Last Modified: Fri, 09 May 2025 20:32:13 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f537cb7dfc2ab9640b4ffdb70aaba4e4bf53a75a69fb5d4b6fd5b055cdaf64d`  
		Last Modified: Fri, 09 May 2025 20:32:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbf45d55d567a25ad5fa34f43f3c32610fb280b6f2695e9e8230db3acb3028d`  
		Last Modified: Fri, 09 May 2025 20:32:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efd8d1ae6edc72d79353814a68bac45de146b5d205cb18060e8e866812f85d3`  
		Last Modified: Fri, 09 May 2025 20:32:15 GMT  
		Size: 4.8 KB (4764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b4a49d1e41d16c5a4ab429ed103450cda0ece7e638b2cd30cd9f23c8ff2b30`  
		Last Modified: Fri, 09 May 2025 20:32:15 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8c29b9c259fd9a3c6334cd8ad2be6acec2524b7b64d246a3e35512168cdc85`  
		Last Modified: Fri, 09 May 2025 20:32:15 GMT  
		Size: 183.4 KB (183423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc688fa66c09884b54e195d55eea1f68631318d74b93ec1cfc76e121435ac05`  
		Last Modified: Fri, 09 May 2025 20:32:16 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.1` - unknown; unknown

```console
$ docker pull kibana@sha256:aaff86150ef9baf232ed85078bd422409cb960e287eda03a9def963cf39e5a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4672165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fe0b88b28995ba78b6a15bea30be5b0f56f5023b93ee0f3ee19f356c77ec6f`

```dockerfile
```

-	Layers:
	-	`sha256:38273aa4b49c7c0639a4826f8b1430080aad0ce372fe824a8f92a9bfcda8a611`  
		Last Modified: Fri, 09 May 2025 20:32:13 GMT  
		Size: 4.6 MB (4631237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:216d64e6fab5564d6619596f1cd2113efd2558375a9419ddb8ecaf55e5088e62`  
		Last Modified: Fri, 09 May 2025 20:32:13 GMT  
		Size: 40.9 KB (40928 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.1`

```console
$ docker pull kibana@sha256:8ad2c629475b62a8bf46d51bc7a7e10f668c09f8f8c702431ba6c086b8405bce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.1` - linux; amd64

```console
$ docker pull kibana@sha256:d8fac2e4f56d103079ac91946d45aece0e71d9f065d2b3aaedc03e5d1a44990a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.6 MB (430564005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c67d0f3a5fe878ec69b23b318b6f1bfc97046089228f567b4fa58b868fa11`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL url="https://www.redhat.com"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Apr 2025 15:46:09 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Apr 2025 15:46:09 GMT
ENV container oci
# Mon, 28 Apr 2025 15:46:09 GMT
COPY dir:6446605ab0b234f56f65ee435d3f1ec849764d2e258ed27d2cce90dc59963fc1 in / 
# Mon, 28 Apr 2025 15:46:09 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 28 Apr 2025 15:46:09 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 15:46:10 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 28 Apr 2025 15:46:10 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Mon, 28 Apr 2025 15:46:10 GMT
LABEL "build-date"="2025-04-28T15:45:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Fri, 09 May 2025 04:49:38 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 09 May 2025 04:49:38 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN fc-cache -v # buildkit
# Fri, 09 May 2025 04:49:38 GMT
WORKDIR /usr/share/kibana
# Fri, 09 May 2025 04:49:38 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 09 May 2025 04:49:38 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 09 May 2025 04:49:38 GMT
LABEL org.label-schema.build-date=2025-04-30T12:17:16.628Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=0df588b1a307954a3103991180df23c70184d34c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.1 org.opencontainers.image.created=2025-04-30T12:17:16.628Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=0df588b1a307954a3103991180df23c70184d34c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.1
# Fri, 09 May 2025 04:49:38 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 09 May 2025 04:49:38 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 09 May 2025 04:49:38 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 09 May 2025 04:49:38 GMT
USER 1000
```

-	Layers:
	-	`sha256:0e8d054612b4f0035f5c5cbccf286c0144a13098091c04bd08f3376a1adcaa1d`  
		Last Modified: Mon, 28 Apr 2025 16:55:19 GMT  
		Size: 39.7 MB (39714553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e1f90d8a0cea29a2ddc1b1088757e29b56ee09c3a0fa1f54ec52344d84411b`  
		Last Modified: Fri, 09 May 2025 19:03:49 GMT  
		Size: 19.4 MB (19372050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c28c122270f908e5d060a2f9c65bb73b342a86b52944b0a8b11a79fee2901ff`  
		Last Modified: Fri, 09 May 2025 19:03:54 GMT  
		Size: 354.9 MB (354918786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af4e68fadc3e0edb59b35c477169a884bd33d3311090b2dac8b37b40219ef6f`  
		Last Modified: Fri, 09 May 2025 19:03:49 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4724631101d8f801beec0af5d1af9f923c05db33863b1d72de0018c18440e3`  
		Last Modified: Fri, 09 May 2025 19:03:49 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261c214a9d34fd7e3f0f8446c93711cd8f68c03ab7edc18cfd459e480e94388b`  
		Last Modified: Fri, 09 May 2025 19:03:49 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9928aaa4c4658026b84425a227bf4518caa3a857f8136eb29cb20c6a65e78859`  
		Last Modified: Fri, 09 May 2025 19:03:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba22a9820cd934778cbd1ea47b33311e11de11dfd2ef46fdadc9abd5af1bc833`  
		Last Modified: Fri, 09 May 2025 19:03:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d83972677ee6a763d8be5f9fb82049570e5f3be83327f3243f007dac439372`  
		Last Modified: Fri, 09 May 2025 19:03:50 GMT  
		Size: 4.7 KB (4689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d51aeb085012bee0da8b629f142b241721ac99ac435645fc823e926a712772`  
		Last Modified: Fri, 09 May 2025 19:03:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651fc2d254ca599385aed4c7cba057f96d6c70ce55c6e0fbdc4ff53f06a629c8`  
		Last Modified: Fri, 09 May 2025 19:03:51 GMT  
		Size: 75.0 KB (74972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7524132e169fbe6c5b3743b6873d9e9a3ffc23a5c65d8a4dbeeaeeefad3fb5a8`  
		Last Modified: Fri, 09 May 2025 19:03:51 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a0146a0fa3d5d5ec824920fb83bfa88f9d73c3b9881ba480121938b9fa834`  
		Last Modified: Fri, 09 May 2025 19:03:52 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.1` - unknown; unknown

```console
$ docker pull kibana@sha256:798f655e57e8ac2ef517da53fae7d7a0da67b94c5c5a1e69656472965e5fc76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5478421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8272cc4a9cc7b93e94ea15ac0d30db435d32b14292c923e43c2e387f63ea977`

```dockerfile
```

-	Layers:
	-	`sha256:6fcdabff87ac8a44c04811f607ebdfb4620ff16f3377cb174086706fc9782552`  
		Last Modified: Fri, 09 May 2025 19:03:49 GMT  
		Size: 5.4 MB (5435237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57e82b5be30f061f0c69614856dbf91b1eb11789f0c0313a0947bdf051293a7`  
		Last Modified: Fri, 09 May 2025 19:03:49 GMT  
		Size: 43.2 KB (43184 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e686011e385a6d79ed6a275edba2722a855b11833e20980dac99d2afaaf7bf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.1 MB (441054640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34a74f2ca45258624a97ce10e269ad4d66452bf5a103d25a709120b826e52f0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL url="https://www.redhat.com"
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Apr 2025 15:48:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Apr 2025 15:48:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Apr 2025 15:48:53 GMT
ENV container oci
# Mon, 28 Apr 2025 15:48:53 GMT
COPY dir:37e2781211ed66b85e838f75f63c4036aeedc358075b7ac677bbe4ad43998692 in / 
# Mon, 28 Apr 2025 15:48:54 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 28 Apr 2025 15:48:54 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 15:48:54 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 28 Apr 2025 15:48:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Mon, 28 Apr 2025 15:48:54 GMT
LABEL "build-date"="2025-04-28T15:48:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Fri, 09 May 2025 04:49:38 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 09 May 2025 04:49:38 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN fc-cache -v # buildkit
# Fri, 09 May 2025 04:49:38 GMT
WORKDIR /usr/share/kibana
# Fri, 09 May 2025 04:49:38 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 09 May 2025 04:49:38 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 04:49:38 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 09 May 2025 04:49:38 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 09 May 2025 04:49:38 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 09 May 2025 04:49:38 GMT
LABEL org.label-schema.build-date=2025-04-30T12:17:16.628Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=0df588b1a307954a3103991180df23c70184d34c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.1 org.opencontainers.image.created=2025-04-30T12:17:16.628Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=0df588b1a307954a3103991180df23c70184d34c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.1
# Fri, 09 May 2025 04:49:38 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 09 May 2025 04:49:38 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 09 May 2025 04:49:38 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 09 May 2025 04:49:38 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 09 May 2025 04:49:38 GMT
USER 1000
```

-	Layers:
	-	`sha256:2aa6bd15812764b98217de512ddcd6b7fc8cb96437e1fa30d7963118dce559ff`  
		Last Modified: Mon, 28 Apr 2025 16:55:35 GMT  
		Size: 37.9 MB (37887470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00048a36b4e91220d2d1deb7933f1c359e192a228cf9fda898fa9d9dfd0e19df`  
		Last Modified: Fri, 09 May 2025 20:39:16 GMT  
		Size: 19.3 MB (19313396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274e8aca23ebe4f14ed317d79e88de6b8852c7e75a01c25477b4c23a7ca39ea8`  
		Last Modified: Fri, 09 May 2025 20:39:23 GMT  
		Size: 367.3 MB (367296674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fccdde99420de6d2e9b9b564e29a23bdce11c12bd84e7d72f272b3039ace8ef`  
		Last Modified: Fri, 09 May 2025 20:39:15 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72381a522ecf13dcbcd03a85ca73497610851373e861cca667b6361831c277a6`  
		Last Modified: Fri, 09 May 2025 20:39:17 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893380cd454a6731950ff25903733c6dad71516aba48538d8137698b898b708`  
		Last Modified: Fri, 09 May 2025 20:39:16 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc5596d64c4e1d503b9e645f2c5432625b1ea776e390b227d7878935332b219`  
		Last Modified: Fri, 09 May 2025 20:39:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725fed2a8c868fb45ec1899a671a6c92bbe3ea02ef921e15d3535356a6b65737`  
		Last Modified: Fri, 09 May 2025 20:39:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077b97902a1fa647c52e380f6361920e3d3c30983cc90b443e822170c0407ae`  
		Last Modified: Fri, 09 May 2025 20:39:19 GMT  
		Size: 4.7 KB (4691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46ec31bfb42f9a95eee51f77f67a9a40115abac4e02d74c6cca96d0cf1ebaef`  
		Last Modified: Fri, 09 May 2025 20:39:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50224ea375dcf6de7e15a8f1ff3d19e9c3782777007f78293ea83bc1b3259f33`  
		Last Modified: Fri, 09 May 2025 20:39:19 GMT  
		Size: 73.9 KB (73898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4ce0041e143b81e602d8216669b06ebe554df5b8528dffbaa0d7ff845fcdf6`  
		Last Modified: Fri, 09 May 2025 20:39:20 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c2c5e455401ee41e192f673a89c74ce8dd3f387a7301090289a1e35bd6dff`  
		Last Modified: Fri, 09 May 2025 20:39:20 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.1` - unknown; unknown

```console
$ docker pull kibana@sha256:499373a849911bb0de3f5da4b482fe0d69686a2a7c44c6739b73bb12bd36c9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5477357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503afa7aadcd0322f4c09679e8e87aebfad049d3d1648c6b2d3efd883a435e55`

```dockerfile
```

-	Layers:
	-	`sha256:5e0085a17924ff89203fa1512da68d1d9fa77e11b4a6cb4487e92d748f5bb660`  
		Last Modified: Fri, 09 May 2025 20:39:16 GMT  
		Size: 5.4 MB (5433915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c26a9cebbffa7490450245b1f166d33652ca8eb02007e9478126a80cfcfa47fb`  
		Last Modified: Fri, 09 May 2025 20:39:15 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
