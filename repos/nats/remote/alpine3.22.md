## `nats:alpine3.22`

```console
$ docker pull nats@sha256:c1379a8588df47244a4789ede85e8ae7490bd37006bde837e4d6fb6f559cb0ce
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

### `nats:alpine3.22` - linux; amd64

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

### `nats:alpine3.22` - unknown; unknown

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

### `nats:alpine3.22` - linux; arm variant v6

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

### `nats:alpine3.22` - unknown; unknown

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

### `nats:alpine3.22` - linux; arm variant v7

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

### `nats:alpine3.22` - unknown; unknown

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

### `nats:alpine3.22` - linux; arm64 variant v8

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

### `nats:alpine3.22` - unknown; unknown

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

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:ea21e6eb9baed3f48d70928e28581f139ea88123ae96c10ab7fd753b196f711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10273468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6294e924a35b3ba351e1a9cb918458e4656b4bf790282e9b5b571ef60785615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 20:25:50 GMT
ENV NATS_SERVER=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.5
# Mon, 09 Mar 2026 20:25:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='85caf0500b011a31b105fb04992cb350236e2d5935a4d2ea7cc1efe9203aafc2' ;;     armhf) natsArch='arm6'; sha256='71a4b194ea3c093318fefb30f5aa9bcbc2b25b172ecb9f17fc9ea18b9c4c7f67' ;;     armv7) natsArch='arm7'; sha256='72f0084970ca9605b83db78806717403e1f676a587a4a07bb28a4b86ae201bc6' ;;     x86_64) natsArch='amd64'; sha256='f1967bea3fbf6c86273f1a2edf5be65165d795716ae1ac2a14824f19cdc35c20' ;;     x86) natsArch='386'; sha256='5549c7352ff3b04424c15402656bccfc5bc3fb26433e0b092ee794c1eae00c8e' ;;     s390x) natsArch='s390x'; sha256='ca7235acf15b59d0b29d413ecb2a3654fa2a877d0a5f6d91db28dbc2d4064ad8' ;;     ppc64le) natsArch='ppc64le'; sha256='29cc4c2566e960a85d2b277b99bf24322ce5c3e3da6e197eb253beb372e9839f' ;;     loong64) natsArch='loong64'; sha256='b126457f298c58981fd42f21bff7c9a37e992ab5727862af64b41aa68b0d8d3b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 09 Mar 2026 20:25:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 09 Mar 2026 20:25:52 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 09 Mar 2026 20:25:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:25:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f47dcf083e6405dbb62b78c40e89eddfa579782e18796398d04ac483723b67`  
		Last Modified: Mon, 09 Mar 2026 20:26:00 GMT  
		Size: 6.5 MB (6538200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7cff225f6b222724626788da2eb98a26c2385e0464e86d59d843ae8cd9131b`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72264d913d41a7e5acf68f5c7336a947d1c985b3beb40308165f5e1529c5e7e1`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c395e1e7cdcf166da464ce9b176a78f41cc1e379d12029384d18535e7510dd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd1e702aa11e4a3b35ba6f6d3a008217124ef4d19d93d23e12767750a22642b`

```dockerfile
```

-	Layers:
	-	`sha256:1eed2a8cf66e0339f0d26be0f99591e27aa134d22ad734dce841c59737673453`  
		Last Modified: Mon, 09 Mar 2026 20:25:59 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

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

### `nats:alpine3.22` - unknown; unknown

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
