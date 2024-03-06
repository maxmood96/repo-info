<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.18`](#kibana71718)
-	[`kibana:8.12.2`](#kibana8122)

## `kibana:7.17.18`

```console
$ docker pull kibana@sha256:69a0c09eb1a0c08d6c999c2b0026fca1368429df78fc9c78a8190225862d0cb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.18` - linux; amd64

```console
$ docker pull kibana@sha256:37c195ea6bf71dd13b8a5f6f3f357013609a8db8662c5957ec8272a80ba622cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358403696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117cbfb16aaa22dab5fac8b444f0767fa24cd77c29a58e75c330599debe34b89`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 06 Feb 2024 11:29:54 GMT
ARG RELEASE
# Tue, 06 Feb 2024 11:29:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 06 Feb 2024 11:29:54 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN fc-cache -v # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/kibana
# Tue, 06 Feb 2024 11:29:54 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.build-date=2024-02-01T12:06:00.919Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d9651872f4b223d9f91a873f1d6a9fb7d1fe4f64 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.18 org.opencontainers.image.created=2024-02-01T12:06:00.919Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d9651872f4b223d9f91a873f1d6a9fb7d1fe4f64 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.18
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 Feb 2024 11:29:54 GMT
USER kibana
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274275be56c8620838ffc8f35002c13bdfee9b48b932c90eb06e5fdf659cb340`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 10.5 MB (10533200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14492576505b4e19d13ab7a72609656b8ba747ef6a304e52f39a55985df2404b`  
		Last Modified: Wed, 06 Mar 2024 02:57:31 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52bbd06d19570b0afedd97625f5f674450862a7a101f2ce85764a6588ea291f`  
		Last Modified: Wed, 06 Mar 2024 02:57:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5e8f83515f25eb9f27eafed771ea9e9aa9f4603e43ec1621059a8b699d4000`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53a86481ab48769096eb90a115d8051db116d5597732b050b05631fa559db3`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0dfffbb884bf3f894d24661a0f4ebd57607a35530dda6440f844fa89e732d`  
		Last Modified: Wed, 06 Mar 2024 02:57:39 GMT  
		Size: 303.7 MB (303683987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11da4c54b9c23585cff2562a8544c81565b9fa5ea61e21615f5a42686f2045ad`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8dd7e28c6424bfee88ac80c5a6e49a65bc2de143b6c2a8ad53bb11729e925`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5c83abeca39dab1de1b9e0c4a01ade92f74792b0bc5cbfb6ba439689a5e4da`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ad99e14e5c9f1214071dfe43cada7082412f3abb52a00bda2cf1c4cddb68fd`  
		Last Modified: Wed, 06 Mar 2024 02:57:34 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba2986f5116e2926b4873f41f60eeb67e6cdaf811c877fb58c9d5dbf34e30fc`  
		Last Modified: Wed, 06 Mar 2024 02:57:34 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a8e7c16fa4f9a0bb8ce333629abafe49d33640aa6ee440719608c22fe530d0`  
		Last Modified: Wed, 06 Mar 2024 02:57:34 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.18` - unknown; unknown

```console
$ docker pull kibana@sha256:8f9292ad2f11d582048779a9647278b1edf7bac89243fd007b548d472a2831c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2219584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1271ff77574d43c92544e61ba1eeed1a6ee7c4e9a303e83f969a660a73c734d0`

```dockerfile
```

-	Layers:
	-	`sha256:63bc80312c4f530f38b19defd5c410f4d1810ec2d7ce7ceb682a60858add43b2`  
		Last Modified: Wed, 06 Mar 2024 02:57:31 GMT  
		Size: 2.2 MB (2175222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad2d181cb1a0fcba0922aa44cf3ec6ed46f42bd5786ccafa75d0b5117b978816`  
		Last Modified: Wed, 06 Mar 2024 02:57:31 GMT  
		Size: 44.4 KB (44362 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.18` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:3657ee55ec3fa51f5ce73317e714261ba5262528c1336b9edaa44e0ca9b7fb3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368865395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99a3bca3558ace02c1705ad934cb5d461aa735a802e5419892abdb8e44830df`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN fc-cache -v # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/kibana
# Tue, 06 Feb 2024 11:29:54 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.build-date=2024-02-01T12:06:00.919Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d9651872f4b223d9f91a873f1d6a9fb7d1fe4f64 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.18 org.opencontainers.image.created=2024-02-01T12:06:00.919Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d9651872f4b223d9f91a873f1d6a9fb7d1fe4f64 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.18
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 Feb 2024 11:29:54 GMT
USER kibana
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac834397a55fbd1e7ee31062f71885fec78a6d8986d885ce9aafe77aa2b86b76`  
		Last Modified: Sat, 03 Feb 2024 07:04:22 GMT  
		Size: 10.4 MB (10397217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d71c32333a58df49ca2f3070aea31b05a310d9bcdccc7d703a42f424891fea`  
		Last Modified: Sat, 03 Feb 2024 07:04:21 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966c6f3e77e8669aaea15bf91ca1580945554ed2552803d0da74bafab098bdfb`  
		Last Modified: Sat, 03 Feb 2024 07:04:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc3b481754752b546302f2eb1da65441d7ba1937c537ca5526b7345fcf37f3c`  
		Last Modified: Sat, 03 Feb 2024 07:04:22 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673f9ece3235dd4fccaca8e65297e9dab8177d92966fe81e3e199694e61bb84c`  
		Last Modified: Sat, 03 Feb 2024 07:04:22 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6eba6beeabd2e57cbe341852d397da265cd87c2f0890754477e77f99bac29d`  
		Last Modified: Tue, 06 Feb 2024 22:44:41 GMT  
		Size: 315.8 MB (315826848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87de4b3cbb8b82f6d81589411792483a78da481df085fa014cbd578f0f301bf`  
		Last Modified: Tue, 06 Feb 2024 22:44:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52e3c3049aec7ee1950bc8dd4f18e874702f98a26bdfbe29317b3b849df6952`  
		Last Modified: Tue, 06 Feb 2024 22:44:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af08d089d364fc2c133d227e64b471c89679f4fe696eb29eaa00ac62bdce57d`  
		Last Modified: Tue, 06 Feb 2024 22:44:34 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351fb9fc2ad11baabfb2ddb3a3c15e4e2e1fe96439d68251e5a4bd7961db86b4`  
		Last Modified: Tue, 06 Feb 2024 22:44:35 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2afa35c464a5560a85c04c4e6a52440c4be8a2b40c8adb54f38b960331a24`  
		Last Modified: Sat, 03 Feb 2024 07:04:25 GMT  
		Size: 183.4 KB (183408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687880f1f72aeadd0f3250dcdc7b241f0afb4f0a218e413de9d74efad3b2d0b`  
		Last Modified: Tue, 06 Feb 2024 22:44:35 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.18` - unknown; unknown

```console
$ docker pull kibana@sha256:d1aa315997847ec8d73078ed231e77afa8ce0ebc6ae0a1fce206e333f30e85b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1972471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355a83332bb60e3290de631ae265758061c3b4119d0e2d15f3b968e3537bc91e`

```dockerfile
```

-	Layers:
	-	`sha256:35b49c0189705df5016f075aaa6f6864167893efa6bea670eb6988c27c5b5cb0`  
		Last Modified: Tue, 06 Feb 2024 22:44:34 GMT  
		Size: 1.9 MB (1928265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6897c58d29e7c3e118464af63dde449946390a279084960075ab4f453b06c448`  
		Last Modified: Tue, 06 Feb 2024 22:44:34 GMT  
		Size: 44.2 KB (44206 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.12.2`

```console
$ docker pull kibana@sha256:b3567be8d1fe1577c011b93284642629b1852669bee4ad70fa88629128ae3fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.12.2` - linux; amd64

```console
$ docker pull kibana@sha256:194055ed8cff37a234e7c891bed680e2cc3f4c38308b80c8e389a7c40374f213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371793100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c285823994c439ed9cffd5cb8e161f11a0b3628c2915cac805b6a782012ecc6e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN fc-cache -v # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/kibana
# Thu, 22 Feb 2024 12:50:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.build-date=2024-02-19T12:06:34.117Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f5bd489c5ff9c676c4f861c42da6ea99ae350832 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.12.2 org.opencontainers.image.created=2024-02-19T12:06:34.117Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f5bd489c5ff9c676c4f861c42da6ea99ae350832 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.2
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 22 Feb 2024 12:50:52 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c7eae5a29ce15f2dc1d74b8172f5d8b51a329d5837016b7e33d67465ac8b2`  
		Last Modified: Wed, 06 Mar 2024 02:58:31 GMT  
		Size: 10.5 MB (10533211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd5e461cf45f4052bb78993954e3ffa0615d06f3871cd013d1ae93fbcf91f6`  
		Last Modified: Wed, 06 Mar 2024 02:58:30 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32642d83a7f026522a571a23db6dee76507ef5b8b2ba6a561548d1ad5eaf74d3`  
		Last Modified: Wed, 06 Mar 2024 02:58:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a757158a78d5d6110a7d33e6edf54bc06d3e7704f3205e837fca005151f7a8e`  
		Last Modified: Wed, 06 Mar 2024 02:58:31 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f8381864cde88e6c24be7bd5c015f3348134375e00ee0d180dc896baa46570`  
		Last Modified: Wed, 06 Mar 2024 02:58:32 GMT  
		Size: 5.3 KB (5283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5055cdf698bdec9973c8da23394afcc22766e5d6c469ba11cddf313b68155456`  
		Last Modified: Wed, 06 Mar 2024 02:58:36 GMT  
		Size: 317.1 MB (317073359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae08c5d62807acd6aaa9bd2aa8d2581fac76e2653393a6048fec4124b894c475`  
		Last Modified: Wed, 06 Mar 2024 02:58:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cb1d5240ca6610a657735c9ccd231e68edda7a4f56b997d757481fc873d7c4`  
		Last Modified: Wed, 06 Mar 2024 02:58:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d846c032bc276eccbba2e51417ef1d386d005f55dd27faf22f3244ae011912`  
		Last Modified: Wed, 06 Mar 2024 02:58:32 GMT  
		Size: 4.6 KB (4554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b974acb2af001cb9eee3945d861adfdadb88075a8f1ecf95816508b7926a271e`  
		Last Modified: Wed, 06 Mar 2024 02:58:33 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0181b4b719198ecdf49ab84c4021004de1c1fc1d2aeed90514964e772219f`  
		Last Modified: Wed, 06 Mar 2024 02:58:33 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321933bedb4c1ab5b4c8612f2b66307e600665aa36423760a0ba69e71961254`  
		Last Modified: Wed, 06 Mar 2024 02:58:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.2` - unknown; unknown

```console
$ docker pull kibana@sha256:b0783cc4ce78f3ba4119e54209fee4412d76bc07bc182bca7addd662a061bc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c7aaec3c84685bd7d2eda6157e9e6110a66a8056266ad111e4098f575131ca`

```dockerfile
```

-	Layers:
	-	`sha256:a35d0e031a0e6a61b2e9a64972ef70e381986e3e12273fe3e01bf6041fda14e4`  
		Last Modified: Wed, 06 Mar 2024 02:58:31 GMT  
		Size: 2.1 MB (2125193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d01565e43d84d7488eaffa169fbdb7bab2ca0b0d0656254c6a228ee37cd73d`  
		Last Modified: Wed, 06 Mar 2024 02:58:30 GMT  
		Size: 44.4 KB (44352 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.12.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:0568a4af5c37aaf22186a081a7779125e3948c894b786c8d2a28198e07dffaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382249656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde07164e826703ed82f5c458e72dea8b57b1d3a76d0222488c4b83bf04a602a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN fc-cache -v # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/kibana
# Thu, 22 Feb 2024 12:50:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.build-date=2024-02-19T12:06:34.117Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f5bd489c5ff9c676c4f861c42da6ea99ae350832 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.12.2 org.opencontainers.image.created=2024-02-19T12:06:34.117Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f5bd489c5ff9c676c4f861c42da6ea99ae350832 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.2
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 22 Feb 2024 12:50:52 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac834397a55fbd1e7ee31062f71885fec78a6d8986d885ce9aafe77aa2b86b76`  
		Last Modified: Sat, 03 Feb 2024 07:04:22 GMT  
		Size: 10.4 MB (10397217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d71c32333a58df49ca2f3070aea31b05a310d9bcdccc7d703a42f424891fea`  
		Last Modified: Sat, 03 Feb 2024 07:04:21 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966c6f3e77e8669aaea15bf91ca1580945554ed2552803d0da74bafab098bdfb`  
		Last Modified: Sat, 03 Feb 2024 07:04:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc3b481754752b546302f2eb1da65441d7ba1937c537ca5526b7345fcf37f3c`  
		Last Modified: Sat, 03 Feb 2024 07:04:22 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673f9ece3235dd4fccaca8e65297e9dab8177d92966fe81e3e199694e61bb84c`  
		Last Modified: Sat, 03 Feb 2024 07:04:22 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f664b12024303b476b2540dbf717de6de6d7e282a733ef2e571a6b94c831b6`  
		Last Modified: Thu, 22 Feb 2024 23:57:47 GMT  
		Size: 329.2 MB (329211067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39363755e456ded04af460ffd0721e6a07c749c84046fedabfbc73709668f0c2`  
		Last Modified: Thu, 22 Feb 2024 23:57:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703928321e8123e90f2526001f96d2b16915a654188673e378291943ac9fddf4`  
		Last Modified: Thu, 22 Feb 2024 23:57:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3678c2bf5fc47d119b9e49184aaec73d6249e46a593a81a4781d2c35d6a874f`  
		Last Modified: Thu, 22 Feb 2024 23:57:41 GMT  
		Size: 4.6 KB (4552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc62a03be81af1ac0769c012c197b3b084a3a96414da106ed003782e3f0a52c`  
		Last Modified: Thu, 22 Feb 2024 23:57:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2afa35c464a5560a85c04c4e6a52440c4be8a2b40c8adb54f38b960331a24`  
		Last Modified: Sat, 03 Feb 2024 07:04:25 GMT  
		Size: 183.4 KB (183408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d824a2363e66165fa851dd19ab1c81dfa33edaea0b39305891fd5ff21cb93c7`  
		Last Modified: Thu, 22 Feb 2024 23:57:42 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.2` - unknown; unknown

```console
$ docker pull kibana@sha256:b70eb698516d6c81a69018ee09e9a9352c28694092e47126a432ccb2a6a4d467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c77a70364d30f3602704fbd01f982aabd6acc98d9f56dc1e3e59aef6e3dfaf`

```dockerfile
```

-	Layers:
	-	`sha256:5c2b507069c8a226213dacc03a6cc4779841ef5029a8aed1e376bc9bca344613`  
		Last Modified: Thu, 22 Feb 2024 23:57:41 GMT  
		Size: 2.1 MB (2125428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ed1c9019d93a152a883d30d9ad381938840f65421b595263d0abf28fac22be`  
		Last Modified: Thu, 22 Feb 2024 23:57:40 GMT  
		Size: 44.4 KB (44353 bytes)  
		MIME: application/vnd.in-toto+json
