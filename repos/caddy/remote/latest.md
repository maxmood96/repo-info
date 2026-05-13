## `caddy:latest`

```console
$ docker pull caddy@sha256:f6ec72f1a5c5927d4e269f27f4d8c7e4a9cb06641d2118eb33d91f68d9fbd14f
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
$ docker pull caddy@sha256:7260463ad61733ff5f6f59f878486624bbd2a9b4272518ac08c116c975bec166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22649843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1a8cd86ebff26a92c1450ba06041bbb070b5680a8ea42d13336c38486362a0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 07:16:52 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Fri, 17 Apr 2026 07:16:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Fri, 17 Apr 2026 07:17:01 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 17 Apr 2026 07:17:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2513b289054386b76642a9e8bfc10d217df2b5361e4cdd0c72672b0eeab57ae737d57466eb70f1a44233cbcc697ecf21de88137ca45ef4b64f150a32b58f5f14' ;; 		armhf)   binArch='armv6'; checksum='bdce2a9c07a17d1ef36fd81cbfcae282de5b5ecc1b911592463e9f06033ff395bbbc2322bff557d086a614223c005f046cc0d5679b70813a8da3c2e2a93463de' ;; 		armv7)   binArch='armv7'; checksum='acb0dc3ece97922b374fef492682b7ecd6d302a417e01abd12570360f055ebe1673d6032a987525475c1181eee7ea7c2efc0b17f1aeec1799303a1efa57deabd' ;; 		aarch64) binArch='arm64'; checksum='630d1e096e3c9594fd2f4f7129356ee5d6c7e53d0ca1b9a0c7486612c6d752ff355c96738c7a28c60367a5f1da4b51afca731bb745fb0b97cda4c811214cdc48' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2f885d026be962b3959cb24adc2294c30f4a385b111216d8aa4296adf700854065c62b4bae7b32228176c8c26ac97193db3a7a38fdffaf74cadde1293ad2e304' ;; 		riscv64) binArch='riscv64'; checksum='4fd9ed8feaa3f239901fd3376897a132ee05c467d73c8b448163cb341c570208b9907ca316a1e475a5b8d4594507a1c5cf65d6cbe2e309af81f7b8a620b3796b' ;; 		s390x)   binArch='s390x'; checksum='d9f6b53330aa36badcde1cce49f38e4e577c24b91ea522eb6680fb49e07cda3b2ee83de83a7e253c3ebf8f2ec38f7de16f75c09a8590c1bf126bdc67df576185' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 17 Apr 2026 07:17:01 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 17 Apr 2026 07:17:01 GMT
ENV XDG_DATA_HOME=/data
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 17 Apr 2026 07:17:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 17 Apr 2026 07:17:01 GMT
EXPOSE map[80/tcp:{}]
# Fri, 17 Apr 2026 07:17:01 GMT
EXPOSE map[443/tcp:{}]
# Fri, 17 Apr 2026 07:17:01 GMT
EXPOSE map[443/udp:{}]
# Fri, 17 Apr 2026 07:17:01 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 17 Apr 2026 07:17:01 GMT
WORKDIR /srv
# Fri, 17 Apr 2026 07:17:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218bd489171f8531b5e25c99a8157d3b666349873396cc06bbc5ba06381d7d03`  
		Last Modified: Fri, 17 Apr 2026 07:17:48 GMT  
		Size: 3.0 MB (3024643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92411b5bbb77817778886815977dc6ed7c75809299e34e4d778a2b7a4d621f1`  
		Last Modified: Fri, 17 Apr 2026 07:17:47 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8071266f877b5adc028242f20e06c6519af755b22e85e6c83dda823a1e9f8d`  
		Last Modified: Fri, 17 Apr 2026 07:17:50 GMT  
		Size: 16.0 MB (16030001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:5683d2f88f26b57f115706a618e2e3f6979b05adbd4e9b6ec3479953c14139fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 KB (350862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64a36beba079609ff2e8ca9f5462b1c9c83de54a347c79d1711addde2dfcff1`

```dockerfile
```

-	Layers:
	-	`sha256:9a67824e1f9bf4caa331a77e012a1ec5ca808374fba22ae8b6f002d139af5c31`  
		Last Modified: Fri, 17 Apr 2026 07:17:47 GMT  
		Size: 332.4 KB (332360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90887d3a5a531e740d5d7de9677bd6c552e11be06d922bb3b262b6a788cc51bb`  
		Last Modified: Fri, 17 Apr 2026 07:17:47 GMT  
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
