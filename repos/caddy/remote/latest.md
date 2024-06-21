## `caddy:latest`

```console
$ docker pull caddy@sha256:83d99edad2f0ac5e52068e065e42bd40c4ff7465a8f582482566c9d48350663a
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
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:de7100f2dc60d933ba28a915c8d788f3ce89c7baf14c4b9c5a6fd67549bae7a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18627619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accd318080c538106641ab06f8383ef9979ad7919004ae6a55bced90f39c35f8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ada5eb3540e4dca0204132c9b0c5ea6593e286b86258eb74e181c7fac06ad5`  
		Last Modified: Thu, 20 Jun 2024 20:56:48 GMT  
		Size: 357.4 KB (357359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b78b6bd1c817222ea54d7f525925db43e6e215d5f92a0fb5b6e0962cfb1275`  
		Last Modified: Thu, 20 Jun 2024 20:56:48 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14de6039f1505f64546cf32b38e20eb0d6dfc3ffcf73595f2507d061bfff021f`  
		Last Modified: Thu, 20 Jun 2024 20:56:48 GMT  
		Size: 14.6 MB (14638935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:9404ddc071773075e0c61ec7e45538d1e6d0270d0ce1357fd7f8458635ab090d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 KB (281845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51adcda97fe5558b194ecbcf85e9c6ac9c58ffc7b5d88a42a9fdc51d02ba88eb`

```dockerfile
```

-	Layers:
	-	`sha256:712ae6b6ed31482d27bf508aa484f05932084eb22c6fe0b5f3aaca47b49a1c23`  
		Last Modified: Thu, 20 Jun 2024 20:56:48 GMT  
		Size: 263.8 KB (263815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4b5ec6e66c9725423e518b3656395df1065475086e7b7f33eb3de35fbb768a`  
		Last Modified: Thu, 20 Jun 2024 20:56:48 GMT  
		Size: 18.0 KB (18030 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cf03c28b9a2d265bd4f8b3db5dc968255e08c5db466a1a6456659ae457c0fd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17498169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb194a2567e047b786408e953ad6982305d105ec7b5d7a631b55eee3ed7d8706`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78cee73483197c6198a84d5e9e609b36b05cda0ffd573246d300d3ea06affd2`  
		Last Modified: Fri, 21 Jun 2024 05:20:13 GMT  
		Size: 357.7 KB (357698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f02705521644f3e5b02ddabf6f12c6c6d61cc55b84786f02ff9f07c0a711442`  
		Last Modified: Fri, 21 Jun 2024 05:20:12 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f422744d7cf2576e3485758a2a3f4a020c0003a9e6889bd4958b004c1c7108d`  
		Last Modified: Fri, 21 Jun 2024 05:20:13 GMT  
		Size: 13.8 MB (13765833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:c4e1523511a250bcecf015b4193307897d61b669db9be5f1203ff1f96f2d71a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71058f83df2bd64602e11004c02d0bcfa8a224d44f86a84a0a616d5d753d0971`

```dockerfile
```

-	Layers:
	-	`sha256:e6eb26abf625c0e2b20c9df07b94a2683944d3127199647949c179b972b4a75b`  
		Last Modified: Fri, 21 Jun 2024 05:20:12 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:58643f5673132d6980223d5e1fee63aad4d5874a7badc23eb0e9056b770f8d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17196242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a39956332f30be2b2a64aac38ec51d32faf685cdeb1207276d701eb72afaa4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd0f6f3b1ad24f929c3cefcf6c07191bf1e6a97669a8678187561dc322750a`  
		Last Modified: Fri, 21 Jun 2024 05:11:19 GMT  
		Size: 354.1 KB (354053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0086cb12674a386c85e4871956cbb76cabdd5a973164cdc64e550cf1125e3d79`  
		Last Modified: Fri, 21 Jun 2024 05:11:19 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dd9d7271814b03c3dc889c9b06ec365115c2c7088ffcb466e2808e41e2e336`  
		Last Modified: Fri, 21 Jun 2024 05:11:19 GMT  
		Size: 13.7 MB (13739852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:3c24dad3d181ffc36a6de7e98c1eab6c6aa719ae6733275a908a0272827ab9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 KB (282041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7298397e5af54dcb16e481ec95df0513b6f90d434ba929ff07f23f029ede364`

```dockerfile
```

-	Layers:
	-	`sha256:a3fa806da0197762c5a761be797fe993e21e5a7196e24cbd3bc21ca84798d002`  
		Last Modified: Fri, 21 Jun 2024 05:11:19 GMT  
		Size: 263.9 KB (263883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f8f19ac28fb586fef161c7c6915fdacb1e35566caa1b6d890d4c54af4a6188`  
		Last Modified: Fri, 21 Jun 2024 05:11:19 GMT  
		Size: 18.2 KB (18158 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:48912b36bbb0a7fe802624f04d369bd93f3a1b54b64170ab1bc57be73d657aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18016508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a3686fbe0f0cd9df6605ba9ee7de425b9e27cd694aa97be91fa37cc17b5f07`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e0558e566fe6e69138a492c4e983f766f5ad6384605531dc55940332bf1565`  
		Last Modified: Fri, 21 Jun 2024 07:02:52 GMT  
		Size: 369.2 KB (369156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11342c0f8ed29f6c8fcd9309a03773c2b1e215e67ecc736a321360c6de018aa4`  
		Last Modified: Fri, 21 Jun 2024 07:02:52 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb518111bbafbf554d12702c0cfd4e5b61c3c5c4ac74026b374ddc31d8d0eaf`  
		Last Modified: Fri, 21 Jun 2024 07:02:52 GMT  
		Size: 13.6 MB (13551068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:312145bd8db1db7ec992ebccefbc415d570acef956288c89f3157055d6f0be69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 KB (282297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202fe706dc089fe0a25258b1ebe73b3daaa576f9faab458dcdef5f64e451e778`

```dockerfile
```

-	Layers:
	-	`sha256:6f560c73c84a4ba79a8aaf2814abf403cc532e3f69cac0a7a8922e1045847907`  
		Last Modified: Fri, 21 Jun 2024 07:02:52 GMT  
		Size: 263.9 KB (263919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c108e85a08f9dd053bb31928bf9d93b121608593adb70298e920d9085ab77aa`  
		Last Modified: Fri, 21 Jun 2024 07:02:52 GMT  
		Size: 18.4 KB (18378 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:a06b4b216c0f2c16d44f6ca4b46489f928370679b5d637ef2ba17f604e9a81c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63a12357ee75ed2b86ebd2281c21d79f87af4286dedc5fcf82e69affa4e1639`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b703e5ec1b293446d02f4eb313f388a0ea66f7b9a459db787aefdcaeda02f2d`  
		Last Modified: Fri, 21 Jun 2024 03:17:55 GMT  
		Size: 370.4 KB (370399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8e3c71bfa96822e737350baa7eb63960ed54378104b205733f547da5755568`  
		Last Modified: Fri, 21 Jun 2024 03:17:55 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3115ebefaaa67ad1259183d027a7831bf2ecdda0858e36658c7570d6d2d009`  
		Last Modified: Fri, 21 Jun 2024 03:17:56 GMT  
		Size: 13.3 MB (13292037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:16aab166fc45a2c944fc324fc0115efcf8afe1f4240c1a465ae9c434492640ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 KB (280014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04083f0b7116138c7f9addbe81913c0ab2e4d4595e424b53e61645f8b33f2633`

```dockerfile
```

-	Layers:
	-	`sha256:e6cff693d8467992a13b730bb4e97f84efc148054aeb2b6deab761528ef67099`  
		Last Modified: Fri, 21 Jun 2024 03:17:55 GMT  
		Size: 261.9 KB (261919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2aabf902816261ef110fe9fac72351f0873aa88810782de156742bcb90ba40d`  
		Last Modified: Fri, 21 Jun 2024 03:17:55 GMT  
		Size: 18.1 KB (18095 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; riscv64

```console
$ docker pull caddy@sha256:f2a7d22cd9ad3194ec80543d6b4aacf5aaa0104ca9e0cb5497e4aa2dcf4f2d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17595896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b67e8f4f94acfc3e511199e17b162e48ac518619b0827b6caeb06c4ceaf25a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3b03c0bbdde17ee418794d5667c13b42f0ef3103defe5489b6ac3f906f58f9`  
		Last Modified: Wed, 05 Jun 2024 01:10:14 GMT  
		Size: 360.8 KB (360843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc68b6bd9de647eade60bdcdf9a271da74b9b53efc69fdb8bf14bf0cfa678fa`  
		Last Modified: Wed, 05 Jun 2024 01:10:14 GMT  
		Size: 7.5 KB (7451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d872ad35f4c16c23c7bc479b62ddd8f2efd829650bcd842b08329a341a780e10`  
		Last Modified: Wed, 05 Jun 2024 01:10:16 GMT  
		Size: 13.9 MB (13859010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:bb3f2794789709528e7fe48a28351f4790137c9e42e92de44fab8837f4a43fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 KB (279961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f37590f1b21ac54f4417878a2b98fee1471dd26d9f1273c66823849dc589819`

```dockerfile
```

-	Layers:
	-	`sha256:f57985fb31edb1383be05f85c26a3ad03827f44d84416d020fe1fbfd95e6a6ea`  
		Last Modified: Wed, 05 Jun 2024 01:10:19 GMT  
		Size: 261.9 KB (261914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f207c2c87cf61d67e60ca3825931210f2208879c8308ce42ca6fa22f528205`  
		Last Modified: Wed, 05 Jun 2024 01:10:18 GMT  
		Size: 18.0 KB (18047 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:e624007118a1fd782697fa129da1cfb1e96787b275a66d46b659cf7cb6a3db27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17990345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09130ba97d5fbe11df684f5405f56939353a04d4ff6f314cc5d940010c34fe8b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4364eced6a2ecc7e0174509146c54368a869e8cb08a79722013dbf70cbc767e5`  
		Last Modified: Fri, 21 Jun 2024 06:06:33 GMT  
		Size: 364.9 KB (364880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531c4457c073eaaa81cb341b3eec51d559f1ef9e45af86eb029bb8c06ef2a1ec`  
		Last Modified: Fri, 21 Jun 2024 06:06:32 GMT  
		Size: 7.4 KB (7449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886c466c34bc3799b91a7b6b9062ce09ce00428222a4724c6e6a5bc622bae3e9`  
		Last Modified: Fri, 21 Jun 2024 06:06:33 GMT  
		Size: 14.2 MB (14156128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:c8325ca58db9e7f822eaef69061565eb4abc97cc50f1319a4ca20603e001ed7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 KB (279890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee936be165540eaa3bf8285b2fd2fd564a553c2c7a580c8aa788a5f5560d7536`

```dockerfile
```

-	Layers:
	-	`sha256:a7b2b774e8d7fb45a8f7c3b6ba3fdfd094fc8d636bdb56722e6e40531977ede5`  
		Last Modified: Fri, 21 Jun 2024 06:06:32 GMT  
		Size: 261.9 KB (261861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65c4393669973d8ace73ea1d2c6a68934aa63a616baa8987fd8310e4f653920`  
		Last Modified: Fri, 21 Jun 2024 06:06:32 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.20348.2527; amd64

```console
$ docker pull caddy@sha256:51147c928efe77a4b4099cc27d06e7db18a5721176cec3e20105fa142c09b25f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2134147349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560d413e8be5e8e31f17540371afc251b4e57a43c55063617d40892e4473e898`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:05:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:05:56 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Jun 2024 18:05:57 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 12 Jun 2024 18:06:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Jun 2024 18:06:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Jun 2024 18:06:09 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Jun 2024 18:06:10 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Wed, 12 Jun 2024 18:06:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Jun 2024 18:06:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Jun 2024 18:06:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Jun 2024 18:06:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Jun 2024 18:06:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Jun 2024 18:06:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Jun 2024 18:06:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Jun 2024 18:06:17 GMT
EXPOSE 80
# Wed, 12 Jun 2024 18:06:18 GMT
EXPOSE 443
# Wed, 12 Jun 2024 18:06:19 GMT
EXPOSE 443/udp
# Wed, 12 Jun 2024 18:06:20 GMT
EXPOSE 2019
# Wed, 12 Jun 2024 18:06:25 GMT
RUN caddy version
# Wed, 12 Jun 2024 18:06:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e545a2fc5d3075adc1d6a745e6b2672175e0edb524c41741a015287407c7cf`  
		Last Modified: Wed, 12 Jun 2024 18:06:37 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5722a8f2906463d5d6778f51a612a3ffbf427a41451e46844f664f0c9b994f4`  
		Last Modified: Wed, 12 Jun 2024 18:06:38 GMT  
		Size: 357.8 KB (357844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f62cb99602a812ea5ca60f8dd34b8a72c163c7f5943990bf844c94439b09fe8`  
		Last Modified: Wed, 12 Jun 2024 18:06:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86705d66327fb336a3dc0795058217a72a83959f56078c243bfc567de39ec9c6`  
		Last Modified: Wed, 12 Jun 2024 18:06:39 GMT  
		Size: 15.3 MB (15251871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee45ca65f4b3ff2e1f52cd7fde719a06fbfff1d0836be6ebe0bdaa6d0e745aa`  
		Last Modified: Wed, 12 Jun 2024 18:06:37 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a739cfe2c04e879f40533d04fba63f9fd68ace6361ba73ba2effcac3bafa690`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a29797e301bc36a0546ef4e042054bf93256cb3888578aca83e018bc77368b`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988d07a5554acc0d603c5e058d487da8edc7ebfe95eb1232f07ab7ea0366280`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ef2c93189ec1bc02ecce2f44a4bf9a255a7f320782e6340eea391895f3f303`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb0ade3e94278b0df4f52923ad65406d5fc4a000aa97049fe7db8387c6e6076`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aa98437e0f860e5163d5a8368019dc14dd3fb53a791c27738dc4b7a16a0b13`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eaecae7891029f0ee7757e03a7b4b74cabb083fdb028d17cc43ee464829794`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf00901eaa304c584a21dbe8a70c3b80a6b0c6fde285f57db9c47d1f4d66f30`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09121d08b868a076afba48cc26857cdc4410e5fbab4452d138a5ba00e10c8a61`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095968204cbc805ee64ab0fac270bd2ed576ea57cbd7a82b338ebbe689d31538`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672972d9699e689d8896c7a21c5dfaa9ee3a2b58b871a9df0c18e56b7f4ff08`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f435a4624de5ceec43b71f0c3e6372a1ab64e41e906b8fa18483115027e98d3`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf1139230913bc0093c2a4c3328ca2de4798f7246b53faab1f5f52dfea039c3`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad623230e152a65511f5223dbfc568f8236a7857f4b4d15edf79c0a7181a780`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 337.1 KB (337086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91574d61749f6b283be1b9468a9fb0b557b1872546a8b307275bcc8dca2c912e`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5936; amd64

```console
$ docker pull caddy@sha256:a5c00013b5cfa9cd49996e182bd9f5a85abed2a8d0d74f1dc61bde309ee3cfcd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2236778768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e90a84406eff7717cfb437b2d988f4c7f58f428f885806782315bcf6942141`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:14:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:15:50 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Jun 2024 18:15:50 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 12 Jun 2024 18:16:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Jun 2024 18:16:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Jun 2024 18:16:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Jun 2024 18:16:15 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Wed, 12 Jun 2024 18:16:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Jun 2024 18:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Jun 2024 18:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Jun 2024 18:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Jun 2024 18:16:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Jun 2024 18:16:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Jun 2024 18:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Jun 2024 18:16:20 GMT
EXPOSE 80
# Wed, 12 Jun 2024 18:16:21 GMT
EXPOSE 443
# Wed, 12 Jun 2024 18:16:21 GMT
EXPOSE 443/udp
# Wed, 12 Jun 2024 18:16:22 GMT
EXPOSE 2019
# Wed, 12 Jun 2024 18:16:39 GMT
RUN caddy version
# Wed, 12 Jun 2024 18:16:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e451e2214cb46d91701a5efdeec888aa7d4bb1abd886b3ea1ab94b6f5c77434`  
		Last Modified: Wed, 12 Jun 2024 18:16:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a5d9b53c9cd647493df39a9e4f81260cf4cfd352c829b59120980dbda419`  
		Last Modified: Wed, 12 Jun 2024 18:16:45 GMT  
		Size: 486.0 KB (486040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fee2e008257210ce03b0310c3fd46ad00de102869b57f0c49d72b851b5e1cff`  
		Last Modified: Wed, 12 Jun 2024 18:16:45 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a1730fab799de2f3376ad39d417775e7d729f9eab97fb0ee5807e57f82b57f`  
		Last Modified: Wed, 12 Jun 2024 18:16:46 GMT  
		Size: 15.3 MB (15253086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c97e474161736db0a5fa6376934e5f1a87063b5a6b5c29a1538e57d31f2d5d`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351ff70de2baa55d09f0fd436e5796ce05ac94304b5a49adaf5356738bcdb3eb`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505357b6cd3601e73aa7b4bea94c23fae309eca2582315471ec7a37f40ccd097`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d13d827172c8dd1a368ba470e93fcac50603791ad749be0b000394b2a6cc9d`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815a80b170874260ad13f80b080aea2b92f8b70e0d700f7df5c6152d6e5073d3`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e67694cd431f519e9a418acf8118968562ce07d38bd1cc6a8c23c0e6b3855c`  
		Last Modified: Wed, 12 Jun 2024 18:16:43 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c65a7507f079159e33c8113457614026bef357e6c79e264edf07ac5ec619212`  
		Last Modified: Wed, 12 Jun 2024 18:16:43 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231d80673520560b892fd3c9af92d9762023cf7ba67240380ca0ad8480e4761e`  
		Last Modified: Wed, 12 Jun 2024 18:16:43 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96693e4ec5c88c00f528b2e4cc30a6d25825d886b4f6cc8533ca34d772028262`  
		Last Modified: Wed, 12 Jun 2024 18:16:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60bb90d75c3d81b23efab09d3ff3a10b79c44ce139cad2e8c16b3981c37df3f`  
		Last Modified: Wed, 12 Jun 2024 18:16:42 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f4729482dc6a862c6da3ad00f05b6ee5819cb96c72fe579a3f347231c68cd`  
		Last Modified: Wed, 12 Jun 2024 18:16:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab02387e2baa16a12f15698e549a0767d32017af6314c0f6971ca06845a744f`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb07b0c0cca090fa9ab548d7b5bf0809605f6d7938939e2e50757041425e94`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289563f0fb9ba9caf2a30b6a7fd4221f28071a6ad712056531bb8e32b8cd1695`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcda06e9916af1f402738739c5ae633f9b3adc283ca2dd8772744d857b0867f`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 336.4 KB (336380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ec8747b8e7791d503f3e814ec490ec965b506aa5d9b24f319e43bd0f16a0b9`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
