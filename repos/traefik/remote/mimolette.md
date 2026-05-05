## `traefik:mimolette`

```console
$ docker pull traefik@sha256:70d4d8f6e0d76757311b3b3ca7755b6f9557c198011d115b6a7fe542b27fe85a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:38add146404712ca68b43ea040ceb94e1f5753ebcf1079bb99332222cd81a692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53215490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b6bcebfb79e9e2a34f73aec6dbb0615f1101b760a39660fc4f01b26093a297`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 19:11:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 05 May 2026 19:12:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.45/traefik_v2.11.45_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 05 May 2026 19:12:32 GMT
COPY entrypoint.sh / # buildkit
# Tue, 05 May 2026 19:12:32 GMT
EXPOSE map[80/tcp:{}]
# Tue, 05 May 2026 19:12:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 May 2026 19:12:32 GMT
CMD ["traefik"]
# Tue, 05 May 2026 19:12:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.45 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86794de37ca754c614a9eaa510a62350b4e42bee4dcb180db661df0d572cac88`  
		Last Modified: Tue, 05 May 2026 19:11:46 GMT  
		Size: 455.5 KB (455485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31dfb1da727bf7df2faf12b2872418cd88fbddbe2a26f0c2b790bbf2cce7b5a1`  
		Last Modified: Tue, 05 May 2026 19:12:58 GMT  
		Size: 48.9 MB (48895446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f6688e93ca74a2b15122c16b6bd41eab5c2760cad72f5cbadc8251788d65db`  
		Last Modified: Tue, 05 May 2026 19:12:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:ee61430f0aff8c56b5fa1f77346911f8d5d53aa194ebe9d6e4920e73de36d80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **878.3 KB (878315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9739745d7e2d225a393d1b889a2d4db24e78da328945abbdd6cca26b8acac1`

```dockerfile
```

-	Layers:
	-	`sha256:3076b9f329d6ec7f49b9af273df3154963a28c99b4fd000d42d92e0fa3225bf3`  
		Last Modified: Tue, 05 May 2026 19:12:56 GMT  
		Size: 865.7 KB (865705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5d7d9b4e81b17e8cd3a2f524c001b53c665a9325da9d10ff5707b89d8eec66`  
		Last Modified: Tue, 05 May 2026 19:12:57 GMT  
		Size: 12.6 KB (12610 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8e3bba8fbe3d20ddcadc2610e2e457322fb70f13539182dc3fe12e1330808f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48863006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0b4daedb76ba6b7c34e23ef55df24b4a28bfc1dbd03ef638b0659904faa98d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 19:02:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 05 May 2026 19:02:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.45/traefik_v2.11.45_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 05 May 2026 19:02:40 GMT
COPY entrypoint.sh / # buildkit
# Tue, 05 May 2026 19:02:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 05 May 2026 19:02:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 May 2026 19:02:40 GMT
CMD ["traefik"]
# Tue, 05 May 2026 19:02:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.45 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1589b4e397e08f9264bcb91495fa435416ed104c15f188a2ba0b915410aee4df`  
		Last Modified: Tue, 05 May 2026 19:02:28 GMT  
		Size: 456.3 KB (456334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c1ec7ffd20887224b73259450aba63d9f8cf0d8f4017ca0978e9deafd9914`  
		Last Modified: Tue, 05 May 2026 19:02:50 GMT  
		Size: 44.8 MB (44834439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097fc1eec3b5e4eb10cc0d3f61514c05054a1a2695b7f70495d5ec32bd4ad75f`  
		Last Modified: Tue, 05 May 2026 19:02:49 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c3718e090981e6288f9c61240e01af479ed7bf3c464ffaea2a1f6df399c7fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d6d1064b874736330144d1054363fde8527f2c269c34f7e17cb4ce8d2efe33`

```dockerfile
```

-	Layers:
	-	`sha256:e6ff4d9344225456b59fd94d209d747a733baab6936b3a819cb6fcad685354c2`  
		Last Modified: Tue, 05 May 2026 19:02:49 GMT  
		Size: 12.5 KB (12512 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4b91a0afbd546903ff26f6ae247b55ff1b5579b15b49d961e213fbf203e1bb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48493844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2052407c689163249a41e1823ee6b6e3b06d528478132768646fc235c6a4a0b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 19:09:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 05 May 2026 19:10:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.45/traefik_v2.11.45_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 05 May 2026 19:10:27 GMT
COPY entrypoint.sh / # buildkit
# Tue, 05 May 2026 19:10:27 GMT
EXPOSE map[80/tcp:{}]
# Tue, 05 May 2026 19:10:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 May 2026 19:10:27 GMT
CMD ["traefik"]
# Tue, 05 May 2026 19:10:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.45 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de787452bc4a8e4e94bb4a7b752ccfe8a1d22a8f43dd33946feefc9686ed12b0`  
		Last Modified: Tue, 05 May 2026 19:09:41 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1313c79957823656e05c029fc4a4dbf6d01e39887b54fbb7a36b95cffc26731`  
		Last Modified: Tue, 05 May 2026 19:10:53 GMT  
		Size: 43.8 MB (43835859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e04f01e6a3a8064d130975cd38880d76a782357f173b4f78642f7cfd3212e7f`  
		Last Modified: Tue, 05 May 2026 19:10:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:f9c92d8cdc51e67e9dd81cf1c5130f5d2c3ee0a428d6753d27fef075a89f936a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.9 KB (877912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcb0b0352c1304de7b7a017c59545f9a5b579df42a12dcfe7bfd80297513a15`

```dockerfile
```

-	Layers:
	-	`sha256:9c5b5c8f201403f7f3bd2d6f1585fd6a94e0fd6115d8417b4a4915ebb1de3fa0`  
		Last Modified: Tue, 05 May 2026 19:10:52 GMT  
		Size: 865.1 KB (865147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0abdc0b3c5f517164fe18454aefa3ac2edc48aab00824b67179fe55189dd000`  
		Last Modified: Tue, 05 May 2026 19:10:51 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:0202c7a10f8a5823f535a27888eaa6d639d3020ed0ff6b2b4f4ce56f11c47135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47007814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee822f90a906151ce7abd2956f8483b986ee22e0513b6087102ed04db7dbd2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 19:01:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 05 May 2026 19:02:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.45/traefik_v2.11.45_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 05 May 2026 19:02:35 GMT
COPY entrypoint.sh / # buildkit
# Tue, 05 May 2026 19:02:35 GMT
EXPOSE map[80/tcp:{}]
# Tue, 05 May 2026 19:02:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 May 2026 19:02:35 GMT
CMD ["traefik"]
# Tue, 05 May 2026 19:02:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.45 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c01d2200c9f8f0e9515bebf8416986bd23c28a79eef5f49a672a5d4f889966`  
		Last Modified: Tue, 05 May 2026 19:02:18 GMT  
		Size: 458.2 KB (458167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4059a8257a8cacb1b5f687a7b4e466a87e15998b12b29512d4d568c37ffcb65`  
		Last Modified: Tue, 05 May 2026 19:03:25 GMT  
		Size: 42.7 MB (42718349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33141f3cf46ef3438c1d8c141d0f8ba2dcff105392db32a044ae7ecca09c16f`  
		Last Modified: Tue, 05 May 2026 19:03:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:b182c6384b20c4aefce79623fee6339f19e713de1f40476a006f160eb718693a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.8 KB (877780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc3dd8374574c9d692b587b5294d91079f903d7e6c4fc8b6a7040ae6a8351b9`

```dockerfile
```

-	Layers:
	-	`sha256:74056b2ed7fc3106ca355cb0e68440de3b90233a80f2813d9a6a6cfb1caa57b9`  
		Last Modified: Tue, 05 May 2026 19:03:23 GMT  
		Size: 865.1 KB (865106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28d98d7222766fa0d606db29fd4a97187a091f7af0ea80ec29c9fe81a60ba1ac`  
		Last Modified: Tue, 05 May 2026 19:03:23 GMT  
		Size: 12.7 KB (12674 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:53a45b43934ba668340f30ac5dbad3e5bc261dc6d33e9b5eb7ec0764359b5c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51387828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f49e65feae60e76384bb83a6d929467d1182ff19cf187e896b63b2051cbbf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 23:19:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 29 Apr 2026 23:32:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.44/traefik_v2.11.44_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 29 Apr 2026 23:32:05 GMT
COPY entrypoint.sh / # buildkit
# Wed, 29 Apr 2026 23:32:05 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 Apr 2026 23:32:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Apr 2026 23:32:05 GMT
CMD ["traefik"]
# Wed, 29 Apr 2026 23:32:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.44 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8040dc8746cf581b029763636c03350dc436da84d2d3e62bb733e1090fff9ada`  
		Last Modified: Wed, 29 Apr 2026 23:25:23 GMT  
		Size: 455.8 KB (455802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3d7afadb64603152e2952833dc6a8f77cdde2d7964422c3887684db3a069ed`  
		Last Modified: Wed, 29 Apr 2026 23:37:29 GMT  
		Size: 47.3 MB (47343994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8873f90c5eaec0c4c08d4c84b2f97510b9394552b635f3cc3db37f1f141305e5`  
		Last Modified: Wed, 29 Apr 2026 23:37:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:03a24cb7110516007952ce52cbd56fae3cec64a95ad8050b155eda8cef487624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.0 KB (877000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987767ef3d5d44ee10739707aa26822b5c3b78e4fa7768fb925367fa9b6d2d90`

```dockerfile
```

-	Layers:
	-	`sha256:e9f80e52ed7f7458dc13dd860240fb07cccf4885fd314f4abaebdd4059a2ef71`  
		Last Modified: Wed, 29 Apr 2026 23:37:22 GMT  
		Size: 864.3 KB (864327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fadb731fb7c9f684c25b462fe50000cabc9eaf0759199c542945df5ddb57f84`  
		Last Modified: Wed, 29 Apr 2026 23:37:22 GMT  
		Size: 12.7 KB (12673 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:e5ae807d79b938eb47837206a5d4f11feda0c7a918bd274ff1b990dfbcdb125e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51635602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031bd27e91e7ea3df1b8aedf0caac8191cabbad642660a2bf5f477e778045e58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 23:19:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 05 May 2026 19:02:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.45/traefik_v2.11.45_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 05 May 2026 19:02:58 GMT
COPY entrypoint.sh / # buildkit
# Tue, 05 May 2026 19:02:58 GMT
EXPOSE map[80/tcp:{}]
# Tue, 05 May 2026 19:02:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 May 2026 19:02:58 GMT
CMD ["traefik"]
# Tue, 05 May 2026 19:02:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.45 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a695583892a4b770ae13ca46cd98d2519dacf812ea9ad59c02194a45b32e0`  
		Last Modified: Wed, 29 Apr 2026 23:20:11 GMT  
		Size: 456.5 KB (456456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2c1ae29cfc4b65e5b29f3303cfccc58b237484f8a1f99965fa0bc76f9c04c6`  
		Last Modified: Tue, 05 May 2026 19:05:26 GMT  
		Size: 47.5 MB (47452244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b090af2cfccc856ce21f267889f8b0245f0c7b0e8bf4ff9cbe14a488cdedbfcf`  
		Last Modified: Tue, 05 May 2026 19:05:14 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:825c7ad84662d3f12d8b11b7756a8569e76bab963fe531be212d1cbdeded1d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.7 KB (877660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e310a0bc90de7f53002b62a90502eb4532f5484c078fb5420c6fdcb34808c`

```dockerfile
```

-	Layers:
	-	`sha256:14d0f917ae59b8c1edb6eb953aebab51f0b6a378daee102e6ebb728f21561591`  
		Last Modified: Tue, 05 May 2026 19:05:14 GMT  
		Size: 865.0 KB (865050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a3aec28f47e15c765776f38950cda2c5da51f50960d3c44a6904aab937c222`  
		Last Modified: Tue, 05 May 2026 19:05:13 GMT  
		Size: 12.6 KB (12610 bytes)  
		MIME: application/vnd.in-toto+json
