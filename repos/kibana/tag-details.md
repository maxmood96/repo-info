<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.27`](#kibana71727)
-	[`kibana:8.16.2`](#kibana8162)
-	[`kibana:8.17.0`](#kibana8170)

## `kibana:7.17.27`

```console
$ docker pull kibana@sha256:c5e9f523a8333e608889d69661b2cca68b9e299496039584fd455a636992c79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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
		Last Modified: Wed, 15 Jan 2025 02:27:40 GMT  
		Size: 10.7 MB (10725000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63651b590418d874d8574b9cdcdbe301183b9ecf18980be5f1c71fc5a549bfa0`  
		Last Modified: Wed, 15 Jan 2025 00:15:14 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593bbdf6888355d7487fefd9f04d8b4b54384d38b591aaa925354bf0514bd158`  
		Last Modified: Wed, 15 Jan 2025 00:15:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf06efdd0995b2138ddf83c86f57859174de236d8ef8a1df66b8a9f053348f59`  
		Last Modified: Tue, 14 Jan 2025 20:29:03 GMT  
		Size: 16.5 MB (16460474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3539429b045618df7d9a30d0db2750b6be2466a5d27387818d5779a52f46c0`  
		Last Modified: Wed, 15 Jan 2025 00:15:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17777628cce521346fd7cd5a83f02744ab926b68db1eee53e3c123e704de31c2`  
		Last Modified: Wed, 15 Jan 2025 00:40:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b319ffd1364f835bf3e05252f7fc457b02ccc8c4319574493392fe74d54e3f32`  
		Last Modified: Tue, 14 Jan 2025 20:29:04 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a80dec08c41e94b03475ca9da0aa4c33b661b4b19565d287801a137050134c`  
		Last Modified: Wed, 15 Jan 2025 00:15:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc3c558b130d86e2c8c15edb27b7717b56ce8d8963418515491879b6d80583`  
		Last Modified: Wed, 15 Jan 2025 00:15:45 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fc701eff08c3ae20cd0fe3878dc08cd01e3f540198384aea215fb5a5814ed5`  
		Last Modified: Wed, 15 Jan 2025 00:15:47 GMT  
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

## `kibana:8.16.2`

```console
$ docker pull kibana@sha256:40c106833c924d62b7df362eb20e8612c285bdf510edae272c6d92c6b137ac7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.16.2` - linux; amd64

```console
$ docker pull kibana@sha256:a45c2e53e54a0a3858100f181dc7996822be7495613a3e863a314418708099dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.5 MB (399473069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445e87ed0ba5bc56e94dbe5877eaa1cb09c611ec72687b9e615d9b2364a4d06b`
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
# Tue, 17 Dec 2024 15:31:13 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 17 Dec 2024 15:31:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN fc-cache -v # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
WORKDIR /usr/share/kibana
# Tue, 17 Dec 2024 15:31:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Dec 2024 15:31:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
LABEL org.label-schema.build-date=2024-12-12T03:12:34.105Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c5bc2be5a28eadff737e48dfbf73c4ae17d3426e org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.2 org.opencontainers.image.created=2024-12-12T03:12:34.105Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c5bc2be5a28eadff737e48dfbf73c4ae17d3426e org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.2
# Tue, 17 Dec 2024 15:31:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 17 Dec 2024 15:31:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 17 Dec 2024 15:31:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d49834d1c9a257cdb80611139bbed71853a5e3314533368e3f889311e783200`  
		Last Modified: Tue, 17 Dec 2024 19:31:53 GMT  
		Size: 11.0 MB (10967635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90f379800010a2da13b7a1d0a4290d9a0bef43445e5c5493a7674422a4fc4e1`  
		Last Modified: Tue, 17 Dec 2024 19:31:58 GMT  
		Size: 344.3 MB (344322177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a823b7626c8442ca5845459c1fa716af8adc9f54cb9db0fb44699a96df153a16`  
		Last Modified: Tue, 17 Dec 2024 21:15:45 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276b40792a14d3eb794b4bf4d0145568493ead027b2117569b2599cef1f78499`  
		Last Modified: Tue, 17 Dec 2024 19:31:53 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cd0fab4864f4b1f511b1fa08f7d48ceedee1b445cea20097d9dc6d08de1d6c`  
		Last Modified: Wed, 18 Dec 2024 03:07:17 GMT  
		Size: 5.3 KB (5284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58340c8eb9226626c02be1e94328a7b769c017ec17a87c2055ab24220edf8968`  
		Last Modified: Wed, 18 Dec 2024 08:22:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f64304f1c41620a63e80b7c8e0f2665e9e90ef746b65c96a19cc5bfca4e575e`  
		Last Modified: Tue, 17 Dec 2024 19:31:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40128cc4a0906f2c7f78c8e419560dae2edc7be468b6ca857c8e7f2e277027a7`  
		Last Modified: Tue, 17 Dec 2024 19:31:54 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f0bb9c03f1b04e51a2c0fff0380677c4a2f8aa19ee929ba47e57e308d0770d`  
		Last Modified: Tue, 17 Dec 2024 19:31:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98be939e0cfba610fe3d9357ba46695f4f259bd1a91d791c5c4d03c56c1cda8`  
		Last Modified: Wed, 18 Dec 2024 01:41:58 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9b159006151514fc03a9e7717b6395fdfcfd00ad2c4e6ed53605156040fd75`  
		Last Modified: Wed, 18 Dec 2024 08:22:46 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.2` - unknown; unknown

```console
$ docker pull kibana@sha256:13a204d6ef9a6f50bb01332432cd10a877105c77d71e1fde91b982a7146af22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4354856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e808d0181bc0f6b5a62a419cf73bc589172a0a2e5651d1a2f993619d5b2052`

```dockerfile
```

-	Layers:
	-	`sha256:a47e48fb80c33aa70bb052aafee1b0bf5c85b13b5344bce94214f6e97cdc9c6e`  
		Last Modified: Mon, 06 Jan 2025 17:48:06 GMT  
		Size: 4.3 MB (4314212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b170d4e47e4c2aba9097cd5e5d11ffed0a68417c9cfe16b504b176eba123250e`  
		Last Modified: Wed, 18 Dec 2024 21:03:50 GMT  
		Size: 40.6 KB (40644 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.16.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:16b5ef7e6922a98f9fa6d369d4cc9b2e2f7d8db6d6523136ff779b21738ac0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.9 MB (409947916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc634d2dbf7491142002ec760bd98c55c1f73fdaf59a674ddba4ea4197d5858d`
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
# Tue, 17 Dec 2024 15:31:13 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 17 Dec 2024 15:31:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN fc-cache -v # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
WORKDIR /usr/share/kibana
# Tue, 17 Dec 2024 15:31:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Dec 2024 15:31:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
LABEL org.label-schema.build-date=2024-12-12T03:12:34.105Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c5bc2be5a28eadff737e48dfbf73c4ae17d3426e org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.2 org.opencontainers.image.created=2024-12-12T03:12:34.105Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c5bc2be5a28eadff737e48dfbf73c4ae17d3426e org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.2
# Tue, 17 Dec 2024 15:31:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 17 Dec 2024 15:31:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 17 Dec 2024 15:31:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f7d301b481d7c894635eaf4e60ef6d0efc4b40557c8aa2dc4a14bee9530c6`  
		Last Modified: Tue, 17 Dec 2024 19:40:51 GMT  
		Size: 10.8 MB (10818795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2fef794c8da6f321580f85894f3a9ce00dba234be66aebe17f09e0e5f98b68`  
		Last Modified: Tue, 17 Dec 2024 19:40:58 GMT  
		Size: 356.5 MB (356489536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f98a63ebf617fbd06bad76d06e8582a9bf76ac9d875cf5bb92c716cf96f43f`  
		Last Modified: Tue, 17 Dec 2024 23:39:35 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce4868a1a1f002cc117e9163acb24f9c594a99cd85470ed3daabc53c911af9f`  
		Last Modified: Tue, 17 Dec 2024 19:40:51 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af060f043cc6071bf29281cea4f29e63f2cb75f7b45d131b80afd27cc87984e`  
		Last Modified: Tue, 17 Dec 2024 19:40:51 GMT  
		Size: 5.3 KB (5285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fb63742ac80afd9d13ac3327f57c495c4b96aff790262d2a5f1fd89ad2c63`  
		Last Modified: Tue, 17 Dec 2024 19:40:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc1149372c86e7dd1ec8669d00970f8ad93771efba0ea8399d54aa4df38d731`  
		Last Modified: Wed, 18 Dec 2024 03:38:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443931acc4f142759d34b9c13c98fb25ccf09b11e6b7e1483deaedb9712dc0cf`  
		Last Modified: Tue, 17 Dec 2024 19:40:52 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca2d7b60b051b007fa867aad27c78744beca000da3ee3a9a7ab691c38ded79a`  
		Last Modified: Tue, 17 Dec 2024 19:40:53 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561a569034fe4b0a5c8709767f67b89c632f9feaf59f05188417efc39e3fc3d3`  
		Last Modified: Wed, 18 Dec 2024 08:24:50 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ae66c138dfdcccc3b0b39c0629ddff270bdc335e47c6944d9e0f42547277a3`  
		Last Modified: Wed, 18 Dec 2024 19:20:35 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.2` - unknown; unknown

```console
$ docker pull kibana@sha256:22a9414e69c416676feddfa8d8ede0b05686e3d7770ab841b51fb0ed6e7f8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfdc5b656dc9437575ffe0e63ec2238c5f516bbf2f7de58cf1dca2fad8edc17`

```dockerfile
```

-	Layers:
	-	`sha256:51e4191890fc68c73ea2a7904f877a1c07d71a2a87ce9df37f4e14ad7b36b0c7`  
		Last Modified: Tue, 17 Dec 2024 19:40:51 GMT  
		Size: 4.3 MB (4314463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91baf27f30c805c0eaa893377740be084a0b71e51543270ee40285cd28e39692`  
		Last Modified: Tue, 17 Dec 2024 19:40:50 GMT  
		Size: 40.9 KB (40892 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.0`

```console
$ docker pull kibana@sha256:a41c1a96bb2511f23cfc54ff9830169c19cc42facd29cf9db2c8e640b8da0dbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.0` - linux; amd64

```console
$ docker pull kibana@sha256:5fbdbd0652e4c464536b5635005c9d29b646a5da961019d5f05b1955c60c46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 MB (398700822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad644db4f4acf2e553a1bdedafd8c1a2cb7c1a6c73cd825ec256a2f070fcc599`
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
# Mon, 16 Dec 2024 18:48:50 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 16 Dec 2024 18:48:50 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN fc-cache -v # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
WORKDIR /usr/share/kibana
# Mon, 16 Dec 2024 18:48:50 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 16 Dec 2024 18:48:50 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
LABEL org.label-schema.build-date=2024-12-11T11:12:31.173Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=86cbc85e621f4f3f701ed230f4e859ac5a80145b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.0 org.opencontainers.image.created=2024-12-11T11:12:31.173Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=86cbc85e621f4f3f701ed230f4e859ac5a80145b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.0
# Mon, 16 Dec 2024 18:48:50 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 16 Dec 2024 18:48:50 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 16 Dec 2024 18:48:50 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f5536f9c3a295578719ead17ee1141860a84e6d379a010b9dd4d6b1b6e8866`  
		Last Modified: Tue, 17 Dec 2024 19:31:56 GMT  
		Size: 11.0 MB (10967644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda9ab0b57da54e065c8bbaa39c2c786a9715937a4fa26785ece7dc5bb3d24d`  
		Last Modified: Tue, 17 Dec 2024 22:11:10 GMT  
		Size: 343.5 MB (343549921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce087b1d53dd00c15b43cee10b2ae9461190e7507decaeb8ff83b1ad0243f2f`  
		Last Modified: Wed, 18 Dec 2024 00:29:55 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059086aea0e54491240b45aab83ed7d54107e0c91ad9b7e2a27993f767023f88`  
		Last Modified: Tue, 17 Dec 2024 21:49:25 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ad0e5e97058e5e0f676867b3b02b4eed67b09904af9b661de8d11ea65dc105`  
		Last Modified: Tue, 17 Dec 2024 19:31:56 GMT  
		Size: 5.3 KB (5276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324cbb3dbd808e04d80f902efeb5327a9fde458562eba9024839aa80ff503527`  
		Last Modified: Wed, 18 Dec 2024 00:29:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748267f8f9a5fc7466f687d37421b7f3a8853312aa57833b077bc5bda1b14150`  
		Last Modified: Tue, 17 Dec 2024 19:31:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dea0f9db3c94e8abe7536e4602b5adace549d5a02c0d44b97c3f7617b843b9d`  
		Last Modified: Tue, 17 Dec 2024 19:31:57 GMT  
		Size: 4.7 KB (4719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5530ca11b47c3cce8c62867703ae8ba74548992b47b9f0abf1b45492254ee9bc`  
		Last Modified: Tue, 17 Dec 2024 21:16:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90490d9d682cae7136bb9f08491d6e7d7d0305c1bad5e611f8961d9696aa2788`  
		Last Modified: Tue, 17 Dec 2024 19:31:58 GMT  
		Size: 189.4 KB (189431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f11a3f62908791cd37345196107e3913dc305e25c513a7dc0c9b3f1c1c5f07`  
		Last Modified: Tue, 17 Dec 2024 19:31:58 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.0` - unknown; unknown

```console
$ docker pull kibana@sha256:7f0c25a435a5b235355fe511411ae5ca7f308c2ffdbe4cb81e3649cae069f9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4457792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ac44e4f3b4b388bd2e83d49bea60c33cf52e72c97f628757e01d1db2f2e4d0`

```dockerfile
```

-	Layers:
	-	`sha256:1294a08df7501e4babfe4f0bac793165ad49016f21a0beb17105ed9e0cabb91b`  
		Last Modified: Mon, 23 Dec 2024 06:39:50 GMT  
		Size: 4.4 MB (4417148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2e5dbf511478ea563e2dbc7c9652e61378a76b8f80729664b21ce0251a4f51b`  
		Last Modified: Tue, 17 Dec 2024 19:31:56 GMT  
		Size: 40.6 KB (40644 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:a06b126a31813e819e2d0791b46bd0410a212bf805f7f70852f18fd01a74ffd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.2 MB (409182949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff3f87391be81f8e0986f3cc8feb79a65bcd81ee5a9fc459820b7d3f78fa604`
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
# Mon, 16 Dec 2024 18:48:50 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 16 Dec 2024 18:48:50 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN fc-cache -v # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
WORKDIR /usr/share/kibana
# Mon, 16 Dec 2024 18:48:50 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 16 Dec 2024 18:48:50 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
LABEL org.label-schema.build-date=2024-12-11T11:12:31.173Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=86cbc85e621f4f3f701ed230f4e859ac5a80145b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.0 org.opencontainers.image.created=2024-12-11T11:12:31.173Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=86cbc85e621f4f3f701ed230f4e859ac5a80145b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.0
# Mon, 16 Dec 2024 18:48:50 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 16 Dec 2024 18:48:50 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 16 Dec 2024 18:48:50 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f7d301b481d7c894635eaf4e60ef6d0efc4b40557c8aa2dc4a14bee9530c6`  
		Last Modified: Tue, 17 Dec 2024 19:40:51 GMT  
		Size: 10.8 MB (10818795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ff73b91a4b71898b18acd3a192bacf72697b921fc43ca23b86e0c5dc4dc22a`  
		Last Modified: Wed, 18 Dec 2024 06:35:59 GMT  
		Size: 355.7 MB (355724574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307fb35d7d5ec3051d139ac084e84369ad6ca7c619de15c48aecb82bd9b83be2`  
		Last Modified: Tue, 17 Dec 2024 19:47:15 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad960f820a8221ecbd4275b11b2452764de1943e92dea27120fb5eed9ecde5fd`  
		Last Modified: Tue, 17 Dec 2024 19:47:16 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a63ec993967914208345fc6503d80e65995c506a8c1d30d0991231574765db`  
		Last Modified: Tue, 17 Dec 2024 19:47:15 GMT  
		Size: 5.3 KB (5274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9a3c7ac6550e931f0e78053ac9ff2348de3420ebe3da2be2fa25528b50bde9`  
		Last Modified: Tue, 17 Dec 2024 19:47:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62f8d1a89a8436b3fbebb8ed1e34ba184669f541eab2a6386c74026c8980cac`  
		Last Modified: Tue, 17 Dec 2024 19:47:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a8f6c85de230e65924ebd09db8f38256ae2a2e72e35d480be18b67bfee2b60`  
		Last Modified: Wed, 18 Dec 2024 01:15:00 GMT  
		Size: 4.7 KB (4716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f239d4bf5eef662f79d4da136190c410736f36ec841195886e40d2d224fd8fd6`  
		Last Modified: Tue, 17 Dec 2024 21:16:15 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5781ae08a3e2ecd03caa509dc18c26fbab10689fdfeae8a7df6bc733cd3ab61`  
		Last Modified: Tue, 17 Dec 2024 19:47:17 GMT  
		Size: 183.4 KB (183418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d7a4c1ce97f37619c3717a348a99a4df95c6315470f14c0b6766a3f427562f`  
		Last Modified: Wed, 18 Dec 2024 11:51:34 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.0` - unknown; unknown

```console
$ docker pull kibana@sha256:3a063d76d0a7964e89fe1e4348265cc6da2d18f82e4975752647f319923f6410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4458291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c1d3a96ef1a1f9fa65ad2744717e5f0278ee63eeacbf8fe3d3cca04eb3c7c6`

```dockerfile
```

-	Layers:
	-	`sha256:22cb46bfeee20af883fc28ef3588d621eae6116e7f3cd8c83a478e61730a9714`  
		Last Modified: Tue, 17 Dec 2024 19:47:15 GMT  
		Size: 4.4 MB (4417399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:908b4ad136537f2fffd444b751bd09eebad9ece8369fd683b1cfbff3e7155f3e`  
		Last Modified: Tue, 17 Dec 2024 19:47:15 GMT  
		Size: 40.9 KB (40892 bytes)  
		MIME: application/vnd.in-toto+json
