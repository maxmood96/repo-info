## `traefik:langres`

```console
$ docker pull traefik@sha256:72e7324cd2e62aacfb9e7d50f42016f9c6320f6333756b03c312a476f92fb0ac
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

### `traefik:langres` - linux; amd64

```console
$ docker pull traefik@sha256:b42a26a904c28d1136133cbcd71db45a9a6f57f3ae2b033e017ea66242a76cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52299402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52de6cebbd527145cb0fd83f1bd0cab251219cc6191c5bde823f954ffd054b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:22:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 15 Apr 2026 20:22:34 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.1/traefik_v3.7.0-rc.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 15 Apr 2026 20:22:34 GMT
COPY entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:22:34 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:22:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:22:34 GMT
CMD ["traefik"]
# Wed, 15 Apr 2026 20:22:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765ddb02fcb836ae5bcb3b945bb890cd25854321c80e9215bff7e65756bec166`  
		Last Modified: Wed, 15 Apr 2026 20:22:59 GMT  
		Size: 455.7 KB (455660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050323aa452f46fb95c857427d25e45c0c5819b800b6a202920112326c25ea09`  
		Last Modified: Wed, 15 Apr 2026 20:23:00 GMT  
		Size: 48.0 MB (47979184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4460fa00c6db3070d5aea59ba74e47558fdcd11f1fa6de545b88246e30eb7ac7`  
		Last Modified: Wed, 15 Apr 2026 20:22:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:3cfaca0cbb7ad21eba891573f456e4f9b1abede78a513167d8fd78aa0027c3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.0 KB (852027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae8e306189313f0d0a00a13a674fdf72958cf162e6c7395342e1f08d8882ab1`

```dockerfile
```

-	Layers:
	-	`sha256:2c798c75423128d1b2d792f9f78792d69af9af09c7936dd48a398288ec28ac17`  
		Last Modified: Wed, 15 Apr 2026 20:22:59 GMT  
		Size: 840.6 KB (840570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10576efba35d8116dd459d6348c8dbd0eaf3c154a85adeabb27fbbb6d1bca47`  
		Last Modified: Wed, 15 Apr 2026 20:22:59 GMT  
		Size: 11.5 KB (11457 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; arm variant v6

```console
$ docker pull traefik@sha256:797417200d7dfd7a9122b6b63eaf4bebb84d4c4c4e31453c618a77b68ab1cffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47584509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f968fbad07f65f269d06523ddf89ae91e5745a9a25d30a42c103719895229fee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:31:03 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 15 Apr 2026 20:31:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.1/traefik_v3.7.0-rc.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 15 Apr 2026 20:31:06 GMT
COPY entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:31:06 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:31:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:31:06 GMT
CMD ["traefik"]
# Wed, 15 Apr 2026 20:31:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586cfa819cf4737a7190bb705e7aaa60f33e84749c8bedf7d4f7c3ddb73bde70`  
		Last Modified: Wed, 15 Apr 2026 20:31:14 GMT  
		Size: 456.5 KB (456520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6ed55c8b10f7717b17401fcb300171fad01b1f5d17888a0304b95726f0999`  
		Last Modified: Wed, 15 Apr 2026 20:31:15 GMT  
		Size: 43.6 MB (43555757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c376472586a7ec72a78b87d4dad32366f79028baaf7ec5b4eca0d24411777ba2`  
		Last Modified: Wed, 15 Apr 2026 20:31:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:2184255791e3a891d5b6bf6035775bcd2f3f08e317cb9943e86bd286c89f0a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4472fb2c902be13e1d84124532aa5d0251d487239fd42793427ac2dd4db1af46`

```dockerfile
```

-	Layers:
	-	`sha256:248a95c1f6cfb2dcc6ce79939e428e2896d58be56a03ff1b7d0227becf38cb54`  
		Last Modified: Wed, 15 Apr 2026 20:31:14 GMT  
		Size: 11.3 KB (11327 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3f6ab6b053ad023198694f32ac799c1a05a0c56d751ab4d4caa582703bb7c468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47508371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897a7895e586dc23aa998e470d2a7d2530fa3bc40fe407c89b94e3c8644d8ffb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:22:18 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 15 Apr 2026 20:22:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.1/traefik_v3.7.0-rc.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 15 Apr 2026 20:22:21 GMT
COPY entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:22:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:22:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:22:21 GMT
CMD ["traefik"]
# Wed, 15 Apr 2026 20:22:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31819f3f4842034f917aba4880863d9207285e0cac69f65a579c5a6147cbc180`  
		Last Modified: Wed, 15 Apr 2026 20:22:46 GMT  
		Size: 457.9 KB (457916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c59e3c58429b81c8ea1c6d65c2c85bfbc07e7e5812ecd6e4d8ccf58df173c`  
		Last Modified: Wed, 15 Apr 2026 20:22:47 GMT  
		Size: 42.9 MB (42850216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75d494f5ffee1b08db7c22bffb6cab5d9f2f1f41991fe912fe01820de0bcb59`  
		Last Modified: Wed, 15 Apr 2026 20:22:46 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:451dc37de59de2315a778110943f5cae01c96589232fbfd65ce1e8be5da12ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.5 KB (851528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a73514a559b82f77baec781ad6d590637d0c17e1fcadc1a8fd5ee81420a29f`

```dockerfile
```

-	Layers:
	-	`sha256:ad168c66ab9878fd23d536634ecbdf3dc51e2ec884c71493a12f79dd0f2d7b0b`  
		Last Modified: Wed, 15 Apr 2026 20:22:46 GMT  
		Size: 840.0 KB (839964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28525d6df9a2e0d1b8c2df308ac0f95bcb063349555089ff908fb1f92524d30b`  
		Last Modified: Wed, 15 Apr 2026 20:22:45 GMT  
		Size: 11.6 KB (11564 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; ppc64le

```console
$ docker pull traefik@sha256:7a5f23f1d4f0fb0c710df535bb30b656b47b30722cb95d120fefd3b25a999056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45722184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03bcdd6022e65e237403be4b9c3a328b6652fbf292c82f953f5dff47f58f0cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:08:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 15 Apr 2026 21:08:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.1/traefik_v3.7.0-rc.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 15 Apr 2026 21:08:05 GMT
COPY entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:08:05 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 21:08:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:08:05 GMT
CMD ["traefik"]
# Wed, 15 Apr 2026 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ce53e29a62df07c200ac0d7cc718585a7031556056c94626ccbb010496ad7d`  
		Last Modified: Wed, 15 Apr 2026 21:08:51 GMT  
		Size: 458.3 KB (458325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f788543eb5f083591aef3690a2f13f7d15154ac88db46bf6d1902e75d1a818`  
		Last Modified: Wed, 15 Apr 2026 21:08:53 GMT  
		Size: 41.4 MB (41432560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4e1925fd894a8bbbcfdc7b9107d6c5d103b64081c1c60223d33c33199a357f`  
		Last Modified: Wed, 15 Apr 2026 21:08:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:3fc52eb49f353538395dd2f1f29f06842d4f392ba111948d2181712713950c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5ae1f792208c7bcc5c3b46f7f4cf3e9a80cf6d67e14f42bfe40b5859ef57e2`

```dockerfile
```

-	Layers:
	-	`sha256:42e6b42c3aa79904ff8a3845110960a6e576c3eee5a708e717bcd7e3b72f9f14`  
		Last Modified: Wed, 15 Apr 2026 21:08:51 GMT  
		Size: 839.9 KB (839947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8651b4d10ae1f3b2b0193c74b5aeaf1784cac8b606dcf97f3fd2bd9da114dd1f`  
		Last Modified: Wed, 15 Apr 2026 21:08:51 GMT  
		Size: 11.5 KB (11496 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; riscv64

```console
$ docker pull traefik@sha256:8171fbd9a4f8983a416615ea594327a0931cd2aa553c4d1d5937a06f3352b9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50387608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0308e54f8f7fca0ddad539409f19144ca8f1935ad5ae6360c2cb052f411379d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 20 Mar 2026 21:32:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 09 Apr 2026 00:15:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.1/traefik_v3.7.0-rc.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 09 Apr 2026 00:15:00 GMT
COPY entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 00:15:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 00:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 00:15:00 GMT
CMD ["traefik"]
# Thu, 09 Apr 2026 00:15:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2138e9bd4a0faccf25a9170a648b7e113eea3d334c9206782528231fbf39f`  
		Last Modified: Fri, 20 Mar 2026 21:38:03 GMT  
		Size: 461.0 KB (460986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d2bb5f37de278aaeffc3b31bccfe3b50a51a50a4def8b1d37fab6c5c7069a9`  
		Last Modified: Thu, 09 Apr 2026 00:20:14 GMT  
		Size: 46.3 MB (46340965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d981b5ada06c21ae28d6ae5ea64bbb5f30e419afb420f9c4e003d6d0d74bef`  
		Last Modified: Thu, 09 Apr 2026 00:20:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:aa2b246f527b397d68ef2b6c459d27c3a2f0f9325a93808e33c32a5c0f15faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.4 KB (853393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28a994a99e5ce4a08ae128837073341cc6e3c1bd6740bb698653c14bc7743b8`

```dockerfile
```

-	Layers:
	-	`sha256:320a8efc86b959f461c427129a3a1ee0fbcf0bdabeddfb5d7d3fea1751c9037d`  
		Last Modified: Thu, 09 Apr 2026 00:20:07 GMT  
		Size: 841.9 KB (841898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f51808a2086d6225bc567a22fe4d5baf241aab3ecdb5c04a2ea79de82d79f97b`  
		Last Modified: Thu, 09 Apr 2026 00:20:06 GMT  
		Size: 11.5 KB (11495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; s390x

```console
$ docker pull traefik@sha256:ae2927f728e011caf43534cec0f53c94894d5f443ed25011982c7e05e07af904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50332487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583325318c0b56396859ca31c17f255361ebcb9ab5ebb2f33755a73aa98e6d76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 15 Apr 2026 20:41:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.1/traefik_v3.7.0-rc.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 15 Apr 2026 20:41:47 GMT
COPY entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:41:47 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:41:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:41:47 GMT
CMD ["traefik"]
# Wed, 15 Apr 2026 20:41:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935dd66668d2f6e060f9d991a73aee8127a53466085251bae64e750e36112cdc`  
		Last Modified: Wed, 15 Apr 2026 20:42:42 GMT  
		Size: 456.7 KB (456660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66326936510ee7ccc0b0cd3450045b079a82827493e8fddd4f89e5641e022ec0`  
		Last Modified: Wed, 15 Apr 2026 20:42:42 GMT  
		Size: 46.1 MB (46148926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9b689fab87ddde2932d720ed0c8479cf6cc3fd5f260ed36ec1300816bedd1`  
		Last Modified: Wed, 15 Apr 2026 20:42:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:a388947a8d44f11367019094d68a040dc3f010f727875c440a5ae61706b28b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc9d6341427ca6979e17813fd7d8719a8352713dd830aa8fcd84af3d479dc2d`

```dockerfile
```

-	Layers:
	-	`sha256:b32f991866138a9c78b1fa04b3433e70da83a3d177d275fe5cb29d628c6f86b4`  
		Last Modified: Wed, 15 Apr 2026 20:42:42 GMT  
		Size: 839.9 KB (839917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c530c6bdd2988236aa1819616fb13addd8b871073757c2931a08f9f5651f9360`  
		Last Modified: Wed, 15 Apr 2026 20:42:42 GMT  
		Size: 11.5 KB (11457 bytes)  
		MIME: application/vnd.in-toto+json
