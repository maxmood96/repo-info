<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-ltsc2022`](#caddy2-builder-windowsservercore-ltsc2022)
-	[`caddy:2-builder-windowsservercore-ltsc2025`](#caddy2-builder-windowsservercore-ltsc2025)
-	[`caddy:2-nanoserver`](#caddy2-nanoserver)
-	[`caddy:2-nanoserver-ltsc2022`](#caddy2-nanoserver-ltsc2022)
-	[`caddy:2-nanoserver-ltsc2025`](#caddy2-nanoserver-ltsc2025)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-ltsc2022`](#caddy2-windowsservercore-ltsc2022)
-	[`caddy:2-windowsservercore-ltsc2025`](#caddy2-windowsservercore-ltsc2025)
-	[`caddy:2.11`](#caddy211)
-	[`caddy:2.11-alpine`](#caddy211-alpine)
-	[`caddy:2.11-builder`](#caddy211-builder)
-	[`caddy:2.11-builder-alpine`](#caddy211-builder-alpine)
-	[`caddy:2.11-builder-windowsservercore-ltsc2022`](#caddy211-builder-windowsservercore-ltsc2022)
-	[`caddy:2.11-builder-windowsservercore-ltsc2025`](#caddy211-builder-windowsservercore-ltsc2025)
-	[`caddy:2.11-nanoserver`](#caddy211-nanoserver)
-	[`caddy:2.11-nanoserver-ltsc2022`](#caddy211-nanoserver-ltsc2022)
-	[`caddy:2.11-nanoserver-ltsc2025`](#caddy211-nanoserver-ltsc2025)
-	[`caddy:2.11-windowsservercore`](#caddy211-windowsservercore)
-	[`caddy:2.11-windowsservercore-ltsc2022`](#caddy211-windowsservercore-ltsc2022)
-	[`caddy:2.11-windowsservercore-ltsc2025`](#caddy211-windowsservercore-ltsc2025)
-	[`caddy:2.11.4`](#caddy2114)
-	[`caddy:2.11.4-alpine`](#caddy2114-alpine)
-	[`caddy:2.11.4-builder`](#caddy2114-builder)
-	[`caddy:2.11.4-builder-alpine`](#caddy2114-builder-alpine)
-	[`caddy:2.11.4-builder-windowsservercore-ltsc2022`](#caddy2114-builder-windowsservercore-ltsc2022)
-	[`caddy:2.11.4-builder-windowsservercore-ltsc2025`](#caddy2114-builder-windowsservercore-ltsc2025)
-	[`caddy:2.11.4-nanoserver`](#caddy2114-nanoserver)
-	[`caddy:2.11.4-nanoserver-ltsc2022`](#caddy2114-nanoserver-ltsc2022)
-	[`caddy:2.11.4-nanoserver-ltsc2025`](#caddy2114-nanoserver-ltsc2025)
-	[`caddy:2.11.4-windowsservercore`](#caddy2114-windowsservercore)
-	[`caddy:2.11.4-windowsservercore-ltsc2022`](#caddy2114-windowsservercore-ltsc2022)
-	[`caddy:2.11.4-windowsservercore-ltsc2025`](#caddy2114-windowsservercore-ltsc2025)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-ltsc2022`](#caddybuilder-windowsservercore-ltsc2022)
-	[`caddy:builder-windowsservercore-ltsc2025`](#caddybuilder-windowsservercore-ltsc2025)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:nanoserver`](#caddynanoserver)
-	[`caddy:nanoserver-ltsc2022`](#caddynanoserver-ltsc2022)
-	[`caddy:nanoserver-ltsc2025`](#caddynanoserver-ltsc2025)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-ltsc2022`](#caddywindowsservercore-ltsc2022)
-	[`caddy:windowsservercore-ltsc2025`](#caddywindowsservercore-ltsc2025)

## `caddy:2`

```console
$ docker pull caddy@sha256:ec18ee54aab3315c22e25f3b2babda73ff8007d39b13b3bd1bfffa2f0444c7d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:3739ea4f0c877259a693d932693cf8f3408e9a9497c004f031b0e830e93e1546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23985030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5190456911cee510988a5fb9996188ef866fbcca3235cad19bf05f5f8f33386f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:12 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920de1d55d9880b00fbeaf8fa3757e89f7ea6170ff12633cbe766c2152a858d`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 2.9 MB (2886638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057c497bda068e80884e6836fbf8971a954593242af7694d080e6b81758b67f4`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b55c68e4a0feeeaec6f86ced6bd8790e19ed68399cff61bab00adc15895ec13`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 17.2 MB (17226669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:e08c659e9fe301aa2814b2cafc4a5211423fcaa307a515772efeb816684ceb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cd52ea603ed29abf30a13e9ab37f92acffb93b53042a6bfaf1d22d9bdb8be`

```dockerfile
```

-	Layers:
	-	`sha256:4c4f094b32e82a0c66e0e5c00015a86d670049e4e9a336febc6c2a2fd626b19b`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 332.9 KB (332947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16285c7326d137b74e90d1f477040eb15643c312e7a46770316c0c258033326a`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:018595a3226de0d5c9055279af90983e9e91ca5f12dde17e93925455d19bc0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ce61ba53a04521d0e684e8048cde82ebd35cd3d72a9d1f7616056976e75253`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:40:51 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:40:52 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:40:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b1247b4f1cad33af22f46d45d07b1ee65401981dccc3fa920dafbde1fb072`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 2.8 MB (2819583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d84aa44715b44ce12b2cc9b98a20167ca060c5869ab67124210f554413d56ee`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93038fb49fb9d7664bc1a8209857cde656b4e5ff6ab5a7bf4b270d942f499d0`  
		Last Modified: Tue, 12 May 2026 21:41:00 GMT  
		Size: 16.3 MB (16311628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:de7fac8a337ded6fa61288d6dcc5837d472ed26f9d6b7230f0c8487fb9db984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feea7dba17177c5d72e8d8b883cd3bcdcda396dcc918c1e1e6d3868632932251`

```dockerfile
```

-	Layers:
	-	`sha256:2bd47793d94047373cab54d4b18f46ce16d19438827a8a41e3c5960cd1da48ca`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 18.4 KB (18353 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:2c3d3047a1705945ca9376ef8d3e9eb431f0f07f16e6ae2511326d7f0b664ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22262035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a70cfe7deb0544e9098ef10e20ebbc18e346bb3b8df5b140b9f184e71b4a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:42:08 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:42:09 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:42:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce55fb7d543ef0a1f852326909b7cdb22fb514199bd31b9543d92f04e878f4`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 2.7 MB (2681516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49caf58b5069e136a5fcd2fbaa18da4c786566963ba48bcedc27100b8a43365b`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ba28a73ebab4ca57472bca296d741e3d9b1cb27478c6adde87b7c314ba7810`  
		Last Modified: Tue, 12 May 2026 21:42:18 GMT  
		Size: 16.3 MB (16289861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:08ab34ff2df00fe711e074db26cf28e9b5ff1dbfe8355e0f414ed9a7c465cfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb11059736745812fc6bfa910b2d1cce68b03317d8452425d1f7954f2023f495`

```dockerfile
```

-	Layers:
	-	`sha256:95b578e25712b12ba424efc0abb0e6a4daa0cb6d145f200869796d863a0535dd`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 332.4 KB (332365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876e5685474ad9dfce16688d11127988be62753bb83e66c138c382a181530636`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 18.6 KB (18568 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ae38d5cc9674696bfec2dd7a20ea5495a2653d788ee39bff6aaf1007f8dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22800642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64000d357283f8b74cfc9cabce60768a6957447b74a7eb73c573c5d344a398`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:44:57 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:44:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:00 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6cabef06141e7f3aba6fa7d3898c4282f7316acb2ad612b8ea82ac9172cd99`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 2.9 MB (2900862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69f6bd08e27b5a1e9b73c99efae612626fabe895c78a156e402e5938112fff9`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 7.5 KB (7500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4e100b255f5c935bb23c7e5f2a23ee2b5b683a152149ad5db9b32d8455edf`  
		Last Modified: Tue, 12 May 2026 21:45:07 GMT  
		Size: 15.7 MB (15692378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:99d5c41f924f43a16554137091afc6dc8c34e2976b4011ea8793c6211676f8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 KB (351013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f8ace5e5ed9603a8a26766f5df8fd3efe32a76bb3d66c4017bf8bb842691c`

```dockerfile
```

-	Layers:
	-	`sha256:43c50900a0619c09f3987cc62bbfffd4d10da1b9d81fd21f3605e47dbb741967`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 332.4 KB (332401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e57f91d95d6c31886fc5dc74e74b86782c292b27bf964bb5023e301c36f8270`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:d6f3adf638edd88132caec6005766ec86f31796069549755af52d172a03ebd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22551245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d82ac569eea06185f6688d103c7d7e2ef313dce067d6f1aca3b7255025aa450`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:46 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:52 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aba3acae7a944d3cb59ff0085839ecf6bc67e67a1ff5c9d62453ec36405516d`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 3.0 MB (3024677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef81e00b6b88436c8856bd7f6a2a40abea36897a22c7707cdf06722a09f8b819`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1e87608e2891184dfb2f547b0a2062b1bba1b787d3cd95ff36446affe940e`  
		Last Modified: Tue, 12 May 2026 21:46:12 GMT  
		Size: 15.7 MB (15688108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:863e023f3571814b385c37ac309e71a9a712f4aea420d2cea5032e2a362bf7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef881e7b8f82faab6a4473932499599574eb0bc9d0264c779647d0b099584f`

```dockerfile
```

-	Layers:
	-	`sha256:aa780bcad124738bdb6864e89c3299ebdcee766cde92da7db3f2ca1d99c22f23`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 332.4 KB (332354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cabca92420dc637383da8dc8f0d0276fcf258532404ff1d3fb1e80473359b1`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; riscv64

```console
$ docker pull caddy@sha256:69328a1677b50e71a30c554ca8dddf7f1ad2474084385dabd7a0d6fedc9a4118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22851653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086f5adaba5ab0d6ae67e9e685607028248302272c9befb82e9fba4246d6537e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 02:12:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Thu, 14 May 2026 02:12:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV CADDY_VERSION=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_DATA_HOME=/data
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/udp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
WORKDIR /srv
# Thu, 14 May 2026 02:12:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a638da60daf650b51909ed97e65ca82d6b4c622d9aad9e05a1fe86e41b1b8`  
		Last Modified: Thu, 14 May 2026 02:13:15 GMT  
		Size: 3.0 MB (3024903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e9ab663ff84756b43ea4456b9675a7bb4e9a21db93cfb2860477f1acc49fa3`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 7.5 KB (7506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207dafa63c1803835db9d283a462accf88a7d65b6c6a62ef6d00c05e7e2d4d85`  
		Last Modified: Thu, 14 May 2026 02:13:17 GMT  
		Size: 16.2 MB (16231550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:2a37fc42537c780173072b08a797af48db02d1ca4bb14afe8301f380deb5f108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1087260f2ba70b75cfc134c58bb57369b570c4c836ad26b8a6774cfb2c421a26`

```dockerfile
```

-	Layers:
	-	`sha256:50741c878fc4519cf8be95491297cbbf12889e7fe8fe4cb6f0cb7a32aacd5a4d`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 332.4 KB (332350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074f80835103901f06cabe60ac917a34ae1a55cf6637768028867d83f6f31640`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:2be760d0b6dcefcee4d8e8de79e4fbc5bff379cc71f6ba4be329b95fee14ed53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23338359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bb7983fab4c669751406633c3cd0bacc33744d3c43dcecd96b365041e7d3b5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:39:41 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:39:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:39:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cb0bfcc1c8a81033ff4911e9096b260f4711f66484b04586fd6fa5ca95e44f`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 3.0 MB (3010703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bd7ba8a52c9fc9419b92337580db55dcd8690a637184fb22bec4871ffb8c0`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798a8d976afd31ca55ef92d83a93374f6c3e7ccd3add31769d768349700d623`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 16.6 MB (16593589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2` - unknown; unknown

```console
$ docker pull caddy@sha256:4a728924f65d2a9612ff66fbadd33d9a2d6e6b198cfc95cd6b23b89948cc2a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43f0c042f1bc3d80c67c0b0ad7df18ed102df0765f312c2619bed3d8392597`

```dockerfile
```

-	Layers:
	-	`sha256:4b3e6e6b8593dd35d4f0b59b89b012680c12c5498a7b01ae16bcb7ed34ac49a8`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 332.3 KB (332296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3864730b4cf584aa87e923de4848636482e8621df04a87733e10e42cc44e9b3`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:672b320378b1e89dde74d15a8a123068d26dafce6901597f4f8a837c5c38e7b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141244276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a5337ff6c38ebefe95a0943a39f42bab87a62f05d840422d53a0be69b65f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:59:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:59:25 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:59:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:59:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:59:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:59:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:59:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 80
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 443
# Tue, 12 May 2026 23:59:42 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:59:43 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:59:48 GMT
RUN caddy version
# Tue, 12 May 2026 23:59:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be1f105178ea258d105ecbaf5ec1f6000c5b289826e3b432c22080c650f719`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 524.5 KB (524474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7902ee53436295b9cb02bfa64ac6aa3b314c1e926ec77f7bb59eea811e28a846`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170554e1bf42badb647bc34b5718a5915fede948183bf5dc3d0d21e5540a0b67`  
		Last Modified: Wed, 13 May 2026 00:00:00 GMT  
		Size: 17.9 MB (17925247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a6d017c1aab65f96bd924d664427c093dba8210995905eaf00df2fbd142cb`  
		Last Modified: Tue, 12 May 2026 23:59:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04fc399abb90e3e2df99498e2eb88e7afd2a3f97e84400a40b7439ea46f1fa5`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d26c10fbf4dafe70c44037417bb3457e50a549f998a6f8b4799cf456c446e2`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295c37ba01761384092ce6a3f611a8792a57e0f772e6d8e3bfb099f51932a73`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb5b45ec93d301f781dc64b899fdfaa452f3d35dbbe0ba52fc5c87b02593d0`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0f84b59aead90c71aa95cd5340904935ff3da90339fa6ff21049d0f56f9ec`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1aeb5b58eaf433feb7668159802420e22345953cd345a111f5ff264e659bdf`  
		Last Modified: Tue, 12 May 2026 23:59:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03412a72c6ae737ad61b888338ad28fdc2b3477281195707e27619683236208`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a705083dc71361abc6a1e82aa158830dc6f3dd6e486a403f011f357eae4d884`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5637de44873a5862f646124e27d0fe311506c6fa1eec39c15df5312e1d41881`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4356db0d34adcecf1c9218951422411d7f942cb4d50621800af19388fdcc0`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a670d1e50cdca965f8cebdbf95f43d51e7fe8d7daf65312384a5731f3f743e`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc67002143e99034340b46a68c760d90626fe51d4e087bca7be0aa904ec8b45`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c8eddb6ea788613d96893c8e7c570d4a29a2b07f6d1ce823bf72faa05cf7b`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c21c96cd26011f147afe2c8c693897e2a126fbba132af7fc830d2d7559f19`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 351.6 KB (351565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c0ee074e227c1b13e1438189cfa031217727fc8085182b53234397774d341`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:86deaf5e3d3408a6ccec08fbb79989783dd26e206ae10bcf78a801dc8c9ab794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:3739ea4f0c877259a693d932693cf8f3408e9a9497c004f031b0e830e93e1546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23985030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5190456911cee510988a5fb9996188ef866fbcca3235cad19bf05f5f8f33386f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:12 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920de1d55d9880b00fbeaf8fa3757e89f7ea6170ff12633cbe766c2152a858d`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 2.9 MB (2886638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057c497bda068e80884e6836fbf8971a954593242af7694d080e6b81758b67f4`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b55c68e4a0feeeaec6f86ced6bd8790e19ed68399cff61bab00adc15895ec13`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 17.2 MB (17226669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e08c659e9fe301aa2814b2cafc4a5211423fcaa307a515772efeb816684ceb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cd52ea603ed29abf30a13e9ab37f92acffb93b53042a6bfaf1d22d9bdb8be`

```dockerfile
```

-	Layers:
	-	`sha256:4c4f094b32e82a0c66e0e5c00015a86d670049e4e9a336febc6c2a2fd626b19b`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 332.9 KB (332947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16285c7326d137b74e90d1f477040eb15643c312e7a46770316c0c258033326a`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:018595a3226de0d5c9055279af90983e9e91ca5f12dde17e93925455d19bc0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ce61ba53a04521d0e684e8048cde82ebd35cd3d72a9d1f7616056976e75253`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:40:51 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:40:52 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:40:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b1247b4f1cad33af22f46d45d07b1ee65401981dccc3fa920dafbde1fb072`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 2.8 MB (2819583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d84aa44715b44ce12b2cc9b98a20167ca060c5869ab67124210f554413d56ee`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93038fb49fb9d7664bc1a8209857cde656b4e5ff6ab5a7bf4b270d942f499d0`  
		Last Modified: Tue, 12 May 2026 21:41:00 GMT  
		Size: 16.3 MB (16311628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:de7fac8a337ded6fa61288d6dcc5837d472ed26f9d6b7230f0c8487fb9db984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feea7dba17177c5d72e8d8b883cd3bcdcda396dcc918c1e1e6d3868632932251`

```dockerfile
```

-	Layers:
	-	`sha256:2bd47793d94047373cab54d4b18f46ce16d19438827a8a41e3c5960cd1da48ca`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 18.4 KB (18353 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:2c3d3047a1705945ca9376ef8d3e9eb431f0f07f16e6ae2511326d7f0b664ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22262035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a70cfe7deb0544e9098ef10e20ebbc18e346bb3b8df5b140b9f184e71b4a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:42:08 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:42:09 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:42:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce55fb7d543ef0a1f852326909b7cdb22fb514199bd31b9543d92f04e878f4`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 2.7 MB (2681516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49caf58b5069e136a5fcd2fbaa18da4c786566963ba48bcedc27100b8a43365b`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ba28a73ebab4ca57472bca296d741e3d9b1cb27478c6adde87b7c314ba7810`  
		Last Modified: Tue, 12 May 2026 21:42:18 GMT  
		Size: 16.3 MB (16289861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:08ab34ff2df00fe711e074db26cf28e9b5ff1dbfe8355e0f414ed9a7c465cfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb11059736745812fc6bfa910b2d1cce68b03317d8452425d1f7954f2023f495`

```dockerfile
```

-	Layers:
	-	`sha256:95b578e25712b12ba424efc0abb0e6a4daa0cb6d145f200869796d863a0535dd`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 332.4 KB (332365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876e5685474ad9dfce16688d11127988be62753bb83e66c138c382a181530636`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 18.6 KB (18568 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ae38d5cc9674696bfec2dd7a20ea5495a2653d788ee39bff6aaf1007f8dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22800642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64000d357283f8b74cfc9cabce60768a6957447b74a7eb73c573c5d344a398`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:44:57 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:44:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:00 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6cabef06141e7f3aba6fa7d3898c4282f7316acb2ad612b8ea82ac9172cd99`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 2.9 MB (2900862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69f6bd08e27b5a1e9b73c99efae612626fabe895c78a156e402e5938112fff9`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 7.5 KB (7500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4e100b255f5c935bb23c7e5f2a23ee2b5b683a152149ad5db9b32d8455edf`  
		Last Modified: Tue, 12 May 2026 21:45:07 GMT  
		Size: 15.7 MB (15692378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:99d5c41f924f43a16554137091afc6dc8c34e2976b4011ea8793c6211676f8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 KB (351013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f8ace5e5ed9603a8a26766f5df8fd3efe32a76bb3d66c4017bf8bb842691c`

```dockerfile
```

-	Layers:
	-	`sha256:43c50900a0619c09f3987cc62bbfffd4d10da1b9d81fd21f3605e47dbb741967`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 332.4 KB (332401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e57f91d95d6c31886fc5dc74e74b86782c292b27bf964bb5023e301c36f8270`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d6f3adf638edd88132caec6005766ec86f31796069549755af52d172a03ebd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22551245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d82ac569eea06185f6688d103c7d7e2ef313dce067d6f1aca3b7255025aa450`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:46 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:52 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aba3acae7a944d3cb59ff0085839ecf6bc67e67a1ff5c9d62453ec36405516d`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 3.0 MB (3024677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef81e00b6b88436c8856bd7f6a2a40abea36897a22c7707cdf06722a09f8b819`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1e87608e2891184dfb2f547b0a2062b1bba1b787d3cd95ff36446affe940e`  
		Last Modified: Tue, 12 May 2026 21:46:12 GMT  
		Size: 15.7 MB (15688108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:863e023f3571814b385c37ac309e71a9a712f4aea420d2cea5032e2a362bf7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef881e7b8f82faab6a4473932499599574eb0bc9d0264c779647d0b099584f`

```dockerfile
```

-	Layers:
	-	`sha256:aa780bcad124738bdb6864e89c3299ebdcee766cde92da7db3f2ca1d99c22f23`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 332.4 KB (332354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cabca92420dc637383da8dc8f0d0276fcf258532404ff1d3fb1e80473359b1`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:69328a1677b50e71a30c554ca8dddf7f1ad2474084385dabd7a0d6fedc9a4118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22851653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086f5adaba5ab0d6ae67e9e685607028248302272c9befb82e9fba4246d6537e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 02:12:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Thu, 14 May 2026 02:12:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV CADDY_VERSION=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_DATA_HOME=/data
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/udp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
WORKDIR /srv
# Thu, 14 May 2026 02:12:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a638da60daf650b51909ed97e65ca82d6b4c622d9aad9e05a1fe86e41b1b8`  
		Last Modified: Thu, 14 May 2026 02:13:15 GMT  
		Size: 3.0 MB (3024903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e9ab663ff84756b43ea4456b9675a7bb4e9a21db93cfb2860477f1acc49fa3`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 7.5 KB (7506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207dafa63c1803835db9d283a462accf88a7d65b6c6a62ef6d00c05e7e2d4d85`  
		Last Modified: Thu, 14 May 2026 02:13:17 GMT  
		Size: 16.2 MB (16231550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2a37fc42537c780173072b08a797af48db02d1ca4bb14afe8301f380deb5f108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1087260f2ba70b75cfc134c58bb57369b570c4c836ad26b8a6774cfb2c421a26`

```dockerfile
```

-	Layers:
	-	`sha256:50741c878fc4519cf8be95491297cbbf12889e7fe8fe4cb6f0cb7a32aacd5a4d`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 332.4 KB (332350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074f80835103901f06cabe60ac917a34ae1a55cf6637768028867d83f6f31640`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:2be760d0b6dcefcee4d8e8de79e4fbc5bff379cc71f6ba4be329b95fee14ed53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23338359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bb7983fab4c669751406633c3cd0bacc33744d3c43dcecd96b365041e7d3b5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:39:41 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:39:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:39:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cb0bfcc1c8a81033ff4911e9096b260f4711f66484b04586fd6fa5ca95e44f`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 3.0 MB (3010703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bd7ba8a52c9fc9419b92337580db55dcd8690a637184fb22bec4871ffb8c0`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798a8d976afd31ca55ef92d83a93374f6c3e7ccd3add31769d768349700d623`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 16.6 MB (16593589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4a728924f65d2a9612ff66fbadd33d9a2d6e6b198cfc95cd6b23b89948cc2a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43f0c042f1bc3d80c67c0b0ad7df18ed102df0765f312c2619bed3d8392597`

```dockerfile
```

-	Layers:
	-	`sha256:4b3e6e6b8593dd35d4f0b59b89b012680c12c5498a7b01ae16bcb7ed34ac49a8`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 332.3 KB (332296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3864730b4cf584aa87e923de4848636482e8621df04a87733e10e42cc44e9b3`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:d57008618f743e6308058d7bd990eb3489dfd04e2b82978cca7b953e1b491fc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:db3ae9a5913d5b9305c729247b8ee6ca7596823a3a9419eaac330e5f374c3157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79773771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591706032a9a5c14da6e7f446e0083d6747768d50d0bf9da36e55c2421e94a2f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:53 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:11:59 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:00 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30edd47abbca5172a1775d1ba8a17aef65500a7a1ecc50af582706ad0c19ab`  
		Last Modified: Tue, 02 Jun 2026 21:45:09 GMT  
		Size: 290.2 KB (290247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaa626ba3010d60ab55d9cdc69c0b12ebff5d1b5ece83ff220fb46a7709b3b`  
		Last Modified: Tue, 02 Jun 2026 21:44:37 GMT  
		Size: 67.3 MB (67283031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abecc8ee46932a01c961a896c3c87dd0efe1301916e124bdac46f96ae6e9dee`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca4922139842e28e1d61aaac141bc8576337fa9b8d64d1d9f723d161fb30612`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 6.5 MB (6489213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fa1420c37ef3c625b9f14ee901574c588fc49b3eb5a8fca1a8a732fd47620b`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 1.8 MB (1846501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e306254cc3a4dab0c2ccd0f548ad566fa5aa81a412b9b432d81889526a2bbf2`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ddd773e864a4f4e091e1f4bfdbd60371b4c51910be5ccb610589b8a6883de8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4dc9d9bcee8d699bb42f311997ea36c642596e4004aa8859d0781b30ac2c9d`

```dockerfile
```

-	Layers:
	-	`sha256:d055d9682529a9387da6c4adbc8bdc265d0466484002fca96e29c90f179091be`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 280.8 KB (280776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490b4b762d29e23f9c30e7d63d2f4fde87253b5f126903cfd336647e4cf6c3af`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67c97e86bbcf6c6d84c8a191e6f9c07550c3ff25bfef23d3e8ee6a6407d6d801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77801132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8375fe7e15b17bead87deaac11514fa70da1cd8427509b1c228967a15f141eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:01 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:15:26 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:15:27 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:15:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dc79104d8e3b9e93b7ff3163839b44dd0979c52b2f81f68e01be8f60d9d090`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 291.0 KB (291036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb989b4b1329f80799d899b8d7259a6658047b39b2b670ed0cc8620dd1d357c`  
		Last Modified: Tue, 02 Jun 2026 21:44:18 GMT  
		Size: 65.8 MB (65785954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e947158a0266891a134507f0a6253aec12f2c7656af2daefbed99f399148f5`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620327b269f4fa8f6e186115a4ab2a342dedb497a9044abd4a5b3246f11d3ac3`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 6.4 MB (6406685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a7c7f37dd2ddabcd39c4ec78c16b8efaf799e1db677a0a88c55ba2bd16132e`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037287d5c994a910febeca5542dc101d590c0256e293e25e7ddb97f4b25eba7b`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ee8a613597922f4a0c6ad805948acd213e018eb8e3548ca5b98e7cb6c0410659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a997af74d3004a92cc163aa5d9f843ecd7552d9fad60e39cc23d5f4340ebdbd1`

```dockerfile
```

-	Layers:
	-	`sha256:b77f8ee7de0cc1af47105376a1a978c3bd700001392879cba9b348c38f53c909`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:081203e78dbbdf584d644a704dbce3dd01e8d923760b1e4160a615e9c0282f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cece6d48bcb1d2e37ff13a3299d3382dd7c3a18c66cd620c334b6e7e45b85c5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:51 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:54 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:48 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa788fec666273423bc95c719209c3f49b0d2c1c28fdaf669e4ebcab932954`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 290.2 KB (290169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f46eeae83dd5d801ff20835cd1ea98f630698b9c066e10ddf320a1c9d42c07`  
		Last Modified: Tue, 02 Jun 2026 21:45:10 GMT  
		Size: 65.8 MB (65786124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494a0eb08b28e7075149245f5ff666eeadec03e6b1b08870ad1caa24151d00b`  
		Last Modified: Tue, 02 Jun 2026 21:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba6d2d27897ace71b8214e93839ab4dddfb4bf51e5dd9871755073b452fd92`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 5.9 MB (5859405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d200f1ff9040ab5ed074d40e2c5d715e5ca869a8c3c9ca357f24b30cc08f2`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 1.7 MB (1738762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392245d1b10f490bef242becdaf6b658edb173425508af51312e2d0c7703b3c5`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0207715e319528107b0ca90c4b3ae044a8636067b8544656cf7cfa660dbd93d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd6848c1a5afb6c01dd7ed0eea80f86a4053eb96a8d94f50bbb86131989d4a`

```dockerfile
```

-	Layers:
	-	`sha256:dda72704ff023245a1d0202ebcabc8675ff1d722be6ba03fec1b7ce479c3a68c`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 283.2 KB (283168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac1a6806382a02068a2684ad9fc775685c890f3913b65b2de640fe3eca324e6`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:13da9d8308a65d8402c19528f51e19a2535fcd2f28ee893feabfefab09afb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76951883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114e448de61888adef08f63408e9426eb63ce6db5c2c1066219d9ba0222717c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2c0198c180cf41cbfd73e25946fc0ccc373d0fee89deb6e7eeec7b1f8612ee`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 292.9 KB (292861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477eaf154b7c8070862d9db01681f78c8a60ce90e8936310f6a906696df475a`  
		Last Modified: Tue, 02 Jun 2026 21:43:59 GMT  
		Size: 64.2 MB (64166971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb4739b26b76346d1281fb8fac14c5bc8025bfc580405cc95aa21736e41116`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e7c04c5116e56a4edea922d39e62c3fe0cfb06ee580b89926af1db83402ce`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 6.6 MB (6575206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57c7a67944f4fa914947979e30a6c1db54ab3c9b1aac79a9ebd7b36e8e39b0`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 1.7 MB (1716384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ee51343f308260ed7fa9020154c216542e21fd2589bc41d85b57f77166a81`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ce914fd434a8d09e7d2f73c5c9b354b42cf9c31d65fefbe292f23eacb6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 KB (300526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbed50fbf772e7e0ff9b816eb3a8dc3e213df0f8c75ba10dc5924412b0e4d841`

```dockerfile
```

-	Layers:
	-	`sha256:add9c054a1ac3653aed38da164cb08126bb46bb4bc153c6f12848191bed15b4b`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 280.2 KB (280230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838bb928d6772b6ebe8d87d60a85b358fd40eb2166c93cb622cee8a22a537ca3`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:658d12b9b7e489cdf05a0115f8fd9c8e392ee3160ba5b96d5f6b1e3cf0e02802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2568f1df66f499486924dad3ad55e9449d549bbb37426e3354addf15c6c7df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:42:40 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:18 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:19:34 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:19:35 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:19:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94153723d1545849cb54e33c3f8f977f110afcb00da0d5d32236b24537c1a4a3`  
		Last Modified: Tue, 02 Jun 2026 21:43:46 GMT  
		Size: 64.8 MB (64840550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4ff149d61b69213dc146324696a7a3af1a2b46684c6f928dfca1ae8489a0e`  
		Last Modified: Tue, 02 Jun 2026 21:44:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3cb06425959c67588985a91f934858685c3d7e6f0a3094af6c96ef93508d2`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 6.9 MB (6906465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966eded362018ac5d0b34cafa47d109cf32bbdeac194c1582640c28fd31f3cb0`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 1.7 MB (1705993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88bcc980b0c8d2d3de3ae12ec5a268bf23ac450cf0e10b8726131fa5f50dd3a`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:636aaf3183699721a688bf9903f4a642af3556d22fb14b8142bb3d77e9e02f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4888dfc41af739498c0157e20326f403f56cd8400b521203907e2cce1bfb8403`

```dockerfile
```

-	Layers:
	-	`sha256:00729d38b67285f7a79eb306240810accdabec647d996c8e36ab458f490a827c`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 280.2 KB (280199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ec6cfbc1bfecb50f2c2e12352351ad7a86aa62458697127bd6d635c92ce4cb`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:851cb908798b1538ffe3a3053bb98a32903f158a7f1ca9eeafb0fa30f6f34f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77424217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfc4a9d5f64621b356f7b47c6c48337fe32d5912cfc96a0484d5c999eabca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 23:12:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 23:12:42 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
WORKDIR /go
# Wed, 03 Jun 2026 05:24:30 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 05:24:32 GMT
ENV CADDY_VERSION=v2.11.3
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 05:24:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8f135b9aec9b42cabcdbc9e60e1e2b738fe71cb50c44dd091c53fb8edc94a`  
		Last Modified: Tue, 02 Jun 2026 23:19:15 GMT  
		Size: 65.1 MB (65148394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c4848fcf3e91f4413c1666bace4337c4f1c12c50976959bd29ad011c4d936`  
		Last Modified: Tue, 02 Jun 2026 23:22:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc28d768f2c71e4a402e2f4424963bfaa465d9c4a2f36c428bd41b08e3d6d2d`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 6.7 MB (6672809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5d5e4441c4e23a30ad21c2b66c3a336df57c4bfda44ff5113b5b3be8e2ffc`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 1.7 MB (1724208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80fdf8a500696ba07bd03f2a260b2e578f3e7909bec500d7122de9d25041d6`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:dca192295748614e125d445ca613cc0972469b2e1774dca65dd6b47fe9d2682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a911353b6377828995df9827f453d124992e5ff9b7484ef6ebc4da9d7258c820`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc98528c0380ded7049be92a37c9302d44d983dd53bba1648e04dedd55efb4`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 280.2 KB (280195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb92a4e503b3fefa7c0f01279adf8084dd01665b4d68fcef6d623b33d866cb16`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:4b90e008693f441e0c5337ba3fedad55597c1c61e2ecf25f2241f3a878b58d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cee611b412138469260e614e91691e6b1868b70e66aabd6488d8013d7cf3ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:02 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:13:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:13:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95f9225fe123215e56024e7fcaa3f2eb9fb3081c2d6160ebae532ca6d5eefd`  
		Last Modified: Tue, 02 Jun 2026 21:43:22 GMT  
		Size: 66.5 MB (66513822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9138885877e3f590d4144dfc2ec737113acde73b99374df82c5be8c2901f3dd`  
		Last Modified: Tue, 02 Jun 2026 21:43:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91584af5ed277f32349e17cda1214326d518b9f94719dc5c4e741329ee86f375`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 6.8 MB (6779991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30090c473a211354bad44ab67b863187e6614231a73dcf0aa22173ee79b1a359`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 1.8 MB (1782842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3da51a38e8b113b744ea5418d02a52a6b6def3db40a219f602fa5e52065bfb`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:578a971dec1e6528eb9512ec7c3c538b18cbeb2a8d6c72b4f420d6992b30009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f17854159ec165c92bf0e0220d91246d07bd68f48b8fa569c16a68552d0058`

```dockerfile
```

-	Layers:
	-	`sha256:4915df098870636a12ece0bc09cc5fc8dee8954c6116a7cfb93bf9f3169bd426`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 280.1 KB (280125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97af12336dd47a218f778a32b9bf8cf6ecc4d8ef33a28f7bb8c621a730e6343b`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:6bac99d1de9debbb801646208c923809fe18cbb945c6d430cc8f1d38c5ba14ff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335210672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45bc764ed6ce43900c66e7269ef9b64bff9f78aca8a5412c2bdddba4456a779`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 21:46:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 21:47:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 21:47:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 21:47:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 21:47:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 21:48:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:48:54 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 21:49:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 21:49:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:50:55 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:50:57 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:33:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:33:57 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:33:58 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:33:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:34:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:34:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03db002b9e59a168b97269178d3cea6be969a491719ca1c8d3f4c33ad9ad07f7`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b9c42b86ca2e7aa4eb41766a6f755119c65c8b2c03b320ba0980b9d2f6547a`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8f4def2bce82d1e544606aaf3e5895ae29437220f1b41211727fbeff83ac8`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16228e0f3edb3815e34fd2d8c6d575e9ed737e1d5cc07909e430d670860bc7cc`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca5f94c0122485a7417a90a87018bf739ef6ef80f60454b5258cefa6a58eed5`  
		Last Modified: Tue, 02 Jun 2026 21:51:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1397a64df19d921e6ad74f8c6ca0ea5b401c7731318c4dd85002c5dbb6df922c`  
		Last Modified: Tue, 02 Jun 2026 21:51:15 GMT  
		Size: 51.3 MB (51286214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871cad50024619c7f067652dc3cc2e678a8c70180235a578d249123c21479637`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007a76e9414e0db486efb9ff5a4409e15cef9f66f3c19a6efc5d554db55f0e4b`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 367.1 KB (367144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fea8e7d4ba560522bf09b19a63fc47cca6a724baa7e90623086a8d46f1d8f2`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44107094e22c635252ccb6df8685c7968f63f084760fcbec0f4cb08857a74`  
		Last Modified: Tue, 02 Jun 2026 21:51:19 GMT  
		Size: 75.3 MB (75252822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35936631b6cd9bd6e5cf14e0cb4f8a287786047d069c23d09ed69d69e5672e`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfefceaacb32ce75c4aaba58b81bced50aae117cc616944d49a92ce10e866b2`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d897cbe5e09e88bd391baaa18698e2d8eb277aa581a683b8025c4f230f1adf7e`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4b32c912e804ac74f332ad5ab2d2b281dc7e6d481f6f80a4f43df475616659`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f053ec3b21275df3413b9168645d21fb9bb677da4c1d6c12e96049e54cabfcd`  
		Last Modified: Tue, 02 Jun 2026 22:34:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b1f65dcb82cba9c705872f745be1ac11720b8c76eebbe4e9942f2f2e810cf7`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 2.3 MB (2345713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcd5aef19be6456c21bb9609b574709a6500a0642321c9435e2421d39818fd`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:5c6e7364201194ab26b433feaf24cec26dd47fa67d0191fd5aac9a3145f2d75a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2246342426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4817db1df805c59c442b0aae0af3740b59c437f926600e3382586defd6c6bd84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 22:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:11:59 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 22:12:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 22:12:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 22:13:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:13:36 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 22:13:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 22:13:43 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 22:15:53 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:15:55 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:48:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:48:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:48:17 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:48:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:48:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:48:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16556704259948e469d295ad17c0b83303b045ecaedafdd2e16e153313e1dfb6`  
		Last Modified: Tue, 02 Jun 2026 22:16:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d711fc9f348f8b578e18995374d27b40e5900dd346ce6989dbf8a03d6379ed3`  
		Last Modified: Tue, 02 Jun 2026 22:16:04 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591205aec584bc9bf82bf950d86511bf856df5b80cfc692ffebf5597ca68b7e6`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22c20181a321c9aa31806b3a6299f064d89d5be9ef4ec4b8643e9648f096b20`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875bb11e80c093d7133bdc63d9eae1ac2b5c3615c2548955f18ce7dc1cbcdd1`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec55ad5b4586a55352fbd4acd5057d226c2736b7bf5617ba58c7b1ec5a01595`  
		Last Modified: Tue, 02 Jun 2026 22:16:08 GMT  
		Size: 51.4 MB (51351865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8157f646be5f683d250a6f17ff707476c9c8021878b249e269ce011d3ff874db`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363dcd54d5e980b27d8e067e3aa0681d0a3b914f0cd2fee65597fc3cc09fecb3`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 347.5 KB (347472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89e7d73520ffce5ef45fce95d33eb59c6e81aa2a9b702762d10955702c63f88`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03786a5498c3138a7f68d31bb4b48bba38614a87e19b581dfb213237d20256`  
		Last Modified: Tue, 02 Jun 2026 22:16:12 GMT  
		Size: 69.9 MB (69908615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717522dbb34fae4042da878f0e2b02e156afeb7efa63dd68f87a0e670c1777a0`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c100a71c72bd8a3ae733ff302b773d79c1f9d9567e2ea92e5a14cabfad16946`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973c59f163b420ad3e89ff70cbb614dd936a7c672446a4f96680cf7ea2033b1`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23746fb5a19760542ceaf1982c31d671001d1e61c45ef53459e38fe02213c2`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d27ae839dc6cc7d7a119bd9b2c302ae49b265e40e36003baed2d882a8b80f`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415c477003a7c45c620ddf022beae3a2649f87cdd579da1617144d132e961953`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 2.3 MB (2296661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5287c072e6ec74e531802fe71a613d30d89698c4a47bc8e3f1ca00ee98a1249a`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:3eae6b351ecdb05da6d16e341261a457692d344a435764c5ece7a60cf03a23f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:db3ae9a5913d5b9305c729247b8ee6ca7596823a3a9419eaac330e5f374c3157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79773771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591706032a9a5c14da6e7f446e0083d6747768d50d0bf9da36e55c2421e94a2f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:53 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:11:59 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:00 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30edd47abbca5172a1775d1ba8a17aef65500a7a1ecc50af582706ad0c19ab`  
		Last Modified: Tue, 02 Jun 2026 21:45:09 GMT  
		Size: 290.2 KB (290247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaa626ba3010d60ab55d9cdc69c0b12ebff5d1b5ece83ff220fb46a7709b3b`  
		Last Modified: Tue, 02 Jun 2026 21:44:37 GMT  
		Size: 67.3 MB (67283031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abecc8ee46932a01c961a896c3c87dd0efe1301916e124bdac46f96ae6e9dee`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca4922139842e28e1d61aaac141bc8576337fa9b8d64d1d9f723d161fb30612`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 6.5 MB (6489213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fa1420c37ef3c625b9f14ee901574c588fc49b3eb5a8fca1a8a732fd47620b`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 1.8 MB (1846501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e306254cc3a4dab0c2ccd0f548ad566fa5aa81a412b9b432d81889526a2bbf2`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ddd773e864a4f4e091e1f4bfdbd60371b4c51910be5ccb610589b8a6883de8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4dc9d9bcee8d699bb42f311997ea36c642596e4004aa8859d0781b30ac2c9d`

```dockerfile
```

-	Layers:
	-	`sha256:d055d9682529a9387da6c4adbc8bdc265d0466484002fca96e29c90f179091be`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 280.8 KB (280776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490b4b762d29e23f9c30e7d63d2f4fde87253b5f126903cfd336647e4cf6c3af`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67c97e86bbcf6c6d84c8a191e6f9c07550c3ff25bfef23d3e8ee6a6407d6d801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77801132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8375fe7e15b17bead87deaac11514fa70da1cd8427509b1c228967a15f141eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:01 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:15:26 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:15:27 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:15:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dc79104d8e3b9e93b7ff3163839b44dd0979c52b2f81f68e01be8f60d9d090`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 291.0 KB (291036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb989b4b1329f80799d899b8d7259a6658047b39b2b670ed0cc8620dd1d357c`  
		Last Modified: Tue, 02 Jun 2026 21:44:18 GMT  
		Size: 65.8 MB (65785954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e947158a0266891a134507f0a6253aec12f2c7656af2daefbed99f399148f5`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620327b269f4fa8f6e186115a4ab2a342dedb497a9044abd4a5b3246f11d3ac3`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 6.4 MB (6406685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a7c7f37dd2ddabcd39c4ec78c16b8efaf799e1db677a0a88c55ba2bd16132e`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037287d5c994a910febeca5542dc101d590c0256e293e25e7ddb97f4b25eba7b`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ee8a613597922f4a0c6ad805948acd213e018eb8e3548ca5b98e7cb6c0410659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a997af74d3004a92cc163aa5d9f843ecd7552d9fad60e39cc23d5f4340ebdbd1`

```dockerfile
```

-	Layers:
	-	`sha256:b77f8ee7de0cc1af47105376a1a978c3bd700001392879cba9b348c38f53c909`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:081203e78dbbdf584d644a704dbce3dd01e8d923760b1e4160a615e9c0282f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cece6d48bcb1d2e37ff13a3299d3382dd7c3a18c66cd620c334b6e7e45b85c5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:51 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:54 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:48 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa788fec666273423bc95c719209c3f49b0d2c1c28fdaf669e4ebcab932954`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 290.2 KB (290169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f46eeae83dd5d801ff20835cd1ea98f630698b9c066e10ddf320a1c9d42c07`  
		Last Modified: Tue, 02 Jun 2026 21:45:10 GMT  
		Size: 65.8 MB (65786124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494a0eb08b28e7075149245f5ff666eeadec03e6b1b08870ad1caa24151d00b`  
		Last Modified: Tue, 02 Jun 2026 21:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba6d2d27897ace71b8214e93839ab4dddfb4bf51e5dd9871755073b452fd92`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 5.9 MB (5859405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d200f1ff9040ab5ed074d40e2c5d715e5ca869a8c3c9ca357f24b30cc08f2`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 1.7 MB (1738762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392245d1b10f490bef242becdaf6b658edb173425508af51312e2d0c7703b3c5`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0207715e319528107b0ca90c4b3ae044a8636067b8544656cf7cfa660dbd93d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd6848c1a5afb6c01dd7ed0eea80f86a4053eb96a8d94f50bbb86131989d4a`

```dockerfile
```

-	Layers:
	-	`sha256:dda72704ff023245a1d0202ebcabc8675ff1d722be6ba03fec1b7ce479c3a68c`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 283.2 KB (283168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac1a6806382a02068a2684ad9fc775685c890f3913b65b2de640fe3eca324e6`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:13da9d8308a65d8402c19528f51e19a2535fcd2f28ee893feabfefab09afb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76951883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114e448de61888adef08f63408e9426eb63ce6db5c2c1066219d9ba0222717c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2c0198c180cf41cbfd73e25946fc0ccc373d0fee89deb6e7eeec7b1f8612ee`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 292.9 KB (292861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477eaf154b7c8070862d9db01681f78c8a60ce90e8936310f6a906696df475a`  
		Last Modified: Tue, 02 Jun 2026 21:43:59 GMT  
		Size: 64.2 MB (64166971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb4739b26b76346d1281fb8fac14c5bc8025bfc580405cc95aa21736e41116`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e7c04c5116e56a4edea922d39e62c3fe0cfb06ee580b89926af1db83402ce`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 6.6 MB (6575206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57c7a67944f4fa914947979e30a6c1db54ab3c9b1aac79a9ebd7b36e8e39b0`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 1.7 MB (1716384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ee51343f308260ed7fa9020154c216542e21fd2589bc41d85b57f77166a81`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ce914fd434a8d09e7d2f73c5c9b354b42cf9c31d65fefbe292f23eacb6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 KB (300526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbed50fbf772e7e0ff9b816eb3a8dc3e213df0f8c75ba10dc5924412b0e4d841`

```dockerfile
```

-	Layers:
	-	`sha256:add9c054a1ac3653aed38da164cb08126bb46bb4bc153c6f12848191bed15b4b`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 280.2 KB (280230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838bb928d6772b6ebe8d87d60a85b358fd40eb2166c93cb622cee8a22a537ca3`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:658d12b9b7e489cdf05a0115f8fd9c8e392ee3160ba5b96d5f6b1e3cf0e02802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2568f1df66f499486924dad3ad55e9449d549bbb37426e3354addf15c6c7df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:42:40 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:18 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:19:34 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:19:35 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:19:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94153723d1545849cb54e33c3f8f977f110afcb00da0d5d32236b24537c1a4a3`  
		Last Modified: Tue, 02 Jun 2026 21:43:46 GMT  
		Size: 64.8 MB (64840550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4ff149d61b69213dc146324696a7a3af1a2b46684c6f928dfca1ae8489a0e`  
		Last Modified: Tue, 02 Jun 2026 21:44:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3cb06425959c67588985a91f934858685c3d7e6f0a3094af6c96ef93508d2`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 6.9 MB (6906465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966eded362018ac5d0b34cafa47d109cf32bbdeac194c1582640c28fd31f3cb0`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 1.7 MB (1705993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88bcc980b0c8d2d3de3ae12ec5a268bf23ac450cf0e10b8726131fa5f50dd3a`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:636aaf3183699721a688bf9903f4a642af3556d22fb14b8142bb3d77e9e02f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4888dfc41af739498c0157e20326f403f56cd8400b521203907e2cce1bfb8403`

```dockerfile
```

-	Layers:
	-	`sha256:00729d38b67285f7a79eb306240810accdabec647d996c8e36ab458f490a827c`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 280.2 KB (280199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ec6cfbc1bfecb50f2c2e12352351ad7a86aa62458697127bd6d635c92ce4cb`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:851cb908798b1538ffe3a3053bb98a32903f158a7f1ca9eeafb0fa30f6f34f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77424217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfc4a9d5f64621b356f7b47c6c48337fe32d5912cfc96a0484d5c999eabca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 23:12:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 23:12:42 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
WORKDIR /go
# Wed, 03 Jun 2026 05:24:30 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 05:24:32 GMT
ENV CADDY_VERSION=v2.11.3
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 05:24:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8f135b9aec9b42cabcdbc9e60e1e2b738fe71cb50c44dd091c53fb8edc94a`  
		Last Modified: Tue, 02 Jun 2026 23:19:15 GMT  
		Size: 65.1 MB (65148394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c4848fcf3e91f4413c1666bace4337c4f1c12c50976959bd29ad011c4d936`  
		Last Modified: Tue, 02 Jun 2026 23:22:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc28d768f2c71e4a402e2f4424963bfaa465d9c4a2f36c428bd41b08e3d6d2d`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 6.7 MB (6672809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5d5e4441c4e23a30ad21c2b66c3a336df57c4bfda44ff5113b5b3be8e2ffc`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 1.7 MB (1724208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80fdf8a500696ba07bd03f2a260b2e578f3e7909bec500d7122de9d25041d6`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:dca192295748614e125d445ca613cc0972469b2e1774dca65dd6b47fe9d2682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a911353b6377828995df9827f453d124992e5ff9b7484ef6ebc4da9d7258c820`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc98528c0380ded7049be92a37c9302d44d983dd53bba1648e04dedd55efb4`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 280.2 KB (280195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb92a4e503b3fefa7c0f01279adf8084dd01665b4d68fcef6d623b33d866cb16`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4b90e008693f441e0c5337ba3fedad55597c1c61e2ecf25f2241f3a878b58d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cee611b412138469260e614e91691e6b1868b70e66aabd6488d8013d7cf3ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:02 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:13:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:13:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95f9225fe123215e56024e7fcaa3f2eb9fb3081c2d6160ebae532ca6d5eefd`  
		Last Modified: Tue, 02 Jun 2026 21:43:22 GMT  
		Size: 66.5 MB (66513822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9138885877e3f590d4144dfc2ec737113acde73b99374df82c5be8c2901f3dd`  
		Last Modified: Tue, 02 Jun 2026 21:43:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91584af5ed277f32349e17cda1214326d518b9f94719dc5c4e741329ee86f375`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 6.8 MB (6779991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30090c473a211354bad44ab67b863187e6614231a73dcf0aa22173ee79b1a359`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 1.8 MB (1782842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3da51a38e8b113b744ea5418d02a52a6b6def3db40a219f602fa5e52065bfb`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:578a971dec1e6528eb9512ec7c3c538b18cbeb2a8d6c72b4f420d6992b30009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f17854159ec165c92bf0e0220d91246d07bd68f48b8fa569c16a68552d0058`

```dockerfile
```

-	Layers:
	-	`sha256:4915df098870636a12ece0bc09cc5fc8dee8954c6116a7cfb93bf9f3169bd426`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 280.1 KB (280125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97af12336dd47a218f778a32b9bf8cf6ecc4d8ef33a28f7bb8c621a730e6343b`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:2507e19ef745b79bb6d80853a1f496cf6ccc33b2952dd338d29574b3a40b7817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:5c6e7364201194ab26b433feaf24cec26dd47fa67d0191fd5aac9a3145f2d75a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2246342426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4817db1df805c59c442b0aae0af3740b59c437f926600e3382586defd6c6bd84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 22:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:11:59 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 22:12:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 22:12:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 22:13:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:13:36 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 22:13:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 22:13:43 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 22:15:53 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:15:55 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:48:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:48:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:48:17 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:48:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:48:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:48:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16556704259948e469d295ad17c0b83303b045ecaedafdd2e16e153313e1dfb6`  
		Last Modified: Tue, 02 Jun 2026 22:16:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d711fc9f348f8b578e18995374d27b40e5900dd346ce6989dbf8a03d6379ed3`  
		Last Modified: Tue, 02 Jun 2026 22:16:04 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591205aec584bc9bf82bf950d86511bf856df5b80cfc692ffebf5597ca68b7e6`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22c20181a321c9aa31806b3a6299f064d89d5be9ef4ec4b8643e9648f096b20`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875bb11e80c093d7133bdc63d9eae1ac2b5c3615c2548955f18ce7dc1cbcdd1`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec55ad5b4586a55352fbd4acd5057d226c2736b7bf5617ba58c7b1ec5a01595`  
		Last Modified: Tue, 02 Jun 2026 22:16:08 GMT  
		Size: 51.4 MB (51351865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8157f646be5f683d250a6f17ff707476c9c8021878b249e269ce011d3ff874db`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363dcd54d5e980b27d8e067e3aa0681d0a3b914f0cd2fee65597fc3cc09fecb3`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 347.5 KB (347472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89e7d73520ffce5ef45fce95d33eb59c6e81aa2a9b702762d10955702c63f88`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03786a5498c3138a7f68d31bb4b48bba38614a87e19b581dfb213237d20256`  
		Last Modified: Tue, 02 Jun 2026 22:16:12 GMT  
		Size: 69.9 MB (69908615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717522dbb34fae4042da878f0e2b02e156afeb7efa63dd68f87a0e670c1777a0`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c100a71c72bd8a3ae733ff302b773d79c1f9d9567e2ea92e5a14cabfad16946`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973c59f163b420ad3e89ff70cbb614dd936a7c672446a4f96680cf7ea2033b1`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23746fb5a19760542ceaf1982c31d671001d1e61c45ef53459e38fe02213c2`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d27ae839dc6cc7d7a119bd9b2c302ae49b265e40e36003baed2d882a8b80f`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415c477003a7c45c620ddf022beae3a2649f87cdd579da1617144d132e961953`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 2.3 MB (2296661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5287c072e6ec74e531802fe71a613d30d89698c4a47bc8e3f1ca00ee98a1249a`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:688be35a61ebeccf90e1956f0225b3db0280e79964863fe7b93addc0864838fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:6bac99d1de9debbb801646208c923809fe18cbb945c6d430cc8f1d38c5ba14ff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335210672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45bc764ed6ce43900c66e7269ef9b64bff9f78aca8a5412c2bdddba4456a779`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 21:46:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 21:47:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 21:47:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 21:47:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 21:47:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 21:48:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:48:54 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 21:49:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 21:49:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:50:55 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:50:57 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:33:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:33:57 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:33:58 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:33:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:34:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:34:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03db002b9e59a168b97269178d3cea6be969a491719ca1c8d3f4c33ad9ad07f7`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b9c42b86ca2e7aa4eb41766a6f755119c65c8b2c03b320ba0980b9d2f6547a`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8f4def2bce82d1e544606aaf3e5895ae29437220f1b41211727fbeff83ac8`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16228e0f3edb3815e34fd2d8c6d575e9ed737e1d5cc07909e430d670860bc7cc`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca5f94c0122485a7417a90a87018bf739ef6ef80f60454b5258cefa6a58eed5`  
		Last Modified: Tue, 02 Jun 2026 21:51:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1397a64df19d921e6ad74f8c6ca0ea5b401c7731318c4dd85002c5dbb6df922c`  
		Last Modified: Tue, 02 Jun 2026 21:51:15 GMT  
		Size: 51.3 MB (51286214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871cad50024619c7f067652dc3cc2e678a8c70180235a578d249123c21479637`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007a76e9414e0db486efb9ff5a4409e15cef9f66f3c19a6efc5d554db55f0e4b`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 367.1 KB (367144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fea8e7d4ba560522bf09b19a63fc47cca6a724baa7e90623086a8d46f1d8f2`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44107094e22c635252ccb6df8685c7968f63f084760fcbec0f4cb08857a74`  
		Last Modified: Tue, 02 Jun 2026 21:51:19 GMT  
		Size: 75.3 MB (75252822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35936631b6cd9bd6e5cf14e0cb4f8a287786047d069c23d09ed69d69e5672e`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfefceaacb32ce75c4aaba58b81bced50aae117cc616944d49a92ce10e866b2`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d897cbe5e09e88bd391baaa18698e2d8eb277aa581a683b8025c4f230f1adf7e`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4b32c912e804ac74f332ad5ab2d2b281dc7e6d481f6f80a4f43df475616659`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f053ec3b21275df3413b9168645d21fb9bb677da4c1d6c12e96049e54cabfcd`  
		Last Modified: Tue, 02 Jun 2026 22:34:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b1f65dcb82cba9c705872f745be1ac11720b8c76eebbe4e9942f2f2e810cf7`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 2.3 MB (2345713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcd5aef19be6456c21bb9609b574709a6500a0642321c9435e2421d39818fd`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-nanoserver`

```console
$ docker pull caddy@sha256:99fae4af425b9fcc81d4b2efd241cbe3dcac78350f37c4ed2daa6c35df2793df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:2-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:3e5afaeda3465c585afea0828ec650f60e760f92ab1096cbdd12bbb7044f93f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217870731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4c6463b2201d0e16cdf07c19f7038d51083193293932e21b857521bf02bab9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:30:16 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:30:18 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:30:22 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:30:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:30:33 GMT
RUN caddy version
# Wed, 13 May 2026 00:30:33 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1fedb6255043325f0c6a8118656684fcc0c1eb9b84857ff574105bdd45da85`  
		Last Modified: Wed, 13 May 2026 00:30:44 GMT  
		Size: 71.9 KB (71893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde99a62b5456da395a4f921712e08ec242d9c53791f22763e904483b90bb0ff`  
		Last Modified: Wed, 13 May 2026 00:30:46 GMT  
		Size: 17.5 MB (17549616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfaf73426fda2a4ab3e9ef51a62f30bf03cd7bb09987eaed20cca2f4baf6c72`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 271.7 KB (271708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee506f35cf26ab6a4307a617c899a31108d35a38976dcbace37f776be3fa88b9`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 111.9 KB (111876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae64a8691f6412e9e7b124cb1506d63cbc0888dfda70af2a058cd92483d1bf3`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e08e3975dc80abab1d7078a935b8310dfd0436900117ac019cf7e74e96327`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa53d7a29128e22ba5071bc2c061d21df2672618f2d335495eee03b57b30eec9`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9aa3dda4800660b0c498edee92d63a95f3487dea910ee7b1e32237e7d8c01`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602df0b26626bd70f3e3b7e338c29f3774aadcb1993b32e11424961d5818b71`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c12f0b0a957349df9e5cdec68e05f8555034292db7712c2189c98bd96a1e`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573942fa9e85b5ae2a2dd8eebbfe68a15cbc4562d77ed7b34b827ddf38d67873`  
		Last Modified: Wed, 13 May 2026 00:30:40 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6577aceea038d31c6741058ac70f3042052944add747d78e1e98f4768056ad9`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f767fdb48bc45cf9dfc7586e7f3bb6923b4260220f4751867e56819d9198c6f7`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805ccff5e068c1b1ef4ee49960a7779be478d8aac505863b20d6779b21c86cbc`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a088d5cf08a67d2b16495569498bf84dc519c98894eef90450facae9b2b1fd0`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a013ec9aa226e3c490885f2df243f133e073c70c9f7fe42acf1c7c6d646c4`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c59e03f4cda98b2b89df28ea3599e7ce642f3438c9607747e027edae7d633`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df98da5df2a594f3eaf8a18d588dd2dd717a8b9d65120307073b5097a7461ab1`  
		Last Modified: Wed, 13 May 2026 00:30:38 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738c190dc62e002473b0f2e0a6b4d56acd58d4befffd3a5254489344e3f514ad`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 110.6 KB (110619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d153bfc2eaf47e5d03b6d7723d1c90e94fbc34f9bd5394c155057ec6cb0fc42e`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:f2b8fdc30136d5694f4d937911af2a98122816cd9382f30f5e188034eb925ee8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145172029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a188f7374e0862b018d9c6a58ee464b17ed26b607a136f3c2f81f6ba750a8d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:33:03 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:33:04 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:33:08 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:33:11 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:33:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:33:21 GMT
RUN caddy version
# Wed, 13 May 2026 00:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471afcd67b75eae029a73dd0dd5c78c7a867343259b55e8a2ce811a682e0cecc`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 75.7 KB (75727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82a36e1bbf75e8321fe17d1997dc9a3fb4d0322fec9092d1c1da3f90b2872be`  
		Last Modified: Wed, 13 May 2026 00:33:34 GMT  
		Size: 17.5 MB (17549625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1c8055df56386428b23be9cc63963727ee8c65d8ccffd1cccb3768eb2e2233`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 271.9 KB (271937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802218197b7b44f15d0c35e1f92bcebeab5b5348fef8370532d04f6e9eae967`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 109.6 KB (109634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1878ea730f12e1f174b5f94eae4c28852ba7d131ff79831bb232b1d3bd2a9195`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5dcf5eafb5625f15b6c8221a6e8033e90b2e194cf46387f7384e9b4a9fbd3c`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4835c93d3898ae70cc7ac56c9260fd82bf21232d466b88b0c18317f927fad95`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e837a3b4c7f62a51617a0817e87c40d393639d84181cce582cdecd0ed04f6b49`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4bdc974f597917738eb16a57d09d2eb7d4932fb411b582d7397d1e49d850ee`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa60544a60e2a9391135d903f2cf2e1104b968bf0cb17d7fdc7896f5e8a41d7`  
		Last Modified: Wed, 13 May 2026 00:33:29 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f676e12689f61e65afafa2dbabe0f87066ea23a433b6bab30a252984ea3bfcce`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c8bcb78837d9611d2e6d737f1983724070a8b8dc651967aa131aaf3b53db2`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fd9964db11cc46a832c192535f0da8d40411e0e4b90d4735a417e2b21e546`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b24ac8b6e8779c0ea8641c14aa97c30b88dfb2dccfef053e31a383bf8772a0`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14623bf8cac2234d2402f1b77f9f8b9ad17f42b63c25eac6a03a874f2b96603`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf92d85a26150eb8504b9bffa3855decbd94a1cc1614f643dccb2a544ed2818`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6be3b806219581d0384bebe4e25fde1cc050ad9ea5def7c549bbfc37fdec69`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183f69d2299c1c4178f5941ded18872ae1a092d5822f9b2470a9bff9febadfc3`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4db159e8ff27f5e761dfc5a73a64fc1bdeeec4bb736d0de7ccdb6479e4d49d`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 110.4 KB (110391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec19313137639151ccfb4e3125b9f946f903e0153e167a6df587f323d036934e`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:5d09312d850c343bf10c4b5d1f831d63fd9e62aaba2eb17ab04136849c9b7731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:2-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:f2b8fdc30136d5694f4d937911af2a98122816cd9382f30f5e188034eb925ee8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145172029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a188f7374e0862b018d9c6a58ee464b17ed26b607a136f3c2f81f6ba750a8d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:33:03 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:33:04 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:33:08 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:33:11 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:33:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:33:21 GMT
RUN caddy version
# Wed, 13 May 2026 00:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471afcd67b75eae029a73dd0dd5c78c7a867343259b55e8a2ce811a682e0cecc`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 75.7 KB (75727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82a36e1bbf75e8321fe17d1997dc9a3fb4d0322fec9092d1c1da3f90b2872be`  
		Last Modified: Wed, 13 May 2026 00:33:34 GMT  
		Size: 17.5 MB (17549625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1c8055df56386428b23be9cc63963727ee8c65d8ccffd1cccb3768eb2e2233`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 271.9 KB (271937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802218197b7b44f15d0c35e1f92bcebeab5b5348fef8370532d04f6e9eae967`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 109.6 KB (109634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1878ea730f12e1f174b5f94eae4c28852ba7d131ff79831bb232b1d3bd2a9195`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5dcf5eafb5625f15b6c8221a6e8033e90b2e194cf46387f7384e9b4a9fbd3c`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4835c93d3898ae70cc7ac56c9260fd82bf21232d466b88b0c18317f927fad95`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e837a3b4c7f62a51617a0817e87c40d393639d84181cce582cdecd0ed04f6b49`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4bdc974f597917738eb16a57d09d2eb7d4932fb411b582d7397d1e49d850ee`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa60544a60e2a9391135d903f2cf2e1104b968bf0cb17d7fdc7896f5e8a41d7`  
		Last Modified: Wed, 13 May 2026 00:33:29 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f676e12689f61e65afafa2dbabe0f87066ea23a433b6bab30a252984ea3bfcce`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c8bcb78837d9611d2e6d737f1983724070a8b8dc651967aa131aaf3b53db2`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fd9964db11cc46a832c192535f0da8d40411e0e4b90d4735a417e2b21e546`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b24ac8b6e8779c0ea8641c14aa97c30b88dfb2dccfef053e31a383bf8772a0`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14623bf8cac2234d2402f1b77f9f8b9ad17f42b63c25eac6a03a874f2b96603`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf92d85a26150eb8504b9bffa3855decbd94a1cc1614f643dccb2a544ed2818`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6be3b806219581d0384bebe4e25fde1cc050ad9ea5def7c549bbfc37fdec69`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183f69d2299c1c4178f5941ded18872ae1a092d5822f9b2470a9bff9febadfc3`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4db159e8ff27f5e761dfc5a73a64fc1bdeeec4bb736d0de7ccdb6479e4d49d`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 110.4 KB (110391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec19313137639151ccfb4e3125b9f946f903e0153e167a6df587f323d036934e`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:0cd979a2fb38e0ef8a3f7e405a19569c9930e820125c1d08720b752d6ba78e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:2-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:3e5afaeda3465c585afea0828ec650f60e760f92ab1096cbdd12bbb7044f93f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217870731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4c6463b2201d0e16cdf07c19f7038d51083193293932e21b857521bf02bab9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:30:16 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:30:18 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:30:22 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:30:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:30:33 GMT
RUN caddy version
# Wed, 13 May 2026 00:30:33 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1fedb6255043325f0c6a8118656684fcc0c1eb9b84857ff574105bdd45da85`  
		Last Modified: Wed, 13 May 2026 00:30:44 GMT  
		Size: 71.9 KB (71893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde99a62b5456da395a4f921712e08ec242d9c53791f22763e904483b90bb0ff`  
		Last Modified: Wed, 13 May 2026 00:30:46 GMT  
		Size: 17.5 MB (17549616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfaf73426fda2a4ab3e9ef51a62f30bf03cd7bb09987eaed20cca2f4baf6c72`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 271.7 KB (271708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee506f35cf26ab6a4307a617c899a31108d35a38976dcbace37f776be3fa88b9`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 111.9 KB (111876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae64a8691f6412e9e7b124cb1506d63cbc0888dfda70af2a058cd92483d1bf3`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e08e3975dc80abab1d7078a935b8310dfd0436900117ac019cf7e74e96327`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa53d7a29128e22ba5071bc2c061d21df2672618f2d335495eee03b57b30eec9`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9aa3dda4800660b0c498edee92d63a95f3487dea910ee7b1e32237e7d8c01`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602df0b26626bd70f3e3b7e338c29f3774aadcb1993b32e11424961d5818b71`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c12f0b0a957349df9e5cdec68e05f8555034292db7712c2189c98bd96a1e`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573942fa9e85b5ae2a2dd8eebbfe68a15cbc4562d77ed7b34b827ddf38d67873`  
		Last Modified: Wed, 13 May 2026 00:30:40 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6577aceea038d31c6741058ac70f3042052944add747d78e1e98f4768056ad9`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f767fdb48bc45cf9dfc7586e7f3bb6923b4260220f4751867e56819d9198c6f7`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805ccff5e068c1b1ef4ee49960a7779be478d8aac505863b20d6779b21c86cbc`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a088d5cf08a67d2b16495569498bf84dc519c98894eef90450facae9b2b1fd0`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a013ec9aa226e3c490885f2df243f133e073c70c9f7fe42acf1c7c6d646c4`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c59e03f4cda98b2b89df28ea3599e7ce642f3438c9607747e027edae7d633`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df98da5df2a594f3eaf8a18d588dd2dd717a8b9d65120307073b5097a7461ab1`  
		Last Modified: Wed, 13 May 2026 00:30:38 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738c190dc62e002473b0f2e0a6b4d56acd58d4befffd3a5254489344e3f514ad`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 110.6 KB (110619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d153bfc2eaf47e5d03b6d7723d1c90e94fbc34f9bd5394c155057ec6cb0fc42e`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:4b2309a8fe290a6271bb2bdd006c30f27a06e0e18787c56c8604b1facf1cc9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:2-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:672b320378b1e89dde74d15a8a123068d26dafce6901597f4f8a837c5c38e7b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141244276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a5337ff6c38ebefe95a0943a39f42bab87a62f05d840422d53a0be69b65f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:59:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:59:25 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:59:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:59:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:59:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:59:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:59:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 80
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 443
# Tue, 12 May 2026 23:59:42 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:59:43 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:59:48 GMT
RUN caddy version
# Tue, 12 May 2026 23:59:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be1f105178ea258d105ecbaf5ec1f6000c5b289826e3b432c22080c650f719`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 524.5 KB (524474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7902ee53436295b9cb02bfa64ac6aa3b314c1e926ec77f7bb59eea811e28a846`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170554e1bf42badb647bc34b5718a5915fede948183bf5dc3d0d21e5540a0b67`  
		Last Modified: Wed, 13 May 2026 00:00:00 GMT  
		Size: 17.9 MB (17925247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a6d017c1aab65f96bd924d664427c093dba8210995905eaf00df2fbd142cb`  
		Last Modified: Tue, 12 May 2026 23:59:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04fc399abb90e3e2df99498e2eb88e7afd2a3f97e84400a40b7439ea46f1fa5`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d26c10fbf4dafe70c44037417bb3457e50a549f998a6f8b4799cf456c446e2`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295c37ba01761384092ce6a3f611a8792a57e0f772e6d8e3bfb099f51932a73`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb5b45ec93d301f781dc64b899fdfaa452f3d35dbbe0ba52fc5c87b02593d0`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0f84b59aead90c71aa95cd5340904935ff3da90339fa6ff21049d0f56f9ec`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1aeb5b58eaf433feb7668159802420e22345953cd345a111f5ff264e659bdf`  
		Last Modified: Tue, 12 May 2026 23:59:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03412a72c6ae737ad61b888338ad28fdc2b3477281195707e27619683236208`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a705083dc71361abc6a1e82aa158830dc6f3dd6e486a403f011f357eae4d884`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5637de44873a5862f646124e27d0fe311506c6fa1eec39c15df5312e1d41881`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4356db0d34adcecf1c9218951422411d7f942cb4d50621800af19388fdcc0`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a670d1e50cdca965f8cebdbf95f43d51e7fe8d7daf65312384a5731f3f743e`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc67002143e99034340b46a68c760d90626fe51d4e087bca7be0aa904ec8b45`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c8eddb6ea788613d96893c8e7c570d4a29a2b07f6d1ce823bf72faa05cf7b`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c21c96cd26011f147afe2c8c693897e2a126fbba132af7fc830d2d7559f19`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 351.6 KB (351565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c0ee074e227c1b13e1438189cfa031217727fc8085182b53234397774d341`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:13a01e024e1f987d2133e73315fea5688b3dde0f70bced70f1caad7c2b53e092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:672b320378b1e89dde74d15a8a123068d26dafce6901597f4f8a837c5c38e7b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141244276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a5337ff6c38ebefe95a0943a39f42bab87a62f05d840422d53a0be69b65f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:59:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:59:25 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:59:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:59:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:59:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:59:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:59:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 80
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 443
# Tue, 12 May 2026 23:59:42 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:59:43 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:59:48 GMT
RUN caddy version
# Tue, 12 May 2026 23:59:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be1f105178ea258d105ecbaf5ec1f6000c5b289826e3b432c22080c650f719`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 524.5 KB (524474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7902ee53436295b9cb02bfa64ac6aa3b314c1e926ec77f7bb59eea811e28a846`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170554e1bf42badb647bc34b5718a5915fede948183bf5dc3d0d21e5540a0b67`  
		Last Modified: Wed, 13 May 2026 00:00:00 GMT  
		Size: 17.9 MB (17925247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a6d017c1aab65f96bd924d664427c093dba8210995905eaf00df2fbd142cb`  
		Last Modified: Tue, 12 May 2026 23:59:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04fc399abb90e3e2df99498e2eb88e7afd2a3f97e84400a40b7439ea46f1fa5`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d26c10fbf4dafe70c44037417bb3457e50a549f998a6f8b4799cf456c446e2`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295c37ba01761384092ce6a3f611a8792a57e0f772e6d8e3bfb099f51932a73`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb5b45ec93d301f781dc64b899fdfaa452f3d35dbbe0ba52fc5c87b02593d0`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0f84b59aead90c71aa95cd5340904935ff3da90339fa6ff21049d0f56f9ec`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1aeb5b58eaf433feb7668159802420e22345953cd345a111f5ff264e659bdf`  
		Last Modified: Tue, 12 May 2026 23:59:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03412a72c6ae737ad61b888338ad28fdc2b3477281195707e27619683236208`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a705083dc71361abc6a1e82aa158830dc6f3dd6e486a403f011f357eae4d884`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5637de44873a5862f646124e27d0fe311506c6fa1eec39c15df5312e1d41881`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4356db0d34adcecf1c9218951422411d7f942cb4d50621800af19388fdcc0`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a670d1e50cdca965f8cebdbf95f43d51e7fe8d7daf65312384a5731f3f743e`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc67002143e99034340b46a68c760d90626fe51d4e087bca7be0aa904ec8b45`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c8eddb6ea788613d96893c8e7c570d4a29a2b07f6d1ce823bf72faa05cf7b`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c21c96cd26011f147afe2c8c693897e2a126fbba132af7fc830d2d7559f19`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 351.6 KB (351565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c0ee074e227c1b13e1438189cfa031217727fc8085182b53234397774d341`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:206dde5cb85762b952e1ced7003d7630ae6e1f8f347ae67b56c84026948e8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:2-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11`

```console
$ docker pull caddy@sha256:ec18ee54aab3315c22e25f3b2babda73ff8007d39b13b3bd1bfffa2f0444c7d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:2.11` - linux; amd64

```console
$ docker pull caddy@sha256:3739ea4f0c877259a693d932693cf8f3408e9a9497c004f031b0e830e93e1546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23985030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5190456911cee510988a5fb9996188ef866fbcca3235cad19bf05f5f8f33386f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:12 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920de1d55d9880b00fbeaf8fa3757e89f7ea6170ff12633cbe766c2152a858d`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 2.9 MB (2886638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057c497bda068e80884e6836fbf8971a954593242af7694d080e6b81758b67f4`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b55c68e4a0feeeaec6f86ced6bd8790e19ed68399cff61bab00adc15895ec13`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 17.2 MB (17226669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11` - unknown; unknown

```console
$ docker pull caddy@sha256:e08c659e9fe301aa2814b2cafc4a5211423fcaa307a515772efeb816684ceb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cd52ea603ed29abf30a13e9ab37f92acffb93b53042a6bfaf1d22d9bdb8be`

```dockerfile
```

-	Layers:
	-	`sha256:4c4f094b32e82a0c66e0e5c00015a86d670049e4e9a336febc6c2a2fd626b19b`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 332.9 KB (332947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16285c7326d137b74e90d1f477040eb15643c312e7a46770316c0c258033326a`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11` - linux; arm variant v6

```console
$ docker pull caddy@sha256:018595a3226de0d5c9055279af90983e9e91ca5f12dde17e93925455d19bc0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ce61ba53a04521d0e684e8048cde82ebd35cd3d72a9d1f7616056976e75253`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:40:51 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:40:52 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:40:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b1247b4f1cad33af22f46d45d07b1ee65401981dccc3fa920dafbde1fb072`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 2.8 MB (2819583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d84aa44715b44ce12b2cc9b98a20167ca060c5869ab67124210f554413d56ee`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93038fb49fb9d7664bc1a8209857cde656b4e5ff6ab5a7bf4b270d942f499d0`  
		Last Modified: Tue, 12 May 2026 21:41:00 GMT  
		Size: 16.3 MB (16311628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11` - unknown; unknown

```console
$ docker pull caddy@sha256:de7fac8a337ded6fa61288d6dcc5837d472ed26f9d6b7230f0c8487fb9db984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feea7dba17177c5d72e8d8b883cd3bcdcda396dcc918c1e1e6d3868632932251`

```dockerfile
```

-	Layers:
	-	`sha256:2bd47793d94047373cab54d4b18f46ce16d19438827a8a41e3c5960cd1da48ca`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 18.4 KB (18353 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11` - linux; arm variant v7

```console
$ docker pull caddy@sha256:2c3d3047a1705945ca9376ef8d3e9eb431f0f07f16e6ae2511326d7f0b664ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22262035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a70cfe7deb0544e9098ef10e20ebbc18e346bb3b8df5b140b9f184e71b4a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:42:08 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:42:09 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:42:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce55fb7d543ef0a1f852326909b7cdb22fb514199bd31b9543d92f04e878f4`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 2.7 MB (2681516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49caf58b5069e136a5fcd2fbaa18da4c786566963ba48bcedc27100b8a43365b`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ba28a73ebab4ca57472bca296d741e3d9b1cb27478c6adde87b7c314ba7810`  
		Last Modified: Tue, 12 May 2026 21:42:18 GMT  
		Size: 16.3 MB (16289861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11` - unknown; unknown

```console
$ docker pull caddy@sha256:08ab34ff2df00fe711e074db26cf28e9b5ff1dbfe8355e0f414ed9a7c465cfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb11059736745812fc6bfa910b2d1cce68b03317d8452425d1f7954f2023f495`

```dockerfile
```

-	Layers:
	-	`sha256:95b578e25712b12ba424efc0abb0e6a4daa0cb6d145f200869796d863a0535dd`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 332.4 KB (332365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876e5685474ad9dfce16688d11127988be62753bb83e66c138c382a181530636`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 18.6 KB (18568 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ae38d5cc9674696bfec2dd7a20ea5495a2653d788ee39bff6aaf1007f8dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22800642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64000d357283f8b74cfc9cabce60768a6957447b74a7eb73c573c5d344a398`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:44:57 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:44:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:00 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6cabef06141e7f3aba6fa7d3898c4282f7316acb2ad612b8ea82ac9172cd99`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 2.9 MB (2900862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69f6bd08e27b5a1e9b73c99efae612626fabe895c78a156e402e5938112fff9`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 7.5 KB (7500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4e100b255f5c935bb23c7e5f2a23ee2b5b683a152149ad5db9b32d8455edf`  
		Last Modified: Tue, 12 May 2026 21:45:07 GMT  
		Size: 15.7 MB (15692378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11` - unknown; unknown

```console
$ docker pull caddy@sha256:99d5c41f924f43a16554137091afc6dc8c34e2976b4011ea8793c6211676f8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 KB (351013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f8ace5e5ed9603a8a26766f5df8fd3efe32a76bb3d66c4017bf8bb842691c`

```dockerfile
```

-	Layers:
	-	`sha256:43c50900a0619c09f3987cc62bbfffd4d10da1b9d81fd21f3605e47dbb741967`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 332.4 KB (332401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e57f91d95d6c31886fc5dc74e74b86782c292b27bf964bb5023e301c36f8270`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11` - linux; ppc64le

```console
$ docker pull caddy@sha256:d6f3adf638edd88132caec6005766ec86f31796069549755af52d172a03ebd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22551245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d82ac569eea06185f6688d103c7d7e2ef313dce067d6f1aca3b7255025aa450`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:46 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:52 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aba3acae7a944d3cb59ff0085839ecf6bc67e67a1ff5c9d62453ec36405516d`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 3.0 MB (3024677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef81e00b6b88436c8856bd7f6a2a40abea36897a22c7707cdf06722a09f8b819`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1e87608e2891184dfb2f547b0a2062b1bba1b787d3cd95ff36446affe940e`  
		Last Modified: Tue, 12 May 2026 21:46:12 GMT  
		Size: 15.7 MB (15688108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11` - unknown; unknown

```console
$ docker pull caddy@sha256:863e023f3571814b385c37ac309e71a9a712f4aea420d2cea5032e2a362bf7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef881e7b8f82faab6a4473932499599574eb0bc9d0264c779647d0b099584f`

```dockerfile
```

-	Layers:
	-	`sha256:aa780bcad124738bdb6864e89c3299ebdcee766cde92da7db3f2ca1d99c22f23`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 332.4 KB (332354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cabca92420dc637383da8dc8f0d0276fcf258532404ff1d3fb1e80473359b1`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11` - linux; riscv64

```console
$ docker pull caddy@sha256:69328a1677b50e71a30c554ca8dddf7f1ad2474084385dabd7a0d6fedc9a4118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22851653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086f5adaba5ab0d6ae67e9e685607028248302272c9befb82e9fba4246d6537e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 02:12:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Thu, 14 May 2026 02:12:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV CADDY_VERSION=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_DATA_HOME=/data
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/udp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
WORKDIR /srv
# Thu, 14 May 2026 02:12:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a638da60daf650b51909ed97e65ca82d6b4c622d9aad9e05a1fe86e41b1b8`  
		Last Modified: Thu, 14 May 2026 02:13:15 GMT  
		Size: 3.0 MB (3024903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e9ab663ff84756b43ea4456b9675a7bb4e9a21db93cfb2860477f1acc49fa3`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 7.5 KB (7506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207dafa63c1803835db9d283a462accf88a7d65b6c6a62ef6d00c05e7e2d4d85`  
		Last Modified: Thu, 14 May 2026 02:13:17 GMT  
		Size: 16.2 MB (16231550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11` - unknown; unknown

```console
$ docker pull caddy@sha256:2a37fc42537c780173072b08a797af48db02d1ca4bb14afe8301f380deb5f108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1087260f2ba70b75cfc134c58bb57369b570c4c836ad26b8a6774cfb2c421a26`

```dockerfile
```

-	Layers:
	-	`sha256:50741c878fc4519cf8be95491297cbbf12889e7fe8fe4cb6f0cb7a32aacd5a4d`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 332.4 KB (332350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074f80835103901f06cabe60ac917a34ae1a55cf6637768028867d83f6f31640`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11` - linux; s390x

```console
$ docker pull caddy@sha256:2be760d0b6dcefcee4d8e8de79e4fbc5bff379cc71f6ba4be329b95fee14ed53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23338359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bb7983fab4c669751406633c3cd0bacc33744d3c43dcecd96b365041e7d3b5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:39:41 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:39:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:39:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cb0bfcc1c8a81033ff4911e9096b260f4711f66484b04586fd6fa5ca95e44f`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 3.0 MB (3010703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bd7ba8a52c9fc9419b92337580db55dcd8690a637184fb22bec4871ffb8c0`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798a8d976afd31ca55ef92d83a93374f6c3e7ccd3add31769d768349700d623`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 16.6 MB (16593589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11` - unknown; unknown

```console
$ docker pull caddy@sha256:4a728924f65d2a9612ff66fbadd33d9a2d6e6b198cfc95cd6b23b89948cc2a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43f0c042f1bc3d80c67c0b0ad7df18ed102df0765f312c2619bed3d8392597`

```dockerfile
```

-	Layers:
	-	`sha256:4b3e6e6b8593dd35d4f0b59b89b012680c12c5498a7b01ae16bcb7ed34ac49a8`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 332.3 KB (332296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3864730b4cf584aa87e923de4848636482e8621df04a87733e10e42cc44e9b3`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.11` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:672b320378b1e89dde74d15a8a123068d26dafce6901597f4f8a837c5c38e7b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141244276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a5337ff6c38ebefe95a0943a39f42bab87a62f05d840422d53a0be69b65f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:59:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:59:25 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:59:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:59:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:59:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:59:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:59:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 80
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 443
# Tue, 12 May 2026 23:59:42 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:59:43 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:59:48 GMT
RUN caddy version
# Tue, 12 May 2026 23:59:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be1f105178ea258d105ecbaf5ec1f6000c5b289826e3b432c22080c650f719`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 524.5 KB (524474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7902ee53436295b9cb02bfa64ac6aa3b314c1e926ec77f7bb59eea811e28a846`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170554e1bf42badb647bc34b5718a5915fede948183bf5dc3d0d21e5540a0b67`  
		Last Modified: Wed, 13 May 2026 00:00:00 GMT  
		Size: 17.9 MB (17925247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a6d017c1aab65f96bd924d664427c093dba8210995905eaf00df2fbd142cb`  
		Last Modified: Tue, 12 May 2026 23:59:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04fc399abb90e3e2df99498e2eb88e7afd2a3f97e84400a40b7439ea46f1fa5`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d26c10fbf4dafe70c44037417bb3457e50a549f998a6f8b4799cf456c446e2`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295c37ba01761384092ce6a3f611a8792a57e0f772e6d8e3bfb099f51932a73`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb5b45ec93d301f781dc64b899fdfaa452f3d35dbbe0ba52fc5c87b02593d0`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0f84b59aead90c71aa95cd5340904935ff3da90339fa6ff21049d0f56f9ec`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1aeb5b58eaf433feb7668159802420e22345953cd345a111f5ff264e659bdf`  
		Last Modified: Tue, 12 May 2026 23:59:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03412a72c6ae737ad61b888338ad28fdc2b3477281195707e27619683236208`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a705083dc71361abc6a1e82aa158830dc6f3dd6e486a403f011f357eae4d884`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5637de44873a5862f646124e27d0fe311506c6fa1eec39c15df5312e1d41881`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4356db0d34adcecf1c9218951422411d7f942cb4d50621800af19388fdcc0`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a670d1e50cdca965f8cebdbf95f43d51e7fe8d7daf65312384a5731f3f743e`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc67002143e99034340b46a68c760d90626fe51d4e087bca7be0aa904ec8b45`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c8eddb6ea788613d96893c8e7c570d4a29a2b07f6d1ce823bf72faa05cf7b`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c21c96cd26011f147afe2c8c693897e2a126fbba132af7fc830d2d7559f19`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 351.6 KB (351565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c0ee074e227c1b13e1438189cfa031217727fc8085182b53234397774d341`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11-alpine`

```console
$ docker pull caddy@sha256:86deaf5e3d3408a6ccec08fbb79989783dd26e206ae10bcf78a801dc8c9ab794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2.11-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:3739ea4f0c877259a693d932693cf8f3408e9a9497c004f031b0e830e93e1546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23985030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5190456911cee510988a5fb9996188ef866fbcca3235cad19bf05f5f8f33386f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:12 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920de1d55d9880b00fbeaf8fa3757e89f7ea6170ff12633cbe766c2152a858d`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 2.9 MB (2886638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057c497bda068e80884e6836fbf8971a954593242af7694d080e6b81758b67f4`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b55c68e4a0feeeaec6f86ced6bd8790e19ed68399cff61bab00adc15895ec13`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 17.2 MB (17226669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e08c659e9fe301aa2814b2cafc4a5211423fcaa307a515772efeb816684ceb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cd52ea603ed29abf30a13e9ab37f92acffb93b53042a6bfaf1d22d9bdb8be`

```dockerfile
```

-	Layers:
	-	`sha256:4c4f094b32e82a0c66e0e5c00015a86d670049e4e9a336febc6c2a2fd626b19b`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 332.9 KB (332947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16285c7326d137b74e90d1f477040eb15643c312e7a46770316c0c258033326a`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:018595a3226de0d5c9055279af90983e9e91ca5f12dde17e93925455d19bc0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ce61ba53a04521d0e684e8048cde82ebd35cd3d72a9d1f7616056976e75253`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:40:51 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:40:52 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:40:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b1247b4f1cad33af22f46d45d07b1ee65401981dccc3fa920dafbde1fb072`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 2.8 MB (2819583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d84aa44715b44ce12b2cc9b98a20167ca060c5869ab67124210f554413d56ee`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93038fb49fb9d7664bc1a8209857cde656b4e5ff6ab5a7bf4b270d942f499d0`  
		Last Modified: Tue, 12 May 2026 21:41:00 GMT  
		Size: 16.3 MB (16311628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:de7fac8a337ded6fa61288d6dcc5837d472ed26f9d6b7230f0c8487fb9db984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feea7dba17177c5d72e8d8b883cd3bcdcda396dcc918c1e1e6d3868632932251`

```dockerfile
```

-	Layers:
	-	`sha256:2bd47793d94047373cab54d4b18f46ce16d19438827a8a41e3c5960cd1da48ca`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 18.4 KB (18353 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:2c3d3047a1705945ca9376ef8d3e9eb431f0f07f16e6ae2511326d7f0b664ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22262035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a70cfe7deb0544e9098ef10e20ebbc18e346bb3b8df5b140b9f184e71b4a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:42:08 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:42:09 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:42:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce55fb7d543ef0a1f852326909b7cdb22fb514199bd31b9543d92f04e878f4`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 2.7 MB (2681516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49caf58b5069e136a5fcd2fbaa18da4c786566963ba48bcedc27100b8a43365b`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ba28a73ebab4ca57472bca296d741e3d9b1cb27478c6adde87b7c314ba7810`  
		Last Modified: Tue, 12 May 2026 21:42:18 GMT  
		Size: 16.3 MB (16289861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:08ab34ff2df00fe711e074db26cf28e9b5ff1dbfe8355e0f414ed9a7c465cfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb11059736745812fc6bfa910b2d1cce68b03317d8452425d1f7954f2023f495`

```dockerfile
```

-	Layers:
	-	`sha256:95b578e25712b12ba424efc0abb0e6a4daa0cb6d145f200869796d863a0535dd`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 332.4 KB (332365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876e5685474ad9dfce16688d11127988be62753bb83e66c138c382a181530636`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 18.6 KB (18568 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ae38d5cc9674696bfec2dd7a20ea5495a2653d788ee39bff6aaf1007f8dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22800642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64000d357283f8b74cfc9cabce60768a6957447b74a7eb73c573c5d344a398`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:44:57 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:44:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:00 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6cabef06141e7f3aba6fa7d3898c4282f7316acb2ad612b8ea82ac9172cd99`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 2.9 MB (2900862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69f6bd08e27b5a1e9b73c99efae612626fabe895c78a156e402e5938112fff9`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 7.5 KB (7500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4e100b255f5c935bb23c7e5f2a23ee2b5b683a152149ad5db9b32d8455edf`  
		Last Modified: Tue, 12 May 2026 21:45:07 GMT  
		Size: 15.7 MB (15692378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:99d5c41f924f43a16554137091afc6dc8c34e2976b4011ea8793c6211676f8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 KB (351013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f8ace5e5ed9603a8a26766f5df8fd3efe32a76bb3d66c4017bf8bb842691c`

```dockerfile
```

-	Layers:
	-	`sha256:43c50900a0619c09f3987cc62bbfffd4d10da1b9d81fd21f3605e47dbb741967`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 332.4 KB (332401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e57f91d95d6c31886fc5dc74e74b86782c292b27bf964bb5023e301c36f8270`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d6f3adf638edd88132caec6005766ec86f31796069549755af52d172a03ebd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22551245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d82ac569eea06185f6688d103c7d7e2ef313dce067d6f1aca3b7255025aa450`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:46 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:52 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aba3acae7a944d3cb59ff0085839ecf6bc67e67a1ff5c9d62453ec36405516d`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 3.0 MB (3024677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef81e00b6b88436c8856bd7f6a2a40abea36897a22c7707cdf06722a09f8b819`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1e87608e2891184dfb2f547b0a2062b1bba1b787d3cd95ff36446affe940e`  
		Last Modified: Tue, 12 May 2026 21:46:12 GMT  
		Size: 15.7 MB (15688108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:863e023f3571814b385c37ac309e71a9a712f4aea420d2cea5032e2a362bf7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef881e7b8f82faab6a4473932499599574eb0bc9d0264c779647d0b099584f`

```dockerfile
```

-	Layers:
	-	`sha256:aa780bcad124738bdb6864e89c3299ebdcee766cde92da7db3f2ca1d99c22f23`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 332.4 KB (332354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cabca92420dc637383da8dc8f0d0276fcf258532404ff1d3fb1e80473359b1`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:69328a1677b50e71a30c554ca8dddf7f1ad2474084385dabd7a0d6fedc9a4118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22851653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086f5adaba5ab0d6ae67e9e685607028248302272c9befb82e9fba4246d6537e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 02:12:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Thu, 14 May 2026 02:12:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV CADDY_VERSION=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_DATA_HOME=/data
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/udp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
WORKDIR /srv
# Thu, 14 May 2026 02:12:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a638da60daf650b51909ed97e65ca82d6b4c622d9aad9e05a1fe86e41b1b8`  
		Last Modified: Thu, 14 May 2026 02:13:15 GMT  
		Size: 3.0 MB (3024903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e9ab663ff84756b43ea4456b9675a7bb4e9a21db93cfb2860477f1acc49fa3`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 7.5 KB (7506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207dafa63c1803835db9d283a462accf88a7d65b6c6a62ef6d00c05e7e2d4d85`  
		Last Modified: Thu, 14 May 2026 02:13:17 GMT  
		Size: 16.2 MB (16231550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2a37fc42537c780173072b08a797af48db02d1ca4bb14afe8301f380deb5f108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1087260f2ba70b75cfc134c58bb57369b570c4c836ad26b8a6774cfb2c421a26`

```dockerfile
```

-	Layers:
	-	`sha256:50741c878fc4519cf8be95491297cbbf12889e7fe8fe4cb6f0cb7a32aacd5a4d`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 332.4 KB (332350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074f80835103901f06cabe60ac917a34ae1a55cf6637768028867d83f6f31640`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:2be760d0b6dcefcee4d8e8de79e4fbc5bff379cc71f6ba4be329b95fee14ed53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23338359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bb7983fab4c669751406633c3cd0bacc33744d3c43dcecd96b365041e7d3b5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:39:41 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:39:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:39:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cb0bfcc1c8a81033ff4911e9096b260f4711f66484b04586fd6fa5ca95e44f`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 3.0 MB (3010703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bd7ba8a52c9fc9419b92337580db55dcd8690a637184fb22bec4871ffb8c0`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798a8d976afd31ca55ef92d83a93374f6c3e7ccd3add31769d768349700d623`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 16.6 MB (16593589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4a728924f65d2a9612ff66fbadd33d9a2d6e6b198cfc95cd6b23b89948cc2a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43f0c042f1bc3d80c67c0b0ad7df18ed102df0765f312c2619bed3d8392597`

```dockerfile
```

-	Layers:
	-	`sha256:4b3e6e6b8593dd35d4f0b59b89b012680c12c5498a7b01ae16bcb7ed34ac49a8`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 332.3 KB (332296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3864730b4cf584aa87e923de4848636482e8621df04a87733e10e42cc44e9b3`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.11-builder`

```console
$ docker pull caddy@sha256:d57008618f743e6308058d7bd990eb3489dfd04e2b82978cca7b953e1b491fc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:2.11-builder` - linux; amd64

```console
$ docker pull caddy@sha256:db3ae9a5913d5b9305c729247b8ee6ca7596823a3a9419eaac330e5f374c3157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79773771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591706032a9a5c14da6e7f446e0083d6747768d50d0bf9da36e55c2421e94a2f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:53 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:11:59 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:00 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30edd47abbca5172a1775d1ba8a17aef65500a7a1ecc50af582706ad0c19ab`  
		Last Modified: Tue, 02 Jun 2026 21:45:09 GMT  
		Size: 290.2 KB (290247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaa626ba3010d60ab55d9cdc69c0b12ebff5d1b5ece83ff220fb46a7709b3b`  
		Last Modified: Tue, 02 Jun 2026 21:44:37 GMT  
		Size: 67.3 MB (67283031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abecc8ee46932a01c961a896c3c87dd0efe1301916e124bdac46f96ae6e9dee`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca4922139842e28e1d61aaac141bc8576337fa9b8d64d1d9f723d161fb30612`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 6.5 MB (6489213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fa1420c37ef3c625b9f14ee901574c588fc49b3eb5a8fca1a8a732fd47620b`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 1.8 MB (1846501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e306254cc3a4dab0c2ccd0f548ad566fa5aa81a412b9b432d81889526a2bbf2`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ddd773e864a4f4e091e1f4bfdbd60371b4c51910be5ccb610589b8a6883de8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4dc9d9bcee8d699bb42f311997ea36c642596e4004aa8859d0781b30ac2c9d`

```dockerfile
```

-	Layers:
	-	`sha256:d055d9682529a9387da6c4adbc8bdc265d0466484002fca96e29c90f179091be`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 280.8 KB (280776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490b4b762d29e23f9c30e7d63d2f4fde87253b5f126903cfd336647e4cf6c3af`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67c97e86bbcf6c6d84c8a191e6f9c07550c3ff25bfef23d3e8ee6a6407d6d801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77801132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8375fe7e15b17bead87deaac11514fa70da1cd8427509b1c228967a15f141eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:01 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:15:26 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:15:27 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:15:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dc79104d8e3b9e93b7ff3163839b44dd0979c52b2f81f68e01be8f60d9d090`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 291.0 KB (291036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb989b4b1329f80799d899b8d7259a6658047b39b2b670ed0cc8620dd1d357c`  
		Last Modified: Tue, 02 Jun 2026 21:44:18 GMT  
		Size: 65.8 MB (65785954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e947158a0266891a134507f0a6253aec12f2c7656af2daefbed99f399148f5`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620327b269f4fa8f6e186115a4ab2a342dedb497a9044abd4a5b3246f11d3ac3`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 6.4 MB (6406685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a7c7f37dd2ddabcd39c4ec78c16b8efaf799e1db677a0a88c55ba2bd16132e`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037287d5c994a910febeca5542dc101d590c0256e293e25e7ddb97f4b25eba7b`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ee8a613597922f4a0c6ad805948acd213e018eb8e3548ca5b98e7cb6c0410659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a997af74d3004a92cc163aa5d9f843ecd7552d9fad60e39cc23d5f4340ebdbd1`

```dockerfile
```

-	Layers:
	-	`sha256:b77f8ee7de0cc1af47105376a1a978c3bd700001392879cba9b348c38f53c909`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:081203e78dbbdf584d644a704dbce3dd01e8d923760b1e4160a615e9c0282f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cece6d48bcb1d2e37ff13a3299d3382dd7c3a18c66cd620c334b6e7e45b85c5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:51 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:54 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:48 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa788fec666273423bc95c719209c3f49b0d2c1c28fdaf669e4ebcab932954`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 290.2 KB (290169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f46eeae83dd5d801ff20835cd1ea98f630698b9c066e10ddf320a1c9d42c07`  
		Last Modified: Tue, 02 Jun 2026 21:45:10 GMT  
		Size: 65.8 MB (65786124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494a0eb08b28e7075149245f5ff666eeadec03e6b1b08870ad1caa24151d00b`  
		Last Modified: Tue, 02 Jun 2026 21:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba6d2d27897ace71b8214e93839ab4dddfb4bf51e5dd9871755073b452fd92`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 5.9 MB (5859405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d200f1ff9040ab5ed074d40e2c5d715e5ca869a8c3c9ca357f24b30cc08f2`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 1.7 MB (1738762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392245d1b10f490bef242becdaf6b658edb173425508af51312e2d0c7703b3c5`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0207715e319528107b0ca90c4b3ae044a8636067b8544656cf7cfa660dbd93d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd6848c1a5afb6c01dd7ed0eea80f86a4053eb96a8d94f50bbb86131989d4a`

```dockerfile
```

-	Layers:
	-	`sha256:dda72704ff023245a1d0202ebcabc8675ff1d722be6ba03fec1b7ce479c3a68c`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 283.2 KB (283168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac1a6806382a02068a2684ad9fc775685c890f3913b65b2de640fe3eca324e6`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:13da9d8308a65d8402c19528f51e19a2535fcd2f28ee893feabfefab09afb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76951883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114e448de61888adef08f63408e9426eb63ce6db5c2c1066219d9ba0222717c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2c0198c180cf41cbfd73e25946fc0ccc373d0fee89deb6e7eeec7b1f8612ee`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 292.9 KB (292861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477eaf154b7c8070862d9db01681f78c8a60ce90e8936310f6a906696df475a`  
		Last Modified: Tue, 02 Jun 2026 21:43:59 GMT  
		Size: 64.2 MB (64166971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb4739b26b76346d1281fb8fac14c5bc8025bfc580405cc95aa21736e41116`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e7c04c5116e56a4edea922d39e62c3fe0cfb06ee580b89926af1db83402ce`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 6.6 MB (6575206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57c7a67944f4fa914947979e30a6c1db54ab3c9b1aac79a9ebd7b36e8e39b0`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 1.7 MB (1716384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ee51343f308260ed7fa9020154c216542e21fd2589bc41d85b57f77166a81`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ce914fd434a8d09e7d2f73c5c9b354b42cf9c31d65fefbe292f23eacb6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 KB (300526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbed50fbf772e7e0ff9b816eb3a8dc3e213df0f8c75ba10dc5924412b0e4d841`

```dockerfile
```

-	Layers:
	-	`sha256:add9c054a1ac3653aed38da164cb08126bb46bb4bc153c6f12848191bed15b4b`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 280.2 KB (280230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838bb928d6772b6ebe8d87d60a85b358fd40eb2166c93cb622cee8a22a537ca3`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:658d12b9b7e489cdf05a0115f8fd9c8e392ee3160ba5b96d5f6b1e3cf0e02802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2568f1df66f499486924dad3ad55e9449d549bbb37426e3354addf15c6c7df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:42:40 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:18 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:19:34 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:19:35 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:19:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94153723d1545849cb54e33c3f8f977f110afcb00da0d5d32236b24537c1a4a3`  
		Last Modified: Tue, 02 Jun 2026 21:43:46 GMT  
		Size: 64.8 MB (64840550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4ff149d61b69213dc146324696a7a3af1a2b46684c6f928dfca1ae8489a0e`  
		Last Modified: Tue, 02 Jun 2026 21:44:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3cb06425959c67588985a91f934858685c3d7e6f0a3094af6c96ef93508d2`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 6.9 MB (6906465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966eded362018ac5d0b34cafa47d109cf32bbdeac194c1582640c28fd31f3cb0`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 1.7 MB (1705993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88bcc980b0c8d2d3de3ae12ec5a268bf23ac450cf0e10b8726131fa5f50dd3a`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:636aaf3183699721a688bf9903f4a642af3556d22fb14b8142bb3d77e9e02f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4888dfc41af739498c0157e20326f403f56cd8400b521203907e2cce1bfb8403`

```dockerfile
```

-	Layers:
	-	`sha256:00729d38b67285f7a79eb306240810accdabec647d996c8e36ab458f490a827c`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 280.2 KB (280199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ec6cfbc1bfecb50f2c2e12352351ad7a86aa62458697127bd6d635c92ce4cb`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:851cb908798b1538ffe3a3053bb98a32903f158a7f1ca9eeafb0fa30f6f34f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77424217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfc4a9d5f64621b356f7b47c6c48337fe32d5912cfc96a0484d5c999eabca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 23:12:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 23:12:42 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
WORKDIR /go
# Wed, 03 Jun 2026 05:24:30 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 05:24:32 GMT
ENV CADDY_VERSION=v2.11.3
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 05:24:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8f135b9aec9b42cabcdbc9e60e1e2b738fe71cb50c44dd091c53fb8edc94a`  
		Last Modified: Tue, 02 Jun 2026 23:19:15 GMT  
		Size: 65.1 MB (65148394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c4848fcf3e91f4413c1666bace4337c4f1c12c50976959bd29ad011c4d936`  
		Last Modified: Tue, 02 Jun 2026 23:22:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc28d768f2c71e4a402e2f4424963bfaa465d9c4a2f36c428bd41b08e3d6d2d`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 6.7 MB (6672809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5d5e4441c4e23a30ad21c2b66c3a336df57c4bfda44ff5113b5b3be8e2ffc`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 1.7 MB (1724208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80fdf8a500696ba07bd03f2a260b2e578f3e7909bec500d7122de9d25041d6`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:dca192295748614e125d445ca613cc0972469b2e1774dca65dd6b47fe9d2682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a911353b6377828995df9827f453d124992e5ff9b7484ef6ebc4da9d7258c820`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc98528c0380ded7049be92a37c9302d44d983dd53bba1648e04dedd55efb4`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 280.2 KB (280195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb92a4e503b3fefa7c0f01279adf8084dd01665b4d68fcef6d623b33d866cb16`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder` - linux; s390x

```console
$ docker pull caddy@sha256:4b90e008693f441e0c5337ba3fedad55597c1c61e2ecf25f2241f3a878b58d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cee611b412138469260e614e91691e6b1868b70e66aabd6488d8013d7cf3ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:02 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:13:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:13:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95f9225fe123215e56024e7fcaa3f2eb9fb3081c2d6160ebae532ca6d5eefd`  
		Last Modified: Tue, 02 Jun 2026 21:43:22 GMT  
		Size: 66.5 MB (66513822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9138885877e3f590d4144dfc2ec737113acde73b99374df82c5be8c2901f3dd`  
		Last Modified: Tue, 02 Jun 2026 21:43:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91584af5ed277f32349e17cda1214326d518b9f94719dc5c4e741329ee86f375`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 6.8 MB (6779991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30090c473a211354bad44ab67b863187e6614231a73dcf0aa22173ee79b1a359`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 1.8 MB (1782842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3da51a38e8b113b744ea5418d02a52a6b6def3db40a219f602fa5e52065bfb`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:578a971dec1e6528eb9512ec7c3c538b18cbeb2a8d6c72b4f420d6992b30009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f17854159ec165c92bf0e0220d91246d07bd68f48b8fa569c16a68552d0058`

```dockerfile
```

-	Layers:
	-	`sha256:4915df098870636a12ece0bc09cc5fc8dee8954c6116a7cfb93bf9f3169bd426`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 280.1 KB (280125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97af12336dd47a218f778a32b9bf8cf6ecc4d8ef33a28f7bb8c621a730e6343b`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:6bac99d1de9debbb801646208c923809fe18cbb945c6d430cc8f1d38c5ba14ff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335210672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45bc764ed6ce43900c66e7269ef9b64bff9f78aca8a5412c2bdddba4456a779`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 21:46:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 21:47:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 21:47:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 21:47:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 21:47:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 21:48:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:48:54 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 21:49:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 21:49:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:50:55 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:50:57 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:33:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:33:57 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:33:58 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:33:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:34:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:34:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03db002b9e59a168b97269178d3cea6be969a491719ca1c8d3f4c33ad9ad07f7`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b9c42b86ca2e7aa4eb41766a6f755119c65c8b2c03b320ba0980b9d2f6547a`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8f4def2bce82d1e544606aaf3e5895ae29437220f1b41211727fbeff83ac8`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16228e0f3edb3815e34fd2d8c6d575e9ed737e1d5cc07909e430d670860bc7cc`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca5f94c0122485a7417a90a87018bf739ef6ef80f60454b5258cefa6a58eed5`  
		Last Modified: Tue, 02 Jun 2026 21:51:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1397a64df19d921e6ad74f8c6ca0ea5b401c7731318c4dd85002c5dbb6df922c`  
		Last Modified: Tue, 02 Jun 2026 21:51:15 GMT  
		Size: 51.3 MB (51286214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871cad50024619c7f067652dc3cc2e678a8c70180235a578d249123c21479637`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007a76e9414e0db486efb9ff5a4409e15cef9f66f3c19a6efc5d554db55f0e4b`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 367.1 KB (367144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fea8e7d4ba560522bf09b19a63fc47cca6a724baa7e90623086a8d46f1d8f2`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44107094e22c635252ccb6df8685c7968f63f084760fcbec0f4cb08857a74`  
		Last Modified: Tue, 02 Jun 2026 21:51:19 GMT  
		Size: 75.3 MB (75252822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35936631b6cd9bd6e5cf14e0cb4f8a287786047d069c23d09ed69d69e5672e`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfefceaacb32ce75c4aaba58b81bced50aae117cc616944d49a92ce10e866b2`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d897cbe5e09e88bd391baaa18698e2d8eb277aa581a683b8025c4f230f1adf7e`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4b32c912e804ac74f332ad5ab2d2b281dc7e6d481f6f80a4f43df475616659`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f053ec3b21275df3413b9168645d21fb9bb677da4c1d6c12e96049e54cabfcd`  
		Last Modified: Tue, 02 Jun 2026 22:34:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b1f65dcb82cba9c705872f745be1ac11720b8c76eebbe4e9942f2f2e810cf7`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 2.3 MB (2345713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcd5aef19be6456c21bb9609b574709a6500a0642321c9435e2421d39818fd`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.11-builder` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:5c6e7364201194ab26b433feaf24cec26dd47fa67d0191fd5aac9a3145f2d75a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2246342426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4817db1df805c59c442b0aae0af3740b59c437f926600e3382586defd6c6bd84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 22:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:11:59 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 22:12:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 22:12:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 22:13:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:13:36 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 22:13:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 22:13:43 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 22:15:53 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:15:55 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:48:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:48:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:48:17 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:48:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:48:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:48:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16556704259948e469d295ad17c0b83303b045ecaedafdd2e16e153313e1dfb6`  
		Last Modified: Tue, 02 Jun 2026 22:16:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d711fc9f348f8b578e18995374d27b40e5900dd346ce6989dbf8a03d6379ed3`  
		Last Modified: Tue, 02 Jun 2026 22:16:04 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591205aec584bc9bf82bf950d86511bf856df5b80cfc692ffebf5597ca68b7e6`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22c20181a321c9aa31806b3a6299f064d89d5be9ef4ec4b8643e9648f096b20`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875bb11e80c093d7133bdc63d9eae1ac2b5c3615c2548955f18ce7dc1cbcdd1`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec55ad5b4586a55352fbd4acd5057d226c2736b7bf5617ba58c7b1ec5a01595`  
		Last Modified: Tue, 02 Jun 2026 22:16:08 GMT  
		Size: 51.4 MB (51351865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8157f646be5f683d250a6f17ff707476c9c8021878b249e269ce011d3ff874db`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363dcd54d5e980b27d8e067e3aa0681d0a3b914f0cd2fee65597fc3cc09fecb3`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 347.5 KB (347472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89e7d73520ffce5ef45fce95d33eb59c6e81aa2a9b702762d10955702c63f88`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03786a5498c3138a7f68d31bb4b48bba38614a87e19b581dfb213237d20256`  
		Last Modified: Tue, 02 Jun 2026 22:16:12 GMT  
		Size: 69.9 MB (69908615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717522dbb34fae4042da878f0e2b02e156afeb7efa63dd68f87a0e670c1777a0`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c100a71c72bd8a3ae733ff302b773d79c1f9d9567e2ea92e5a14cabfad16946`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973c59f163b420ad3e89ff70cbb614dd936a7c672446a4f96680cf7ea2033b1`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23746fb5a19760542ceaf1982c31d671001d1e61c45ef53459e38fe02213c2`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d27ae839dc6cc7d7a119bd9b2c302ae49b265e40e36003baed2d882a8b80f`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415c477003a7c45c620ddf022beae3a2649f87cdd579da1617144d132e961953`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 2.3 MB (2296661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5287c072e6ec74e531802fe71a613d30d89698c4a47bc8e3f1ca00ee98a1249a`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11-builder-alpine`

```console
$ docker pull caddy@sha256:3eae6b351ecdb05da6d16e341261a457692d344a435764c5ece7a60cf03a23f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2.11-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:db3ae9a5913d5b9305c729247b8ee6ca7596823a3a9419eaac330e5f374c3157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79773771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591706032a9a5c14da6e7f446e0083d6747768d50d0bf9da36e55c2421e94a2f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:53 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:11:59 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:00 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30edd47abbca5172a1775d1ba8a17aef65500a7a1ecc50af582706ad0c19ab`  
		Last Modified: Tue, 02 Jun 2026 21:45:09 GMT  
		Size: 290.2 KB (290247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaa626ba3010d60ab55d9cdc69c0b12ebff5d1b5ece83ff220fb46a7709b3b`  
		Last Modified: Tue, 02 Jun 2026 21:44:37 GMT  
		Size: 67.3 MB (67283031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abecc8ee46932a01c961a896c3c87dd0efe1301916e124bdac46f96ae6e9dee`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca4922139842e28e1d61aaac141bc8576337fa9b8d64d1d9f723d161fb30612`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 6.5 MB (6489213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fa1420c37ef3c625b9f14ee901574c588fc49b3eb5a8fca1a8a732fd47620b`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 1.8 MB (1846501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e306254cc3a4dab0c2ccd0f548ad566fa5aa81a412b9b432d81889526a2bbf2`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ddd773e864a4f4e091e1f4bfdbd60371b4c51910be5ccb610589b8a6883de8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4dc9d9bcee8d699bb42f311997ea36c642596e4004aa8859d0781b30ac2c9d`

```dockerfile
```

-	Layers:
	-	`sha256:d055d9682529a9387da6c4adbc8bdc265d0466484002fca96e29c90f179091be`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 280.8 KB (280776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490b4b762d29e23f9c30e7d63d2f4fde87253b5f126903cfd336647e4cf6c3af`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67c97e86bbcf6c6d84c8a191e6f9c07550c3ff25bfef23d3e8ee6a6407d6d801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77801132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8375fe7e15b17bead87deaac11514fa70da1cd8427509b1c228967a15f141eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:01 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:15:26 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:15:27 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:15:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dc79104d8e3b9e93b7ff3163839b44dd0979c52b2f81f68e01be8f60d9d090`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 291.0 KB (291036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb989b4b1329f80799d899b8d7259a6658047b39b2b670ed0cc8620dd1d357c`  
		Last Modified: Tue, 02 Jun 2026 21:44:18 GMT  
		Size: 65.8 MB (65785954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e947158a0266891a134507f0a6253aec12f2c7656af2daefbed99f399148f5`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620327b269f4fa8f6e186115a4ab2a342dedb497a9044abd4a5b3246f11d3ac3`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 6.4 MB (6406685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a7c7f37dd2ddabcd39c4ec78c16b8efaf799e1db677a0a88c55ba2bd16132e`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037287d5c994a910febeca5542dc101d590c0256e293e25e7ddb97f4b25eba7b`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ee8a613597922f4a0c6ad805948acd213e018eb8e3548ca5b98e7cb6c0410659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a997af74d3004a92cc163aa5d9f843ecd7552d9fad60e39cc23d5f4340ebdbd1`

```dockerfile
```

-	Layers:
	-	`sha256:b77f8ee7de0cc1af47105376a1a978c3bd700001392879cba9b348c38f53c909`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:081203e78dbbdf584d644a704dbce3dd01e8d923760b1e4160a615e9c0282f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cece6d48bcb1d2e37ff13a3299d3382dd7c3a18c66cd620c334b6e7e45b85c5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:51 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:54 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:48 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa788fec666273423bc95c719209c3f49b0d2c1c28fdaf669e4ebcab932954`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 290.2 KB (290169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f46eeae83dd5d801ff20835cd1ea98f630698b9c066e10ddf320a1c9d42c07`  
		Last Modified: Tue, 02 Jun 2026 21:45:10 GMT  
		Size: 65.8 MB (65786124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494a0eb08b28e7075149245f5ff666eeadec03e6b1b08870ad1caa24151d00b`  
		Last Modified: Tue, 02 Jun 2026 21:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba6d2d27897ace71b8214e93839ab4dddfb4bf51e5dd9871755073b452fd92`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 5.9 MB (5859405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d200f1ff9040ab5ed074d40e2c5d715e5ca869a8c3c9ca357f24b30cc08f2`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 1.7 MB (1738762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392245d1b10f490bef242becdaf6b658edb173425508af51312e2d0c7703b3c5`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0207715e319528107b0ca90c4b3ae044a8636067b8544656cf7cfa660dbd93d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd6848c1a5afb6c01dd7ed0eea80f86a4053eb96a8d94f50bbb86131989d4a`

```dockerfile
```

-	Layers:
	-	`sha256:dda72704ff023245a1d0202ebcabc8675ff1d722be6ba03fec1b7ce479c3a68c`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 283.2 KB (283168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac1a6806382a02068a2684ad9fc775685c890f3913b65b2de640fe3eca324e6`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:13da9d8308a65d8402c19528f51e19a2535fcd2f28ee893feabfefab09afb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76951883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114e448de61888adef08f63408e9426eb63ce6db5c2c1066219d9ba0222717c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2c0198c180cf41cbfd73e25946fc0ccc373d0fee89deb6e7eeec7b1f8612ee`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 292.9 KB (292861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477eaf154b7c8070862d9db01681f78c8a60ce90e8936310f6a906696df475a`  
		Last Modified: Tue, 02 Jun 2026 21:43:59 GMT  
		Size: 64.2 MB (64166971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb4739b26b76346d1281fb8fac14c5bc8025bfc580405cc95aa21736e41116`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e7c04c5116e56a4edea922d39e62c3fe0cfb06ee580b89926af1db83402ce`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 6.6 MB (6575206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57c7a67944f4fa914947979e30a6c1db54ab3c9b1aac79a9ebd7b36e8e39b0`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 1.7 MB (1716384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ee51343f308260ed7fa9020154c216542e21fd2589bc41d85b57f77166a81`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ce914fd434a8d09e7d2f73c5c9b354b42cf9c31d65fefbe292f23eacb6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 KB (300526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbed50fbf772e7e0ff9b816eb3a8dc3e213df0f8c75ba10dc5924412b0e4d841`

```dockerfile
```

-	Layers:
	-	`sha256:add9c054a1ac3653aed38da164cb08126bb46bb4bc153c6f12848191bed15b4b`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 280.2 KB (280230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838bb928d6772b6ebe8d87d60a85b358fd40eb2166c93cb622cee8a22a537ca3`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:658d12b9b7e489cdf05a0115f8fd9c8e392ee3160ba5b96d5f6b1e3cf0e02802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2568f1df66f499486924dad3ad55e9449d549bbb37426e3354addf15c6c7df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:42:40 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:18 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:19:34 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:19:35 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:19:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94153723d1545849cb54e33c3f8f977f110afcb00da0d5d32236b24537c1a4a3`  
		Last Modified: Tue, 02 Jun 2026 21:43:46 GMT  
		Size: 64.8 MB (64840550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4ff149d61b69213dc146324696a7a3af1a2b46684c6f928dfca1ae8489a0e`  
		Last Modified: Tue, 02 Jun 2026 21:44:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3cb06425959c67588985a91f934858685c3d7e6f0a3094af6c96ef93508d2`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 6.9 MB (6906465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966eded362018ac5d0b34cafa47d109cf32bbdeac194c1582640c28fd31f3cb0`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 1.7 MB (1705993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88bcc980b0c8d2d3de3ae12ec5a268bf23ac450cf0e10b8726131fa5f50dd3a`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:636aaf3183699721a688bf9903f4a642af3556d22fb14b8142bb3d77e9e02f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4888dfc41af739498c0157e20326f403f56cd8400b521203907e2cce1bfb8403`

```dockerfile
```

-	Layers:
	-	`sha256:00729d38b67285f7a79eb306240810accdabec647d996c8e36ab458f490a827c`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 280.2 KB (280199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ec6cfbc1bfecb50f2c2e12352351ad7a86aa62458697127bd6d635c92ce4cb`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:851cb908798b1538ffe3a3053bb98a32903f158a7f1ca9eeafb0fa30f6f34f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77424217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfc4a9d5f64621b356f7b47c6c48337fe32d5912cfc96a0484d5c999eabca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 23:12:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 23:12:42 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
WORKDIR /go
# Wed, 03 Jun 2026 05:24:30 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 05:24:32 GMT
ENV CADDY_VERSION=v2.11.3
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 05:24:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8f135b9aec9b42cabcdbc9e60e1e2b738fe71cb50c44dd091c53fb8edc94a`  
		Last Modified: Tue, 02 Jun 2026 23:19:15 GMT  
		Size: 65.1 MB (65148394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c4848fcf3e91f4413c1666bace4337c4f1c12c50976959bd29ad011c4d936`  
		Last Modified: Tue, 02 Jun 2026 23:22:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc28d768f2c71e4a402e2f4424963bfaa465d9c4a2f36c428bd41b08e3d6d2d`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 6.7 MB (6672809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5d5e4441c4e23a30ad21c2b66c3a336df57c4bfda44ff5113b5b3be8e2ffc`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 1.7 MB (1724208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80fdf8a500696ba07bd03f2a260b2e578f3e7909bec500d7122de9d25041d6`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:dca192295748614e125d445ca613cc0972469b2e1774dca65dd6b47fe9d2682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a911353b6377828995df9827f453d124992e5ff9b7484ef6ebc4da9d7258c820`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc98528c0380ded7049be92a37c9302d44d983dd53bba1648e04dedd55efb4`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 280.2 KB (280195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb92a4e503b3fefa7c0f01279adf8084dd01665b4d68fcef6d623b33d866cb16`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2.11-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4b90e008693f441e0c5337ba3fedad55597c1c61e2ecf25f2241f3a878b58d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cee611b412138469260e614e91691e6b1868b70e66aabd6488d8013d7cf3ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:02 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:13:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:13:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95f9225fe123215e56024e7fcaa3f2eb9fb3081c2d6160ebae532ca6d5eefd`  
		Last Modified: Tue, 02 Jun 2026 21:43:22 GMT  
		Size: 66.5 MB (66513822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9138885877e3f590d4144dfc2ec737113acde73b99374df82c5be8c2901f3dd`  
		Last Modified: Tue, 02 Jun 2026 21:43:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91584af5ed277f32349e17cda1214326d518b9f94719dc5c4e741329ee86f375`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 6.8 MB (6779991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30090c473a211354bad44ab67b863187e6614231a73dcf0aa22173ee79b1a359`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 1.8 MB (1782842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3da51a38e8b113b744ea5418d02a52a6b6def3db40a219f602fa5e52065bfb`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2.11-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:578a971dec1e6528eb9512ec7c3c538b18cbeb2a8d6c72b4f420d6992b30009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f17854159ec165c92bf0e0220d91246d07bd68f48b8fa569c16a68552d0058`

```dockerfile
```

-	Layers:
	-	`sha256:4915df098870636a12ece0bc09cc5fc8dee8954c6116a7cfb93bf9f3169bd426`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 280.1 KB (280125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97af12336dd47a218f778a32b9bf8cf6ecc4d8ef33a28f7bb8c621a730e6343b`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:2.11-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:2507e19ef745b79bb6d80853a1f496cf6ccc33b2952dd338d29574b3a40b7817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:2.11-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:5c6e7364201194ab26b433feaf24cec26dd47fa67d0191fd5aac9a3145f2d75a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2246342426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4817db1df805c59c442b0aae0af3740b59c437f926600e3382586defd6c6bd84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 22:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:11:59 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 22:12:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 22:12:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 22:13:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:13:36 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 22:13:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 22:13:43 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 22:15:53 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:15:55 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:48:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:48:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:48:17 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:48:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:48:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:48:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16556704259948e469d295ad17c0b83303b045ecaedafdd2e16e153313e1dfb6`  
		Last Modified: Tue, 02 Jun 2026 22:16:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d711fc9f348f8b578e18995374d27b40e5900dd346ce6989dbf8a03d6379ed3`  
		Last Modified: Tue, 02 Jun 2026 22:16:04 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591205aec584bc9bf82bf950d86511bf856df5b80cfc692ffebf5597ca68b7e6`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22c20181a321c9aa31806b3a6299f064d89d5be9ef4ec4b8643e9648f096b20`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875bb11e80c093d7133bdc63d9eae1ac2b5c3615c2548955f18ce7dc1cbcdd1`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec55ad5b4586a55352fbd4acd5057d226c2736b7bf5617ba58c7b1ec5a01595`  
		Last Modified: Tue, 02 Jun 2026 22:16:08 GMT  
		Size: 51.4 MB (51351865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8157f646be5f683d250a6f17ff707476c9c8021878b249e269ce011d3ff874db`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363dcd54d5e980b27d8e067e3aa0681d0a3b914f0cd2fee65597fc3cc09fecb3`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 347.5 KB (347472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89e7d73520ffce5ef45fce95d33eb59c6e81aa2a9b702762d10955702c63f88`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03786a5498c3138a7f68d31bb4b48bba38614a87e19b581dfb213237d20256`  
		Last Modified: Tue, 02 Jun 2026 22:16:12 GMT  
		Size: 69.9 MB (69908615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717522dbb34fae4042da878f0e2b02e156afeb7efa63dd68f87a0e670c1777a0`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c100a71c72bd8a3ae733ff302b773d79c1f9d9567e2ea92e5a14cabfad16946`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973c59f163b420ad3e89ff70cbb614dd936a7c672446a4f96680cf7ea2033b1`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23746fb5a19760542ceaf1982c31d671001d1e61c45ef53459e38fe02213c2`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d27ae839dc6cc7d7a119bd9b2c302ae49b265e40e36003baed2d882a8b80f`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415c477003a7c45c620ddf022beae3a2649f87cdd579da1617144d132e961953`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 2.3 MB (2296661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5287c072e6ec74e531802fe71a613d30d89698c4a47bc8e3f1ca00ee98a1249a`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:688be35a61ebeccf90e1956f0225b3db0280e79964863fe7b93addc0864838fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:2.11-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:6bac99d1de9debbb801646208c923809fe18cbb945c6d430cc8f1d38c5ba14ff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335210672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45bc764ed6ce43900c66e7269ef9b64bff9f78aca8a5412c2bdddba4456a779`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 21:46:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 21:47:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 21:47:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 21:47:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 21:47:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 21:48:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:48:54 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 21:49:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 21:49:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:50:55 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:50:57 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:33:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:33:57 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:33:58 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:33:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:34:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:34:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03db002b9e59a168b97269178d3cea6be969a491719ca1c8d3f4c33ad9ad07f7`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b9c42b86ca2e7aa4eb41766a6f755119c65c8b2c03b320ba0980b9d2f6547a`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8f4def2bce82d1e544606aaf3e5895ae29437220f1b41211727fbeff83ac8`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16228e0f3edb3815e34fd2d8c6d575e9ed737e1d5cc07909e430d670860bc7cc`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca5f94c0122485a7417a90a87018bf739ef6ef80f60454b5258cefa6a58eed5`  
		Last Modified: Tue, 02 Jun 2026 21:51:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1397a64df19d921e6ad74f8c6ca0ea5b401c7731318c4dd85002c5dbb6df922c`  
		Last Modified: Tue, 02 Jun 2026 21:51:15 GMT  
		Size: 51.3 MB (51286214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871cad50024619c7f067652dc3cc2e678a8c70180235a578d249123c21479637`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007a76e9414e0db486efb9ff5a4409e15cef9f66f3c19a6efc5d554db55f0e4b`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 367.1 KB (367144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fea8e7d4ba560522bf09b19a63fc47cca6a724baa7e90623086a8d46f1d8f2`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44107094e22c635252ccb6df8685c7968f63f084760fcbec0f4cb08857a74`  
		Last Modified: Tue, 02 Jun 2026 21:51:19 GMT  
		Size: 75.3 MB (75252822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35936631b6cd9bd6e5cf14e0cb4f8a287786047d069c23d09ed69d69e5672e`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfefceaacb32ce75c4aaba58b81bced50aae117cc616944d49a92ce10e866b2`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d897cbe5e09e88bd391baaa18698e2d8eb277aa581a683b8025c4f230f1adf7e`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4b32c912e804ac74f332ad5ab2d2b281dc7e6d481f6f80a4f43df475616659`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f053ec3b21275df3413b9168645d21fb9bb677da4c1d6c12e96049e54cabfcd`  
		Last Modified: Tue, 02 Jun 2026 22:34:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b1f65dcb82cba9c705872f745be1ac11720b8c76eebbe4e9942f2f2e810cf7`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 2.3 MB (2345713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcd5aef19be6456c21bb9609b574709a6500a0642321c9435e2421d39818fd`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11-nanoserver`

```console
$ docker pull caddy@sha256:99fae4af425b9fcc81d4b2efd241cbe3dcac78350f37c4ed2daa6c35df2793df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:2.11-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:3e5afaeda3465c585afea0828ec650f60e760f92ab1096cbdd12bbb7044f93f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217870731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4c6463b2201d0e16cdf07c19f7038d51083193293932e21b857521bf02bab9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:30:16 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:30:18 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:30:22 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:30:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:30:33 GMT
RUN caddy version
# Wed, 13 May 2026 00:30:33 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1fedb6255043325f0c6a8118656684fcc0c1eb9b84857ff574105bdd45da85`  
		Last Modified: Wed, 13 May 2026 00:30:44 GMT  
		Size: 71.9 KB (71893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde99a62b5456da395a4f921712e08ec242d9c53791f22763e904483b90bb0ff`  
		Last Modified: Wed, 13 May 2026 00:30:46 GMT  
		Size: 17.5 MB (17549616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfaf73426fda2a4ab3e9ef51a62f30bf03cd7bb09987eaed20cca2f4baf6c72`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 271.7 KB (271708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee506f35cf26ab6a4307a617c899a31108d35a38976dcbace37f776be3fa88b9`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 111.9 KB (111876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae64a8691f6412e9e7b124cb1506d63cbc0888dfda70af2a058cd92483d1bf3`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e08e3975dc80abab1d7078a935b8310dfd0436900117ac019cf7e74e96327`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa53d7a29128e22ba5071bc2c061d21df2672618f2d335495eee03b57b30eec9`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9aa3dda4800660b0c498edee92d63a95f3487dea910ee7b1e32237e7d8c01`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602df0b26626bd70f3e3b7e338c29f3774aadcb1993b32e11424961d5818b71`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c12f0b0a957349df9e5cdec68e05f8555034292db7712c2189c98bd96a1e`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573942fa9e85b5ae2a2dd8eebbfe68a15cbc4562d77ed7b34b827ddf38d67873`  
		Last Modified: Wed, 13 May 2026 00:30:40 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6577aceea038d31c6741058ac70f3042052944add747d78e1e98f4768056ad9`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f767fdb48bc45cf9dfc7586e7f3bb6923b4260220f4751867e56819d9198c6f7`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805ccff5e068c1b1ef4ee49960a7779be478d8aac505863b20d6779b21c86cbc`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a088d5cf08a67d2b16495569498bf84dc519c98894eef90450facae9b2b1fd0`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a013ec9aa226e3c490885f2df243f133e073c70c9f7fe42acf1c7c6d646c4`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c59e03f4cda98b2b89df28ea3599e7ce642f3438c9607747e027edae7d633`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df98da5df2a594f3eaf8a18d588dd2dd717a8b9d65120307073b5097a7461ab1`  
		Last Modified: Wed, 13 May 2026 00:30:38 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738c190dc62e002473b0f2e0a6b4d56acd58d4befffd3a5254489344e3f514ad`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 110.6 KB (110619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d153bfc2eaf47e5d03b6d7723d1c90e94fbc34f9bd5394c155057ec6cb0fc42e`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.11-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:f2b8fdc30136d5694f4d937911af2a98122816cd9382f30f5e188034eb925ee8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145172029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a188f7374e0862b018d9c6a58ee464b17ed26b607a136f3c2f81f6ba750a8d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:33:03 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:33:04 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:33:08 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:33:11 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:33:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:33:21 GMT
RUN caddy version
# Wed, 13 May 2026 00:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471afcd67b75eae029a73dd0dd5c78c7a867343259b55e8a2ce811a682e0cecc`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 75.7 KB (75727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82a36e1bbf75e8321fe17d1997dc9a3fb4d0322fec9092d1c1da3f90b2872be`  
		Last Modified: Wed, 13 May 2026 00:33:34 GMT  
		Size: 17.5 MB (17549625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1c8055df56386428b23be9cc63963727ee8c65d8ccffd1cccb3768eb2e2233`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 271.9 KB (271937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802218197b7b44f15d0c35e1f92bcebeab5b5348fef8370532d04f6e9eae967`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 109.6 KB (109634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1878ea730f12e1f174b5f94eae4c28852ba7d131ff79831bb232b1d3bd2a9195`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5dcf5eafb5625f15b6c8221a6e8033e90b2e194cf46387f7384e9b4a9fbd3c`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4835c93d3898ae70cc7ac56c9260fd82bf21232d466b88b0c18317f927fad95`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e837a3b4c7f62a51617a0817e87c40d393639d84181cce582cdecd0ed04f6b49`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4bdc974f597917738eb16a57d09d2eb7d4932fb411b582d7397d1e49d850ee`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa60544a60e2a9391135d903f2cf2e1104b968bf0cb17d7fdc7896f5e8a41d7`  
		Last Modified: Wed, 13 May 2026 00:33:29 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f676e12689f61e65afafa2dbabe0f87066ea23a433b6bab30a252984ea3bfcce`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c8bcb78837d9611d2e6d737f1983724070a8b8dc651967aa131aaf3b53db2`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fd9964db11cc46a832c192535f0da8d40411e0e4b90d4735a417e2b21e546`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b24ac8b6e8779c0ea8641c14aa97c30b88dfb2dccfef053e31a383bf8772a0`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14623bf8cac2234d2402f1b77f9f8b9ad17f42b63c25eac6a03a874f2b96603`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf92d85a26150eb8504b9bffa3855decbd94a1cc1614f643dccb2a544ed2818`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6be3b806219581d0384bebe4e25fde1cc050ad9ea5def7c549bbfc37fdec69`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183f69d2299c1c4178f5941ded18872ae1a092d5822f9b2470a9bff9febadfc3`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4db159e8ff27f5e761dfc5a73a64fc1bdeeec4bb736d0de7ccdb6479e4d49d`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 110.4 KB (110391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec19313137639151ccfb4e3125b9f946f903e0153e167a6df587f323d036934e`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11-nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:5d09312d850c343bf10c4b5d1f831d63fd9e62aaba2eb17ab04136849c9b7731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:f2b8fdc30136d5694f4d937911af2a98122816cd9382f30f5e188034eb925ee8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145172029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a188f7374e0862b018d9c6a58ee464b17ed26b607a136f3c2f81f6ba750a8d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:33:03 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:33:04 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:33:08 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:33:11 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:33:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:33:21 GMT
RUN caddy version
# Wed, 13 May 2026 00:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471afcd67b75eae029a73dd0dd5c78c7a867343259b55e8a2ce811a682e0cecc`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 75.7 KB (75727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82a36e1bbf75e8321fe17d1997dc9a3fb4d0322fec9092d1c1da3f90b2872be`  
		Last Modified: Wed, 13 May 2026 00:33:34 GMT  
		Size: 17.5 MB (17549625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1c8055df56386428b23be9cc63963727ee8c65d8ccffd1cccb3768eb2e2233`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 271.9 KB (271937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802218197b7b44f15d0c35e1f92bcebeab5b5348fef8370532d04f6e9eae967`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 109.6 KB (109634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1878ea730f12e1f174b5f94eae4c28852ba7d131ff79831bb232b1d3bd2a9195`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5dcf5eafb5625f15b6c8221a6e8033e90b2e194cf46387f7384e9b4a9fbd3c`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4835c93d3898ae70cc7ac56c9260fd82bf21232d466b88b0c18317f927fad95`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e837a3b4c7f62a51617a0817e87c40d393639d84181cce582cdecd0ed04f6b49`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4bdc974f597917738eb16a57d09d2eb7d4932fb411b582d7397d1e49d850ee`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa60544a60e2a9391135d903f2cf2e1104b968bf0cb17d7fdc7896f5e8a41d7`  
		Last Modified: Wed, 13 May 2026 00:33:29 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f676e12689f61e65afafa2dbabe0f87066ea23a433b6bab30a252984ea3bfcce`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c8bcb78837d9611d2e6d737f1983724070a8b8dc651967aa131aaf3b53db2`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fd9964db11cc46a832c192535f0da8d40411e0e4b90d4735a417e2b21e546`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b24ac8b6e8779c0ea8641c14aa97c30b88dfb2dccfef053e31a383bf8772a0`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14623bf8cac2234d2402f1b77f9f8b9ad17f42b63c25eac6a03a874f2b96603`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf92d85a26150eb8504b9bffa3855decbd94a1cc1614f643dccb2a544ed2818`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6be3b806219581d0384bebe4e25fde1cc050ad9ea5def7c549bbfc37fdec69`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183f69d2299c1c4178f5941ded18872ae1a092d5822f9b2470a9bff9febadfc3`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4db159e8ff27f5e761dfc5a73a64fc1bdeeec4bb736d0de7ccdb6479e4d49d`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 110.4 KB (110391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec19313137639151ccfb4e3125b9f946f903e0153e167a6df587f323d036934e`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11-nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:0cd979a2fb38e0ef8a3f7e405a19569c9930e820125c1d08720b752d6ba78e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:2.11-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:3e5afaeda3465c585afea0828ec650f60e760f92ab1096cbdd12bbb7044f93f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217870731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4c6463b2201d0e16cdf07c19f7038d51083193293932e21b857521bf02bab9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:30:16 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:30:18 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:30:22 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:30:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:30:33 GMT
RUN caddy version
# Wed, 13 May 2026 00:30:33 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1fedb6255043325f0c6a8118656684fcc0c1eb9b84857ff574105bdd45da85`  
		Last Modified: Wed, 13 May 2026 00:30:44 GMT  
		Size: 71.9 KB (71893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde99a62b5456da395a4f921712e08ec242d9c53791f22763e904483b90bb0ff`  
		Last Modified: Wed, 13 May 2026 00:30:46 GMT  
		Size: 17.5 MB (17549616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfaf73426fda2a4ab3e9ef51a62f30bf03cd7bb09987eaed20cca2f4baf6c72`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 271.7 KB (271708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee506f35cf26ab6a4307a617c899a31108d35a38976dcbace37f776be3fa88b9`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 111.9 KB (111876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae64a8691f6412e9e7b124cb1506d63cbc0888dfda70af2a058cd92483d1bf3`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e08e3975dc80abab1d7078a935b8310dfd0436900117ac019cf7e74e96327`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa53d7a29128e22ba5071bc2c061d21df2672618f2d335495eee03b57b30eec9`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9aa3dda4800660b0c498edee92d63a95f3487dea910ee7b1e32237e7d8c01`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602df0b26626bd70f3e3b7e338c29f3774aadcb1993b32e11424961d5818b71`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c12f0b0a957349df9e5cdec68e05f8555034292db7712c2189c98bd96a1e`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573942fa9e85b5ae2a2dd8eebbfe68a15cbc4562d77ed7b34b827ddf38d67873`  
		Last Modified: Wed, 13 May 2026 00:30:40 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6577aceea038d31c6741058ac70f3042052944add747d78e1e98f4768056ad9`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f767fdb48bc45cf9dfc7586e7f3bb6923b4260220f4751867e56819d9198c6f7`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805ccff5e068c1b1ef4ee49960a7779be478d8aac505863b20d6779b21c86cbc`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a088d5cf08a67d2b16495569498bf84dc519c98894eef90450facae9b2b1fd0`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a013ec9aa226e3c490885f2df243f133e073c70c9f7fe42acf1c7c6d646c4`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c59e03f4cda98b2b89df28ea3599e7ce642f3438c9607747e027edae7d633`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df98da5df2a594f3eaf8a18d588dd2dd717a8b9d65120307073b5097a7461ab1`  
		Last Modified: Wed, 13 May 2026 00:30:38 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738c190dc62e002473b0f2e0a6b4d56acd58d4befffd3a5254489344e3f514ad`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 110.6 KB (110619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d153bfc2eaf47e5d03b6d7723d1c90e94fbc34f9bd5394c155057ec6cb0fc42e`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11-windowsservercore`

```console
$ docker pull caddy@sha256:4b2309a8fe290a6271bb2bdd006c30f27a06e0e18787c56c8604b1facf1cc9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:2.11-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.11-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:672b320378b1e89dde74d15a8a123068d26dafce6901597f4f8a837c5c38e7b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141244276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a5337ff6c38ebefe95a0943a39f42bab87a62f05d840422d53a0be69b65f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:59:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:59:25 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:59:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:59:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:59:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:59:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:59:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 80
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 443
# Tue, 12 May 2026 23:59:42 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:59:43 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:59:48 GMT
RUN caddy version
# Tue, 12 May 2026 23:59:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be1f105178ea258d105ecbaf5ec1f6000c5b289826e3b432c22080c650f719`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 524.5 KB (524474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7902ee53436295b9cb02bfa64ac6aa3b314c1e926ec77f7bb59eea811e28a846`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170554e1bf42badb647bc34b5718a5915fede948183bf5dc3d0d21e5540a0b67`  
		Last Modified: Wed, 13 May 2026 00:00:00 GMT  
		Size: 17.9 MB (17925247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a6d017c1aab65f96bd924d664427c093dba8210995905eaf00df2fbd142cb`  
		Last Modified: Tue, 12 May 2026 23:59:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04fc399abb90e3e2df99498e2eb88e7afd2a3f97e84400a40b7439ea46f1fa5`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d26c10fbf4dafe70c44037417bb3457e50a549f998a6f8b4799cf456c446e2`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295c37ba01761384092ce6a3f611a8792a57e0f772e6d8e3bfb099f51932a73`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb5b45ec93d301f781dc64b899fdfaa452f3d35dbbe0ba52fc5c87b02593d0`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0f84b59aead90c71aa95cd5340904935ff3da90339fa6ff21049d0f56f9ec`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1aeb5b58eaf433feb7668159802420e22345953cd345a111f5ff264e659bdf`  
		Last Modified: Tue, 12 May 2026 23:59:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03412a72c6ae737ad61b888338ad28fdc2b3477281195707e27619683236208`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a705083dc71361abc6a1e82aa158830dc6f3dd6e486a403f011f357eae4d884`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5637de44873a5862f646124e27d0fe311506c6fa1eec39c15df5312e1d41881`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4356db0d34adcecf1c9218951422411d7f942cb4d50621800af19388fdcc0`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a670d1e50cdca965f8cebdbf95f43d51e7fe8d7daf65312384a5731f3f743e`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc67002143e99034340b46a68c760d90626fe51d4e087bca7be0aa904ec8b45`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c8eddb6ea788613d96893c8e7c570d4a29a2b07f6d1ce823bf72faa05cf7b`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c21c96cd26011f147afe2c8c693897e2a126fbba132af7fc830d2d7559f19`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 351.6 KB (351565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c0ee074e227c1b13e1438189cfa031217727fc8085182b53234397774d341`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:13a01e024e1f987d2133e73315fea5688b3dde0f70bced70f1caad7c2b53e092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:672b320378b1e89dde74d15a8a123068d26dafce6901597f4f8a837c5c38e7b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141244276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a5337ff6c38ebefe95a0943a39f42bab87a62f05d840422d53a0be69b65f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:59:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:59:25 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:59:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:59:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:59:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:59:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:59:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 80
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 443
# Tue, 12 May 2026 23:59:42 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:59:43 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:59:48 GMT
RUN caddy version
# Tue, 12 May 2026 23:59:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be1f105178ea258d105ecbaf5ec1f6000c5b289826e3b432c22080c650f719`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 524.5 KB (524474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7902ee53436295b9cb02bfa64ac6aa3b314c1e926ec77f7bb59eea811e28a846`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170554e1bf42badb647bc34b5718a5915fede948183bf5dc3d0d21e5540a0b67`  
		Last Modified: Wed, 13 May 2026 00:00:00 GMT  
		Size: 17.9 MB (17925247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a6d017c1aab65f96bd924d664427c093dba8210995905eaf00df2fbd142cb`  
		Last Modified: Tue, 12 May 2026 23:59:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04fc399abb90e3e2df99498e2eb88e7afd2a3f97e84400a40b7439ea46f1fa5`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d26c10fbf4dafe70c44037417bb3457e50a549f998a6f8b4799cf456c446e2`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295c37ba01761384092ce6a3f611a8792a57e0f772e6d8e3bfb099f51932a73`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb5b45ec93d301f781dc64b899fdfaa452f3d35dbbe0ba52fc5c87b02593d0`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0f84b59aead90c71aa95cd5340904935ff3da90339fa6ff21049d0f56f9ec`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1aeb5b58eaf433feb7668159802420e22345953cd345a111f5ff264e659bdf`  
		Last Modified: Tue, 12 May 2026 23:59:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03412a72c6ae737ad61b888338ad28fdc2b3477281195707e27619683236208`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a705083dc71361abc6a1e82aa158830dc6f3dd6e486a403f011f357eae4d884`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5637de44873a5862f646124e27d0fe311506c6fa1eec39c15df5312e1d41881`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4356db0d34adcecf1c9218951422411d7f942cb4d50621800af19388fdcc0`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a670d1e50cdca965f8cebdbf95f43d51e7fe8d7daf65312384a5731f3f743e`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc67002143e99034340b46a68c760d90626fe51d4e087bca7be0aa904ec8b45`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c8eddb6ea788613d96893c8e7c570d4a29a2b07f6d1ce823bf72faa05cf7b`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c21c96cd26011f147afe2c8c693897e2a126fbba132af7fc830d2d7559f19`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 351.6 KB (351565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c0ee074e227c1b13e1438189cfa031217727fc8085182b53234397774d341`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:206dde5cb85762b952e1ced7003d7630ae6e1f8f347ae67b56c84026948e8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:2.11-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.11.4`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-alpine`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-builder`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-builder-alpine`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-nanoserver`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-windowsservercore`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:2.11.4-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `caddy:alpine`

```console
$ docker pull caddy@sha256:86deaf5e3d3408a6ccec08fbb79989783dd26e206ae10bcf78a801dc8c9ab794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:3739ea4f0c877259a693d932693cf8f3408e9a9497c004f031b0e830e93e1546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23985030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5190456911cee510988a5fb9996188ef866fbcca3235cad19bf05f5f8f33386f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:12 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920de1d55d9880b00fbeaf8fa3757e89f7ea6170ff12633cbe766c2152a858d`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 2.9 MB (2886638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057c497bda068e80884e6836fbf8971a954593242af7694d080e6b81758b67f4`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b55c68e4a0feeeaec6f86ced6bd8790e19ed68399cff61bab00adc15895ec13`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 17.2 MB (17226669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e08c659e9fe301aa2814b2cafc4a5211423fcaa307a515772efeb816684ceb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cd52ea603ed29abf30a13e9ab37f92acffb93b53042a6bfaf1d22d9bdb8be`

```dockerfile
```

-	Layers:
	-	`sha256:4c4f094b32e82a0c66e0e5c00015a86d670049e4e9a336febc6c2a2fd626b19b`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 332.9 KB (332947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16285c7326d137b74e90d1f477040eb15643c312e7a46770316c0c258033326a`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:018595a3226de0d5c9055279af90983e9e91ca5f12dde17e93925455d19bc0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ce61ba53a04521d0e684e8048cde82ebd35cd3d72a9d1f7616056976e75253`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:40:51 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:40:52 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:40:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b1247b4f1cad33af22f46d45d07b1ee65401981dccc3fa920dafbde1fb072`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 2.8 MB (2819583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d84aa44715b44ce12b2cc9b98a20167ca060c5869ab67124210f554413d56ee`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93038fb49fb9d7664bc1a8209857cde656b4e5ff6ab5a7bf4b270d942f499d0`  
		Last Modified: Tue, 12 May 2026 21:41:00 GMT  
		Size: 16.3 MB (16311628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:de7fac8a337ded6fa61288d6dcc5837d472ed26f9d6b7230f0c8487fb9db984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feea7dba17177c5d72e8d8b883cd3bcdcda396dcc918c1e1e6d3868632932251`

```dockerfile
```

-	Layers:
	-	`sha256:2bd47793d94047373cab54d4b18f46ce16d19438827a8a41e3c5960cd1da48ca`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 18.4 KB (18353 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:2c3d3047a1705945ca9376ef8d3e9eb431f0f07f16e6ae2511326d7f0b664ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22262035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a70cfe7deb0544e9098ef10e20ebbc18e346bb3b8df5b140b9f184e71b4a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:42:08 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:42:09 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:42:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce55fb7d543ef0a1f852326909b7cdb22fb514199bd31b9543d92f04e878f4`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 2.7 MB (2681516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49caf58b5069e136a5fcd2fbaa18da4c786566963ba48bcedc27100b8a43365b`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ba28a73ebab4ca57472bca296d741e3d9b1cb27478c6adde87b7c314ba7810`  
		Last Modified: Tue, 12 May 2026 21:42:18 GMT  
		Size: 16.3 MB (16289861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:08ab34ff2df00fe711e074db26cf28e9b5ff1dbfe8355e0f414ed9a7c465cfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb11059736745812fc6bfa910b2d1cce68b03317d8452425d1f7954f2023f495`

```dockerfile
```

-	Layers:
	-	`sha256:95b578e25712b12ba424efc0abb0e6a4daa0cb6d145f200869796d863a0535dd`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 332.4 KB (332365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876e5685474ad9dfce16688d11127988be62753bb83e66c138c382a181530636`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 18.6 KB (18568 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ae38d5cc9674696bfec2dd7a20ea5495a2653d788ee39bff6aaf1007f8dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22800642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64000d357283f8b74cfc9cabce60768a6957447b74a7eb73c573c5d344a398`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:44:57 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:44:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:00 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6cabef06141e7f3aba6fa7d3898c4282f7316acb2ad612b8ea82ac9172cd99`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 2.9 MB (2900862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69f6bd08e27b5a1e9b73c99efae612626fabe895c78a156e402e5938112fff9`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 7.5 KB (7500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4e100b255f5c935bb23c7e5f2a23ee2b5b683a152149ad5db9b32d8455edf`  
		Last Modified: Tue, 12 May 2026 21:45:07 GMT  
		Size: 15.7 MB (15692378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:99d5c41f924f43a16554137091afc6dc8c34e2976b4011ea8793c6211676f8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 KB (351013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f8ace5e5ed9603a8a26766f5df8fd3efe32a76bb3d66c4017bf8bb842691c`

```dockerfile
```

-	Layers:
	-	`sha256:43c50900a0619c09f3987cc62bbfffd4d10da1b9d81fd21f3605e47dbb741967`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 332.4 KB (332401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e57f91d95d6c31886fc5dc74e74b86782c292b27bf964bb5023e301c36f8270`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d6f3adf638edd88132caec6005766ec86f31796069549755af52d172a03ebd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22551245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d82ac569eea06185f6688d103c7d7e2ef313dce067d6f1aca3b7255025aa450`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:46 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:52 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aba3acae7a944d3cb59ff0085839ecf6bc67e67a1ff5c9d62453ec36405516d`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 3.0 MB (3024677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef81e00b6b88436c8856bd7f6a2a40abea36897a22c7707cdf06722a09f8b819`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1e87608e2891184dfb2f547b0a2062b1bba1b787d3cd95ff36446affe940e`  
		Last Modified: Tue, 12 May 2026 21:46:12 GMT  
		Size: 15.7 MB (15688108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:863e023f3571814b385c37ac309e71a9a712f4aea420d2cea5032e2a362bf7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef881e7b8f82faab6a4473932499599574eb0bc9d0264c779647d0b099584f`

```dockerfile
```

-	Layers:
	-	`sha256:aa780bcad124738bdb6864e89c3299ebdcee766cde92da7db3f2ca1d99c22f23`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 332.4 KB (332354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cabca92420dc637383da8dc8f0d0276fcf258532404ff1d3fb1e80473359b1`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:69328a1677b50e71a30c554ca8dddf7f1ad2474084385dabd7a0d6fedc9a4118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22851653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086f5adaba5ab0d6ae67e9e685607028248302272c9befb82e9fba4246d6537e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 02:12:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Thu, 14 May 2026 02:12:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV CADDY_VERSION=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_DATA_HOME=/data
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/udp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
WORKDIR /srv
# Thu, 14 May 2026 02:12:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a638da60daf650b51909ed97e65ca82d6b4c622d9aad9e05a1fe86e41b1b8`  
		Last Modified: Thu, 14 May 2026 02:13:15 GMT  
		Size: 3.0 MB (3024903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e9ab663ff84756b43ea4456b9675a7bb4e9a21db93cfb2860477f1acc49fa3`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 7.5 KB (7506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207dafa63c1803835db9d283a462accf88a7d65b6c6a62ef6d00c05e7e2d4d85`  
		Last Modified: Thu, 14 May 2026 02:13:17 GMT  
		Size: 16.2 MB (16231550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2a37fc42537c780173072b08a797af48db02d1ca4bb14afe8301f380deb5f108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1087260f2ba70b75cfc134c58bb57369b570c4c836ad26b8a6774cfb2c421a26`

```dockerfile
```

-	Layers:
	-	`sha256:50741c878fc4519cf8be95491297cbbf12889e7fe8fe4cb6f0cb7a32aacd5a4d`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 332.4 KB (332350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074f80835103901f06cabe60ac917a34ae1a55cf6637768028867d83f6f31640`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:2be760d0b6dcefcee4d8e8de79e4fbc5bff379cc71f6ba4be329b95fee14ed53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23338359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bb7983fab4c669751406633c3cd0bacc33744d3c43dcecd96b365041e7d3b5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:39:41 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:39:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:39:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cb0bfcc1c8a81033ff4911e9096b260f4711f66484b04586fd6fa5ca95e44f`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 3.0 MB (3010703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bd7ba8a52c9fc9419b92337580db55dcd8690a637184fb22bec4871ffb8c0`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798a8d976afd31ca55ef92d83a93374f6c3e7ccd3add31769d768349700d623`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 16.6 MB (16593589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4a728924f65d2a9612ff66fbadd33d9a2d6e6b198cfc95cd6b23b89948cc2a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43f0c042f1bc3d80c67c0b0ad7df18ed102df0765f312c2619bed3d8392597`

```dockerfile
```

-	Layers:
	-	`sha256:4b3e6e6b8593dd35d4f0b59b89b012680c12c5498a7b01ae16bcb7ed34ac49a8`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 332.3 KB (332296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3864730b4cf584aa87e923de4848636482e8621df04a87733e10e42cc44e9b3`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder`

```console
$ docker pull caddy@sha256:d57008618f743e6308058d7bd990eb3489dfd04e2b82978cca7b953e1b491fc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:db3ae9a5913d5b9305c729247b8ee6ca7596823a3a9419eaac330e5f374c3157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79773771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591706032a9a5c14da6e7f446e0083d6747768d50d0bf9da36e55c2421e94a2f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:53 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:11:59 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:00 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30edd47abbca5172a1775d1ba8a17aef65500a7a1ecc50af582706ad0c19ab`  
		Last Modified: Tue, 02 Jun 2026 21:45:09 GMT  
		Size: 290.2 KB (290247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaa626ba3010d60ab55d9cdc69c0b12ebff5d1b5ece83ff220fb46a7709b3b`  
		Last Modified: Tue, 02 Jun 2026 21:44:37 GMT  
		Size: 67.3 MB (67283031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abecc8ee46932a01c961a896c3c87dd0efe1301916e124bdac46f96ae6e9dee`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca4922139842e28e1d61aaac141bc8576337fa9b8d64d1d9f723d161fb30612`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 6.5 MB (6489213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fa1420c37ef3c625b9f14ee901574c588fc49b3eb5a8fca1a8a732fd47620b`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 1.8 MB (1846501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e306254cc3a4dab0c2ccd0f548ad566fa5aa81a412b9b432d81889526a2bbf2`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ddd773e864a4f4e091e1f4bfdbd60371b4c51910be5ccb610589b8a6883de8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4dc9d9bcee8d699bb42f311997ea36c642596e4004aa8859d0781b30ac2c9d`

```dockerfile
```

-	Layers:
	-	`sha256:d055d9682529a9387da6c4adbc8bdc265d0466484002fca96e29c90f179091be`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 280.8 KB (280776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490b4b762d29e23f9c30e7d63d2f4fde87253b5f126903cfd336647e4cf6c3af`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67c97e86bbcf6c6d84c8a191e6f9c07550c3ff25bfef23d3e8ee6a6407d6d801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77801132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8375fe7e15b17bead87deaac11514fa70da1cd8427509b1c228967a15f141eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:01 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:15:26 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:15:27 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:15:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dc79104d8e3b9e93b7ff3163839b44dd0979c52b2f81f68e01be8f60d9d090`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 291.0 KB (291036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb989b4b1329f80799d899b8d7259a6658047b39b2b670ed0cc8620dd1d357c`  
		Last Modified: Tue, 02 Jun 2026 21:44:18 GMT  
		Size: 65.8 MB (65785954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e947158a0266891a134507f0a6253aec12f2c7656af2daefbed99f399148f5`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620327b269f4fa8f6e186115a4ab2a342dedb497a9044abd4a5b3246f11d3ac3`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 6.4 MB (6406685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a7c7f37dd2ddabcd39c4ec78c16b8efaf799e1db677a0a88c55ba2bd16132e`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037287d5c994a910febeca5542dc101d590c0256e293e25e7ddb97f4b25eba7b`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ee8a613597922f4a0c6ad805948acd213e018eb8e3548ca5b98e7cb6c0410659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a997af74d3004a92cc163aa5d9f843ecd7552d9fad60e39cc23d5f4340ebdbd1`

```dockerfile
```

-	Layers:
	-	`sha256:b77f8ee7de0cc1af47105376a1a978c3bd700001392879cba9b348c38f53c909`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:081203e78dbbdf584d644a704dbce3dd01e8d923760b1e4160a615e9c0282f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cece6d48bcb1d2e37ff13a3299d3382dd7c3a18c66cd620c334b6e7e45b85c5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:51 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:54 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:48 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa788fec666273423bc95c719209c3f49b0d2c1c28fdaf669e4ebcab932954`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 290.2 KB (290169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f46eeae83dd5d801ff20835cd1ea98f630698b9c066e10ddf320a1c9d42c07`  
		Last Modified: Tue, 02 Jun 2026 21:45:10 GMT  
		Size: 65.8 MB (65786124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494a0eb08b28e7075149245f5ff666eeadec03e6b1b08870ad1caa24151d00b`  
		Last Modified: Tue, 02 Jun 2026 21:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba6d2d27897ace71b8214e93839ab4dddfb4bf51e5dd9871755073b452fd92`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 5.9 MB (5859405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d200f1ff9040ab5ed074d40e2c5d715e5ca869a8c3c9ca357f24b30cc08f2`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 1.7 MB (1738762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392245d1b10f490bef242becdaf6b658edb173425508af51312e2d0c7703b3c5`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0207715e319528107b0ca90c4b3ae044a8636067b8544656cf7cfa660dbd93d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd6848c1a5afb6c01dd7ed0eea80f86a4053eb96a8d94f50bbb86131989d4a`

```dockerfile
```

-	Layers:
	-	`sha256:dda72704ff023245a1d0202ebcabc8675ff1d722be6ba03fec1b7ce479c3a68c`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 283.2 KB (283168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac1a6806382a02068a2684ad9fc775685c890f3913b65b2de640fe3eca324e6`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:13da9d8308a65d8402c19528f51e19a2535fcd2f28ee893feabfefab09afb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76951883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114e448de61888adef08f63408e9426eb63ce6db5c2c1066219d9ba0222717c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2c0198c180cf41cbfd73e25946fc0ccc373d0fee89deb6e7eeec7b1f8612ee`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 292.9 KB (292861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477eaf154b7c8070862d9db01681f78c8a60ce90e8936310f6a906696df475a`  
		Last Modified: Tue, 02 Jun 2026 21:43:59 GMT  
		Size: 64.2 MB (64166971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb4739b26b76346d1281fb8fac14c5bc8025bfc580405cc95aa21736e41116`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e7c04c5116e56a4edea922d39e62c3fe0cfb06ee580b89926af1db83402ce`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 6.6 MB (6575206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57c7a67944f4fa914947979e30a6c1db54ab3c9b1aac79a9ebd7b36e8e39b0`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 1.7 MB (1716384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ee51343f308260ed7fa9020154c216542e21fd2589bc41d85b57f77166a81`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ce914fd434a8d09e7d2f73c5c9b354b42cf9c31d65fefbe292f23eacb6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 KB (300526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbed50fbf772e7e0ff9b816eb3a8dc3e213df0f8c75ba10dc5924412b0e4d841`

```dockerfile
```

-	Layers:
	-	`sha256:add9c054a1ac3653aed38da164cb08126bb46bb4bc153c6f12848191bed15b4b`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 280.2 KB (280230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838bb928d6772b6ebe8d87d60a85b358fd40eb2166c93cb622cee8a22a537ca3`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:658d12b9b7e489cdf05a0115f8fd9c8e392ee3160ba5b96d5f6b1e3cf0e02802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2568f1df66f499486924dad3ad55e9449d549bbb37426e3354addf15c6c7df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:42:40 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:18 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:19:34 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:19:35 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:19:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94153723d1545849cb54e33c3f8f977f110afcb00da0d5d32236b24537c1a4a3`  
		Last Modified: Tue, 02 Jun 2026 21:43:46 GMT  
		Size: 64.8 MB (64840550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4ff149d61b69213dc146324696a7a3af1a2b46684c6f928dfca1ae8489a0e`  
		Last Modified: Tue, 02 Jun 2026 21:44:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3cb06425959c67588985a91f934858685c3d7e6f0a3094af6c96ef93508d2`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 6.9 MB (6906465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966eded362018ac5d0b34cafa47d109cf32bbdeac194c1582640c28fd31f3cb0`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 1.7 MB (1705993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88bcc980b0c8d2d3de3ae12ec5a268bf23ac450cf0e10b8726131fa5f50dd3a`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:636aaf3183699721a688bf9903f4a642af3556d22fb14b8142bb3d77e9e02f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4888dfc41af739498c0157e20326f403f56cd8400b521203907e2cce1bfb8403`

```dockerfile
```

-	Layers:
	-	`sha256:00729d38b67285f7a79eb306240810accdabec647d996c8e36ab458f490a827c`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 280.2 KB (280199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ec6cfbc1bfecb50f2c2e12352351ad7a86aa62458697127bd6d635c92ce4cb`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; riscv64

```console
$ docker pull caddy@sha256:851cb908798b1538ffe3a3053bb98a32903f158a7f1ca9eeafb0fa30f6f34f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77424217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfc4a9d5f64621b356f7b47c6c48337fe32d5912cfc96a0484d5c999eabca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 23:12:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 23:12:42 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
WORKDIR /go
# Wed, 03 Jun 2026 05:24:30 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 05:24:32 GMT
ENV CADDY_VERSION=v2.11.3
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 05:24:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8f135b9aec9b42cabcdbc9e60e1e2b738fe71cb50c44dd091c53fb8edc94a`  
		Last Modified: Tue, 02 Jun 2026 23:19:15 GMT  
		Size: 65.1 MB (65148394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c4848fcf3e91f4413c1666bace4337c4f1c12c50976959bd29ad011c4d936`  
		Last Modified: Tue, 02 Jun 2026 23:22:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc28d768f2c71e4a402e2f4424963bfaa465d9c4a2f36c428bd41b08e3d6d2d`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 6.7 MB (6672809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5d5e4441c4e23a30ad21c2b66c3a336df57c4bfda44ff5113b5b3be8e2ffc`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 1.7 MB (1724208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80fdf8a500696ba07bd03f2a260b2e578f3e7909bec500d7122de9d25041d6`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:dca192295748614e125d445ca613cc0972469b2e1774dca65dd6b47fe9d2682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a911353b6377828995df9827f453d124992e5ff9b7484ef6ebc4da9d7258c820`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc98528c0380ded7049be92a37c9302d44d983dd53bba1648e04dedd55efb4`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 280.2 KB (280195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb92a4e503b3fefa7c0f01279adf8084dd01665b4d68fcef6d623b33d866cb16`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:4b90e008693f441e0c5337ba3fedad55597c1c61e2ecf25f2241f3a878b58d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cee611b412138469260e614e91691e6b1868b70e66aabd6488d8013d7cf3ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:02 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:13:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:13:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95f9225fe123215e56024e7fcaa3f2eb9fb3081c2d6160ebae532ca6d5eefd`  
		Last Modified: Tue, 02 Jun 2026 21:43:22 GMT  
		Size: 66.5 MB (66513822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9138885877e3f590d4144dfc2ec737113acde73b99374df82c5be8c2901f3dd`  
		Last Modified: Tue, 02 Jun 2026 21:43:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91584af5ed277f32349e17cda1214326d518b9f94719dc5c4e741329ee86f375`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 6.8 MB (6779991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30090c473a211354bad44ab67b863187e6614231a73dcf0aa22173ee79b1a359`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 1.8 MB (1782842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3da51a38e8b113b744ea5418d02a52a6b6def3db40a219f602fa5e52065bfb`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:578a971dec1e6528eb9512ec7c3c538b18cbeb2a8d6c72b4f420d6992b30009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f17854159ec165c92bf0e0220d91246d07bd68f48b8fa569c16a68552d0058`

```dockerfile
```

-	Layers:
	-	`sha256:4915df098870636a12ece0bc09cc5fc8dee8954c6116a7cfb93bf9f3169bd426`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 280.1 KB (280125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97af12336dd47a218f778a32b9bf8cf6ecc4d8ef33a28f7bb8c621a730e6343b`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:6bac99d1de9debbb801646208c923809fe18cbb945c6d430cc8f1d38c5ba14ff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335210672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45bc764ed6ce43900c66e7269ef9b64bff9f78aca8a5412c2bdddba4456a779`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 21:46:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 21:47:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 21:47:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 21:47:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 21:47:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 21:48:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:48:54 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 21:49:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 21:49:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:50:55 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:50:57 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:33:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:33:57 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:33:58 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:33:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:34:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:34:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03db002b9e59a168b97269178d3cea6be969a491719ca1c8d3f4c33ad9ad07f7`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b9c42b86ca2e7aa4eb41766a6f755119c65c8b2c03b320ba0980b9d2f6547a`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8f4def2bce82d1e544606aaf3e5895ae29437220f1b41211727fbeff83ac8`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16228e0f3edb3815e34fd2d8c6d575e9ed737e1d5cc07909e430d670860bc7cc`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca5f94c0122485a7417a90a87018bf739ef6ef80f60454b5258cefa6a58eed5`  
		Last Modified: Tue, 02 Jun 2026 21:51:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1397a64df19d921e6ad74f8c6ca0ea5b401c7731318c4dd85002c5dbb6df922c`  
		Last Modified: Tue, 02 Jun 2026 21:51:15 GMT  
		Size: 51.3 MB (51286214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871cad50024619c7f067652dc3cc2e678a8c70180235a578d249123c21479637`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007a76e9414e0db486efb9ff5a4409e15cef9f66f3c19a6efc5d554db55f0e4b`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 367.1 KB (367144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fea8e7d4ba560522bf09b19a63fc47cca6a724baa7e90623086a8d46f1d8f2`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44107094e22c635252ccb6df8685c7968f63f084760fcbec0f4cb08857a74`  
		Last Modified: Tue, 02 Jun 2026 21:51:19 GMT  
		Size: 75.3 MB (75252822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35936631b6cd9bd6e5cf14e0cb4f8a287786047d069c23d09ed69d69e5672e`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfefceaacb32ce75c4aaba58b81bced50aae117cc616944d49a92ce10e866b2`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d897cbe5e09e88bd391baaa18698e2d8eb277aa581a683b8025c4f230f1adf7e`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4b32c912e804ac74f332ad5ab2d2b281dc7e6d481f6f80a4f43df475616659`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f053ec3b21275df3413b9168645d21fb9bb677da4c1d6c12e96049e54cabfcd`  
		Last Modified: Tue, 02 Jun 2026 22:34:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b1f65dcb82cba9c705872f745be1ac11720b8c76eebbe4e9942f2f2e810cf7`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 2.3 MB (2345713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcd5aef19be6456c21bb9609b574709a6500a0642321c9435e2421d39818fd`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:5c6e7364201194ab26b433feaf24cec26dd47fa67d0191fd5aac9a3145f2d75a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2246342426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4817db1df805c59c442b0aae0af3740b59c437f926600e3382586defd6c6bd84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 22:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:11:59 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 22:12:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 22:12:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 22:13:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:13:36 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 22:13:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 22:13:43 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 22:15:53 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:15:55 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:48:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:48:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:48:17 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:48:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:48:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:48:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16556704259948e469d295ad17c0b83303b045ecaedafdd2e16e153313e1dfb6`  
		Last Modified: Tue, 02 Jun 2026 22:16:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d711fc9f348f8b578e18995374d27b40e5900dd346ce6989dbf8a03d6379ed3`  
		Last Modified: Tue, 02 Jun 2026 22:16:04 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591205aec584bc9bf82bf950d86511bf856df5b80cfc692ffebf5597ca68b7e6`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22c20181a321c9aa31806b3a6299f064d89d5be9ef4ec4b8643e9648f096b20`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875bb11e80c093d7133bdc63d9eae1ac2b5c3615c2548955f18ce7dc1cbcdd1`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec55ad5b4586a55352fbd4acd5057d226c2736b7bf5617ba58c7b1ec5a01595`  
		Last Modified: Tue, 02 Jun 2026 22:16:08 GMT  
		Size: 51.4 MB (51351865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8157f646be5f683d250a6f17ff707476c9c8021878b249e269ce011d3ff874db`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363dcd54d5e980b27d8e067e3aa0681d0a3b914f0cd2fee65597fc3cc09fecb3`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 347.5 KB (347472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89e7d73520ffce5ef45fce95d33eb59c6e81aa2a9b702762d10955702c63f88`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03786a5498c3138a7f68d31bb4b48bba38614a87e19b581dfb213237d20256`  
		Last Modified: Tue, 02 Jun 2026 22:16:12 GMT  
		Size: 69.9 MB (69908615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717522dbb34fae4042da878f0e2b02e156afeb7efa63dd68f87a0e670c1777a0`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c100a71c72bd8a3ae733ff302b773d79c1f9d9567e2ea92e5a14cabfad16946`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973c59f163b420ad3e89ff70cbb614dd936a7c672446a4f96680cf7ea2033b1`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23746fb5a19760542ceaf1982c31d671001d1e61c45ef53459e38fe02213c2`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d27ae839dc6cc7d7a119bd9b2c302ae49b265e40e36003baed2d882a8b80f`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415c477003a7c45c620ddf022beae3a2649f87cdd579da1617144d132e961953`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 2.3 MB (2296661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5287c072e6ec74e531802fe71a613d30d89698c4a47bc8e3f1ca00ee98a1249a`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:3eae6b351ecdb05da6d16e341261a457692d344a435764c5ece7a60cf03a23f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:db3ae9a5913d5b9305c729247b8ee6ca7596823a3a9419eaac330e5f374c3157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79773771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591706032a9a5c14da6e7f446e0083d6747768d50d0bf9da36e55c2421e94a2f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:53 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:11:59 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:00 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30edd47abbca5172a1775d1ba8a17aef65500a7a1ecc50af582706ad0c19ab`  
		Last Modified: Tue, 02 Jun 2026 21:45:09 GMT  
		Size: 290.2 KB (290247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaa626ba3010d60ab55d9cdc69c0b12ebff5d1b5ece83ff220fb46a7709b3b`  
		Last Modified: Tue, 02 Jun 2026 21:44:37 GMT  
		Size: 67.3 MB (67283031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abecc8ee46932a01c961a896c3c87dd0efe1301916e124bdac46f96ae6e9dee`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca4922139842e28e1d61aaac141bc8576337fa9b8d64d1d9f723d161fb30612`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 6.5 MB (6489213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fa1420c37ef3c625b9f14ee901574c588fc49b3eb5a8fca1a8a732fd47620b`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 1.8 MB (1846501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e306254cc3a4dab0c2ccd0f548ad566fa5aa81a412b9b432d81889526a2bbf2`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ddd773e864a4f4e091e1f4bfdbd60371b4c51910be5ccb610589b8a6883de8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4dc9d9bcee8d699bb42f311997ea36c642596e4004aa8859d0781b30ac2c9d`

```dockerfile
```

-	Layers:
	-	`sha256:d055d9682529a9387da6c4adbc8bdc265d0466484002fca96e29c90f179091be`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 280.8 KB (280776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490b4b762d29e23f9c30e7d63d2f4fde87253b5f126903cfd336647e4cf6c3af`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67c97e86bbcf6c6d84c8a191e6f9c07550c3ff25bfef23d3e8ee6a6407d6d801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77801132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8375fe7e15b17bead87deaac11514fa70da1cd8427509b1c228967a15f141eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:01 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:15:26 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:15:27 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:15:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dc79104d8e3b9e93b7ff3163839b44dd0979c52b2f81f68e01be8f60d9d090`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 291.0 KB (291036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb989b4b1329f80799d899b8d7259a6658047b39b2b670ed0cc8620dd1d357c`  
		Last Modified: Tue, 02 Jun 2026 21:44:18 GMT  
		Size: 65.8 MB (65785954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e947158a0266891a134507f0a6253aec12f2c7656af2daefbed99f399148f5`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620327b269f4fa8f6e186115a4ab2a342dedb497a9044abd4a5b3246f11d3ac3`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 6.4 MB (6406685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a7c7f37dd2ddabcd39c4ec78c16b8efaf799e1db677a0a88c55ba2bd16132e`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037287d5c994a910febeca5542dc101d590c0256e293e25e7ddb97f4b25eba7b`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ee8a613597922f4a0c6ad805948acd213e018eb8e3548ca5b98e7cb6c0410659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a997af74d3004a92cc163aa5d9f843ecd7552d9fad60e39cc23d5f4340ebdbd1`

```dockerfile
```

-	Layers:
	-	`sha256:b77f8ee7de0cc1af47105376a1a978c3bd700001392879cba9b348c38f53c909`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:081203e78dbbdf584d644a704dbce3dd01e8d923760b1e4160a615e9c0282f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cece6d48bcb1d2e37ff13a3299d3382dd7c3a18c66cd620c334b6e7e45b85c5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:51 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:54 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:48 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa788fec666273423bc95c719209c3f49b0d2c1c28fdaf669e4ebcab932954`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 290.2 KB (290169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f46eeae83dd5d801ff20835cd1ea98f630698b9c066e10ddf320a1c9d42c07`  
		Last Modified: Tue, 02 Jun 2026 21:45:10 GMT  
		Size: 65.8 MB (65786124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494a0eb08b28e7075149245f5ff666eeadec03e6b1b08870ad1caa24151d00b`  
		Last Modified: Tue, 02 Jun 2026 21:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba6d2d27897ace71b8214e93839ab4dddfb4bf51e5dd9871755073b452fd92`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 5.9 MB (5859405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d200f1ff9040ab5ed074d40e2c5d715e5ca869a8c3c9ca357f24b30cc08f2`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 1.7 MB (1738762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392245d1b10f490bef242becdaf6b658edb173425508af51312e2d0c7703b3c5`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0207715e319528107b0ca90c4b3ae044a8636067b8544656cf7cfa660dbd93d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd6848c1a5afb6c01dd7ed0eea80f86a4053eb96a8d94f50bbb86131989d4a`

```dockerfile
```

-	Layers:
	-	`sha256:dda72704ff023245a1d0202ebcabc8675ff1d722be6ba03fec1b7ce479c3a68c`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 283.2 KB (283168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac1a6806382a02068a2684ad9fc775685c890f3913b65b2de640fe3eca324e6`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:13da9d8308a65d8402c19528f51e19a2535fcd2f28ee893feabfefab09afb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76951883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114e448de61888adef08f63408e9426eb63ce6db5c2c1066219d9ba0222717c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2c0198c180cf41cbfd73e25946fc0ccc373d0fee89deb6e7eeec7b1f8612ee`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 292.9 KB (292861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477eaf154b7c8070862d9db01681f78c8a60ce90e8936310f6a906696df475a`  
		Last Modified: Tue, 02 Jun 2026 21:43:59 GMT  
		Size: 64.2 MB (64166971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb4739b26b76346d1281fb8fac14c5bc8025bfc580405cc95aa21736e41116`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e7c04c5116e56a4edea922d39e62c3fe0cfb06ee580b89926af1db83402ce`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 6.6 MB (6575206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57c7a67944f4fa914947979e30a6c1db54ab3c9b1aac79a9ebd7b36e8e39b0`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 1.7 MB (1716384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ee51343f308260ed7fa9020154c216542e21fd2589bc41d85b57f77166a81`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ce914fd434a8d09e7d2f73c5c9b354b42cf9c31d65fefbe292f23eacb6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 KB (300526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbed50fbf772e7e0ff9b816eb3a8dc3e213df0f8c75ba10dc5924412b0e4d841`

```dockerfile
```

-	Layers:
	-	`sha256:add9c054a1ac3653aed38da164cb08126bb46bb4bc153c6f12848191bed15b4b`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 280.2 KB (280230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838bb928d6772b6ebe8d87d60a85b358fd40eb2166c93cb622cee8a22a537ca3`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:658d12b9b7e489cdf05a0115f8fd9c8e392ee3160ba5b96d5f6b1e3cf0e02802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2568f1df66f499486924dad3ad55e9449d549bbb37426e3354addf15c6c7df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:42:40 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:18 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:19:34 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:19:35 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:19:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94153723d1545849cb54e33c3f8f977f110afcb00da0d5d32236b24537c1a4a3`  
		Last Modified: Tue, 02 Jun 2026 21:43:46 GMT  
		Size: 64.8 MB (64840550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4ff149d61b69213dc146324696a7a3af1a2b46684c6f928dfca1ae8489a0e`  
		Last Modified: Tue, 02 Jun 2026 21:44:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3cb06425959c67588985a91f934858685c3d7e6f0a3094af6c96ef93508d2`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 6.9 MB (6906465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966eded362018ac5d0b34cafa47d109cf32bbdeac194c1582640c28fd31f3cb0`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 1.7 MB (1705993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88bcc980b0c8d2d3de3ae12ec5a268bf23ac450cf0e10b8726131fa5f50dd3a`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:636aaf3183699721a688bf9903f4a642af3556d22fb14b8142bb3d77e9e02f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4888dfc41af739498c0157e20326f403f56cd8400b521203907e2cce1bfb8403`

```dockerfile
```

-	Layers:
	-	`sha256:00729d38b67285f7a79eb306240810accdabec647d996c8e36ab458f490a827c`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 280.2 KB (280199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ec6cfbc1bfecb50f2c2e12352351ad7a86aa62458697127bd6d635c92ce4cb`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:851cb908798b1538ffe3a3053bb98a32903f158a7f1ca9eeafb0fa30f6f34f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77424217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfc4a9d5f64621b356f7b47c6c48337fe32d5912cfc96a0484d5c999eabca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 23:12:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 23:12:42 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
WORKDIR /go
# Wed, 03 Jun 2026 05:24:30 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 05:24:32 GMT
ENV CADDY_VERSION=v2.11.3
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 05:24:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8f135b9aec9b42cabcdbc9e60e1e2b738fe71cb50c44dd091c53fb8edc94a`  
		Last Modified: Tue, 02 Jun 2026 23:19:15 GMT  
		Size: 65.1 MB (65148394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c4848fcf3e91f4413c1666bace4337c4f1c12c50976959bd29ad011c4d936`  
		Last Modified: Tue, 02 Jun 2026 23:22:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc28d768f2c71e4a402e2f4424963bfaa465d9c4a2f36c428bd41b08e3d6d2d`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 6.7 MB (6672809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5d5e4441c4e23a30ad21c2b66c3a336df57c4bfda44ff5113b5b3be8e2ffc`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 1.7 MB (1724208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80fdf8a500696ba07bd03f2a260b2e578f3e7909bec500d7122de9d25041d6`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:dca192295748614e125d445ca613cc0972469b2e1774dca65dd6b47fe9d2682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a911353b6377828995df9827f453d124992e5ff9b7484ef6ebc4da9d7258c820`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc98528c0380ded7049be92a37c9302d44d983dd53bba1648e04dedd55efb4`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 280.2 KB (280195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb92a4e503b3fefa7c0f01279adf8084dd01665b4d68fcef6d623b33d866cb16`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4b90e008693f441e0c5337ba3fedad55597c1c61e2ecf25f2241f3a878b58d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cee611b412138469260e614e91691e6b1868b70e66aabd6488d8013d7cf3ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:02 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:13:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:13:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95f9225fe123215e56024e7fcaa3f2eb9fb3081c2d6160ebae532ca6d5eefd`  
		Last Modified: Tue, 02 Jun 2026 21:43:22 GMT  
		Size: 66.5 MB (66513822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9138885877e3f590d4144dfc2ec737113acde73b99374df82c5be8c2901f3dd`  
		Last Modified: Tue, 02 Jun 2026 21:43:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91584af5ed277f32349e17cda1214326d518b9f94719dc5c4e741329ee86f375`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 6.8 MB (6779991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30090c473a211354bad44ab67b863187e6614231a73dcf0aa22173ee79b1a359`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 1.8 MB (1782842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3da51a38e8b113b744ea5418d02a52a6b6def3db40a219f602fa5e52065bfb`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:578a971dec1e6528eb9512ec7c3c538b18cbeb2a8d6c72b4f420d6992b30009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f17854159ec165c92bf0e0220d91246d07bd68f48b8fa569c16a68552d0058`

```dockerfile
```

-	Layers:
	-	`sha256:4915df098870636a12ece0bc09cc5fc8dee8954c6116a7cfb93bf9f3169bd426`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 280.1 KB (280125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97af12336dd47a218f778a32b9bf8cf6ecc4d8ef33a28f7bb8c621a730e6343b`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:2507e19ef745b79bb6d80853a1f496cf6ccc33b2952dd338d29574b3a40b7817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:5c6e7364201194ab26b433feaf24cec26dd47fa67d0191fd5aac9a3145f2d75a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2246342426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4817db1df805c59c442b0aae0af3740b59c437f926600e3382586defd6c6bd84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 22:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:11:59 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 22:12:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 22:12:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 22:13:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:13:36 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 22:13:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 22:13:43 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 22:15:53 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:15:55 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:48:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:48:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:48:17 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:48:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:48:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:48:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16556704259948e469d295ad17c0b83303b045ecaedafdd2e16e153313e1dfb6`  
		Last Modified: Tue, 02 Jun 2026 22:16:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d711fc9f348f8b578e18995374d27b40e5900dd346ce6989dbf8a03d6379ed3`  
		Last Modified: Tue, 02 Jun 2026 22:16:04 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591205aec584bc9bf82bf950d86511bf856df5b80cfc692ffebf5597ca68b7e6`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22c20181a321c9aa31806b3a6299f064d89d5be9ef4ec4b8643e9648f096b20`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875bb11e80c093d7133bdc63d9eae1ac2b5c3615c2548955f18ce7dc1cbcdd1`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec55ad5b4586a55352fbd4acd5057d226c2736b7bf5617ba58c7b1ec5a01595`  
		Last Modified: Tue, 02 Jun 2026 22:16:08 GMT  
		Size: 51.4 MB (51351865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8157f646be5f683d250a6f17ff707476c9c8021878b249e269ce011d3ff874db`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363dcd54d5e980b27d8e067e3aa0681d0a3b914f0cd2fee65597fc3cc09fecb3`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 347.5 KB (347472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89e7d73520ffce5ef45fce95d33eb59c6e81aa2a9b702762d10955702c63f88`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03786a5498c3138a7f68d31bb4b48bba38614a87e19b581dfb213237d20256`  
		Last Modified: Tue, 02 Jun 2026 22:16:12 GMT  
		Size: 69.9 MB (69908615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717522dbb34fae4042da878f0e2b02e156afeb7efa63dd68f87a0e670c1777a0`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c100a71c72bd8a3ae733ff302b773d79c1f9d9567e2ea92e5a14cabfad16946`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973c59f163b420ad3e89ff70cbb614dd936a7c672446a4f96680cf7ea2033b1`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23746fb5a19760542ceaf1982c31d671001d1e61c45ef53459e38fe02213c2`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d27ae839dc6cc7d7a119bd9b2c302ae49b265e40e36003baed2d882a8b80f`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415c477003a7c45c620ddf022beae3a2649f87cdd579da1617144d132e961953`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 2.3 MB (2296661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5287c072e6ec74e531802fe71a613d30d89698c4a47bc8e3f1ca00ee98a1249a`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:688be35a61ebeccf90e1956f0225b3db0280e79964863fe7b93addc0864838fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:6bac99d1de9debbb801646208c923809fe18cbb945c6d430cc8f1d38c5ba14ff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335210672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45bc764ed6ce43900c66e7269ef9b64bff9f78aca8a5412c2bdddba4456a779`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 21:46:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 21:47:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 21:47:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 21:47:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 21:47:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 21:48:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:48:54 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 21:49:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 21:49:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:50:55 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:50:57 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:33:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:33:57 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:33:58 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:33:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:34:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:34:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03db002b9e59a168b97269178d3cea6be969a491719ca1c8d3f4c33ad9ad07f7`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b9c42b86ca2e7aa4eb41766a6f755119c65c8b2c03b320ba0980b9d2f6547a`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8f4def2bce82d1e544606aaf3e5895ae29437220f1b41211727fbeff83ac8`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16228e0f3edb3815e34fd2d8c6d575e9ed737e1d5cc07909e430d670860bc7cc`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca5f94c0122485a7417a90a87018bf739ef6ef80f60454b5258cefa6a58eed5`  
		Last Modified: Tue, 02 Jun 2026 21:51:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1397a64df19d921e6ad74f8c6ca0ea5b401c7731318c4dd85002c5dbb6df922c`  
		Last Modified: Tue, 02 Jun 2026 21:51:15 GMT  
		Size: 51.3 MB (51286214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871cad50024619c7f067652dc3cc2e678a8c70180235a578d249123c21479637`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007a76e9414e0db486efb9ff5a4409e15cef9f66f3c19a6efc5d554db55f0e4b`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 367.1 KB (367144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fea8e7d4ba560522bf09b19a63fc47cca6a724baa7e90623086a8d46f1d8f2`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44107094e22c635252ccb6df8685c7968f63f084760fcbec0f4cb08857a74`  
		Last Modified: Tue, 02 Jun 2026 21:51:19 GMT  
		Size: 75.3 MB (75252822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35936631b6cd9bd6e5cf14e0cb4f8a287786047d069c23d09ed69d69e5672e`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfefceaacb32ce75c4aaba58b81bced50aae117cc616944d49a92ce10e866b2`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d897cbe5e09e88bd391baaa18698e2d8eb277aa581a683b8025c4f230f1adf7e`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4b32c912e804ac74f332ad5ab2d2b281dc7e6d481f6f80a4f43df475616659`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f053ec3b21275df3413b9168645d21fb9bb677da4c1d6c12e96049e54cabfcd`  
		Last Modified: Tue, 02 Jun 2026 22:34:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b1f65dcb82cba9c705872f745be1ac11720b8c76eebbe4e9942f2f2e810cf7`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 2.3 MB (2345713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcd5aef19be6456c21bb9609b574709a6500a0642321c9435e2421d39818fd`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:ec18ee54aab3315c22e25f3b2babda73ff8007d39b13b3bd1bfffa2f0444c7d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:3739ea4f0c877259a693d932693cf8f3408e9a9497c004f031b0e830e93e1546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23985030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5190456911cee510988a5fb9996188ef866fbcca3235cad19bf05f5f8f33386f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:12 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:14 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920de1d55d9880b00fbeaf8fa3757e89f7ea6170ff12633cbe766c2152a858d`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 2.9 MB (2886638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057c497bda068e80884e6836fbf8971a954593242af7694d080e6b81758b67f4`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b55c68e4a0feeeaec6f86ced6bd8790e19ed68399cff61bab00adc15895ec13`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 17.2 MB (17226669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:e08c659e9fe301aa2814b2cafc4a5211423fcaa307a515772efeb816684ceb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 KB (351377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cd52ea603ed29abf30a13e9ab37f92acffb93b53042a6bfaf1d22d9bdb8be`

```dockerfile
```

-	Layers:
	-	`sha256:4c4f094b32e82a0c66e0e5c00015a86d670049e4e9a336febc6c2a2fd626b19b`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 332.9 KB (332947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16285c7326d137b74e90d1f477040eb15643c312e7a46770316c0c258033326a`  
		Last Modified: Tue, 12 May 2026 21:45:20 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:018595a3226de0d5c9055279af90983e9e91ca5f12dde17e93925455d19bc0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ce61ba53a04521d0e684e8048cde82ebd35cd3d72a9d1f7616056976e75253`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:40:51 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:40:52 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:40:54 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:40:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:40:54 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:40:54 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:40:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b1247b4f1cad33af22f46d45d07b1ee65401981dccc3fa920dafbde1fb072`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 2.8 MB (2819583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d84aa44715b44ce12b2cc9b98a20167ca060c5869ab67124210f554413d56ee`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93038fb49fb9d7664bc1a8209857cde656b4e5ff6ab5a7bf4b270d942f499d0`  
		Last Modified: Tue, 12 May 2026 21:41:00 GMT  
		Size: 16.3 MB (16311628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:de7fac8a337ded6fa61288d6dcc5837d472ed26f9d6b7230f0c8487fb9db984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feea7dba17177c5d72e8d8b883cd3bcdcda396dcc918c1e1e6d3868632932251`

```dockerfile
```

-	Layers:
	-	`sha256:2bd47793d94047373cab54d4b18f46ce16d19438827a8a41e3c5960cd1da48ca`  
		Last Modified: Tue, 12 May 2026 21:40:59 GMT  
		Size: 18.4 KB (18353 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:2c3d3047a1705945ca9376ef8d3e9eb431f0f07f16e6ae2511326d7f0b664ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22262035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a70cfe7deb0544e9098ef10e20ebbc18e346bb3b8df5b140b9f184e71b4a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:42:08 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:42:09 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:42:10 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:42:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:42:10 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:42:10 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:42:10 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce55fb7d543ef0a1f852326909b7cdb22fb514199bd31b9543d92f04e878f4`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 2.7 MB (2681516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49caf58b5069e136a5fcd2fbaa18da4c786566963ba48bcedc27100b8a43365b`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ba28a73ebab4ca57472bca296d741e3d9b1cb27478c6adde87b7c314ba7810`  
		Last Modified: Tue, 12 May 2026 21:42:18 GMT  
		Size: 16.3 MB (16289861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:08ab34ff2df00fe711e074db26cf28e9b5ff1dbfe8355e0f414ed9a7c465cfae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb11059736745812fc6bfa910b2d1cce68b03317d8452425d1f7954f2023f495`

```dockerfile
```

-	Layers:
	-	`sha256:95b578e25712b12ba424efc0abb0e6a4daa0cb6d145f200869796d863a0535dd`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 332.4 KB (332365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876e5685474ad9dfce16688d11127988be62753bb83e66c138c382a181530636`  
		Last Modified: Tue, 12 May 2026 21:42:17 GMT  
		Size: 18.6 KB (18568 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:780ae38d5cc9674696bfec2dd7a20ea5495a2653d788ee39bff6aaf1007f8dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22800642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de64000d357283f8b74cfc9cabce60768a6957447b74a7eb73c573c5d344a398`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:44:57 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:44:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:44:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:44:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:44:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:00 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6cabef06141e7f3aba6fa7d3898c4282f7316acb2ad612b8ea82ac9172cd99`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 2.9 MB (2900862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69f6bd08e27b5a1e9b73c99efae612626fabe895c78a156e402e5938112fff9`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 7.5 KB (7500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4e100b255f5c935bb23c7e5f2a23ee2b5b683a152149ad5db9b32d8455edf`  
		Last Modified: Tue, 12 May 2026 21:45:07 GMT  
		Size: 15.7 MB (15692378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:99d5c41f924f43a16554137091afc6dc8c34e2976b4011ea8793c6211676f8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 KB (351013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f8ace5e5ed9603a8a26766f5df8fd3efe32a76bb3d66c4017bf8bb842691c`

```dockerfile
```

-	Layers:
	-	`sha256:43c50900a0619c09f3987cc62bbfffd4d10da1b9d81fd21f3605e47dbb741967`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 332.4 KB (332401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e57f91d95d6c31886fc5dc74e74b86782c292b27bf964bb5023e301c36f8270`  
		Last Modified: Tue, 12 May 2026 21:45:06 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:d6f3adf638edd88132caec6005766ec86f31796069549755af52d172a03ebd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22551245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d82ac569eea06185f6688d103c7d7e2ef313dce067d6f1aca3b7255025aa450`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:45:46 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:45:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:45:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:45:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:45:51 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:45:52 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:45:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aba3acae7a944d3cb59ff0085839ecf6bc67e67a1ff5c9d62453ec36405516d`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 3.0 MB (3024677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef81e00b6b88436c8856bd7f6a2a40abea36897a22c7707cdf06722a09f8b819`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d1e87608e2891184dfb2f547b0a2062b1bba1b787d3cd95ff36446affe940e`  
		Last Modified: Tue, 12 May 2026 21:46:12 GMT  
		Size: 15.7 MB (15688108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:863e023f3571814b385c37ac309e71a9a712f4aea420d2cea5032e2a362bf7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef881e7b8f82faab6a4473932499599574eb0bc9d0264c779647d0b099584f`

```dockerfile
```

-	Layers:
	-	`sha256:aa780bcad124738bdb6864e89c3299ebdcee766cde92da7db3f2ca1d99c22f23`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 332.4 KB (332354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cabca92420dc637383da8dc8f0d0276fcf258532404ff1d3fb1e80473359b1`  
		Last Modified: Tue, 12 May 2026 21:46:11 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; riscv64

```console
$ docker pull caddy@sha256:69328a1677b50e71a30c554ca8dddf7f1ad2474084385dabd7a0d6fedc9a4118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22851653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086f5adaba5ab0d6ae67e9e685607028248302272c9befb82e9fba4246d6537e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 02:12:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Thu, 14 May 2026 02:12:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV CADDY_VERSION=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 14 May 2026 02:12:27 GMT
ENV XDG_DATA_HOME=/data
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 May 2026 02:12:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[443/udp:{}]
# Thu, 14 May 2026 02:12:27 GMT
EXPOSE map[2019/tcp:{}]
# Thu, 14 May 2026 02:12:27 GMT
WORKDIR /srv
# Thu, 14 May 2026 02:12:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a638da60daf650b51909ed97e65ca82d6b4c622d9aad9e05a1fe86e41b1b8`  
		Last Modified: Thu, 14 May 2026 02:13:15 GMT  
		Size: 3.0 MB (3024903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e9ab663ff84756b43ea4456b9675a7bb4e9a21db93cfb2860477f1acc49fa3`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 7.5 KB (7506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207dafa63c1803835db9d283a462accf88a7d65b6c6a62ef6d00c05e7e2d4d85`  
		Last Modified: Thu, 14 May 2026 02:13:17 GMT  
		Size: 16.2 MB (16231550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:2a37fc42537c780173072b08a797af48db02d1ca4bb14afe8301f380deb5f108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1087260f2ba70b75cfc134c58bb57369b570c4c836ad26b8a6774cfb2c421a26`

```dockerfile
```

-	Layers:
	-	`sha256:50741c878fc4519cf8be95491297cbbf12889e7fe8fe4cb6f0cb7a32aacd5a4d`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 332.4 KB (332350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074f80835103901f06cabe60ac917a34ae1a55cf6637768028867d83f6f31640`  
		Last Modified: Thu, 14 May 2026 02:13:14 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:2be760d0b6dcefcee4d8e8de79e4fbc5bff379cc71f6ba4be329b95fee14ed53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23338359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bb7983fab4c669751406633c3cd0bacc33744d3c43dcecd96b365041e7d3b5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 21:39:41 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 12 May 2026 21:39:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ee886eceda0ff9f30610d3be9b5b594026591e19add6b3961a341c72abe468e5eac9d7c2c2450bbb8420db1f827b954521f9336be4872f81090b8618adf8815a' ;; 		armhf)   binArch='armv6'; checksum='84b3baef4f1850a8a75ab38f1da8c08eea5a19a9081ecb62af2658e7c9919203ef1907233e8b27b4dc4ddd6f0a8f57893d10190c611f15e2325ea9962f2073d5' ;; 		armv7)   binArch='armv7'; checksum='7ae0bcf5a1060ac0bcb0c9d454f21f70b2655c2e883a3a1617069d12193eae650e4410807cc50e216b01775cb0e0c16ab84490a03454153d189cfe5775cf775c' ;; 		aarch64) binArch='arm64'; checksum='bd06996e1612cf5e9770dc7134313067ef3fdfde43b1a2196004906006de779372dcf7a0e7c7fb0890c23791179f12be4625f1b6e666a2abf37e8aff4c3a1826' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e1f33af0869f8234fc28575ee6eef04f7dfd0b3a6255be6efdc3aa3d05d05db833c4571e90287908eae93da1383e07e93ed9c6ad0199ccc0f1fe798cb88f43ce' ;; 		riscv64) binArch='riscv64'; checksum='9b0f3f8ab8816d57878f251e7913d7622340dff9092770397db740ca5e9930b5718c67231c97ef6cd3ba886de57060fc01ca1ab018d9cac1d0878092312fd280' ;; 		s390x)   binArch='s390x'; checksum='eb71dfa44b5ed5db32af566b6fa2e3f711df828b847c55f250ff8cfd9af22ab79048f3bc8d9756ac06683c54d46ba2e11c6b109fdda16c6a28c29a88f327d9e1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 12 May 2026 21:39:43 GMT
ENV XDG_DATA_HOME=/data
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 21:39:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[443/udp:{}]
# Tue, 12 May 2026 21:39:43 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 12 May 2026 21:39:43 GMT
WORKDIR /srv
# Tue, 12 May 2026 21:39:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cb0bfcc1c8a81033ff4911e9096b260f4711f66484b04586fd6fa5ca95e44f`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 3.0 MB (3010703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bd7ba8a52c9fc9419b92337580db55dcd8690a637184fb22bec4871ffb8c0`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798a8d976afd31ca55ef92d83a93374f6c3e7ccd3add31769d768349700d623`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 16.6 MB (16593589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:4a728924f65d2a9612ff66fbadd33d9a2d6e6b198cfc95cd6b23b89948cc2a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 KB (350726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43f0c042f1bc3d80c67c0b0ad7df18ed102df0765f312c2619bed3d8392597`

```dockerfile
```

-	Layers:
	-	`sha256:4b3e6e6b8593dd35d4f0b59b89b012680c12c5498a7b01ae16bcb7ed34ac49a8`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 332.3 KB (332296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3864730b4cf584aa87e923de4848636482e8621df04a87733e10e42cc44e9b3`  
		Last Modified: Tue, 12 May 2026 21:39:54 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:672b320378b1e89dde74d15a8a123068d26dafce6901597f4f8a837c5c38e7b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141244276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a5337ff6c38ebefe95a0943a39f42bab87a62f05d840422d53a0be69b65f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:59:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:59:25 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:59:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:59:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:59:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:59:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:59:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 80
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 443
# Tue, 12 May 2026 23:59:42 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:59:43 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:59:48 GMT
RUN caddy version
# Tue, 12 May 2026 23:59:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be1f105178ea258d105ecbaf5ec1f6000c5b289826e3b432c22080c650f719`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 524.5 KB (524474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7902ee53436295b9cb02bfa64ac6aa3b314c1e926ec77f7bb59eea811e28a846`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170554e1bf42badb647bc34b5718a5915fede948183bf5dc3d0d21e5540a0b67`  
		Last Modified: Wed, 13 May 2026 00:00:00 GMT  
		Size: 17.9 MB (17925247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a6d017c1aab65f96bd924d664427c093dba8210995905eaf00df2fbd142cb`  
		Last Modified: Tue, 12 May 2026 23:59:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04fc399abb90e3e2df99498e2eb88e7afd2a3f97e84400a40b7439ea46f1fa5`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d26c10fbf4dafe70c44037417bb3457e50a549f998a6f8b4799cf456c446e2`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295c37ba01761384092ce6a3f611a8792a57e0f772e6d8e3bfb099f51932a73`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb5b45ec93d301f781dc64b899fdfaa452f3d35dbbe0ba52fc5c87b02593d0`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0f84b59aead90c71aa95cd5340904935ff3da90339fa6ff21049d0f56f9ec`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1aeb5b58eaf433feb7668159802420e22345953cd345a111f5ff264e659bdf`  
		Last Modified: Tue, 12 May 2026 23:59:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03412a72c6ae737ad61b888338ad28fdc2b3477281195707e27619683236208`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a705083dc71361abc6a1e82aa158830dc6f3dd6e486a403f011f357eae4d884`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5637de44873a5862f646124e27d0fe311506c6fa1eec39c15df5312e1d41881`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4356db0d34adcecf1c9218951422411d7f942cb4d50621800af19388fdcc0`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a670d1e50cdca965f8cebdbf95f43d51e7fe8d7daf65312384a5731f3f743e`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc67002143e99034340b46a68c760d90626fe51d4e087bca7be0aa904ec8b45`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c8eddb6ea788613d96893c8e7c570d4a29a2b07f6d1ce823bf72faa05cf7b`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c21c96cd26011f147afe2c8c693897e2a126fbba132af7fc830d2d7559f19`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 351.6 KB (351565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c0ee074e227c1b13e1438189cfa031217727fc8085182b53234397774d341`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:nanoserver`

```console
$ docker pull caddy@sha256:99fae4af425b9fcc81d4b2efd241cbe3dcac78350f37c4ed2daa6c35df2793df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:3e5afaeda3465c585afea0828ec650f60e760f92ab1096cbdd12bbb7044f93f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217870731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4c6463b2201d0e16cdf07c19f7038d51083193293932e21b857521bf02bab9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:30:16 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:30:18 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:30:22 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:30:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:30:33 GMT
RUN caddy version
# Wed, 13 May 2026 00:30:33 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1fedb6255043325f0c6a8118656684fcc0c1eb9b84857ff574105bdd45da85`  
		Last Modified: Wed, 13 May 2026 00:30:44 GMT  
		Size: 71.9 KB (71893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde99a62b5456da395a4f921712e08ec242d9c53791f22763e904483b90bb0ff`  
		Last Modified: Wed, 13 May 2026 00:30:46 GMT  
		Size: 17.5 MB (17549616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfaf73426fda2a4ab3e9ef51a62f30bf03cd7bb09987eaed20cca2f4baf6c72`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 271.7 KB (271708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee506f35cf26ab6a4307a617c899a31108d35a38976dcbace37f776be3fa88b9`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 111.9 KB (111876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae64a8691f6412e9e7b124cb1506d63cbc0888dfda70af2a058cd92483d1bf3`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e08e3975dc80abab1d7078a935b8310dfd0436900117ac019cf7e74e96327`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa53d7a29128e22ba5071bc2c061d21df2672618f2d335495eee03b57b30eec9`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9aa3dda4800660b0c498edee92d63a95f3487dea910ee7b1e32237e7d8c01`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602df0b26626bd70f3e3b7e338c29f3774aadcb1993b32e11424961d5818b71`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c12f0b0a957349df9e5cdec68e05f8555034292db7712c2189c98bd96a1e`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573942fa9e85b5ae2a2dd8eebbfe68a15cbc4562d77ed7b34b827ddf38d67873`  
		Last Modified: Wed, 13 May 2026 00:30:40 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6577aceea038d31c6741058ac70f3042052944add747d78e1e98f4768056ad9`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f767fdb48bc45cf9dfc7586e7f3bb6923b4260220f4751867e56819d9198c6f7`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805ccff5e068c1b1ef4ee49960a7779be478d8aac505863b20d6779b21c86cbc`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a088d5cf08a67d2b16495569498bf84dc519c98894eef90450facae9b2b1fd0`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a013ec9aa226e3c490885f2df243f133e073c70c9f7fe42acf1c7c6d646c4`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c59e03f4cda98b2b89df28ea3599e7ce642f3438c9607747e027edae7d633`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df98da5df2a594f3eaf8a18d588dd2dd717a8b9d65120307073b5097a7461ab1`  
		Last Modified: Wed, 13 May 2026 00:30:38 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738c190dc62e002473b0f2e0a6b4d56acd58d4befffd3a5254489344e3f514ad`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 110.6 KB (110619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d153bfc2eaf47e5d03b6d7723d1c90e94fbc34f9bd5394c155057ec6cb0fc42e`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:f2b8fdc30136d5694f4d937911af2a98122816cd9382f30f5e188034eb925ee8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145172029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a188f7374e0862b018d9c6a58ee464b17ed26b607a136f3c2f81f6ba750a8d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:33:03 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:33:04 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:33:08 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:33:11 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:33:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:33:21 GMT
RUN caddy version
# Wed, 13 May 2026 00:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471afcd67b75eae029a73dd0dd5c78c7a867343259b55e8a2ce811a682e0cecc`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 75.7 KB (75727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82a36e1bbf75e8321fe17d1997dc9a3fb4d0322fec9092d1c1da3f90b2872be`  
		Last Modified: Wed, 13 May 2026 00:33:34 GMT  
		Size: 17.5 MB (17549625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1c8055df56386428b23be9cc63963727ee8c65d8ccffd1cccb3768eb2e2233`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 271.9 KB (271937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802218197b7b44f15d0c35e1f92bcebeab5b5348fef8370532d04f6e9eae967`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 109.6 KB (109634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1878ea730f12e1f174b5f94eae4c28852ba7d131ff79831bb232b1d3bd2a9195`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5dcf5eafb5625f15b6c8221a6e8033e90b2e194cf46387f7384e9b4a9fbd3c`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4835c93d3898ae70cc7ac56c9260fd82bf21232d466b88b0c18317f927fad95`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e837a3b4c7f62a51617a0817e87c40d393639d84181cce582cdecd0ed04f6b49`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4bdc974f597917738eb16a57d09d2eb7d4932fb411b582d7397d1e49d850ee`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa60544a60e2a9391135d903f2cf2e1104b968bf0cb17d7fdc7896f5e8a41d7`  
		Last Modified: Wed, 13 May 2026 00:33:29 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f676e12689f61e65afafa2dbabe0f87066ea23a433b6bab30a252984ea3bfcce`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c8bcb78837d9611d2e6d737f1983724070a8b8dc651967aa131aaf3b53db2`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fd9964db11cc46a832c192535f0da8d40411e0e4b90d4735a417e2b21e546`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b24ac8b6e8779c0ea8641c14aa97c30b88dfb2dccfef053e31a383bf8772a0`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14623bf8cac2234d2402f1b77f9f8b9ad17f42b63c25eac6a03a874f2b96603`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf92d85a26150eb8504b9bffa3855decbd94a1cc1614f643dccb2a544ed2818`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6be3b806219581d0384bebe4e25fde1cc050ad9ea5def7c549bbfc37fdec69`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183f69d2299c1c4178f5941ded18872ae1a092d5822f9b2470a9bff9febadfc3`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4db159e8ff27f5e761dfc5a73a64fc1bdeeec4bb736d0de7ccdb6479e4d49d`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 110.4 KB (110391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec19313137639151ccfb4e3125b9f946f903e0153e167a6df587f323d036934e`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:5d09312d850c343bf10c4b5d1f831d63fd9e62aaba2eb17ab04136849c9b7731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:f2b8fdc30136d5694f4d937911af2a98122816cd9382f30f5e188034eb925ee8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145172029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a188f7374e0862b018d9c6a58ee464b17ed26b607a136f3c2f81f6ba750a8d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:33:03 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:33:04 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:33:08 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:33:11 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:33:12 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:33:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:33:14 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:33:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:33:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:33:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:33:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:33:21 GMT
RUN caddy version
# Wed, 13 May 2026 00:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471afcd67b75eae029a73dd0dd5c78c7a867343259b55e8a2ce811a682e0cecc`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 75.7 KB (75727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82a36e1bbf75e8321fe17d1997dc9a3fb4d0322fec9092d1c1da3f90b2872be`  
		Last Modified: Wed, 13 May 2026 00:33:34 GMT  
		Size: 17.5 MB (17549625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1c8055df56386428b23be9cc63963727ee8c65d8ccffd1cccb3768eb2e2233`  
		Last Modified: Wed, 13 May 2026 00:33:32 GMT  
		Size: 271.9 KB (271937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802218197b7b44f15d0c35e1f92bcebeab5b5348fef8370532d04f6e9eae967`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 109.6 KB (109634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1878ea730f12e1f174b5f94eae4c28852ba7d131ff79831bb232b1d3bd2a9195`  
		Last Modified: Wed, 13 May 2026 00:33:31 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5dcf5eafb5625f15b6c8221a6e8033e90b2e194cf46387f7384e9b4a9fbd3c`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4835c93d3898ae70cc7ac56c9260fd82bf21232d466b88b0c18317f927fad95`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e837a3b4c7f62a51617a0817e87c40d393639d84181cce582cdecd0ed04f6b49`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4bdc974f597917738eb16a57d09d2eb7d4932fb411b582d7397d1e49d850ee`  
		Last Modified: Wed, 13 May 2026 00:33:30 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa60544a60e2a9391135d903f2cf2e1104b968bf0cb17d7fdc7896f5e8a41d7`  
		Last Modified: Wed, 13 May 2026 00:33:29 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f676e12689f61e65afafa2dbabe0f87066ea23a433b6bab30a252984ea3bfcce`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c8bcb78837d9611d2e6d737f1983724070a8b8dc651967aa131aaf3b53db2`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3fd9964db11cc46a832c192535f0da8d40411e0e4b90d4735a417e2b21e546`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b24ac8b6e8779c0ea8641c14aa97c30b88dfb2dccfef053e31a383bf8772a0`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14623bf8cac2234d2402f1b77f9f8b9ad17f42b63c25eac6a03a874f2b96603`  
		Last Modified: Wed, 13 May 2026 00:33:28 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf92d85a26150eb8504b9bffa3855decbd94a1cc1614f643dccb2a544ed2818`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6be3b806219581d0384bebe4e25fde1cc050ad9ea5def7c549bbfc37fdec69`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183f69d2299c1c4178f5941ded18872ae1a092d5822f9b2470a9bff9febadfc3`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4db159e8ff27f5e761dfc5a73a64fc1bdeeec4bb736d0de7ccdb6479e4d49d`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 110.4 KB (110391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec19313137639151ccfb4e3125b9f946f903e0153e167a6df587f323d036934e`  
		Last Modified: Wed, 13 May 2026 00:33:26 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:0cd979a2fb38e0ef8a3f7e405a19569c9930e820125c1d08720b752d6ba78e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:3e5afaeda3465c585afea0828ec650f60e760f92ab1096cbdd12bbb7044f93f2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217870731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4c6463b2201d0e16cdf07c19f7038d51083193293932e21b857521bf02bab9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:30:16 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 13 May 2026 00:30:18 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Wed, 13 May 2026 00:30:22 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2026 00:30:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Wed, 13 May 2026 00:30:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2026 00:30:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2026 00:30:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2026 00:30:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 13 May 2026 00:30:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 13 May 2026 00:30:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 13 May 2026 00:30:33 GMT
RUN caddy version
# Wed, 13 May 2026 00:30:33 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1fedb6255043325f0c6a8118656684fcc0c1eb9b84857ff574105bdd45da85`  
		Last Modified: Wed, 13 May 2026 00:30:44 GMT  
		Size: 71.9 KB (71893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde99a62b5456da395a4f921712e08ec242d9c53791f22763e904483b90bb0ff`  
		Last Modified: Wed, 13 May 2026 00:30:46 GMT  
		Size: 17.5 MB (17549616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfaf73426fda2a4ab3e9ef51a62f30bf03cd7bb09987eaed20cca2f4baf6c72`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 271.7 KB (271708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee506f35cf26ab6a4307a617c899a31108d35a38976dcbace37f776be3fa88b9`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 111.9 KB (111876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae64a8691f6412e9e7b124cb1506d63cbc0888dfda70af2a058cd92483d1bf3`  
		Last Modified: Wed, 13 May 2026 00:30:43 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e08e3975dc80abab1d7078a935b8310dfd0436900117ac019cf7e74e96327`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa53d7a29128e22ba5071bc2c061d21df2672618f2d335495eee03b57b30eec9`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9aa3dda4800660b0c498edee92d63a95f3487dea910ee7b1e32237e7d8c01`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602df0b26626bd70f3e3b7e338c29f3774aadcb1993b32e11424961d5818b71`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c12f0b0a957349df9e5cdec68e05f8555034292db7712c2189c98bd96a1e`  
		Last Modified: Wed, 13 May 2026 00:30:41 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573942fa9e85b5ae2a2dd8eebbfe68a15cbc4562d77ed7b34b827ddf38d67873`  
		Last Modified: Wed, 13 May 2026 00:30:40 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6577aceea038d31c6741058ac70f3042052944add747d78e1e98f4768056ad9`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f767fdb48bc45cf9dfc7586e7f3bb6923b4260220f4751867e56819d9198c6f7`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805ccff5e068c1b1ef4ee49960a7779be478d8aac505863b20d6779b21c86cbc`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a088d5cf08a67d2b16495569498bf84dc519c98894eef90450facae9b2b1fd0`  
		Last Modified: Wed, 13 May 2026 00:30:39 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a013ec9aa226e3c490885f2df243f133e073c70c9f7fe42acf1c7c6d646c4`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9c59e03f4cda98b2b89df28ea3599e7ce642f3438c9607747e027edae7d633`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df98da5df2a594f3eaf8a18d588dd2dd717a8b9d65120307073b5097a7461ab1`  
		Last Modified: Wed, 13 May 2026 00:30:38 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738c190dc62e002473b0f2e0a6b4d56acd58d4befffd3a5254489344e3f514ad`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 110.6 KB (110619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d153bfc2eaf47e5d03b6d7723d1c90e94fbc34f9bd5394c155057ec6cb0fc42e`  
		Last Modified: Wed, 13 May 2026 00:30:37 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:4b2309a8fe290a6271bb2bdd006c30f27a06e0e18787c56c8604b1facf1cc9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:672b320378b1e89dde74d15a8a123068d26dafce6901597f4f8a837c5c38e7b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141244276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a5337ff6c38ebefe95a0943a39f42bab87a62f05d840422d53a0be69b65f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:59:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:59:25 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:59:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:59:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:59:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:59:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:59:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 80
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 443
# Tue, 12 May 2026 23:59:42 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:59:43 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:59:48 GMT
RUN caddy version
# Tue, 12 May 2026 23:59:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be1f105178ea258d105ecbaf5ec1f6000c5b289826e3b432c22080c650f719`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 524.5 KB (524474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7902ee53436295b9cb02bfa64ac6aa3b314c1e926ec77f7bb59eea811e28a846`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170554e1bf42badb647bc34b5718a5915fede948183bf5dc3d0d21e5540a0b67`  
		Last Modified: Wed, 13 May 2026 00:00:00 GMT  
		Size: 17.9 MB (17925247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a6d017c1aab65f96bd924d664427c093dba8210995905eaf00df2fbd142cb`  
		Last Modified: Tue, 12 May 2026 23:59:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04fc399abb90e3e2df99498e2eb88e7afd2a3f97e84400a40b7439ea46f1fa5`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d26c10fbf4dafe70c44037417bb3457e50a549f998a6f8b4799cf456c446e2`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295c37ba01761384092ce6a3f611a8792a57e0f772e6d8e3bfb099f51932a73`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb5b45ec93d301f781dc64b899fdfaa452f3d35dbbe0ba52fc5c87b02593d0`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0f84b59aead90c71aa95cd5340904935ff3da90339fa6ff21049d0f56f9ec`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1aeb5b58eaf433feb7668159802420e22345953cd345a111f5ff264e659bdf`  
		Last Modified: Tue, 12 May 2026 23:59:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03412a72c6ae737ad61b888338ad28fdc2b3477281195707e27619683236208`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a705083dc71361abc6a1e82aa158830dc6f3dd6e486a403f011f357eae4d884`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5637de44873a5862f646124e27d0fe311506c6fa1eec39c15df5312e1d41881`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4356db0d34adcecf1c9218951422411d7f942cb4d50621800af19388fdcc0`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a670d1e50cdca965f8cebdbf95f43d51e7fe8d7daf65312384a5731f3f743e`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc67002143e99034340b46a68c760d90626fe51d4e087bca7be0aa904ec8b45`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c8eddb6ea788613d96893c8e7c570d4a29a2b07f6d1ce823bf72faa05cf7b`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c21c96cd26011f147afe2c8c693897e2a126fbba132af7fc830d2d7559f19`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 351.6 KB (351565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c0ee074e227c1b13e1438189cfa031217727fc8085182b53234397774d341`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:13a01e024e1f987d2133e73315fea5688b3dde0f70bced70f1caad7c2b53e092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:672b320378b1e89dde74d15a8a123068d26dafce6901597f4f8a837c5c38e7b2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141244276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a5337ff6c38ebefe95a0943a39f42bab87a62f05d840422d53a0be69b65f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:59:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:59:25 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:59:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:59:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:59:36 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:59:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:59:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:59:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:59:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:59:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 80
# Tue, 12 May 2026 23:59:41 GMT
EXPOSE 443
# Tue, 12 May 2026 23:59:42 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:59:43 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:59:48 GMT
RUN caddy version
# Tue, 12 May 2026 23:59:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be1f105178ea258d105ecbaf5ec1f6000c5b289826e3b432c22080c650f719`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 524.5 KB (524474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7902ee53436295b9cb02bfa64ac6aa3b314c1e926ec77f7bb59eea811e28a846`  
		Last Modified: Tue, 12 May 2026 23:59:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170554e1bf42badb647bc34b5718a5915fede948183bf5dc3d0d21e5540a0b67`  
		Last Modified: Wed, 13 May 2026 00:00:00 GMT  
		Size: 17.9 MB (17925247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a6d017c1aab65f96bd924d664427c093dba8210995905eaf00df2fbd142cb`  
		Last Modified: Tue, 12 May 2026 23:59:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04fc399abb90e3e2df99498e2eb88e7afd2a3f97e84400a40b7439ea46f1fa5`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d26c10fbf4dafe70c44037417bb3457e50a549f998a6f8b4799cf456c446e2`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6295c37ba01761384092ce6a3f611a8792a57e0f772e6d8e3bfb099f51932a73`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb5b45ec93d301f781dc64b899fdfaa452f3d35dbbe0ba52fc5c87b02593d0`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0f84b59aead90c71aa95cd5340904935ff3da90339fa6ff21049d0f56f9ec`  
		Last Modified: Tue, 12 May 2026 23:59:56 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1aeb5b58eaf433feb7668159802420e22345953cd345a111f5ff264e659bdf`  
		Last Modified: Tue, 12 May 2026 23:59:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03412a72c6ae737ad61b888338ad28fdc2b3477281195707e27619683236208`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a705083dc71361abc6a1e82aa158830dc6f3dd6e486a403f011f357eae4d884`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5637de44873a5862f646124e27d0fe311506c6fa1eec39c15df5312e1d41881`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4356db0d34adcecf1c9218951422411d7f942cb4d50621800af19388fdcc0`  
		Last Modified: Tue, 12 May 2026 23:59:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a670d1e50cdca965f8cebdbf95f43d51e7fe8d7daf65312384a5731f3f743e`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc67002143e99034340b46a68c760d90626fe51d4e087bca7be0aa904ec8b45`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c8eddb6ea788613d96893c8e7c570d4a29a2b07f6d1ce823bf72faa05cf7b`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4c21c96cd26011f147afe2c8c693897e2a126fbba132af7fc830d2d7559f19`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 351.6 KB (351565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c0ee074e227c1b13e1438189cfa031217727fc8085182b53234397774d341`  
		Last Modified: Tue, 12 May 2026 23:59:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:206dde5cb85762b952e1ced7003d7630ae6e1f8f347ae67b56c84026948e8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
