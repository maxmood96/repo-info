## `nats:2-alpine`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
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

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json
