<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.22`](#kibana71722)
-	[`kibana:8.14.2`](#kibana8142)

## `kibana:7.17.22`

```console
$ docker pull kibana@sha256:834864700792e3a228b6ddf9313f53cd1a156b435714c30677a67f47eca4eb2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
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

### `kibana:7.17.22` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:122e8e068280e8225d59645db1778b1be8a93470272518bc18f2243338860e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372243396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc77103cdcedaa9f900a2d5242c868e155cbd118a4377c302e4d17423183fe6`
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
	-	`sha256:aff5ab6ad1db83d7f533a122075cb8972361358cf03c7316b0dda3a712eb84b0`  
		Last Modified: Fri, 14 Jun 2024 03:42:17 GMT  
		Size: 319.1 MB (319052955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965bf714641fcc7b9f0b8e5ba43d0b6a9396fbd7922e21c619655e1f43bb89f1`  
		Last Modified: Fri, 14 Jun 2024 03:42:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9367756c12b173dc050a25f2f57b1bb09407c8a0df7299b3fd1f2edc1d281b5`  
		Last Modified: Fri, 14 Jun 2024 03:42:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7c57a8cb3d40d7eee847df86d03dafd0e4fe01986025fccec70cdd8b052afb`  
		Last Modified: Fri, 14 Jun 2024 03:42:10 GMT  
		Size: 4.5 KB (4512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2410ee9da48c74055aa1410814ad550d960d6cf647fd0aeeba14b60c388a431`  
		Last Modified: Fri, 14 Jun 2024 03:42:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9857a80288b1e7330fd7d3c833a9aa1df38c9a722a52796dee4a4835ef22b9`  
		Last Modified: Wed, 05 Jun 2024 16:01:47 GMT  
		Size: 183.4 KB (183420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faec4c7660f32efd3fb1ab1846bd376e515fb11976472bfcc100b953af6e4c`  
		Last Modified: Fri, 14 Jun 2024 03:42:11 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.22` - unknown; unknown

```console
$ docker pull kibana@sha256:637321968384ee40f079bf55c1ab15cda6b7bf0cd5b2ac40825d33b3c7eeec23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3335137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f5877e014fa6231072b6c0f57a81693aa8140fee2372474e9d7c476af8752b`

```dockerfile
```

-	Layers:
	-	`sha256:578743d98ea7952de0c1ffa7f6e0cee5e76e41e55559555c30efe7555d228421`  
		Last Modified: Fri, 14 Jun 2024 03:42:10 GMT  
		Size: 3.3 MB (3290617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67910ce6f831d0bb3c41ffdf95794cf1951d0ab9892504a6e6c6b2119bba5699`  
		Last Modified: Fri, 14 Jun 2024 03:42:10 GMT  
		Size: 44.5 KB (44520 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.14.2`

```console
$ docker pull kibana@sha256:bf8ef448a383670beb55d73b063e21576c2c912313ec343e869db4ce8daee18f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.14.2` - linux; amd64

```console
$ docker pull kibana@sha256:3fefed28e69fd8978795cc7881d4bed478837d03f388423d86d1332b222e4e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 MB (395042934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb109bda9a5413576174ffca6583b26a06a6dcbe276e2dc8c820b5bfed0574e`
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
# Thu, 04 Jul 2024 07:59:16 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 04 Jul 2024 07:59:16 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN fc-cache -v # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
WORKDIR /usr/share/kibana
# Thu, 04 Jul 2024 07:59:16 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 04 Jul 2024 07:59:16 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 07:59:16 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
LABEL org.label-schema.build-date=2024-07-01T18:11:39.861Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=50d89958910ab6fa9b8c4f4f40c53e89ad6dbbe1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.14.2 org.opencontainers.image.created=2024-07-01T18:11:39.861Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=50d89958910ab6fa9b8c4f4f40c53e89ad6dbbe1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.2
# Thu, 04 Jul 2024 07:59:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 04 Jul 2024 07:59:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 04 Jul 2024 07:59:16 GMT
USER 1000
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50232bd1023f2627631ac8250e107ff0f2f2bb3ce7df322817844ea7345a080`  
		Last Modified: Mon, 08 Jul 2024 18:01:24 GMT  
		Size: 10.7 MB (10705210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b861bb377d67d2f3c0fbab08c2f07cf773f182b7411f1634c011cebb894a8a9b`  
		Last Modified: Mon, 08 Jul 2024 18:01:24 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a062ffa75acb24f5cb153ead61aff4cf60348876db6ab1ae3d20fb916262b0bd`  
		Last Modified: Mon, 08 Jul 2024 18:01:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d502242b76a60bd5d4bfaa2ab359e7c9c554c545018c0f9e2d8e1ff5da9afc75`  
		Last Modified: Mon, 08 Jul 2024 18:01:24 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41caa611d49004ca014a5478fdcddca9af56381428d7a2dee41d322a024566ce`  
		Last Modified: Mon, 08 Jul 2024 18:01:24 GMT  
		Size: 5.3 KB (5293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a71dff16b6762b3ff56ef697084de609cc1903449f2e47fff682d6ad9eeaa3`  
		Last Modified: Mon, 08 Jul 2024 18:01:29 GMT  
		Size: 340.2 MB (340153662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155fc407d6068259ec0f38e93f68be520b364f323e84f04303fe16fe10dce331`  
		Last Modified: Mon, 08 Jul 2024 18:01:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c0fee4ed6c37d553b134251cf340613c2832c333c65fce4b3e513d5d70e87`  
		Last Modified: Mon, 08 Jul 2024 18:01:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc1564fe66f8926ceac22e7a5bef4b546cb81f1f79fb8bc0c1252b08d3811ad`  
		Last Modified: Mon, 08 Jul 2024 18:01:25 GMT  
		Size: 4.6 KB (4596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae91dfd4c2e323c7d5113e0f594b8a32270449662dffbbca5a8dc6590654c8d3`  
		Last Modified: Mon, 08 Jul 2024 18:01:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91d40307b0ef37e55638dcff1dcbe9e7b640282efa705e4ebd5ff1dcbc6db20`  
		Last Modified: Mon, 08 Jul 2024 18:01:26 GMT  
		Size: 189.4 KB (189433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15187c91ec6648aa08a4817a755dab175bce8f6f79e954aa4f9290504fcc31b9`  
		Last Modified: Mon, 08 Jul 2024 18:01:26 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.14.2` - unknown; unknown

```console
$ docker pull kibana@sha256:9f62c7a28cb2be58e95686118001c994f94a89483c80076ff7ea7f9277dac871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf89f30cb31a97dea1bb78eaa7ee802368688e8c47df55134a0974b4bb9c9f8`

```dockerfile
```

-	Layers:
	-	`sha256:d70ac07c2a35dc6dd0798e93f74c32c4c68b0a0c8c3da328b8a5b0282592b0f7`  
		Last Modified: Mon, 08 Jul 2024 18:01:24 GMT  
		Size: 3.8 MB (3809687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656ffd4f653ebcee5fcbee1a314ca9fb23f069f3781139b7f8b89923b32b5880`  
		Last Modified: Mon, 08 Jul 2024 18:01:23 GMT  
		Size: 44.2 KB (44243 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.14.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:44702430d0637f98b769fcbe88e4d79dbec22b80da80309babf0635a16c66db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.0 MB (405984793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3843414189f8c04250825dbf28940650261491fb4266bd9eabf912b3770fa8d`
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
# Thu, 04 Jul 2024 07:59:16 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 04 Jul 2024 07:59:16 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN fc-cache -v # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
WORKDIR /usr/share/kibana
# Thu, 04 Jul 2024 07:59:16 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 04 Jul 2024 07:59:16 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 07:59:16 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 04 Jul 2024 07:59:16 GMT
LABEL org.label-schema.build-date=2024-07-01T18:11:39.861Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=50d89958910ab6fa9b8c4f4f40c53e89ad6dbbe1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.14.2 org.opencontainers.image.created=2024-07-01T18:11:39.861Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=50d89958910ab6fa9b8c4f4f40c53e89ad6dbbe1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.2
# Thu, 04 Jul 2024 07:59:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 04 Jul 2024 07:59:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 04 Jul 2024 07:59:16 GMT
USER 1000
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6e081d1b0fe95c95ce18ad6737677671a8252899edd1a552628d8aa4588ed`  
		Last Modified: Mon, 08 Jul 2024 18:46:06 GMT  
		Size: 10.6 MB (10550816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff931329e939e36c97b8fd1b2b92a4b300e0efb44153085eab7a3204f9b53371`  
		Last Modified: Mon, 08 Jul 2024 18:46:06 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c808741b8a9f60dcc3352acfeeaa2a996c000ed5a6d914dad16b46439f5e69b5`  
		Last Modified: Mon, 08 Jul 2024 18:46:06 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5325506853020476d39f03096bda3b7c2ead8af07516cccc585fc1b6fa228a74`  
		Last Modified: Mon, 08 Jul 2024 18:46:07 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd62849130771c2421ea7ada13d4a382bd818b768049864d4f1867a90ca7098`  
		Last Modified: Mon, 08 Jul 2024 18:46:07 GMT  
		Size: 5.3 KB (5285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2150e493f8d952f5d255bf470586e889c3a2f16a90083f6bdd5c3952af5254`  
		Last Modified: Mon, 08 Jul 2024 18:46:15 GMT  
		Size: 352.8 MB (352793920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9629b919119d619dc075f68849f0540ad32a4480e5e3ff58caada696b70d8e4`  
		Last Modified: Mon, 08 Jul 2024 18:46:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f337427b554c8c366b316403e467001d8b248ef5a37b495e2af4b128e71f855c`  
		Last Modified: Mon, 08 Jul 2024 18:46:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac80b6445482ea1f59e9cf1aa94213290aa9740b69437943f45c9d77f8eab860`  
		Last Modified: Mon, 08 Jul 2024 18:46:08 GMT  
		Size: 4.6 KB (4596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d66c8ceed54580889fece17808570f063be916e52c2bc0f001e7c00b12ad79a`  
		Last Modified: Mon, 08 Jul 2024 18:46:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bceec0cc05e71bc4aee4161fd7f8a99878f509563bc12e8ba3ae1374f211b25`  
		Last Modified: Mon, 08 Jul 2024 18:46:09 GMT  
		Size: 183.4 KB (183420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c0658f3615dd37c33affacc037054341634536632f6d03a3bdea8d128424fd`  
		Last Modified: Mon, 08 Jul 2024 18:46:09 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.14.2` - unknown; unknown

```console
$ docker pull kibana@sha256:e3bb1dea2dd8974d7ecaeba99c353aad9f820e70cef9c214e7f555c8f6bcef48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e326999575a13a9b8e3f41d8971c903cdd4a8b557c31da92ca9e8026e1d8c2a5`

```dockerfile
```

-	Layers:
	-	`sha256:aecb251356a4239707fcc34ab6399059bf2dda344ee980db9e33a7c95620afc3`  
		Last Modified: Mon, 08 Jul 2024 18:46:06 GMT  
		Size: 3.8 MB (3809937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5e807b519539e4adac48539c358bb4537ad23a64b11fe6b3a8e55779720d44`  
		Last Modified: Mon, 08 Jul 2024 18:46:06 GMT  
		Size: 44.5 KB (44508 bytes)  
		MIME: application/vnd.in-toto+json
