## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:c65706cb6f36cd8ac2cf2ed7683e0bf3bc865019df07972ee011ffd875383235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:19f88d98fda45c99e4880b262cd4e36ebfdb9c88b628058102ab6059a0bc5c39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18624502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545582b7cdf47e597a961949ed4fc9613a3baccb84fb747ab85c31972b149dcc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:30:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 03 Aug 2023 21:19:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/welcome/index.html"
# Thu, 03 Aug 2023 21:19:28 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 03 Aug 2023 21:19:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b6690cd345f016b4795195f30e626a54644e66f95dc106fb72b44e009aad87433258cd091dc72d8ae357e1b2081d173da528d3f745fe5eb12286c20aa919a21c' ;; 		armhf)   binArch='armv6'; checksum='7911c1a7129550e8f712d6a9c8ec695e2ec8fa025109b360a94275fe50ae9b5039099464e02e30030e5349fa33106600d05623d60aa3bc1d520697c5b07db120' ;; 		armv7)   binArch='armv7'; checksum='fa8596887d1ea7652caea888511377c7c6ea4492889ec0ab1bf76c366f9e52247d41844bffc2f961cc4d06607d65982d8443651ef53f348c7d60f4fb98efbdb9' ;; 		aarch64) binArch='arm64'; checksum='48db86b764e23b892547741e30bf7c95561e804ec999c42fc1dac237ba8b0797abea76556e45c3b231f7acf303e3511507268c62f88076fd31891fc3a03564a7' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='049f0b0529e3e9334388fd099f03fa48a2f5fa2d17b00f46566117397a5468acbc392782abfe815f15f0ef6d8e3f1055bd1d275a927a42590782b83e01259a79' ;; 		s390x)   binArch='s390x'; checksum='3dadb51b4b1e03b884ba00a96fa7371b80aaf97f820bde7e15d2be745b02b91fa00b66422088bc94725ab86600206c458dc3a393e74f9192ef7e76d6fa54cb1f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.2/caddy_2.7.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 03 Aug 2023 21:19:30 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 03 Aug 2023 21:19:30 GMT
ENV XDG_DATA_HOME=/data
# Thu, 03 Aug 2023 21:19:30 GMT
LABEL org.opencontainers.image.version=v2.7.2
# Thu, 03 Aug 2023 21:19:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 03 Aug 2023 21:19:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 03 Aug 2023 21:19:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 03 Aug 2023 21:19:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 03 Aug 2023 21:19:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 03 Aug 2023 21:19:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 03 Aug 2023 21:19:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 03 Aug 2023 21:19:31 GMT
EXPOSE 80
# Thu, 03 Aug 2023 21:19:31 GMT
EXPOSE 443
# Thu, 03 Aug 2023 21:19:31 GMT
EXPOSE 443/udp
# Thu, 03 Aug 2023 21:19:31 GMT
EXPOSE 2019
# Thu, 03 Aug 2023 21:19:31 GMT
WORKDIR /srv
# Thu, 03 Aug 2023 21:19:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63974018b45d5f7b164c2773c4e021850d331db87debfbb86f651137d009b6e8`  
		Last Modified: Thu, 15 Jun 2023 05:30:55 GMT  
		Size: 350.8 KB (350845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ec8f60906a88707dba540f011464ae0cd721ee14cbc1c89cd7003289f890c2`  
		Last Modified: Thu, 03 Aug 2023 21:19:54 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d038dc6c45f5dc62a01d1739559dd23ba895a87c02d6b7db49cfa89099ce3279`  
		Last Modified: Thu, 03 Aug 2023 21:19:57 GMT  
		Size: 14.9 MB (14868275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:20567e1a6bebe3f25633565d0bff6246c016409c6d8e0165473cbcd28ec7afb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17685310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302d5c481e2c3ecbccb8cf06c724f4d4cd20d93aee79688e4d02a01f4e93c32a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:19:50 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 03 Aug 2023 21:49:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/welcome/index.html"
# Thu, 03 Aug 2023 21:49:13 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 03 Aug 2023 21:49:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b6690cd345f016b4795195f30e626a54644e66f95dc106fb72b44e009aad87433258cd091dc72d8ae357e1b2081d173da528d3f745fe5eb12286c20aa919a21c' ;; 		armhf)   binArch='armv6'; checksum='7911c1a7129550e8f712d6a9c8ec695e2ec8fa025109b360a94275fe50ae9b5039099464e02e30030e5349fa33106600d05623d60aa3bc1d520697c5b07db120' ;; 		armv7)   binArch='armv7'; checksum='fa8596887d1ea7652caea888511377c7c6ea4492889ec0ab1bf76c366f9e52247d41844bffc2f961cc4d06607d65982d8443651ef53f348c7d60f4fb98efbdb9' ;; 		aarch64) binArch='arm64'; checksum='48db86b764e23b892547741e30bf7c95561e804ec999c42fc1dac237ba8b0797abea76556e45c3b231f7acf303e3511507268c62f88076fd31891fc3a03564a7' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='049f0b0529e3e9334388fd099f03fa48a2f5fa2d17b00f46566117397a5468acbc392782abfe815f15f0ef6d8e3f1055bd1d275a927a42590782b83e01259a79' ;; 		s390x)   binArch='s390x'; checksum='3dadb51b4b1e03b884ba00a96fa7371b80aaf97f820bde7e15d2be745b02b91fa00b66422088bc94725ab86600206c458dc3a393e74f9192ef7e76d6fa54cb1f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.2/caddy_2.7.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 03 Aug 2023 21:49:16 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 03 Aug 2023 21:49:16 GMT
ENV XDG_DATA_HOME=/data
# Thu, 03 Aug 2023 21:49:16 GMT
LABEL org.opencontainers.image.version=v2.7.2
# Thu, 03 Aug 2023 21:49:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 03 Aug 2023 21:49:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 03 Aug 2023 21:49:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 03 Aug 2023 21:49:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 03 Aug 2023 21:49:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 03 Aug 2023 21:49:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 03 Aug 2023 21:49:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 03 Aug 2023 21:49:17 GMT
EXPOSE 80
# Thu, 03 Aug 2023 21:49:17 GMT
EXPOSE 443
# Thu, 03 Aug 2023 21:49:17 GMT
EXPOSE 443/udp
# Thu, 03 Aug 2023 21:49:17 GMT
EXPOSE 2019
# Thu, 03 Aug 2023 21:49:17 GMT
WORKDIR /srv
# Thu, 03 Aug 2023 21:49:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1307a8613ad92eee47b12de837dc212d252e41489fd7443b6f7df3af69fe79`  
		Last Modified: Wed, 14 Jun 2023 20:20:54 GMT  
		Size: 347.6 KB (347620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f4df12ce70b3a13e8cfe005d513d8d725cf6657fe7379b3b44e8e2aaea6445`  
		Last Modified: Thu, 03 Aug 2023 21:49:36 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96055b6e3dcd90cd5717e94f85371edd36b9bada09264f4ea5da53045dd8e348`  
		Last Modified: Thu, 03 Aug 2023 21:49:39 GMT  
		Size: 14.2 MB (14186830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7f04236a3404ab045af24f804fc352f7f52b8a7510176e98681717c717aaec68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17410878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177538ed18e541b0e13574dccfce4ba48f460df727af2d411a9b65998381d490`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:49:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 03 Aug 2023 21:57:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/welcome/index.html"
# Thu, 03 Aug 2023 21:57:18 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 03 Aug 2023 21:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b6690cd345f016b4795195f30e626a54644e66f95dc106fb72b44e009aad87433258cd091dc72d8ae357e1b2081d173da528d3f745fe5eb12286c20aa919a21c' ;; 		armhf)   binArch='armv6'; checksum='7911c1a7129550e8f712d6a9c8ec695e2ec8fa025109b360a94275fe50ae9b5039099464e02e30030e5349fa33106600d05623d60aa3bc1d520697c5b07db120' ;; 		armv7)   binArch='armv7'; checksum='fa8596887d1ea7652caea888511377c7c6ea4492889ec0ab1bf76c366f9e52247d41844bffc2f961cc4d06607d65982d8443651ef53f348c7d60f4fb98efbdb9' ;; 		aarch64) binArch='arm64'; checksum='48db86b764e23b892547741e30bf7c95561e804ec999c42fc1dac237ba8b0797abea76556e45c3b231f7acf303e3511507268c62f88076fd31891fc3a03564a7' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='049f0b0529e3e9334388fd099f03fa48a2f5fa2d17b00f46566117397a5468acbc392782abfe815f15f0ef6d8e3f1055bd1d275a927a42590782b83e01259a79' ;; 		s390x)   binArch='s390x'; checksum='3dadb51b4b1e03b884ba00a96fa7371b80aaf97f820bde7e15d2be745b02b91fa00b66422088bc94725ab86600206c458dc3a393e74f9192ef7e76d6fa54cb1f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.2/caddy_2.7.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 03 Aug 2023 21:57:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 03 Aug 2023 21:57:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 03 Aug 2023 21:57:21 GMT
LABEL org.opencontainers.image.version=v2.7.2
# Thu, 03 Aug 2023 21:57:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 03 Aug 2023 21:57:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 03 Aug 2023 21:57:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 03 Aug 2023 21:57:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 03 Aug 2023 21:57:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 03 Aug 2023 21:57:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 03 Aug 2023 21:57:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 03 Aug 2023 21:57:21 GMT
EXPOSE 80
# Thu, 03 Aug 2023 21:57:21 GMT
EXPOSE 443
# Thu, 03 Aug 2023 21:57:21 GMT
EXPOSE 443/udp
# Thu, 03 Aug 2023 21:57:21 GMT
EXPOSE 2019
# Thu, 03 Aug 2023 21:57:22 GMT
WORKDIR /srv
# Thu, 03 Aug 2023 21:57:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b11fd72724952a9dc9d91c238074f615906af72e1ae9b471d33adb92b4d1d9`  
		Last Modified: Thu, 15 Jun 2023 01:49:49 GMT  
		Size: 344.5 KB (344458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1215419211ea4f58b105a726335fcf12b387a1827e9acfafda56279e41a9cdb4`  
		Last Modified: Thu, 03 Aug 2023 21:57:45 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addf372ed13639d76eaa7de7afc94a0e93d442e57816aebbd36a6cae0e01e8d0`  
		Last Modified: Thu, 03 Aug 2023 21:57:48 GMT  
		Size: 14.2 MB (14160409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:222f959af1d2369295395b725184a2bc8c35da59615c18a04369bca89adb5c74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17322033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b141280160f778ddf83f36cd61b36db3f63f5549e65b9e432bfa4d5672f6fa8e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:37:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 03 Aug 2023 21:39:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/welcome/index.html"
# Thu, 03 Aug 2023 21:39:18 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 03 Aug 2023 21:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b6690cd345f016b4795195f30e626a54644e66f95dc106fb72b44e009aad87433258cd091dc72d8ae357e1b2081d173da528d3f745fe5eb12286c20aa919a21c' ;; 		armhf)   binArch='armv6'; checksum='7911c1a7129550e8f712d6a9c8ec695e2ec8fa025109b360a94275fe50ae9b5039099464e02e30030e5349fa33106600d05623d60aa3bc1d520697c5b07db120' ;; 		armv7)   binArch='armv7'; checksum='fa8596887d1ea7652caea888511377c7c6ea4492889ec0ab1bf76c366f9e52247d41844bffc2f961cc4d06607d65982d8443651ef53f348c7d60f4fb98efbdb9' ;; 		aarch64) binArch='arm64'; checksum='48db86b764e23b892547741e30bf7c95561e804ec999c42fc1dac237ba8b0797abea76556e45c3b231f7acf303e3511507268c62f88076fd31891fc3a03564a7' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='049f0b0529e3e9334388fd099f03fa48a2f5fa2d17b00f46566117397a5468acbc392782abfe815f15f0ef6d8e3f1055bd1d275a927a42590782b83e01259a79' ;; 		s390x)   binArch='s390x'; checksum='3dadb51b4b1e03b884ba00a96fa7371b80aaf97f820bde7e15d2be745b02b91fa00b66422088bc94725ab86600206c458dc3a393e74f9192ef7e76d6fa54cb1f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.2/caddy_2.7.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 03 Aug 2023 21:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 03 Aug 2023 21:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 03 Aug 2023 21:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.2
# Thu, 03 Aug 2023 21:39:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 03 Aug 2023 21:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 03 Aug 2023 21:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 03 Aug 2023 21:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 03 Aug 2023 21:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 03 Aug 2023 21:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 03 Aug 2023 21:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 03 Aug 2023 21:39:21 GMT
EXPOSE 80
# Thu, 03 Aug 2023 21:39:21 GMT
EXPOSE 443
# Thu, 03 Aug 2023 21:39:21 GMT
EXPOSE 443/udp
# Thu, 03 Aug 2023 21:39:21 GMT
EXPOSE 2019
# Thu, 03 Aug 2023 21:39:21 GMT
WORKDIR /srv
# Thu, 03 Aug 2023 21:39:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca8dc2b64d8698387b1ff7efd6d1d4a15073f57e2dfa6cd6c1501d6b6574fb`  
		Last Modified: Wed, 14 Jun 2023 22:37:44 GMT  
		Size: 360.6 KB (360650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2541b55ff26684c14fd3327fae00ecec33227c463052c5aee9b1e9c8e861a5df`  
		Last Modified: Thu, 03 Aug 2023 21:39:41 GMT  
		Size: 7.5 KB (7508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e238c4a0a49bc87100e8e7414769e559769c94de229334cb00ab94fc0379448d`  
		Last Modified: Thu, 03 Aug 2023 21:39:43 GMT  
		Size: 13.6 MB (13624624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8aef0cbb676dbb1e40ed8ce0b026f30ee3bc5f02cbb3035d7da5a150b31d5a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17020317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b5c402827d7a896ee934ffc366e22798625311f8247a67e2002a903791c7b5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:49 GMT
ADD file:694c636c0dd19fd01accbc189e4c1dc4d063952692c6e7eb26dce02a7adba833 in / 
# Thu, 15 Jun 2023 00:39:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:18:31 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 03 Aug 2023 21:16:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/welcome/index.html"
# Thu, 03 Aug 2023 21:16:29 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 03 Aug 2023 21:16:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b6690cd345f016b4795195f30e626a54644e66f95dc106fb72b44e009aad87433258cd091dc72d8ae357e1b2081d173da528d3f745fe5eb12286c20aa919a21c' ;; 		armhf)   binArch='armv6'; checksum='7911c1a7129550e8f712d6a9c8ec695e2ec8fa025109b360a94275fe50ae9b5039099464e02e30030e5349fa33106600d05623d60aa3bc1d520697c5b07db120' ;; 		armv7)   binArch='armv7'; checksum='fa8596887d1ea7652caea888511377c7c6ea4492889ec0ab1bf76c366f9e52247d41844bffc2f961cc4d06607d65982d8443651ef53f348c7d60f4fb98efbdb9' ;; 		aarch64) binArch='arm64'; checksum='48db86b764e23b892547741e30bf7c95561e804ec999c42fc1dac237ba8b0797abea76556e45c3b231f7acf303e3511507268c62f88076fd31891fc3a03564a7' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='049f0b0529e3e9334388fd099f03fa48a2f5fa2d17b00f46566117397a5468acbc392782abfe815f15f0ef6d8e3f1055bd1d275a927a42590782b83e01259a79' ;; 		s390x)   binArch='s390x'; checksum='3dadb51b4b1e03b884ba00a96fa7371b80aaf97f820bde7e15d2be745b02b91fa00b66422088bc94725ab86600206c458dc3a393e74f9192ef7e76d6fa54cb1f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.2/caddy_2.7.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 03 Aug 2023 21:16:36 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 03 Aug 2023 21:16:37 GMT
ENV XDG_DATA_HOME=/data
# Thu, 03 Aug 2023 21:16:38 GMT
LABEL org.opencontainers.image.version=v2.7.2
# Thu, 03 Aug 2023 21:16:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 03 Aug 2023 21:16:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 03 Aug 2023 21:16:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 03 Aug 2023 21:16:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 03 Aug 2023 21:16:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 03 Aug 2023 21:16:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 03 Aug 2023 21:16:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 03 Aug 2023 21:16:47 GMT
EXPOSE 80
# Thu, 03 Aug 2023 21:16:47 GMT
EXPOSE 443
# Thu, 03 Aug 2023 21:16:48 GMT
EXPOSE 443/udp
# Thu, 03 Aug 2023 21:16:50 GMT
EXPOSE 2019
# Thu, 03 Aug 2023 21:16:52 GMT
WORKDIR /srv
# Thu, 03 Aug 2023 21:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ffa4a466dbb8eebd7e7f25590a9df12390de9016abf82279c29c9a64aa76491a`  
		Last Modified: Thu, 15 Jun 2023 00:40:26 GMT  
		Size: 3.3 MB (3344781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1814cc276fc1ae018ae6108f9956a25fd03dc10b300e8a2d67bd381b5cbb691`  
		Last Modified: Thu, 15 Jun 2023 01:19:17 GMT  
		Size: 362.2 KB (362174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5570f5a562715ef06785c9056cf9a0afa7bceb0d32f8cad2b5a75c29e72a9c81`  
		Last Modified: Thu, 03 Aug 2023 21:17:36 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449f5d02ad5959585b0d940d332042389611ab9f17c117e9009de8d9e3a3113b`  
		Last Modified: Thu, 03 Aug 2023 21:17:39 GMT  
		Size: 13.3 MB (13305857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5855a7738bf1cfb6f342a5c2c652f4e85a5be5b6d9c37671cfc3057fe9fcefc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17980131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f62ded8147140e561a49cc33c44b7fb036d785228dd0b097992db0015e466`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Fri, 16 Jun 2023 15:41:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 03 Aug 2023 21:41:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/welcome/index.html"
# Thu, 03 Aug 2023 21:41:41 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 03 Aug 2023 21:41:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b6690cd345f016b4795195f30e626a54644e66f95dc106fb72b44e009aad87433258cd091dc72d8ae357e1b2081d173da528d3f745fe5eb12286c20aa919a21c' ;; 		armhf)   binArch='armv6'; checksum='7911c1a7129550e8f712d6a9c8ec695e2ec8fa025109b360a94275fe50ae9b5039099464e02e30030e5349fa33106600d05623d60aa3bc1d520697c5b07db120' ;; 		armv7)   binArch='armv7'; checksum='fa8596887d1ea7652caea888511377c7c6ea4492889ec0ab1bf76c366f9e52247d41844bffc2f961cc4d06607d65982d8443651ef53f348c7d60f4fb98efbdb9' ;; 		aarch64) binArch='arm64'; checksum='48db86b764e23b892547741e30bf7c95561e804ec999c42fc1dac237ba8b0797abea76556e45c3b231f7acf303e3511507268c62f88076fd31891fc3a03564a7' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='049f0b0529e3e9334388fd099f03fa48a2f5fa2d17b00f46566117397a5468acbc392782abfe815f15f0ef6d8e3f1055bd1d275a927a42590782b83e01259a79' ;; 		s390x)   binArch='s390x'; checksum='3dadb51b4b1e03b884ba00a96fa7371b80aaf97f820bde7e15d2be745b02b91fa00b66422088bc94725ab86600206c458dc3a393e74f9192ef7e76d6fa54cb1f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.2/caddy_2.7.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 03 Aug 2023 21:41:56 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 03 Aug 2023 21:41:57 GMT
ENV XDG_DATA_HOME=/data
# Thu, 03 Aug 2023 21:41:58 GMT
LABEL org.opencontainers.image.version=v2.7.2
# Thu, 03 Aug 2023 21:41:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 03 Aug 2023 21:42:00 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 03 Aug 2023 21:42:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 03 Aug 2023 21:42:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 03 Aug 2023 21:42:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 03 Aug 2023 21:42:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 03 Aug 2023 21:42:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 03 Aug 2023 21:42:04 GMT
EXPOSE 80
# Thu, 03 Aug 2023 21:42:05 GMT
EXPOSE 443
# Thu, 03 Aug 2023 21:42:06 GMT
EXPOSE 443/udp
# Thu, 03 Aug 2023 21:42:07 GMT
EXPOSE 2019
# Thu, 03 Aug 2023 21:42:07 GMT
WORKDIR /srv
# Thu, 03 Aug 2023 21:42:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abc06373f1c925869603487727505d0e07b5c8496ea8c9d3cedb1d81763ab26`  
		Last Modified: Fri, 16 Jun 2023 15:42:21 GMT  
		Size: 354.9 KB (354946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a69320bf77cd36a2ab083b635ca6acc3d35cf18f44924865a635848fb38e606`  
		Last Modified: Thu, 03 Aug 2023 21:42:49 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408b13cba2a8a565d408273b22c03146867cb9777231ad69decced11d373aa35`  
		Last Modified: Thu, 03 Aug 2023 21:42:51 GMT  
		Size: 14.4 MB (14404181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
