## `nats:alpine`

```console
$ docker pull nats@sha256:26f5f314d531efd9fc6857781f0c09a57f6e1881991c2e68ebb226d019762017
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

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:f55092a58ef4b6883fd9b9e67c8741139c3701acff2d7e57930abbb54d2d4478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10886061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81529466020c291e5ad80f56987ed653d491e1b9476ccbdeaf67b72affa3c278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:34:38 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:34:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8887a98e8249b73b0777bfbc8c0a30b02d3c21e3c39a9d768c5871b5585777`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 7.1 MB (7080215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dead58ebc17268f1b2f4cec215f560e3a07cc610d28eeff77d5f1c5d8e2517`  
		Last Modified: Mon, 09 Mar 2026 18:34:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b4cd24f67b5d5afe059593810655b6887ba69dbdb160f71907e3daca8a8dc`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:685e730f881ec97c5e115e96bfe8066a26a611e53bcbfa4f0e69d4b4a174b46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb00ece4ca5cf51cc4d452e9249450fed5b54cfe2a9112947dca28d2ea8dbfc`

```dockerfile
```

-	Layers:
	-	`sha256:e0a3ba67a28104834d1d93b1e7e33ff17be9085f62d4b1100860816af7c9e0de`  
		Last Modified: Mon, 09 Mar 2026 18:34:42 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c7bf3f984b3b64f0c1f9f4674a8f76c32e17a58c3a69291ad03b749fb8275ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10303789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52985b6ab22ea9e18f31378c7d723405b36c8533ab7e35049e80e606ec5042e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:48:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:48:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:48:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148f12e063d142770b6e05b9f9c2ab014ab5763dff5f40cf43b4d8741dea20e0`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 6.8 MB (6797772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb32797a1c1b66b3d5d82193923eb3b39bbd560af58c01e71d7f46127eda32c`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c38be02f7f6968455354dfe4a4a05e5f20fbcdad07b63a3add2b522b3fc163`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7f5278fc819e312da44d7f8c6548fbd4f008b7047b81aaec0c88e1b6e7bf80d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbf1a9035fbf11bd94daf97ff6446b8c962f779e52915fdb47f723375a90161`

```dockerfile
```

-	Layers:
	-	`sha256:d069f32f6e0103cf7962bc3e50c1be2b0953ab9edcfb7db9f63defe80ce6c7b2`  
		Last Modified: Mon, 09 Mar 2026 18:48:34 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:de66d6fac8ce8ebef0e1032f68c75720b2d9fe3a040132c69bce4613ae04a5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10016287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb89708d609d7d7c02e11f18dbd6f2ebbd095aee4402d8d2d9a9c4ca7917e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:52:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:52:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:52:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4627631ba1918c54c7a3365b569389ba221a3fcbd467f2f68c02834aa91cc94f`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 6.8 MB (6791688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1909a283e1b0f458613bac969dccdc3e622f3167995890a9b73344d1afe42e0c`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dc1d6c83015eb80bc6e00a18fd3fe4b50483b56a1b8d381db8551986ad949e`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a89cb4125128c4481995506bc126626436c2a4398b4d1ca640b05c513c9c3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576436877db30f3cde211a66a4c4013292cae5b6f4cdcba857a0f440e84397a8`

```dockerfile
```

-	Layers:
	-	`sha256:c681f3aa2919334b313a7f825221815da8a74b0c5717aece45a141747c4666a4`  
		Last Modified: Mon, 09 Mar 2026 18:52:16 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ce72c5047aac010d13d69e087e2ef792ba483b581d3fe131a06f24f4bcd64499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10629509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78db93426f4ce81493b1740958536016471acce7c2469d30642d1ce5e2505028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 18:36:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 18:36:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 18:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:36:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825bb7632b2910036c4e99446261eaccf38a5407182667a9a5544165b29a3a66`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 6.5 MB (6489020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a075238f2783d207491918f497c4935823239fef8402991a1501e453f6dba`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e51ee93c455d52b0a680fe79d12a069061e5d506026beeda5e511a4b3221a49`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6803835c0dc24ce636ea74af20236401d626a7086072c838f1bdc957a100b7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0389309d70c5e974ba909c72462ccaecc37686be93ec78f5b3f4ec005cb0760b`

```dockerfile
```

-	Layers:
	-	`sha256:3c6a9525024c9f083b6bf1027d0683e9da385aa15944aa3dd296418810f297b6`  
		Last Modified: Mon, 09 Mar 2026 18:36:06 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:242d9dc765cb5b612c1758d0600274f601af275d3c7e593b61ac7f9296d5de33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0cd1feec1da5b6b7fa386873251c01f31ca6b27979b4fbe1a1bf7ce6755479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:35:04 GMT
ENV NATS_SERVER=2.12.4
# Wed, 28 Jan 2026 02:35:04 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.4
# Wed, 28 Jan 2026 02:35:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='44a6ff34eff7e8d0e1409dbac0b733cff7ecbb4f19388a4d0d3d6085d899f017' ;;     armhf) natsArch='arm6'; sha256='4e59df78e00edb75544aac70e1e99008cd97a039fad6ea1942b7986ee7289245' ;;     armv7) natsArch='arm7'; sha256='67e7708005b615d1b63280c752616ff8663fa8bd3e83bb24890905b9a0a4e789' ;;     x86_64) natsArch='amd64'; sha256='92388f2e4aa1e6dea402eb173cbdb1fcb1df9a9c899cb807b91ddbb45c131b65' ;;     x86) natsArch='386'; sha256='0899515b18dcbfba3572e91ea0bf7b7577a00d102ca91be44840a8a1ad68b4d7' ;;     s390x) natsArch='s390x'; sha256='8c084d41b8ef405c31ff75f84bb03028295001f9741724a8d0fb2c28aa0f3690' ;;     ppc64le) natsArch='ppc64le'; sha256='5b073b7cdfb91b30f226a687311193ce4544700eaf69fd32df2809451e9e5fc0' ;;     loong64) natsArch='loong64'; sha256='e58995ac0402050a0bd6a9513fc144e9f8f6bb01224fdeb5476691cad187a1c7' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Wed, 28 Jan 2026 02:35:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Wed, 28 Jan 2026 02:35:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 28 Jan 2026 02:35:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Wed, 28 Jan 2026 02:35:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84147a59d31c7f9c2780a1992852c031b75236cb0e89f49ce197a35821de105f`  
		Last Modified: Wed, 28 Jan 2026 02:35:14 GMT  
		Size: 6.5 MB (6519029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03fac75cf7049455170e27923866db34d10a3d5c26add784969ae48cac5db20`  
		Last Modified: Wed, 28 Jan 2026 02:35:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5323a65f58a6a07cd25cdbe725d5c311647f7832b17a39964619fb826889ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:13 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:64cae85877a781a6a3715811f47721796595030701518ba5feaf6dedb9f2a343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a462304addd89cc67ed0881e5e574ccdee34a1e1cc3fdd3422cc619877067a15`

```dockerfile
```

-	Layers:
	-	`sha256:e4cb677f51ac5207db78ce533d80881f1181df93df5858c71eff05bfdc06df85`  
		Last Modified: Wed, 28 Jan 2026 02:35:14 GMT  
		Size: 15.5 KB (15471 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:922a66519e1e1d9166fcdf6ffc4ee018befd6cde9b8b53d7e614d2e41ed770f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10571920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a50c0d0127f61de22b52cfc3acbf5c208e15f76b7a6e18a51e075465786d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 19:01:21 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 19:01:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 19:01:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 19:01:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 19:01:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403a6cdb957401649789e5b4f2cbe88f55a7b8e0a8bd0609c92d9eef2c3a417e`  
		Last Modified: Mon, 09 Mar 2026 19:01:30 GMT  
		Size: 6.9 MB (6920512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7111270df9c5fff857ec52c3ba39df86a8800642c13f0d00bd04a1712b9d4e0`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c919a6d79781833003c5f530b73820bdd56e515c4670f1a782d6f68bd6cbaf8d`  
		Last Modified: Mon, 09 Mar 2026 19:01:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dd1073397e51e35ad7dd3e192c8a292dede602bcea951e4d02a8e2acc25cc31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f173e09372d1c0d616aa2b5e814f124a00b622196f5122bbe8ceb997b7f93d`

```dockerfile
```

-	Layers:
	-	`sha256:f149e96bc2411d24ddb1f3bd40351a3b5649c09c2f17f7db57ca653a6e4731ee`  
		Last Modified: Mon, 09 Mar 2026 19:01:29 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json
