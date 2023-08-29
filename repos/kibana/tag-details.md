<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.11`](#kibana71711)
-	[`kibana:7.17.12`](#kibana71712)
-	[`kibana:8.8.2`](#kibana882)
-	[`kibana:8.9.0`](#kibana890)
-	[`kibana:8.9.1`](#kibana891)

## `kibana:7.17.11`

```console
$ docker pull kibana@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `kibana:7.17.12`

```console
$ docker pull kibana@sha256:e718974b8ff5e1aee9c37e04dfe4309ddbde151a629b7734f724d000979b7386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:7.17.12` - linux; amd64

```console
$ docker pull kibana@sha256:8f5502f17ad75b8de7997632d4198c9f5681e41ca4bf17acf2f77053329b5b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332901377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e08aea2289529a218960b4d42110b3ac01a302e5d88e3791a24a5252b08db9e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 11:39:57 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 20 Jul 2023 11:39:57 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 20 Jul 2023 11:39:58 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 20 Jul 2023 11:39:58 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 20 Jul 2023 11:39:59 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 20 Jul 2023 11:40:00 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 20 Jul 2023 11:40:00 GMT
RUN fc-cache -v # buildkit
# Thu, 20 Jul 2023 11:41:04 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 20 Jul 2023 11:41:04 GMT
WORKDIR /usr/share/kibana
# Thu, 20 Jul 2023 11:41:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 20 Jul 2023 11:41:04 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 20 Jul 2023 11:41:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jul 2023 11:41:04 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 20 Jul 2023 11:41:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 11:41:05 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 20 Jul 2023 11:41:06 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 20 Jul 2023 11:41:06 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 20 Jul 2023 11:41:06 GMT
LABEL org.label-schema.build-date=2023-07-20T11:13:46.772Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=47018eedac59fbc169e961fe698501adf762ebb1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.12 org.opencontainers.image.created=2023-07-20T11:13:46.772Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=47018eedac59fbc169e961fe698501adf762ebb1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.12
# Thu, 20 Jul 2023 11:41:06 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 20 Jul 2023 11:41:06 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 20 Jul 2023 11:41:06 GMT
USER kibana
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0143f1f7907395b9cca587735b83407cc2e8a4c201ce3ee02cacae4f097da5f1`  
		Last Modified: Thu, 03 Aug 2023 07:21:00 GMT  
		Size: 10.5 MB (10531751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba4d34e03dbb35e2d8af7ad950f5f7342fee5e3f6235b705ce03dd9abf3aca4`  
		Last Modified: Thu, 03 Aug 2023 07:20:56 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432971d798a1d17ee3f6f8a3dccc94f6eb9b4022fbcbd62531fa533e049e3b5e`  
		Last Modified: Thu, 03 Aug 2023 07:20:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826b7c71d2b50e6a447e48b3371f478ef46209a39bfd7540f95b7b9d3d148ab6`  
		Last Modified: Thu, 03 Aug 2023 07:20:55 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b4f78551b9251f89ab00ab45e68e976b5d3a0abe213397fc72aa3db475426c`  
		Last Modified: Thu, 03 Aug 2023 07:20:51 GMT  
		Size: 5.3 KB (5284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a746e82542e6a9323753301044f2b3dae14b62f705cacc645323ae48b37116fa`  
		Last Modified: Thu, 03 Aug 2023 07:21:50 GMT  
		Size: 277.1 MB (277117442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8abbd297d9036c7e562b372749bc31a93aeb2b262b3b36f235947019f6f0fb6`  
		Last Modified: Thu, 03 Aug 2023 07:20:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe3d899ca78128086721e4db8bbe3d9f1cd05774b732e37164e824980fcc93e`  
		Last Modified: Thu, 03 Aug 2023 07:20:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b66e77191012ca036b83a7a83bfc4b26f2553f0709db99683153760b7824046`  
		Last Modified: Thu, 03 Aug 2023 07:20:45 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2c47381f7f9f94bd7ff2425c86eee08388e46ff076980194f9d26b8ef6c755`  
		Last Modified: Thu, 03 Aug 2023 07:20:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940e527b10fe1c9b0673a5c879cf459e4205ee1c76c01e30dae60e88a466ccaf`  
		Last Modified: Thu, 03 Aug 2023 07:20:46 GMT  
		Size: 189.4 KB (189403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1ab67e8374104d29dd5f10eb846c169c03a78fc63ce8d372947dbf08715d55`  
		Last Modified: Thu, 03 Aug 2023 07:20:45 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:7.17.12` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:107913c9dad08a114f1575425589a34c3f7c7ed0cfa22b9519b3091ffcc15c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.1 MB (344114365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7791082bc7ef5a7c1360529847038db421283f0153de25473057df4cf60b8e0c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2023 11:43:08 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 20 Jul 2023 11:43:08 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 20 Jul 2023 11:43:10 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 20 Jul 2023 11:43:10 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 20 Jul 2023 11:43:13 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 20 Jul 2023 11:43:14 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 20 Jul 2023 11:43:14 GMT
RUN fc-cache -v # buildkit
# Thu, 20 Jul 2023 11:44:18 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 20 Jul 2023 11:44:18 GMT
WORKDIR /usr/share/kibana
# Thu, 20 Jul 2023 11:44:18 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 20 Jul 2023 11:44:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 20 Jul 2023 11:44:18 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jul 2023 11:44:18 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 20 Jul 2023 11:44:18 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 20 Jul 2023 11:44:19 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 20 Jul 2023 11:44:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 20 Jul 2023 11:44:20 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 20 Jul 2023 11:44:20 GMT
LABEL org.label-schema.build-date=2023-07-20T11:13:46.772Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=47018eedac59fbc169e961fe698501adf762ebb1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.12 org.opencontainers.image.created=2023-07-20T11:13:46.772Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=47018eedac59fbc169e961fe698501adf762ebb1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.12
# Thu, 20 Jul 2023 11:44:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 20 Jul 2023 11:44:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 20 Jul 2023 11:44:20 GMT
USER kibana
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b026f2633e8633ef54f64abfa3087743718ac8b5499d88825dae438efcce5bf2`  
		Last Modified: Wed, 23 Aug 2023 23:51:39 GMT  
		Size: 10.4 MB (10398607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049f7f15308338ebed7d1dd30890da226fbf72b01f5d167db563e02633ec82e0`  
		Last Modified: Wed, 23 Aug 2023 23:51:38 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f385685c28e815026bdcba6b6ff58c53b57ddd162f0461b04e1d97977c4f6496`  
		Last Modified: Wed, 23 Aug 2023 23:51:36 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc53bfa04011f0870a37ad7819565dabfb1d05ba0405fb8d8010f52dd3676486`  
		Last Modified: Wed, 23 Aug 2023 23:51:37 GMT  
		Size: 16.5 MB (16460497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e65beae18c72362b6d1a0131ad7eba4d24e7acddbcdb424c031db71a6da3f00`  
		Last Modified: Wed, 23 Aug 2023 23:51:36 GMT  
		Size: 5.3 KB (5305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b98aa52a73eae55cb4c10f3cccbb3ea001af476c7ea6af942d01e349ee826`  
		Last Modified: Wed, 23 Aug 2023 23:52:00 GMT  
		Size: 289.9 MB (289851627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b3d52315889d0e914ffbae265d3b7a2ba5ea03da067c13be4857f9215320f8`  
		Last Modified: Wed, 23 Aug 2023 23:51:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd89cfe4f774c241a4f31fea35610da347507531cca60f63d7a18ba9eb894595`  
		Last Modified: Wed, 23 Aug 2023 23:51:33 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12da41ed3fc38ec822af8947f590733ba3f473261761df88f6ea90266549d8c8`  
		Last Modified: Wed, 23 Aug 2023 23:51:33 GMT  
		Size: 4.5 KB (4507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1abf5cc06834f1543df047ff7dd3519fee8882f295e7a9a30caaedd309cadfe`  
		Last Modified: Wed, 23 Aug 2023 23:51:33 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82924918fcbbca2611b439867e20e1d5024a66ac78238bb482e9ea3adfc0b729`  
		Last Modified: Wed, 23 Aug 2023 23:51:34 GMT  
		Size: 183.4 KB (183410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec13a2968aeb71b6d40e4c26a68a83620308ea5414c075f3e5625342fb9fa5a`  
		Last Modified: Wed, 23 Aug 2023 23:51:33 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:8.8.2`

```console
$ docker pull kibana@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `kibana:8.9.0`

```console
$ docker pull kibana@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `kibana:8.9.1`

```console
$ docker pull kibana@sha256:55b0e7901b78f0a2c59b7a6acdb4d0d5421f9b72cfb4d33afe3ecb91538965cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:8.9.1` - linux; amd64

```console
$ docker pull kibana@sha256:3a3bac2d884657129822e522fd2f456cd7475bd4cbe9d7db13c469160ffe72bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343163570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992f03cc5c663100029a7818535a9caddf94da792a73057f3e94b7b0b96a1290`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 10 Aug 2023 11:44:24 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 10 Aug 2023 11:44:24 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 10 Aug 2023 11:44:25 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 10 Aug 2023 11:44:26 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 10 Aug 2023 11:44:27 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 10 Aug 2023 11:44:27 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 10 Aug 2023 11:44:27 GMT
RUN fc-cache -v # buildkit
# Thu, 10 Aug 2023 11:46:13 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 10 Aug 2023 11:46:13 GMT
WORKDIR /usr/share/kibana
# Thu, 10 Aug 2023 11:46:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 10 Aug 2023 11:46:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 10 Aug 2023 11:46:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Aug 2023 11:46:13 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 10 Aug 2023 11:46:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 11:46:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 10 Aug 2023 11:46:15 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 10 Aug 2023 11:46:15 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 10 Aug 2023 11:46:15 GMT
LABEL org.label-schema.build-date=2023-08-10T11:12:21.350Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c664aeb22673e6eb42348ea50b5a098509f7deb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.9.1 org.opencontainers.image.created=2023-08-10T11:12:21.350Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c664aeb22673e6eb42348ea50b5a098509f7deb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.9.1
# Thu, 10 Aug 2023 11:46:15 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 10 Aug 2023 11:46:15 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 10 Aug 2023 11:46:15 GMT
USER kibana
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09a7dcdf63551a1cdd9174be4037d5d066156e76cbeaf703cd62baae7431209`  
		Last Modified: Tue, 22 Aug 2023 11:27:58 GMT  
		Size: 10.5 MB (10531728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820fd54045415801a41ede90b3dd4748edc980ab365f61cf43a99089039da14b`  
		Last Modified: Tue, 22 Aug 2023 11:27:52 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e923868ab4e74b6d7bea32f5cf99b55147974d0753c0d5b820584b015f82987d`  
		Last Modified: Tue, 22 Aug 2023 11:27:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937439e66d39c33066570d860b2660cabd30713048c94269c258a15370a65063`  
		Last Modified: Tue, 22 Aug 2023 11:27:55 GMT  
		Size: 16.5 MB (16460478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc1893edb389e776a0340691e5ede940ba3ffc17eef7bc5877f64bfa2333d25`  
		Last Modified: Tue, 22 Aug 2023 11:27:51 GMT  
		Size: 5.3 KB (5295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1f1dcfc301aa06a9bb889d27a2a2b7c4f9bb4e1830e15fbef43948ab5ef311`  
		Last Modified: Tue, 22 Aug 2023 11:28:45 GMT  
		Size: 287.4 MB (287378964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609e16529d15a4fd5a1d9060143e0dc098ab6c0472d93c44b851ba3568c776ef`  
		Last Modified: Tue, 22 Aug 2023 11:27:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6210b874ea81511685340326e314e8d8ea977c6d66c1a814d0e387a632a973eb`  
		Last Modified: Tue, 22 Aug 2023 11:27:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c48db6ec4ff158ae04334ed3bc7c30641c709ab00a6a9fa2f4b6d6ded8cff6`  
		Last Modified: Tue, 22 Aug 2023 11:27:48 GMT  
		Size: 4.5 KB (4534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d083525a8a1771f24ca6c1ee28c9d1c33f4c8fe14982683abddc3f29966485bc`  
		Last Modified: Tue, 22 Aug 2023 11:27:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31128be7b8490ce968f9d2da98b04ae5ca11c6d2edbaba63ef9aee0be32cb83`  
		Last Modified: Tue, 22 Aug 2023 11:27:46 GMT  
		Size: 189.4 KB (189404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf45bc5bdad1d6d09b3c260d48290c8b019f7ecd72b23ecc22cf5c49df899e34`  
		Last Modified: Tue, 22 Aug 2023 11:27:45 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:8.9.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:8bce3552bfabb189e43eb7029a78fa94862c39d840320811d7dcef202267774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.4 MB (354404814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ec32117c7fa00601908f029efaa8b80f68048cab342e33190562e73fd83cef`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 10 Aug 2023 11:48:27 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 10 Aug 2023 11:48:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 10 Aug 2023 11:48:29 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 10 Aug 2023 11:48:29 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 10 Aug 2023 11:48:32 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 10 Aug 2023 11:48:32 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 10 Aug 2023 11:48:33 GMT
RUN fc-cache -v # buildkit
# Thu, 10 Aug 2023 11:50:16 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 10 Aug 2023 11:50:16 GMT
WORKDIR /usr/share/kibana
# Thu, 10 Aug 2023 11:50:16 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 10 Aug 2023 11:50:16 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 10 Aug 2023 11:50:16 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Aug 2023 11:50:16 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 10 Aug 2023 11:50:16 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 11:50:17 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 10 Aug 2023 11:50:18 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 10 Aug 2023 11:50:19 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 10 Aug 2023 11:50:19 GMT
LABEL org.label-schema.build-date=2023-08-10T11:12:21.350Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c664aeb22673e6eb42348ea50b5a098509f7deb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.9.1 org.opencontainers.image.created=2023-08-10T11:12:21.350Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c664aeb22673e6eb42348ea50b5a098509f7deb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.9.1
# Thu, 10 Aug 2023 11:50:19 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 10 Aug 2023 11:50:19 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 10 Aug 2023 11:50:19 GMT
USER kibana
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5e28530761a55e9d926dddef2ebe4013be57b54e383529ed76bb50b9fa8f4c`  
		Last Modified: Wed, 23 Aug 2023 23:50:57 GMT  
		Size: 10.4 MB (10399360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b33318ff6867fdef4b83ade627aea2929ce8d3701b3b3902038745fa2e32d3`  
		Last Modified: Wed, 23 Aug 2023 23:50:55 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966b4291d9f8d6a9bb5c83ffad2c62344d38d82c480af7769e7db3f242cbf23`  
		Last Modified: Wed, 23 Aug 2023 23:50:54 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731d9759a702db144c3ffb3629859b07f52ecdf77677edd22502fe6fdc08c448`  
		Last Modified: Wed, 23 Aug 2023 23:50:54 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2d2ecc8eabb2c0a8fbe313da1b92f270f0ded3bf6303f6978b2ec181e0943a`  
		Last Modified: Wed, 23 Aug 2023 23:50:53 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ca61f702b8950870f2036bed47aa2faa3a67deceaf3792285e25354a0f8756`  
		Last Modified: Wed, 23 Aug 2023 23:51:22 GMT  
		Size: 300.1 MB (300139083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508c397e3dc4412a9efbfebcb6ae737a10ab6c95817de7d98d2a32bcd4895cc5`  
		Last Modified: Wed, 23 Aug 2023 23:50:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c294d68c7c4e0ca1b11183f7fdfdda66bb68560de929892dfe56474f87a32aaf`  
		Last Modified: Wed, 23 Aug 2023 23:50:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0603c781426e778ddf1091da210725f3e2c163d5328bb2cdfa3cff6f67283df2`  
		Last Modified: Wed, 23 Aug 2023 23:50:51 GMT  
		Size: 4.5 KB (4538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c58637fd46d7e7320031365c11642216584a9df834559bd8f5ff8b4c7776f7b`  
		Last Modified: Wed, 23 Aug 2023 23:50:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9fd8fad3601c1e7762e5dfc3f42e7b981251691255c5a62647ea51cbfa6415`  
		Last Modified: Wed, 23 Aug 2023 23:50:50 GMT  
		Size: 183.4 KB (183408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9166da551c08d45324244cb2753f49f90ee679b42371616c5c571947072807bb`  
		Last Modified: Wed, 23 Aug 2023 23:50:54 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
