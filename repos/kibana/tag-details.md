<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.22`](#kibana71722)
-	[`kibana:8.14.1`](#kibana8141)

## `kibana:7.17.22`

```console
$ docker pull kibana@sha256:778cd745a5b22cd72ab1e5b636bcdbea754b6974967ef4cff8deb4077cebfc28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kibana:7.17.22` - linux; amd64

```console
$ docker pull kibana@sha256:48bb8b46801cc88b510cb4326eab5f4a93ae5d648b0467843089ce962d8cccf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.3 MB (361306259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a027d69b0b250eaccb984647fae574053bef375b949b09182021db7809b105f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 13:25:43 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Jun 2024 13:25:43 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Jun 2024 13:25:43 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Jun 2024 13:25:43 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 13:25:43 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Jun 2024 13:25:43 GMT
LABEL org.label-schema.build-date=2024-06-05T11:07:35.640Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=43696930d77d3bb567e445624874eab9cf363872 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.22 org.opencontainers.image.created=2024-06-05T11:07:35.640Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=43696930d77d3bb567e445624874eab9cf363872 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.22
# Thu, 13 Jun 2024 13:25:43 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Jun 2024 13:25:43 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Jun 2024 13:25:43 GMT
USER kibana
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b8ca19b57abb8b74c75cdef0f6c8f2d11a46675f6910488864ffa33e236558`  
		Last Modified: Thu, 13 Jun 2024 18:30:37 GMT  
		Size: 10.7 MB (10705117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4aeb5ed077fb5b2f10388ece711771197ec3c1254333c12b8de56209e7c8139`  
		Last Modified: Thu, 13 Jun 2024 18:30:37 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497d352b8c5bbca6eaf17657c581dd330fb302cd8154579277a296d3d3ef9ff1`  
		Last Modified: Thu, 13 Jun 2024 18:30:37 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d1ed5a7ccf7c36b0d5148da4d708ffabbf70097ab3dbcbb9f7a9aaeba4487c`  
		Last Modified: Thu, 13 Jun 2024 18:30:37 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dbb6288e3ccbd5eb0802178b1650a9084df53bc01d40abf825c0ab47d0e185`  
		Last Modified: Thu, 13 Jun 2024 18:30:38 GMT  
		Size: 5.3 KB (5287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb748dbaf286558f0449ecab795b90e5cbf3168ae81591f2177f4f08ce03a4b7`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 306.4 MB (306417423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904762bb586b1ed1175a4b636415f59b3b07880ba9360fae01c133aad15ff344`  
		Last Modified: Thu, 13 Jun 2024 18:30:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a7797c818cab799321431e727a2a9969269681d861f0a4b61a70b9b65b7bb0`  
		Last Modified: Thu, 13 Jun 2024 18:30:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf9cc991a8eaa8e987955e151475d8a2fe8d109477fbf33c371e214028d4a27`  
		Last Modified: Thu, 13 Jun 2024 18:30:38 GMT  
		Size: 4.5 KB (4512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4030300a4a392a3bbc5be2ce7ff30bf2aa192c7bd5adfb938dde64823100c7ef`  
		Last Modified: Thu, 13 Jun 2024 18:30:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a9af8199fe9bdf4f23cb70d8012fe765f0041fa999f9d2e2532351ec660ff8`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 189.4 KB (189433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d808047390f7f4a45c11e99d904011bbd152668704efd20c88b4c23e06085b`  
		Last Modified: Thu, 13 Jun 2024 18:30:39 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.22` - unknown; unknown

```console
$ docker pull kibana@sha256:d28529b09b4afea546dfba529709e867d751cb823c3fdc36a54605f81231d415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3334622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50e6fc35c36b036524608ab5e723c2d89af1ec2ab624907ed8739e6da8771fb`

```dockerfile
```

-	Layers:
	-	`sha256:b4c2c4619153faacbeba6b899a2f0a60dd9defd97d43597054d011e03ba235f6`  
		Last Modified: Thu, 13 Jun 2024 18:30:37 GMT  
		Size: 3.3 MB (3290367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e96fbbf98ae7d3632c3d1c18a994b221699308976e01c06b3f93df2a560176`  
		Last Modified: Thu, 13 Jun 2024 18:30:37 GMT  
		Size: 44.3 KB (44255 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.14.1`

```console
$ docker pull kibana@sha256:fb4a2e06dfa175c17b839788825d31883eaabd2d6296be96c03ce6418a0d8dfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.14.1` - linux; amd64

```console
$ docker pull kibana@sha256:1af206e6b8c22d214aa9dfc729dcdc492b2854386e59f87157c907b0d8d6dca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 MB (394989149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdea2e4cfba487c7f5401176e93da3101b491abbe4da68b44f16d1802f7379f4`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 13:14:46 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 12 Jun 2024 13:14:46 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN fc-cache -v # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
WORKDIR /usr/share/kibana
# Wed, 12 Jun 2024 13:14:46 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Jun 2024 13:14:46 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 13:14:46 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
LABEL org.label-schema.build-date=2024-06-11T00:21:28.765Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=afbd904e868f2a48a2bbeb8ff20baee8d4aeb468 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.14.1 org.opencontainers.image.created=2024-06-11T00:21:28.765Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=afbd904e868f2a48a2bbeb8ff20baee8d4aeb468 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.1
# Wed, 12 Jun 2024 13:14:46 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 12 Jun 2024 13:14:46 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 12 Jun 2024 13:14:46 GMT
USER 1000
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ccfe615a24a78582887b5ca44ec33064146af58321bc7245b5f1839f02af3d`  
		Last Modified: Wed, 12 Jun 2024 17:59:00 GMT  
		Size: 10.7 MB (10705201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dcd1c7ae467db81d03ecf27010199380adda039c6a80ae403a2628daf18a69`  
		Last Modified: Wed, 12 Jun 2024 17:58:59 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d2259cbbd2c93ed3986bb80f5546d91920587c945ab5b8693806bcdd023ce8`  
		Last Modified: Wed, 12 Jun 2024 17:58:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e870b3acdde41c6f41c499d697f541c15d2ca6a7d74accfd8e4dfa6823d32a7`  
		Last Modified: Wed, 12 Jun 2024 17:59:00 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a50c94af494e40bd025cfef1f99e23f66d17124fed3b410110e9ecbf4bf771`  
		Last Modified: Wed, 12 Jun 2024 17:59:00 GMT  
		Size: 5.3 KB (5295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cac297ddcfe97ad61c633a510be932b5f47d42c28437f89056771622328cdd4`  
		Last Modified: Wed, 12 Jun 2024 17:59:07 GMT  
		Size: 340.1 MB (340100141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086d1ac207052df9edc75bbed4f37e92dee7b688034ea08aaf181ba2c65033d3`  
		Last Modified: Wed, 12 Jun 2024 17:59:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8e7dc0f99f35d75da9fbd68b782b5dfd95cf04164ba17f2f9c6dd7ae3bf08`  
		Last Modified: Wed, 12 Jun 2024 17:59:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd75dd5880504bb1418c22116f67b38e711a9f88402b90c17c7d3ac9dc34992`  
		Last Modified: Wed, 12 Jun 2024 17:59:01 GMT  
		Size: 4.6 KB (4589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d3c8e7fa5560f63a08acf899d646abd9452e69e16b28108abda099d18a5c07`  
		Last Modified: Wed, 12 Jun 2024 17:59:02 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb61cf4bc1fa1c897bebd7d4089ee73670be989bfbcb8d09d3351e023685d92`  
		Last Modified: Wed, 12 Jun 2024 17:59:02 GMT  
		Size: 189.4 KB (189433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bfae460dafd2302119c84b8973c8397f21409391d2b13b0f161612c4bf4a05`  
		Last Modified: Wed, 12 Jun 2024 17:59:02 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.14.1` - unknown; unknown

```console
$ docker pull kibana@sha256:3fa6e0b91bdbe124957ad144c8beade31a8f1483ebbdc1128bb6d6283e3c9662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dbcb90f6bb1464441b3ff014e37923a3d2f95f055138d84bb161c32a02e41c`

```dockerfile
```

-	Layers:
	-	`sha256:50d3a4dc6d574babebb75738324d1a3ac0eb9b8fb866ff97059adc3e8a1a2ccc`  
		Last Modified: Wed, 12 Jun 2024 17:58:59 GMT  
		Size: 3.8 MB (3786996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62344a25bb26d73d719a73c76be99c6140c2986d6f8c2ae1d43d335ef0765843`  
		Last Modified: Wed, 12 Jun 2024 17:58:59 GMT  
		Size: 44.2 KB (44244 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.14.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:b813bf38f3fa5c832de297273f7ec72c02c951c05792fd814e9a700cdde6596b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.0 MB (405951666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695d2bd1c2a652f04532ceb48a135a0d16fffa06d264f24713fe6cf03cff0f7e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 12 Jun 2024 13:14:46 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 12 Jun 2024 13:14:46 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN fc-cache -v # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
WORKDIR /usr/share/kibana
# Wed, 12 Jun 2024 13:14:46 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Jun 2024 13:14:46 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 13:14:46 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 12 Jun 2024 13:14:46 GMT
LABEL org.label-schema.build-date=2024-06-11T00:21:28.765Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=afbd904e868f2a48a2bbeb8ff20baee8d4aeb468 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.14.1 org.opencontainers.image.created=2024-06-11T00:21:28.765Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=afbd904e868f2a48a2bbeb8ff20baee8d4aeb468 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.1
# Wed, 12 Jun 2024 13:14:46 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 12 Jun 2024 13:14:46 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 12 Jun 2024 13:14:46 GMT
USER 1000
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dd30ab58335cfc64b8644d22d1edf54b10726a5dd7eb89ff73ee78013860a`  
		Last Modified: Wed, 05 Jun 2024 16:01:43 GMT  
		Size: 10.6 MB (10550719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395764de8c16ca9fdf511b85693276262681625012db63283350548fb437524d`  
		Last Modified: Wed, 05 Jun 2024 16:01:43 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3687c8f64db803aba5cbbdd491fb195b22f7771198fced7b8167373e2ba0d617`  
		Last Modified: Wed, 05 Jun 2024 16:01:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab0c1d5f43e5ebd3d0f4cdff9ceb5aefa40137e177b9517e2383c2ec0c82f99`  
		Last Modified: Wed, 05 Jun 2024 16:01:44 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409b485e7538528aec5d9dd7a45870c294c0784478c9884441494df4431da66f`  
		Last Modified: Wed, 05 Jun 2024 16:01:44 GMT  
		Size: 5.3 KB (5286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798a50dcca3b101183ee61259c7b2eb681bf4dd665b31eca8aabe9b971171b47`  
		Last Modified: Wed, 12 Jun 2024 18:39:54 GMT  
		Size: 352.8 MB (352761149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81d160f6cbf18e9ae0375cf395b02d0e6f6681beb25bf64fcfffa2df394ff1a`  
		Last Modified: Wed, 12 Jun 2024 18:39:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd44b9b6dc0ae83a6f9723e27a86de45ecd318137e5ff4df0744874bd236c426`  
		Last Modified: Wed, 12 Jun 2024 18:39:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0825bb4695344abc9888c4265aee93137bf2bf28076e39393e4736b8c6aedc`  
		Last Modified: Wed, 12 Jun 2024 18:39:46 GMT  
		Size: 4.6 KB (4588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe4cc42b9d23a37f2c1bc660ef3a38584d4449a88e3b86cc717d7c4b75d8893`  
		Last Modified: Wed, 12 Jun 2024 18:39:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9857a80288b1e7330fd7d3c833a9aa1df38c9a722a52796dee4a4835ef22b9`  
		Last Modified: Wed, 05 Jun 2024 16:01:47 GMT  
		Size: 183.4 KB (183420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024d20979bc2f341a7b525c71960f6fbce23951a423ac2fb63e1bd01e73adb14`  
		Last Modified: Wed, 12 Jun 2024 18:39:48 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.14.1` - unknown; unknown

```console
$ docker pull kibana@sha256:9952154949dc5ecaf03c51ba1f0e14fa324c0122f6bcfc0967e6367186600ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec683e77e7389b1225898c63b6bbef4baa63c29ba8f5b7f346bf57779d7034e`

```dockerfile
```

-	Layers:
	-	`sha256:b50293bb1c452f9e86dd45a470724b17602d758429bfbfa06d05540edf1ee32e`  
		Last Modified: Wed, 12 Jun 2024 18:39:47 GMT  
		Size: 3.8 MB (3787246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9450b97ed1e848a1de05085047f7d2cb06d8e10b4c417668f276ca700e549b02`  
		Last Modified: Wed, 12 Jun 2024 18:39:46 GMT  
		Size: 44.5 KB (44508 bytes)  
		MIME: application/vnd.in-toto+json
