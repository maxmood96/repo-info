## `caddy:latest`

```console
$ docker pull caddy@sha256:c5876b163e84c44815e2fbba68245367dcf341a15947f80bffffa011bdc90ece
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
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

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

### `caddy:latest` - windows version 10.0.26100.4349; amd64

```console
$ docker pull caddy@sha256:e36d18a89c288bae717237f6ec4551d12c2a8bc61a70ca60abb653cf4b6ee3a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3492599094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc47cc456e5ffe80e00e628995343ffb7ef9801d9805db9d4b9db444f6fa91`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:34:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:34:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 10 Jun 2025 21:34:43 GMT
ENV CADDY_VERSION=v2.10.0
# Tue, 10 Jun 2025 21:34:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cb97adb2bff5de752e470486ae72d55a6ddcfe4bfa43f09ed849260955df7f61385ac1e2d28fc80458b6910d71fa38d4295bb0689263dcc1743f2050d847c2ad')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 10 Jun 2025 21:34:54 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 10 Jun 2025 21:34:55 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 10 Jun 2025 21:34:56 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Tue, 10 Jun 2025 21:34:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 10 Jun 2025 21:34:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 10 Jun 2025 21:34:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 10 Jun 2025 21:34:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 10 Jun 2025 21:35:01 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 10 Jun 2025 21:35:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 10 Jun 2025 21:35:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 10 Jun 2025 21:35:03 GMT
EXPOSE 80
# Tue, 10 Jun 2025 21:35:04 GMT
EXPOSE 443
# Tue, 10 Jun 2025 21:35:05 GMT
EXPOSE 443/udp
# Tue, 10 Jun 2025 21:35:06 GMT
EXPOSE 2019
# Tue, 10 Jun 2025 21:35:11 GMT
RUN caddy version
# Tue, 10 Jun 2025 21:35:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3caab1dcbf5b8d24435dfe840a2125725f4a9a2176fee372f045bc85cdb0cf`  
		Last Modified: Tue, 10 Jun 2025 21:38:57 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a083786cf955a53a1e72ca79c58db985baf0b47d78f1358ecfbbd2b13d02e6a1`  
		Last Modified: Tue, 10 Jun 2025 21:38:58 GMT  
		Size: 388.3 KB (388311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9ce4bf9e7447e94642c6c121f3bd81b79169d94685b9e7f8f3c275b6db1755`  
		Last Modified: Tue, 10 Jun 2025 21:38:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96349fcf026f07bce17631d0b6ac19e533b0cd2cfafcd7968502a81afc83d67`  
		Last Modified: Tue, 10 Jun 2025 21:39:00 GMT  
		Size: 15.6 MB (15640456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bbfe63f9fb6ee82533d599e69bda2cd333cdbc0752070eb3606e329c068a0e`  
		Last Modified: Tue, 10 Jun 2025 21:38:59 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac8ec186e23e63c916f3800277ba39c5b2488f807d97036b1cd22591b7e4690`  
		Last Modified: Tue, 10 Jun 2025 21:38:59 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9734d9135874c0de3633c63e6b53d8b25e3ae755c6ab4071bcffab46a06f3b`  
		Last Modified: Tue, 10 Jun 2025 21:39:00 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf82296b97f6852031dcd90ea98e718f0ea0b1c6f9457e4ff8f227189837a08`  
		Last Modified: Tue, 10 Jun 2025 21:39:00 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a929112da06ad53dd76381285921c4b0743e30e3532b9e190f8dc6139da3b49`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8579a3adac1583b54fc9db9fe3abf4cf015a1360a2dcb23b7b3da632e7249e3c`  
		Last Modified: Tue, 10 Jun 2025 21:39:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f90066cdfadc8a932f6d2d1a9534e55e90d88af1301c1a22d646f376be53ac`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54a9f76c009405dc8c726ddc4b16b1e761b48442af4ea352ec41b992736db30`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9747180ce23a71373095bbafbcfd9336d86b2658245b8ef726dc294cded3fa`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1f6332ffdfdc483a13e2f0b99dc27b9d25769a80de3dc13e9f64e4b326be38`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135c6694a5f6f21e6842b65034228f2ebabcca7a02522653d8f5537b47dbb81d`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4820d05441404d06f206e63f58441f2096db0c3764d17d83224f8d566ebd00`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58106080363bb83028d5b03b1a625c5c1d408856efc741fef7a9a2a83bb480af`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3ff34450abf1162a5107abd80c46694b1e55c990ae4e2028688e6db2ce3d30`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e2298a4816f7b1d3c66211e72de5575c54346c6a118940dd632faa34ad5dab`  
		Last Modified: Tue, 10 Jun 2025 21:39:03 GMT  
		Size: 374.1 KB (374087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d78efe76ea42dd6481f214527712a8d331e2ea38ac0e2e3d92580b2e68599d3`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.3807; amd64

```console
$ docker pull caddy@sha256:1feb3de40efb531422cb3a85c6b7c743da6a79e855488a003ec9d35a05c58961
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296602328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d88530b88111e70daac13ae8cfdf0089f7e67042b3b8b222959d2b240e8ed7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:37:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 10 Jun 2025 21:37:25 GMT
ENV CADDY_VERSION=v2.10.0
# Tue, 10 Jun 2025 21:37:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cb97adb2bff5de752e470486ae72d55a6ddcfe4bfa43f09ed849260955df7f61385ac1e2d28fc80458b6910d71fa38d4295bb0689263dcc1743f2050d847c2ad')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 10 Jun 2025 21:37:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 10 Jun 2025 21:37:35 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 10 Jun 2025 21:37:36 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Tue, 10 Jun 2025 21:37:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 10 Jun 2025 21:37:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 10 Jun 2025 21:37:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 10 Jun 2025 21:37:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 10 Jun 2025 21:37:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 10 Jun 2025 21:37:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 10 Jun 2025 21:37:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 10 Jun 2025 21:37:40 GMT
EXPOSE 80
# Tue, 10 Jun 2025 21:37:41 GMT
EXPOSE 443
# Tue, 10 Jun 2025 21:37:42 GMT
EXPOSE 443/udp
# Tue, 10 Jun 2025 21:37:42 GMT
EXPOSE 2019
# Tue, 10 Jun 2025 21:37:47 GMT
RUN caddy version
# Tue, 10 Jun 2025 21:37:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f384a69fd63a497121790182b27d85aab1922fc24a9e1fbbc08d2690575b0fdd`  
		Last Modified: Tue, 10 Jun 2025 21:39:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc34bdcb8cd1f3bd14f8af2743ab939cf9b6ab8f7bbda2cdf245aef51be18563`  
		Last Modified: Tue, 10 Jun 2025 21:39:16 GMT  
		Size: 366.3 KB (366342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8033d9d5acb672d743f449249e4194737802a8510a54baf70a07bb8ec143c`  
		Last Modified: Tue, 10 Jun 2025 21:39:15 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c7ecc3c39a158f22582a80bd8c35d5f21e51cdeacd8151f7526a4cbe3406a6`  
		Last Modified: Tue, 10 Jun 2025 21:39:17 GMT  
		Size: 15.6 MB (15623315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efabb4b955b652b4b17f9c2153fbb1dc4f05874a747c8b29294226dfea6e12e`  
		Last Modified: Tue, 10 Jun 2025 21:39:15 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33b4c3173b978c2c67141b9b1ee9d63129cfcee6b845ea90b76e2009671a738`  
		Last Modified: Tue, 10 Jun 2025 21:39:15 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9255ef9ae4276d5de3280b1c5ea2e0eb6bac4d915c9775ef899e770d1e9a8679`  
		Last Modified: Tue, 10 Jun 2025 21:39:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434ed6a66cc2254d0294c5ea59b2cee8db274dd1b473292ddc83c911ec3ce8be`  
		Last Modified: Tue, 10 Jun 2025 21:39:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e653eee771a8d715bad67e79f3ef1c4f6de4ffd20807c1d22ac1b9c2beba4e5`  
		Last Modified: Tue, 10 Jun 2025 21:39:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05551e39c3d3b34a309e7a941711d1e236d339d26550ec214a69c99c3e617836`  
		Last Modified: Tue, 10 Jun 2025 21:39:15 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eda5de0938c780fa6340f56f163c25311fe091e63e0c5a4878efb4b5577bf99`  
		Last Modified: Tue, 10 Jun 2025 21:39:16 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bfb08112bdd48cdf85e8d8e38041c74d73a216a8939c188964dba7aba9f35`  
		Last Modified: Tue, 10 Jun 2025 21:39:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86666f874c60895c71e7f2e0cfafde43d32e09f640e44dc3b13596d34f396d21`  
		Last Modified: Tue, 10 Jun 2025 21:39:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119286e8f3eab5eeaf82414d9132df91db284e2c8166b17be9cb0e261bb7f6c6`  
		Last Modified: Tue, 10 Jun 2025 21:39:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977e3b17e583baf97032ed84dcfffc0a5b1ad2e7638c8dcc0cc051f339f53834`  
		Last Modified: Tue, 10 Jun 2025 21:39:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e2f75d227d9d64f334bc679e0e529dc31fef74fc654f161aa74f16989371c1`  
		Last Modified: Tue, 10 Jun 2025 21:39:17 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e79284767b324cea4abf9f09443cb63506638f243ea3d11eb8f248d8a790c5f`  
		Last Modified: Tue, 10 Jun 2025 21:39:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b620ac538cbcb1a8099d94e4e734412c9e9045950dc768268f297cb29780f881`  
		Last Modified: Tue, 10 Jun 2025 21:39:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287dc5744cb9fda5640c8f8c6c6d2c11cf3f50de9a294460aa996d63bbc19c28`  
		Last Modified: Tue, 10 Jun 2025 21:39:17 GMT  
		Size: 339.2 KB (339195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5efbaf99f9e8ff6a21eca812ede292a79a931df387e04dae03b79aec5b2df8`  
		Last Modified: Tue, 10 Jun 2025 21:39:17 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
