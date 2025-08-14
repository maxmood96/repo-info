<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.10`](#kibana81710)
-	[`kibana:8.18.5`](#kibana8185)
-	[`kibana:8.19.2`](#kibana8192)
-	[`kibana:9.0.5`](#kibana905)
-	[`kibana:9.1.2`](#kibana912)

## `kibana:7.17.28`

```console
$ docker pull kibana@sha256:5746dfa67b2e363bc8464988ca899b5859dd5679aad2b8f0016577b685202b60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.28` - linux; amd64

```console
$ docker pull kibana@sha256:ae7529c338c95253bfb7400b3de3d05885614d0ae64ee419158f2806796410db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (353985258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182a8b55517ee47a2fbb2fecfc275fce5fb188efb19653045c68b4687d506362`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
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
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c489c21c21996e4bf7fba9c4bb798ca2191be98423ce0706ffec9d8b084a410`  
		Last Modified: Tue, 12 Aug 2025 20:11:25 GMT  
		Size: 9.5 MB (9505917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e66b1412989ad2eb8708597f7a770bd181a0bcd13e920a4126df876a1b39c8`  
		Last Modified: Tue, 12 Aug 2025 17:30:52 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b44a06fd1ff404bd1fd45652187f3bd0a4ba7fc0d748c38d6569a8eaf8fb87`  
		Last Modified: Tue, 12 Aug 2025 17:30:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab626423431855f2d522ce5325df78305ae33eeb2e5c12086cc73156f0fa554`  
		Last Modified: Tue, 12 Aug 2025 20:11:27 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66f92e33c1adbc7e27c748cbace09ca1200e34dca9babaaff289e77c2ef0447`  
		Last Modified: Tue, 12 Aug 2025 17:30:58 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d919888680bde7e1631284716acb0edfea7170fa3d15d9dfaab69544993dc6`  
		Last Modified: Tue, 12 Aug 2025 20:11:42 GMT  
		Size: 298.1 MB (298112530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b689ecbe81df7888c299b04e78f46e317ce54596dae2de6645e050794abe19`  
		Last Modified: Tue, 12 Aug 2025 17:31:02 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabf137bcafdf490eea26a2d26ee1082922bf793318467527d93b57862b1ad20`  
		Last Modified: Tue, 12 Aug 2025 17:31:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9804b60bdd9642d93e71e688529a60c4147ed361aea8913059f1643bd6d8d6`  
		Last Modified: Tue, 12 Aug 2025 17:31:08 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182ae48cab71bb558e4e44122f36d23ae9d8b7598f1c18968b970dd67cf16c1c`  
		Last Modified: Tue, 12 Aug 2025 17:31:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2540a019ed1130208ff4ea6f3d3fd7034637c56858ac44118e8d4acb6fcb42`  
		Last Modified: Tue, 12 Aug 2025 17:31:14 GMT  
		Size: 161.5 KB (161457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048041c387b14dd5878d65443fc3d39136ff860755a4d58b3b3807f1e704e4b`  
		Last Modified: Tue, 12 Aug 2025 17:31:18 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:4a7b00b5852149797c4ee5c31437eca0cd54baf01d6fc54142a61435f8e98578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2ffaa1e7581f167fe4b52067829b7ced1351d92a204e928aba53b4ffe0e9d1`

```dockerfile
```

-	Layers:
	-	`sha256:3779cd7cfb56d95fa70990d6ca08a32becc84ccc073789b01322e2b8b44298d3`  
		Last Modified: Tue, 12 Aug 2025 20:11:22 GMT  
		Size: 3.5 MB (3506830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc5907ad7de0cebc6780d54367eecce39c212a1dace411961f3ef062d138f37`  
		Last Modified: Tue, 12 Aug 2025 20:11:23 GMT  
		Size: 44.6 KB (44554 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.28` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:881a636d46c2ec1ee3afd7402a388183f80c26ba97d96541b6cf181176b3002c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366174215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4860e9fd2dcf13538914e5ca2a024d3e3dc857a7dae562a8a1b9d9381ee22d57`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
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
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0022fcadab11aac508c44fe2564d57dba4958e2459fe3601997f0b0e1fbe4f3`  
		Last Modified: Tue, 12 Aug 2025 19:32:47 GMT  
		Size: 9.5 MB (9526043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73251f8340ddcf2b3ee116db30533c21e52164484a360324511d647f75c8462a`  
		Last Modified: Tue, 12 Aug 2025 19:32:43 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1127a44491b4f226e5189c6a31536b1c79650020e7e30aaf8e1e7940ce5bce`  
		Last Modified: Tue, 12 Aug 2025 19:32:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5303fdaa61e274cddd3bca2ae09c8443327b5e364a50f33be0f0d7d177ad9383`  
		Last Modified: Tue, 12 Aug 2025 19:32:42 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a401df8c2556e38352092346e4f7738d8d30a4b5a39fcf58b9de74b60e523549`  
		Last Modified: Tue, 12 Aug 2025 19:32:39 GMT  
		Size: 5.2 KB (5245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5aa9124afe2c12964cca9df55086cf36aa0106b3c4d8105987e1c2805696e59`  
		Last Modified: Tue, 12 Aug 2025 20:15:41 GMT  
		Size: 311.1 MB (311148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293edb58c34bef9bcf7d31aee314e7dc1bc0d1c893f8b1e0896cccb82c1089bb`  
		Last Modified: Tue, 12 Aug 2025 19:32:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad04a1ef7d1a97f3569b2e80f82de9e039cdf2efb90146ecb3605e5a040f1e0`  
		Last Modified: Tue, 12 Aug 2025 19:32:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498cd5a3324096ff5866a223ab1bafbad237d7bcbef088c43cbf3b1ce2ee263c`  
		Last Modified: Tue, 12 Aug 2025 19:32:38 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c051d9f38c8d59a8b381f1e4308ff8d1059b26c5769e5cbbe8f6be38b378cf`  
		Last Modified: Tue, 12 Aug 2025 19:32:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1d3947101d0f169cba7fbe369d2a56ff46edfa53d0f9f94228e3ec825f3e75`  
		Last Modified: Tue, 12 Aug 2025 19:32:39 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f069672ef6242bc544c55162d3e17675d724b3c420085b7efe865229c7c400`  
		Last Modified: Tue, 12 Aug 2025 19:32:40 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:30ebceca5baf6355650c39e28aca0d8830c92e15add5920b87c4f63ba218ab27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2347078ee9652d86809bee5427a1d2706268b6008df0005e854eb5e98550b9`

```dockerfile
```

-	Layers:
	-	`sha256:737a4a6267fa88409d9c08f1955981d0c6188067791a83e5a35cb9b02ebc1f73`  
		Last Modified: Tue, 12 Aug 2025 20:11:29 GMT  
		Size: 3.5 MB (3507894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:133cdcbb0ac57251fa0735b1b06fe9d1ede8302c778949c66d1fff3a47e2035d`  
		Last Modified: Tue, 12 Aug 2025 20:11:30 GMT  
		Size: 44.8 KB (44832 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.10`

```console
$ docker pull kibana@sha256:5d82568eb7b2e51b535e292deb920414a1b4349d70e9c43da6512114bc4e6a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.10` - linux; amd64

```console
$ docker pull kibana@sha256:3a94f36efdaf2408e934125c97a6d75cec44305cb0d3ad178f687331dda209f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403375379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b31578e70710ad6dbf24250708f18f79b12fa5a0c9c011decd3c5bb79e6ced2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
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
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0072cb9c05fb81e3bf22323d02831b01fa503ea498fe8fbcf5d849a80ee92ffd`  
		Last Modified: Tue, 12 Aug 2025 20:16:23 GMT  
		Size: 9.5 MB (9505895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17698d41ff8dafd625e504668c5a129f5aa24e6f7ca0325e15314e4677c7cdb6`  
		Last Modified: Tue, 12 Aug 2025 20:16:34 GMT  
		Size: 347.5 MB (347502646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0957eed4ae00925b233a5ba0afab08f7690c874a7d620510cce42e66f6810498`  
		Last Modified: Tue, 12 Aug 2025 18:16:43 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ac7046ea433afb8732a9fd8607bc8bfdd4892e0ca9aefb1d86f59f547431a3`  
		Last Modified: Tue, 12 Aug 2025 18:16:53 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c96ac924fb0127b91419c08f98a1defc0bdb0681c60a4be4db0e7e7c6e14e4c`  
		Last Modified: Tue, 12 Aug 2025 18:16:59 GMT  
		Size: 5.2 KB (5238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8427857b60ee5124a4b75602fe547e80c398d8aa801f2641eec37756c6a80f`  
		Last Modified: Tue, 12 Aug 2025 18:17:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe1366d39a6065627f634298317ff73ace537398220ea9661651db198c04073`  
		Last Modified: Tue, 12 Aug 2025 18:17:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b582626e4b4f2b77a51b5d2fc9128f8415aeb1b033094cf5d8048facc0e487`  
		Last Modified: Tue, 12 Aug 2025 18:17:08 GMT  
		Size: 4.7 KB (4729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa20f86cb1d60f9fdb19a02f200437f3074e12cf092a29f7d4c4456dba8b3ce`  
		Last Modified: Tue, 12 Aug 2025 18:17:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35857afa928fc9a2172f2e134584c10676acf8985f93ae4441f5916fbfe37a9f`  
		Last Modified: Tue, 12 Aug 2025 18:17:15 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe944ac58ba64baf537f3bd90ec0b78a8ada39cc8e5e00124edd0938cafe36c`  
		Last Modified: Tue, 12 Aug 2025 18:17:19 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:6024e1f3ea90ad01a9fea8b259e12a1ee797eaed8ab36f2dfff1cc5867f13b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4560869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf50a97f17a540cc4cd1641a8dc4deef21183890edd8c4e9a03286ed67b0b7a`

```dockerfile
```

-	Layers:
	-	`sha256:e99b3f1307d62a3e38cd468e868d4f8385939d86582615e2667849c142384ba1`  
		Last Modified: Tue, 12 Aug 2025 20:11:30 GMT  
		Size: 4.5 MB (4520136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d47859e30d42d15a7ec29717ad007186e08d7a492a6d10cfe76dfaa0ce0a6bc`  
		Last Modified: Tue, 12 Aug 2025 20:11:31 GMT  
		Size: 40.7 KB (40733 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:7acfa3b707f2b64f9b9fd0e7cdd4a0421ef864e343dce1f7453668455e4c0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.6 MB (415577885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bc8c38600bb09844c45b14e9b995421aa186ff8374101a1c1449c42af5be23`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
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
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7390382d183389d73c2977b686c41af0e633e39481df6d453af5527481b586d`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 9.5 MB (9526104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc776529f99083751cf1e4452cc4866d0f572414ee285ded33b5ccd51fa6d23`  
		Last Modified: Tue, 12 Aug 2025 20:16:39 GMT  
		Size: 360.6 MB (360551661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d0211a2426add1c35807523043ab786a07865793e6694ec6c4ae07815e9ce5`  
		Last Modified: Tue, 12 Aug 2025 19:39:35 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa91fbf8d346949dd3aefc24a63810183dad4c5266c8cc08a790eed613807a8`  
		Last Modified: Tue, 12 Aug 2025 19:39:38 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be9050a3bdcd0176433bde36b71825f176f53f134866839417fc44e38c05f3`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c80e85b8d4678b0968fbf03123771f052e8b797a896a9c923c394a92b0d269`  
		Last Modified: Tue, 12 Aug 2025 19:39:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102463ea3d08147234ef1574d4fdd7621ac9305ed4b155e5ad724fceeb5a744f`  
		Last Modified: Tue, 12 Aug 2025 19:39:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d1dc04b68cf303d22568798e37f5d940934243d9b83bc167c083846d1406ea`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 4.7 KB (4728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6758d959f227508fe70511f58d0e3e960127b0078cc88d79b559bf926b10316`  
		Last Modified: Tue, 12 Aug 2025 19:39:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95590b862e14b9d89bca6a6168b6b357a8eb1f1a3fa713d56cc80fe65e546c17`  
		Last Modified: Tue, 12 Aug 2025 19:39:38 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b28ca260c092690bada595ae9dda52fe478a586c4b0ba887ee758274faa70`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:f5e80f783d2a355c5d1ff96e78e8bff08ffe0ba2bb86b6077c81dc9b86df9081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4562181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19ecc548ad09cdafa0747c26084e5866862526a46a4dc16461d56a6c4d73b87`

```dockerfile
```

-	Layers:
	-	`sha256:12bcacc2a25da2b0de7a947d1c0fc474f320a8a3b929323f2ef45a78ed177c57`  
		Last Modified: Tue, 12 Aug 2025 20:11:37 GMT  
		Size: 4.5 MB (4521200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95f3e16cbace48a24d20556d4358599a81dd971108e6dfa1101d43a1aafc54a`  
		Last Modified: Tue, 12 Aug 2025 20:11:37 GMT  
		Size: 41.0 KB (40981 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.5`

```console
$ docker pull kibana@sha256:49a800209074d2fab1a9fee8f615c334e1913c3daafed109d3686665270e6e10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.5` - linux; amd64

```console
$ docker pull kibana@sha256:a346e9b284413466d669adac0866890ae50d1657885c673b95e7e4793d700bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.4 MB (423390241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a316f5bf1116936afa7c2192a0c5d1c18937254cd6909e4f07e4f444538083e9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T20:16:41.306Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=1ac33f19e9d91983b71ac580abe325579e2d7495 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T20:16:41.306Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=1ac33f19e9d91983b71ac580abe325579e2d7495 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832b5b5c9d2c2f2d616dc810b2708b76f10d729313ea1ab857f1e79c2dc1342d`  
		Last Modified: Tue, 12 Aug 2025 17:29:56 GMT  
		Size: 9.5 MB (9505804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f88178dc268b1b5ee9b43592143041ea2f8ee117afee4af74272c20d289a2ef`  
		Last Modified: Tue, 12 Aug 2025 20:24:49 GMT  
		Size: 367.5 MB (367517564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd12f745555fe41a8a437c7b7fd3e8fc92dee4eba3f9fc2d69030c78f7fd684`  
		Last Modified: Tue, 12 Aug 2025 17:29:56 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531f44bee60ad47342a01912c1dd6341ccae1b3b668ae171f57904408003a492`  
		Last Modified: Tue, 12 Aug 2025 17:29:57 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b82bccdda80f0daf2f742ee3de2c8a2d62e0a4304f182f97b600abcf3079058`  
		Last Modified: Tue, 12 Aug 2025 17:29:56 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e84c0a2cbde8e027f823635bef466d84ded220522926e0d09e2721033f3082`  
		Last Modified: Tue, 12 Aug 2025 17:29:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976071f82f1775c61fe4461eec29bc5921240fba20de901f6aae2f6853a482be`  
		Last Modified: Tue, 12 Aug 2025 17:29:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636c1208d54e862c7990bb68a10f8c09d488b4586732a50e0f7197df26987f38`  
		Last Modified: Tue, 12 Aug 2025 17:29:52 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ef69ed76a79aa703099c5062a064d4378cd4114b16e1ea1e0f3c64c241f4ef`  
		Last Modified: Tue, 12 Aug 2025 17:29:52 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dd7b026b3ce565c216dcf9e3a1d9aaabff8d4164888f2300df85d4f9499f57`  
		Last Modified: Tue, 12 Aug 2025 17:29:52 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1005486e0e12b2a81fa7151a51c877b7a749f3ac20309adee6c80cf3cae4a6`  
		Last Modified: Tue, 12 Aug 2025 17:29:51 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.5` - unknown; unknown

```console
$ docker pull kibana@sha256:8c7b4a62232a0b18c042c60c6aad4b042ab5ac8255a2edeafb7b855787848040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4917379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9791615a22831da4d4276d068f1f4408cd783d0563772c4d78a5c3f225ee8de5`

```dockerfile
```

-	Layers:
	-	`sha256:5bcfc49566fcaaf240c3e9108fd6c472c4365d315f923d1b3e08306d935fbfa2`  
		Last Modified: Tue, 12 Aug 2025 20:11:46 GMT  
		Size: 4.9 MB (4876652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47fc5eea000a66ef2838af2660f0d2f16c4bb5aac35fed3320ece217e3b72c8b`  
		Last Modified: Tue, 12 Aug 2025 20:11:46 GMT  
		Size: 40.7 KB (40727 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d5c1cad8f5ac13f609254e66c89183f2f0b4ebc8209e5b1a085dfe94f90451b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.6 MB (435577219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e59c32c41d5aa8be163d3db3fec4ba65ca2cbcb98b0054dd2b5084021bc16bd`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T20:16:41.306Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=1ac33f19e9d91983b71ac580abe325579e2d7495 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T20:16:41.306Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=1ac33f19e9d91983b71ac580abe325579e2d7495 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7390382d183389d73c2977b686c41af0e633e39481df6d453af5527481b586d`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 9.5 MB (9526104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a9f6c64a42cc1c96d909eb6b19238041654050a211a1ad74841debf205b21b`  
		Last Modified: Tue, 12 Aug 2025 20:17:03 GMT  
		Size: 380.6 MB (380550981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcd5373e34f6124e0955e0902f4a5b54b9ee04def8deb33aa0bcfa8e8f5b560`  
		Last Modified: Tue, 12 Aug 2025 19:47:10 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073d1060274aabb8a7b32412d624565821cd408c2d9a66b30b621a25d37b315d`  
		Last Modified: Tue, 12 Aug 2025 19:47:15 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849a09cf15308406ee80ba2e129ac811c40db1554c7ef0d11cd61e3429b43645`  
		Last Modified: Tue, 12 Aug 2025 19:47:10 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301af5c80a49456004215f01ebde7b965909ba10fdb36dcd897543d520fbf1d7`  
		Last Modified: Tue, 12 Aug 2025 19:47:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a2702a433bac855d21b1cf01c4ec74387987fbffa81bf757b18fb485711ed0`  
		Last Modified: Tue, 12 Aug 2025 19:47:12 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b973a700064fdf1c9610c18e1e3416052d8f9632f32ee3ffaafc0a8b2761c6`  
		Last Modified: Tue, 12 Aug 2025 19:47:12 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6ef2d0d986e66e8419cb495ce6283a8931991706e520c34cb6e36c05ce44fa`  
		Last Modified: Tue, 12 Aug 2025 19:47:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03628bf22b0c94880b89acd6a68c5014a10d98bd3a232e4f3a14e015cf613ffa`  
		Last Modified: Tue, 12 Aug 2025 19:47:12 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e0ce080dc01fdbc30d59bcb1698f53c0457b1fa7809b05056934b02e6d233`  
		Last Modified: Tue, 12 Aug 2025 19:47:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.5` - unknown; unknown

```console
$ docker pull kibana@sha256:9db96a53183648403742ca628987eecececb24112767f1fc819c5c8f92804b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4918691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d46e12c1556b0bec948e415f79da2c122265383c858863e2408d06d7fd7ce9`

```dockerfile
```

-	Layers:
	-	`sha256:19a3ee6a8eb8ed1d176a51dde0b48d8a045fab2a648e26753bfa1c4af589590a`  
		Last Modified: Tue, 12 Aug 2025 20:11:52 GMT  
		Size: 4.9 MB (4877716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7e86d59f2f08d23d142dc5e52ace62e9a3fb2636f5d6d1c416d9c95198eec9`  
		Last Modified: Tue, 12 Aug 2025 20:11:53 GMT  
		Size: 41.0 KB (40975 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.2`

```console
$ docker pull kibana@sha256:c66abdde6d51a439c97f0b1fc9811c53f3c0e0c9a2412626bd3f2f31882fb985
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.2` - linux; amd64

```console
$ docker pull kibana@sha256:0c4f4cae3c3743c258c4dfbcdb87a6d150ed63ccc4fb3f8650dfd69381d02ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.1 MB (436105022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338973c3d4a6ee0772f8a2317bb133d282f5c14e42f99df69be7d4db54f3d415`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:48:35 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T11:07:38.658Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=8634f44eaffa9f009f50401a2fbba85c95739a38 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T11:07:38.658Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=8634f44eaffa9f009f50401a2fbba85c95739a38 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da17328db70290ef7b80821f8054954a568947465e25c3068fce3aeadb88bccc`  
		Last Modified: Tue, 12 Aug 2025 20:53:48 GMT  
		Size: 9.4 MB (9431896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82658e0f4cb406114596d343ca43fb3eabc8fdd6eae7983f69367117ddada4c0`  
		Last Modified: Tue, 12 Aug 2025 20:53:57 GMT  
		Size: 380.3 MB (380306211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb6341ab5c510120c27292bec3eb8c87720080c2bfcd0faf0740f434d71b7c1`  
		Last Modified: Tue, 12 Aug 2025 18:15:36 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f939b814ca408fb1f402fb0c99537a0e69f3d03e40980f529bd49089e87d17d`  
		Last Modified: Tue, 12 Aug 2025 18:15:42 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291c2fe09bcd6c4a14934302c5fadad0a5ff31400a88c3c38455e07885ccddbb`  
		Last Modified: Tue, 12 Aug 2025 18:15:45 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd48ca0389843dd2c612fefad7b9057030a89ac275b2026efcb642e6dce7124`  
		Last Modified: Tue, 12 Aug 2025 18:15:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f31944749346534401c795f90da43ae1f1c87b65d4c37f8bc4c3a82b53e2e`  
		Last Modified: Tue, 12 Aug 2025 18:15:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd581cbe1a52c1b395be1492854226741a79ec0c764d048fef54ab98f063877e`  
		Last Modified: Tue, 12 Aug 2025 18:15:55 GMT  
		Size: 4.8 KB (4805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43236fc8c0a186df486008a154db7377d4844131cab6e6b9c0184fefad7c5847`  
		Last Modified: Tue, 12 Aug 2025 18:15:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c750ac78bc5ebf738bcd3d04f466befea060fb5a709848747588b459ce4bba1e`  
		Last Modified: Tue, 12 Aug 2025 18:16:01 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a40661d2eb7857a0d24dc453238eb3a88a54df9e6b860b8cf55b8a35c84b88`  
		Last Modified: Tue, 12 Aug 2025 17:29:33 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.2` - unknown; unknown

```console
$ docker pull kibana@sha256:0b119042ca531f6ceddde3204def3cef24a23dbcf8fc8110aaeec339159f62db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac521052eec2d2a51e37f1c4cbbd332a61b499c689a40c1dd0374472828bb4d`

```dockerfile
```

-	Layers:
	-	`sha256:66b241b6f3919489f6344fac133506a0b54f66ad048574e3d62990c15be055f5`  
		Last Modified: Tue, 12 Aug 2025 20:11:50 GMT  
		Size: 4.9 MB (4891307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0961084184c2b8fb87dbd3bc954eb7ab6baccc1625440107e3c660a3e5b87e5`  
		Last Modified: Tue, 12 Aug 2025 20:11:51 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:eee6e493afc50ca4a28941c22e861fc8d2374383f39bb077a945f03f877d6a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.0 MB (448035263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f510adfcf1a2ded4926b47c213bac7b7eaeab7372fcf81a3f35c86c269f296`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:48:35 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T11:07:38.658Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=8634f44eaffa9f009f50401a2fbba85c95739a38 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T11:07:38.658Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=8634f44eaffa9f009f50401a2fbba85c95739a38 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422aadf3d556125efcb65d8d104d95a37b722aff4a4d8a96cb3dd6fda4c0155a`  
		Last Modified: Tue, 12 Aug 2025 19:54:44 GMT  
		Size: 9.4 MB (9445862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad9a5d9a0e9e06309942022d1324b81b1ef1964c71aecaf1cb90bdd8d0b7b8f`  
		Last Modified: Tue, 12 Aug 2025 20:53:59 GMT  
		Size: 393.1 MB (393089223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670e9d0dd118efa243d60a6896ce630c01eee62a5174ff428fc87a54d6fe47e4`  
		Last Modified: Tue, 12 Aug 2025 19:54:41 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cd33f87bf420cc3b32e513728f7c88ff79d2c0828dd31ca88cf19c0d48ddcb`  
		Last Modified: Tue, 12 Aug 2025 19:54:42 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331e7271430bc0a42b4fb796020036437aab22d506df200a70b324bbac9e994d`  
		Last Modified: Tue, 12 Aug 2025 19:54:42 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187df41b8e20c23ce12a0d30a9755f1fdd57abbddd7c7c0244e0eeab13c9324e`  
		Last Modified: Tue, 12 Aug 2025 19:54:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c672cae6028529928ab9409e4b771de681f739abc69782837a90eb66547749`  
		Last Modified: Tue, 12 Aug 2025 19:54:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cbe5b76070cb6599cc57f60357447ec15677d328b5a70a81c8e7caa741ff3e`  
		Last Modified: Tue, 12 Aug 2025 19:54:37 GMT  
		Size: 4.8 KB (4802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d23a7a2d582d899453f16f09865c6c92a0667cd04fb14fc782194cecf4d223f`  
		Last Modified: Tue, 12 Aug 2025 19:54:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c33cfac144a39d3564d910a303471d6ed8c71470d2b0f1958b8267c01a37e5`  
		Last Modified: Tue, 12 Aug 2025 19:54:38 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f12ac502b491ab8bcfc8711ebd60e606d5198ed8d7044714c37f1e43c2ec46c`  
		Last Modified: Tue, 12 Aug 2025 19:54:38 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.2` - unknown; unknown

```console
$ docker pull kibana@sha256:5c67a51b12abcc5744acd8f6ddb17e168362f99bfd39ac3c7ade45b8892410f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a3ab730d50b7a5a5b543d45ab41d7cf4a9e5d22cc385fe1a40cdf35be7b5cc`

```dockerfile
```

-	Layers:
	-	`sha256:8057fb77284f7700a7952cbd0f1ba79e63422dae0686fa02d33c711e16bd1a71`  
		Last Modified: Tue, 12 Aug 2025 20:11:57 GMT  
		Size: 4.9 MB (4892371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1475c2301f5aa03b7ee35d00a08b7e1bfaddf879563bb8cbede5f4a5fc322122`  
		Last Modified: Tue, 12 Aug 2025 20:11:58 GMT  
		Size: 41.2 KB (41199 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.5`

```console
$ docker pull kibana@sha256:5975d68f9ff177576be62543874f8ee0309be2c25ee784e8b11cbc0ae0e4e66a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.5` - linux; amd64

```console
$ docker pull kibana@sha256:f8b9ed352c9b225dfc5e30b6f9f25fab635920b1a2a5e501e8e8b19f0644c388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.8 MB (437760299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32de0c5031e6711cde8c6e4f3258ce205c62420ae61ab1513446031a2c61501`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:38:57 GMT
ENV container oci
# Thu, 07 Aug 2025 16:38:58 GMT
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Thu, 07 Aug 2025 16:38:58 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:38:58 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:38:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:38:59 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T20:32:53.139Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T20:32:53.139Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a0d2f3afa2fb98404d0ec6a8d22cee2d2899d55db936b11ae2b56cc89ce4b`  
		Last Modified: Wed, 13 Aug 2025 23:17:45 GMT  
		Size: 19.4 MB (19379651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8da4afdd441b8d47538e759690a73df088813b4f8c9bd2d5945d84a4231867a`  
		Last Modified: Wed, 13 Aug 2025 23:17:55 GMT  
		Size: 362.2 MB (362170606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a99c9e1aefa425d714c0119fe052f2211bf59e0a3babc296b57261417bd43b`  
		Last Modified: Wed, 13 Aug 2025 23:17:38 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f2cc6a113f85bcdbac9653c1bab9a1033b28207b0a9c2a86599ef2c8cf5c5e`  
		Last Modified: Wed, 13 Aug 2025 23:17:40 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff0ab48baf8abf3c599742ba3ee6373365eaa0cba5d52738efbeeab87a41e22`  
		Last Modified: Wed, 13 Aug 2025 23:17:38 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92907021a023f83493e47e4349da4e708f6e5b8a21bb3a78227bba78461b3578`  
		Last Modified: Wed, 13 Aug 2025 23:17:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7131a70b37618ca62f91a37d4da4671531d4c9dd47dccb20560ddb69fefa12`  
		Last Modified: Wed, 13 Aug 2025 23:17:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e11e0c0eb6b6bd2b2be1382ce8a6accef4cb78a3bc7d3aff9e1d10d53d9915d`  
		Last Modified: Wed, 13 Aug 2025 23:17:40 GMT  
		Size: 4.7 KB (4686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cfe21b2de962c9254305b009428dfe4c7d4071ba424798bb59d49339e96a0b`  
		Last Modified: Wed, 13 Aug 2025 23:17:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a28a0a215b42c54d7a5cf6cfd6e354fbc6513398b4d6f6f60aa8b26b1064b6d`  
		Last Modified: Wed, 13 Aug 2025 23:17:40 GMT  
		Size: 75.1 KB (75099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be22b8faa5da67098eb35b0c90dfeb86ce909b14de1a188bc52bebfc3365b286`  
		Last Modified: Wed, 13 Aug 2025 23:17:40 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888f3ec4da49b47402ad84210865b1784553e11d8238091adda05e2e84da3794`  
		Last Modified: Wed, 13 Aug 2025 23:17:40 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.5` - unknown; unknown

```console
$ docker pull kibana@sha256:d35a190fe6a28c76fdedca7e3a12ac75ebb26386b9a96ab15583d16e3f35d496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1d001b9a25026811754822b7675b09afd316681621a4f174c58871e81c10e4`

```dockerfile
```

-	Layers:
	-	`sha256:2672f63dfd33ba72fb27ee4de6ddd37309f8e25f410f1ee69747e6fdbe9124ae`  
		Last Modified: Thu, 14 Aug 2025 02:11:20 GMT  
		Size: 5.6 MB (5585066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb69f03e927b50182059ce98fb0e8edd3427c567bc53b4b692abf225f7f5d8e`  
		Last Modified: Thu, 14 Aug 2025 02:11:21 GMT  
		Size: 43.2 KB (43184 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:c666cbdbdb7478a6b61d74afea502ecc9f44bf88c9ca5c9f99df3dbd7ee98830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448915454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527cedd92cc49e079e35dce93daa859f2d112bdceaf03889768ece7cfff55d4b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:43:47 GMT
ENV container oci
# Thu, 07 Aug 2025 16:43:48 GMT
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:43:48 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:43:49 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T20:32:53.139Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T20:32:53.139Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:ae68ff313f78851fbf66137c0a49a327986447045fa7f2497adbc1b57f88db56`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.8 MB (37819116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3bb33d49d3e4be3796cbdd0154b7074a57d0d984ccb6faa844f2dd1f9a1b16`  
		Last Modified: Thu, 14 Aug 2025 09:31:12 GMT  
		Size: 19.3 MB (19312754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8186b340064f2221fcc4798bb4c89edfe9695acb6aad3fde011019abc656c6`  
		Last Modified: Thu, 14 Aug 2025 11:15:50 GMT  
		Size: 375.2 MB (375226394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5979695854111794e0a9a5b410b8084e28687fb691aa2488c351c52408ea6a`  
		Last Modified: Thu, 14 Aug 2025 09:31:07 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee5861112db193ed85c83e05077921c1d4f97c9b5b576b9320f6ad482dc79b2`  
		Last Modified: Thu, 14 Aug 2025 10:11:15 GMT  
		Size: 16.5 MB (16460480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b696a6a1f84c086adc96e14c26526ff7090c0cfd7a17542d526b27c0de21bd12`  
		Last Modified: Thu, 14 Aug 2025 10:11:06 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18daaeb5ebf29dcd1d001380c7b6480429ff262edb8f66548cdaea3a447c442`  
		Last Modified: Thu, 14 Aug 2025 10:11:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52e4943bc4e8f0448116438a3e3c2435576541bc5ec678bfb8ddba1489d2f96`  
		Last Modified: Thu, 14 Aug 2025 10:11:06 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c310fc9754abad8d81add219abd1758ff7d809c9e5dae24175bbcd89c35b5fb9`  
		Last Modified: Thu, 14 Aug 2025 10:11:07 GMT  
		Size: 4.7 KB (4687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fde4101ca203a7596c22eb3c6fd4cab9f6f2a743531441e04d6eb1fdaafa219`  
		Last Modified: Thu, 14 Aug 2025 10:11:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e691ad45652944e71de0aacbf3827df751d0a4b8adbf3074eb14c8cb93a09`  
		Last Modified: Thu, 14 Aug 2025 10:11:06 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8686bbcb4659a6c1c3645f28e7676024b73d7d95cdb42e0b6f243352966cb5`  
		Last Modified: Thu, 14 Aug 2025 10:11:06 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b538eb813498016e564f95d2454aaec823977be77e23fc256a63629a1ff2db`  
		Last Modified: Thu, 14 Aug 2025 10:11:07 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.5` - unknown; unknown

```console
$ docker pull kibana@sha256:a39f27671aac2a6ccc720334475565d393dd83f7e71af03919fff1efde0ef8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5627183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71dfc3d911c949d0f263847783e07f89060b0689426a468c4eb8b988e1496a7`

```dockerfile
```

-	Layers:
	-	`sha256:2527674dfee3c8484bfbee1f0f8acb3ea37e4419eaa3d32477b2b3821c1d9b00`  
		Last Modified: Thu, 14 Aug 2025 11:11:23 GMT  
		Size: 5.6 MB (5583744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cdc45385e626062d60f21b151f61838997218f8c604dd7c94253fcfc4a2453c`  
		Last Modified: Thu, 14 Aug 2025 11:11:24 GMT  
		Size: 43.4 KB (43439 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.2`

```console
$ docker pull kibana@sha256:4fa683d1211cca3d848aced0900fef74b46cb78eb661c7216e64db07b45a6b3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.2` - linux; amd64

```console
$ docker pull kibana@sha256:e90369ad2687d2a3f6d138c2dc094eb5ee733c01979772be8ddf5131d7b1e566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.7 MB (435702292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30138ff7165f8f83c0930506b8b915dd0203a7aaf9a6f8223573f285a0927019`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:38:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:38:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:38:57 GMT
ENV container oci
# Thu, 07 Aug 2025 16:38:58 GMT
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Thu, 07 Aug 2025 16:38:58 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:38:58 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:38:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:38:59 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T16:35:56.587Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=616b79995b497dd1c83937d5f71450516b36b6fa org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T16:35:56.587Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=616b79995b497dd1c83937d5f71450516b36b6fa org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
```

-	Layers:
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd49ba6856c91abb6dd98ef991f1b4c22f25f133e048dc82f2c4779fc294519`  
		Last Modified: Wed, 13 Aug 2025 23:17:27 GMT  
		Size: 19.4 MB (19379633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3778d8fa67b4bc0931bbd68b3e998122dfa91af8ae2c642fc1f3f5ca22fee31e`  
		Last Modified: Wed, 13 Aug 2025 23:17:46 GMT  
		Size: 360.1 MB (360112571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30dfb682ebf9df0ee65dda6ea146e290f81c21530731e6c27a881170e0cddb7`  
		Last Modified: Wed, 13 Aug 2025 23:17:41 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919058619a1e5ff9b52c6f0c8ee1c67a4688664eed721f0441e1edabb0cdc436`  
		Last Modified: Wed, 13 Aug 2025 23:17:40 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b459c394bc2cd0701885511112ac3dbc2edf2aca288a8f20c6eebc65fce0683`  
		Last Modified: Wed, 13 Aug 2025 23:17:37 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0882b02b3c8505cdbf363b745895f21eec0f47b6c0d815e004d26dc990cb27`  
		Last Modified: Wed, 13 Aug 2025 23:17:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4dbc87d5b2908caed49b95f0171e786364e335372d1d9ef27ef8e58f2e8c23`  
		Last Modified: Wed, 13 Aug 2025 23:17:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d6ad4b73869a0d19704b26300adc9c1b2aa3c542a8bcfb206072c5b462df2e`  
		Last Modified: Wed, 13 Aug 2025 23:17:37 GMT  
		Size: 4.7 KB (4724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d85f84d1e284a5d567727d7eca82308e34d6041bcba7325d7fad785c76759a`  
		Last Modified: Wed, 13 Aug 2025 23:17:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a099d9d80a120ddd7b0443f6c733e714f63328f3cc6120327bda46ceb4170df4`  
		Last Modified: Wed, 13 Aug 2025 23:17:37 GMT  
		Size: 75.1 KB (75099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334f5884acb654696e69d1af9b1f3a32be68513f01eafd2a17111f41e2335cd9`  
		Last Modified: Wed, 13 Aug 2025 23:17:37 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e70d02304ae2c2005c41919ae0324b3d36ee62f6c9513ab897739f420c91aa0`  
		Last Modified: Wed, 13 Aug 2025 23:17:37 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.2` - unknown; unknown

```console
$ docker pull kibana@sha256:f0de121e1a075b009b2bcac3fc1cb1add827a4bb08be13386693b6e001c07827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5737511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680362f95123d5ba427265636addf2a843f4fb320b7ae1a1bff2e973447d2ec`

```dockerfile
```

-	Layers:
	-	`sha256:3e63fb221efee9dc870284241062bfe08d720b1a6b7c8ec2abe90eb481291762`  
		Last Modified: Thu, 14 Aug 2025 02:11:26 GMT  
		Size: 5.7 MB (5694326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17283758291e65762c43c6cd474eee185cedfdfeeb4542abd288cd5ff1864d7e`  
		Last Modified: Thu, 14 Aug 2025 02:11:27 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:3a76112e7f5019970375fcb57676e992da36f4e69a8de6d249d6414b9624fb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446561310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b469892e53466b01a50d85f918fd58c8b2fffcbefdd735b2b5f5747a2d129d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Aug 2025 16:43:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Aug 2025 16:43:47 GMT
ENV container oci
# Thu, 07 Aug 2025 16:43:48 GMT
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 07 Aug 2025 16:43:48 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:43:48 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 07 Aug 2025 16:43:49 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T16:35:56.587Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=616b79995b497dd1c83937d5f71450516b36b6fa org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T16:35:56.587Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=616b79995b497dd1c83937d5f71450516b36b6fa org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
```

-	Layers:
	-	`sha256:ae68ff313f78851fbf66137c0a49a327986447045fa7f2497adbc1b57f88db56`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.8 MB (37819116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3bb33d49d3e4be3796cbdd0154b7074a57d0d984ccb6faa844f2dd1f9a1b16`  
		Last Modified: Thu, 14 Aug 2025 09:31:12 GMT  
		Size: 19.3 MB (19312754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0c6447ae8b87ff0328a3148df669590c6a01ee8045dc139df7033a5fdf904`  
		Last Modified: Thu, 14 Aug 2025 10:17:35 GMT  
		Size: 372.9 MB (372872198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d17354441ba5cb58414906a2c1468273631974e0ad009e8111f81cc05abb9`  
		Last Modified: Thu, 14 Aug 2025 09:45:13 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d571f29820662b24a5e206f6e5ee95ad44c56e88836411c2ff8fbf366c7269`  
		Last Modified: Thu, 14 Aug 2025 09:45:33 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659c936425831d2d58691504f9fef6278ba342bb18dd63c32eb54d12da7c9f91`  
		Last Modified: Thu, 14 Aug 2025 09:45:32 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c770475cddcff9b58f18afb4d7ddd701e0012f3015358b74bce4bf27e727194`  
		Last Modified: Thu, 14 Aug 2025 09:45:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27245f026527478c085cc62f74554989ddb26206a16b0175e1af2b96a104d21e`  
		Last Modified: Thu, 14 Aug 2025 09:45:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab0fc18ff2ce398b2027593d813d52cad8b68794f6dad632e8f0bb4d7c8847`  
		Last Modified: Thu, 14 Aug 2025 09:45:56 GMT  
		Size: 4.7 KB (4727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b8461367b696b7599cd0ea25f62cec94c020692684de59430d0734e67d5838`  
		Last Modified: Thu, 14 Aug 2025 09:45:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32d3e887006ffc22d6fe103f6d5cca2d6374c52f8ba1a4fdf7fda95be820b5e`  
		Last Modified: Thu, 14 Aug 2025 09:46:02 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d13ad69fc4ec1c7bbaabf6c1a082e39847ea9f2cbf7a3f2aa6a3202cd6a88`  
		Last Modified: Thu, 14 Aug 2025 09:46:06 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218f35c289b73b753e9cef8d1e2b4deb7c2255428d28da95f247273fdeaf1228`  
		Last Modified: Thu, 14 Aug 2025 09:46:09 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.2` - unknown; unknown

```console
$ docker pull kibana@sha256:6787ef374c0145765f060a13673921fef7aef139c1e48b57a20bf70b1792d22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5736446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173c5a6b2326ce83e0246d24ad8b30b800114632198556ab163aedfe1a47f801`

```dockerfile
```

-	Layers:
	-	`sha256:b18d7745bb41dd08d52b7c81a87cbda4ac7a5745015d4018be1237aaf9e7ee5f`  
		Last Modified: Thu, 14 Aug 2025 11:11:31 GMT  
		Size: 5.7 MB (5693004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86e545e0cb0ad83fdbc8e24f0281881d11fc7aa5b3f6485305e653c804aadd3`  
		Last Modified: Thu, 14 Aug 2025 11:11:31 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
