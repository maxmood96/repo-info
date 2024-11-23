<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.25`](#kibana71725)
-	[`kibana:8.15.4`](#kibana8154)
-	[`kibana:8.16.1`](#kibana8161)

## `kibana:7.17.25`

```console
$ docker pull kibana@sha256:2a023f14326f8172cba9fb1d2c8546caedc30d5092e8c0bfa744864c22f8a3dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.25` - linux; amd64

```console
$ docker pull kibana@sha256:bff796b0c616ca1e18f7172baae740c2c0b46c1e34909d63bd71c5c58b583574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349959098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b099d33c968f606eac8abe12ad335446cc4ddb556d10dff5d9121590cd10168`
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
# Tue, 22 Oct 2024 09:34:17 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 22 Oct 2024 09:34:17 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN fc-cache -v # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
WORKDIR /usr/share/kibana
# Tue, 22 Oct 2024 09:34:17 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 22 Oct 2024 09:34:17 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Oct 2024 09:34:17 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
LABEL org.label-schema.build-date=2024-10-16T11:09:06.408Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=427e9521131a6f5f96fe79fb6d6eca013a5f89f3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.25 org.opencontainers.image.created=2024-10-16T11:09:06.408Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=427e9521131a6f5f96fe79fb6d6eca013a5f89f3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.25
# Tue, 22 Oct 2024 09:34:17 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 22 Oct 2024 09:34:17 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 22 Oct 2024 09:34:17 GMT
USER kibana
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6b2fd750b09fc1aa1a6a2bc3ff346de848d6956603f725a95d9a55edde719`  
		Last Modified: Tue, 22 Oct 2024 17:58:17 GMT  
		Size: 10.7 MB (10723882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f528fabc9b1239a42cf0a65941b4c67cbb502c28a324eca33a24c0280eda942`  
		Last Modified: Tue, 22 Oct 2024 17:58:17 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a4b250827209044f01ee5ac368caad27a0599eb36637473cd6ac11f3297e65`  
		Last Modified: Tue, 22 Oct 2024 17:58:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf8bf1c7b8d53bcc53d5202f69b444d68afd9ac110a3e11313186ee9e8a649d`  
		Last Modified: Tue, 22 Oct 2024 17:58:17 GMT  
		Size: 16.5 MB (16460479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9694fe72ae7c76eb419a528eb314c747f9e35bc18f1c71ef1963914212c9b3`  
		Last Modified: Tue, 22 Oct 2024 17:58:17 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829d2fe0e0854881bbbc7f426edb25ef9d08d13f4224ac13e6db93fa10ae83e1`  
		Last Modified: Tue, 22 Oct 2024 17:58:22 GMT  
		Size: 295.1 MB (295051985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e2da553b26655dc02b3f85cd0dfffc7fd73c9b6841e9efa828eeefda91dcef`  
		Last Modified: Tue, 22 Oct 2024 17:58:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa5d952f21e785fc9d26925a56fc59e6850766b89272eecf0b95a97469328e0`  
		Last Modified: Tue, 22 Oct 2024 17:58:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444dc18d22b8bb5b3b631876709942bfa0bc0e8bce1aee5fede70fe2e2b90d24`  
		Last Modified: Tue, 22 Oct 2024 17:58:18 GMT  
		Size: 4.5 KB (4503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bf7136591272fe0b38f4270fd8d251c9350ad3ad9430302aca47019796e7b7`  
		Last Modified: Tue, 22 Oct 2024 17:58:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0252f53ae7539f2d37374d53eb2b0f7a2ffdb8a0e872e53330209711629e0bd3`  
		Last Modified: Tue, 22 Oct 2024 17:58:19 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62f69fc4d402a48fa1f9c6773c7f4ab10af552ac73e533e7d26a2941c11946a`  
		Last Modified: Tue, 22 Oct 2024 17:58:19 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.25` - unknown; unknown

```console
$ docker pull kibana@sha256:b3dd8ec3354bb8c768ae13593bd7d9f7c2180017153eb9ad145796ec9ac28658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbc134d9aa4ff90393808d713a7c55784faf8c5bbbcfda6202f3a51ef1ef8e5`

```dockerfile
```

-	Layers:
	-	`sha256:76b1907edbce184fd96444aa145116bc0379652779c8832f036dec0f6b9b7b5d`  
		Last Modified: Tue, 22 Oct 2024 17:58:17 GMT  
		Size: 3.5 MB (3515765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d725190eef370ef82bb6c0bf1f6874bc9419a95bb7dc8da9ba04ab831cc78a17`  
		Last Modified: Tue, 22 Oct 2024 17:58:17 GMT  
		Size: 44.5 KB (44509 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.25` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:4888c354aa9a8aa38ad0b953c45a3ce9f56fdeb2df020155836446de7a5f0f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (361045291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa0d4bc22dbca0391f138794772e5537c32177714e02eadc7667c74104e2de3`
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
# Tue, 22 Oct 2024 09:34:17 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 22 Oct 2024 09:34:17 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN fc-cache -v # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
WORKDIR /usr/share/kibana
# Tue, 22 Oct 2024 09:34:17 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 22 Oct 2024 09:34:17 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Oct 2024 09:34:17 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 22 Oct 2024 09:34:17 GMT
LABEL org.label-schema.build-date=2024-10-16T11:09:06.408Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=427e9521131a6f5f96fe79fb6d6eca013a5f89f3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.25 org.opencontainers.image.created=2024-10-16T11:09:06.408Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=427e9521131a6f5f96fe79fb6d6eca013a5f89f3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.25
# Tue, 22 Oct 2024 09:34:17 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 22 Oct 2024 09:34:17 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 22 Oct 2024 09:34:17 GMT
USER kibana
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9292fd052a4e5afdfe32d05bbde9aa9737b03f4f092222375f58aa893250f48`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 10.6 MB (10575032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe65c4e7d35e036f20c05c604524a12b7c180dcf8354448b764990a740a798`  
		Last Modified: Wed, 16 Oct 2024 03:24:58 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed698c438cb75e359246a05f0a09d8ab3744169938947a81eab7ff9c35ad192c`  
		Last Modified: Wed, 16 Oct 2024 03:24:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bf4c1f716146058b2b87961c282bbca1bc4015028244ed2a66f638d20b70c6`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1172c9a679de7f18a23a7d365c9a4ba12121e229f42af8fce85cd18a15227b`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83738fafefe30085fa7d65cc5e8fdd26e27b3e8852f66fa6bbd2d516995192ab`  
		Last Modified: Tue, 22 Oct 2024 18:03:24 GMT  
		Size: 307.8 MB (307830694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81efd58689104f4b9dbe3a27201cb7c5e6c0238e9787fbe212f95f1b311ff18`  
		Last Modified: Tue, 22 Oct 2024 18:03:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fead5819d5f8218c95a7a4104ce99120c0956961ba74c8abe4fc45770d61ca7b`  
		Last Modified: Tue, 22 Oct 2024 18:03:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08ab59e2e31cf3ea445d32e4d3f86932340d3a3f3722352a562336ffa82254b`  
		Last Modified: Tue, 22 Oct 2024 18:03:13 GMT  
		Size: 4.5 KB (4502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00d54cebf0e7b8d9367e8d458dc4d910367993ea1b592d79a594862408750f0`  
		Last Modified: Tue, 22 Oct 2024 18:03:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9065d414e85b530c093e7b87fd94b7d633affef7f2b3684d624a0befa1a3ae35`  
		Last Modified: Wed, 16 Oct 2024 03:25:01 GMT  
		Size: 183.4 KB (183416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d292abb956b53dc6da11deed287d4734ec5fffa05dbe8543f2365bd9f153396`  
		Last Modified: Tue, 22 Oct 2024 18:03:14 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.25` - unknown; unknown

```console
$ docker pull kibana@sha256:27dfe629be631e48f69ba7e244e80f36736a117586c27b137c802c0c03f4c397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9052c911147c5792496c276c32ac350a617c0ca2e1927fecab869c3e9084f0f6`

```dockerfile
```

-	Layers:
	-	`sha256:1cfc8cd1166a28be3e7d3bc9fcf319f11cc4ad214a3719d80abee010be7b39af`  
		Last Modified: Tue, 22 Oct 2024 18:03:13 GMT  
		Size: 3.5 MB (3516015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:335207d47ffae7f8062019dd69a9d1cf3edd9f7145eec55f1ebded7fd1756609`  
		Last Modified: Tue, 22 Oct 2024 18:03:13 GMT  
		Size: 44.8 KB (44787 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.15.4`

```console
$ docker pull kibana@sha256:0c2f74cae0e1b31a2ece21d50ebb864fd8db73bafc32d4b660b87533d8f50240
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.4` - linux; amd64

```console
$ docker pull kibana@sha256:28b5cb2309d580cb5d8df0c199d2f8cc76b426450d1e94577e0703387a085557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394768345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446e0f6d342a7b69a5311c08f7445ed21d92014c93f53cc2fd69b25315931389`
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
# Tue, 12 Nov 2024 16:58:33 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Nov 2024 16:58:33 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Nov 2024 16:58:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 16:58:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
LABEL org.label-schema.build-date=2024-11-06T19:12:41.867Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=79d00ab0a960bc3594ebf8d96c7523673b84e745 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.4 org.opencontainers.image.created=2024-11-06T19:12:41.867Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=79d00ab0a960bc3594ebf8d96c7523673b84e745 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.4
# Tue, 12 Nov 2024 16:58:33 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Nov 2024 16:58:33 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Nov 2024 16:58:33 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e58f3b44b01bfac8d1f34cde796993448497af2036b86ed6e49e0ca66a66a8b`  
		Last Modified: Mon, 18 Nov 2024 23:06:51 GMT  
		Size: 11.0 MB (10966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ec3aa278ea4ee284a1e6ac2d39827d0137a12f98c9cf52699c58a0d02d7ede`  
		Last Modified: Mon, 18 Nov 2024 23:06:57 GMT  
		Size: 339.6 MB (339618508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3518689886f378677085a79e6f15544d9ee647dc3fee947100148e92a2b0401`  
		Last Modified: Mon, 18 Nov 2024 23:06:51 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e154c397b8a5baf90ef3b382f7006c9ad6ed3a19730fd6d773437c8c666e719`  
		Last Modified: Mon, 18 Nov 2024 23:06:51 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1ae7357ac99602fbf71ba98f98e63d9eb97ae83691f8c2d866917befdfb4d`  
		Last Modified: Mon, 18 Nov 2024 23:06:52 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f22edb858101724a502dc04d30d182cd5ad89dfda0d965339b9f38e4706e76`  
		Last Modified: Mon, 18 Nov 2024 23:06:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b709b13e130bdb963597efe55cded9197a8e4d20f99a226ceb57a452fe193f00`  
		Last Modified: Mon, 18 Nov 2024 23:06:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029831e7b1e3a5a5c2d2db00bf8e155e9a20e5918fe44df2dbbb47201573ba93`  
		Last Modified: Mon, 18 Nov 2024 23:06:53 GMT  
		Size: 4.6 KB (4629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027bf88f9375a0163019c8780c12e3c312528ada6c3de8e304e5de3466871340`  
		Last Modified: Mon, 18 Nov 2024 23:06:53 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262f1269258b7e363e5e4e2d0a3988df2bc94fcda896a68e4056b1cda88e4e75`  
		Last Modified: Mon, 18 Nov 2024 23:06:53 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49d85b40a3f28a0ce6eae93173b056860f2bad4b06240efc783faed95c88787`  
		Last Modified: Mon, 18 Nov 2024 23:06:53 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.4` - unknown; unknown

```console
$ docker pull kibana@sha256:3e42ce3b82bfc2851f8df395542969125ef080fe89ec6602c3e5aea030731110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d97ec94b5db72564e8a4ee7af1c812d10a505b70b9fc277489b65d92f9de2f5`

```dockerfile
```

-	Layers:
	-	`sha256:551771e2d2b7aa9912a86f0d83b274e590b57e96b1433cef06ac3c5d27da4d76`  
		Last Modified: Mon, 18 Nov 2024 23:06:51 GMT  
		Size: 4.3 MB (4271735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e887cd51c5f685abbfd6bd016fc8dc9413c6a378f62f2e2e932c8ac647d750`  
		Last Modified: Mon, 18 Nov 2024 23:06:51 GMT  
		Size: 40.6 KB (40642 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:ac2e80f64f1b0686614052a57cde65d4773c3490e3b964fdc126565d3a0c7a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.8 MB (405837314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b54340c540e74d2d5ae0d84770d319a3e8b5bdee939b10c5fc50cf6d4e831b8`
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
# Tue, 12 Nov 2024 16:58:33 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Nov 2024 16:58:33 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Nov 2024 16:58:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 16:58:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 16:58:33 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Nov 2024 16:58:33 GMT
LABEL org.label-schema.build-date=2024-11-06T19:12:41.867Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=79d00ab0a960bc3594ebf8d96c7523673b84e745 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.4 org.opencontainers.image.created=2024-11-06T19:12:41.867Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=79d00ab0a960bc3594ebf8d96c7523673b84e745 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.4
# Tue, 12 Nov 2024 16:58:33 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Nov 2024 16:58:33 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Nov 2024 16:58:33 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5615ce72569ba1d15512469e51a8912567f652afdf4f67ce8df86e055a26c182`  
		Last Modified: Mon, 18 Nov 2024 23:48:55 GMT  
		Size: 10.8 MB (10818065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188be2140cf2760b756d30bb343c2868fa72111c606ee3c37204324d40afda91`  
		Last Modified: Mon, 18 Nov 2024 23:49:02 GMT  
		Size: 352.4 MB (352379744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686a94e05215caf3f8f446416b670836ca053a616713e3be04c021f0ac5b1818`  
		Last Modified: Mon, 18 Nov 2024 23:48:54 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd95f8df248a7a8c4dcfea33d87a7ac80ff816a25f5e26f1dce6d3abdfc6fb85`  
		Last Modified: Mon, 18 Nov 2024 23:48:55 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d71f1fa15cf48f67e72660a723a354b7561b29bbafd541f22c903067bfb8c`  
		Last Modified: Mon, 18 Nov 2024 23:48:55 GMT  
		Size: 5.3 KB (5287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9283161cc26e4f7e9127ee78de9defdfff0a9e19ddf5c02eb325e847cff7aa85`  
		Last Modified: Mon, 18 Nov 2024 23:48:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965bdf0d7f9e144c615ab7e2622f29f505412190bbb65989ba541eed38381ff5`  
		Last Modified: Mon, 18 Nov 2024 23:48:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d89159c7b5699521649bfc775854aad472a16af033f47211edbcbab215e7af`  
		Last Modified: Mon, 18 Nov 2024 23:48:56 GMT  
		Size: 4.6 KB (4625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908aaa9840c3faf6f2c1e447384d94df02b23575d1f6b3bcc4cfd554ffd07833`  
		Last Modified: Mon, 18 Nov 2024 23:48:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51726ba729828541df09fb8d1cd44a79a8d6c9689cff339e8327a0fd8dbe6cfd`  
		Last Modified: Mon, 18 Nov 2024 23:48:57 GMT  
		Size: 183.4 KB (183418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30ac1541ed4b06a0643031fed872a138a0d1e6780345cd47f4dadf2cf6bc6e3`  
		Last Modified: Mon, 18 Nov 2024 23:48:57 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.4` - unknown; unknown

```console
$ docker pull kibana@sha256:fe10bd87d89f5a2d6cd67fc1c77de26b546fab8adb05b0edb2f62fc3fdedd06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e50dca3164d71dd30d7de656e907f992587ab5e78c754a7ea276ae1f7f25a1`

```dockerfile
```

-	Layers:
	-	`sha256:e80449fd4153221055d5a6a5954b450a9111541806bde424ada4d81244ce9ae5`  
		Last Modified: Mon, 18 Nov 2024 23:48:55 GMT  
		Size: 4.3 MB (4271985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33f414a42c1ccc33c8cdd7e3aa610b283d8fad6fb8a170cbeb1d1f5d77b6fd9`  
		Last Modified: Mon, 18 Nov 2024 23:48:54 GMT  
		Size: 40.9 KB (40890 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.16.1`

```console
$ docker pull kibana@sha256:e18c1f6d92e819b1c577a1af9a02bfcae6e8b63596368eec3b40e9ad98fa3caa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.16.1` - linux; amd64

```console
$ docker pull kibana@sha256:f8c9ef95178e2d69f235b7608002aad6e65a9bd5619a97c6fcf70cd711b54e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.5 MB (399539259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd512e662b948d5cb401f5157a796b1637867982f9ee6ec7e3fe570bcbc7fd8`
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
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN fc-cache -v # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/kibana
# Thu, 21 Nov 2024 14:43:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.build-date=2024-11-18T21:51:43.597Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c8b46e87c4d61de4fe046ce5ea0a0b68aad5acf9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.1 org.opencontainers.image.created=2024-11-18T21:51:43.597Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c8b46e87c4d61de4fe046ce5ea0a0b68aad5acf9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.1
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 21 Nov 2024 14:43:56 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c09c13c28a9457ae8351feba0af26380ec81d28b0bd85a34ff46ceb4c10b97b`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 11.0 MB (10966600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2725ea15fd504d7a1bf6e70379bc8601ccfbf419f42b27157fe7970cf783f153`  
		Last Modified: Fri, 22 Nov 2024 22:27:24 GMT  
		Size: 344.4 MB (344389396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7555efbf0e0e57d6b2ff7f4c5ec164d7fcdfe15222fc645085df8df3a304b883`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe02a55404585e7ba59c162fa3f9a5d22908ba8f8b5a1d7edd3626afe001f00`  
		Last Modified: Fri, 22 Nov 2024 22:27:21 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f98293cbc6ee0a63d7a9aaa66dde40d8caa26cc9301dc9c845e7be74f83349`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5912356d257df2378fbf4e0e1601eb09c1ab582a5e76ff57b777f590d4a7717b`  
		Last Modified: Fri, 22 Nov 2024 22:27:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8e5194538bf0faa60f77fd2416b0c75033479286330004357b4abaafe3a573`  
		Last Modified: Fri, 22 Nov 2024 22:27:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5699e7e34f4ccf05533b5238e7d1fdbe1893518f9ad00273dc0fb7ffa11fa720`  
		Last Modified: Fri, 22 Nov 2024 22:27:22 GMT  
		Size: 4.7 KB (4708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e199b4ca13004e31fe8f8fa3379b1e9f271337cbd39ef478c95107a931aa37ed`  
		Last Modified: Fri, 22 Nov 2024 22:27:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ada342a4c70a9fe6662eff41981563444cbcedec1d35f2b844b62f4e8d788df`  
		Last Modified: Fri, 22 Nov 2024 22:27:22 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7750700c9c9421908a7e3f9f52fada3f55362c5da62ff98a2a74e02317583b`  
		Last Modified: Fri, 22 Nov 2024 22:27:22 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.1` - unknown; unknown

```console
$ docker pull kibana@sha256:b4aa4248184403e507fd219e79f6859fe0077a35e563436f8c8404aeaff15bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e804663ffe72a322e0f84fb4ac958bb9a7c272d46569121ff310180c525701`

```dockerfile
```

-	Layers:
	-	`sha256:41934a059eb1faeb4aeaf432637557ad04d70f8f64d0656beb02ae94ddc2c1fe`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 4.3 MB (4323778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a800f48aaa0002734c84931f1d1fee08b9db544317974f6b8b9ee5adb76f4e87`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 40.6 KB (40644 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.16.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9e7acb4155627f28c22393035c665a25584cf572e99c49d77151146de305620d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.0 MB (409996531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d452e3e905302d366dfab749cefbc8d33425ab0d23c704da3068eb846b331cb`
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
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN fc-cache -v # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/kibana
# Thu, 21 Nov 2024 14:43:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.build-date=2024-11-18T21:51:43.597Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c8b46e87c4d61de4fe046ce5ea0a0b68aad5acf9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.1 org.opencontainers.image.created=2024-11-18T21:51:43.597Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c8b46e87c4d61de4fe046ce5ea0a0b68aad5acf9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.1
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 21 Nov 2024 14:43:56 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5615ce72569ba1d15512469e51a8912567f652afdf4f67ce8df86e055a26c182`  
		Last Modified: Mon, 18 Nov 2024 23:48:55 GMT  
		Size: 10.8 MB (10818065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b409364d0faea72e610f0cd83134cc8f421ea09c56f11155195e3ab835a4ee`  
		Last Modified: Fri, 22 Nov 2024 22:39:05 GMT  
		Size: 356.5 MB (356538873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fe55bca762601e2d11ddf23be97d01b719c223c3f0bc4302aed063a6e743cb`  
		Last Modified: Fri, 22 Nov 2024 22:38:58 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447ba0f4f0a7a3d3b1c6030f799a243f2364446c81e551aad0e35525200c8d92`  
		Last Modified: Fri, 22 Nov 2024 22:38:59 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e483b95a7aa3b08845bc7d00b547558a4d4a3744dd8ca37aaf5e4c65a2886c`  
		Last Modified: Fri, 22 Nov 2024 22:38:58 GMT  
		Size: 5.3 KB (5303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6384c0b839e59f38f5cd8400b77bec6765b5efdbd52fbb427a22d0ae02f02`  
		Last Modified: Fri, 22 Nov 2024 22:38:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58061144adaca5875d0db1f3f2d4ea6906e17b928a7b3ce79ece9f8a4fe84cca`  
		Last Modified: Fri, 22 Nov 2024 22:38:59 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9270968484519e50d572e5d5f17fa406777a96191002a969429309dce43a7`  
		Last Modified: Fri, 22 Nov 2024 22:39:00 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14870c37dd46589a85a047128425fa7c700c506d689e9c63fb4d1c34404d7859`  
		Last Modified: Fri, 22 Nov 2024 22:39:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfde3d9a2ab78c0e68bce005be30e0b3acac5b28a902c29b39a7afedadba7c5`  
		Last Modified: Fri, 22 Nov 2024 22:39:00 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe0788bd1a53fe8a126ee2ec298e99c57cea0d0b797a010e629446dd3e8dea8`  
		Last Modified: Fri, 22 Nov 2024 22:39:01 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.1` - unknown; unknown

```console
$ docker pull kibana@sha256:e580f4749fb6d1388ee43e14bd93b79fb878d175e1f37e93f72487383775ddf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e141e58e99da2968ac2899210c50abf25e1213e97e83b7b4bf66ade5901dc3a2`

```dockerfile
```

-	Layers:
	-	`sha256:dcb10ceb483b232f5f4c16ae741b97f7192ab25ba3485956c346060ca9dcce13`  
		Last Modified: Fri, 22 Nov 2024 22:38:58 GMT  
		Size: 4.3 MB (4324028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a639ba57f141e261ec6210b2eb2351fae2b68b6db4cc333634c7424a24fd4c`  
		Last Modified: Fri, 22 Nov 2024 22:38:58 GMT  
		Size: 40.9 KB (40892 bytes)  
		MIME: application/vnd.in-toto+json
