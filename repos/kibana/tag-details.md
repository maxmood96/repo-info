<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.10`](#kibana81710)
-	[`kibana:8.18.8`](#kibana8188)
-	[`kibana:8.19.5`](#kibana8195)
-	[`kibana:9.0.8`](#kibana908)
-	[`kibana:9.1.5`](#kibana915)

## `kibana:7.17.28`

```console
$ docker pull kibana@sha256:69f188281a5dd3524a7b8accd36bc16faccfc977aeec3814ef539629f095eb4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.28` - linux; amd64

```console
$ docker pull kibana@sha256:20e9cffd82cbba7dadb5bf1f949451a1248ad1813d42753cae4c1ff75b8a17f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356307460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926aaaed455b312834811b83724588491957f5aca46e9c6a2b1a081e56674f6a`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae06239dba48234ce3e93e3c996fd33430a687efd826964fa4aa4453775ab63`  
		Last Modified: Thu, 02 Oct 2025 06:21:18 GMT  
		Size: 11.8 MB (11828335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4606077dfdb3657499b415e17884957fd5a5ebefe09f597ebea00174c6dcb23`  
		Last Modified: Thu, 02 Oct 2025 06:08:51 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8174e7d51c4f95ce47e672d0bbaf08d087b9935bbac1002b1d5cfb02bf7c9e67`  
		Last Modified: Thu, 02 Oct 2025 06:08:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcac0e42f1cd0d8afb705a44b10a3a2067b5460385f5d8d0bfa22be38afa11de`  
		Last Modified: Thu, 02 Oct 2025 06:21:18 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560dd8cbf3d9857a4351430a5097f509a4f1ec8f35ee932dbfe3a2e361a418c6`  
		Last Modified: Thu, 02 Oct 2025 05:13:55 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9463a8f695cfc920b3f5b83ebf786bc4a255a49c9469d3e9f9765faa5c6348e1`  
		Last Modified: Thu, 02 Oct 2025 06:21:48 GMT  
		Size: 298.1 MB (298112530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e08bf08def5f8df10a2bfe445f5d1e29e32de430c2cebfe78807623677b1464`  
		Last Modified: Thu, 02 Oct 2025 05:13:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0c142868d8de0ee5c0708e02acf3d4ac3ebeb6b99b15b400832f45e274f15b`  
		Last Modified: Thu, 02 Oct 2025 05:13:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f39eebbe23ec0e012475bce8e8a2470c3355ac3536a8568fbdfecd8d61f7431`  
		Last Modified: Thu, 02 Oct 2025 05:13:55 GMT  
		Size: 4.5 KB (4503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21938c699550184c7f9fcd3bb19ab74d1571dd83a6777ba80fd3528db992884a`  
		Last Modified: Thu, 02 Oct 2025 05:13:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6f62a121b016500d6a950f445bd005bd4dd23cfd6a5f239a4a0dd2140ff156`  
		Last Modified: Thu, 02 Oct 2025 05:13:55 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ce0710a18fc33337290c507dfaf9b470b50e4cf21e840545484e53db76eabf`  
		Last Modified: Thu, 02 Oct 2025 05:13:55 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:ea0602e7494445653329db310934ab0337b13adac4d4cae52b30f1f35bb5d57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fabc825ac61fd16b0d5f6b2e4b2ad3365560759b46715c4cbb8a170e4c0844e`

```dockerfile
```

-	Layers:
	-	`sha256:1b0661268a3ddbcfe4bfb871639f4943f3daca40dfef39b640598311c343691c`  
		Last Modified: Thu, 02 Oct 2025 08:11:19 GMT  
		Size: 3.5 MB (3506834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e0993589da97d770054a7a5c1e9ec0ac3c5437536d899a56199f2d4b8f133d`  
		Last Modified: Thu, 02 Oct 2025 08:11:20 GMT  
		Size: 44.6 KB (44568 bytes)  
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
$ docker pull kibana@sha256:27f8ab1b8db2ced52753a340f2bb31a3ea1df3c81fa8853c00e4f7968c1e3fd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.10` - linux; amd64

```console
$ docker pull kibana@sha256:b139c844389e3260ecbad9193c3b3c0b7440f5ec4b6dd657d9ce03334317f42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 MB (405697632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c3c8d4b27ff384708b21c862d9fce07022ced2c1a959e454a9f84d8d11e8c1`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e96f04ea9d07cdc37034fd93c484e121e75e4ecc5a4cbf03bdb0fefd958c6e7`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 11.8 MB (11828363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35583d68b49d2d7c430fb239d83d42f9d6e64b9e78445c5f2bcd901ff3b21ea9`  
		Last Modified: Thu, 02 Oct 2025 08:16:33 GMT  
		Size: 347.5 MB (347502637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d18c4092602fd6e2aa179e466c02152f2aa0f39c8974ba09de9ed88fcd060e6`  
		Last Modified: Thu, 02 Oct 2025 05:17:57 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1fca01f5f955712a1b56d5563084fa6778793804fd86bb98f5747b46d0c183`  
		Last Modified: Thu, 02 Oct 2025 05:17:58 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad33a8b45975f9f9039fc3dd86815985981c4d7c9c5dd5d20b75fa0f62c215e`  
		Last Modified: Thu, 02 Oct 2025 05:17:57 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2061c6c83aec80347d588a8031fbea12513de476781196276b831f9dce6ae62d`  
		Last Modified: Thu, 02 Oct 2025 05:17:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3d5c500deb824592d58783c113368f724a389fc487be8128777bff6c959c23`  
		Last Modified: Thu, 02 Oct 2025 05:17:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde55392bbcc4649b833ea1a2337bcad3912d995dbc3659d27391af90124e8a1`  
		Last Modified: Thu, 02 Oct 2025 05:17:57 GMT  
		Size: 4.7 KB (4727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e471cd94ddd46b17d83d99cb899da3bfeeb0744be9deac9505a34aca3a6eb1c`  
		Last Modified: Thu, 02 Oct 2025 05:17:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf428e48617a940a7bbc8fc5b537ef1bb1fb99446aac9bfad75db166940f8e4`  
		Last Modified: Thu, 02 Oct 2025 05:17:58 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4d4031365c07867334cb0130f60077d5d6358716bedc8455a6cf5a150fe60`  
		Last Modified: Thu, 02 Oct 2025 05:17:58 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:7763cd21dc426efb9884f3cf28a23e625c773614c8c2198506f8dfdb29078d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4560885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1208b6d986472e824be82cab0f13fe93cb13163e6b194e3153ee92b9d85b71`

```dockerfile
```

-	Layers:
	-	`sha256:e8c6cd7d7cf2bab35fc198b913f0645aa5b5d5216d3f17226d7009d10c5cc902`  
		Last Modified: Thu, 02 Oct 2025 08:11:25 GMT  
		Size: 4.5 MB (4520140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8acee0fa88304ee8f8fa07bf8d86fe76b5c677aac34a773f08d5512d98b09a4f`  
		Last Modified: Thu, 02 Oct 2025 08:11:26 GMT  
		Size: 40.7 KB (40745 bytes)  
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

## `kibana:8.18.8`

```console
$ docker pull kibana@sha256:0fde9465ea61e4fcbd61c1d7c8c1fcc4a3085b0c0b37c1ed111a6881bb01e7be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.8` - linux; amd64

```console
$ docker pull kibana@sha256:721d85f82225cee468be03bbeba6f076e396926303b5932687ea94eec6003fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.5 MB (426474239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a8bd02dc1e8fd646879dd103a9781a10586bcf010b5d2e4c498c92e6f7da49`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 13:08:19 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T20:20:10.933Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T20:20:10.933Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af67f23893603a2b3a2c94b26469fc3047bcde2ccf90e9543966f6b62e68dbaa`  
		Last Modified: Mon, 06 Oct 2025 20:45:05 GMT  
		Size: 11.8 MB (11828430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f445eb0458a0ce524fe83e1eccc0d52a1a4bfede49999b9f62f0e21fb7436b8`  
		Last Modified: Mon, 06 Oct 2025 23:16:23 GMT  
		Size: 368.3 MB (368279129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80e396e82644006c641ce66276c9c651e7a1346678e8275af4a45d95a29a316`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4b2eb6a80d2c8fe8147880f3fe39c830476d3dfa314f08eef0b4c5026585bb`  
		Last Modified: Mon, 06 Oct 2025 20:45:14 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac63027273a395ff83465b8f928a85f4719c37b41d9ce0f3aa74420a77858ca`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0959bb684ccf335572d6a0a64f39f90f776055e552f119a2cd8b9356d172398`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe104783274fa299dd3ef6c8cf2b3ee533b2a0377107ffa96c640c841644a68`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cedf077f39087950494b5cff26dcb0c86446c7fb9fb38ea5778cde19a4a705c`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 4.8 KB (4765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f4079a739b9c40ede6a549349e64cbeaf2841d5c567ecdf78e77ca1bf1476d`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127d4a324ea1892ed188747e0fda9460ec2eb71a1f9550e304e325c44df646af`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8120e2b8a76b1cc6e43706ce0662813f80f62f66ae929acf317eba7d697640`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.8` - unknown; unknown

```console
$ docker pull kibana@sha256:0a18685fe1416568547db19d181095cbe854b8643074dff675d742c804ac3c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4897629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed834b3409f2bfb36f4c3381d17bc5c53d31a98928546379439f72edaf410b6`

```dockerfile
```

-	Layers:
	-	`sha256:94eb050236083daa0275e6b5cb43c505118d84ae5be98eaae20604ccba3d7485`  
		Last Modified: Mon, 06 Oct 2025 23:11:25 GMT  
		Size: 4.9 MB (4856890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f77b992d0dfe254eb40e6b830ac12f8fea47ee01ec45da9f708797091b85e31`  
		Last Modified: Mon, 06 Oct 2025 23:11:26 GMT  
		Size: 40.7 KB (40739 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:4cb4a80f12a84eeed2a0399f92dec1d27055f3cdead8ead7f3b7a9e9fe7f703d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.6 MB (438570537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691faa68942b53b51540a16d4ee7fdad42eb30426b8d80f1a34868496a71a560`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 13:08:19 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T20:20:10.933Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T20:20:10.933Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2517d9622d5e73dd61e05ca560a96f4b837dcb7542dab410d682ea13b6e3f67`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 11.7 MB (11661899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497bd360f504a55f4d3fb87cd25484626983eeff1d3b2bffd6bfbb223ceab67`  
		Last Modified: Mon, 06 Oct 2025 23:12:56 GMT  
		Size: 381.4 MB (381407294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0aad46af8ca55fb6f42527266f7366cd3c777b516a480f6d2024fe381c0ec7`  
		Last Modified: Mon, 06 Oct 2025 20:44:03 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6cc8744b67129e752e7219a0996c072c6c77ed31decc9392ab11a9a679972f`  
		Last Modified: Mon, 06 Oct 2025 20:44:05 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b8a63cd5ffe661b2c647c946d3b9f7fba1f1a09f809d05220d62370944db51`  
		Last Modified: Mon, 06 Oct 2025 20:44:03 GMT  
		Size: 5.2 KB (5248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77224ff5310168768090776eb37dbadd058effca03e24a7e52c56aabd10b1e7`  
		Last Modified: Mon, 06 Oct 2025 20:44:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433089f772e1eacfd550613489ae0d8042e1fd091ddcd8c663e08a01d1c1b1d4`  
		Last Modified: Mon, 06 Oct 2025 20:44:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb02d3fa782c41931c157507120a359e674192a1dcb9a8356ce712193cdae1e`  
		Last Modified: Mon, 06 Oct 2025 20:44:03 GMT  
		Size: 4.8 KB (4765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e4332403b819059d4bce5d1a2efbd3116b5a7091cbffc52d576c009cfa6e01`  
		Last Modified: Mon, 06 Oct 2025 20:44:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63dbdf0e098d9c537942e9658231c121a6bdd4ba5c59662b3c6cf8f7e96de33`  
		Last Modified: Mon, 06 Oct 2025 20:44:03 GMT  
		Size: 158.0 KB (157998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1dbc05094c7109c8768da41d8ef448724fca143ee068aa66ad874dc7501831`  
		Last Modified: Mon, 06 Oct 2025 20:44:03 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.8` - unknown; unknown

```console
$ docker pull kibana@sha256:239658580b9e70357748bb0e594967775c980d84b65d4edae4c6f8f04fad6548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4898940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6121d94c3e8a1b33b7136f7e5f5086e11a219e1ed46f1251f3592a4584a2e5`

```dockerfile
```

-	Layers:
	-	`sha256:7825b85d84f3ee7c22f7143837ddf768495c8188792bb1903982a914ba30344c`  
		Last Modified: Mon, 06 Oct 2025 23:11:31 GMT  
		Size: 4.9 MB (4857954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755e08d204643c22bb6eb56de699c2896798f17f04281d283ca5fcd3ce04f32d`  
		Last Modified: Mon, 06 Oct 2025 23:11:32 GMT  
		Size: 41.0 KB (40986 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.5`

```console
$ docker pull kibana@sha256:ec4e24225e989eb5c44e8f661643f144a1aab66c3d782bd4dc829ffeeefe79c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.5` - linux; amd64

```console
$ docker pull kibana@sha256:015deb552ffac06ac5461a403b9016310d6b71122ed0b7208017a60a10a22834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.3 MB (439261854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5bc8b7976d5694a53ffa0074b0674459e612bc0822b2de35a282097fb24a8a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 13:08:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.build-date=2025-10-03T16:17:52.399Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2ceb68bd03a3cc20c26495ec986ed4f244589d69 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.5 org.opencontainers.image.created=2025-10-03T16:17:52.399Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2ceb68bd03a3cc20c26495ec986ed4f244589d69 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.5
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 13:08:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dc5edd07d53768b9773ec56e0e6054c422e105b9ce0969119c88465d6251f6`  
		Last Modified: Mon, 06 Oct 2025 20:47:16 GMT  
		Size: 11.8 MB (11828385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16837d54e55badcf0b9f913c5aa0b07937cfdc38887cff828cb1f680a82f353e`  
		Last Modified: Mon, 06 Oct 2025 23:13:19 GMT  
		Size: 381.1 MB (381066735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99b33587297a4c26c26e06b8c276847a4dfc97c3ead347bc6550201ce67b2ad`  
		Last Modified: Mon, 06 Oct 2025 20:47:04 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5bc56a84cba35c31c22ff10ac359989971bd61bb96e9f3f9cd6ec3c92eeb70`  
		Last Modified: Mon, 06 Oct 2025 20:47:05 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051b29612af83ae08ecb1dc28ed9796339eb5d1536cda26d0d918b9b3cc5745d`  
		Last Modified: Mon, 06 Oct 2025 20:47:04 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210d3c298937af86f6e335f5dc933c1946c1c7ad2bc1a861d53c40fec6f727f1`  
		Last Modified: Mon, 06 Oct 2025 20:47:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58219c9e36be8791afb6948b5fdf47a60f40bbe189b35681910b3cd1fdcc3905`  
		Last Modified: Mon, 06 Oct 2025 20:47:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185a986fbbccae5b3c98715c9ed9672676e59af6fc935550b802cbfe1c84aee7`  
		Last Modified: Mon, 06 Oct 2025 20:47:04 GMT  
		Size: 4.8 KB (4811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d64dbdb75ffb8c0ed76b16db3cc012c5a47a0f66cbeb820fda384fa57482f`  
		Last Modified: Mon, 06 Oct 2025 20:47:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347d4a2e814631017ee352a8ad1acfacb47f848f90f22ab9980ec31d362bba24`  
		Last Modified: Mon, 06 Oct 2025 20:47:04 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d36120d41532aba70f8deb5bc24b699bbbebd84a994e3d9d418d84e2ade13e`  
		Last Modified: Mon, 06 Oct 2025 20:47:03 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.5` - unknown; unknown

```console
$ docker pull kibana@sha256:28904c912b1c4840b3f708d00890b6bec1c4d7bbaa87ea802b25e7f8e1e3cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ea049e2c0ebb315ee6a26853733bf8effd70bb68fc089b790919d8821ff747`

```dockerfile
```

-	Layers:
	-	`sha256:4c0cff3f8efe82b99b2234d4bdb84451c30d3b75394cd2220c3af9e9e74290b0`  
		Last Modified: Mon, 06 Oct 2025 23:11:35 GMT  
		Size: 4.9 MB (4870464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72a520d3698145916eff1a5846e763c2a8b179dda62cf5e9feb439b60add99c`  
		Last Modified: Mon, 06 Oct 2025 23:11:36 GMT  
		Size: 41.0 KB (40963 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:b4980e99d764c7adceeb4df0b9ecd77e89831fc70a640c6128c07187fc72f01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.1 MB (451093509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b92203a800cdef0d7fb0bd88c4d59b044d062ded5e942ac2d16425861f771`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 13:08:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.build-date=2025-10-03T16:17:52.399Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2ceb68bd03a3cc20c26495ec986ed4f244589d69 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.5 org.opencontainers.image.created=2025-10-03T16:17:52.399Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2ceb68bd03a3cc20c26495ec986ed4f244589d69 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.5
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 13:08:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfe7fd4ae52359a4531e099609aad86ca9e85ddc01cbf9c67184aecf5da97da`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 11.7 MB (11661853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b147355a54b16a677937365d1dbeda39b5ab737591883fffa9d72c0c1ee87`  
		Last Modified: Mon, 06 Oct 2025 21:01:47 GMT  
		Size: 393.9 MB (393930249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e5f9678f74ced7e6ab7e157f7387a45fdf16aaae91c4645dda833894f2a7d8`  
		Last Modified: Mon, 06 Oct 2025 20:45:03 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2355d22cc93688579bdff890d265795f8e71a355294840f8d74412a6c0ce4e91`  
		Last Modified: Mon, 06 Oct 2025 20:45:07 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0c1aa223e7c9ccd8a63ece4686eeb0779a3ebe0eaf224094044995edb8310`  
		Last Modified: Mon, 06 Oct 2025 20:45:03 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67c069d05c6fd8d67be1b494fdb13c66ff32adfdbe111380b70e1e2fae9f5a3`  
		Last Modified: Mon, 06 Oct 2025 20:45:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940a9ee430da3b73d15194017e8f5bfee5ac630a1d579228a49ef8c0a8e47e8`  
		Last Modified: Mon, 06 Oct 2025 20:45:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09a7bf62f25074f8568136bd01b70ef92a2893961f88c778cc04696cbdf5bf0`  
		Last Modified: Mon, 06 Oct 2025 20:45:03 GMT  
		Size: 4.8 KB (4811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1bdbfc406d92a2af74af57bc5dd491f011f1e81c9b9671fa9d37595b153290`  
		Last Modified: Mon, 06 Oct 2025 20:45:03 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c62ddec2468bebb2b2b4aee0cb7183ba7259f376c54afd89df013a5d0eb42a`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 158.0 KB (157998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f173c3e61b530d0ff431801d2c7ca5fcf4177fd766cdf03d5de999de0a6da671`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.5` - unknown; unknown

```console
$ docker pull kibana@sha256:9b7e25f0540254ba7cd68a286bfe234287afb26ae6e905f3682357e99a018fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4912739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a331236e381ea4c585e673a1bddfd85970e8ea0adc5936c3a421162eb5346d51`

```dockerfile
```

-	Layers:
	-	`sha256:da159824ac1d5a6c35f0efa42f8364b705180bb09c7a0d3c8c16911e5e4e2823`  
		Last Modified: Mon, 06 Oct 2025 23:11:40 GMT  
		Size: 4.9 MB (4871528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8d67b98c80a54a556a9b2676126445d8d33d116e1a72b8771d81625e57453c`  
		Last Modified: Mon, 06 Oct 2025 23:11:41 GMT  
		Size: 41.2 KB (41211 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.8`

```console
$ docker pull kibana@sha256:bdede99bf0bdf6bc479853e240267407114c8d6df0d896b7436b28ff22ec99e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.8` - linux; amd64

```console
$ docker pull kibana@sha256:22886ec0684a416d254de39e38efccf7cc1ebae5a160ad7cf77e78b1181fcb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 MB (438675980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43aa288a1f678d6c1603944c8cb8fc76b13a9e909d51c53ee43eb1ba23441869`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 11:09:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-10-02T20:34:56.884Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=16276053a4c29c654785bb35bce6b512c15435b1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-10-02T20:34:56.884Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=16276053a4c29c654785bb35bce6b512c15435b1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 06 Oct 2025 11:09:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75e84f04f894b1fb2d3ef516685957b5ebc6a128ea3d9576a63178ccd45c57`  
		Last Modified: Mon, 06 Oct 2025 20:45:23 GMT  
		Size: 19.5 MB (19530233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ad91a1f0856d9bd8a2f26379d808365eac1b4b52e58b7818c660cc8006d7c0`  
		Last Modified: Mon, 06 Oct 2025 23:17:45 GMT  
		Size: 362.9 MB (362938759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd75f1238ae60161925e3a502dfaef8eaf03e6e0984fb3110a7b82ca4f206c8e`  
		Last Modified: Mon, 06 Oct 2025 20:45:22 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dfddc13aa21b49c539e7e30f04f6f34867a12113e6948f7ade4a7efa024341`  
		Last Modified: Mon, 06 Oct 2025 20:45:31 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54158db2a58382ba54dd754ff2c99c38fa8ef6b4ac76134ee3179e8ce5897dc0`  
		Last Modified: Mon, 06 Oct 2025 20:45:22 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4338866cf344d98a1759933588330330ee31c60e95745262daedc2ef595e2`  
		Last Modified: Mon, 06 Oct 2025 20:45:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0158fe9ef44a9638e104242bbbe8a898c84ea60a9fa796df17764ee2fcd7dfb`  
		Last Modified: Mon, 06 Oct 2025 20:45:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312ec1cea8bfff9751a06944d7bf7a88dac35a6bea58cc83dce75412db2dd398`  
		Last Modified: Mon, 06 Oct 2025 20:45:22 GMT  
		Size: 4.7 KB (4692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee26aa7f1d2729bbd34ceb16b5b59416fb71fa4fc92ffa63d847860298811d8f`  
		Last Modified: Mon, 06 Oct 2025 20:45:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3015a91cc6e924c33ec10e4a350a6a0e2e728cf783e0955db183171a89b09d`  
		Last Modified: Mon, 06 Oct 2025 20:45:22 GMT  
		Size: 75.1 KB (75097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee203fb39ce85cda4c22120da9a1c4cdb198e4223d3069680322048545acd70`  
		Last Modified: Mon, 06 Oct 2025 20:45:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678de55328f2a6249bf4aa0aacc40db7645b93a058cb76cc1d3ba0d9160325a6`  
		Last Modified: Mon, 06 Oct 2025 20:45:29 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.8` - unknown; unknown

```console
$ docker pull kibana@sha256:13cd21c3a5146f50db523d35d7ebf7bfd1dc38e433d44a777ae317389b99156c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5609776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d4049bb81efa213d30ddbc43764c2c3a73aed4cdacc7834ab1ab78e43f02e2`

```dockerfile
```

-	Layers:
	-	`sha256:f2a1a30192b0bc031dcf32adbd956cb67b00e1b3e9663b3d864de04281070177`  
		Last Modified: Mon, 06 Oct 2025 23:11:45 GMT  
		Size: 5.6 MB (5566591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485ddb813c38e0e7a77905121d3d3d3adc76808378a487700f659864668e2b25`  
		Last Modified: Mon, 06 Oct 2025 23:11:46 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:36baf10ecbd1d65b9710cc3f5574941efe4ad3fa007c1939f11e2779c4079f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.0 MB (450029055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0f1659d20718d739ae4d51961000908afbc6e862b29cb0243560b3321fcf5d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:39:52 GMT
ENV container oci
# Thu, 18 Sep 2025 08:39:53 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:39:53 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:39:53 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:39:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 11:09:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-10-02T20:34:56.884Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=16276053a4c29c654785bb35bce6b512c15435b1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-10-02T20:34:56.884Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=16276053a4c29c654785bb35bce6b512c15435b1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 06 Oct 2025 11:09:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c13ab99f36d9c8e889d871705abdb00049b76de0086040408501dd9d7bc152`  
		Last Modified: Mon, 06 Oct 2025 20:44:06 GMT  
		Size: 19.5 MB (19487802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2756b0f4c055c6d97a5dafa2e2814881f56060b52cdbec5b4128be2fe5ef5e78`  
		Last Modified: Mon, 06 Oct 2025 23:17:35 GMT  
		Size: 376.1 MB (376083900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8c37b71e0822b7ade649a69e78c7d66d97fd2d54516fc14875d7aa551da63`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8168d8d883d69069d0d1d195965291149b53603ba9032254f81378fe71e5102`  
		Last Modified: Mon, 06 Oct 2025 20:44:08 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580f08b9e23efa0d0d284245b1cb80fa352dfbc5b4da5b7daef38f395dab6645`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f7ab72a26e96149356215236c256481996bd49a188d450d072837b3b0fbae`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4524c9b7db5aab9a7d2640dd3392d4a9cba30f610ef138500a77cfbe53c1109a`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9831042438d481f3af2e62c7cddb44013f0a42d185c360426aedb90b1331609`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 4.7 KB (4690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d85b67076c268f7bb6711c3cf7685d271aa120b8bb4d07c8a136ab930ce269`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9914ce9357a514737b34a961dd466c530dc4da3817008b7c4e432f904818856`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 74.0 KB (73987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce166cd76d8b45dd0377483c8741476875a5196f568483b3fb16086f5526edc`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb445d1ccd029a27e67dd1c9a461b0ee5f46b81dcc45645019d944155afb92a3`  
		Last Modified: Mon, 06 Oct 2025 20:44:04 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.8` - unknown; unknown

```console
$ docker pull kibana@sha256:813a81141b1936c7705b80553edf1c6b35353cb6f132e52c417f606662b8d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844cb0ee619f8a2b8265ab33b9b5cf68af71a625c1d502e99a527429f530a3c8`

```dockerfile
```

-	Layers:
	-	`sha256:75220359ed9dbef74de6aefdc0e75c3754b25f780994c19a8812f2f3bd41d2fb`  
		Last Modified: Mon, 06 Oct 2025 23:11:51 GMT  
		Size: 5.6 MB (5565269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c503b3eecca9db188a086c1c592817ebd2c8f7cb9ed1132843cd8214e68704`  
		Last Modified: Mon, 06 Oct 2025 23:11:52 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.5`

```console
$ docker pull kibana@sha256:e32e8eff990e8485ab63b621dc2a71fe08688e5b92fca67b3a0ab3bc425ace85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.5` - linux; amd64

```console
$ docker pull kibana@sha256:cf3f2fbc9b05e8f9e6cf4bc891b8a8c1b38bcc9fffab5c95bb65096debadc228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (437999460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020cb244075ab80c6ea4173c2cced7e49689a730a0fc7abf7b5357c9cc068f74`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 11:10:10 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-10-02T12:43:32.321Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4a62c99c68a5156b84e1bf986d47e0a317591820 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-10-02T12:43:32.321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4a62c99c68a5156b84e1bf986d47e0a317591820 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 06 Oct 2025 11:10:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd55408cece5d6abe1f54a39f42c62647a48dca9adb4f4171c3df05afe00243`  
		Last Modified: Mon, 06 Oct 2025 20:59:29 GMT  
		Size: 19.5 MB (19530343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a1ebcf21a728bec2e8bfac19b44bf53f24db694c3420f05a56db0c7ce52f52`  
		Last Modified: Mon, 06 Oct 2025 21:00:35 GMT  
		Size: 362.3 MB (362262094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0427a11ef07145bb04ad45d1d6b5692f6dc4e30c4b789f8c457488c1fc6bd5a5`  
		Last Modified: Mon, 06 Oct 2025 20:59:23 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe287e4461f9a391fe20fb0fa3e2f6b068c6a22bdbb8679d31a64817c51280d`  
		Last Modified: Mon, 06 Oct 2025 20:59:27 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a9e4f1e940fabde907062ad98d6ec2e4e72f50217ffed23d8ae2d2b064f9e`  
		Last Modified: Mon, 06 Oct 2025 20:59:25 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e3c890efae0426513956d4d4e1b85724457ef563664cff84accf386dfa1b53`  
		Last Modified: Mon, 06 Oct 2025 20:59:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b79450bff058414f8488a5651b34a6a096dd3094a156bd8dbbbdee91ac2331`  
		Last Modified: Mon, 06 Oct 2025 20:59:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c16a385844ab207bbbcc3b05a5cf8986353394a8bd227b125ac48e2278f50d`  
		Last Modified: Mon, 06 Oct 2025 20:59:23 GMT  
		Size: 4.7 KB (4729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0af5d566584ab8a322c3e532f79a8d188d3aae9442a00094034275dcd57e25`  
		Last Modified: Mon, 06 Oct 2025 20:59:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88d37394ebd5dcd64fb6b6781f89018a47d93c34ef6f2d19d3069bad27811e3`  
		Last Modified: Mon, 06 Oct 2025 20:59:25 GMT  
		Size: 75.1 KB (75098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba817e3e40bd927c70cbd31e3fec314c9f12216a16ca616d8d085b7940b22a40`  
		Last Modified: Mon, 06 Oct 2025 20:59:23 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f63bec1934bc2bdcfb2d75f7b5d1dead78382203ab0e5c372ddacb0d0d0d7c1`  
		Last Modified: Mon, 06 Oct 2025 20:59:24 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.5` - unknown; unknown

```console
$ docker pull kibana@sha256:a3bc50ed5ebfd333807ed637b2759dc01a52386712eb8ddfbcb2988580abf882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5734458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210fbd39cf899c8ebd7ab630c708abe09b647d4a5151fe967ab79124f6fb8a77`

```dockerfile
```

-	Layers:
	-	`sha256:ee41aef00b6190875f573c2ec4f2762740b988273296ad49e488a02d3632290b`  
		Last Modified: Mon, 06 Oct 2025 23:11:56 GMT  
		Size: 5.7 MB (5691274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7fb3fd70a645e4b5a287d4fcd2acaeba62add1d7bdabbe104505fc49d072efb`  
		Last Modified: Mon, 06 Oct 2025 23:11:57 GMT  
		Size: 43.2 KB (43184 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:2e6b3f367ccb3294f11658c00cc7d02ad33e933430e417314ea2e4eb0185158f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449072581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b672ab1b4c60bcba29c3628c9649e0b1aaf23ce5dc1900a4b19fe6a909a15849`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:39:52 GMT
ENV container oci
# Thu, 18 Sep 2025 08:39:53 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:39:53 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:39:53 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:39:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 11:10:10 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-10-02T12:43:32.321Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4a62c99c68a5156b84e1bf986d47e0a317591820 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-10-02T12:43:32.321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4a62c99c68a5156b84e1bf986d47e0a317591820 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 06 Oct 2025 11:10:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b202ebec67b074b8baf5e3dbd1a5f2280b11b1427a06a5bb98f784f73e5dc8b8`  
		Last Modified: Mon, 06 Oct 2025 20:45:07 GMT  
		Size: 19.5 MB (19487819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b20ba997d81dae6e07809acc003f23e1dfbc426c49401500650d0665acf0f8`  
		Last Modified: Mon, 06 Oct 2025 23:18:05 GMT  
		Size: 375.1 MB (375127364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275e44b33d305dff47c93b1e40075db1937c69a10ccaf981dcaa9d89dc5647cd`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec52ae2ee08341bcad2505f8aaf8a0fb43867405e5940cd6eb290a8bbcb8be`  
		Last Modified: Mon, 06 Oct 2025 20:45:05 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d566459d3f4b17a7819a7a5aa9764f308510d04fcc190e25e56e4b826789a3`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 5.2 KB (5230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e080ace07c09ec554c8376106247678eb97cdb7c3f31787ad281245ddabe507`  
		Last Modified: Mon, 06 Oct 2025 20:45:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b28cf0a1dbdcd576c36b2400cd58cfd1700acb63400a6a1b6099cded5de7d7`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30fdc5964c7e7e87100bec74ada69001e009997e2c515d9f66dedee80003c82`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 4.7 KB (4730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a47ae3f5d28e335c35907d69cc164e2aa4fdbbbbdc3b01f993925b108ad741`  
		Last Modified: Mon, 06 Oct 2025 20:45:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99aacc3ad49dcf1f6abf2b516de9ca5778ed747bff502e6dedc4133fee096a2`  
		Last Modified: Mon, 06 Oct 2025 20:45:03 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a258a188719e1174e93068031fec8ed9baaf87e1467539ac35d6b3a558e279a`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe6c5fbfa1763832e5b8c482fd81b10fd4c1fce888a5ea8ddb62e0648a363f0`  
		Last Modified: Mon, 06 Oct 2025 20:45:04 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.5` - unknown; unknown

```console
$ docker pull kibana@sha256:de26ce0bebcf1de9d8db5dc1502e26de3a286808c4ff561518b2ea1112e0e889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5733394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354d50635b02c140b96917c8ddd6f2406a10af6cdf96def7d35bb9f9e4d5e0cb`

```dockerfile
```

-	Layers:
	-	`sha256:c90954a6072edabc1efdb571a509fff52ab0a9699f3c5b2896f6937e94691df9`  
		Last Modified: Mon, 06 Oct 2025 23:12:02 GMT  
		Size: 5.7 MB (5689952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147b9dbcacc96ab805660745f45dcea53b9b6dd3738fe077ac073a2a359d7420`  
		Last Modified: Mon, 06 Oct 2025 23:12:03 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
