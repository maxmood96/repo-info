## `traefik:langres`

```console
$ docker pull traefik@sha256:331eae025e82b064c1f3b9af02116eb61dc80abbf273b2d2a2c106b31e485734
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
$ docker pull traefik@sha256:ce932496ba280bc3fbe2834826b8f411f31270378d4b236bd60ba6856ed983d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46237392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0249681ae14b1b0d0f6814f5425828160638c945fd997e885c80a94e20c97c6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:08:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 20:18:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.2/traefik_v3.7.0-rc.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 20:18:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 20:18:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 20:18:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 20:18:58 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 20:18:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:4bb927b4f9cce527e7d195333cba1d304bb8a2f3b072da61b4580219e3838746`  
		Last Modified: Wed, 22 Apr 2026 20:19:58 GMT  
		Size: 41.9 MB (41947768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26147e5ed0ea7e8cf521ac11fa304829213c4ad272d1bf8ca38da67f60df8dab`  
		Last Modified: Wed, 22 Apr 2026 20:19:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:bb8257859a477e072024d964666fcc6f55c0b07478b59dd667a266b0506c4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.6 KB (858633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2e2d3f68806b64725224c64ab782d6a9529eddc3055bf1c35bd82431bd8bb3`

```dockerfile
```

-	Layers:
	-	`sha256:90b47504ce0af134c4477846bd8303b2fd80fc317b35f2d68ea5d6a19c62b1ee`  
		Last Modified: Wed, 22 Apr 2026 20:19:57 GMT  
		Size: 847.1 KB (847136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9fc1aee83a431e5c6442fe6f841f81d8b4ecd514591716d1c51bc82ae1e9943`  
		Last Modified: Wed, 22 Apr 2026 20:19:56 GMT  
		Size: 11.5 KB (11497 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:langres` - linux; riscv64

```console
$ docker pull traefik@sha256:91b98cc038695d57059d90da95e75e8659b36eeb90e57adef4e44fe31d0816dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50910976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7f03dffeb95f9e444d1048d65264f98c12a9385db73a0c9a7547b09c16f54a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Sat, 25 Apr 2026 18:28:43 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 25 Apr 2026 18:28:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.2/traefik_v3.7.0-rc.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 25 Apr 2026 18:28:56 GMT
COPY entrypoint.sh / # buildkit
# Sat, 25 Apr 2026 18:28:56 GMT
EXPOSE map[80/tcp:{}]
# Sat, 25 Apr 2026 18:28:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Apr 2026 18:28:56 GMT
CMD ["traefik"]
# Sat, 25 Apr 2026 18:28:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa86f96704c7abcae65c8930cd34ae1dbc4acb6727e475216f605e390365e73`  
		Last Modified: Sat, 25 Apr 2026 18:34:29 GMT  
		Size: 456.0 KB (456001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e01d4bcfe784338fa38359a3036f0d19cb88e0cff03d7abd71bed12bb33157b`  
		Last Modified: Sat, 25 Apr 2026 18:34:36 GMT  
		Size: 46.9 MB (46866943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599325cffe488dfccd4f64f494d29a5b3287fec6af458f9f807669c958524aca`  
		Last Modified: Sat, 25 Apr 2026 18:34:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:langres` - unknown; unknown

```console
$ docker pull traefik@sha256:970985eb53801c4e77cc2acd4cfc840c811e20179bc7e6864276c7de64587378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **858.6 KB (858629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca91914e19dbe850978bab84e1a06df3392a77b897cbb06180033e384f8b5af6`

```dockerfile
```

-	Layers:
	-	`sha256:3b7fda82e0a3518c7b9abccd101fdd0ad0bc5031a1d997e5aa6a314c9b99b372`  
		Last Modified: Sat, 25 Apr 2026 18:34:29 GMT  
		Size: 847.1 KB (847132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f78db0b5ae336882c53fbe962d239387996bb4ee11a2ee21c59502aba56797bd`  
		Last Modified: Sat, 25 Apr 2026 18:34:29 GMT  
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
