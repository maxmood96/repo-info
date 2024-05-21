## `nats:alpine3.19`

```console
$ docker pull nats@sha256:866569467e526287a31ed970a0349637336661050d0d103af519d44dfb46905a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:d8db0ade59946baad440b32e1e29e559bedf8c4ef184449c18cec3b09e651a1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15418627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c8a1867e3ade5b29f586d4af425c5af2c5b77d83afc82d6b4df3c1197a1179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:34:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:34:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:34:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:34:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:34:48 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:34:48 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:34:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930875d3c07e9c11015b7a87cc3680faf0cf5f431f1fbdc3538f0dc7fbba5f73`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 6.3 MB (6300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58623f692b1176118937a136b2a84de7bde4a57cff6c875eedf3a05a8c8c11`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859a16e256149aa535e3b92a42035dc1171480b2582e419a0d652cf9d40267ee`  
		Last Modified: Tue, 21 May 2024 23:35:27 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfa5674686a490dd961d0c0c057b4ab79ec8ef711fe45c5ee02be48beefddf6`  
		Last Modified: Tue, 21 May 2024 23:35:28 GMT  
		Size: 5.7 MB (5708415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:1adfb327abdec112e1ef8e07b47a65e9359224a5c2fd6f41d5d37b9674e6f65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad98a5ab46e9563fb76d02ee9d0b4a4e520beab7c3a1a8c7b6914115c24170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 22:49:24 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 22:49:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 22:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 22:49:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 22:49:28 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 22:49:28 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 22:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 22:49:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c50cc966eb4cbc4a4b881ff20948920be4f45ab8e2cf62ab712cac444395ee`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 6.0 MB (5977107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482b47d1cf301cc352bae57642f522722da3324f7b667b1c7ab9a6727d88f527`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9121bc5ccbbd746d1fb23bd55dddbf3d7e34dfc3cb7df700f8ca078f0ec344`  
		Last Modified: Tue, 21 May 2024 22:50:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155a51d233cc945101d877e9a8d394d4b8114026d50c46107ca509e73414a4`  
		Last Modified: Tue, 21 May 2024 22:50:04 GMT  
		Size: 5.4 MB (5383712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:a3f56e81749917f8b07128d633c16d54338fb686f6ddcaa849a23b024cdc62cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd587d768a05bc1431c931ab535c88081752285018604a5cae23518073a5fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:03:44 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:03:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:03:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:03:49 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:03:49 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:03:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e9b04dcae92028f76d8d03593f5da713c1b30e4413f516ac6feb1931c7b2e6`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 6.0 MB (5966263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42806fb40884dc31d08d85dc9811fd14e2d5c8a3f1d355140fe35d2b0e8572`  
		Last Modified: Tue, 21 May 2024 23:04:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da704e6a7abb5014e315123b47670ed2c5da374a12abe0c8a16ac5c00984bc5b`  
		Last Modified: Tue, 21 May 2024 23:04:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a13bc359472f8406932f00ed1e4a78c2bd57597328886fca2d157b4fd875f`  
		Last Modified: Tue, 21 May 2024 23:04:32 GMT  
		Size: 5.4 MB (5373248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8e0de73f92a021e34a4a3a2d9fe7db10ea0c5374f6acc4839aafa07f83389a89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14486423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30706d32b39530e9b48913eb6b49e5b607cdf805b5b583ca6a10da052e8c863`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:10 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:13 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:13 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e451ccd47ce6074c0eb5a19f953f3cf1b5f7582fa1629fb446c5e98df5bca96b`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.9 MB (5865815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c46871a02794fd3e02f3a96648cfe21cc7bba92e4a12880704bc4f5099fa6`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973b29973a14e29ca26a3bf6ce557a818c454e502f2a1625d12916b94a63c7f`  
		Last Modified: Tue, 21 May 2024 23:22:03 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d832ebe187b943a16762d91e06cfed3a2af866c23fb50873bc206b8ff64b15`  
		Last Modified: Tue, 21 May 2024 23:22:04 GMT  
		Size: 5.3 MB (5271890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; ppc64le

```console
$ docker pull nats@sha256:0b37f107c7121fb4970a680686bf47c0bdc6e221f073948f91fe1ccf935a8069
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14453737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3f441c8f17081f4726462e440f695fc1f61e1a2f10e242f42e4bd984077bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:08 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:15 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:16 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c871a04ac5c3a745fc1b9fc0bf0df8eb4429cfc19a6d0c0e5dc82ead6caa5`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.8 MB (5844103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cdce720d8bce5ea7df85548fc0591d2f54a82aaa905dcf4d5c862d090a59e`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cb8a321e6c477eee1702a71c5d6712719ebf97439a8e5ce5e98052caa4d73`  
		Last Modified: Tue, 21 May 2024 23:21:51 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74163ae1a817e733dfe24bdc0793bd29a32f24f194a83320208429d1d8a41355`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.3 MB (5250277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:6d5ae5c55bd610f20af66cdcb962dc1467df57e229a88bd21e4aa67b0125a4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14983722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e6fda5c2edf46ae713164e45bc6d3db65c81e9d94751fa2b474f4491b6dee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 23:21:19 GMT
ENV NATS_SERVER=2.10.16
# Tue, 21 May 2024 23:21:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a7d9cee900c7035efadeeffced4ede6ceb32f19028a839148d3fb4c285b0106e' ;; 		armhf) natsArch='arm6'; sha256='d8f2807df727d3f8adbc54694813a18b53768903075805c4bf4bd978d961461e' ;; 		armv7) natsArch='arm7'; sha256='a395fe2af1d167429ad8284c8b30abb33f0eca97b2dd6d6bed38697104cef0f5' ;; 		x86_64) natsArch='amd64'; sha256='ed2585edff10a393916e665ad808f97124c726407d926d5f033ad43805ae4de1' ;; 		x86) natsArch='386'; sha256='8e16f3d9cc0cc08f45125c05b456d15c7d0e813d919de65a655abd222a35e4ab' ;; 		s390x) natsArch='s390x'; sha256='5caf7848375536e0e585ac18245635d617eb265f1ec894adeddfad2b78cec223' ;; 		ppc64le) natsArch='ppc64le'; sha256='82e2559bccf20c27bfbd4bceb2daea753a93981a11cbb371fbe5f5802f5ca0a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 21 May 2024 23:21:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 21 May 2024 23:21:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 21 May 2024 23:21:23 GMT
RUN apk add --no-cache libcap   && setcap cap_net_bind_service=+ep /usr/local/bin/nats-server   && apk del libcap
# Tue, 21 May 2024 23:21:23 GMT
EXPOSE 4222 6222 8222
# Tue, 21 May 2024 23:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 23:21:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03de2766ed1b649ad8022c7178d9fb18b54afafd6768b26cc8418bc8ee6ca3`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 6.2 MB (6166358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca420f0a7f6b1e669c0fc2fb845bb3a3e3b5918ae5e6ca274bbe962f098a7c9`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08ad1d4d29a3891a6cef4dd154aebf959965bbae6c2df8f3f88d4d0b617b06f`  
		Last Modified: Tue, 21 May 2024 23:21:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e270d0402a827b66e36de07d5f201dc2ad24fdf690b07d53315ef189c7d5aaa`  
		Last Modified: Tue, 21 May 2024 23:21:53 GMT  
		Size: 5.6 MB (5573725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
