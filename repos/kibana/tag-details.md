<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.17`](#kibana71717)
-	[`kibana:8.12.0`](#kibana8120)

## `kibana:7.17.17`

```console
$ docker pull kibana@sha256:cbe773a659521d3ae03e03a686c90a01282ba6194ae58ee469e42398e9b0dfb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.17` - linux; amd64

```console
$ docker pull kibana@sha256:2bce94f3641a3174a913c78e540c1dd6f3a9c7afd738337522b232c95f63809f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357945396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460d6808cf68470e1805318b2d99e8be04d3e0290c843b3cd52c8b316bcb4706`
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
# Tue, 23 Jan 2024 14:25:39 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 23 Jan 2024 14:25:39 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN fc-cache -v # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
WORKDIR /usr/share/kibana
# Tue, 23 Jan 2024 14:25:39 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jan 2024 14:25:39 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 14:25:39 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
LABEL org.label-schema.build-date=2024-01-18T12:06:03.434Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca09dff039c82e70b081f86f30b19515eb2968dc org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.17 org.opencontainers.image.created=2024-01-18T12:06:03.434Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca09dff039c82e70b081f86f30b19515eb2968dc org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.17
# Tue, 23 Jan 2024 14:25:39 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 23 Jan 2024 14:25:39 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 23 Jan 2024 14:25:39 GMT
USER kibana
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7533b93e9ae2595f498e9da2d06a23703d0d1eda18e15b630ddc6dfe44d4c693`  
		Last Modified: Fri, 02 Feb 2024 00:56:54 GMT  
		Size: 10.5 MB (10531960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d0b7f4bb6ab15d28340dcbf95a5f4d7093de1223aeb91c2959a64557f4ae7e`  
		Last Modified: Fri, 02 Feb 2024 00:56:54 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4bf31632bef55a3dd003198171486290927002c95b60054f22055e86afc2a`  
		Last Modified: Fri, 02 Feb 2024 00:56:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7bdae5ab3219608a03f7e6cba330feed9efa0bf5847b2ae3369cea15dc33a`  
		Last Modified: Fri, 02 Feb 2024 00:56:54 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9e948a30b2978dc1bbd80ff822399e397e377dac5c99570ca717782e8fdb58`  
		Last Modified: Fri, 02 Feb 2024 00:56:55 GMT  
		Size: 5.3 KB (5293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8579de3518a83b3be5022af70dc68f538c37dc818149164d29b59b4f904cc8e1`  
		Last Modified: Fri, 02 Feb 2024 00:57:00 GMT  
		Size: 303.2 MB (303226341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da10c3645497fdbd20323673d604b91a7981f1d34e8779c21c3143c2b2364fd5`  
		Last Modified: Fri, 02 Feb 2024 00:56:55 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaf9c04b723912d5ae3043f57f422598237a5a95306c8694a29d7512550d363`  
		Last Modified: Fri, 02 Feb 2024 00:56:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da9252d576f63229f374aa1accb9ff853ef74762b5ccbfb7aeda9ff16141ffd`  
		Last Modified: Fri, 02 Feb 2024 00:56:56 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1e025ed1b9bf0bd074397aaef79acb84da64f2e4505a64302d5e26208729d7`  
		Last Modified: Fri, 02 Feb 2024 00:56:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055226a25aae6f6b1d05f0d6aa08aa84656c40b651c160bf4b32acec581791b0`  
		Last Modified: Fri, 02 Feb 2024 00:56:56 GMT  
		Size: 189.4 KB (189405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4aee1701ba04a77cd7462cab41f28dc2682f8f6158aa5df2c81cda23c10286`  
		Last Modified: Fri, 02 Feb 2024 00:56:57 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.17` - unknown; unknown

```console
$ docker pull kibana@sha256:06b203e866a2ffca92ef545c9f69ada895c52473f62a9fa331752307e9483797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d9c5a188d30f602791d914073ee03617c2c3d512a710a02ecf07aaff7f7063`

```dockerfile
```

-	Layers:
	-	`sha256:3b37b8b8452f460ddc46530ca79b0b40c06ab417b58925da34dbdfd3c2e372e8`  
		Last Modified: Fri, 02 Feb 2024 00:56:54 GMT  
		Size: 3.0 MB (3032994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7e4e5aea681d9043210968b6f0fa573dea29dd64e3f906ab9b515e91f2e05ca`  
		Last Modified: Fri, 02 Feb 2024 00:56:54 GMT  
		Size: 44.4 KB (44363 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.17` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:861c68e5ae05cbf1e169c164145f0829843f6a8ab821138d605aa5822711b69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368594904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcfa7c648efbeab53e2c5168249f98f6b13be2f9ec8dba070241a61fe22c99f`
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
# Tue, 23 Jan 2024 14:25:39 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 23 Jan 2024 14:25:39 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN fc-cache -v # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
WORKDIR /usr/share/kibana
# Tue, 23 Jan 2024 14:25:39 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jan 2024 14:25:39 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 14:25:39 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
LABEL org.label-schema.build-date=2024-01-18T12:06:03.434Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca09dff039c82e70b081f86f30b19515eb2968dc org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.17 org.opencontainers.image.created=2024-01-18T12:06:03.434Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca09dff039c82e70b081f86f30b19515eb2968dc org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.17
# Tue, 23 Jan 2024 14:25:39 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 23 Jan 2024 14:25:39 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 23 Jan 2024 14:25:39 GMT
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
	-	`sha256:02e45375df25649a72c8ff8dc43823608912851704a250884393fdc7c9e92995`  
		Last Modified: Sat, 03 Feb 2024 07:42:39 GMT  
		Size: 315.6 MB (315556357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4570b7e37d85b8b02f881c15a5b4979bd6dfa035c0811595fc0823b411d9e6`  
		Last Modified: Sat, 03 Feb 2024 07:42:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c8f6103d6fcd51ce88dee806474882a2a70032f58a26c0465046cf34b081ed`  
		Last Modified: Sat, 03 Feb 2024 07:42:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b3ab03da9ca206b160ed8db472c6cb0443b7cd0fadbdf50debdbfa55e0b686`  
		Last Modified: Sat, 03 Feb 2024 07:42:32 GMT  
		Size: 4.5 KB (4503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a241ad888fdc997899737284f9c8530afc4d4dbc54e14390152dfa66793d45d0`  
		Last Modified: Sat, 03 Feb 2024 07:42:33 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2afa35c464a5560a85c04c4e6a52440c4be8a2b40c8adb54f38b960331a24`  
		Last Modified: Sat, 03 Feb 2024 07:04:25 GMT  
		Size: 183.4 KB (183408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90ec076ed5797e570a87b9ef34195339f768de25da79b21dc2bab799ae91264`  
		Last Modified: Sat, 03 Feb 2024 07:42:34 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.17` - unknown; unknown

```console
$ docker pull kibana@sha256:26453ee914604d9b721c455efc189896745d3b40f5845af73d359ba4a0e4004b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1972471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3b59da3d7bf9d8b1c3a0464996ebf8e2e1c61b1489e6cc0b8ef5add3bda691`

```dockerfile
```

-	Layers:
	-	`sha256:a7d40413a11f378ffd05fc0d2de3f8eda9e58d5e5ba5b40668e92005e716850c`  
		Last Modified: Sat, 03 Feb 2024 07:42:32 GMT  
		Size: 1.9 MB (1928265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9661d2f96bc4455e00607220e83941cf7bd2582d84c788b02c666dbf17fd029`  
		Last Modified: Sat, 03 Feb 2024 07:42:32 GMT  
		Size: 44.2 KB (44206 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.12.0`

```console
$ docker pull kibana@sha256:59c4f971a5e73c674dc777dcf94bf545e2ca42abe7ff09b74f9cf685c2487cc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.12.0` - linux; amd64

```console
$ docker pull kibana@sha256:1e4dc91c86f483e19f8a370f7dda0bf6b7f26d9d1c3805a15e4346e95416faa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371777232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c450deccd41412a98fd72d1156b0a2168b52d8c3124c9e0d7980403cc6d79c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 17 Jan 2024 15:49:20 GMT
ARG RELEASE
# Wed, 17 Jan 2024 15:49:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Jan 2024 15:49:20 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 15:49:20 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 17 Jan 2024 15:49:20 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN fc-cache -v # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
WORKDIR /usr/share/kibana
# Wed, 17 Jan 2024 15:49:20 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 17 Jan 2024 15:49:20 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.label-schema.build-date=2024-01-10T23:07:27.032Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=e9092c0a17923f4ed984456b8a5db619b0a794b3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.12.0 org.opencontainers.image.created=2024-01-10T23:07:27.032Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=e9092c0a17923f4ed984456b8a5db619b0a794b3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.0
# Wed, 17 Jan 2024 15:49:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 17 Jan 2024 15:49:20 GMT
USER 1000
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5f975913803f39cbb4b358a9ecfe63b8d3c4d8869f3eab22513b5b78ce1cf6`  
		Last Modified: Fri, 02 Feb 2024 00:57:30 GMT  
		Size: 10.5 MB (10532019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841f33a9607079a327c338a34e171023f0fa5b8bcf661881cec46b0d655caacd`  
		Last Modified: Fri, 02 Feb 2024 00:57:29 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1e697814e8647960924a7413365e3a2a0ff038ef5b63c4a0096514697ca660`  
		Last Modified: Fri, 02 Feb 2024 00:57:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49734fcf88d21c7bf125100aba7b130ef1d856b137f47c2e47befa03775d666`  
		Last Modified: Fri, 02 Feb 2024 00:57:30 GMT  
		Size: 16.5 MB (16460478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a596afc3f816cfc96382e98338613925656185f1046ea4a6c12d683d60b18d`  
		Last Modified: Fri, 02 Feb 2024 00:57:30 GMT  
		Size: 5.3 KB (5287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be78bb40703357cc561f58265f6f4f2c87c0754d11f12e0dd914a3b5264959`  
		Last Modified: Fri, 02 Feb 2024 00:57:36 GMT  
		Size: 317.1 MB (317058086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11bc4bb6686939fcd3bb5c02385dbf756dc6b9d49795765b56fe2a1c1c9f143`  
		Last Modified: Fri, 02 Feb 2024 00:57:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdab6502ecbe4dd568c695ba6ce12331072bc415af2555082647a5b00678afa`  
		Last Modified: Fri, 02 Feb 2024 00:57:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786c5838ee80d41239d91335064b71ee4495776cfb3a8d28ecb1cce9c411da7`  
		Last Modified: Fri, 02 Feb 2024 00:57:31 GMT  
		Size: 4.6 KB (4553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe49bd8bd6e3718371406553f5639f1b382cb1874e0b50794e7e075b7fe84ed1`  
		Last Modified: Fri, 02 Feb 2024 00:57:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758705a540697400ea25cecce04a784de0f508347215e6c43593e15493f93157`  
		Last Modified: Fri, 02 Feb 2024 00:57:32 GMT  
		Size: 189.4 KB (189405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc4dab6220d9bb4e295621f4c04674b0ad3f84beb678438b81d165855e1431`  
		Last Modified: Fri, 02 Feb 2024 00:57:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.0` - unknown; unknown

```console
$ docker pull kibana@sha256:7da7dca9f5ffa32e5ae253aaf03359e4ee00f8ef4fffa757783541f0ff84d25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3518702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf96b18fb8538c29c49aef3e03a79ebfb8922f528475f922ac3383d19ad0ecb8`

```dockerfile
```

-	Layers:
	-	`sha256:793c46a96539aa03d135fa609b0175787ffd96f1fc20fb3d7a7c212033bcedc7`  
		Last Modified: Fri, 02 Feb 2024 00:57:29 GMT  
		Size: 3.5 MB (3474351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dff1c1b9621aed975ba051533411abbf84f072cd50a25a7a141b07953b76550`  
		Last Modified: Fri, 02 Feb 2024 00:57:29 GMT  
		Size: 44.4 KB (44351 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.12.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:02d71aaaf18482669a1e62844c84ba37bea649ae09cf913f9088654e415df975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.4 MB (382392161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce01e6561c2f7ce9b6763a33bdfc68c13456573d081cf92217df04ab34321cb`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 17 Jan 2024 15:49:20 GMT
ARG RELEASE
# Wed, 17 Jan 2024 15:49:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Jan 2024 15:49:20 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 15:49:20 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 17 Jan 2024 15:49:20 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN fc-cache -v # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
WORKDIR /usr/share/kibana
# Wed, 17 Jan 2024 15:49:20 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 17 Jan 2024 15:49:20 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 15:49:20 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.label-schema.build-date=2024-01-10T23:07:27.032Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=e9092c0a17923f4ed984456b8a5db619b0a794b3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.12.0 org.opencontainers.image.created=2024-01-10T23:07:27.032Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=e9092c0a17923f4ed984456b8a5db619b0a794b3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.0
# Wed, 17 Jan 2024 15:49:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 17 Jan 2024 15:49:20 GMT
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
	-	`sha256:821ed4dddd11c05f4e1b5891847e7e95134eedce20c044cd04c38834fa20484a`  
		Last Modified: Sat, 03 Feb 2024 07:04:29 GMT  
		Size: 329.4 MB (329353571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdb52edf8fb2c41556d3cae21b1e9e6f49dad38b7ae80dbee2501cf667bb37f`  
		Last Modified: Sat, 03 Feb 2024 07:04:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7f1d6e5645de3e043a6a024e880a3ccc51111053f9b7a37791482b041ea3cc`  
		Last Modified: Sat, 03 Feb 2024 07:04:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f34b6711f09c068a3087ca802bdaab9a636e3f003003b24dff7592e932d2c0c`  
		Last Modified: Sat, 03 Feb 2024 07:04:23 GMT  
		Size: 4.6 KB (4552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b61feeba44c2d6d874f6f8b058817a5cd3315908659946787d2364ae6ba5f9a`  
		Last Modified: Sat, 03 Feb 2024 07:04:24 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2afa35c464a5560a85c04c4e6a52440c4be8a2b40c8adb54f38b960331a24`  
		Last Modified: Sat, 03 Feb 2024 07:04:25 GMT  
		Size: 183.4 KB (183408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca025db5018e8ad8a148d5b00ca6d617ad1289b068880be212d4cedc1031b766`  
		Last Modified: Sat, 03 Feb 2024 07:04:25 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.0` - unknown; unknown

```console
$ docker pull kibana@sha256:38a3d6010a450e7c4f860a284bf574413cb9dcbd6d7b4ee800bd35bf6e5ee3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1922430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957d2d367b1274549a5d7c6108821a1ac36308e3944098969ea3813a7db36a25`

```dockerfile
```

-	Layers:
	-	`sha256:72aa10cb095e15c72064de841ac9896e86b7558b4f01432cba8ba8f408240833`  
		Last Modified: Sat, 03 Feb 2024 07:04:22 GMT  
		Size: 1.9 MB (1878236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e356d5190ba6bda97873f1f1f8fc5fe332a223dc8753c56038227bf5daa0ee3`  
		Last Modified: Sat, 03 Feb 2024 07:04:21 GMT  
		Size: 44.2 KB (44194 bytes)  
		MIME: application/vnd.in-toto+json
