## `caddy:latest`

```console
$ docker pull caddy@sha256:30ccf0cb027e1d06cd6e453c04fc1c8eec665629b22ed69602c14c8a0512ead0
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
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:168773f6a71e59a547227f4a0f876fd16eadb091548d6742a450c155dc89370d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19000250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14300de7e087290520999f00d6a12b61385d1fe780ea83f38eabb7e8be66225f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5475df3da1b8b8e7fc4d03cecc2855d17d9afd6a39bb8c38230e593898f5871`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 359.7 KB (359712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0ae3ace4a6677e8f7dd581b01b00ff6e6c7a0e7d3c4d10498fe4402e13223d`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb621c62f244f7193bb19bd2cca4acccc4c11379cad707e6ca0aaf33eec9e71f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 15.0 MB (14990762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:ec9b53818c7c5f2bc4cb7e492d5c9f99403a4501c12b7c8b5096587d54f294a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 KB (307675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eced5b4e89aa1736dc4f697091a590bf8ebb9b0b152dd8d3bcb524b110b1aad4`

```dockerfile
```

-	Layers:
	-	`sha256:468a16bf043861989d7ec5629968e881b54a12572296a0e06462e3fec77bc395`  
		Last Modified: Thu, 08 May 2025 21:27:50 GMT  
		Size: 289.4 KB (289397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a08642e0e5e7a10cf5ebc4a79b7942099dee3a27a2ce4aa03f46ae69067eca9`  
		Last Modified: Thu, 08 May 2025 21:27:51 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0f600bd70f1263ad2c44e6c719c944946a36df2e5be767a7787858bcefc41980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17847842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec2556c47f457dc30e8a48173d5371f717a2dd079d24900a408a525e7136a2a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b30f46e58aeb7154ecc77c4fac1f2045f0e81c1c6affc8f59ed0ae9b0ef894`  
		Last Modified: Thu, 08 May 2025 18:17:58 GMT  
		Size: 359.8 KB (359826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2851d2281d8488137149315d279645417c41f41b0ab05a60924c6fe6726d10`  
		Last Modified: Thu, 08 May 2025 18:17:58 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5006317a9d58664318050c90ad2c6eabbf1b9e7ecafec64a97f5cf15698d0f`  
		Last Modified: Thu, 08 May 2025 18:17:59 GMT  
		Size: 14.1 MB (14115756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:709e23547d12f2e0566d2da0ae35201b8bae0a1efdb28104442ce7dbaea9eb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d1963edebbbc59bc768b99631f774445ad034af5c9e422976e0603397a970c`

```dockerfile
```

-	Layers:
	-	`sha256:e18058a686ef7099af30b96a6f0a9eaabe42543aab8487651992f7bf311aa47c`  
		Last Modified: Thu, 08 May 2025 21:27:53 GMT  
		Size: 18.2 KB (18196 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ef76d40199a773a4d7d2fb4aa90c1f6973b66ebe867607a139ea106b18f62545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17551935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc0e56bf857a3db48c8a4877f8ae7eaf1a3213c554bf0307a355663e47c90db`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b486ad787eef6ee3449c20ea2e033a60c94975170108deded72601cb351e96`  
		Last Modified: Thu, 08 May 2025 17:24:16 GMT  
		Size: 356.2 KB (356173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ea30f793f2042fcd87e05691085f5048a6345213bede96531bb1255fe5d7bd`  
		Last Modified: Thu, 08 May 2025 17:24:16 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1577028b4f9ddb3e411e793941ff5944925f142711591227cbfc64b0e0e14e92`  
		Last Modified: Thu, 08 May 2025 17:24:25 GMT  
		Size: 14.1 MB (14090109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:5876f355e6976d4c26cd3971e64f21eb08e361cffd5a6a4acc1cf10c5a028e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 KB (307876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4901dda94de5b5034b642d1ccdb1899fc312ff365563d20ac945e8b489aeb`

```dockerfile
```

-	Layers:
	-	`sha256:c5e1861069bca57d120dfc27c27864d78dcf0597a3f1df435d8d92ea3a5dc464`  
		Last Modified: Thu, 08 May 2025 21:27:55 GMT  
		Size: 289.5 KB (289465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fadf0e4cc0639c97dad7f964afea4e206fd6967ad188c97621b32d6a742248ca`  
		Last Modified: Thu, 08 May 2025 21:27:55 GMT  
		Size: 18.4 KB (18411 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a66f5bac01988c757fb3e2b91fcc873ddb2d88c6b8411abb913cf715beb0b90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18177332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d929019a0918720a60b006a595d05c2ffeeff649c00187cf7bc560e2baa2c199`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6e55cd805349a25f66903d67e800bfb884c4e28423889241b268c5f0c72cf6`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 369.4 KB (369372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1d2c43b341f4a4e9143550be625217e7a35973dfb389f2e9a07f2de63d7f42`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014036ce367bf93136e5103e0d3640285faad8c2a155bf9a89fc9601be609483`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 13.8 MB (13807403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:f703c5a3a90966c81395c785a3ea2532dc899a380b55cd8177f28e8c3d14114b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (307961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f3fdaec79a6fa2179539ea7e556a0d12eeddded7ad3a862bef7f933dfc80a4`

```dockerfile
```

-	Layers:
	-	`sha256:45c1db52fe8fae62f0ed06cf622c45af794fd12cd25f2574a58641813ddffae2`  
		Last Modified: Thu, 08 May 2025 21:27:58 GMT  
		Size: 289.5 KB (289501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b4fe8c9b051bd21f710e8cf1c3e864632fb7c8750daf5a2e85e41f6451df06`  
		Last Modified: Thu, 08 May 2025 21:27:58 GMT  
		Size: 18.5 KB (18460 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:1970c50819427850bdb66696913103d86eb7dfbc7b41ff7cb286d1068d19d2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17537430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3978bf973264af23340cd2bc3ab966e7f8274ba83d286ffbb124e874daf53a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b94ecb1569d71d505d1fd7d767dc522c8fc7abc5685bd2619d4091c7ccb7819`  
		Last Modified: Fri, 09 May 2025 01:58:15 GMT  
		Size: 372.2 KB (372240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3991d5255392de9ce88e69adde15bbd39e3851a388bb6be10994bc4cd1397a9`  
		Last Modified: Fri, 09 May 2025 01:58:14 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db5199582ffcf470247b3f98bbe12ee3f541182eab10c873b53c3d3872ded97`  
		Last Modified: Fri, 09 May 2025 01:58:16 GMT  
		Size: 13.6 MB (13583315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:6611557177235a592c58f5dd1acf4fda5cb97ec3b075484667927709b44ee27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 KB (305853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd5df6690ef820de578fad397a171db71c01bb3595888233931b1a71d2a9177`

```dockerfile
```

-	Layers:
	-	`sha256:d8b91a7908d7598bf364b8ad9f0dab63b2ba9ba6b210480fb7bc9472508e3d91`  
		Last Modified: Thu, 08 May 2025 21:28:00 GMT  
		Size: 287.5 KB (287504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:524217752cd4d242b2d3e0c37d1fc40edaa3d3bc640514dc37ba0a64d59b8ad4`  
		Last Modified: Thu, 08 May 2025 21:28:01 GMT  
		Size: 18.3 KB (18349 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; riscv64

```console
$ docker pull caddy@sha256:764df8a529f027ddda853b996dac6fd0b66adb79554704d5845b64adf5ccae94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17972169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a09af47c78232e33db53f46bdae051830f9bb854e5cc7f432c8b82e58c2b6e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c99b63711423ce29b2b6496d52c616a66df016341559d14178cf3bcf6055ff`  
		Last Modified: Fri, 09 May 2025 01:58:15 GMT  
		Size: 361.4 KB (361446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee0f48f29753795e0b6387a3f1b3b1eb6332759ee258e311d178a771bedc3d5`  
		Last Modified: Fri, 09 May 2025 01:58:14 GMT  
		Size: 7.5 KB (7501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cfe4d3e49edeb5ca45aebc62489093dac7c952ddd442c24f0a74933dfdb176`  
		Last Modified: Fri, 09 May 2025 01:58:17 GMT  
		Size: 14.3 MB (14251751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:d6f61c0f6bb5985497cd9776676cb32094d62a9d19e4094fac9205f42f56b509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 KB (305849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e769a3142ae080ae0a59d5746c7586d96e586e56735c3e89b294de5d9e5ad959`

```dockerfile
```

-	Layers:
	-	`sha256:59058a89eaa642483feade7c88fa07b3c161bf8a5e97cb464a7c90c461027826`  
		Last Modified: Thu, 08 May 2025 21:28:03 GMT  
		Size: 287.5 KB (287500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ac08399bbb018a4992c122dbc5ff662ca7dbae6f00d437d76a7133de33818da`  
		Last Modified: Thu, 08 May 2025 21:28:03 GMT  
		Size: 18.3 KB (18349 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:8a91307be6c5e5aef08f2b16f2d04cac28cd66fb85a743ad3919382f577cd493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18296550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7cdf03fae2e688e6bdec77b971a227043b2144fc70cb3eaa067df732322aa3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Apr 2025 03:51:58 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV CADDY_VERSION=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='626682d623ca04356ab3c9a93a82386cfde6d8243b11f2d0eea9e97ba630c7ada62373401e96b72c6690c98ae8dd004d61fafe477f5249690d5cb251ebbfd2d9' ;; 		armhf)   binArch='armv6'; checksum='c4647ed1b5407bd61d55f357af62d3935f2972bb5b03472a2747c4c19610376174bdb573f10b936cbc81acd8a103a0b961118d360cebe2b60693161f83e7f046' ;; 		armv7)   binArch='armv7'; checksum='e6794aef179ec3319c5d692fedbb424532a47d7caf19a67ad2a4317c5f2776baaf47658f9e1f7fd37d6f3447a18285cd1d7cb91d0088f5cd01d73874a43aa9c2' ;; 		aarch64) binArch='arm64'; checksum='6d100bfd609e8cfe6a51afe1b86066ac68f53ac56670c74a7d7537d93c643aa7f0e82b9f3083218eee1d369a427bfcdafcb445c7a730f9fc0ddf546401d95484' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='9559d544b8f919837f66623955fd95b03511d85c56455f43d9cc6d0010c00bb1e81fc3b7b5e5a2f8d1d0f65d9571c80cb8b706ea94e2baaaeffec5ae52f68a34' ;; 		riscv64) binArch='riscv64'; checksum='9633d6f6c2bf1911d5887a5d0ea885413785e0968550875b995eecc3bb5fbd1267edec0add94a0286349273e4df0dc1f1067d5639c2393019e235536c1b7c477' ;; 		s390x)   binArch='s390x'; checksum='5b29b377409abb9b8d241b95a11f1dd5d709759760b1514c9fbf616c3975048cf384441527fdc179bb8b08dc6189afe9df33499b46509e5d0e3bd6da8bb293b1' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Apr 2025 03:51:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Apr 2025 03:51:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[80/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[443/udp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
EXPOSE map[2019/tcp:{}]
# Sat, 19 Apr 2025 03:51:58 GMT
WORKDIR /srv
# Sat, 19 Apr 2025 03:51:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ee347a7f748980f8331e4226e98ccbf36b00b44c46921a8b47a39502b344c7`  
		Last Modified: Fri, 09 May 2025 01:58:16 GMT  
		Size: 366.9 KB (366907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39916ac955bcb2c4ce48380caa442377e7f12e20b150efab4c38b1dfff7f74a6`  
		Last Modified: Fri, 09 May 2025 01:58:15 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318d1c77b7a4994b00fb22110f92235a2f18c38977436099320cf3e99652243`  
		Last Modified: Fri, 09 May 2025 01:58:17 GMT  
		Size: 14.5 MB (14454546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:2dd801e7bcc79b26ee94f52b2368550fdf129137252c4d834cca859e61c074c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 KB (305724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8bc58c5a925208e6d428c1c1672e260f866fc40b989ca41dc930c9e5cc310d`

```dockerfile
```

-	Layers:
	-	`sha256:37a0537dbd2a4dee8acbe612d4abd06b22997aadd632e6fcfc89fb0e93e4c9d2`  
		Last Modified: Thu, 08 May 2025 21:28:06 GMT  
		Size: 287.4 KB (287446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369b258a2fa362b7d82a7bbaf01e690d9944293503a0b11380abe6c6d875c74a`  
		Last Modified: Thu, 08 May 2025 21:28:06 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.20348.3692; amd64

```console
$ docker pull caddy@sha256:44f20ec51b71402b6b8277ea4c2da1d30339b76013c608682a1d34773bc3ab6e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289937043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b43e7689ba9c40bc52c17df841c24f8d4a12ebf22ed8a44c0586d10b9fc4368`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:13:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:13:21 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 May 2025 21:13:21 GMT
ENV CADDY_VERSION=v2.10.0
# Wed, 14 May 2025 21:13:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cb97adb2bff5de752e470486ae72d55a6ddcfe4bfa43f09ed849260955df7f61385ac1e2d28fc80458b6910d71fa38d4295bb0689263dcc1743f2050d847c2ad')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 May 2025 21:13:32 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 May 2025 21:13:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 May 2025 21:13:33 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Wed, 14 May 2025 21:13:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 May 2025 21:13:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 May 2025 21:13:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 May 2025 21:13:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 May 2025 21:13:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 May 2025 21:13:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 May 2025 21:13:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 May 2025 21:13:40 GMT
EXPOSE 80
# Wed, 14 May 2025 21:13:41 GMT
EXPOSE 443
# Wed, 14 May 2025 21:13:41 GMT
EXPOSE 443/udp
# Wed, 14 May 2025 21:13:42 GMT
EXPOSE 2019
# Wed, 14 May 2025 21:13:47 GMT
RUN caddy version
# Wed, 14 May 2025 21:13:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3774c38aded90a32237b47099f5d0c5b4ae5907cff795e83cec47ab8da64234b`  
		Last Modified: Fri, 16 May 2025 14:42:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7299d406e42a4323e3ec0b297d9224f92280d1471de9f8ca7d5b39a57a57f63`  
		Last Modified: Fri, 16 May 2025 14:42:57 GMT  
		Size: 345.7 KB (345689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0430d40418bf59f5653799f54cd1cb259185675f09cd7622ad3d6ebdbe02ff2`  
		Last Modified: Fri, 16 May 2025 14:42:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901686b3434c3d1953133fa9543b31cff53651fea548d67a69d2a3cee980937`  
		Last Modified: Fri, 16 May 2025 14:43:00 GMT  
		Size: 15.6 MB (15601994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2e820ef0f10cc9bb789e73ef65a3b9976f5f71211e68ee81983c346ddc6542`  
		Last Modified: Fri, 16 May 2025 14:42:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db837c93884436b76f9a7684f6ece1697cc24198890423b8cb970545556947a1`  
		Last Modified: Fri, 16 May 2025 14:42:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba20387152e18221acd8b43eba572070f34cf3fd361351b8455757241f386ed0`  
		Last Modified: Fri, 16 May 2025 14:42:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150d0732b6d1945b3733a17e3e7a918361fc158f81e9e35981a5777b9961ccf2`  
		Last Modified: Fri, 16 May 2025 14:42:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61732a9c422acd496075fd26316432522a4ab232009a061fdfd90bf2374744f`  
		Last Modified: Fri, 16 May 2025 14:43:00 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a661e52a5bb9fd330fee6f444e50e6cb8e4bd7ac0c43b9de36c010eb650c75`  
		Last Modified: Fri, 16 May 2025 14:43:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18c885e2fec1e0155028271a3f76db6a07c9467e5ce95ce6b7d99e105b8a28`  
		Last Modified: Fri, 16 May 2025 14:43:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17121e3234fd9e657ff05b74dc9df64a1eebfe9ad69dbadca727bcc43e8e736`  
		Last Modified: Fri, 16 May 2025 14:43:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27d08f95daa6a22a997e60826ca01bab1ef6a73ecbb7abe68afed40dc6f21b7`  
		Last Modified: Fri, 16 May 2025 14:43:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcfe1bded2693c2559aac6507e7759338ae55764b40d3ddc13cb127467ba954`  
		Last Modified: Fri, 16 May 2025 14:43:02 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ba5617d8d789ee415761fc2deb49db082127b3ec5882dda3f4e220ee30411`  
		Last Modified: Fri, 16 May 2025 14:43:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e801dfa8e565b6a764546cf59d37766031cabefae950bac71e00556d3181925a`  
		Last Modified: Fri, 16 May 2025 14:43:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868edfcff37e597842cd4c8e4a2ec1aea69b62b47887ff2c5c9869daf266e50a`  
		Last Modified: Fri, 16 May 2025 14:43:03 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc17f222d8403aec5c10c7e74eedc05c61aa532f5f5c96bb524ed903929089a`  
		Last Modified: Fri, 16 May 2025 14:43:03 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ace187b2921d578888456e562dbea6270eef3147e12138c151a878446adf8f`  
		Last Modified: Fri, 16 May 2025 14:43:03 GMT  
		Size: 339.0 KB (339040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d78a56066095c33c16c4b8f724545c3241d74dd931e62ff5501d1208b72aaa2`  
		Last Modified: Fri, 16 May 2025 14:43:04 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.7314; amd64

```console
$ docker pull caddy@sha256:3d368129f276d4d15c37d532ffe197600f0e5ce4915a2a0e8f36ac2cd89f9673
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2200043435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21ae73e3551f096c385f65742da4c5242fed5251d1e3a82bec37813bfa07309`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:12:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:13:34 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 May 2025 21:13:35 GMT
ENV CADDY_VERSION=v2.10.0
# Wed, 14 May 2025 21:13:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cb97adb2bff5de752e470486ae72d55a6ddcfe4bfa43f09ed849260955df7f61385ac1e2d28fc80458b6910d71fa38d4295bb0689263dcc1743f2050d847c2ad')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 May 2025 21:13:47 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 May 2025 21:13:48 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 May 2025 21:13:49 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Wed, 14 May 2025 21:13:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 May 2025 21:13:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 May 2025 21:13:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 May 2025 21:13:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 May 2025 21:13:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 May 2025 21:13:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 May 2025 21:13:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 May 2025 21:13:55 GMT
EXPOSE 80
# Wed, 14 May 2025 21:13:55 GMT
EXPOSE 443
# Wed, 14 May 2025 21:13:56 GMT
EXPOSE 443/udp
# Wed, 14 May 2025 21:13:57 GMT
EXPOSE 2019
# Wed, 14 May 2025 21:14:02 GMT
RUN caddy version
# Wed, 14 May 2025 21:14:02 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff360741fc146a9e5a8abd1de22c377c4abe58b079116fc0e4db80d4933fe25e`  
		Last Modified: Thu, 15 May 2025 20:32:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd1863845f304aa1fa8f7549473c757ae8e1e9a77cfea88d1b5d5947ea2e238`  
		Last Modified: Thu, 15 May 2025 20:32:06 GMT  
		Size: 355.6 KB (355593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc68349540ba5028c91efb0928a4e87919f8dab4ccb036ac03c71c28342c5f6`  
		Last Modified: Thu, 15 May 2025 20:32:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72977218970bfa46c10729f93140e4b97b52c2ad6ee7d9bd93fe85fda9c09def`  
		Last Modified: Thu, 15 May 2025 20:32:12 GMT  
		Size: 15.6 MB (15610610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecccb40d70e4d1df31d7893c206dbd5d896194208edfa48a14763cbc1e78533`  
		Last Modified: Thu, 15 May 2025 20:32:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83e8a7c3c82ed815cd41ef92db99ed6dcfaae1f435a061d4cea207868bbb8dd`  
		Last Modified: Thu, 15 May 2025 20:32:15 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a26c843c2febd8351e97ebfe8e7017386df58b571427102a02548efbb982214`  
		Last Modified: Thu, 15 May 2025 20:32:16 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b45af0ffe57c1f44c3f46f3b7cfb9402545c07628ff14f05254b24fa8999b85`  
		Last Modified: Thu, 15 May 2025 20:32:17 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deaa31918858357e973f51186c422afa476b5622faf608b6de749d8e44b275ee`  
		Last Modified: Thu, 15 May 2025 20:32:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301947824fc58ac1977f31c1270ba2b24ffa51b01b8d35fe9d0bb177c0026c5c`  
		Last Modified: Thu, 15 May 2025 20:32:19 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aab28ffd968f44bcd11b326d120b6ca8b5b36e50209461857c6b552499288af`  
		Last Modified: Thu, 15 May 2025 20:32:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7cb7c5e12d3df6d7b3ae8f92b151de0ac2d5944ca842a6e5111f497ee1ee2c`  
		Last Modified: Thu, 15 May 2025 20:32:21 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4678a9955eb9fd8b9d79be35eaf885c899799d2ba7bf97d87fd39c57c50054`  
		Last Modified: Thu, 15 May 2025 20:32:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdf500837bc2f19e72e103b452b74382013947dab4f1236f73190e4c57b59c4`  
		Last Modified: Thu, 15 May 2025 20:32:22 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251e8b3e7baba526f8124288ac1e675c1cb49e4fa161b25ff7df03b2b86688a`  
		Last Modified: Thu, 15 May 2025 20:32:23 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f491754ab67d404be6a9e61f3bacaa711ea67b158d0c44721dc696395ed15bf`  
		Last Modified: Thu, 15 May 2025 20:32:25 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cefedb06852da4f954893c3180e11c8dae4152c5c5e3bb78af561fe4f88aca`  
		Last Modified: Thu, 15 May 2025 20:32:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d48c7c115f3ac6523b5fb0e6e5e405549b56233dddc2aa59385b6bfbe19fef6`  
		Last Modified: Thu, 15 May 2025 20:32:26 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5736c9951e0befe82655aa5adf793f4489a4930ab297294b7b9937691fe01df`  
		Last Modified: Thu, 15 May 2025 20:32:28 GMT  
		Size: 337.3 KB (337345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfa73a0ffd70fbe1380771e72683b623040af43d80950f67c270ff3c1cec369`  
		Last Modified: Thu, 15 May 2025 20:32:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
