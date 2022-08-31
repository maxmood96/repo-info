<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.23`](#kibana6823)
-	[`kibana:7.17.6`](#kibana7176)
-	[`kibana:8.4.1`](#kibana841)

## `kibana:6.8.23`

```console
$ docker pull kibana@sha256:dd123d133fa7e995f83eef23df6aad30c589711e6171fee8db63097a7706eae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kibana:6.8.23` - linux; amd64

```console
$ docker pull kibana@sha256:adb468810c34ccc141f01ea79135d5a2f48d09890ecd08ce59ec94444f0a09f1
```

-	Docker Version: 20.10.10
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325750637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e174261beaec7ef8b8fc7e3df6b62b87e442f3451d408e7fe4525b151a061ebd`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Jan 2022 22:40:29 GMT
EXPOSE 5601
# Thu, 06 Jan 2022 22:41:30 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Thu, 06 Jan 2022 22:42:25 GMT
COPY --chown=1000:0dir:91d1ac171c4ceb98ce1764191b4bde36072fa18167199a2214eb559670a34b06 in /usr/share/kibana 
# Thu, 06 Jan 2022 22:42:28 GMT
WORKDIR /usr/share/kibana
# Thu, 06 Jan 2022 22:42:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Thu, 06 Jan 2022 22:42:30 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 06 Jan 2022 22:42:30 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jan 2022 22:42:31 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Thu, 06 Jan 2022 22:42:31 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Thu, 06 Jan 2022 22:42:34 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Thu, 06 Jan 2022 22:42:39 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Thu, 06 Jan 2022 22:42:39 GMT
USER kibana
# Thu, 06 Jan 2022 22:42:40 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.23 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Thu, 06 Jan 2022 22:42:41 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842e4249e10492c4ab35d3e76f93cad922781f7d61752e1b4b3ca25636b5c56f`  
		Last Modified: Thu, 13 Jan 2022 16:11:43 GMT  
		Size: 61.0 MB (61010271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f4609300d658bf52b006741f5590abdf93d8d575e0ddf04ce5be28e82b50a4`  
		Last Modified: Thu, 13 Jan 2022 16:11:58 GMT  
		Size: 188.6 MB (188638449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784cf3007996898653e12b85f6cf71597349b95377a60e1c57d40aaf682ddc3e`  
		Last Modified: Thu, 13 Jan 2022 16:11:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e291dafdd6a7112a1b18f88f42cbef2225094f58f18d2f364d0d34006b69e1`  
		Last Modified: Thu, 13 Jan 2022 16:11:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90f666fc9fbd62181b8b51f391386e0a1a137451605b6f0a105171abe51380`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8abc3a9f73c2948571140a610a8c9f79b87c33bcbfdf320cd0f6e5d9fbe944`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73634fb3f49af52529a1b025a3cebf50531fdbcbdb3876b7b00908dfe9dc0a85`  
		Last Modified: Thu, 13 Jan 2022 16:11:29 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.17.6`

```console
$ docker pull kibana@sha256:ae5a501355903443b6cc7ff4a3af2dd76ba73f986d0612014b8370cd04bb6da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:7.17.6` - linux; amd64

```console
$ docker pull kibana@sha256:a031b02cd029ce22abed498362f4ebbcd63cc8fc7bc364e95de7ceeb5eb1dfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325453183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4239c3f5bd3d17a8a64cde246ea36e3329effe834ac38e3151f9279ec4fff004`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Mon, 22 Aug 2022 11:31:20 GMT
RUN EXPOSE map[5601/tcp:{}]
# Mon, 22 Aug 2022 11:31:20 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 22 Aug 2022 11:31:21 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Mon, 22 Aug 2022 11:31:21 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Mon, 22 Aug 2022 11:31:22 GMT
RUN RUN /bin/sh -c curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Mon, 22 Aug 2022 11:31:23 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Mon, 22 Aug 2022 11:31:23 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Mon, 22 Aug 2022 11:32:25 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 22 Aug 2022 11:32:25 GMT
RUN WORKDIR /usr/share/kibana
# Mon, 22 Aug 2022 11:32:25 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 22 Aug 2022 11:32:25 GMT
RUN ENV ELASTIC_CONTAINER=true
# Mon, 22 Aug 2022 11:32:25 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Aug 2022 11:32:26 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 22 Aug 2022 11:32:26 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 22 Aug 2022 11:32:26 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 22 Aug 2022 11:32:27 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 22 Aug 2022 11:32:27 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 22 Aug 2022 11:32:27 GMT
RUN LABEL org.label-schema.build-date=2022-08-22T11:05:33.075Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d2647b053b769d4517fbb14ce37765808a1b6e0c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.6 org.opencontainers.image.created=2022-08-22T11:05:33.075Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d2647b053b769d4517fbb14ce37765808a1b6e0c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.6
# Mon, 22 Aug 2022 11:32:27 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Mon, 22 Aug 2022 11:32:27 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Mon, 22 Aug 2022 11:32:27 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4909e7eae242ddcd04ea4cac57905cde860307c129f881473a17640f26c77c22`  
		Last Modified: Wed, 24 Aug 2022 23:34:31 GMT  
		Size: 11.4 MB (11402602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d6fb24c0886259a755e922a95303529eb029e1832db71f8a14982cfba201`  
		Last Modified: Wed, 24 Aug 2022 23:34:29 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcaf4a9c0882e6eb369888122a32f1f3ff9c9c17fe4d43d5115afcd3be4d69b`  
		Last Modified: Wed, 24 Aug 2022 23:34:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338bcf0d330658b4a5060ae46689eb526ad90811fe9fe3a5dad5f423052b025c`  
		Last Modified: Wed, 24 Aug 2022 23:34:28 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af5505a20feb5f0627a99c2f926ba87c2c8de93c16ad5ce60b2fb05fde4e38e`  
		Last Modified: Wed, 24 Aug 2022 23:34:27 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe77eb249d6ffdbb9ace2b8c472e6601e48fa6eae4b6c3e6ab4a52560ff4d4d0`  
		Last Modified: Wed, 24 Aug 2022 23:34:58 GMT  
		Size: 268.8 MB (268805804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25728b71e5a44fc7a4e2eded91557b5d50399f103c7d69bb69c4d711242bc7b`  
		Last Modified: Wed, 24 Aug 2022 23:34:26 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35830107ab914645b77f72703837b4845d46e2ea9e789ecd0e2a785aff4715f1`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1209f693487452a4793e8fcab07dd4e8d085bd70ba07bc66e042cf4ad7be65`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 4.5 KB (4509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb27ec66f047fd0c1c30851d2089ce1dedb11fc081f75efd80c5a1026a583a9`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6216454c4b6e809c3de959f46e320085ee49f81831ffbf88f3dacd31f32d1da1`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 189.4 KB (189390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9baec0471caba7ed8badff4bb66852efdf363c69411b328a0e2cf26ea0b1971d`  
		Last Modified: Wed, 24 Aug 2022 23:34:24 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:7.17.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:009a1aac9f56bd44888ab033a9f7c59845aefa182ca764877ab45009a25fc5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338517103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b0941d8c060d54a324a9dcb750eedc6f6e5fe7d247160e6dffd84d924ff77c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Mon, 22 Aug 2022 11:34:32 GMT
RUN EXPOSE map[5601/tcp:{}]
# Mon, 22 Aug 2022 11:34:32 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 22 Aug 2022 11:34:34 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Mon, 22 Aug 2022 11:34:34 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Mon, 22 Aug 2022 11:34:38 GMT
RUN RUN /bin/sh -c curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Mon, 22 Aug 2022 11:34:38 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Mon, 22 Aug 2022 11:34:39 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Mon, 22 Aug 2022 11:35:40 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 22 Aug 2022 11:35:40 GMT
RUN WORKDIR /usr/share/kibana
# Mon, 22 Aug 2022 11:35:41 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 22 Aug 2022 11:35:41 GMT
RUN ENV ELASTIC_CONTAINER=true
# Mon, 22 Aug 2022 11:35:41 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Aug 2022 11:35:41 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 22 Aug 2022 11:35:41 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 22 Aug 2022 11:35:41 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 22 Aug 2022 11:35:42 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 22 Aug 2022 11:35:43 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 22 Aug 2022 11:35:43 GMT
RUN LABEL org.label-schema.build-date=2022-08-22T11:05:33.075Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d2647b053b769d4517fbb14ce37765808a1b6e0c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.6 org.opencontainers.image.created=2022-08-22T11:05:33.075Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d2647b053b769d4517fbb14ce37765808a1b6e0c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.6
# Mon, 22 Aug 2022 11:35:43 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Mon, 22 Aug 2022 11:35:43 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Mon, 22 Aug 2022 11:35:43 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd40621629c438532eea92191837d0b33bf9a9723296a3ba24bc5d2c65f5206b`  
		Last Modified: Thu, 25 Aug 2022 02:10:43 GMT  
		Size: 11.2 MB (11235723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffa1dada9fbb499bbaee1ea95ea74e7d3d22d7b0083708ea9b238c47ed9e67e`  
		Last Modified: Thu, 25 Aug 2022 02:10:41 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47665c1ab65b80afa553144f99db53f5674e6944231ff774bf86edfb5d48fadf`  
		Last Modified: Thu, 25 Aug 2022 02:10:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d302b8066a42a7de4b005648be9cfa2f9fbed4fedd4231d6b4390f6fc01c93f1`  
		Last Modified: Thu, 25 Aug 2022 02:10:40 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2f75aefff3d84203de2b23fb7c8d77eb2ae9317ee0cf9b939f7e658f6a0e98`  
		Last Modified: Thu, 25 Aug 2022 02:10:38 GMT  
		Size: 5.3 KB (5295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f5af82b89cea04c1b92ca87f916b546dd42a2c8a09e25016575601be6fbf12`  
		Last Modified: Thu, 25 Aug 2022 02:11:14 GMT  
		Size: 283.4 MB (283423810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a1ca11cb812a2cecfbffd7bcab0ee97dff1b936273aa486ff0627afabaa6a9`  
		Last Modified: Thu, 25 Aug 2022 02:10:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be289adf6ffa9e50dd4e9a9e1d04f0ce3f3ad3f9163dfd549c025458750faa0`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983daadcd4e22eb300b6d99c7087d1c6f00d10a3e9965a02d5d870427e9f98da`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43daa7054f14326442b8e1880957a36ad9255b3cd0cfc2d12198b14f0e7af20`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e57cde9f2bfc25283f648cae139da69a696537aa26288a3ea8f34b0b82e23f4`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 183.4 KB (183396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c001dea654d707e36e6a5180ad98399546b091c076ad6e5dbdc93e67cb13ba`  
		Last Modified: Thu, 25 Aug 2022 02:10:36 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:8.4.1`

```console
$ docker pull kibana@sha256:3f73f7b286c1821f4c238497ed972bbcc3d1b2796da8a660b15f8a891b7c2d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:8.4.1` - linux; amd64

```console
$ docker pull kibana@sha256:34c4b719b1946512378cdd78d04adb82c1e711794815c37f5780377be880c401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342515924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349611cc26a40726252faff8faab4b066361560cf804a19763db4df8d00bd1d7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Fri, 26 Aug 2022 11:36:43 GMT
RUN EXPOSE map[5601/tcp:{}]
# Fri, 26 Aug 2022 11:36:43 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Fri, 26 Aug 2022 11:36:44 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Fri, 26 Aug 2022 11:36:45 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Fri, 26 Aug 2022 11:36:45 GMT
RUN RUN /bin/sh -c curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Fri, 26 Aug 2022 11:36:46 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Fri, 26 Aug 2022 11:36:46 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Fri, 26 Aug 2022 11:37:52 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 26 Aug 2022 11:37:52 GMT
RUN WORKDIR /usr/share/kibana
# Fri, 26 Aug 2022 11:37:53 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 26 Aug 2022 11:37:53 GMT
RUN ENV ELASTIC_CONTAINER=true
# Fri, 26 Aug 2022 11:37:53 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 11:37:53 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 26 Aug 2022 11:37:53 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 26 Aug 2022 11:37:53 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 26 Aug 2022 11:37:54 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 26 Aug 2022 11:37:54 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 26 Aug 2022 11:37:54 GMT
RUN LABEL org.label-schema.build-date=2022-08-26T11:09:11.482Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=415cecc1c67ed775c4d9f6592fe5acc35dc9dce5 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.4.1 org.opencontainers.image.created=2022-08-26T11:09:11.482Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=415cecc1c67ed775c4d9f6592fe5acc35dc9dce5 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.4.1
# Fri, 26 Aug 2022 11:37:54 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Fri, 26 Aug 2022 11:37:54 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Fri, 26 Aug 2022 11:37:54 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e973c653758933938ea0ec2a4edc790462992c3c1801ee6045549e53f377ca`  
		Last Modified: Wed, 31 Aug 2022 13:48:25 GMT  
		Size: 11.5 MB (11463684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4d6ff1beeac8dc119e4090106dc759b6585bb66e345e515243bfb70c03beab`  
		Last Modified: Wed, 31 Aug 2022 13:48:20 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab0b3cd95607c397d950444f054332419d00e8faa7bf7b9db746a22ec215ef4`  
		Last Modified: Wed, 31 Aug 2022 13:48:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f4f8050d5be9a13f11d8739cf60fa7e272da94015f7aec807077a0ce04ae20`  
		Last Modified: Wed, 31 Aug 2022 13:48:19 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49268f2195f1f00c478fbea5bd5a906cec2f8bb3220f637c69704789de3fd58`  
		Last Modified: Wed, 31 Aug 2022 13:48:15 GMT  
		Size: 5.3 KB (5280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ba5efa5762c0aa2968d0736e5e26cdbdd3f1c2eff8c9b31788aae23cb55976`  
		Last Modified: Wed, 31 Aug 2022 13:50:39 GMT  
		Size: 285.8 MB (285807609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d26e95fdf35dca2948dedd8a46908028649c12d960a20c663257fce72bcfc8`  
		Last Modified: Wed, 31 Aug 2022 13:48:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b40291f3a1a6b8c511c5033cc5a88230e547b0f78e43c562e0b0fa81fc7f6`  
		Last Modified: Wed, 31 Aug 2022 13:48:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ec8393dfdb0def8286cf95fe418bf0fad1a809dc6f22e2405f4350adbd4e15`  
		Last Modified: Wed, 31 Aug 2022 13:48:10 GMT  
		Size: 4.4 KB (4381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3163e2a0ae6926d37ee4837e052285e6453e5f9c506b4344c2b7172bce78e`  
		Last Modified: Wed, 31 Aug 2022 13:48:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3123f742516bc10de385e9cefcdb38d15eef5cf45c27cc23fb3e6a25b9b07171`  
		Last Modified: Wed, 31 Aug 2022 13:48:11 GMT  
		Size: 189.4 KB (189392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc56b0650e1dbd3cdc7806e6ba89b2d2b33a8b82881e7aab08ca0b37beb6c28`  
		Last Modified: Wed, 31 Aug 2022 13:48:10 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:8.4.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:6a343cf56eff1f836da44c0b60e837b680ae5a9a70e0b2e3c64b3fadd67210dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355621001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63714b2b0452ab49f5144ee6ec3758c8c3c55b7aab0b3facc19564b2b56813ae`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Fri, 26 Aug 2022 11:39:57 GMT
RUN EXPOSE map[5601/tcp:{}]
# Fri, 26 Aug 2022 11:39:57 GMT
RUN RUN /bin/sh -c for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Fri, 26 Aug 2022 11:39:59 GMT
RUN RUN /bin/sh -c set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Fri, 26 Aug 2022 11:39:59 GMT
RUN RUN /bin/sh -c mkdir /usr/share/fonts/local # buildkit
# Fri, 26 Aug 2022 11:40:02 GMT
RUN RUN /bin/sh -c curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Fri, 26 Aug 2022 11:40:02 GMT
RUN RUN /bin/sh -c echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Fri, 26 Aug 2022 11:40:03 GMT
RUN RUN /bin/sh -c fc-cache -v # buildkit
# Fri, 26 Aug 2022 11:41:09 GMT
RUN COPY /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 26 Aug 2022 11:41:09 GMT
RUN WORKDIR /usr/share/kibana
# Fri, 26 Aug 2022 11:41:09 GMT
RUN RUN /bin/sh -c ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 26 Aug 2022 11:41:09 GMT
RUN ENV ELASTIC_CONTAINER=true
# Fri, 26 Aug 2022 11:41:09 GMT
RUN ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 11:41:09 GMT
RUN COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 26 Aug 2022 11:41:09 GMT
RUN COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 26 Aug 2022 11:41:10 GMT
RUN RUN /bin/sh -c chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 26 Aug 2022 11:41:11 GMT
RUN RUN /bin/sh -c find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 26 Aug 2022 11:41:12 GMT
RUN RUN /bin/sh -c groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 26 Aug 2022 11:41:12 GMT
RUN LABEL org.label-schema.build-date=2022-08-26T11:09:11.482Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=415cecc1c67ed775c4d9f6592fe5acc35dc9dce5 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.4.1 org.opencontainers.image.created=2022-08-26T11:09:11.482Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=415cecc1c67ed775c4d9f6592fe5acc35dc9dce5 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.4.1
# Fri, 26 Aug 2022 11:41:12 GMT
RUN ENTRYPOINT ["/bin/tini" "--"]
# Fri, 26 Aug 2022 11:41:12 GMT
RUN CMD ["/usr/local/bin/kibana-docker"]
# Fri, 26 Aug 2022 11:41:12 GMT
RUN USER kibana
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46c7df7ac0a0d80193e38c72adc2891bfd2e248269956a3d2b9dc92060e6849`  
		Last Modified: Wed, 31 Aug 2022 19:34:39 GMT  
		Size: 11.3 MB (11302199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801bf796e5655b140c6b378754a58a6c0c1032073e183769f9bb3bf10393d5f3`  
		Last Modified: Wed, 31 Aug 2022 19:34:37 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d524be1a17f1952d2dca2506ea481e2f91d6adbe0252c339224c87f6ba6c042`  
		Last Modified: Wed, 31 Aug 2022 19:34:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ca07e4e65d32a620bc6546c42a697ddc2bba1d2a3a34cc12b09ab582bfa1a2`  
		Last Modified: Wed, 31 Aug 2022 19:34:37 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31a9d8ab938bf0296471209c7563bafbf6347267958b025f0c30d5d6fe4247`  
		Last Modified: Wed, 31 Aug 2022 19:34:35 GMT  
		Size: 5.3 KB (5290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c934a7f750f48869514408f6b1781661a607377927dc773cd2455fc69b15f1`  
		Last Modified: Wed, 31 Aug 2022 19:35:13 GMT  
		Size: 300.5 MB (300461370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed4a7c989eea59dc8a297720bb5e181e9e2ca4045376ec3e2df216eaf1a820`  
		Last Modified: Wed, 31 Aug 2022 19:34:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08513b328d47433a31f75b9e8c594b93c736f41c9f32fb1d01c4ad8656fe556`  
		Last Modified: Wed, 31 Aug 2022 19:34:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbc39f492d117805a0e87820da3b6582a1a2f35191da2d6293d08e14250f6cb`  
		Last Modified: Wed, 31 Aug 2022 19:34:32 GMT  
		Size: 4.4 KB (4380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79d33e94b05ceb90fe9e344c1f7ac777024c72ff83c3ec476076e773e9952a2`  
		Last Modified: Wed, 31 Aug 2022 19:34:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29861786639ad2966b1f3c3333ca417dfd378de95c1ac3d78b6df676d4855aaa`  
		Last Modified: Wed, 31 Aug 2022 19:34:32 GMT  
		Size: 183.4 KB (183396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2441c9227f8a3966396be3c46b6b3222ff311c2b909fc2208c1ddc76b2c1cb7c`  
		Last Modified: Wed, 31 Aug 2022 19:34:33 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
