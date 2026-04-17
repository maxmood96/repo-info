## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:e602ceca19bddc3dd7197b4b1afde53a16cd9d31a5500a8ae5620f36cb01963c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:16179be8b1ec51f6e587273a8f77f42773ea1f12228ad777764d971e7b43c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9559d6064637f63c271167a9d7c010ff5364b1eec2b0208599b50488ba703d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a1e64c52df3467627e6d1c644bcb8211343cd68dddf6166bdffbccaf244fd`  
		Last Modified: Fri, 17 Apr 2026 00:15:33 GMT  
		Size: 7.1 MB (7102043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029b2f91063f4996b4cd7e46a633ab1a441fa1b56b1f99ed0b8451abeca076cb`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d704923a1249776a808f8aeafbe1adf7092d06b738b33f076cad79dcad5cf25`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ca41342c8a71a1155058491c46bc3acc5e7cdb6651860972e62fb3c748ab050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7c6232cacba47988be2ed2b963902987d654145e91fa75e175f098bdbdb14`

```dockerfile
```

-	Layers:
	-	`sha256:dc14f6b45ffd0cf094851f620d7c09a23513353217e1640bd80f9752ae64eb67`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:46f43a77c9d9be15ca3b2787d01a7fc76c0ad5c1f84b62acdfe9c75bdf2364cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5fcf3af1aec5f8186371ced026734b0dc358f81fd79977d24923f55da091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52664fd029115b59e10665beb1de4db22437397f1e12d9ef21a10227a4bcb0b3`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 6.8 MB (6821275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a63f62b766f87fc00d415fb393198a177ca29d74ef894de1081a534644c51f`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42627bd4fc0b9abb95a7fe4472894e86dac74bcfafc35397fe46a8b51863a24b`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:02712ae3dfd268f7c0f286d515e88ffd04661bd2afa30df5ef55d8c1251c2d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc157db9d7cfbdfb06f25ffab6be682d8f329dbd5cb945f440a0b934ff633ae`

```dockerfile
```

-	Layers:
	-	`sha256:3921d54fa2bad5abd1ccb3ba03fdde77fb3342fb0c2f5f4ae861e1142b27e559`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:dc95c9071c61ae217f8b7ccc6c6cc4ed7135efd907ab216185d7a046f848263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edceff3cd31a9ba3c0916ec5a29e6f96072c9da161efff71263cdbd8bb621fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3ef39893803a1aa71385b7b4a0e2f2489c1714926ebc5a17f0f283f992c574`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 6.8 MB (6812139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05c0dd84c92bf393d4eeb2e08cb836caae1367d08914ed39ee6012bc7979eb`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5b69ca76cd026d2a3a3104034ad0bcde0f0a1ff1a54e334a1d5f2b7aa2ce0`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a096ab49bf85fe59d54ca81110922ea5bdd2e0d348e69d0f6025e938b39f26b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af01ae40e078b504a99160d21be1719bf0893debfd46c721e0f3f1b5fb2b8d88`

```dockerfile
```

-	Layers:
	-	`sha256:23e4cd5325bfcff95bbb97f89ba5f6e6dc0407032e7c0fb1cde3ad1ac6830a7b`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb1c336dc892313409a8a9be0bd058eeb502231aa3383b448d862253abe72660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10653076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7263323b7691f6bfc1ce77845e1493322e0a7fb05848ba9496d17994e3c358`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ff6f42514787c192e710db9db418be359224a6173e1237a72689ab899901a`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 6.5 MB (6510214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb42c58d7e11c558e5072fdac886e2e8d5119360c8339777bf525f6b3de3be`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5a1bbeb5c096e363e206a3d729f50c23ae559b4b3d9fea208d0b170b4864d`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a80cf61114fd852a49cc7cc405df6566531f25fb08f1698e38110bd13b16bcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1eea64ca314ff49953a4d62c6f57c8921b550e4a65eef8447cab8789dafa98`

```dockerfile
```

-	Layers:
	-	`sha256:f96940dabf37dc5e896241d7598fd3bf014ea2f2dec81a8253215bce6dd38616`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:53b58d1e5ac5757d0090c9c82d6b43c4fa3983e2af4ada84b96a6431d7a6cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412c201b02e670a6c66daff1a839dbf8949e02fd7bab2be04cea5c1e0c738e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:02 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ed90b89f0799173e6fccc22fecf8ff6c8973c8ed4ff1831c68a7c7569b4cd`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 6.6 MB (6560526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac41c2bd3722584f61f21b39d46ec42523bd6ea86f211b9027e5acf3135de9`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49b420d0d646e4990b9696c25668a04fb23ae54be76f6897fbd49eae67b24c`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:35462817b467f61ebceb4eca3c0ac8d23fbdee1ba0b903f77d995d769a172ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729ef5c8fed43aecc14c5a725ab776840e1a16f702f8496ef3b696338d2f4d3`

```dockerfile
```

-	Layers:
	-	`sha256:822b657516851096b98cd62907a761f8ccbbb44813254a0078eb31d4f272c619`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:8dd0bb86b226ee0c00b11bee7e5402a505865da642006ff14293d14912b11e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10596317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033c7f5d89abe8c752cd0bceac3d04d00854284c008645ba31f91ef04652287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7537aff86e4637878e5664a942467243a0f2cd0f3724bad313542c288b66619f`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 6.9 MB (6941474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c98718326853d62529f33a4745f08a21999d45bddc49bf4d4175feb2bd9c49`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b57122821a0589eb6f05dc704b4f828e3060b27f5c6eeec2cad9b5b52bf3c`  
		Last Modified: Fri, 17 Apr 2026 00:13:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6a1b0dd4f10ca2f0dcfcd22ebcb04999217fcbf87ad066c7993d2a45e3970490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0a8646f0475362f0b87ffe0fba73b5631df8220475194d2849b657ea3b049`

```dockerfile
```

-	Layers:
	-	`sha256:a85160fd978747e6ebfeae736628c48024e7b74f2f00bc194d8b8fb7b1c81552`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json
