<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.25`](#kibana71725)
-	[`kibana:8.15.3`](#kibana8153)
-	[`kibana:8.16.0`](#kibana8160)

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

## `kibana:8.15.3`

```console
$ docker pull kibana@sha256:47824ff5ca06578c8de76ab9b38b655b5d12550d413393cb626b66efdbf24617
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.3` - linux; amd64

```console
$ docker pull kibana@sha256:36a568fa4917d5b7bbf9f542de45ac4224b1e2dfa239ddfb0512602549d908ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394758461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e79e6b434938854674a4ac367f2e08d8ef489152a7a0e60fa023d8cb57474c9`
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
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN fc-cache -v # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/kibana
# Thu, 17 Oct 2024 12:21:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.build-date=2024-10-09T11:11:49.786Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3933429968aafb1ba31319fc38649d0f974044bf org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.3 org.opencontainers.image.created=2024-10-09T11:11:49.786Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3933429968aafb1ba31319fc38649d0f974044bf org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.3
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 17 Oct 2024 12:21:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e81878edc4fac5cec441a43d55d42a4ccda5f061205c121fc4806d01d95877`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 11.0 MB (10966616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2312b8c1d8c6c295daae8801c856bbc9b0c27a80133f5004d467ea0351eea946`  
		Last Modified: Thu, 17 Oct 2024 21:00:53 GMT  
		Size: 339.6 MB (339608695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86e1486e58baf6985b65ce10f332493c50d5bd307ad22a81b264bde6c97855f`  
		Last Modified: Thu, 17 Oct 2024 21:00:44 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042420ce6076b22215500cd72e65b7f9fd3e99d77f564209379821b4de4048c1`  
		Last Modified: Thu, 17 Oct 2024 21:00:46 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bca47f98c76ebfc15952de4cafd4504bb69312e94d8b284cd94d9720a0d737f`  
		Last Modified: Thu, 17 Oct 2024 21:00:46 GMT  
		Size: 5.3 KB (5274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d84a8a04346d1d0bf8c478a3ac35cf80e96fdee3738b154bf3506f61ab24988`  
		Last Modified: Thu, 17 Oct 2024 21:00:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f20def6164ce76efac95afb410323a0a66d330d86d7c02c5f651a92dbe7206`  
		Last Modified: Thu, 17 Oct 2024 21:00:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e373104978a531f777adb63d24a126bc369d5700bd7474fba3962904b5a12569`  
		Last Modified: Thu, 17 Oct 2024 21:00:47 GMT  
		Size: 4.6 KB (4625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bbb965b9c197734fb6626e5b9d1714b4bcf6978f33dfd2e998d1722cd39480`  
		Last Modified: Thu, 17 Oct 2024 21:00:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c325d52041107a5e71b22b4aec6ebc45fb4781664785c955f36e6167777f40`  
		Last Modified: Thu, 17 Oct 2024 21:00:48 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906d54432ff1d9fa69551f460ac8d6bb74b0cd352a0598329c98a66588304bba`  
		Last Modified: Thu, 17 Oct 2024 21:00:48 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.3` - unknown; unknown

```console
$ docker pull kibana@sha256:2db1e594ec8332860c9e2499c44c4fdf07562db7d6e04b24ee4c0375f4bf77f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69ced5ac5c204ace914bf4b33739fe49c2b8b28341048696cac2381b26cb327`

```dockerfile
```

-	Layers:
	-	`sha256:612a809daf52ccb82d52289f1ea32ffbc36f91b74263e50aa40d6c235431bad3`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 4.1 MB (4070903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de951ebc07571c3da9af40a247b641c44bbcbff680cae6aed81d707512cdf6a`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 40.4 KB (40425 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e2e2e6f9ed8902087e0592730a7c6edc94148a4f977d9df9189c1f9925f57727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.8 MB (405821992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e436961c293225cddc2793b96d9e46a070fbdfa3f8ece9b0f110335f7fdd6`
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
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN fc-cache -v # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/kibana
# Thu, 17 Oct 2024 12:21:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.build-date=2024-10-09T11:11:49.786Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3933429968aafb1ba31319fc38649d0f974044bf org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.3 org.opencontainers.image.created=2024-10-09T11:11:49.786Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3933429968aafb1ba31319fc38649d0f974044bf org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.3
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 17 Oct 2024 12:21:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6ba831b83cf620584ce3ad5fef753a25663549f8d119af4a0a620914f0f1de`  
		Last Modified: Wed, 16 Oct 2024 03:20:59 GMT  
		Size: 10.8 MB (10818125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ee6d8e35c71b9d4909022afbad37efb7d48f1f6b1ca819347270106f5106b6`  
		Last Modified: Thu, 17 Oct 2024 22:20:54 GMT  
		Size: 352.4 MB (352364368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff30b920890a2c495f379f559e7064243ab5398065c95db39cae562ef8e97b1d`  
		Last Modified: Thu, 17 Oct 2024 22:20:46 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c12a1fabb536688d5956b33b5a0593e172990d62beefd0b3171bbda3f2bd88c`  
		Last Modified: Thu, 17 Oct 2024 22:20:47 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b75b292032195705ebb38ddb4930e1a69ee95aac385a79400d427d30aaa86c`  
		Last Modified: Thu, 17 Oct 2024 22:20:46 GMT  
		Size: 5.3 KB (5281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f56cdecc00fd6f6b663514cf57e1c8b5d4ef7ba3bfd56d301235fabaa31e7c`  
		Last Modified: Thu, 17 Oct 2024 22:20:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7a7e5d863dcf9d0e36c8576f063cb52f382a80c3ae67475f75e672d3fa6858`  
		Last Modified: Thu, 17 Oct 2024 22:20:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1e14346d69ba3c49fd2a23443c75f2935c0f96795a6971bfb7b83ff1629702`  
		Last Modified: Thu, 17 Oct 2024 22:20:48 GMT  
		Size: 4.6 KB (4623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869cd104df7f51d5115842c750f0a10beee0a2621b08f44e37161340336c95c8`  
		Last Modified: Thu, 17 Oct 2024 22:20:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af00746a9670a0545c6c46c2ffe66a53dee088167099f7e64a8bde7536ad23f`  
		Last Modified: Thu, 17 Oct 2024 22:20:48 GMT  
		Size: 183.4 KB (183415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5038d92764f308df1f22dcd158bca835dfb5f364a810cdabd9c2cde631fc2a0b`  
		Last Modified: Thu, 17 Oct 2024 22:20:49 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.3` - unknown; unknown

```console
$ docker pull kibana@sha256:8d82ccf652591320627593027c061950e5cbbc5d08ccf2d5aad8b90013489c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5c05e4a1ae1c86831c41d4adde2bc3a2284edc5db19162fa530d0ca5903598`

```dockerfile
```

-	Layers:
	-	`sha256:93ebb2f405d78ae1e481a0e3fd67cf24c6c9aec60e2fb0f2c365182bd2f91826`  
		Last Modified: Thu, 17 Oct 2024 22:20:47 GMT  
		Size: 4.1 MB (4071153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3660dc8315cc9f2ad6de2053f9eaf3ac6a826ecea7aede54f175303c30ebd2`  
		Last Modified: Thu, 17 Oct 2024 22:20:46 GMT  
		Size: 40.7 KB (40667 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.16.0`

```console
$ docker pull kibana@sha256:3b77bcaf55f592c69075d718f3723142992f2daea464e9743aa1ce3b4bcdb118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kibana:8.16.0` - linux; amd64

```console
$ docker pull kibana@sha256:0e09b18d11b3f0427a7cfc3b0b538c8939fde06d136b094d06dc24d8406e89b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.3 MB (398289778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295afe00942995f7b94d26d2c4b234939dd39dac7a81cc3684a7cf730492be0f`
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
# Tue, 12 Nov 2024 13:42:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Nov 2024 13:42:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Nov 2024 13:42:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Nov 2024 13:42:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Nov 2024 13:42:14 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Nov 2024 13:42:14 GMT
LABEL org.label-schema.build-date=2024-11-07T12:08:23.851Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a8a07dfc586d78b8f4b7997b00e126363d68c043 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.0 org.opencontainers.image.created=2024-11-07T12:08:23.851Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a8a07dfc586d78b8f4b7997b00e126363d68c043 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.0
# Tue, 12 Nov 2024 13:42:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Nov 2024 13:42:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Nov 2024 13:42:14 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48575f852d90dc9890c291548141e4368edcde1d9540209cb3647dca3bd95545`  
		Last Modified: Tue, 12 Nov 2024 20:11:28 GMT  
		Size: 11.0 MB (10966613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebce24fd4223e12ee484744bad9746851dc3bea3da5e62e12fff134e87c6c62`  
		Last Modified: Tue, 12 Nov 2024 20:11:33 GMT  
		Size: 343.1 MB (343139903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e984c44cd176152a58f513ccd57215015e9f401eebfbdd7a16cab5cd29e055a`  
		Last Modified: Tue, 12 Nov 2024 20:11:28 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3efcd37b293ae22620877fd0dd1365f33c3588f891aac6ce7ec3434a0e6921`  
		Last Modified: Tue, 12 Nov 2024 20:11:29 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f20863855b3e74c7f26d004b1f714c1b31e416fb03bf063f727e0972a60be0`  
		Last Modified: Tue, 12 Nov 2024 20:11:29 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cadda25850bc7db6c596bc8fef8ae4d65b262f794ed4a27601d8827551e80f1`  
		Last Modified: Tue, 12 Nov 2024 20:11:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e07617db9fda9c7ec9664b8e078e84f6501f47d9dac6bd1176751b7cca3a5d9`  
		Last Modified: Tue, 12 Nov 2024 20:11:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33109392f44d70c349dd85597fdd8fab9977f04397d5ecb20c235046b6ba996c`  
		Last Modified: Tue, 12 Nov 2024 20:11:30 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9a3d430efa0803783c8670d2f30286b3437d67875cb93e4094b1037c2f59a9`  
		Last Modified: Tue, 12 Nov 2024 20:11:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bf2b2396d979456bfcc6997a047b65b9f6cb1bdbb51be0eb93321e9fcdc093`  
		Last Modified: Tue, 12 Nov 2024 20:11:30 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc909314cbeece0e478649c6769b78ef925ee95467f4e3bc2b2416674fa85345`  
		Last Modified: Tue, 12 Nov 2024 20:11:31 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.0` - unknown; unknown

```console
$ docker pull kibana@sha256:f42f16b975d3c65810220666fdfdc38d96fe81cadda3028d40d9a767a892706b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4441703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e388f22a19020dec902ef41bcf7e0a74b62cbac23530022e669303a69056ab`

```dockerfile
```

-	Layers:
	-	`sha256:9e106317a13e1976a4b2aefbbbf7737b526f195d1fd589551ceb3afefc002e06`  
		Last Modified: Tue, 12 Nov 2024 20:11:28 GMT  
		Size: 4.4 MB (4401060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afcbc7867368749e941252ec264cd89e731f2da8f0deb74c11f6f2d97a71780f`  
		Last Modified: Tue, 12 Nov 2024 20:11:28 GMT  
		Size: 40.6 KB (40643 bytes)  
		MIME: application/vnd.in-toto+json
