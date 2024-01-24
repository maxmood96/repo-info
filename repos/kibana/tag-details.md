<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.17`](#kibana71717)
-	[`kibana:8.12.0`](#kibana8120)

## `kibana:7.17.17`

```console
$ docker pull kibana@sha256:3741c53e9074a780b2496229806e3f332a86ce8e117c0774ea8667e075bd1cd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.17` - linux; amd64

```console
$ docker pull kibana@sha256:61334ca9796b8ad37164f608a9e64eff4d8e92c26cb1661c631ef063d3b54962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359682872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34e266f31715ede61a7425bbf3ae773939eec4ac93dc2f75f229cd974cd8bcd`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
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
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1614351bf9feaecee39654ef10374ca499d8e03d65bb54216b17aa0298f99b85`  
		Last Modified: Tue, 23 Jan 2024 20:52:02 GMT  
		Size: 12.3 MB (12271548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aede53604d6e919323bdcf3bf27ac86d6098c1e3528c68abec83e2175c77c07`  
		Last Modified: Tue, 23 Jan 2024 20:52:01 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466856ec2e311674456b263fc34530832cdef2064cdaacc628845edb4e7dcdc7`  
		Last Modified: Tue, 23 Jan 2024 20:52:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becb33ba173fb9f802d8f9e1b3cb2895640118ab384efeb3699e78e110f2b709`  
		Last Modified: Tue, 23 Jan 2024 20:52:02 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1604adc4c7e2c98d9472fa7af15e90efcbd832c163709034ebd5a70375b13c7d`  
		Last Modified: Tue, 23 Jan 2024 20:52:02 GMT  
		Size: 5.3 KB (5283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b90a258ac13374fbc1022162b7a53fffe9e35ebd6fe81cf8e087f076c68cd2`  
		Last Modified: Tue, 23 Jan 2024 20:52:11 GMT  
		Size: 303.2 MB (303226389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf965a3c859b9f5c0b5601a589a585d30b917f160d8023ef511ccacecb9cca6`  
		Last Modified: Tue, 23 Jan 2024 20:52:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f2ee62d036e622bb8b2e6b32e050ecdc5b63bed3c899621134cbf241becf18`  
		Last Modified: Tue, 23 Jan 2024 20:52:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08deb57ab8616218933a638bb312d2be1ecb2397f277221f6cb644dd4390b8f`  
		Last Modified: Tue, 23 Jan 2024 20:52:05 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c560993dbfab6c2d6c31fc988bc3bc656b3e2b24b6107212cf9ecdbb54cd76f`  
		Last Modified: Tue, 23 Jan 2024 20:52:05 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e28736ef059545ad2a66dc0cd88eae0c0f8b70f3271eb5f4df84d69add9f2ee`  
		Last Modified: Tue, 23 Jan 2024 20:52:05 GMT  
		Size: 189.4 KB (189406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8d3fd7dd82bb4584cbcaee00a7796312e529718b9978204c4d23b2300d20d`  
		Last Modified: Tue, 23 Jan 2024 20:52:06 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.17` - unknown; unknown

```console
$ docker pull kibana@sha256:41d5f44e5bb01158c47985a2c7ff89b93fa02e40ebbae4c0b28ea6a2827c61d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2f7796e8aa00e1f98edbac210ff349a7371672ef2c2862a42b17cfa371e0f8`

```dockerfile
```

-	Layers:
	-	`sha256:6118d90635c2ff1b84261435658eed561e5d4168ba7fe6779178fa9b8c9e9c2b`  
		Last Modified: Tue, 23 Jan 2024 20:52:02 GMT  
		Size: 3.0 MB (3032988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477128a9b9b09dffd4a20569ea172d0b42604787254ed3a6df1b206527657364`  
		Last Modified: Tue, 23 Jan 2024 20:52:01 GMT  
		Size: 44.4 KB (44363 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.17` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:039da7072ed45df68cc4be80e514865b7f8d9784f336fba36e36247d1ec571fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368593529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaa9f781e229ed8acea44a594e5263b2dfce5578467500c0636afe07e4d5ff2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
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
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b33c1a27bbb4c31c43eb167ae3df748361fefa96bbfa0dec48c68a4c1e33ca1`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 10.4 MB (10396649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98059de69b424d043bad0fbc3aa68baae6367fabf5f63704de018bfe92e97239`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae0f05ad9a7ff1532ceaf39932fb0b9a88a8de625669867c4f1e74135770c4d`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c897b19d6be892715b84b17db2bce8870bb544cd8aaa14b5d69487582a2542`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 16.5 MB (16460497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e8ede858fed3dc2c66c8f0b11d0b7b977202fc35ee37a2c50784b2b716f601`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff11673a3062ef6792b5b74d208ce14bf95358bb6181c20a974f286beac417c`  
		Last Modified: Tue, 23 Jan 2024 21:44:01 GMT  
		Size: 315.6 MB (315556350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746b20fb19be4d9b434d2c3153d67d29dae9efac65e22cec2aefdf8c138e5301`  
		Last Modified: Tue, 23 Jan 2024 21:43:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7a3715cf4e2fb60274d85ba1641f9a54bf362a77effee68a8c248cf989532`  
		Last Modified: Tue, 23 Jan 2024 21:43:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2010b8164377566c12296e2caea434ee4dc6b471d5a8f8f841663dc5a2eed383`  
		Last Modified: Tue, 23 Jan 2024 21:43:54 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788b6e373c9a375d8b67fcce52315bb464e740061fa93224b0484a3eae69c7a0`  
		Last Modified: Tue, 23 Jan 2024 21:43:55 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec71c63e4e93a26c161397366b453e569e598b46b8508c9fa90cdc32767563`  
		Last Modified: Mon, 18 Dec 2023 19:57:34 GMT  
		Size: 183.4 KB (183409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572a98f81b85282be763517ea848584b2ca5d57281db017ba5cebda656a49719`  
		Last Modified: Tue, 23 Jan 2024 21:43:55 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.17` - unknown; unknown

```console
$ docker pull kibana@sha256:4199858f98f069a71fc6d8288e24a7d002cfa24235422ba7979e9f0479050256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f7b1273e4eefae6f7816510b48da7a1c965856afed2701da80230f61d5f06c`

```dockerfile
```

-	Layers:
	-	`sha256:26cddd2e5d461b2757b2268c482c72a8e4027f959891254f68331c42b52c2b0f`  
		Last Modified: Tue, 23 Jan 2024 21:43:54 GMT  
		Size: 3.0 MB (3033325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:150711d90062ee1d1454c3f83119cfa8a20c941a1daf66955c428e0b051ca884`  
		Last Modified: Tue, 23 Jan 2024 21:43:54 GMT  
		Size: 44.4 KB (44367 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.12.0`

```console
$ docker pull kibana@sha256:7347237e0a282d7ab9f22d0b88ef38fed40058a384bfa7dac7c9b67e53ab8558
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.12.0` - linux; amd64

```console
$ docker pull kibana@sha256:fdcfab18908e65595a15789cba8527cf9e7d3a3a66c872b54a3bc7be13355e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372157422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308313df6bd00d528844241ffe410b435e70d9f563a9a9676ff1cefb713402a1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
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
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65134a0aa3d6e64463331b31ef3080cd7d1d121b24dfcb65d897bc82b103655`  
		Last Modified: Thu, 18 Jan 2024 18:15:47 GMT  
		Size: 10.9 MB (10914382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eac609b569123cfd58c739949cb3899933818d9b0f682e37d28a70e6287ff6b`  
		Last Modified: Thu, 18 Jan 2024 18:15:47 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d094a756a66ce2c8406f4b1990e32300371d9feacf66a6a7e7b037e43dfae129`  
		Last Modified: Thu, 18 Jan 2024 18:15:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da93aa1dd98af6492df9c72d92c431b5389468d1962fe3f41dd882a732e482f3`  
		Last Modified: Thu, 18 Jan 2024 18:15:47 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75d14a3a9212eca642bf7b758b41bb38ebf9a8bbc9c6441d7e523e77b3b6f99`  
		Last Modified: Thu, 18 Jan 2024 18:15:48 GMT  
		Size: 5.3 KB (5286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d00272e429fdd2c057c15c96af07675d65762c70b271edfdb07dcd478a4ed2`  
		Last Modified: Thu, 18 Jan 2024 18:15:53 GMT  
		Size: 317.1 MB (317058070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbebcfcfa33736abe562d098378714d13611f5bedc61dbe21116b5e07f0ec11`  
		Last Modified: Thu, 18 Jan 2024 18:15:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3baf9b3478cd6b8a8119503043588a1c24b16802fb90fbe60e7536f7e0de6f2`  
		Last Modified: Thu, 18 Jan 2024 18:15:48 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6880b0babb06f56c981a303d3009e26634e3e988119a25dcb18bc7df08c2a5f3`  
		Last Modified: Thu, 18 Jan 2024 18:15:49 GMT  
		Size: 4.5 KB (4549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3c8345c290c1c9d6566476629a1c47768afaf96ac15ffdf213b6783a0e299a`  
		Last Modified: Thu, 18 Jan 2024 18:15:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce09c1fc465e6a1552440e59140dd15281f31a8742c886e35d289ae54b3ffa0`  
		Last Modified: Thu, 18 Jan 2024 18:15:49 GMT  
		Size: 189.4 KB (189405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1270de2840b86192cba3afc04ae1dfe73ffd8f19f9f191cd66fbf0f917f09c9c`  
		Last Modified: Thu, 18 Jan 2024 18:15:49 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.0` - unknown; unknown

```console
$ docker pull kibana@sha256:e48766e8434428008d058d949cde9410d387913c05ba7ed3243952d87c2c2def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3518692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae68c800ba1997a0a563086f02464e5036e938f24ad5ca0a2ee20f6ba59b00d6`

```dockerfile
```

-	Layers:
	-	`sha256:3de4b4241cfb5539b5272396b95adfa09b3f5fbbe3e617c6af2e0af46b3a4782`  
		Last Modified: Thu, 18 Jan 2024 18:15:47 GMT  
		Size: 3.5 MB (3474341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04527e41178e911c3748a74d5293b1ca3a97827ab895b433a3063ddd1bb94947`  
		Last Modified: Thu, 18 Jan 2024 18:15:47 GMT  
		Size: 44.4 KB (44351 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.12.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:4a3b71615fd9ce17ca8cb041c458175d9101b4371f4d0784b5a1728901468286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.4 MB (382390836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3a0fb6e1d9e10ccb075bb0279c387fdefb3b429597ffc9691cee40477a7d2e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
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
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b33c1a27bbb4c31c43eb167ae3df748361fefa96bbfa0dec48c68a4c1e33ca1`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 10.4 MB (10396649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98059de69b424d043bad0fbc3aa68baae6367fabf5f63704de018bfe92e97239`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae0f05ad9a7ff1532ceaf39932fb0b9a88a8de625669867c4f1e74135770c4d`  
		Last Modified: Mon, 18 Dec 2023 19:57:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c897b19d6be892715b84b17db2bce8870bb544cd8aaa14b5d69487582a2542`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 16.5 MB (16460497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e8ede858fed3dc2c66c8f0b11d0b7b977202fc35ee37a2c50784b2b716f601`  
		Last Modified: Mon, 18 Dec 2023 19:57:32 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04e478a3edf69281604e69d438155015f806e4abb036635ba1ca8e0e9efa38d`  
		Last Modified: Thu, 18 Jan 2024 21:52:13 GMT  
		Size: 329.4 MB (329353611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a2e1479ef36b5030df1e4180dd8c023aae7cda5e29d8fd9ac56352b76b3fea`  
		Last Modified: Thu, 18 Jan 2024 21:52:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6d801b282977ee21d2343480873b9802e0ef5bb1fb7c20b1293af25ac79f38`  
		Last Modified: Thu, 18 Jan 2024 21:52:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea8fa24ad5595b1cf71dbfe958dfa545d5822486b03f4b728cdd4632250dcbb`  
		Last Modified: Thu, 18 Jan 2024 21:52:06 GMT  
		Size: 4.6 KB (4554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da914ecc505c91bb6ac92a9bc15a7767cd5abeb6e6bc8d8fdbe40343c3758002`  
		Last Modified: Thu, 18 Jan 2024 21:52:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec71c63e4e93a26c161397366b453e569e598b46b8508c9fa90cdc32767563`  
		Last Modified: Mon, 18 Dec 2023 19:57:34 GMT  
		Size: 183.4 KB (183409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b3663fe4bfb2057fdff0bd4804547711b28404549348b00564fbfb8f6acc09`  
		Last Modified: Thu, 18 Jan 2024 21:52:07 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.0` - unknown; unknown

```console
$ docker pull kibana@sha256:dd75bfc5fb4327b7f4de7f48323101c169c9ccf330575724dc9184b8dbbefc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3518877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a2306dbb626ec047685b2ae80519bc0bae25f19daa2025618b4d7546ec0799`

```dockerfile
```

-	Layers:
	-	`sha256:75e438da0fcb31e96544a02ee4825d50d97f26b932858e73c888f68066b2f5ba`  
		Last Modified: Thu, 18 Jan 2024 21:52:06 GMT  
		Size: 3.5 MB (3474682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0bd424a26ee22bfb2d5651312bd2348b9ee024e560dabee586316a05adb9cee`  
		Last Modified: Thu, 18 Jan 2024 21:52:05 GMT  
		Size: 44.2 KB (44195 bytes)  
		MIME: application/vnd.in-toto+json
