<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.10`](#kibana81710)
-	[`kibana:8.18.7`](#kibana8187)
-	[`kibana:8.19.4`](#kibana8194)
-	[`kibana:9.0.7`](#kibana907)
-	[`kibana:9.1.4`](#kibana914)

## `kibana:7.17.28`

```console
$ docker pull kibana@sha256:b768af1c4116777eb178dc237b432f52c415f2d53d08539ee84983bafcfd9a9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.28` - linux; amd64

```console
$ docker pull kibana@sha256:8c077b790e8ed307024e950f63169a8423a9118eea742d3b2c1ba2bf3c6cc1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353911510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a502980c08af4d35aac3cc6c1351bc4f634c53976877f6ca0cfcf89edcc27d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 31 Jul 2025 10:41:27 GMT
ARG RELEASE
# Thu, 31 Jul 2025 10:41:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 10:41:27 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 10:41:27 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 31 Jul 2025 10:41:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN fc-cache -v # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
WORKDIR /usr/share/kibana
# Thu, 31 Jul 2025 10:41:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 31 Jul 2025 10:41:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 31 Jul 2025 10:41:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 31 Jul 2025 10:41:27 GMT
USER kibana
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce7a9ecc935c9018ccc1770178b11986729441325b347f6a0ca2cdbd9abfb48`  
		Last Modified: Mon, 15 Sep 2025 22:25:19 GMT  
		Size: 9.4 MB (9431929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ad9b75ffc05c147455da48591847b1b688b27ce3beb143a0542c623505599`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c8b18c19270140ee63388cb260ccb5f852ca92b802daad6cf7669e72ab86a3`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd355434a97ddb6174c09eab64be756129a6b52a0ba65d24a524965ed5d3e03`  
		Last Modified: Mon, 15 Sep 2025 22:25:03 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc3b9669d90d4ba6fb3888bf7d7241fcd2767868e67c25414c9dc4ae3dc635e`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66785adf8849e0c3f854c7dc79aa8a7519ad43bd0f028f1dc855fe6189ce403`  
		Last Modified: Tue, 16 Sep 2025 02:13:54 GMT  
		Size: 298.1 MB (298112549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7a4a1f970c756ad6e34e323a4ed089d77872e82849b78c168d96015ec53cec`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e75e8397532b2b0936912911441bae590a4309be67e3a451e5c0281567c8a0e`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a41ed6b48d656d28ae80be03923f90412aae6ab6fc4316d6cc1b46aca72de6`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 4.5 KB (4502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a186bb1fb63faccadc32d85e70f3f9cbf83188bfbe3a2933757c93d98553e8`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e56a482f274a08b5aa7db229f481c2dee921c61f5b069ee80d1e43e218006`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 161.5 KB (161454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6971b6b93ec394b47b570ed7a5501fb3568bc04044580a423b24cb5a788e2d3f`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:81a5b2f7be311d55baceb4c214709888f845f45bd36c8f0bed10188b7f02fd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50092b40efd3cd81f110cc7b2e477f47ef20ef7ffb796d09ed069e664a0e54d9`

```dockerfile
```

-	Layers:
	-	`sha256:9d451f2b8a7dd90ae424e1cb022f6e170b55978f853216d8b4a47ecf6de5ac8d`  
		Last Modified: Tue, 16 Sep 2025 02:11:22 GMT  
		Size: 3.5 MB (3506834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:852e72838fdf1197f8b13366ecf21c48b98290b5983d012fd1bd9538780acdc4`  
		Last Modified: Tue, 16 Sep 2025 02:11:23 GMT  
		Size: 44.6 KB (44554 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.28` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1a7c7d2b4930bfc2100dcdb91509183c80793e69a818ac532ca979a8ebede7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368311226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee5215a6e61ac2c5c7a8102a1d3d00c53cbf9003e2b37aa69072422a357259b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 31 Jul 2025 10:41:27 GMT
ARG RELEASE
# Thu, 31 Jul 2025 10:41:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 10:41:27 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 10:41:27 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 31 Jul 2025 10:41:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN fc-cache -v # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
WORKDIR /usr/share/kibana
# Thu, 31 Jul 2025 10:41:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 31 Jul 2025 10:41:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 31 Jul 2025 10:41:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 31 Jul 2025 10:41:27 GMT
USER kibana
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1854241f5004c72ca3d32f90520bdc930ed16c8e73182a3c0324764fdb6bf64c`  
		Last Modified: Thu, 02 Oct 2025 01:28:09 GMT  
		Size: 11.7 MB (11661839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa48375fe3df45bcc1f65b397f67a268791a2bb484ebe281fd145967bd214f11`  
		Last Modified: Thu, 02 Oct 2025 01:28:07 GMT  
		Size: 9.1 KB (9093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e3bc7edde6b4679b2589e1587704da506795d5a9181fa7c8fe600d36a9df14`  
		Last Modified: Thu, 02 Oct 2025 01:28:08 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232b1b6275e53ad3f00f476a80998701b9d590bbbb394079ea16973bff8e1b52`  
		Last Modified: Thu, 02 Oct 2025 01:28:09 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c99e74ceb233a45f3b76f4c9d2526dd50394e696fccb829bb6cac4baca1b2e`  
		Last Modified: Thu, 02 Oct 2025 01:28:07 GMT  
		Size: 5.2 KB (5246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62711f3e63e4b1733a4eea1e878ba8b1d22b0b0461b770629d158ae6bb96ddd4`  
		Last Modified: Thu, 02 Oct 2025 05:16:40 GMT  
		Size: 311.1 MB (311148129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d5eae3625d55ac95b9799989b08c389e4c9c866afff540f382d5298fe9cde3`  
		Last Modified: Thu, 02 Oct 2025 01:28:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245e53cb911ae0dba212bc2af4ffc931a7c3d567aed189e46937faf9af42c5e`  
		Last Modified: Thu, 02 Oct 2025 01:28:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97daf9868a8f1a5f37f2ceb6f02986a4ebdbc8c6ae67cce1dd2aeeccf51f9fe6`  
		Last Modified: Thu, 02 Oct 2025 01:28:07 GMT  
		Size: 4.5 KB (4502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ce53517c7f0422e79aa1f675131ef13a24964a7d7e5741ce451ba226bcd294`  
		Last Modified: Thu, 02 Oct 2025 01:28:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e0f282709d0e8d0efee4ac5f55a3aa08629101e3776d7690b250be5a39550`  
		Last Modified: Thu, 02 Oct 2025 01:28:07 GMT  
		Size: 158.0 KB (157993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6a120d06faae4654621393671a825244ec9055328145d49f1f819b3af94a9e`  
		Last Modified: Thu, 02 Oct 2025 01:28:06 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:6d801d7d652e9a705d45fa4634d6b7fc700039e66144144f315a235a47a263a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac6d92ab6f1d8538a477a08789d11e10c727c4b5679b839d82b0225cdcc92f`

```dockerfile
```

-	Layers:
	-	`sha256:c7524dec9976a20d00ce62e78811625080d7249fe0a12040a9484309719aed79`  
		Last Modified: Thu, 02 Oct 2025 05:12:00 GMT  
		Size: 3.5 MB (3507898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b50728385344869cbc7df8798012cd96a123ebd3d3fc763330181f63ac0ddd`  
		Last Modified: Thu, 02 Oct 2025 05:12:06 GMT  
		Size: 44.8 KB (44844 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.10`

```console
$ docker pull kibana@sha256:678682c3890c6ca3ad82112f5b96255a1f33a30eba865fe0914f5081dea583d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.10` - linux; amd64

```console
$ docker pull kibana@sha256:44238afacf7d44dadf439be01ef21bd37700f2e0c5071cbacaab5345e1367239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403301764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a575d693af39c96bb672e2759ee54eaf4db0d37ea9085ab5f574b89f8b7ae73f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:18:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-07T20:18:34.689Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-07T20:18:34.689Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed8d1f45f9020b85b5181ad0aeb9812b36f1d74f06f6ea8da5d77c254064363`  
		Last Modified: Mon, 15 Sep 2025 22:27:34 GMT  
		Size: 9.4 MB (9432038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe00be9766b15485a0cfbe5c59cd71a44d701e70d493861e4d43da3271e9b746`  
		Last Modified: Tue, 16 Sep 2025 02:16:40 GMT  
		Size: 347.5 MB (347502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac41dcab66840ae15727463fd022227b2248bda392adf917032a951e0752db50`  
		Last Modified: Mon, 15 Sep 2025 22:27:33 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56ccde6fe5e4ff3c04248052b164d3cf70e981de190435a2d8a6beb2f004a7e`  
		Last Modified: Mon, 15 Sep 2025 22:27:34 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd734d4f09987cb9459d64e5c09db07f5619c69abc44a2d5640fd6ff682363a6`  
		Last Modified: Mon, 15 Sep 2025 22:27:33 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4912d7eb41415bb7243053e84928b5fdc559230ab3345215438e6f9cc343ce3`  
		Last Modified: Mon, 15 Sep 2025 22:27:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4175fabb12ef89237cb1f663c8032615c19b894583685d9032d2ec202d2e60e2`  
		Last Modified: Mon, 15 Sep 2025 22:27:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48be88743844ca7d3c5906478f7022b45046530a894c5afeedfa5dbb850f705e`  
		Last Modified: Mon, 15 Sep 2025 22:27:33 GMT  
		Size: 4.7 KB (4726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e585404e59a319bdffb6762a7c3cbcac99685e6464d6fdcfdf1735a4f773ad6f`  
		Last Modified: Mon, 15 Sep 2025 22:27:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f18357d46a09d2f911f63af52af512619d862991c6526262a3eed58c0d90a5c`  
		Last Modified: Mon, 15 Sep 2025 22:27:32 GMT  
		Size: 161.5 KB (161454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a5b839b03d2a92323a1ba26f930fb798cd47768ed192d336a01c4187e7a6dc`  
		Last Modified: Mon, 15 Sep 2025 22:27:33 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:c049fde25cf169b285378df1ff52dd46a9ab20d8efeb31706e50b49f01805692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4560874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585138c6cf5167dc074be0c41e889ea52973996e4f696396eb766d359b3644bc`

```dockerfile
```

-	Layers:
	-	`sha256:f993b28ad7c68907d24ff187bd1b999ad0df1d54b9c803a72c7f87f2fdebfe36`  
		Last Modified: Tue, 16 Sep 2025 02:11:33 GMT  
		Size: 4.5 MB (4520140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00655392f83aa0d998b822806c325d0e52fc32bca8bccf8fe4a73ec9d6f32bf9`  
		Last Modified: Tue, 16 Sep 2025 02:11:33 GMT  
		Size: 40.7 KB (40734 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:333bf2748f6ee4157936b85d619aafd247af573948bd05c82c4fe32cbde85e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.7 MB (417714819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713d5fb6009c06847611ce499578375e230fb3968919b183b97392c361f27f1a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:18:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-07T20:18:34.689Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-07T20:18:34.689Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2930a860c87780ce2a08e3d60b41ded9cb19b3dcab16266c4b91b55b25c0d4`  
		Last Modified: Thu, 02 Oct 2025 01:31:26 GMT  
		Size: 11.7 MB (11661910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c229085043b12af3da3d246cbe1ee5745b423b35323a5c1cafe665781dd7f4`  
		Last Modified: Thu, 02 Oct 2025 02:29:41 GMT  
		Size: 360.6 MB (360551598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de5833d340ead483933d554e6962d9f744caad6cef8d965a592c2bcb89d3623`  
		Last Modified: Thu, 02 Oct 2025 01:31:25 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e283b486826836baf5586cd849fdec54fbc9acfcc819dde72349ccd58105993`  
		Last Modified: Thu, 02 Oct 2025 01:31:31 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb9193469673a311bfe4d95e9c07ae03e74756b4e2e5f28383c3a6da8b91d7c`  
		Last Modified: Thu, 02 Oct 2025 01:31:25 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04badfbb790de1d6ff59f099146e8f70f337cec8910a1e5a95fee4fc1a1b9b94`  
		Last Modified: Thu, 02 Oct 2025 01:31:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136e8bf93dcc27638cb7e237b7a5749dc89c3c042daf6b8a6748c99df7b45f80`  
		Last Modified: Thu, 02 Oct 2025 01:31:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8590b227e84bc1f59ab273a22e53ee6227546284e06e45d97dc8e80220b4e5`  
		Last Modified: Thu, 02 Oct 2025 01:31:25 GMT  
		Size: 4.7 KB (4727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad079076ef87ed08d6bda678d903ede4869756bacceee9cb6c12e21ac5f1812`  
		Last Modified: Thu, 02 Oct 2025 01:31:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0e454ceb08a526a8c7f44fb5abfaf5ff5d829ea86c2ada52d333a14b143263`  
		Last Modified: Thu, 02 Oct 2025 01:31:24 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd073c751d4965b17b9a3c71017f5a0c1674c65b77c9720635bf4f7a435d4a92`  
		Last Modified: Thu, 02 Oct 2025 01:31:24 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:717f28a9fa6d1537452f88a2ad4ea0117ef73babefa42a7bf491917e43a538b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4562198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31de9f51b620f0fbb09733cbe7ff2f0269684574cc55a530c587f9fe50bb835c`

```dockerfile
```

-	Layers:
	-	`sha256:562c72b306fb4fdf7bfd7aaf499585756b412f12382b285be130c3a037a59fb5`  
		Last Modified: Thu, 02 Oct 2025 05:12:08 GMT  
		Size: 4.5 MB (4521204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d6ecff394c09d94b0b50c1b380e8d2f6a269cb4c645a10663a914a632c754e`  
		Last Modified: Thu, 02 Oct 2025 05:12:09 GMT  
		Size: 41.0 KB (40994 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.7`

```console
$ docker pull kibana@sha256:72ea8dec3842bd718334d6fc0b36024fa7bbbac29433a9178bf10478ecf9e80c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.7` - linux; amd64

```console
$ docker pull kibana@sha256:6aea27bfa3d82e8d91cbc7cece97debdc07b3a40ca8aa3857ba5a335fdccf714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.1 MB (424060436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a4870148670ee160a9064ff06b2848b374f25a4a1fade4d75b98ee2c6bfa23`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN fc-cache -v # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/kibana
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T20:18:41.039Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=7ccf3080fcbd0ec666f88b3b7515537bd70da14c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T20:18:41.039Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=7ccf3080fcbd0ec666f88b3b7515537bd70da14c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36fa4afddab95148c7af59007a1f58d4478ad91cd8d704e4ffb8a3ff1a45d6f`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 9.4 MB (9431941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1f1c393f52384bb9dafa14786588da009bb517817d8259b4714126c2984d2`  
		Last Modified: Tue, 16 Sep 2025 20:16:25 GMT  
		Size: 368.3 MB (368261404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea93b49b0ef51e8039e8a5d44ab8b79af23176760581fdbb52fef1390fa0c3dc`  
		Last Modified: Tue, 16 Sep 2025 18:08:34 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9a7c685e14192461c16832c186875764e3d3c4cd8d23b9e70dbb99efa3f282`  
		Last Modified: Tue, 16 Sep 2025 18:08:37 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372df1bfdaa67954a145b2c89f3822f34c818210d5029917957814c399c9e783`  
		Last Modified: Tue, 16 Sep 2025 18:08:35 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715b588be7e19d8ae37c03c757cbcb01bf78b1f303982083a08812468e7e89c8`  
		Last Modified: Tue, 16 Sep 2025 18:08:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a219996342d11019b85782c2dd6864fb745076a3cce167cfceea01796506ecb7`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6ba89a5481523fc75f4a4fecfd866d881feee97683541e9c3ecada0cee646b`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 4.8 KB (4758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1f5a4717be51d139af45bdb234a70298b52eabc4f6ef9bae817c439a9970b3`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b861e625bd98b3683ffda27d05437258cc5f9938d0e5be487043095b11a84f1`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 161.5 KB (161455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049214e99d7d44c89275c812d558b5d207799e95c3be6100856bf6a5b3897d2e`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.7` - unknown; unknown

```console
$ docker pull kibana@sha256:e69f1b8fa5cf4cf1d54e7f647f421a36b24194ffdd2fe67625e81eb20efe0f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4897615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81db3c7432307223f82529d76a45f8cd1ab66aa9b184c0ab4628b05e5f4812f4`

```dockerfile
```

-	Layers:
	-	`sha256:8971f97e11fcdc503f65b5e942d47a9ead2268d6003bcde1c3e46b9243e9bc24`  
		Last Modified: Tue, 16 Sep 2025 20:11:23 GMT  
		Size: 4.9 MB (4856888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9013307606a0e891ed352374afa740b69b212109eb8e6bb7dc3b7e3faad87831`  
		Last Modified: Tue, 16 Sep 2025 20:11:24 GMT  
		Size: 40.7 KB (40727 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:3bbbc89915afda112e4e2cc63f571e51ad200f03e234f8ef79d5ce99e28f717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.6 MB (438557211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f165a38d314951df27004724fde3146ef74b0fa6b2a514e04397bc03ea161d3d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
ARG RELEASE
# Tue, 16 Sep 2025 08:32:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Sep 2025 08:32:12 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN fc-cache -v # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/kibana
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T20:18:41.039Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=7ccf3080fcbd0ec666f88b3b7515537bd70da14c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T20:18:41.039Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=7ccf3080fcbd0ec666f88b3b7515537bd70da14c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738eef4d5f06761c67a02fa7099d438ab978de6455725f2fb2f1d93c3ae0660e`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 11.7 MB (11661869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e9777ea361f8041c38e44aa9650e2661cc7b6b04dbe05da6860f9e007e2e11`  
		Last Modified: Thu, 02 Oct 2025 05:19:02 GMT  
		Size: 381.4 MB (381394009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca30ca9ff912da58a1e9b4811fe4302d50fc8258157e1b058335ef8fa755d805`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f000f2f16da722f4dfd1ef1a081bc95dbfdb5d1d335b5b29b84409208f7797`  
		Last Modified: Thu, 02 Oct 2025 01:32:23 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290b4fe22ddbd4e566bf4a8c7f597d40d1ff297512f91a755415b26d9bb45b34`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a79e32712c72ca8b8a2259ebe7405ae6148aa78ba78a820c0e4761d7acc243`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bb3ba75ac51bd2e5b38f2b63690b6f79399edafb9975463acbab6f70c163cd`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3286b66006bbbdde457958f71b0f749dc3656e39bc1505d0ef56ec0ee37ebe28`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60342f1aede3eaadf96b91ba6977fb968383596b5a21f8d0f61042125c60eaf`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287802a34ee59bd350b1a642e93c357345fabffacc998d8c665786349792b90`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 158.0 KB (157990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9ab94ff0a57bf30815ba669c2427f647ca494c4a944cad890b2e6eab7da3c4`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.7` - unknown; unknown

```console
$ docker pull kibana@sha256:781c6873b2d39a21effc9c4638fb541768ad44769f118058dd4f3923c8e75065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4898939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decf5a06a07d91043bdb904446410c9a90d1eb028ad571c98a93e694e8459884`

```dockerfile
```

-	Layers:
	-	`sha256:355f82680e532ae880b6969eb248e2cc435e289439ca1ea9430c43fdf72a0b6d`  
		Last Modified: Thu, 02 Oct 2025 05:12:14 GMT  
		Size: 4.9 MB (4857952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211d194fe475318c496d288f59bd423249c1583bbe5c171922ed068147ccaa18`  
		Last Modified: Thu, 02 Oct 2025 05:12:17 GMT  
		Size: 41.0 KB (40987 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.4`

```console
$ docker pull kibana@sha256:ac2b744e241f7637145596f87c0a0dfb148990150f3befc413cb7648aac3ee61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.4` - linux; amd64

```console
$ docker pull kibana@sha256:d9c60a212584ac18b10777193f08d4920f2aaca07dbf1779ac232094b10df101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436883793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552ac60c6cd69a7fc0f4481bc050fa06b4c4124e5afbc2325244148a3d6bd176`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Sep 2025 08:07:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T11:08:45.034Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=57608cbf53423b24acae7c1e589faf57a6bacaf2 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T11:08:45.034Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=57608cbf53423b24acae7c1e589faf57a6bacaf2 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56558de458071f5470de7ffc60ca1ffd81cae3e76d5c3565cb9bb17e528020a8`  
		Last Modified: Thu, 18 Sep 2025 18:58:53 GMT  
		Size: 9.4 MB (9432027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f02375930a9f8f36c8ddeaf2b8c5183204b18e487e35051d8940498ab824040`  
		Last Modified: Thu, 18 Sep 2025 19:12:18 GMT  
		Size: 381.1 MB (381084642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72c7e10b9112209bdcbc9068e5faa8a81d3142ab5879c9b10e2f5cf83f98ca7`  
		Last Modified: Thu, 18 Sep 2025 18:58:51 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1831e156f53f1195eada618d2677d60672ffe231f461f42e54827789097b4b3f`  
		Last Modified: Thu, 18 Sep 2025 18:58:53 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b4493ff80b34245f3499c234cc155def038d9d9b07d37df87a859b555631d3`  
		Last Modified: Thu, 18 Sep 2025 18:58:51 GMT  
		Size: 5.2 KB (5237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2b9995ea451665334bb996e798d5f2d092321533110d9f41ecf5796d977111`  
		Last Modified: Thu, 18 Sep 2025 18:58:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2015cbc9185718a3e36d413e74fbf8f6304d7c32537a936a5864b86644e4f4`  
		Last Modified: Thu, 18 Sep 2025 18:58:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429cd00e5d4ff66068da70e11f1955dd6a95c640c3addd8227cc2d0ae50ea43`  
		Last Modified: Thu, 18 Sep 2025 18:58:53 GMT  
		Size: 4.8 KB (4801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a2c12027b21bdd9bc4a66dadef6811b4f5ff2e02e764f5619f9499a24011b5`  
		Last Modified: Thu, 18 Sep 2025 18:58:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac29a41b2a16b6bbf2b1dd33f124043eb3aa9a1b0dcbc00b317af5ac5518b56`  
		Last Modified: Thu, 18 Sep 2025 18:58:49 GMT  
		Size: 161.5 KB (161455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b90f081a47a895990a9f9e4351e40deb0d1d3599b5435d01e838c71b7f700a4`  
		Last Modified: Thu, 18 Sep 2025 18:58:49 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.4` - unknown; unknown

```console
$ docker pull kibana@sha256:a1610ed6d6402083252aaed2497b0256e1cc1f3811b644e9708cda50a96e8a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c303da30ff32cfd74d61f6d3a3c96c558efec6a0b2904356ddc24bd57e6e7e`

```dockerfile
```

-	Layers:
	-	`sha256:41c1a1475e169bd28e1bc49be639c8cc44114e75211bced069ed34b917ac347b`  
		Last Modified: Thu, 18 Sep 2025 20:11:28 GMT  
		Size: 4.9 MB (4870464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69c6ef9bafdcae76318ab1a94ecfb1e0bcaa35c371e427287b2a1fa712a5d16`  
		Last Modified: Thu, 18 Sep 2025 20:11:29 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:2a49a59d577dc3e90a413e1d33614f191f723f0afd17eeb1611843455305e982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.1 MB (451111080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a18b6ba6668482dfcd5ee685f55c9152333d1ac68aa0ff81847a9f75a9f2b35`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 18 Sep 2025 08:07:26 GMT
ARG RELEASE
# Thu, 18 Sep 2025 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Sep 2025 08:07:26 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Sep 2025 08:07:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T11:08:45.034Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=57608cbf53423b24acae7c1e589faf57a6bacaf2 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T11:08:45.034Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=57608cbf53423b24acae7c1e589faf57a6bacaf2 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd580c186d5edf836994660f21b534898388b6059810f9bd2aec733c69ab01`  
		Last Modified: Thu, 02 Oct 2025 01:32:23 GMT  
		Size: 11.7 MB (11661818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111399bdc9fe948b997084ed7b4199cce7d79621bc9f64ded34905da1ed477a`  
		Last Modified: Thu, 02 Oct 2025 05:18:14 GMT  
		Size: 393.9 MB (393947864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dc625571ec4a3701e281793851e1184755ac1cd6e37e2f92319219a45fac69`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812f5ecdb9c0e92e8c89c9002e0955e9ba77ef6ee00d9d7b9e96220c16693abf`  
		Last Modified: Thu, 02 Oct 2025 01:32:23 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d9fe7fceb56330a76bbea43992aeb85a90f999c28be699fffc194004b8aa19`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcdd6d27e7bb9467364637a247b7c3fa7cf71f0cda415404aeb458bdd568fd5`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d749fc197b85ea6d921a46159f28bdd3c444656ec1f8df7a606c1adf41da3bc`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3721f0e4dc88cd692c75529da119c4d38f886133f0093ca732d1783d9f50f3`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 4.8 KB (4802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30c3f02e99992499837cedb7ff81f56ac0f01ed38d1b1ed7c8f9dde37171b7`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e944549e2ad3c538ff1ddf0b12247bb150e7dd55139c86539427d8256ab088cb`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54b59c1089e8e8f14682c176d99043e7b750a4dd8ed86e448877fea2ea822c7`  
		Last Modified: Thu, 02 Oct 2025 01:32:22 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.4` - unknown; unknown

```console
$ docker pull kibana@sha256:756147ce43b970c276a305565209b1411d0c235efc2fc639b3084e93bf7d4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4912738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f66bfe1e17c0725eee7e686b08b3326175622cf7377c396c92d1cd44aebb`

```dockerfile
```

-	Layers:
	-	`sha256:88cad033eaea29a0775e40a075bc5312a7b7b0436ef6039b9dcfe5b1473d7177`  
		Last Modified: Thu, 02 Oct 2025 05:12:19 GMT  
		Size: 4.9 MB (4871528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f57483af9b0b4d4e58ad1c9e784a9443d465cb4a6dc4a1751bbfd3f81fc7469`  
		Last Modified: Thu, 02 Oct 2025 05:12:19 GMT  
		Size: 41.2 KB (41210 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.7`

```console
$ docker pull kibana@sha256:c267abf7954ea5f61ada8cc764f6a5082bab1b3002e70d8d1a07d24b56e3e4a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.7` - linux; amd64

```console
$ docker pull kibana@sha256:6dceccbc2908a08df5036cb8ab7567ea7c8abb94fa9944dcb397dc9e86a37e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 MB (438662196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9679cfe731b8caea2db3a4defd3b5927d97fda819a1d5162853bbff5ee5b65`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN fc-cache -v # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/kibana
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:33:24.878Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9d44cc2d50d27f4d3ae7b72f0fe6b612508674bb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:33:24.878Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9d44cc2d50d27f4d3ae7b72f0fe6b612508674bb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4045a7a37d35a23951d5589e4f0758bd42083ec1bb80bbf128998a5711cbbeac`  
		Last Modified: Fri, 19 Sep 2025 20:53:54 GMT  
		Size: 19.5 MB (19530274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd752e4b644407a830db203f480a3bc1d384937739ba12b4ab13418aa56c0361`  
		Last Modified: Fri, 19 Sep 2025 23:16:08 GMT  
		Size: 362.9 MB (362924919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997a9ce9ab8f18746010dfc100cd809fb347ed2ef3c81c12e3245dd642f64c2e`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eddedb85e411d5886be217eca2a16a18c513dc951d04b6e37668f95d49891b`  
		Last Modified: Fri, 19 Sep 2025 20:53:51 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac969651755e8349243a76041b75eaf7e0254abe5b10a34ceed27930dce8f64`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd72eaf096663a7542de1a8993aaabd5f2425d93165d37678dfb9768f3cb87`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c894183b4676744f5803cabeafc8fd275888d28bcbe0eaa5080783ea071984f`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e394a10fd9adceefebd6935b8ddd200562ae9b7687df6dc20111b3c8f47443`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 4.7 KB (4690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e061ed588ae8c28494415a18ddd8194491c405d1060584eb32cc827236ba9797`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ab082fccb15d09740db5549bc49364b4bcce34e5a748bff68174b698cb1071`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 75.1 KB (75097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e4114c35fca4c8b491d5b293f62bbb7da9aeff6affa919455f95e8c0889747`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b976c6f712c0b6f4bd51cd00003feeaa19b7f8108e99562b5e9e40ce70a362b`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.7` - unknown; unknown

```console
$ docker pull kibana@sha256:60418d0642ada29dac26e027e0948b0eba2e9510a84105d6278fc4bbddc04389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5609768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bbe7b10c1ff807688b1c29141f64da11252f06876a5db88e32e6efe2b3e363`

```dockerfile
```

-	Layers:
	-	`sha256:77ccf1c6c2788427ba243729bcc845d49279078de5c02c06173b28ce9cf07a71`  
		Last Modified: Fri, 19 Sep 2025 23:11:24 GMT  
		Size: 5.6 MB (5566583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab64c71b9b4d821b88ac12b4020a375b38ae71ed67b378672c722b7744d77d0`  
		Last Modified: Fri, 19 Sep 2025 23:11:25 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:5391acd93cbcbeea5e628bfc874e2477315721011a5383d53b13f8833f17dd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.0 MB (449994645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ff636f1c4cea49bdf50fef357ef1e4d8fc8f0d64bcb28895ee1924794a46a0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN fc-cache -v # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/kibana
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:33:24.878Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9d44cc2d50d27f4d3ae7b72f0fe6b612508674bb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:33:24.878Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9d44cc2d50d27f4d3ae7b72f0fe6b612508674bb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921f39323e53460d96daddd522f5ba7f35101b6a79c265382af520b9f77dc89b`  
		Last Modified: Fri, 19 Sep 2025 20:52:52 GMT  
		Size: 19.5 MB (19487810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc4834af2e5ce115722da8c6d1184c9d724d5b47bbdb6299a2ebc6bb839396b`  
		Last Modified: Fri, 19 Sep 2025 23:16:36 GMT  
		Size: 376.0 MB (376049478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4931bb7e34c8d20899ec049001cbdd5d34195271b0a07c1f27fe69b9302c2ad7`  
		Last Modified: Fri, 19 Sep 2025 20:52:51 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb225a03bce36b046b98ec21896983aa1ebec9ca34f62669d13a53b35b777ca`  
		Last Modified: Fri, 19 Sep 2025 20:52:54 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae42f40d4330079979aa91001035601784a681b696b209bc8ada08458df2cc2`  
		Last Modified: Fri, 19 Sep 2025 20:52:52 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bca199880cad2c8058cfc03b5851cb7df7a43e22151c2922a16c2a35100d7d`  
		Last Modified: Fri, 19 Sep 2025 20:52:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8defc75851724d091da013b146d55acb2f0f2997b7d39b5c0e2e46719f75718f`  
		Last Modified: Fri, 19 Sep 2025 20:52:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0cd6b8c96c716ac8dfbb0e3ffcb3146fc8b0c9c75bac16adf50563bd7060b6`  
		Last Modified: Fri, 19 Sep 2025 20:52:53 GMT  
		Size: 4.7 KB (4691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b5439a2c657cb628e13a8d8eee57c78a8f67e9afbacac42837c8927deefc49`  
		Last Modified: Fri, 19 Sep 2025 20:52:53 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8981afb0360d08a801c352522b4601f9eba07727e0732d9a7e1b58b6c596cc36`  
		Last Modified: Fri, 19 Sep 2025 20:52:53 GMT  
		Size: 74.0 KB (73987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b640f297618711952e3207ab265ffd9ce264a355aa9adae435a6ce9c6648db00`  
		Last Modified: Fri, 19 Sep 2025 20:52:54 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c26019901bbb2f8867abd0e9f22bbbe59d3ab75e1492177ac7bc9293f2d845`  
		Last Modified: Fri, 19 Sep 2025 20:52:53 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.7` - unknown; unknown

```console
$ docker pull kibana@sha256:d8073da44f1e21fb6867e4aedfc0c7b7627d3a4b913c536ea95dfdd9290f15cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ae099cace36665211dc4a3b9b1ac44cecaa38a344380d8fe4ff424dd10b1ef`

```dockerfile
```

-	Layers:
	-	`sha256:242cbbe79e87860933c9bb5fcfb736221068ef7516103375a616c65a0bff5b7d`  
		Last Modified: Fri, 19 Sep 2025 23:11:31 GMT  
		Size: 5.6 MB (5565261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ebd2ff10af81950a8250c96d60743f83b328ff21a62048b9d1e19632cedbf3`  
		Last Modified: Fri, 19 Sep 2025 23:11:32 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.4`

```console
$ docker pull kibana@sha256:fbe8c7f43ba1cee3f130dfa490a13ec08e71d2b377d68dcdf282f1b184040081
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.4` - linux; amd64

```console
$ docker pull kibana@sha256:2870efd85d9203d93ff6b91914f09efe15e7f1f24c27122cebfc72383b2cea94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.9 MB (437877853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc25709ad108497bd4917c2d4fec885544eee3c3bef64f4f9946ea7b082eb9bf`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T20:31:52.531Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a8042692500503cca8f3d4aed3c38da398c22f9d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T20:31:52.531Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a8042692500503cca8f3d4aed3c38da398c22f9d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0ff6900d59320a5cdf5aa764b7da4b2ea1990d0f64c7230be5ff4e3f87d437`  
		Last Modified: Fri, 19 Sep 2025 20:54:51 GMT  
		Size: 19.5 MB (19530353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dc327c2a5211614aa9091ed08d60f98ee71750a43e6c2cea27d1f644f21ef7`  
		Last Modified: Fri, 19 Sep 2025 21:19:10 GMT  
		Size: 362.1 MB (362140480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41041c4ebf53c7b76f9a416fabece6dad42508d0f639935f318bbbb904d67952`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800b8c70fc0eec6e7a8693bb307c7ff9739612148e6b875b03b4aaf3acd45a71`  
		Last Modified: Fri, 19 Sep 2025 20:54:50 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c36b58541aad7e782fefefc43c743b0091ea855fa7ab1fa947b33170f88696`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c31fdce81bb9bd5495f91fa8562744eb736ac1ccb6d13dd4f3f53d573948336`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bf88aab3e1db77321563080e836f63ae0d954e8c00f83f3b7ee045c97316c2`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc80f0ee980d7d77761ba94182f29c70581dd796dd7152e10bce3c55a7472f10`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c436622930db43b9713a4c474d18e069a4e361d5150fb431a5c58948ffc4c44`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9048c5fbd2af451487278284eae789e0b6be95ae9039a25a304cd505dac9a3`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 75.1 KB (75098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fb8ceebc71b5a5c14119f24678d999d7d04029435dca5eb059d72f5be01b87`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9b712b970f7d02d3d190e59146520adbb256c348332780e2e16d29203a8944`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.4` - unknown; unknown

```console
$ docker pull kibana@sha256:84c98b97ceddb63431c85c5cef98997903012487ece3df0c9d5237e67d53a603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5734453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f259605cf67576a65c6faad5c28b58ae90622e7518e813c4273182624d71a1ba`

```dockerfile
```

-	Layers:
	-	`sha256:ad8c37540abfb6292f6769309aaea4f31b85d46db469763c96dae1b99bbfbba6`  
		Last Modified: Fri, 19 Sep 2025 23:11:36 GMT  
		Size: 5.7 MB (5691268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee73b0ffe77ad49b494587bb0743bf77422e695d4fbe8e5ffaaeb74b359ad7cf`  
		Last Modified: Fri, 19 Sep 2025 23:11:37 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:81ddc03c9779701495eb7118d0ea044719e5fa0696e3fa570997f24cb4d8d388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448937255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ec1ea077a9894a7465e1e647794efb0b80bae351a10d1e3ffa2b379bc2a30b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T20:31:52.531Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a8042692500503cca8f3d4aed3c38da398c22f9d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T20:31:52.531Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a8042692500503cca8f3d4aed3c38da398c22f9d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a589fe1b7484b7b32fda76842867b3e22820d68f901e497aaea69d50b4b21e`  
		Last Modified: Fri, 19 Sep 2025 21:17:59 GMT  
		Size: 19.5 MB (19487762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e624f6982b55cdd460e22b285ab90754b442355f29d36fe72166db258000f7b`  
		Last Modified: Fri, 19 Sep 2025 21:18:33 GMT  
		Size: 375.0 MB (374992105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8919afed3fee77a0155aa1acd61669813ba3e2c9d78daea54813f2aa3a3d9da9`  
		Last Modified: Fri, 19 Sep 2025 21:17:42 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210d968107f3bd2e238cae0bb384c980a65ee2f175982f2078501304a32af3e9`  
		Last Modified: Fri, 19 Sep 2025 21:17:58 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574d6700e05245cf5628ce7449063c71660df7ea64b09bc11fe0ec25b957bc94`  
		Last Modified: Fri, 19 Sep 2025 21:17:44 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b88ba7f76e2d163bdde6d9992baa26c0589161e379da0aecc4fc4791433bed`  
		Last Modified: Fri, 19 Sep 2025 21:17:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69e188feb9bc73f49a8f504af4a73e22e05419e4f2ae82be9af753b2ac7fad7`  
		Last Modified: Fri, 19 Sep 2025 21:17:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276a76e8a3b98363927f4aa814ba24eb55d2fb637b34398b8ad81b6c164e6cb`  
		Last Modified: Fri, 19 Sep 2025 21:17:44 GMT  
		Size: 4.7 KB (4724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce391345a5657cbafcb553dd940465c53d169fbfdc1674ee60dd8168c23e0e9`  
		Last Modified: Fri, 19 Sep 2025 21:17:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef55f0c7e2f1da713de38fd4e67ca4965741b85636fa2c1c5d6a216a2c068847`  
		Last Modified: Fri, 19 Sep 2025 21:17:46 GMT  
		Size: 74.0 KB (73987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c822f4b0405e69ae5a87e2639bdc900c1adcf52e132690ca889d02aa937c3`  
		Last Modified: Fri, 19 Sep 2025 21:17:42 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e44288cb442407b2d828264c629552333083dbb05452b2e9a8d9b58fd50d1`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.4` - unknown; unknown

```console
$ docker pull kibana@sha256:fb207c39b8232427df1789a7735a8017f2d98bbd8d6ae7a1c00b941e9a16b421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5733388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899019ccfff28e86740d5a0de95e23f1c9f72ee189b650d8e550f6df1a934a7a`

```dockerfile
```

-	Layers:
	-	`sha256:73b07c0f58bb8fb4d38f355277258d558e3e9f91940a6fd4f8ee4f4863d7fa8e`  
		Last Modified: Fri, 19 Sep 2025 23:11:45 GMT  
		Size: 5.7 MB (5689946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de59e3c3b1c78be42ffcbff18ffc5de545e705655d0df21eaadbfcf7b129e94b`  
		Last Modified: Fri, 19 Sep 2025 23:11:46 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
