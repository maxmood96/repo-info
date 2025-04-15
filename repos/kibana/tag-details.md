<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.16.6`](#kibana8166)
-	[`kibana:8.17.5`](#kibana8175)

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

## `kibana:8.16.6`

```console
$ docker pull kibana@sha256:1bb6482f0d43823375d875cc2476c692161119c61c28ce5bfa3479be600773e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.16.6` - linux; amd64

```console
$ docker pull kibana@sha256:2406ff5744bf6c325ea8fba43efccad60a04acf0a3723a5fe5ff3fd8a1e71e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.9 MB (394888396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e6460efc17db008e5a56c40c83d97219e7d5c7ae57fd8c1937bbe6ec3ac4d7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 25 Mar 2025 08:54:09 GMT
ARG RELEASE
# Tue, 25 Mar 2025 08:54:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Mar 2025 08:54:09 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN fc-cache -v # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/kibana
# Tue, 25 Mar 2025 08:54:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.build-date=2025-03-20T11:10:41.087Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=39969cb4b1ab957faf1e78d25d83ec04192ddc21 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.6 org.opencontainers.image.created=2025-03-20T11:10:41.087Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=39969cb4b1ab957faf1e78d25d83ec04192ddc21 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.6
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5fcb54725bcc66217a044cabc67d309ebc07f5b3761242820db1729aaf9042`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 10.7 MB (10725848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7b2843daed8653e710921c3a089135c76ea6f3e40689e5aa786f35cd36ff7`  
		Last Modified: Wed, 09 Apr 2025 01:21:24 GMT  
		Size: 340.0 MB (339979976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f95bbe0763949f2a3f2cc2727ffb5d76e58e1f83468bbc8de1485a2b7402bb`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf2fcb034d141c8e4162a1069df0f0bf7d78126eb8f372352fb0128edcbc9ef`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455ee5029c3a8be9f9db1ab09fc134eebdc08417c20b4bd142fc8b8e5f6cd880`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 5.3 KB (5275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0352cd7e09a3cdbc495fcf8a9ea1f97d25d45ca1716ff9085256a4dfc18ab4`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7fdfa04504f5dac47ff0bbd9aec62b5f1ca140c98112accc1003042c1d4750`  
		Last Modified: Wed, 09 Apr 2025 01:21:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ca14aa0bdd02b1bee1c16ee35274fcdcd449f59c69a7c845969f78213ed22a`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc2dda21747e0f24eb8899101c98ef5308da0b0c03d4261d948cc05eeafd3a`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4906035e91e1c2cd24349bba98a0aaca7b0c76b9ababf89c516f7ea68a722f4e`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 189.4 KB (189428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1073bd005f968a5e6a27a563107ce59275075ba0e6a3eb26f1e397c2a26980f`  
		Last Modified: Wed, 09 Apr 2025 01:21:21 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.6` - unknown; unknown

```console
$ docker pull kibana@sha256:f24062e4200766490937d9e643854d86c87c58c0c9bd8ad1c9da4c8be65983dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed16f695a6f55c53698cabb5d626f06211bbe68f1cad347a285ceb6af02b71c2`

```dockerfile
```

-	Layers:
	-	`sha256:2740d294c0c09b344cd1d51ff8d067479c0d0c3115fdadbf578f8d5efea9a249`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 4.3 MB (4302623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21417a4396fa27c6f1b46659e467a7b424814e8594d77dc64ad7b92f465e2ac8`  
		Last Modified: Wed, 09 Apr 2025 01:21:19 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.16.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9a6bb65b55d704a41a70b7329e2734c735ac01152d4cece9023f820450a7344a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 MB (405728624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3f43501ff36be26fa61225c0cdb1d5a514751178b2fe51c0c8b5cbe3004835`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 25 Mar 2025 08:54:09 GMT
ARG RELEASE
# Tue, 25 Mar 2025 08:54:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 Mar 2025 08:54:09 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN fc-cache -v # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/kibana
# Tue, 25 Mar 2025 08:54:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.build-date=2025-03-20T11:10:41.087Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=39969cb4b1ab957faf1e78d25d83ec04192ddc21 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.6 org.opencontainers.image.created=2025-03-20T11:10:41.087Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=39969cb4b1ab957faf1e78d25d83ec04192ddc21 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.6
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388ba6dab9a0f52eba8e0baeb884f4497b3483d4714b11c0afd7ca711ba9c98`  
		Last Modified: Wed, 09 Apr 2025 08:08:41 GMT  
		Size: 10.6 MB (10576615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aee4a613b4a132b4951aa768676ad118db8fbe88f0ceaca24c05657bc02b89`  
		Last Modified: Wed, 09 Apr 2025 08:08:48 GMT  
		Size: 352.5 MB (352508599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6265427c70cf031dc647a5598f95a49f188c33c1fb9a955fdb961572ee8e88`  
		Last Modified: Wed, 09 Apr 2025 08:08:41 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a2710d63599747870d64e19c41a286f53827561f64e2d33befb5af1cca0a75`  
		Last Modified: Wed, 09 Apr 2025 08:08:44 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a937cba541bcfc4f3180b6e37cfd0ffe5c7c6cfc59581613b0bd004f9b58572a`  
		Last Modified: Wed, 09 Apr 2025 08:08:41 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1179dc79ef04cd640b4af0ac71fa63b74ff648d4125f5c75586ab6518aeadb`  
		Last Modified: Wed, 09 Apr 2025 08:08:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0970fce494f94dbbbeb614340c9c11f28bf185f78ce465ca5887281ba952ea`  
		Last Modified: Wed, 09 Apr 2025 08:08:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54f35fd35bf03e1da52301315a1a294abee077b5655b932608922dcc2bfe671`  
		Last Modified: Wed, 09 Apr 2025 08:08:43 GMT  
		Size: 4.7 KB (4707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41153ecb946d77d2ca79b1db609a7b37f1add8f423d7ba4128faaa3e54cac937`  
		Last Modified: Wed, 09 Apr 2025 08:08:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4313c95474613208707587f20c063104e2dce909af874f1ac24579450be790`  
		Last Modified: Wed, 09 Apr 2025 08:08:44 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352377a9b067fbb8b018777dc3b0a9c689361930589d4d4e58a39d16172fc7a`  
		Last Modified: Wed, 09 Apr 2025 08:08:45 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.6` - unknown; unknown

```console
$ docker pull kibana@sha256:4d68cc57306da01e174e9f2d55b9307be7c306a569a553280934f2aa9a59c059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ac90f2122bcd054ec55d764efb40bc4d0bd5f26dd3448fc9d2df09817103ec`

```dockerfile
```

-	Layers:
	-	`sha256:b80ce781503a2022245b38700d1d6240fce58556e37a573ea70c2e674301c3ba`  
		Last Modified: Wed, 09 Apr 2025 08:08:41 GMT  
		Size: 4.3 MB (4302874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f6985ae1d1499dec9a4513500e7e22a8b456e3808ddcb8e83169d60c946aaa`  
		Last Modified: Wed, 09 Apr 2025 08:08:40 GMT  
		Size: 40.9 KB (40928 bytes)  
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
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eef2493b8b415f7620440191a02b3695e1499534060a1be954e3af05c87509`  
		Last Modified: Tue, 15 Apr 2025 17:58:48 GMT  
		Size: 10.7 MB (10725899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b739297d831af9896285d3962e4c8876d76f46970a5814397c375a758f9ab498`  
		Last Modified: Tue, 15 Apr 2025 17:58:53 GMT  
		Size: 341.6 MB (341583009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db87e529a7d3aa9dd6d76c3112cc74bd16d0c7997308c18a958827d92a61c2f`  
		Last Modified: Tue, 15 Apr 2025 17:58:47 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae0c7b9d360ba2efe812fa96d0ad5f258550964097eea120a23a8429b04c8c6`  
		Last Modified: Tue, 15 Apr 2025 17:58:48 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d509cc50c8c602da14518f9fb1bdc9734c3092d7c133e6ad8c585c9696a09f40`  
		Last Modified: Tue, 15 Apr 2025 17:58:48 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e0f9ecf53e081bfa45c9404d49865033a58b2d3323d5695360d3b1fc0c359b`  
		Last Modified: Tue, 15 Apr 2025 17:58:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ab6bacf1090763850de40b17b2c767818e800ae39a47b8351c9309d6937af0`  
		Last Modified: Tue, 15 Apr 2025 17:58:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da820c429190be5338e030c83ea99e5ab7b8a410c2e2ad5d34314b90fb3506d`  
		Last Modified: Tue, 15 Apr 2025 17:58:49 GMT  
		Size: 4.7 KB (4726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b44b6f9824b0f47e92a8f35e688087cf489857f8ee2640b1092637e1815ef4e`  
		Last Modified: Tue, 15 Apr 2025 17:58:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4942b1bdab29085d1f02c8814d3f54718aa2b19782d2d5992e4a0258232d1386`  
		Last Modified: Tue, 15 Apr 2025 17:58:50 GMT  
		Size: 189.4 KB (189428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3075cccd5c56004b5af4898b27151d0611a197588d947acd1b003b11f6eb53d9`  
		Last Modified: Tue, 15 Apr 2025 17:58:50 GMT  
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
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388ba6dab9a0f52eba8e0baeb884f4497b3483d4714b11c0afd7ca711ba9c98`  
		Last Modified: Wed, 09 Apr 2025 08:08:41 GMT  
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
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
