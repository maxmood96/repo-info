<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.18`](#kibana71718)
-	[`kibana:8.12.2`](#kibana8122)

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

## `kibana:8.12.2`

```console
$ docker pull kibana@sha256:a746e254aea8caa92f2251fd9952afe8a15c862615ede927b4299eb12a6de871
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.12.2` - linux; amd64

```console
$ docker pull kibana@sha256:8b6493562a356d48394d51d1827024ff74977e60984141dc15451e635f488ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.6 MB (372571409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c54e388d794b9c87faca7ee7a689be673650a59d905d1461da7ac3cf821e04`
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
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be737d3d8074355b5290a825ba52e497a60dd3e4cddb00e91a29e9781f509ce`  
		Last Modified: Thu, 22 Feb 2024 23:52:01 GMT  
		Size: 11.3 MB (11310860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b6e9da82d3263838b74bee0a705a57e19d944aa75f6144a2ed7e83dec8772`  
		Last Modified: Thu, 22 Feb 2024 23:52:00 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ca03023f795f42eb45c71f2208082caed93071b11d385b52787bdcd250ce74`  
		Last Modified: Thu, 22 Feb 2024 23:52:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2637148f3c747113def4c8db133b173293e855e0b474f35d9ee2f4d97f63b724`  
		Last Modified: Thu, 22 Feb 2024 23:52:01 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0ceea5e4ee58e2e4f1a0a29a04b3dd2ffe4dbb5de8c8d36eb23204ab4abcab`  
		Last Modified: Thu, 22 Feb 2024 23:52:01 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eadf683fd705fc2c2878d3d8fa62b64bf0d39a63e5dfdad966a643d306b7a0`  
		Last Modified: Thu, 22 Feb 2024 23:52:06 GMT  
		Size: 317.1 MB (317073390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a4477c002c17b1687e2fee3369ad5e8ad502ceaf63d015f1a483e406da3cab`  
		Last Modified: Thu, 22 Feb 2024 23:52:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6e2f1f7a5d9d0ca7acbe6f9a4d5d13682da377994cf7123e0023e91dd6276e`  
		Last Modified: Thu, 22 Feb 2024 23:52:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3f8a812ef6edcaa078a2aae195263aac7d27ed1931f39e475dcf9d1cac7164`  
		Last Modified: Thu, 22 Feb 2024 23:52:02 GMT  
		Size: 4.5 KB (4550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273b822ec9ac48c018a07cfdfce44385695767576744015e7562214f3d136a11`  
		Last Modified: Thu, 22 Feb 2024 23:52:03 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8847023af93bc08f403cb1045f4787477ae29c699606a522d337e11efc9ad33d`  
		Last Modified: Thu, 22 Feb 2024 23:52:03 GMT  
		Size: 189.4 KB (189431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08412936eaa2c1bd5a712398f5343f38a3827643af2758cebbd7fdf7e10b4879`  
		Last Modified: Thu, 22 Feb 2024 23:52:03 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.2` - unknown; unknown

```console
$ docker pull kibana@sha256:39e087fc5ff539aa46fa4b6f03eacc5f9bf155b1875f5253077688a4705a469b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d31455c2bd134845dc970fb61c9fd38520e2e4f887e9f60279b1ffe398a7a4`

```dockerfile
```

-	Layers:
	-	`sha256:c7509ce0e0969c02b4b369399863057fd611a516d4bd3683697f39e377c7458c`  
		Last Modified: Thu, 22 Feb 2024 23:52:01 GMT  
		Size: 2.1 MB (2125193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:442caa061d029ccb9071f73167d048143139e8d573fb4217ca78ae84b2c6f1dc`  
		Last Modified: Thu, 22 Feb 2024 23:52:00 GMT  
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
