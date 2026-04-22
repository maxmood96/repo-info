## `traefik:langres`

```console
$ docker pull traefik@sha256:5c7950f7724c0b09807de2eb613fc7ab47f1b37ecd5c9c7723e8105e4c4314b8
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
$ docker pull traefik@sha256:dae2b023267c3b265faf2f48c65b15b274beb45479fbee07fc1d2a41dfed07ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52853788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f110ef8d64951eb4655c569778fdeb15309d2e6b37c06efad26a44440f8a912`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 17:37:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:37:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.2/traefik_v3.7.0-rc.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:37:38 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:37:38 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:37:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:37:38 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:37:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c7e7fcbf25e67b3c51eafd517c963c97736cda523bff1ce8f5156b45c919ad`  
		Last Modified: Wed, 22 Apr 2026 17:38:01 GMT  
		Size: 455.7 KB (455675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae475a7c30094ef0acf251a6c546a38d8d09be99b4a44c28cd02f40a8e0f46a`  
		Last Modified: Wed, 22 Apr 2026 17:38:02 GMT  
		Size: 48.5 MB (48533556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9dd42d46bd53c4318ba390327ec9dc73c988dd3ee12dea02362f8447e6cccd`  
		Last Modified: Wed, 22 Apr 2026 17:37:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:105751c9ef182c5b7bd94b58a413c646e191723f1f42ef07cbb4610ef57d7dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.2 KB (859216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a85e8f0319a5ec6238f959207bd362fe45ffed010f22ee28252b38e567a26b`

```dockerfile
```

-	Layers:
	-	`sha256:09a63e7659d3d04e30e5df935d642504778fb3f4196ca12d1b63e4128f867507`  
		Last Modified: Wed, 22 Apr 2026 17:38:00 GMT  
		Size: 847.8 KB (847759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc75f5261bee93299fe65cdc1fd7dde0d4554e440f5b97243e7f723e297d987`  
		Last Modified: Wed, 22 Apr 2026 17:38:00 GMT  
		Size: 11.5 KB (11457 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8eff9bcbf11b78065b16cb1765e08ff123b8f84cb75985e11ed5ef390f892e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48086619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33738252c204f4b8b01e01439611ab006a8b7abd88423d63bd1280b9e517106`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 17:37:32 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:37:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.2/traefik_v3.7.0-rc.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:37:35 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:37:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:37:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:37:35 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:37:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22733e9b782bed0a545f8955760b4174c55fa47aa4d8e54388e03494e2d1eac9`  
		Last Modified: Wed, 22 Apr 2026 17:37:43 GMT  
		Size: 456.5 KB (456522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78b7f0122b560fa828364d4d65b157e8f03b5ed0623fc4a7e5c64a7fd47df28`  
		Last Modified: Wed, 22 Apr 2026 17:37:46 GMT  
		Size: 44.1 MB (44057865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256bfe91ef086bd305276dc32789b779fb8326947ea27203dd4e0ab29f101ee2`  
		Last Modified: Wed, 22 Apr 2026 17:37:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:6c7d18440f01f1bd015fc3f9fb4548726472488ab2bf91e0aa3ab772e93c270f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c855abb5dcb9a6798a4519591bb7c5da30979e1638e64e87f06ec3aaedb9b7e7`

```dockerfile
```

-	Layers:
	-	`sha256:fac0a9ffab4135313963d822455c8fb06ef16bae9b3dd3c7d8e49f5f08c9f18e`  
		Last Modified: Wed, 22 Apr 2026 17:37:43 GMT  
		Size: 11.3 KB (11327 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:71e8d3c4d1719e91fac944c50333328ed96802d16d094edfaf78b0ea990c0f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48012187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e148877176bc73d3c35d1c1cc458227aa3b5cb3119c44ddaad6df82fc800bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 17:37:32 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:37:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.2/traefik_v3.7.0-rc.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:37:35 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:37:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:37:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:37:35 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:37:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6003e51a02c45a2d65f91b7820d830a8391a474c10b66914f75ec17eaa865b`  
		Last Modified: Wed, 22 Apr 2026 17:38:01 GMT  
		Size: 457.9 KB (457913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b00b092aef118f9c3534747fc1c8891ded66b4513c86cfaadfe15e30eaac8a`  
		Last Modified: Wed, 22 Apr 2026 17:38:02 GMT  
		Size: 43.4 MB (43354035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256bfe91ef086bd305276dc32789b779fb8326947ea27203dd4e0ab29f101ee2`  
		Last Modified: Wed, 22 Apr 2026 17:37:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:f00ac6a5f08b386b02176bcedbf112f6c3c5aae573fbe266abd7481e8031c118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.7 KB (858717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cac6687eac20423b66d6becb2b5d26eaf22bf8d514b4b1de77c245b980f5d5d`

```dockerfile
```

-	Layers:
	-	`sha256:09c3d0365f3402fe946b3bc1af9245c5c13ddd931d122222db58532ca9d338c8`  
		Last Modified: Wed, 22 Apr 2026 17:38:01 GMT  
		Size: 847.2 KB (847153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f96e74fe54e2ba7a44a33c15e21bb2af6914ea00aaf108ee8bd8e82a478459`  
		Last Modified: Wed, 22 Apr 2026 17:38:01 GMT  
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
$ docker pull traefik@sha256:3891e6cf589f4d16558b228880699fbe633b28362d9b21374347d53729339dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50384987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1933dc14c291670a3cba3bbfe0983604fad6111c700d6a6da9d0c384b436c845`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:20:27 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 16 Apr 2026 16:20:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.1/traefik_v3.7.0-rc.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 16 Apr 2026 16:20:40 GMT
COPY entrypoint.sh / # buildkit
# Thu, 16 Apr 2026 16:20:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 16 Apr 2026 16:20:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2026 16:20:40 GMT
CMD ["traefik"]
# Thu, 16 Apr 2026 16:20:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981583f7aacfec3a6d84364895133cc9cba1bc1df0a68220b2ebf6c7c74b60af`  
		Last Modified: Thu, 16 Apr 2026 16:25:55 GMT  
		Size: 456.0 KB (456004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162324e72fcbf0c6e0c31f5d6d98653f1aee33b67c7b65e8c680a05ae3273bd4`  
		Last Modified: Thu, 16 Apr 2026 16:26:02 GMT  
		Size: 46.3 MB (46340953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b28fac8384ad6d3177d687c791d83a4d1b36fd6bf81a200cfec08a0fe28c5ab`  
		Last Modified: Thu, 16 Apr 2026 16:25:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:6240bbf357890195299948d87473cc2c66010cdf1e75c4e6ec39b967d42fb558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **851.4 KB (851440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec89e3edd457cef65e555ef7a4936fbe99e4356580f867d0c1341d6696558c4`

```dockerfile
```

-	Layers:
	-	`sha256:08a5989fb3d62f35972baf46a10bd2f0d110ce8354ac2a5bbefb27dcde0236e9`  
		Last Modified: Thu, 16 Apr 2026 16:25:56 GMT  
		Size: 839.9 KB (839943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac0def855a08547e4a0d88a9d2670bf6699314fe2e1ad1858cf584d76a400720`  
		Last Modified: Thu, 16 Apr 2026 16:25:55 GMT  
		Size: 11.5 KB (11497 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; s390x

```console
$ docker pull traefik@sha256:08d1eed562f69447a99ccc7a0c98637ed769fb997c106bf6c37f190da4657940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50871767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f6b41bb22c30a1c7d3fa1323b3924149c1fb6c364e142b461e49f428c1e85e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:42:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:36:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.2/traefik_v3.7.0-rc.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:36:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:36:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:36:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:36:11 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:36:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494eb62e2b2f8e7cb56e614c01ede0584ec7157112f184259ca7cfdede531537`  
		Last Modified: Wed, 15 Apr 2026 20:43:29 GMT  
		Size: 456.7 KB (456673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68306ff89515009cc6e31a21253d6efd2afeb663604a2e1543f0e57b6d41894e`  
		Last Modified: Wed, 22 Apr 2026 17:37:12 GMT  
		Size: 46.7 MB (46688194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd95b999a389579a258d068a2107695284c3270da308e5600ba66fb0aecece5`  
		Last Modified: Wed, 22 Apr 2026 17:37:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:2194143c1310d7ef8b04d8f3a5a98519100c7a92575ddf1c00ba289ce36057dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.6 KB (858563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179bfc480bf50c209ada742cf886364b0e29f6060570e2a47e696ce12392d43`

```dockerfile
```

-	Layers:
	-	`sha256:2c8ef551901eaf92e5c2197c0fe74871deb4be8c569f930d292622a01bfa3a9d`  
		Last Modified: Wed, 22 Apr 2026 17:37:11 GMT  
		Size: 847.1 KB (847106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f400d573b6420948c528c12f70f911cd7402c5c59ef0ccd365c7ad1cd4821aa`  
		Last Modified: Wed, 22 Apr 2026 17:37:11 GMT  
		Size: 11.5 KB (11457 bytes)  
		MIME: application/vnd.in-toto+json
