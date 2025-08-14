## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:ae4458638da8e1a91aafffb231c5f8778e964bca650c8a8cb23a7e8ac557aa3c
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
$ docker pull caddy@sha256:f43d8810c944e27e6f7ea80b165de11dbdab16cff15c8a80d83ae3e1a109a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18982850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddf74dfb6187e856dab57d2bf87ab6ae10f093dd7ced7ec1f6d485eff7e7649`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3cbe9aede833015a621a459f7f1aef7dc19f5bd8a8ee299843f76ab02fe371`  
		Last Modified: Tue, 15 Jul 2025 19:29:53 GMT  
		Size: 347.0 KB (346993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cbdd0ed56db15f555cea68913014ad4b325a2c8c9a6f39b1502418f6809dbd`  
		Last Modified: Tue, 15 Jul 2025 19:29:53 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3479dbb610224ae6000ff952d4ee14e55bd0e9fd75538ac04098cec8026d10`  
		Last Modified: Tue, 15 Jul 2025 19:29:55 GMT  
		Size: 15.0 MB (14990760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:793ec0315797908e09ffcb83db0a08db98247f59292315b537da465a0e7e2253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 KB (305430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50864c8a751f380fa267ea2c2eec21ab2d4bce5c8e3eec161345b2d9743c2ea`

```dockerfile
```

-	Layers:
	-	`sha256:52b5ab16828747ed2b6f975a549b1ef293fc5ca46e1da18ef12d6d6cd2792f48`  
		Last Modified: Tue, 15 Jul 2025 21:52:19 GMT  
		Size: 287.2 KB (287152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a718c65a96d373ac9eed85ee7fae5ee4700bbf5ec4f6334f032d9bfdb20e0bb6`  
		Last Modified: Tue, 15 Jul 2025 21:52:20 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:55953862c4a554eb95f948bd60ba43a19f227d614684e2c8ad7d0cd87bf5e2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17833623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1d056f38b71d2c4524c15e5bdf5a8a85a048d494bf0774f37a27a608ea0262`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
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
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51b6c88b78ddfe02112371248941ee3915acf1ac96f33e3ef3f39a463e6169a`  
		Last Modified: Wed, 16 Jul 2025 03:29:47 GMT  
		Size: 346.5 KB (346533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39c274db434228d64d42ea897eee87ba7a79298fd5cc64f7cc0e695b6c04da6`  
		Last Modified: Wed, 16 Jul 2025 03:29:47 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18145c5c235699bceebab8363203637bb92922c57d9d9cdea998645097401a8`  
		Last Modified: Wed, 16 Jul 2025 03:29:48 GMT  
		Size: 14.1 MB (14115749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:35b46aefc7c49fc5c4f5e9c8364dceba8529b0ffa4ea371fe6ac9eac13bf0083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc657d91f8e72605fafb24c8c0a7f90dc61d53040e4dd69a1451a919934514d6`

```dockerfile
```

-	Layers:
	-	`sha256:19e4a16ffa819003b6761bd5acaae93f1fb8d32caf9b126fb6eefc2bd7ee1f10`  
		Last Modified: Wed, 16 Jul 2025 06:52:29 GMT  
		Size: 18.2 KB (18197 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:b24c6757a6e1608a489d961b182374a269b857c185a2f4fe92aa0f72e099d035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17537850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96ff8f816911509fe785cf6b7e9e8a03cd73c0d9a443d0256a116f25d14dd81`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
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
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d797bf4c9ea344f6dd8e15018571e8dd98a2f5b05450d0f1ef453c9bdf7a63e`  
		Last Modified: Wed, 16 Jul 2025 03:32:41 GMT  
		Size: 343.3 KB (343348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c5d02f253f89bc3f5c3230d73398f9dc3b5aa5d4a6e914301e24aa62c7b4b2`  
		Last Modified: Wed, 16 Jul 2025 03:32:41 GMT  
		Size: 7.5 KB (7491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32771c342af7378b1dba35a197d3274f76ba2829ded67bf238db1cc48608a16`  
		Last Modified: Wed, 16 Jul 2025 03:32:42 GMT  
		Size: 14.1 MB (14090108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:8f098b60102e426d18d95f41d943eda1dda96486c78c1e52ffcc8c2f74b737ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 KB (305632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9e01c9d4571413cdd962783bd91c0d446f1d541ac950448b9317e5715f9b8c`

```dockerfile
```

-	Layers:
	-	`sha256:f5d41b32325bdb82250d7dfc4698d1cd9ce14fd4c134533591ac52e2f1065dcb`  
		Last Modified: Wed, 16 Jul 2025 06:52:32 GMT  
		Size: 287.2 KB (287220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a749a53612af2842c733521326c53885244b13299e4ca93503f07b4c1f217de`  
		Last Modified: Wed, 16 Jul 2025 06:52:33 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6cbb331b584f701e31f54d68a4e42a51df8bcec32babb79bb9d20458defbf3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18159903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff509efbd450c7fea55901ea87fd2d485c0f27b54d00d993938ae3076b2574d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
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
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514763616e4837a5f1d7c080e7b431e90a2010aefc98465f2051683b631dabf4`  
		Last Modified: Wed, 16 Jul 2025 05:50:43 GMT  
		Size: 358.0 KB (358042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ef7d990d15114cd0057350fa2daf2340bbd98976fbfbb99f5b19c5a5057bea`  
		Last Modified: Wed, 16 Jul 2025 05:50:42 GMT  
		Size: 7.5 KB (7490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e50f5f0c12f038103503a72a2982a3440b6ac344372194bb7e525bb4aed2f8b`  
		Last Modified: Wed, 16 Jul 2025 05:50:44 GMT  
		Size: 13.8 MB (13807402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:37f44284e9f24138b983fb6fece257cff30ecbe17aa176f3e459dd37ce33d745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 KB (305715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1de1bc6afd25cf5bb2b529e46b85d9be001d3b91e934b32c21205d987937e35`

```dockerfile
```

-	Layers:
	-	`sha256:35aa0c508165fcfe813367e2e30b1ad3cd55027fd348bfa0bd1b0ec5d67560df`  
		Last Modified: Wed, 16 Jul 2025 06:52:36 GMT  
		Size: 287.3 KB (287256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e155db5eb5b78d8a493159ba09d3d26363083d4adba596d164ae7e10803497`  
		Last Modified: Wed, 16 Jul 2025 06:52:37 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:189fdf94250d2da747f321dce1cd6898051eb120e3abb9c818f190bbb70444ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17520794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f9e4d6efc0c22b6cb49ccbd93e97d49dc0b4565773c6c28e6c0c4bf43fec0d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
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
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0973d85d8d0dd52d4da8784ff18b17734c7fb0eba98a8ab1254a307eb673dc4`  
		Last Modified: Wed, 16 Jul 2025 01:15:47 GMT  
		Size: 360.8 KB (360820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca59bcf6a9a78735f883018701652e50f5d1f870de34fc0736bf77c46d0bb`  
		Last Modified: Wed, 16 Jul 2025 01:15:43 GMT  
		Size: 7.5 KB (7495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10643123454856a1171c6436bf89ba688ebea16041aba0999e26f4ac0d4ae1c7`  
		Last Modified: Wed, 16 Jul 2025 01:15:45 GMT  
		Size: 13.6 MB (13583322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9a4912979c7b962fbe14383ef26491b24ecaf894495af419d48713a680b55f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 KB (303609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed14bd3f8fbbad9100f9b6bb64a422b9f620f18b18a885e9dde1bf322cbc2984`

```dockerfile
```

-	Layers:
	-	`sha256:9bec1b7ed33c354af9360fb9bafe96947516407ae95ef9374ea56ebf405aeaea`  
		Last Modified: Wed, 16 Jul 2025 03:52:27 GMT  
		Size: 285.3 KB (285259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceee19b3bc3d3149c1df88513887779c91305b091f4817d783aebd77ed78e81`  
		Last Modified: Wed, 16 Jul 2025 03:52:28 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:fab4c562bd13d4fe11cc47963461b4b2f197e38afa3be8a61b698b6319238f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17956644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c209b028cc287828f645bdd0dc227ee3dbc69f503f5bf1a4ad3a944252b78b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
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
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29116abe2cb7489bfe0d514003d7c4822eaf03d2b44e5f1c10c878a603eceb13`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 348.3 KB (348289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ceaafe79989c43b373a7e7780390f12740f15ad106a2c987605998f180cea`  
		Last Modified: Fri, 18 Jul 2025 07:36:43 GMT  
		Size: 7.5 KB (7498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9baf51ef7381285244300ec8288209b2b0dc82267a2c3547eb0644ce4c7948`  
		Last Modified: Fri, 18 Jul 2025 07:36:44 GMT  
		Size: 14.3 MB (14251735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:608fabfae5954b1485e44928f39c3844fbdc7de236202d87c4380838c748a018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 KB (303605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff983ccc8020f39b317500f82d9596ad6b4299338ecb828eaa0685950b57aa46`

```dockerfile
```

-	Layers:
	-	`sha256:090b4908e38667b8110e66242c7d88a6c27ba9f8dc2ebc126e04430fcaff531c`  
		Last Modified: Fri, 18 Jul 2025 09:52:30 GMT  
		Size: 285.3 KB (285255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e87f231dbdaabee2c8a7c7375c70ff7387e5d2387ed1a26033f1a9b77c0e427`  
		Last Modified: Fri, 18 Jul 2025 09:52:31 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:2d51d34db8630e03558db9a587a2060f7c5d6beb160750204de3b087d587e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18277874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55c87b036417ffbb8498391547041f3b5044576a9f341fc5b6871143cfd3c96`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 19 Apr 2025 03:51:58 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Sat, 19 Apr 2025 03:51:58 GMT
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
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb53384d292d3bbf4cbfc9faf53777b4d6315f18890ec37275f300b153c37e5`  
		Last Modified: Wed, 16 Jul 2025 04:56:39 GMT  
		Size: 353.7 KB (353711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58abe92c5c0f121648caef61e2c684f2a063962d487d10f810929f0786dabf0`  
		Last Modified: Wed, 16 Jul 2025 04:56:39 GMT  
		Size: 7.5 KB (7490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff39c1fe57dabbcacfaf9ec1708a337ef98383ad9691662c21bad39ba265205`  
		Last Modified: Wed, 16 Jul 2025 04:56:40 GMT  
		Size: 14.5 MB (14454541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:36331dcb06d168b65d8a73a0a7df4d01e108c2c2a92241f5795b48019dc8d705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 KB (303479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fff1ecb05ada26c62f140379e7d45f984feb7db3a7b6f50c5b57cf08a16a0c9`

```dockerfile
```

-	Layers:
	-	`sha256:1d400590d9b246c4109808d1a7f4b23d11eea2f6ed80fc64758c83e0c3063b1e`  
		Last Modified: Wed, 16 Jul 2025 06:52:44 GMT  
		Size: 285.2 KB (285201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687e3d1b5f80bf7b9a0883d23e514db8ce4fd7fcc3d581a8aef7a3cd13b85fa8`  
		Last Modified: Wed, 16 Jul 2025 06:52:45 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json
