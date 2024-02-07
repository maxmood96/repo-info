<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.18`](#kibana71718)
-	[`kibana:8.12.1`](#kibana8121)

## `kibana:7.17.18`

```console
$ docker pull kibana@sha256:2cb9bca0209e4698ad7cf3105afc4481e5df3660314076399f85fffd11d47c4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.18` - linux; amd64

```console
$ docker pull kibana@sha256:59311cf5391b8cf37b5de9cb1bd7844c6c8a91e0b178952cb3b7ba415caae2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358403467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcf539e7929eed1cbccc2660696b8516282f04ced2057147cf908e65e4294f7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
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
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ff406202b490f1628cb4b86012e08751a41d4b239d5ef08757242d5925c735`  
		Last Modified: Tue, 06 Feb 2024 20:53:31 GMT  
		Size: 10.5 MB (10532371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e5611dc9e0eb2d0c0b0d84cb212461c227f4d9b739acd8ebd3f9e0363755b2`  
		Last Modified: Tue, 06 Feb 2024 20:53:31 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eeb7afbebea4b46c5e9b5469cb392b87ef63180b3e60f0b2f2c35438763d4d`  
		Last Modified: Tue, 06 Feb 2024 20:53:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8cbde5bb5c60df63365d8f970dfe9b6037e90fcfdc7e9afec345102b524e6`  
		Last Modified: Tue, 06 Feb 2024 20:53:32 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be674cd0831e1de9fa32c18e3318941db6f1c18dc02323372726412f14cb8a7`  
		Last Modified: Tue, 06 Feb 2024 20:53:33 GMT  
		Size: 5.3 KB (5300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294cb3be6ff16a77bcfbefe2d59e00650df9c4617f4a26b492937736f2a67c5b`  
		Last Modified: Tue, 06 Feb 2024 20:53:36 GMT  
		Size: 303.7 MB (303683999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9235622ab8ad49d19bab169afd30ddba3ad86c80442d6bf96d34dadbf0bfeb7`  
		Last Modified: Tue, 06 Feb 2024 20:53:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab658c84422b71cff59fba11ef4976b70a7ecabfc1800ecdf79f481f8cfbf15b`  
		Last Modified: Tue, 06 Feb 2024 20:53:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cbb20cf4d535144511642702171b55bc12e6536b62641d6b1335e07a3e713e`  
		Last Modified: Tue, 06 Feb 2024 20:53:34 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874b91818d75cd3fba122a7fc70aebb3c5a156e80d55d24d81a1b880539f69c`  
		Last Modified: Tue, 06 Feb 2024 20:53:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac29bd8e48a6544cc53a5a43a5195baf7fd212c48b1107b7a9b4c5de29f3c53d`  
		Last Modified: Tue, 06 Feb 2024 20:53:34 GMT  
		Size: 189.4 KB (189406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b87cd0b2682590c367899585ecdcd0015d028626b8bcb0e634a93ccd30e712`  
		Last Modified: Tue, 06 Feb 2024 20:53:34 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.18` - unknown; unknown

```console
$ docker pull kibana@sha256:a9b690688094e939203de7a908b3789b3da4478ef746942662f026b09a6de37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1972287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a5a71bda414b2003f343bf26b0e91251d7537987e9b602ae605848701df4c3`

```dockerfile
```

-	Layers:
	-	`sha256:8a0961538bd2f3517f7c00dfd6ec82fdd7e720c00efa607369f644f08cf18eb6`  
		Last Modified: Tue, 06 Feb 2024 20:53:31 GMT  
		Size: 1.9 MB (1927924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b1c2e0f97ae91a047e46bd06d3156b572051d666902d22b6301a5218a298e1`  
		Last Modified: Tue, 06 Feb 2024 20:53:31 GMT  
		Size: 44.4 KB (44363 bytes)  
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

## `kibana:8.12.1`

```console
$ docker pull kibana@sha256:bf50b734ea418bf6dec1f100089db85e65a1bf87b84293bcbade76a62c522530
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.12.1` - linux; amd64

```console
$ docker pull kibana@sha256:a790d0e5267e9cdcbb8b20c1f4622c3eced3d5ca059403800c0fb650b8e7dd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.7 MB (371709889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f19f9f067f944d809e3c86bc7bedf90716a658a17dc38f315cdbc73ee7203de`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:33 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 Feb 2024 11:29:33 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN fc-cache -v # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
WORKDIR /usr/share/kibana
# Tue, 06 Feb 2024 11:29:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:33 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
LABEL org.label-schema.build-date=2024-02-01T13:05:51.943Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3457f326b763887d154c9da00bd4e489221a2ff3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.12.1 org.opencontainers.image.created=2024-02-01T13:05:51.943Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3457f326b763887d154c9da00bd4e489221a2ff3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.1
# Tue, 06 Feb 2024 11:29:33 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 Feb 2024 11:29:33 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 Feb 2024 11:29:33 GMT
USER 1000
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5748f988ceb6e0c090791dd7b2da2e82236f73a047b28680f8617790279af59`  
		Last Modified: Tue, 06 Feb 2024 20:54:34 GMT  
		Size: 10.5 MB (10532333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56effa5cfe467029809792296474ed97d68a5cd50a337f2747d29590c2e62ee4`  
		Last Modified: Tue, 06 Feb 2024 20:54:34 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235b27ba92eae3527e6ea60341acbcc8a7dc459211274eb24ccfb97485cd3cd`  
		Last Modified: Tue, 06 Feb 2024 20:54:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48eb7d6994047cda498e56a642bbd2b3d69e927e365449671ad461653db42a8`  
		Last Modified: Tue, 06 Feb 2024 20:54:34 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c908e0c32d85deb1a3ca8f11f08b02ed32422444a2b59112e2ad36e5b891917f`  
		Last Modified: Tue, 06 Feb 2024 20:54:35 GMT  
		Size: 5.3 KB (5292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f9f48309e857409bbfaa88979109ff71ca9808664d5f75801efbab8b0ebf5d`  
		Last Modified: Tue, 06 Feb 2024 20:54:40 GMT  
		Size: 317.0 MB (316990405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd20982d9fce76c493431a50bf4c99595176d9a10adfa3cb73ac918eb49f8117`  
		Last Modified: Tue, 06 Feb 2024 20:54:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164877131325ca288e8c06bf337cd7145fc02b774f0421ffe4fa2e2281e7dfff`  
		Last Modified: Tue, 06 Feb 2024 20:54:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9d8ae3cf34e9a0337264981189e9a729ea9dfb023b69f0aac1e68854bd5c9f`  
		Last Modified: Tue, 06 Feb 2024 20:54:35 GMT  
		Size: 4.6 KB (4554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857cef8a7e5d5c16b2c87a1d6e685a065123a19238b20bad3a788b11f7487139`  
		Last Modified: Tue, 06 Feb 2024 20:54:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a57a847bc3beebc32e647b66549a5b09a303d22497b1fb91cae2e6faeafb62`  
		Last Modified: Tue, 06 Feb 2024 20:54:37 GMT  
		Size: 189.4 KB (189406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090be46e9cf1d19cd7e97ddfd4562a0e7bde3700fda5ebba9c75599da8a42874`  
		Last Modified: Tue, 06 Feb 2024 20:54:36 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.1` - unknown; unknown

```console
$ docker pull kibana@sha256:86400a1c4d63027ac79a88231843102dace1d34921536c37f7d80c61ab61351d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1922247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f05103691c55ac9098a841e9e4fbfd8d1fe2d1c88ccf8f8e396f585d22494f`

```dockerfile
```

-	Layers:
	-	`sha256:12db04c1b3d3c9bc8f076ee8dc2c3dd30f3c30e4a9f56d9c7bd4a2bbf4dedf6b`  
		Last Modified: Tue, 06 Feb 2024 20:54:34 GMT  
		Size: 1.9 MB (1877895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f6932d5cbf0aa02954e3eb5d1b0b620b7fb300690dde7a414516711c59fd58`  
		Last Modified: Tue, 06 Feb 2024 20:54:34 GMT  
		Size: 44.4 KB (44352 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.12.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:f52e5dd93945e116addf101fecff15420212dc90824a3273b4f803e2f57ac070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382188630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724500de83998b17122c9f48b5ae718da53e6df48bd57373391d753a7aea5203`
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
# Tue, 06 Feb 2024 11:29:33 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 Feb 2024 11:29:33 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN fc-cache -v # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
WORKDIR /usr/share/kibana
# Tue, 06 Feb 2024 11:29:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:33 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 Feb 2024 11:29:33 GMT
LABEL org.label-schema.build-date=2024-02-01T13:05:51.943Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3457f326b763887d154c9da00bd4e489221a2ff3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.12.1 org.opencontainers.image.created=2024-02-01T13:05:51.943Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3457f326b763887d154c9da00bd4e489221a2ff3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.1
# Tue, 06 Feb 2024 11:29:33 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 Feb 2024 11:29:33 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 Feb 2024 11:29:33 GMT
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
	-	`sha256:536151a9f0e9908c56af90352e6e41d218ec7666ce22361f32f46b5e13ff6e72`  
		Last Modified: Tue, 06 Feb 2024 22:39:59 GMT  
		Size: 329.2 MB (329150033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9ecc07396166707ab3f3d5a482fc293717d713c312cde15bce45b92dabe42c`  
		Last Modified: Tue, 06 Feb 2024 22:39:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b852d459f21c3d093519b0183774337697a62d9d4d492e93a543628ef520725`  
		Last Modified: Tue, 06 Feb 2024 22:39:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fd97b367783bf386d766dfbf9d2069f443f13335c170526abefb017d40aea5`  
		Last Modified: Tue, 06 Feb 2024 22:39:51 GMT  
		Size: 4.6 KB (4553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1cb9eb781172f3340dfbdd503e2fd0b74fc0c73b05d7008600cc1eccc7ca8b`  
		Last Modified: Tue, 06 Feb 2024 22:39:52 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2afa35c464a5560a85c04c4e6a52440c4be8a2b40c8adb54f38b960331a24`  
		Last Modified: Sat, 03 Feb 2024 07:04:25 GMT  
		Size: 183.4 KB (183408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8648a826f235d9cf0799c166dff8b9db1f7c21bc56da6134a980c57afcb92d`  
		Last Modified: Tue, 06 Feb 2024 22:39:53 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.1` - unknown; unknown

```console
$ docker pull kibana@sha256:1b55203bf207d51af8b29d0f2da15243dbca8ea3d9e0ff8e31d29729dcf62ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1922592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b3f194b5e6155cdb6ba6c72bb0a2f9b2da13a98a52d0d7f96db2781a98d0cb`

```dockerfile
```

-	Layers:
	-	`sha256:57264e43264085e8d99fe90a6e0a3e568a1be5d58b672143342bec6f5b0dae53`  
		Last Modified: Tue, 06 Feb 2024 22:39:52 GMT  
		Size: 1.9 MB (1878236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2feca43bc1561006b38d9593d9c507b2c0cc3633972d79d82a90041087d420`  
		Last Modified: Tue, 06 Feb 2024 22:39:51 GMT  
		Size: 44.4 KB (44356 bytes)  
		MIME: application/vnd.in-toto+json
