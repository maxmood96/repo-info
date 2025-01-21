<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.27`](#kibana71727)
-	[`kibana:8.16.3`](#kibana8163)
-	[`kibana:8.17.1`](#kibana8171)

## `kibana:7.17.27`

```console
$ docker pull kibana@sha256:5b87e147875855db6c4afe88dfe98dc61e93258126863f10ff631ef3b8f70679
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.27` - linux; amd64

```console
$ docker pull kibana@sha256:38d9290076da8b765b972a07531e8303f69707c999cc2f0361e1114dcc12d3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349816949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cf7ca66f376842c399f67e8f35273a0467b25cc54f1421332235c41899744e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 19:20:58 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 14 Jan 2025 19:20:58 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN fc-cache -v # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
WORKDIR /usr/share/kibana
# Tue, 14 Jan 2025 19:20:58 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Jan 2025 19:20:58 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:20:58 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
LABEL org.label-schema.build-date=2025-01-09T12:11:26.690Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=828e49db669c29d8cc4f3a30f6abe5e8f69a4290 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.27 org.opencontainers.image.created=2025-01-09T12:11:26.690Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=828e49db669c29d8cc4f3a30f6abe5e8f69a4290 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.27
# Tue, 14 Jan 2025 19:20:58 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 14 Jan 2025 19:20:58 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 14 Jan 2025 19:20:58 GMT
USER kibana
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc92c60a5cd6908acdfc6691406f0e91a3541efdb4ca933c7b61f9926c2ef`  
		Last Modified: Tue, 14 Jan 2025 20:29:03 GMT  
		Size: 10.7 MB (10725000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63651b590418d874d8574b9cdcdbe301183b9ecf18980be5f1c71fc5a549bfa0`  
		Last Modified: Tue, 14 Jan 2025 20:29:03 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593bbdf6888355d7487fefd9f04d8b4b54384d38b591aaa925354bf0514bd158`  
		Last Modified: Tue, 14 Jan 2025 20:29:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf06efdd0995b2138ddf83c86f57859174de236d8ef8a1df66b8a9f053348f59`  
		Last Modified: Tue, 14 Jan 2025 20:29:03 GMT  
		Size: 16.5 MB (16460474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99304c37a0a552efaa895e308ef06069778a8d84e1bf4def776fac7546fc1a4`  
		Last Modified: Tue, 14 Jan 2025 20:29:03 GMT  
		Size: 5.3 KB (5275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d7b8f6fd2bf346e3beef21e4baabca6e699d36b517b09e9e5819911c42b6b`  
		Last Modified: Tue, 14 Jan 2025 20:29:08 GMT  
		Size: 294.9 MB (294908725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3539429b045618df7d9a30d0db2750b6be2466a5d27387818d5779a52f46c0`  
		Last Modified: Tue, 14 Jan 2025 20:29:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17777628cce521346fd7cd5a83f02744ab926b68db1eee53e3c123e704de31c2`  
		Last Modified: Tue, 14 Jan 2025 20:29:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b319ffd1364f835bf3e05252f7fc457b02ccc8c4319574493392fe74d54e3f32`  
		Last Modified: Tue, 14 Jan 2025 20:29:04 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a80dec08c41e94b03475ca9da0aa4c33b661b4b19565d287801a137050134c`  
		Last Modified: Tue, 14 Jan 2025 20:29:04 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc3c558b130d86e2c8c15edb27b7717b56ce8d8963418515491879b6d80583`  
		Last Modified: Tue, 14 Jan 2025 20:29:05 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fc701eff08c3ae20cd0fe3878dc08cd01e3f540198384aea215fb5a5814ed5`  
		Last Modified: Tue, 14 Jan 2025 20:29:05 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.27` - unknown; unknown

```console
$ docker pull kibana@sha256:0fc8c79076522d894d6b0c06adc14c26232068fcf25a38c9a39c8546537e1629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3440510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61da529c7a61bdf289aeace4b125a9e49b50354aaf576b3e2cd807fb05146fae`

```dockerfile
```

-	Layers:
	-	`sha256:3e12a02aac8374f35a3dc8ea6c1f521a9f65b62ec51db5163bb6cf2760e488c8`  
		Last Modified: Tue, 14 Jan 2025 20:29:03 GMT  
		Size: 3.4 MB (3396001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a958729c4706579b8588f03ddb316ddcbaff0ccf018579139d25b7429fd467ae`  
		Last Modified: Tue, 14 Jan 2025 20:29:03 GMT  
		Size: 44.5 KB (44509 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.27` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e44509756580102975d9d53d4d4051c3c9ac1daaf0a746611de4283ce6111dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360271758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e228172aefed88e1321f4d1558621faf500481a981c7c3a78f3255352a6a61`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 14 Jan 2025 19:20:58 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 14 Jan 2025 19:20:58 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN fc-cache -v # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
WORKDIR /usr/share/kibana
# Tue, 14 Jan 2025 19:20:58 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Jan 2025 19:20:58 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:20:58 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
LABEL org.label-schema.build-date=2025-01-09T12:11:26.690Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=828e49db669c29d8cc4f3a30f6abe5e8f69a4290 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.27 org.opencontainers.image.created=2025-01-09T12:11:26.690Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=828e49db669c29d8cc4f3a30f6abe5e8f69a4290 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.27
# Tue, 14 Jan 2025 19:20:58 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 14 Jan 2025 19:20:58 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 14 Jan 2025 19:20:58 GMT
USER kibana
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7107accfc20efdd14655c3f01159b969799d2333530870b4f54d6875853ccc47`  
		Last Modified: Wed, 15 Jan 2025 01:33:01 GMT  
		Size: 10.6 MB (10575427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1b01cc57c96bb58fa25ee661288d41061b95c4808efc31705c3e5bc4adcaa3`  
		Last Modified: Wed, 15 Jan 2025 01:33:00 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c3a298a4e11f7dbc9d5421cf3ec03fcbbb97645cdc137598684a6b9f91af30`  
		Last Modified: Wed, 15 Jan 2025 01:33:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724a42df1ae99e497f1a63ae4e7197cfa10c6029e40da46f07728af0fdfa27ef`  
		Last Modified: Wed, 15 Jan 2025 01:33:01 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0be7e91a480e48563cddcc64e9b5c3bba1f52990e5931d595dc66b2fc716f8`  
		Last Modified: Wed, 15 Jan 2025 01:33:01 GMT  
		Size: 5.3 KB (5283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ef64910afb53d1a00a6e70f226376e773491f968d81387c9fe2c315cbefde3`  
		Last Modified: Wed, 15 Jan 2025 01:33:09 GMT  
		Size: 307.1 MB (307056758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7027d2a513b339676fd56a5ad8407089f6d32f047f5bc0d371955e9be2c7aea`  
		Last Modified: Wed, 15 Jan 2025 01:33:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e161e33812f045f7d887f6929e6911c59e9ebe06ca5aebbf934386e4bbc65`  
		Last Modified: Wed, 15 Jan 2025 01:33:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2ac7ef93b5be7db5787a14dae5f32f15a62b263892ebeafe8fa839468f97dd`  
		Last Modified: Wed, 15 Jan 2025 01:33:02 GMT  
		Size: 4.5 KB (4502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02af3836b55f99f4621486dd34353cc53637341512d85224714e4be12bca1ed9`  
		Last Modified: Wed, 15 Jan 2025 01:33:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abbef48da5c02a841d48f43031726d0204029325ba5f1bb9c117befe6bc0d19`  
		Last Modified: Wed, 15 Jan 2025 01:33:03 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a8addb7d83797a707c7a56f9224285b8ee4463bf258efb789ba0d138237159`  
		Last Modified: Wed, 15 Jan 2025 01:33:03 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.27` - unknown; unknown

```console
$ docker pull kibana@sha256:d3d7ca33119afe5ff5c996104e36de76c4e8d31131efffc463d50f12d67bf9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3441038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd4a653cca909c6dd9103fc25cdb512bdcf3cbe85c81c7ff4d632fbc2bdc8ed`

```dockerfile
```

-	Layers:
	-	`sha256:b5da0059a354f1b1f5835c2feaa5e50f33685cd3743cdc6eaba4d7db5f8eb554`  
		Last Modified: Wed, 15 Jan 2025 01:33:00 GMT  
		Size: 3.4 MB (3396252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec9475b3e84652ca660288a37ea349723498aa313b603aaf50a24b33bc28f9a`  
		Last Modified: Wed, 15 Jan 2025 01:33:00 GMT  
		Size: 44.8 KB (44786 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.16.3`

```console
$ docker pull kibana@sha256:8c5f0c1989fa865f1dbe6fd18f1646dc93abcd857cbe8f7ae2277c0f3fd9813a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.16.3` - linux; amd64

```console
$ docker pull kibana@sha256:69ee4c92d4a7e12a4a71f9d0fd18b245ae9465a0f81ecaaa4a7a897b9f3cb8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.2 MB (399204628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a668de317979c5b5c05053138d8fb2750784e200f47dd063908d643eb3f38529`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 08:29:25 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 21 Jan 2025 08:29:25 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN fc-cache -v # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
WORKDIR /usr/share/kibana
# Tue, 21 Jan 2025 08:29:25 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:29:25 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
LABEL org.label-schema.build-date=2025-01-09T12:09:19.137Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=dcb19b0aa33b03224c55afabee0c5fdd03a6c572 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.3 org.opencontainers.image.created=2025-01-09T12:09:19.137Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=dcb19b0aa33b03224c55afabee0c5fdd03a6c572 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.3
# Tue, 21 Jan 2025 08:29:25 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 21 Jan 2025 08:29:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 21 Jan 2025 08:29:25 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197ddd52a79a65926f05c4a93c74cc4e8ca2241afa94ca7b838c509a4db58fd`  
		Last Modified: Tue, 21 Jan 2025 19:31:20 GMT  
		Size: 10.7 MB (10725060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a92fdf2b9dfb9f84f16bd89023db831c2dd12affb4b47791eed263d8b3b7716`  
		Last Modified: Tue, 21 Jan 2025 19:31:25 GMT  
		Size: 344.3 MB (344296299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612bd3b6a295f50151985f5ea40aaa75e3305091cc3b15b3d44a5c48dcac9a7a`  
		Last Modified: Tue, 21 Jan 2025 19:31:20 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd574d34078bcb33a4f07fda85e676c8df5c9b6213f265e34c17ce92fbccbeff`  
		Last Modified: Tue, 21 Jan 2025 19:31:21 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc086b5692b52c82d3d27046bf5784cf3093b0c1b8a269ec396990fe9dac94`  
		Last Modified: Tue, 21 Jan 2025 19:31:21 GMT  
		Size: 5.3 KB (5286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ebaf136f885ad2166fa39c3ad4764d1e37f6d37c3e6f0b9eb7cc2eb0538986`  
		Last Modified: Tue, 21 Jan 2025 19:31:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8eb272bffda53397d042de0c239de305f8e1dede97e3efc93d4b4baec5a484`  
		Last Modified: Tue, 21 Jan 2025 19:31:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8668de79fb8fde22a6aade0ddad96a3d816013d65edffef678fc4e00d195e171`  
		Last Modified: Tue, 21 Jan 2025 19:31:21 GMT  
		Size: 4.7 KB (4708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557ea725bb138dfd7218ccc633edf87fd7a9a167194baec0220b390581793617`  
		Last Modified: Tue, 21 Jan 2025 19:31:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf86354c8bfa8a0934d41015b81554eab6fddece11dd172055d0d44c0caa6fae`  
		Last Modified: Tue, 21 Jan 2025 19:31:22 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22146528185f69e5418f88202a3bb6206395695a23fb2bbf71fa9b260cfd19fe`  
		Last Modified: Tue, 21 Jan 2025 19:31:22 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.3` - unknown; unknown

```console
$ docker pull kibana@sha256:4b2182070b5d76a286ae2d22e568ef21a121492c8db696fb4db25f48a4fa9cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4348088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807d8867d5ac7732885d2515ed8de9aa6428d4871853860e7a8d65042aedc15c`

```dockerfile
```

-	Layers:
	-	`sha256:0028fd11060bfe8172bcfc0cb8235ac0792899094ad81cad4f0afff6631530b0`  
		Last Modified: Tue, 21 Jan 2025 19:31:20 GMT  
		Size: 4.3 MB (4307408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b0416743883b438dd1ef6aaca60aca1ffdf9d0c51a091a61354fc22b4e96fc0`  
		Last Modified: Tue, 21 Jan 2025 19:31:20 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.16.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:5f9abd1bb7197305573223e94c6c158952f58ea60c7c765fc8fdd1b75ec2119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.7 MB (409668938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9073f5b9ce33cd64fdfe72c5c716035a149ed4cfed34e1d0b94c72c55fbc30b0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 08:29:25 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 21 Jan 2025 08:29:25 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN fc-cache -v # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
WORKDIR /usr/share/kibana
# Tue, 21 Jan 2025 08:29:25 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:29:25 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
LABEL org.label-schema.build-date=2025-01-09T12:09:19.137Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=dcb19b0aa33b03224c55afabee0c5fdd03a6c572 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.3 org.opencontainers.image.created=2025-01-09T12:09:19.137Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=dcb19b0aa33b03224c55afabee0c5fdd03a6c572 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.3
# Tue, 21 Jan 2025 08:29:25 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 21 Jan 2025 08:29:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 21 Jan 2025 08:29:25 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a6ea02fafc8518817cd3aadc2b37ab06af1484c8f148526062328e38c5075`  
		Last Modified: Tue, 21 Jan 2025 20:12:21 GMT  
		Size: 10.6 MB (10575391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e2ae9a7b92047a2364c1fec8144ca3b08d584062bc7c6c611421c237704652`  
		Last Modified: Tue, 21 Jan 2025 20:12:28 GMT  
		Size: 356.5 MB (356453983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2339a86cbab4f195fef3c85e83b14dd68a708cb50382161eb4c2ad996842dfae`  
		Last Modified: Tue, 21 Jan 2025 20:12:20 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8c530d3c0224a5b08371913d2e6b32f6ffd9ed86994a4a328a98172301e34e`  
		Last Modified: Tue, 21 Jan 2025 20:12:21 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fd3dcb6cbf3f1757258a8dc63b0a08f86fd086bb4213da1e16b44482ae25f2`  
		Last Modified: Tue, 21 Jan 2025 20:12:21 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de03e0ab4d39e8ea369d2b0079b55f83e1b05961392dc3890d12677d95d0581`  
		Last Modified: Tue, 21 Jan 2025 20:12:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153db322bca54daefe146aa625cac534ec1815ae67ba54bef9cd28f1c317887`  
		Last Modified: Tue, 21 Jan 2025 20:12:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d954991f021a2b664c7ae9cb06935010d68a98f39d1cf0c462912d2d54d86af`  
		Last Modified: Tue, 21 Jan 2025 20:12:22 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48a7e8ad6fd1ec31c3ab8039b3380896112fc381f9338a11f39b9b3df513265`  
		Last Modified: Tue, 21 Jan 2025 20:12:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f012333678dbcc6be6209f327329604c1bd68fc41c58b09d95aa4bef32fbdf`  
		Last Modified: Tue, 21 Jan 2025 20:12:23 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a237a5fdd46571e9ff0c135feb372cb9de61c21a409e60b3a48e6115b1d0661`  
		Last Modified: Tue, 21 Jan 2025 20:12:23 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.3` - unknown; unknown

```console
$ docker pull kibana@sha256:fd3e719889e496ba417eed08a7414b3c74f43172defcfbc98943fbba15d27ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4348587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41f5c170fa6077e746aebebf0aca62378c8b15550e05c7c3779591d2f73ba8b`

```dockerfile
```

-	Layers:
	-	`sha256:66cdd1f354b796ce146affee13c08e0166ec431cbc9298e35c51bcee541309a1`  
		Last Modified: Tue, 21 Jan 2025 20:12:20 GMT  
		Size: 4.3 MB (4307659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e10f86039e4b65aed9a4dabd42a8a54a9339882dffc15a5e8f95653a8105b049`  
		Last Modified: Tue, 21 Jan 2025 20:12:20 GMT  
		Size: 40.9 KB (40928 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.1`

```console
$ docker pull kibana@sha256:269013daeb1e69e6fc8095737cbe23b9688366d6a0505b43f8642fddedbebe48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.1` - linux; amd64

```console
$ docker pull kibana@sha256:df293be13df00cba8cff13a069c21acc06a260ba76c65ab765944b5a6f6a3167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.0 MB (400018849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526e8c1e70c408b0ae2f1a0a39930a3383ef78931cba31e721e1ef21ede60ac7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 08:22:13 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 21 Jan 2025 08:22:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN fc-cache -v # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
WORKDIR /usr/share/kibana
# Tue, 21 Jan 2025 08:22:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:22:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
LABEL org.label-schema.build-date=2025-01-09T12:09:18.841Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9b07116468368c418abf167729c8417c181f8700 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.1 org.opencontainers.image.created=2025-01-09T12:09:18.841Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9b07116468368c418abf167729c8417c181f8700 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.1
# Tue, 21 Jan 2025 08:22:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 21 Jan 2025 08:22:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 21 Jan 2025 08:22:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92227ab80ff3ce9bc2b0c642257e35b96e896ab0f3cef9366c90075d743f1d2`  
		Last Modified: Tue, 21 Jan 2025 19:31:50 GMT  
		Size: 10.7 MB (10725048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2759ea1a5c0d1680b6154a88e2b2795d59ea826b17a54dcfb3284abe02ac1`  
		Last Modified: Tue, 21 Jan 2025 19:31:55 GMT  
		Size: 345.1 MB (345110517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f956a68196fd0d2c75c86929a64f9435214927d56782024c459b78dd9f6f955f`  
		Last Modified: Tue, 21 Jan 2025 19:31:49 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67cbb7c348abecba4646d89049e28db8d740d041ef6e51041150dd2f572fb79`  
		Last Modified: Tue, 21 Jan 2025 19:31:50 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54abace8814425b785477324b72895377d314b5531bbb45032a30d36d542a4d0`  
		Last Modified: Tue, 21 Jan 2025 19:31:50 GMT  
		Size: 5.3 KB (5290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c636bc2950538679b5ad93f14f97e11940bacb3b6400b829b284fb61bb5453`  
		Last Modified: Tue, 21 Jan 2025 19:31:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6f5501d6da11fd39efaff8efb784c1c9c04c7c1e59e9ebaec04600ff52907c`  
		Last Modified: Tue, 21 Jan 2025 19:31:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29073c8d83c3da16d4aebb63cb535c1ad32e4583696563d9ae0917f928dd4ec3`  
		Last Modified: Tue, 21 Jan 2025 19:31:51 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64f26f734e2efabd84ec3dd41e5071989f25b3087ba588391c17407a37e569e`  
		Last Modified: Tue, 21 Jan 2025 19:31:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0506729e23197480b2fa321259038b0ac080870aa99f8e8efa1a43a63b41a2e`  
		Last Modified: Tue, 21 Jan 2025 19:31:51 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852126d23ca4823ba7a69c24ff58dad824a08c17655051c44fa673e120ba84ed`  
		Last Modified: Tue, 21 Jan 2025 19:31:52 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.1` - unknown; unknown

```console
$ docker pull kibana@sha256:24babb011e2274ec9f212ddcea69254fa4aa42a40506c4bc43e69622835a601d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4443530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425ab3f7f5fd7e22815545e34ec3194e83592b77abb090f5f1466f561556b086`

```dockerfile
```

-	Layers:
	-	`sha256:d07d5c0628c7f294df781df6dc7a16ba3d635f4410e8987338906ed5d77bea67`  
		Last Modified: Tue, 21 Jan 2025 19:31:49 GMT  
		Size: 4.4 MB (4402850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c623582dbd47fd67ce9e2e500c11127fb9dd213d1d11c1661096962a648f2836`  
		Last Modified: Tue, 21 Jan 2025 19:31:49 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:c7313f8c1f3636fe45adec3b185632249532db7e8894ff9cc0f9be9b94a4505f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.5 MB (410481231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75b5ccf243b64790234ba85c76c01adf0506350979e7f873803ef901622667f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 08:22:13 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 21 Jan 2025 08:22:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN fc-cache -v # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
WORKDIR /usr/share/kibana
# Tue, 21 Jan 2025 08:22:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:22:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
LABEL org.label-schema.build-date=2025-01-09T12:09:18.841Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9b07116468368c418abf167729c8417c181f8700 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.1 org.opencontainers.image.created=2025-01-09T12:09:18.841Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9b07116468368c418abf167729c8417c181f8700 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.1
# Tue, 21 Jan 2025 08:22:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 21 Jan 2025 08:22:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 21 Jan 2025 08:22:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a6ea02fafc8518817cd3aadc2b37ab06af1484c8f148526062328e38c5075`  
		Last Modified: Tue, 21 Jan 2025 20:12:21 GMT  
		Size: 10.6 MB (10575391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977a984db817996c34b16c5835593be229fc1d478f611df2ecc2f138052a9181`  
		Last Modified: Tue, 21 Jan 2025 20:18:54 GMT  
		Size: 357.3 MB (357266256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5a25482aae04b194961326a66c94bef85502f1bc081e9be2287f37647ca618`  
		Last Modified: Tue, 21 Jan 2025 20:18:47 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f718b9f17819b8fac993db0cfbecd715de18af69dda3075dfedb4db07cf6e32`  
		Last Modified: Tue, 21 Jan 2025 20:18:48 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830fd58201b97816d300d0de45bb4b2cbd5f00ee5eeab4800ec5b4c2e773eb34`  
		Last Modified: Tue, 21 Jan 2025 20:18:47 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29759df641af18c077e4b5050a9a213a01ef5fddaa9e2d24c4f050bacf512d19`  
		Last Modified: Tue, 21 Jan 2025 20:18:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d6e33631c536705f6ef526be23a91f901269f4c07e27308daa6708eb6f70f7`  
		Last Modified: Tue, 21 Jan 2025 20:18:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500b086501e8d471e470da77ccdecbd42416def8a90f5ed434a8fcd797c850a9`  
		Last Modified: Tue, 21 Jan 2025 20:18:49 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22044d0515103f376eef78a51e77380386404a8b72c5c513a001a904eaa659a`  
		Last Modified: Tue, 21 Jan 2025 20:18:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cabb9b475a984e446bac1a7619818b2c9654ec245f2ca815cc5806ab788c36`  
		Last Modified: Tue, 21 Jan 2025 20:18:49 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c3778e8ece0dbc57dd31bccc0312c695e7ac99a14135003099439d43b7c17`  
		Last Modified: Tue, 21 Jan 2025 20:18:50 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.1` - unknown; unknown

```console
$ docker pull kibana@sha256:bf2f93daee7da849a3a7f2c888f250b396b4d5053942d76edada2b43c519fc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4444028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49545f071dab173dc46c10f8ec37d160e0cad79b881ebff854f19d4443c5629`

```dockerfile
```

-	Layers:
	-	`sha256:803b831270b903fa39b6ba7c85df0bf59fc7458ba045052263d1721be403b11f`  
		Last Modified: Tue, 21 Jan 2025 20:18:47 GMT  
		Size: 4.4 MB (4403101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec52da7de245e82f1ece5b2842aef78638342d436daa80efe5efede3080cd2ad`  
		Last Modified: Tue, 21 Jan 2025 20:18:47 GMT  
		Size: 40.9 KB (40927 bytes)  
		MIME: application/vnd.in-toto+json
