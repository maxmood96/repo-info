<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-builder-windowsservercore-ltsc2022`](#caddy2-builder-windowsservercore-ltsc2022)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2-windowsservercore-ltsc2022`](#caddy2-windowsservercore-ltsc2022)
-	[`caddy:2.7`](#caddy27)
-	[`caddy:2.7-alpine`](#caddy27-alpine)
-	[`caddy:2.7-builder`](#caddy27-builder)
-	[`caddy:2.7-builder-alpine`](#caddy27-builder-alpine)
-	[`caddy:2.7-builder-windowsservercore-1809`](#caddy27-builder-windowsservercore-1809)
-	[`caddy:2.7-builder-windowsservercore-ltsc2022`](#caddy27-builder-windowsservercore-ltsc2022)
-	[`caddy:2.7-windowsservercore`](#caddy27-windowsservercore)
-	[`caddy:2.7-windowsservercore-1809`](#caddy27-windowsservercore-1809)
-	[`caddy:2.7-windowsservercore-ltsc2022`](#caddy27-windowsservercore-ltsc2022)
-	[`caddy:2.7.5`](#caddy275)
-	[`caddy:2.7.5-alpine`](#caddy275-alpine)
-	[`caddy:2.7.5-builder`](#caddy275-builder)
-	[`caddy:2.7.5-builder-alpine`](#caddy275-builder-alpine)
-	[`caddy:2.7.5-builder-windowsservercore-1809`](#caddy275-builder-windowsservercore-1809)
-	[`caddy:2.7.5-builder-windowsservercore-ltsc2022`](#caddy275-builder-windowsservercore-ltsc2022)
-	[`caddy:2.7.5-windowsservercore`](#caddy275-windowsservercore)
-	[`caddy:2.7.5-windowsservercore-1809`](#caddy275-windowsservercore-1809)
-	[`caddy:2.7.5-windowsservercore-ltsc2022`](#caddy275-windowsservercore-ltsc2022)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-1809`](#caddybuilder-windowsservercore-1809)
-	[`caddy:builder-windowsservercore-ltsc2022`](#caddybuilder-windowsservercore-ltsc2022)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)
-	[`caddy:windowsservercore-ltsc2022`](#caddywindowsservercore-ltsc2022)

## `caddy:2`

```console
$ docker pull caddy@sha256:db7fa54ce8d507a6c22cdf0ee9cd5229747d8f552c83912b0c5427b92e6e271c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:aaa9d8750860e5b886fab8c4da6842782ec2eb2e963e6d48ad59657fadd9a6aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e21ab2b0efc5ac0207c16134ac96b3779212c692cde05a24f73a68fec756a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:43:13 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:43:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:19:15 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:19:17 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:19:18 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:19:19 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:19:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be51084fb891c6796079e693b73f6f882266a5e66211344173031e2b0c8ffd`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 350.8 KB (350826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d867aa37ac50364bf4082dc48c7d4e1b88ead3164d47855e1bbc2ef3678cfc`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a4bfabc0b0dc6924b7d8aad02805798c86ada09d9d11861f29ed76915f758`  
		Last Modified: Thu, 12 Oct 2023 18:19:43 GMT  
		Size: 14.7 MB (14713998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:be2cb3ef217d514df988a7fef43bc11cf8267f3c3eea319a82c6c4c2985cd7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17422254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375c06eba744fadf74e23a036a6af05a75573760968f9d65a405d7401973be3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:59:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 21:59:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 01:39:17 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:39:22 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:39:22 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 01:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1018057a600163b1c1b92c21ade975c631b2f8ccde66d524cfe0ecdac8e1920d`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 347.6 KB (347613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec54680cbf2cb1a25285c82a7888498ab47d03a68db200a160d7162325a5be19`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38012b56d72a4a2c2a42ed660476530218852cf8953587cb803fab0cf7de99c3`  
		Last Modified: Thu, 12 Oct 2023 01:39:46 GMT  
		Size: 13.9 MB (13921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cc67ef274e0b09f75c4adf46397b2b796c00d9d014d1312d53bc3e16fa763bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b853d3cd7e1ec8e5fdb884e061c15e6da29f25d0954bf803f08625dc542bf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:19:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 23:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:03:38 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:03:42 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:03:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66901ba48d0ee53cd827f4eb2cfd8b049cebba8c3d307b69760e1be917f69476`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 344.4 KB (344448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeb3f6febb36993d8a51ad919784fd152aab5f6e17fe00d579916f32e42911`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00371969ebc6f50beb432e93f29b2658ffdbf2de985784e17b0a8e696970a7d`  
		Last Modified: Thu, 12 Oct 2023 18:04:03 GMT  
		Size: 13.9 MB (13903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c5cdeee3505159e6a4ebd367b13f1a6bb32d424327be8ee4a3e09734c5cf63d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6797cb1033afffac8c55f0ee0f0dd9f60e58dc19ef1edc5852606eced4c793b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:16:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 01:16:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 19:45:02 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 80
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 19:45:05 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 19:45:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f21cb0286edf1f5fefb4a859b414a446bb81baa9e8901fc8f4eca55a43aeeec`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 360.6 KB (360643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444b3f9419d06a4b77a65935a3b1c6e657c607bcfb9e3bd1abebe57eae36e6a`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e60671cdfd4ec2cb64a788cecf65bb2166ba5bf3e7bba029ccf0c8c0dbeb3`  
		Last Modified: Thu, 12 Oct 2023 19:45:30 GMT  
		Size: 13.6 MB (13573811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:65084a14a1557b92af5b8ba6fcba9a7a710ed5caef1e2310f9622166608c9531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba45deaa04c3feac6474c22204ac6f5ebc380b331ff7d585ecd196284459b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:17:03 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 02:17:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Fri, 29 Sep 2023 02:17:06 GMT
ENV CADDY_VERSION=v2.7.4
# Fri, 29 Sep 2023 02:17:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 29 Sep 2023 02:17:13 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 29 Sep 2023 02:17:14 GMT
ENV XDG_DATA_HOME=/data
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 29 Sep 2023 02:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 29 Sep 2023 02:17:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 443
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 443/udp
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 2019
# Fri, 29 Sep 2023 02:17:24 GMT
WORKDIR /srv
# Fri, 29 Sep 2023 02:17:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa65cea7f5d70d1e203b851e43ad676e92f28c930ad32b6691e84ff9b5cda87`  
		Last Modified: Fri, 29 Sep 2023 02:18:03 GMT  
		Size: 362.2 KB (362182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7089a1d537371e29a65d106f43b45f2a0367d4d1db0eb7d6b7099f8ba05645`  
		Last Modified: Fri, 29 Sep 2023 02:18:01 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93ab741fa6270144ea59d6a5fa3c4138286a569f246fdccd829b317b051f3a`  
		Last Modified: Fri, 29 Sep 2023 02:18:05 GMT  
		Size: 13.2 MB (13228998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:9e13bd2b56147eecc80f1fe1710e4350ea63d5edfb389fa89e2c6de06c08593a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17721238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f0101e0f893afb763d99b2050dbf4d68a44aae29785af6c05af5a552b0c1a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:19:38 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:19:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 28 Sep 2023 22:19:39 GMT
ENV CADDY_VERSION=v2.7.4
# Thu, 28 Sep 2023 22:19:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_DATA_HOME=/data
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 80
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443/udp
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 2019
# Thu, 28 Sep 2023 22:19:44 GMT
WORKDIR /srv
# Thu, 28 Sep 2023 22:19:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3df874173df47ad0bd0ef67b8ee598c77921810d84a67fd2984c4f8151c91`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a69c42a5c7fc6d73c00c7f6eb68522f3881aae55db4f85a8400e83b678b181`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793016dc78c9794c627c07afcd2fb34af4ee470ee7fef1a1596eff0c59ba6659`  
		Last Modified: Thu, 28 Sep 2023 22:20:16 GMT  
		Size: 14.1 MB (14143684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:0157ce2e3977145c950dc562b339351cd37d06abe9ac8bf36b04b1b2f8ce6104
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
$ docker pull caddy@sha256:aaa9d8750860e5b886fab8c4da6842782ec2eb2e963e6d48ad59657fadd9a6aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e21ab2b0efc5ac0207c16134ac96b3779212c692cde05a24f73a68fec756a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:43:13 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:43:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:19:15 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:19:17 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:19:18 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:19:19 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:19:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be51084fb891c6796079e693b73f6f882266a5e66211344173031e2b0c8ffd`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 350.8 KB (350826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d867aa37ac50364bf4082dc48c7d4e1b88ead3164d47855e1bbc2ef3678cfc`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a4bfabc0b0dc6924b7d8aad02805798c86ada09d9d11861f29ed76915f758`  
		Last Modified: Thu, 12 Oct 2023 18:19:43 GMT  
		Size: 14.7 MB (14713998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:be2cb3ef217d514df988a7fef43bc11cf8267f3c3eea319a82c6c4c2985cd7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17422254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375c06eba744fadf74e23a036a6af05a75573760968f9d65a405d7401973be3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:59:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 21:59:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 01:39:17 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:39:22 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:39:22 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 01:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1018057a600163b1c1b92c21ade975c631b2f8ccde66d524cfe0ecdac8e1920d`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 347.6 KB (347613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec54680cbf2cb1a25285c82a7888498ab47d03a68db200a160d7162325a5be19`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38012b56d72a4a2c2a42ed660476530218852cf8953587cb803fab0cf7de99c3`  
		Last Modified: Thu, 12 Oct 2023 01:39:46 GMT  
		Size: 13.9 MB (13921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cc67ef274e0b09f75c4adf46397b2b796c00d9d014d1312d53bc3e16fa763bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b853d3cd7e1ec8e5fdb884e061c15e6da29f25d0954bf803f08625dc542bf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:19:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 23:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:03:38 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:03:42 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:03:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66901ba48d0ee53cd827f4eb2cfd8b049cebba8c3d307b69760e1be917f69476`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 344.4 KB (344448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeb3f6febb36993d8a51ad919784fd152aab5f6e17fe00d579916f32e42911`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00371969ebc6f50beb432e93f29b2658ffdbf2de985784e17b0a8e696970a7d`  
		Last Modified: Thu, 12 Oct 2023 18:04:03 GMT  
		Size: 13.9 MB (13903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c5cdeee3505159e6a4ebd367b13f1a6bb32d424327be8ee4a3e09734c5cf63d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6797cb1033afffac8c55f0ee0f0dd9f60e58dc19ef1edc5852606eced4c793b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:16:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 01:16:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 19:45:02 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 80
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 19:45:05 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 19:45:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f21cb0286edf1f5fefb4a859b414a446bb81baa9e8901fc8f4eca55a43aeeec`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 360.6 KB (360643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444b3f9419d06a4b77a65935a3b1c6e657c607bcfb9e3bd1abebe57eae36e6a`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e60671cdfd4ec2cb64a788cecf65bb2166ba5bf3e7bba029ccf0c8c0dbeb3`  
		Last Modified: Thu, 12 Oct 2023 19:45:30 GMT  
		Size: 13.6 MB (13573811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:65084a14a1557b92af5b8ba6fcba9a7a710ed5caef1e2310f9622166608c9531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba45deaa04c3feac6474c22204ac6f5ebc380b331ff7d585ecd196284459b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:17:03 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 02:17:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Fri, 29 Sep 2023 02:17:06 GMT
ENV CADDY_VERSION=v2.7.4
# Fri, 29 Sep 2023 02:17:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 29 Sep 2023 02:17:13 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 29 Sep 2023 02:17:14 GMT
ENV XDG_DATA_HOME=/data
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 29 Sep 2023 02:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 29 Sep 2023 02:17:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 443
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 443/udp
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 2019
# Fri, 29 Sep 2023 02:17:24 GMT
WORKDIR /srv
# Fri, 29 Sep 2023 02:17:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa65cea7f5d70d1e203b851e43ad676e92f28c930ad32b6691e84ff9b5cda87`  
		Last Modified: Fri, 29 Sep 2023 02:18:03 GMT  
		Size: 362.2 KB (362182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7089a1d537371e29a65d106f43b45f2a0367d4d1db0eb7d6b7099f8ba05645`  
		Last Modified: Fri, 29 Sep 2023 02:18:01 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93ab741fa6270144ea59d6a5fa3c4138286a569f246fdccd829b317b051f3a`  
		Last Modified: Fri, 29 Sep 2023 02:18:05 GMT  
		Size: 13.2 MB (13228998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9e13bd2b56147eecc80f1fe1710e4350ea63d5edfb389fa89e2c6de06c08593a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17721238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f0101e0f893afb763d99b2050dbf4d68a44aae29785af6c05af5a552b0c1a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:19:38 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:19:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 28 Sep 2023 22:19:39 GMT
ENV CADDY_VERSION=v2.7.4
# Thu, 28 Sep 2023 22:19:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_DATA_HOME=/data
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 80
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443/udp
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 2019
# Thu, 28 Sep 2023 22:19:44 GMT
WORKDIR /srv
# Thu, 28 Sep 2023 22:19:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3df874173df47ad0bd0ef67b8ee598c77921810d84a67fd2984c4f8151c91`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a69c42a5c7fc6d73c00c7f6eb68522f3881aae55db4f85a8400e83b678b181`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793016dc78c9794c627c07afcd2fb34af4ee470ee7fef1a1596eff0c59ba6659`  
		Last Modified: Thu, 28 Sep 2023 22:20:16 GMT  
		Size: 14.1 MB (14143684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:493c52db91e0afa1fd7804f775be763188d075a528153780946c65eb91efc83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:4306b19982d623e5bda44ecd050491f3f26e18c89d24ca703f293b696d44bd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d9c60a52301fa63992088de297d121e91e89e3971ba8e11ad1d1f0f7a9820`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:54:30 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:54:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:20:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:20:23 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:43:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:43:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:19:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:19:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc37b24bb09971feb8bf4882e861bce9db0c985a16a900adb0dc9de3f854243b`  
		Last Modified: Thu, 28 Sep 2023 22:57:15 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4303e95078c253686dcc16d7717644af63809efcbd753c0a999c9aad3fe72`  
		Last Modified: Tue, 10 Oct 2023 19:26:17 GMT  
		Size: 67.0 MB (67012876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359925be0f358b952dc8be63647139c5aab0fff94f7a070d88cb51dd258f80e5`  
		Last Modified: Tue, 10 Oct 2023 19:26:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fd04581de0d1e57432e3cd2d301b8c86d38131e671e2f9084c4220db3b8a4`  
		Last Modified: Tue, 10 Oct 2023 19:44:17 GMT  
		Size: 5.0 MB (4970359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f405302374c4e7ed3ee716677478b7a65c771aed696a6eae07cacab445c514c6`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 1.3 MB (1302237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8d8c97cfe8c049fd27a671cf8e75310a4c620478a949d0beecf3577e695ae5`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:eba60e558fae5eb5237067ab66dcea5b0c12a3860210e548c2d702c8181969c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75414943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92d489fb77472b86f5254b7c82bedc01dfea7685efa49eb568f03d34718623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:55:22 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:55:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:21 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:49:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:49:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:49:43 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:12:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:12:27 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 01:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 01:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 01:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3da3b9e7a12f6bb6b7f56e9240c2c92ce8c9f5fd5ef3b3063b9a93d454919e`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 284.9 KB (284887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbb7b34bc324d050e49d3dd31294bdde5d6ecda33decf9afe31c11165b138a`  
		Last Modified: Tue, 10 Oct 2023 18:55:32 GMT  
		Size: 65.8 MB (65770135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022f45a9fb1e7649eb4a663acd4ed6437363b4fc6e56f6af3e5f457a5d06ee8`  
		Last Modified: Tue, 10 Oct 2023 18:55:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f1d9e9fe803fc18e89adff41bb7ac628a0499482d0d9b990f99a35dd6d72`  
		Last Modified: Tue, 10 Oct 2023 19:12:49 GMT  
		Size: 5.0 MB (4965397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5054be6311f7b03470317d9f7de58e04e679de2bf5db25ef4c0ef371ff62462`  
		Last Modified: Thu, 12 Oct 2023 01:40:00 GMT  
		Size: 1.2 MB (1248668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2b52d0abb8a046b659afd73ff08c22a087e5dc281a68aa7e1fdb1b48899fe`  
		Last Modified: Thu, 12 Oct 2023 01:39:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9fe2fc9a7aefc762908d8eb62e1f5b715f5c6aa8fbce095cfa2c6d26d462e3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba881a693ec60b5a46375fb85340a3861d008aa7254e7601435adae2d1daf6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:15:15 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:15:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:03 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:58:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:58:20 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:23:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:23:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:03:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:03:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:03:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e0aec75477c9a2cf6993e068fa40a45f0684d622ece61f54e6e02f9adebeb8`  
		Last Modified: Thu, 28 Sep 2023 22:19:29 GMT  
		Size: 284.1 KB (284076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28294fad378329bf4a8672c4c0b712a9e59a45a66612808d85332f4503ebf8f`  
		Last Modified: Tue, 10 Oct 2023 19:05:18 GMT  
		Size: 65.8 MB (65770038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03c9df1b84980cdf17791dc62f86d15d95de066f16d394a456dd8aba48b`  
		Last Modified: Tue, 10 Oct 2023 19:04:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cea91cf5bb06feabb363f5a7b857daa22b1f08afffdfe56760ea0d4e5528cc`  
		Last Modified: Tue, 10 Oct 2023 19:23:34 GMT  
		Size: 4.5 MB (4512286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2b4a58da12fe13357fce681851d77bf6dd233fbd3791fed232ef9d0ef4d52`  
		Last Modified: Thu, 12 Oct 2023 18:04:16 GMT  
		Size: 1.2 MB (1246090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c7342ff285197b8280fd7f6ffd53f282c84c09c6258c8e469f73f113668c`  
		Last Modified: Thu, 12 Oct 2023 18:04:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:afafe5da37d6fc453c6723b1feced43da8d935cfb9d6a99ac4fa46a0d56ca293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73997154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ae4c57df7271ea7d1caabf80c85a272b845d804b2159b225e810bd662b1f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:03:38 GMT
RUN apk add --no-cache ca-certificates
# Fri, 29 Sep 2023 01:40:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:39:56 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:40:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:40:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:40:07 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:05:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:05:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 19:45:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 19:45:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 19:45:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c21914ef412ef71f6092299b025bf4d504a49024701bf684bc9efd218155c63`  
		Last Modified: Fri, 29 Sep 2023 01:03:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b559ff2a6180beeb7515cfd5be18fb2e6dff3732111ac2b0841e36d5ac501`  
		Last Modified: Tue, 10 Oct 2023 19:45:06 GMT  
		Size: 64.1 MB (64110940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b5a6e49d2cdb4e3cfb2aa71d9c6bda6e9d8869367c8a0617db2ba6c1ea01b`  
		Last Modified: Tue, 10 Oct 2023 19:44:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fab64598da5eee75f0f364bf43af2d126525ad1785fd9a0ea5dda73e6406402`  
		Last Modified: Tue, 10 Oct 2023 20:06:14 GMT  
		Size: 5.1 MB (5069056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b277a31c32e84a57ea24d6ef1c227259bbae4aebf8c7656219dd718a05d33292`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a4acb26609b7e59176aadb51d7dcb66727dfbb0d07901022dfd56eac253c9e`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:8ccaa0a876d91c973bd880880eb16fb0a23ed96189c2b2df3a8c774c109edb07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74214371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210df7ee91e01af6665deb0296b08fe5553d0e0596c0fcc573f087b3da068993`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:13:11 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:13:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:17:44 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:18:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:18:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:18:17 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:46:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:46:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 19:46:41 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 19:46:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 19:46:43 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 19:46:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 19:46:45 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 19:46:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc67971d1767eae5019ffeaf8f893e6d81dbba50bde347da0c0433c56e3f2a3`  
		Last Modified: Thu, 28 Sep 2023 22:18:17 GMT  
		Size: 286.7 KB (286659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caf7fa003bdf7c7611eb2e33a11db077a0f632b70d28f5b73096bf051f25aeb`  
		Last Modified: Tue, 10 Oct 2023 19:28:09 GMT  
		Size: 64.1 MB (64125245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9573c5aef56335266ce720d0812f9a0156f628fbd01ba4a6462be56d8742dc8a`  
		Last Modified: Tue, 10 Oct 2023 19:27:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70c30dd200f1712a117ee42ac94a48f111b3d3e482ec05db53cafffc7b35dcf`  
		Last Modified: Tue, 10 Oct 2023 19:47:06 GMT  
		Size: 5.3 MB (5269226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2504109ddadb5c2133e7cfbb1caebb5de6f6c1effa9742ac36eec52a9751a110`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 1.2 MB (1186172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f92baeaf213968278b040b2fc465a59b7027c402bbc58f9ab15658a19e1341`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:ae945b58f882ac574669765568acbf43619d6da9e312750f5e3f4bf323ff64fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76113604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4b9728b30637022d501d3a2858327e288ef5e7fbc14bdbe43a06d71844717a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:38:54 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:38:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:43:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:43:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:43:39 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:00:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 20:00:02 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 20:00:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 20:00:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 20:00:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721f16693d4788a5add1bd0b22764c8887cdc62b24edf388ae895df440f4aa9`  
		Last Modified: Thu, 28 Sep 2023 21:46:22 GMT  
		Size: 285.1 KB (285095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa850520bfe7c982afe0c271ec09526214f569f386fba4c4fc8e4c4ee1b3b536`  
		Last Modified: Tue, 10 Oct 2023 19:40:41 GMT  
		Size: 66.2 MB (66235247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6466a1a32b54238d2aab33605db66c5f9b58dc02e3d202483ebca7dddea04aa5`  
		Last Modified: Tue, 10 Oct 2023 19:40:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bcbbdd4f9b04ca7467a549aa3d4110cbc2dab3bb78f1643c27992f4c0d82c3`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 5.1 MB (5115210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2e4e8bdf6b9562139094c05c60d87a303098f59919f4c20403ba5d815b300`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 1.3 MB (1262388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca343226e4d88ff4f38e0b18cf13f8a1d73a45cee5de97aed1fc8383b8003ca`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:951876270030a4a5404a8bab425d35b64f90babc594bb65c261cc05eab33ed79
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128478401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883908294a37d78f29e796d389d42c83a12c68a6c0f1113bba3bdd9290db5b05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:23:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:23:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:23:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:23:12 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:24:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:24:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:25:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:25:34 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:28:30 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:28:31 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:03:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:03:14 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:42:14 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:42:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fded5ce3c59d7e8d637a5536d6eed085ff6b6a323f42c1df76a7be6e9970ee`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a72a6b595ab9f8f71a34a065e75e609b20ea5e026f901820fce6d3c9134939`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2574f8b7fb0ec5a8c39ee40a8008f0d24c398380247bf7140be1abdede5542b`  
		Last Modified: Wed, 11 Oct 2023 02:46:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c53676fe729ebf5d3c07215d91afa952e6190715f79a7952f4c3aa121231e`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382bb149b70b82f9c2f58ebf6a2672dc4c64460017836d73a5a23b7379ea095`  
		Last Modified: Wed, 11 Oct 2023 02:46:44 GMT  
		Size: 25.6 MB (25557568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a2584f4b3b8f3038fa41c0719005822ab967d85d1231843bd729a7b3d2d60`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058e02ad62f976d823e3035f0578b2868eb09f28986153342a52014cc5c3810`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 284.8 KB (284754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fce039c31b2e60b62a0ede9974b6574519f2e47e1d8f4e09c7a1f30763aee95`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65449f183261f9bbdb731d41f5e6fca94f3e547e8d996133e418773400cfcfe`  
		Last Modified: Wed, 11 Oct 2023 02:46:59 GMT  
		Size: 69.3 MB (69345382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394e07c2ad53e950c47ffb647836822197dc5f8ebe082eaa045854e2b25bafc7`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f5e59c63ef5be894fc498ab0e165faa3129d35a8a8f5173f12c6a4232f588`  
		Last Modified: Wed, 11 Oct 2023 04:06:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c675831130735b443a544dff1b9c188928f34947a5342350ef04eadc0d1ab27`  
		Last Modified: Wed, 11 Oct 2023 04:06:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe7c1d1f5383a4421f2a0e7284e17db440ee5b7be9f487ce9048f76970e7b6`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee998763c3cef90b11adda3322e66e1a89d89409d1ed29dd73a4101fb657e29`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a81b981d5dc89b19acce594b87914fc5bc4777e42b1322ca9b9d4c4b4f179`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.7 MB (1682335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ad6e4e7b1be08f8a79e4d77328648deded93f9ef0d4a1e8202ce4c3a21c67`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:04b6c1b2519c8d35d65976c53b4523d7074d53c7b98fa5b29b83c837e021b493
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1956648108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c3e402a7640df51573fae3237803e1e5fabce3d4c88849d9513c716654d474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:19:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:19:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:20:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:20:18 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:20:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:20:42 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:22:59 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:23:01 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:04:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:04:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:43:30 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:43:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60407a49ce6121c65fa6399c333c5227a09518414fd987c460ea29cb441ac5a`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe632e8cddda4e5f347720b87b8b3868e2e2969048761e3b0a40799d33f5f7a`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4384696fc834e9658e7b3e5d1ceb1f8b362db85865daf29521b3c75c6999c046`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794ea611ef69f54d577f90b68e165e40a17e43b6d1d08f59951a38e084ea5fb`  
		Last Modified: Wed, 11 Oct 2023 02:45:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74dc2d701da2bfabc4d44e6a4e6b92912515e2ca1fb053ffcc6b0d5cae2972`  
		Last Modified: Wed, 11 Oct 2023 02:45:08 GMT  
		Size: 25.5 MB (25531724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91612399ba7df8de0a05ad078c3817548f0a3b44516b76565e14a96ea62452e9`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439c7c4353d2432c780827e4926910b19e84fe436d58e0a8129de2f631bd2b8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 264.4 KB (264384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0eaedd98e739ace4b7934261c71292195e461adcc977d02e57604d4a42ee8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f46e84d4d007a200b1d6e7cb5b48db90116cdeb8bd3ec3964a08191875973e2`  
		Last Modified: Wed, 11 Oct 2023 02:45:25 GMT  
		Size: 69.3 MB (69325670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59bab6d84ca44bbb60474dcf59c9af4f0f15edbdd64249b0eeaf968aff211f`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f449f4d34d707dbde9cbb245c154c0b2e1d1a2c55d172501f8d7da576866f76f`  
		Last Modified: Wed, 11 Oct 2023 04:06:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2edf76facdd17af03954b607484f7f7b36164a30634d19dd96b7320feb6b5`  
		Last Modified: Wed, 11 Oct 2023 04:06:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802c3686d509915fea71538d2c40c7a48c71719fab6144cb4497b6118b276ab9`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb183ed6cdad781eaba7bd1b4cb443befd9042c8a59450ee41f0245dd0ece4`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec33434b55fade6bcd7f3f0dfc10c981de93dc44bbae2b8702fdb6418a37a65b`  
		Last Modified: Thu, 12 Oct 2023 01:45:38 GMT  
		Size: 1.7 MB (1664788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0833369ef8236fcf99aba2d1fa48788db07662d0a9885a8429d435bf9f2227b2`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:fbf0444d9829e43a97cb98d36ae346b6e11682a766701ff61efad79231ce69d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:4306b19982d623e5bda44ecd050491f3f26e18c89d24ca703f293b696d44bd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d9c60a52301fa63992088de297d121e91e89e3971ba8e11ad1d1f0f7a9820`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:54:30 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:54:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:20:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:20:23 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:43:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:43:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:19:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:19:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc37b24bb09971feb8bf4882e861bce9db0c985a16a900adb0dc9de3f854243b`  
		Last Modified: Thu, 28 Sep 2023 22:57:15 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4303e95078c253686dcc16d7717644af63809efcbd753c0a999c9aad3fe72`  
		Last Modified: Tue, 10 Oct 2023 19:26:17 GMT  
		Size: 67.0 MB (67012876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359925be0f358b952dc8be63647139c5aab0fff94f7a070d88cb51dd258f80e5`  
		Last Modified: Tue, 10 Oct 2023 19:26:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fd04581de0d1e57432e3cd2d301b8c86d38131e671e2f9084c4220db3b8a4`  
		Last Modified: Tue, 10 Oct 2023 19:44:17 GMT  
		Size: 5.0 MB (4970359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f405302374c4e7ed3ee716677478b7a65c771aed696a6eae07cacab445c514c6`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 1.3 MB (1302237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8d8c97cfe8c049fd27a671cf8e75310a4c620478a949d0beecf3577e695ae5`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:eba60e558fae5eb5237067ab66dcea5b0c12a3860210e548c2d702c8181969c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75414943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92d489fb77472b86f5254b7c82bedc01dfea7685efa49eb568f03d34718623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:55:22 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:55:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:21 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:49:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:49:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:49:43 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:12:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:12:27 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 01:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 01:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 01:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3da3b9e7a12f6bb6b7f56e9240c2c92ce8c9f5fd5ef3b3063b9a93d454919e`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 284.9 KB (284887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbb7b34bc324d050e49d3dd31294bdde5d6ecda33decf9afe31c11165b138a`  
		Last Modified: Tue, 10 Oct 2023 18:55:32 GMT  
		Size: 65.8 MB (65770135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022f45a9fb1e7649eb4a663acd4ed6437363b4fc6e56f6af3e5f457a5d06ee8`  
		Last Modified: Tue, 10 Oct 2023 18:55:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f1d9e9fe803fc18e89adff41bb7ac628a0499482d0d9b990f99a35dd6d72`  
		Last Modified: Tue, 10 Oct 2023 19:12:49 GMT  
		Size: 5.0 MB (4965397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5054be6311f7b03470317d9f7de58e04e679de2bf5db25ef4c0ef371ff62462`  
		Last Modified: Thu, 12 Oct 2023 01:40:00 GMT  
		Size: 1.2 MB (1248668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2b52d0abb8a046b659afd73ff08c22a087e5dc281a68aa7e1fdb1b48899fe`  
		Last Modified: Thu, 12 Oct 2023 01:39:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9fe2fc9a7aefc762908d8eb62e1f5b715f5c6aa8fbce095cfa2c6d26d462e3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba881a693ec60b5a46375fb85340a3861d008aa7254e7601435adae2d1daf6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:15:15 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:15:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:03 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:58:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:58:20 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:23:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:23:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:03:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:03:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:03:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e0aec75477c9a2cf6993e068fa40a45f0684d622ece61f54e6e02f9adebeb8`  
		Last Modified: Thu, 28 Sep 2023 22:19:29 GMT  
		Size: 284.1 KB (284076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28294fad378329bf4a8672c4c0b712a9e59a45a66612808d85332f4503ebf8f`  
		Last Modified: Tue, 10 Oct 2023 19:05:18 GMT  
		Size: 65.8 MB (65770038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03c9df1b84980cdf17791dc62f86d15d95de066f16d394a456dd8aba48b`  
		Last Modified: Tue, 10 Oct 2023 19:04:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cea91cf5bb06feabb363f5a7b857daa22b1f08afffdfe56760ea0d4e5528cc`  
		Last Modified: Tue, 10 Oct 2023 19:23:34 GMT  
		Size: 4.5 MB (4512286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2b4a58da12fe13357fce681851d77bf6dd233fbd3791fed232ef9d0ef4d52`  
		Last Modified: Thu, 12 Oct 2023 18:04:16 GMT  
		Size: 1.2 MB (1246090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c7342ff285197b8280fd7f6ffd53f282c84c09c6258c8e469f73f113668c`  
		Last Modified: Thu, 12 Oct 2023 18:04:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:afafe5da37d6fc453c6723b1feced43da8d935cfb9d6a99ac4fa46a0d56ca293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73997154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ae4c57df7271ea7d1caabf80c85a272b845d804b2159b225e810bd662b1f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:03:38 GMT
RUN apk add --no-cache ca-certificates
# Fri, 29 Sep 2023 01:40:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:39:56 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:40:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:40:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:40:07 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:05:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:05:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 19:45:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 19:45:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 19:45:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c21914ef412ef71f6092299b025bf4d504a49024701bf684bc9efd218155c63`  
		Last Modified: Fri, 29 Sep 2023 01:03:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b559ff2a6180beeb7515cfd5be18fb2e6dff3732111ac2b0841e36d5ac501`  
		Last Modified: Tue, 10 Oct 2023 19:45:06 GMT  
		Size: 64.1 MB (64110940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b5a6e49d2cdb4e3cfb2aa71d9c6bda6e9d8869367c8a0617db2ba6c1ea01b`  
		Last Modified: Tue, 10 Oct 2023 19:44:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fab64598da5eee75f0f364bf43af2d126525ad1785fd9a0ea5dda73e6406402`  
		Last Modified: Tue, 10 Oct 2023 20:06:14 GMT  
		Size: 5.1 MB (5069056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b277a31c32e84a57ea24d6ef1c227259bbae4aebf8c7656219dd718a05d33292`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a4acb26609b7e59176aadb51d7dcb66727dfbb0d07901022dfd56eac253c9e`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8ccaa0a876d91c973bd880880eb16fb0a23ed96189c2b2df3a8c774c109edb07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74214371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210df7ee91e01af6665deb0296b08fe5553d0e0596c0fcc573f087b3da068993`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:13:11 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:13:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:17:44 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:18:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:18:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:18:17 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:46:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:46:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 19:46:41 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 19:46:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 19:46:43 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 19:46:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 19:46:45 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 19:46:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc67971d1767eae5019ffeaf8f893e6d81dbba50bde347da0c0433c56e3f2a3`  
		Last Modified: Thu, 28 Sep 2023 22:18:17 GMT  
		Size: 286.7 KB (286659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caf7fa003bdf7c7611eb2e33a11db077a0f632b70d28f5b73096bf051f25aeb`  
		Last Modified: Tue, 10 Oct 2023 19:28:09 GMT  
		Size: 64.1 MB (64125245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9573c5aef56335266ce720d0812f9a0156f628fbd01ba4a6462be56d8742dc8a`  
		Last Modified: Tue, 10 Oct 2023 19:27:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70c30dd200f1712a117ee42ac94a48f111b3d3e482ec05db53cafffc7b35dcf`  
		Last Modified: Tue, 10 Oct 2023 19:47:06 GMT  
		Size: 5.3 MB (5269226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2504109ddadb5c2133e7cfbb1caebb5de6f6c1effa9742ac36eec52a9751a110`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 1.2 MB (1186172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f92baeaf213968278b040b2fc465a59b7027c402bbc58f9ab15658a19e1341`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:ae945b58f882ac574669765568acbf43619d6da9e312750f5e3f4bf323ff64fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76113604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4b9728b30637022d501d3a2858327e288ef5e7fbc14bdbe43a06d71844717a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:38:54 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:38:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:43:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:43:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:43:39 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:00:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 20:00:02 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 20:00:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 20:00:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 20:00:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721f16693d4788a5add1bd0b22764c8887cdc62b24edf388ae895df440f4aa9`  
		Last Modified: Thu, 28 Sep 2023 21:46:22 GMT  
		Size: 285.1 KB (285095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa850520bfe7c982afe0c271ec09526214f569f386fba4c4fc8e4c4ee1b3b536`  
		Last Modified: Tue, 10 Oct 2023 19:40:41 GMT  
		Size: 66.2 MB (66235247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6466a1a32b54238d2aab33605db66c5f9b58dc02e3d202483ebca7dddea04aa5`  
		Last Modified: Tue, 10 Oct 2023 19:40:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bcbbdd4f9b04ca7467a549aa3d4110cbc2dab3bb78f1643c27992f4c0d82c3`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 5.1 MB (5115210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2e4e8bdf6b9562139094c05c60d87a303098f59919f4c20403ba5d815b300`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 1.3 MB (1262388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca343226e4d88ff4f38e0b18cf13f8a1d73a45cee5de97aed1fc8383b8003ca`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:c0740b75861440c921e23bec00c2ce3e14bda7ca7967b2aec7855352ea96cd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:951876270030a4a5404a8bab425d35b64f90babc594bb65c261cc05eab33ed79
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128478401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883908294a37d78f29e796d389d42c83a12c68a6c0f1113bba3bdd9290db5b05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:23:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:23:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:23:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:23:12 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:24:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:24:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:25:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:25:34 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:28:30 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:28:31 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:03:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:03:14 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:42:14 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:42:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fded5ce3c59d7e8d637a5536d6eed085ff6b6a323f42c1df76a7be6e9970ee`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a72a6b595ab9f8f71a34a065e75e609b20ea5e026f901820fce6d3c9134939`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2574f8b7fb0ec5a8c39ee40a8008f0d24c398380247bf7140be1abdede5542b`  
		Last Modified: Wed, 11 Oct 2023 02:46:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c53676fe729ebf5d3c07215d91afa952e6190715f79a7952f4c3aa121231e`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382bb149b70b82f9c2f58ebf6a2672dc4c64460017836d73a5a23b7379ea095`  
		Last Modified: Wed, 11 Oct 2023 02:46:44 GMT  
		Size: 25.6 MB (25557568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a2584f4b3b8f3038fa41c0719005822ab967d85d1231843bd729a7b3d2d60`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058e02ad62f976d823e3035f0578b2868eb09f28986153342a52014cc5c3810`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 284.8 KB (284754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fce039c31b2e60b62a0ede9974b6574519f2e47e1d8f4e09c7a1f30763aee95`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65449f183261f9bbdb731d41f5e6fca94f3e547e8d996133e418773400cfcfe`  
		Last Modified: Wed, 11 Oct 2023 02:46:59 GMT  
		Size: 69.3 MB (69345382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394e07c2ad53e950c47ffb647836822197dc5f8ebe082eaa045854e2b25bafc7`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f5e59c63ef5be894fc498ab0e165faa3129d35a8a8f5173f12c6a4232f588`  
		Last Modified: Wed, 11 Oct 2023 04:06:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c675831130735b443a544dff1b9c188928f34947a5342350ef04eadc0d1ab27`  
		Last Modified: Wed, 11 Oct 2023 04:06:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe7c1d1f5383a4421f2a0e7284e17db440ee5b7be9f487ce9048f76970e7b6`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee998763c3cef90b11adda3322e66e1a89d89409d1ed29dd73a4101fb657e29`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a81b981d5dc89b19acce594b87914fc5bc4777e42b1322ca9b9d4c4b4f179`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.7 MB (1682335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ad6e4e7b1be08f8a79e4d77328648deded93f9ef0d4a1e8202ce4c3a21c67`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7a4eaeb7416d6a4b442d55eab7e8c7824e36a07baef33353084b943d46b6b7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:04b6c1b2519c8d35d65976c53b4523d7074d53c7b98fa5b29b83c837e021b493
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1956648108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c3e402a7640df51573fae3237803e1e5fabce3d4c88849d9513c716654d474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:19:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:19:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:20:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:20:18 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:20:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:20:42 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:22:59 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:23:01 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:04:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:04:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:43:30 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:43:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60407a49ce6121c65fa6399c333c5227a09518414fd987c460ea29cb441ac5a`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe632e8cddda4e5f347720b87b8b3868e2e2969048761e3b0a40799d33f5f7a`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4384696fc834e9658e7b3e5d1ceb1f8b362db85865daf29521b3c75c6999c046`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794ea611ef69f54d577f90b68e165e40a17e43b6d1d08f59951a38e084ea5fb`  
		Last Modified: Wed, 11 Oct 2023 02:45:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74dc2d701da2bfabc4d44e6a4e6b92912515e2ca1fb053ffcc6b0d5cae2972`  
		Last Modified: Wed, 11 Oct 2023 02:45:08 GMT  
		Size: 25.5 MB (25531724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91612399ba7df8de0a05ad078c3817548f0a3b44516b76565e14a96ea62452e9`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439c7c4353d2432c780827e4926910b19e84fe436d58e0a8129de2f631bd2b8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 264.4 KB (264384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0eaedd98e739ace4b7934261c71292195e461adcc977d02e57604d4a42ee8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f46e84d4d007a200b1d6e7cb5b48db90116cdeb8bd3ec3964a08191875973e2`  
		Last Modified: Wed, 11 Oct 2023 02:45:25 GMT  
		Size: 69.3 MB (69325670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59bab6d84ca44bbb60474dcf59c9af4f0f15edbdd64249b0eeaf968aff211f`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f449f4d34d707dbde9cbb245c154c0b2e1d1a2c55d172501f8d7da576866f76f`  
		Last Modified: Wed, 11 Oct 2023 04:06:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2edf76facdd17af03954b607484f7f7b36164a30634d19dd96b7320feb6b5`  
		Last Modified: Wed, 11 Oct 2023 04:06:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802c3686d509915fea71538d2c40c7a48c71719fab6144cb4497b6118b276ab9`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb183ed6cdad781eaba7bd1b4cb443befd9042c8a59450ee41f0245dd0ece4`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec33434b55fade6bcd7f3f0dfc10c981de93dc44bbae2b8702fdb6418a37a65b`  
		Last Modified: Thu, 12 Oct 2023 01:45:38 GMT  
		Size: 1.7 MB (1664788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0833369ef8236fcf99aba2d1fa48788db07662d0a9885a8429d435bf9f2227b2`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:b859825f1b8093a4b961d02fb945e63f5180c5e07e56ce7495384835c016c47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8169d134dfa19ddbba9eeeb7210c5227c2a61f00906c340474aab1250aba47f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:278d32be7fb2f9a5e3f48ea6a672747dbb4ad6256e4802aff4a1e11a67e2e518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7`

```console
$ docker pull caddy@sha256:db7fa54ce8d507a6c22cdf0ee9cd5229747d8f552c83912b0c5427b92e6e271c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7` - linux; amd64

```console
$ docker pull caddy@sha256:aaa9d8750860e5b886fab8c4da6842782ec2eb2e963e6d48ad59657fadd9a6aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e21ab2b0efc5ac0207c16134ac96b3779212c692cde05a24f73a68fec756a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:43:13 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:43:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:19:15 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:19:17 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:19:18 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:19:19 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:19:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be51084fb891c6796079e693b73f6f882266a5e66211344173031e2b0c8ffd`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 350.8 KB (350826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d867aa37ac50364bf4082dc48c7d4e1b88ead3164d47855e1bbc2ef3678cfc`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a4bfabc0b0dc6924b7d8aad02805798c86ada09d9d11861f29ed76915f758`  
		Last Modified: Thu, 12 Oct 2023 18:19:43 GMT  
		Size: 14.7 MB (14713998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v6

```console
$ docker pull caddy@sha256:be2cb3ef217d514df988a7fef43bc11cf8267f3c3eea319a82c6c4c2985cd7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17422254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375c06eba744fadf74e23a036a6af05a75573760968f9d65a405d7401973be3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:59:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 21:59:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 01:39:17 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:39:22 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:39:22 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 01:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1018057a600163b1c1b92c21ade975c631b2f8ccde66d524cfe0ecdac8e1920d`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 347.6 KB (347613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec54680cbf2cb1a25285c82a7888498ab47d03a68db200a160d7162325a5be19`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38012b56d72a4a2c2a42ed660476530218852cf8953587cb803fab0cf7de99c3`  
		Last Modified: Thu, 12 Oct 2023 01:39:46 GMT  
		Size: 13.9 MB (13921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cc67ef274e0b09f75c4adf46397b2b796c00d9d014d1312d53bc3e16fa763bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b853d3cd7e1ec8e5fdb884e061c15e6da29f25d0954bf803f08625dc542bf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:19:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 23:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:03:38 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:03:42 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:03:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66901ba48d0ee53cd827f4eb2cfd8b049cebba8c3d307b69760e1be917f69476`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 344.4 KB (344448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeb3f6febb36993d8a51ad919784fd152aab5f6e17fe00d579916f32e42911`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00371969ebc6f50beb432e93f29b2658ffdbf2de985784e17b0a8e696970a7d`  
		Last Modified: Thu, 12 Oct 2023 18:04:03 GMT  
		Size: 13.9 MB (13903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c5cdeee3505159e6a4ebd367b13f1a6bb32d424327be8ee4a3e09734c5cf63d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6797cb1033afffac8c55f0ee0f0dd9f60e58dc19ef1edc5852606eced4c793b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:16:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 01:16:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 19:45:02 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 80
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 19:45:05 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 19:45:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f21cb0286edf1f5fefb4a859b414a446bb81baa9e8901fc8f4eca55a43aeeec`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 360.6 KB (360643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444b3f9419d06a4b77a65935a3b1c6e657c607bcfb9e3bd1abebe57eae36e6a`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e60671cdfd4ec2cb64a788cecf65bb2166ba5bf3e7bba029ccf0c8c0dbeb3`  
		Last Modified: Thu, 12 Oct 2023 19:45:30 GMT  
		Size: 13.6 MB (13573811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; ppc64le

```console
$ docker pull caddy@sha256:65084a14a1557b92af5b8ba6fcba9a7a710ed5caef1e2310f9622166608c9531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba45deaa04c3feac6474c22204ac6f5ebc380b331ff7d585ecd196284459b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:17:03 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 02:17:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Fri, 29 Sep 2023 02:17:06 GMT
ENV CADDY_VERSION=v2.7.4
# Fri, 29 Sep 2023 02:17:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 29 Sep 2023 02:17:13 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 29 Sep 2023 02:17:14 GMT
ENV XDG_DATA_HOME=/data
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 29 Sep 2023 02:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 29 Sep 2023 02:17:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 443
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 443/udp
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 2019
# Fri, 29 Sep 2023 02:17:24 GMT
WORKDIR /srv
# Fri, 29 Sep 2023 02:17:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa65cea7f5d70d1e203b851e43ad676e92f28c930ad32b6691e84ff9b5cda87`  
		Last Modified: Fri, 29 Sep 2023 02:18:03 GMT  
		Size: 362.2 KB (362182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7089a1d537371e29a65d106f43b45f2a0367d4d1db0eb7d6b7099f8ba05645`  
		Last Modified: Fri, 29 Sep 2023 02:18:01 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93ab741fa6270144ea59d6a5fa3c4138286a569f246fdccd829b317b051f3a`  
		Last Modified: Fri, 29 Sep 2023 02:18:05 GMT  
		Size: 13.2 MB (13228998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; s390x

```console
$ docker pull caddy@sha256:9e13bd2b56147eecc80f1fe1710e4350ea63d5edfb389fa89e2c6de06c08593a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17721238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f0101e0f893afb763d99b2050dbf4d68a44aae29785af6c05af5a552b0c1a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:19:38 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:19:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 28 Sep 2023 22:19:39 GMT
ENV CADDY_VERSION=v2.7.4
# Thu, 28 Sep 2023 22:19:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_DATA_HOME=/data
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 80
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443/udp
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 2019
# Thu, 28 Sep 2023 22:19:44 GMT
WORKDIR /srv
# Thu, 28 Sep 2023 22:19:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3df874173df47ad0bd0ef67b8ee598c77921810d84a67fd2984c4f8151c91`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a69c42a5c7fc6d73c00c7f6eb68522f3881aae55db4f85a8400e83b678b181`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793016dc78c9794c627c07afcd2fb34af4ee470ee7fef1a1596eff0c59ba6659`  
		Last Modified: Thu, 28 Sep 2023 22:20:16 GMT  
		Size: 14.1 MB (14143684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-alpine`

```console
$ docker pull caddy@sha256:0157ce2e3977145c950dc562b339351cd37d06abe9ac8bf36b04b1b2f8ce6104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.7-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:aaa9d8750860e5b886fab8c4da6842782ec2eb2e963e6d48ad59657fadd9a6aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e21ab2b0efc5ac0207c16134ac96b3779212c692cde05a24f73a68fec756a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:43:13 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:43:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:19:15 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:19:17 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:19:18 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:19:19 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:19:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be51084fb891c6796079e693b73f6f882266a5e66211344173031e2b0c8ffd`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 350.8 KB (350826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d867aa37ac50364bf4082dc48c7d4e1b88ead3164d47855e1bbc2ef3678cfc`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a4bfabc0b0dc6924b7d8aad02805798c86ada09d9d11861f29ed76915f758`  
		Last Modified: Thu, 12 Oct 2023 18:19:43 GMT  
		Size: 14.7 MB (14713998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:be2cb3ef217d514df988a7fef43bc11cf8267f3c3eea319a82c6c4c2985cd7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17422254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375c06eba744fadf74e23a036a6af05a75573760968f9d65a405d7401973be3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:59:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 21:59:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 01:39:17 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:39:22 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:39:22 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 01:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1018057a600163b1c1b92c21ade975c631b2f8ccde66d524cfe0ecdac8e1920d`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 347.6 KB (347613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec54680cbf2cb1a25285c82a7888498ab47d03a68db200a160d7162325a5be19`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38012b56d72a4a2c2a42ed660476530218852cf8953587cb803fab0cf7de99c3`  
		Last Modified: Thu, 12 Oct 2023 01:39:46 GMT  
		Size: 13.9 MB (13921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cc67ef274e0b09f75c4adf46397b2b796c00d9d014d1312d53bc3e16fa763bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b853d3cd7e1ec8e5fdb884e061c15e6da29f25d0954bf803f08625dc542bf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:19:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 23:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:03:38 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:03:42 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:03:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66901ba48d0ee53cd827f4eb2cfd8b049cebba8c3d307b69760e1be917f69476`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 344.4 KB (344448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeb3f6febb36993d8a51ad919784fd152aab5f6e17fe00d579916f32e42911`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00371969ebc6f50beb432e93f29b2658ffdbf2de985784e17b0a8e696970a7d`  
		Last Modified: Thu, 12 Oct 2023 18:04:03 GMT  
		Size: 13.9 MB (13903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c5cdeee3505159e6a4ebd367b13f1a6bb32d424327be8ee4a3e09734c5cf63d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6797cb1033afffac8c55f0ee0f0dd9f60e58dc19ef1edc5852606eced4c793b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:16:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 01:16:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 19:45:02 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 80
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 19:45:05 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 19:45:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f21cb0286edf1f5fefb4a859b414a446bb81baa9e8901fc8f4eca55a43aeeec`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 360.6 KB (360643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444b3f9419d06a4b77a65935a3b1c6e657c607bcfb9e3bd1abebe57eae36e6a`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e60671cdfd4ec2cb64a788cecf65bb2166ba5bf3e7bba029ccf0c8c0dbeb3`  
		Last Modified: Thu, 12 Oct 2023 19:45:30 GMT  
		Size: 13.6 MB (13573811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:65084a14a1557b92af5b8ba6fcba9a7a710ed5caef1e2310f9622166608c9531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba45deaa04c3feac6474c22204ac6f5ebc380b331ff7d585ecd196284459b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:17:03 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 02:17:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Fri, 29 Sep 2023 02:17:06 GMT
ENV CADDY_VERSION=v2.7.4
# Fri, 29 Sep 2023 02:17:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 29 Sep 2023 02:17:13 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 29 Sep 2023 02:17:14 GMT
ENV XDG_DATA_HOME=/data
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 29 Sep 2023 02:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 29 Sep 2023 02:17:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 443
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 443/udp
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 2019
# Fri, 29 Sep 2023 02:17:24 GMT
WORKDIR /srv
# Fri, 29 Sep 2023 02:17:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa65cea7f5d70d1e203b851e43ad676e92f28c930ad32b6691e84ff9b5cda87`  
		Last Modified: Fri, 29 Sep 2023 02:18:03 GMT  
		Size: 362.2 KB (362182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7089a1d537371e29a65d106f43b45f2a0367d4d1db0eb7d6b7099f8ba05645`  
		Last Modified: Fri, 29 Sep 2023 02:18:01 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93ab741fa6270144ea59d6a5fa3c4138286a569f246fdccd829b317b051f3a`  
		Last Modified: Fri, 29 Sep 2023 02:18:05 GMT  
		Size: 13.2 MB (13228998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9e13bd2b56147eecc80f1fe1710e4350ea63d5edfb389fa89e2c6de06c08593a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17721238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f0101e0f893afb763d99b2050dbf4d68a44aae29785af6c05af5a552b0c1a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:19:38 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:19:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 28 Sep 2023 22:19:39 GMT
ENV CADDY_VERSION=v2.7.4
# Thu, 28 Sep 2023 22:19:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_DATA_HOME=/data
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 80
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443/udp
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 2019
# Thu, 28 Sep 2023 22:19:44 GMT
WORKDIR /srv
# Thu, 28 Sep 2023 22:19:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3df874173df47ad0bd0ef67b8ee598c77921810d84a67fd2984c4f8151c91`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a69c42a5c7fc6d73c00c7f6eb68522f3881aae55db4f85a8400e83b678b181`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793016dc78c9794c627c07afcd2fb34af4ee470ee7fef1a1596eff0c59ba6659`  
		Last Modified: Thu, 28 Sep 2023 22:20:16 GMT  
		Size: 14.1 MB (14143684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder`

```console
$ docker pull caddy@sha256:493c52db91e0afa1fd7804f775be763188d075a528153780946c65eb91efc83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7-builder` - linux; amd64

```console
$ docker pull caddy@sha256:4306b19982d623e5bda44ecd050491f3f26e18c89d24ca703f293b696d44bd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d9c60a52301fa63992088de297d121e91e89e3971ba8e11ad1d1f0f7a9820`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:54:30 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:54:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:20:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:20:23 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:43:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:43:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:19:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:19:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc37b24bb09971feb8bf4882e861bce9db0c985a16a900adb0dc9de3f854243b`  
		Last Modified: Thu, 28 Sep 2023 22:57:15 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4303e95078c253686dcc16d7717644af63809efcbd753c0a999c9aad3fe72`  
		Last Modified: Tue, 10 Oct 2023 19:26:17 GMT  
		Size: 67.0 MB (67012876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359925be0f358b952dc8be63647139c5aab0fff94f7a070d88cb51dd258f80e5`  
		Last Modified: Tue, 10 Oct 2023 19:26:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fd04581de0d1e57432e3cd2d301b8c86d38131e671e2f9084c4220db3b8a4`  
		Last Modified: Tue, 10 Oct 2023 19:44:17 GMT  
		Size: 5.0 MB (4970359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f405302374c4e7ed3ee716677478b7a65c771aed696a6eae07cacab445c514c6`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 1.3 MB (1302237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8d8c97cfe8c049fd27a671cf8e75310a4c620478a949d0beecf3577e695ae5`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:eba60e558fae5eb5237067ab66dcea5b0c12a3860210e548c2d702c8181969c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75414943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92d489fb77472b86f5254b7c82bedc01dfea7685efa49eb568f03d34718623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:55:22 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:55:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:21 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:49:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:49:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:49:43 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:12:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:12:27 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 01:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 01:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 01:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3da3b9e7a12f6bb6b7f56e9240c2c92ce8c9f5fd5ef3b3063b9a93d454919e`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 284.9 KB (284887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbb7b34bc324d050e49d3dd31294bdde5d6ecda33decf9afe31c11165b138a`  
		Last Modified: Tue, 10 Oct 2023 18:55:32 GMT  
		Size: 65.8 MB (65770135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022f45a9fb1e7649eb4a663acd4ed6437363b4fc6e56f6af3e5f457a5d06ee8`  
		Last Modified: Tue, 10 Oct 2023 18:55:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f1d9e9fe803fc18e89adff41bb7ac628a0499482d0d9b990f99a35dd6d72`  
		Last Modified: Tue, 10 Oct 2023 19:12:49 GMT  
		Size: 5.0 MB (4965397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5054be6311f7b03470317d9f7de58e04e679de2bf5db25ef4c0ef371ff62462`  
		Last Modified: Thu, 12 Oct 2023 01:40:00 GMT  
		Size: 1.2 MB (1248668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2b52d0abb8a046b659afd73ff08c22a087e5dc281a68aa7e1fdb1b48899fe`  
		Last Modified: Thu, 12 Oct 2023 01:39:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9fe2fc9a7aefc762908d8eb62e1f5b715f5c6aa8fbce095cfa2c6d26d462e3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba881a693ec60b5a46375fb85340a3861d008aa7254e7601435adae2d1daf6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:15:15 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:15:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:03 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:58:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:58:20 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:23:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:23:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:03:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:03:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:03:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e0aec75477c9a2cf6993e068fa40a45f0684d622ece61f54e6e02f9adebeb8`  
		Last Modified: Thu, 28 Sep 2023 22:19:29 GMT  
		Size: 284.1 KB (284076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28294fad378329bf4a8672c4c0b712a9e59a45a66612808d85332f4503ebf8f`  
		Last Modified: Tue, 10 Oct 2023 19:05:18 GMT  
		Size: 65.8 MB (65770038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03c9df1b84980cdf17791dc62f86d15d95de066f16d394a456dd8aba48b`  
		Last Modified: Tue, 10 Oct 2023 19:04:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cea91cf5bb06feabb363f5a7b857daa22b1f08afffdfe56760ea0d4e5528cc`  
		Last Modified: Tue, 10 Oct 2023 19:23:34 GMT  
		Size: 4.5 MB (4512286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2b4a58da12fe13357fce681851d77bf6dd233fbd3791fed232ef9d0ef4d52`  
		Last Modified: Thu, 12 Oct 2023 18:04:16 GMT  
		Size: 1.2 MB (1246090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c7342ff285197b8280fd7f6ffd53f282c84c09c6258c8e469f73f113668c`  
		Last Modified: Thu, 12 Oct 2023 18:04:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:afafe5da37d6fc453c6723b1feced43da8d935cfb9d6a99ac4fa46a0d56ca293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73997154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ae4c57df7271ea7d1caabf80c85a272b845d804b2159b225e810bd662b1f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:03:38 GMT
RUN apk add --no-cache ca-certificates
# Fri, 29 Sep 2023 01:40:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:39:56 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:40:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:40:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:40:07 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:05:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:05:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 19:45:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 19:45:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 19:45:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c21914ef412ef71f6092299b025bf4d504a49024701bf684bc9efd218155c63`  
		Last Modified: Fri, 29 Sep 2023 01:03:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b559ff2a6180beeb7515cfd5be18fb2e6dff3732111ac2b0841e36d5ac501`  
		Last Modified: Tue, 10 Oct 2023 19:45:06 GMT  
		Size: 64.1 MB (64110940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b5a6e49d2cdb4e3cfb2aa71d9c6bda6e9d8869367c8a0617db2ba6c1ea01b`  
		Last Modified: Tue, 10 Oct 2023 19:44:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fab64598da5eee75f0f364bf43af2d126525ad1785fd9a0ea5dda73e6406402`  
		Last Modified: Tue, 10 Oct 2023 20:06:14 GMT  
		Size: 5.1 MB (5069056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b277a31c32e84a57ea24d6ef1c227259bbae4aebf8c7656219dd718a05d33292`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a4acb26609b7e59176aadb51d7dcb66727dfbb0d07901022dfd56eac253c9e`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:8ccaa0a876d91c973bd880880eb16fb0a23ed96189c2b2df3a8c774c109edb07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74214371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210df7ee91e01af6665deb0296b08fe5553d0e0596c0fcc573f087b3da068993`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:13:11 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:13:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:17:44 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:18:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:18:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:18:17 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:46:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:46:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 19:46:41 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 19:46:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 19:46:43 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 19:46:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 19:46:45 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 19:46:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc67971d1767eae5019ffeaf8f893e6d81dbba50bde347da0c0433c56e3f2a3`  
		Last Modified: Thu, 28 Sep 2023 22:18:17 GMT  
		Size: 286.7 KB (286659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caf7fa003bdf7c7611eb2e33a11db077a0f632b70d28f5b73096bf051f25aeb`  
		Last Modified: Tue, 10 Oct 2023 19:28:09 GMT  
		Size: 64.1 MB (64125245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9573c5aef56335266ce720d0812f9a0156f628fbd01ba4a6462be56d8742dc8a`  
		Last Modified: Tue, 10 Oct 2023 19:27:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70c30dd200f1712a117ee42ac94a48f111b3d3e482ec05db53cafffc7b35dcf`  
		Last Modified: Tue, 10 Oct 2023 19:47:06 GMT  
		Size: 5.3 MB (5269226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2504109ddadb5c2133e7cfbb1caebb5de6f6c1effa9742ac36eec52a9751a110`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 1.2 MB (1186172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f92baeaf213968278b040b2fc465a59b7027c402bbc58f9ab15658a19e1341`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; s390x

```console
$ docker pull caddy@sha256:ae945b58f882ac574669765568acbf43619d6da9e312750f5e3f4bf323ff64fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76113604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4b9728b30637022d501d3a2858327e288ef5e7fbc14bdbe43a06d71844717a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:38:54 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:38:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:43:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:43:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:43:39 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:00:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 20:00:02 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 20:00:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 20:00:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 20:00:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721f16693d4788a5add1bd0b22764c8887cdc62b24edf388ae895df440f4aa9`  
		Last Modified: Thu, 28 Sep 2023 21:46:22 GMT  
		Size: 285.1 KB (285095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa850520bfe7c982afe0c271ec09526214f569f386fba4c4fc8e4c4ee1b3b536`  
		Last Modified: Tue, 10 Oct 2023 19:40:41 GMT  
		Size: 66.2 MB (66235247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6466a1a32b54238d2aab33605db66c5f9b58dc02e3d202483ebca7dddea04aa5`  
		Last Modified: Tue, 10 Oct 2023 19:40:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bcbbdd4f9b04ca7467a549aa3d4110cbc2dab3bb78f1643c27992f4c0d82c3`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 5.1 MB (5115210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2e4e8bdf6b9562139094c05c60d87a303098f59919f4c20403ba5d815b300`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 1.3 MB (1262388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca343226e4d88ff4f38e0b18cf13f8a1d73a45cee5de97aed1fc8383b8003ca`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:951876270030a4a5404a8bab425d35b64f90babc594bb65c261cc05eab33ed79
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128478401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883908294a37d78f29e796d389d42c83a12c68a6c0f1113bba3bdd9290db5b05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:23:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:23:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:23:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:23:12 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:24:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:24:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:25:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:25:34 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:28:30 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:28:31 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:03:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:03:14 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:42:14 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:42:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fded5ce3c59d7e8d637a5536d6eed085ff6b6a323f42c1df76a7be6e9970ee`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a72a6b595ab9f8f71a34a065e75e609b20ea5e026f901820fce6d3c9134939`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2574f8b7fb0ec5a8c39ee40a8008f0d24c398380247bf7140be1abdede5542b`  
		Last Modified: Wed, 11 Oct 2023 02:46:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c53676fe729ebf5d3c07215d91afa952e6190715f79a7952f4c3aa121231e`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382bb149b70b82f9c2f58ebf6a2672dc4c64460017836d73a5a23b7379ea095`  
		Last Modified: Wed, 11 Oct 2023 02:46:44 GMT  
		Size: 25.6 MB (25557568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a2584f4b3b8f3038fa41c0719005822ab967d85d1231843bd729a7b3d2d60`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058e02ad62f976d823e3035f0578b2868eb09f28986153342a52014cc5c3810`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 284.8 KB (284754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fce039c31b2e60b62a0ede9974b6574519f2e47e1d8f4e09c7a1f30763aee95`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65449f183261f9bbdb731d41f5e6fca94f3e547e8d996133e418773400cfcfe`  
		Last Modified: Wed, 11 Oct 2023 02:46:59 GMT  
		Size: 69.3 MB (69345382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394e07c2ad53e950c47ffb647836822197dc5f8ebe082eaa045854e2b25bafc7`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f5e59c63ef5be894fc498ab0e165faa3129d35a8a8f5173f12c6a4232f588`  
		Last Modified: Wed, 11 Oct 2023 04:06:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c675831130735b443a544dff1b9c188928f34947a5342350ef04eadc0d1ab27`  
		Last Modified: Wed, 11 Oct 2023 04:06:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe7c1d1f5383a4421f2a0e7284e17db440ee5b7be9f487ce9048f76970e7b6`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee998763c3cef90b11adda3322e66e1a89d89409d1ed29dd73a4101fb657e29`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a81b981d5dc89b19acce594b87914fc5bc4777e42b1322ca9b9d4c4b4f179`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.7 MB (1682335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ad6e4e7b1be08f8a79e4d77328648deded93f9ef0d4a1e8202ce4c3a21c67`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:04b6c1b2519c8d35d65976c53b4523d7074d53c7b98fa5b29b83c837e021b493
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1956648108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c3e402a7640df51573fae3237803e1e5fabce3d4c88849d9513c716654d474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:19:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:19:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:20:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:20:18 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:20:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:20:42 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:22:59 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:23:01 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:04:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:04:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:43:30 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:43:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60407a49ce6121c65fa6399c333c5227a09518414fd987c460ea29cb441ac5a`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe632e8cddda4e5f347720b87b8b3868e2e2969048761e3b0a40799d33f5f7a`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4384696fc834e9658e7b3e5d1ceb1f8b362db85865daf29521b3c75c6999c046`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794ea611ef69f54d577f90b68e165e40a17e43b6d1d08f59951a38e084ea5fb`  
		Last Modified: Wed, 11 Oct 2023 02:45:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74dc2d701da2bfabc4d44e6a4e6b92912515e2ca1fb053ffcc6b0d5cae2972`  
		Last Modified: Wed, 11 Oct 2023 02:45:08 GMT  
		Size: 25.5 MB (25531724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91612399ba7df8de0a05ad078c3817548f0a3b44516b76565e14a96ea62452e9`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439c7c4353d2432c780827e4926910b19e84fe436d58e0a8129de2f631bd2b8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 264.4 KB (264384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0eaedd98e739ace4b7934261c71292195e461adcc977d02e57604d4a42ee8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f46e84d4d007a200b1d6e7cb5b48db90116cdeb8bd3ec3964a08191875973e2`  
		Last Modified: Wed, 11 Oct 2023 02:45:25 GMT  
		Size: 69.3 MB (69325670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59bab6d84ca44bbb60474dcf59c9af4f0f15edbdd64249b0eeaf968aff211f`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f449f4d34d707dbde9cbb245c154c0b2e1d1a2c55d172501f8d7da576866f76f`  
		Last Modified: Wed, 11 Oct 2023 04:06:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2edf76facdd17af03954b607484f7f7b36164a30634d19dd96b7320feb6b5`  
		Last Modified: Wed, 11 Oct 2023 04:06:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802c3686d509915fea71538d2c40c7a48c71719fab6144cb4497b6118b276ab9`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb183ed6cdad781eaba7bd1b4cb443befd9042c8a59450ee41f0245dd0ece4`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec33434b55fade6bcd7f3f0dfc10c981de93dc44bbae2b8702fdb6418a37a65b`  
		Last Modified: Thu, 12 Oct 2023 01:45:38 GMT  
		Size: 1.7 MB (1664788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0833369ef8236fcf99aba2d1fa48788db07662d0a9885a8429d435bf9f2227b2`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:fbf0444d9829e43a97cb98d36ae346b6e11682a766701ff61efad79231ce69d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.7-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:4306b19982d623e5bda44ecd050491f3f26e18c89d24ca703f293b696d44bd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d9c60a52301fa63992088de297d121e91e89e3971ba8e11ad1d1f0f7a9820`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:54:30 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:54:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:20:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:20:23 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:43:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:43:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:19:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:19:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc37b24bb09971feb8bf4882e861bce9db0c985a16a900adb0dc9de3f854243b`  
		Last Modified: Thu, 28 Sep 2023 22:57:15 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4303e95078c253686dcc16d7717644af63809efcbd753c0a999c9aad3fe72`  
		Last Modified: Tue, 10 Oct 2023 19:26:17 GMT  
		Size: 67.0 MB (67012876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359925be0f358b952dc8be63647139c5aab0fff94f7a070d88cb51dd258f80e5`  
		Last Modified: Tue, 10 Oct 2023 19:26:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fd04581de0d1e57432e3cd2d301b8c86d38131e671e2f9084c4220db3b8a4`  
		Last Modified: Tue, 10 Oct 2023 19:44:17 GMT  
		Size: 5.0 MB (4970359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f405302374c4e7ed3ee716677478b7a65c771aed696a6eae07cacab445c514c6`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 1.3 MB (1302237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8d8c97cfe8c049fd27a671cf8e75310a4c620478a949d0beecf3577e695ae5`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:eba60e558fae5eb5237067ab66dcea5b0c12a3860210e548c2d702c8181969c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75414943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92d489fb77472b86f5254b7c82bedc01dfea7685efa49eb568f03d34718623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:55:22 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:55:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:21 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:49:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:49:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:49:43 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:12:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:12:27 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 01:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 01:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 01:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3da3b9e7a12f6bb6b7f56e9240c2c92ce8c9f5fd5ef3b3063b9a93d454919e`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 284.9 KB (284887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbb7b34bc324d050e49d3dd31294bdde5d6ecda33decf9afe31c11165b138a`  
		Last Modified: Tue, 10 Oct 2023 18:55:32 GMT  
		Size: 65.8 MB (65770135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022f45a9fb1e7649eb4a663acd4ed6437363b4fc6e56f6af3e5f457a5d06ee8`  
		Last Modified: Tue, 10 Oct 2023 18:55:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f1d9e9fe803fc18e89adff41bb7ac628a0499482d0d9b990f99a35dd6d72`  
		Last Modified: Tue, 10 Oct 2023 19:12:49 GMT  
		Size: 5.0 MB (4965397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5054be6311f7b03470317d9f7de58e04e679de2bf5db25ef4c0ef371ff62462`  
		Last Modified: Thu, 12 Oct 2023 01:40:00 GMT  
		Size: 1.2 MB (1248668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2b52d0abb8a046b659afd73ff08c22a087e5dc281a68aa7e1fdb1b48899fe`  
		Last Modified: Thu, 12 Oct 2023 01:39:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9fe2fc9a7aefc762908d8eb62e1f5b715f5c6aa8fbce095cfa2c6d26d462e3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba881a693ec60b5a46375fb85340a3861d008aa7254e7601435adae2d1daf6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:15:15 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:15:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:03 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:58:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:58:20 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:23:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:23:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:03:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:03:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:03:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e0aec75477c9a2cf6993e068fa40a45f0684d622ece61f54e6e02f9adebeb8`  
		Last Modified: Thu, 28 Sep 2023 22:19:29 GMT  
		Size: 284.1 KB (284076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28294fad378329bf4a8672c4c0b712a9e59a45a66612808d85332f4503ebf8f`  
		Last Modified: Tue, 10 Oct 2023 19:05:18 GMT  
		Size: 65.8 MB (65770038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03c9df1b84980cdf17791dc62f86d15d95de066f16d394a456dd8aba48b`  
		Last Modified: Tue, 10 Oct 2023 19:04:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cea91cf5bb06feabb363f5a7b857daa22b1f08afffdfe56760ea0d4e5528cc`  
		Last Modified: Tue, 10 Oct 2023 19:23:34 GMT  
		Size: 4.5 MB (4512286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2b4a58da12fe13357fce681851d77bf6dd233fbd3791fed232ef9d0ef4d52`  
		Last Modified: Thu, 12 Oct 2023 18:04:16 GMT  
		Size: 1.2 MB (1246090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c7342ff285197b8280fd7f6ffd53f282c84c09c6258c8e469f73f113668c`  
		Last Modified: Thu, 12 Oct 2023 18:04:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:afafe5da37d6fc453c6723b1feced43da8d935cfb9d6a99ac4fa46a0d56ca293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73997154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ae4c57df7271ea7d1caabf80c85a272b845d804b2159b225e810bd662b1f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:03:38 GMT
RUN apk add --no-cache ca-certificates
# Fri, 29 Sep 2023 01:40:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:39:56 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:40:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:40:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:40:07 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:05:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:05:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 19:45:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 19:45:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 19:45:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c21914ef412ef71f6092299b025bf4d504a49024701bf684bc9efd218155c63`  
		Last Modified: Fri, 29 Sep 2023 01:03:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b559ff2a6180beeb7515cfd5be18fb2e6dff3732111ac2b0841e36d5ac501`  
		Last Modified: Tue, 10 Oct 2023 19:45:06 GMT  
		Size: 64.1 MB (64110940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b5a6e49d2cdb4e3cfb2aa71d9c6bda6e9d8869367c8a0617db2ba6c1ea01b`  
		Last Modified: Tue, 10 Oct 2023 19:44:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fab64598da5eee75f0f364bf43af2d126525ad1785fd9a0ea5dda73e6406402`  
		Last Modified: Tue, 10 Oct 2023 20:06:14 GMT  
		Size: 5.1 MB (5069056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b277a31c32e84a57ea24d6ef1c227259bbae4aebf8c7656219dd718a05d33292`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a4acb26609b7e59176aadb51d7dcb66727dfbb0d07901022dfd56eac253c9e`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8ccaa0a876d91c973bd880880eb16fb0a23ed96189c2b2df3a8c774c109edb07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74214371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210df7ee91e01af6665deb0296b08fe5553d0e0596c0fcc573f087b3da068993`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:13:11 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:13:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:17:44 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:18:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:18:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:18:17 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:46:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:46:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 19:46:41 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 19:46:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 19:46:43 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 19:46:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 19:46:45 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 19:46:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc67971d1767eae5019ffeaf8f893e6d81dbba50bde347da0c0433c56e3f2a3`  
		Last Modified: Thu, 28 Sep 2023 22:18:17 GMT  
		Size: 286.7 KB (286659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caf7fa003bdf7c7611eb2e33a11db077a0f632b70d28f5b73096bf051f25aeb`  
		Last Modified: Tue, 10 Oct 2023 19:28:09 GMT  
		Size: 64.1 MB (64125245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9573c5aef56335266ce720d0812f9a0156f628fbd01ba4a6462be56d8742dc8a`  
		Last Modified: Tue, 10 Oct 2023 19:27:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70c30dd200f1712a117ee42ac94a48f111b3d3e482ec05db53cafffc7b35dcf`  
		Last Modified: Tue, 10 Oct 2023 19:47:06 GMT  
		Size: 5.3 MB (5269226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2504109ddadb5c2133e7cfbb1caebb5de6f6c1effa9742ac36eec52a9751a110`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 1.2 MB (1186172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f92baeaf213968278b040b2fc465a59b7027c402bbc58f9ab15658a19e1341`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:ae945b58f882ac574669765568acbf43619d6da9e312750f5e3f4bf323ff64fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76113604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4b9728b30637022d501d3a2858327e288ef5e7fbc14bdbe43a06d71844717a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:38:54 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:38:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:43:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:43:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:43:39 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:00:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 20:00:02 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 20:00:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 20:00:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 20:00:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721f16693d4788a5add1bd0b22764c8887cdc62b24edf388ae895df440f4aa9`  
		Last Modified: Thu, 28 Sep 2023 21:46:22 GMT  
		Size: 285.1 KB (285095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa850520bfe7c982afe0c271ec09526214f569f386fba4c4fc8e4c4ee1b3b536`  
		Last Modified: Tue, 10 Oct 2023 19:40:41 GMT  
		Size: 66.2 MB (66235247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6466a1a32b54238d2aab33605db66c5f9b58dc02e3d202483ebca7dddea04aa5`  
		Last Modified: Tue, 10 Oct 2023 19:40:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bcbbdd4f9b04ca7467a549aa3d4110cbc2dab3bb78f1643c27992f4c0d82c3`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 5.1 MB (5115210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2e4e8bdf6b9562139094c05c60d87a303098f59919f4c20403ba5d815b300`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 1.3 MB (1262388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca343226e4d88ff4f38e0b18cf13f8a1d73a45cee5de97aed1fc8383b8003ca`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:c0740b75861440c921e23bec00c2ce3e14bda7ca7967b2aec7855352ea96cd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:951876270030a4a5404a8bab425d35b64f90babc594bb65c261cc05eab33ed79
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128478401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883908294a37d78f29e796d389d42c83a12c68a6c0f1113bba3bdd9290db5b05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:23:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:23:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:23:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:23:12 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:24:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:24:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:25:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:25:34 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:28:30 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:28:31 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:03:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:03:14 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:42:14 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:42:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fded5ce3c59d7e8d637a5536d6eed085ff6b6a323f42c1df76a7be6e9970ee`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a72a6b595ab9f8f71a34a065e75e609b20ea5e026f901820fce6d3c9134939`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2574f8b7fb0ec5a8c39ee40a8008f0d24c398380247bf7140be1abdede5542b`  
		Last Modified: Wed, 11 Oct 2023 02:46:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c53676fe729ebf5d3c07215d91afa952e6190715f79a7952f4c3aa121231e`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382bb149b70b82f9c2f58ebf6a2672dc4c64460017836d73a5a23b7379ea095`  
		Last Modified: Wed, 11 Oct 2023 02:46:44 GMT  
		Size: 25.6 MB (25557568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a2584f4b3b8f3038fa41c0719005822ab967d85d1231843bd729a7b3d2d60`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058e02ad62f976d823e3035f0578b2868eb09f28986153342a52014cc5c3810`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 284.8 KB (284754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fce039c31b2e60b62a0ede9974b6574519f2e47e1d8f4e09c7a1f30763aee95`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65449f183261f9bbdb731d41f5e6fca94f3e547e8d996133e418773400cfcfe`  
		Last Modified: Wed, 11 Oct 2023 02:46:59 GMT  
		Size: 69.3 MB (69345382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394e07c2ad53e950c47ffb647836822197dc5f8ebe082eaa045854e2b25bafc7`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f5e59c63ef5be894fc498ab0e165faa3129d35a8a8f5173f12c6a4232f588`  
		Last Modified: Wed, 11 Oct 2023 04:06:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c675831130735b443a544dff1b9c188928f34947a5342350ef04eadc0d1ab27`  
		Last Modified: Wed, 11 Oct 2023 04:06:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe7c1d1f5383a4421f2a0e7284e17db440ee5b7be9f487ce9048f76970e7b6`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee998763c3cef90b11adda3322e66e1a89d89409d1ed29dd73a4101fb657e29`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a81b981d5dc89b19acce594b87914fc5bc4777e42b1322ca9b9d4c4b4f179`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.7 MB (1682335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ad6e4e7b1be08f8a79e4d77328648deded93f9ef0d4a1e8202ce4c3a21c67`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7a4eaeb7416d6a4b442d55eab7e8c7824e36a07baef33353084b943d46b6b7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:04b6c1b2519c8d35d65976c53b4523d7074d53c7b98fa5b29b83c837e021b493
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1956648108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c3e402a7640df51573fae3237803e1e5fabce3d4c88849d9513c716654d474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:19:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:19:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:20:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:20:18 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:20:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:20:42 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:22:59 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:23:01 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:04:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:04:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:43:30 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:43:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60407a49ce6121c65fa6399c333c5227a09518414fd987c460ea29cb441ac5a`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe632e8cddda4e5f347720b87b8b3868e2e2969048761e3b0a40799d33f5f7a`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4384696fc834e9658e7b3e5d1ceb1f8b362db85865daf29521b3c75c6999c046`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794ea611ef69f54d577f90b68e165e40a17e43b6d1d08f59951a38e084ea5fb`  
		Last Modified: Wed, 11 Oct 2023 02:45:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74dc2d701da2bfabc4d44e6a4e6b92912515e2ca1fb053ffcc6b0d5cae2972`  
		Last Modified: Wed, 11 Oct 2023 02:45:08 GMT  
		Size: 25.5 MB (25531724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91612399ba7df8de0a05ad078c3817548f0a3b44516b76565e14a96ea62452e9`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439c7c4353d2432c780827e4926910b19e84fe436d58e0a8129de2f631bd2b8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 264.4 KB (264384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0eaedd98e739ace4b7934261c71292195e461adcc977d02e57604d4a42ee8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f46e84d4d007a200b1d6e7cb5b48db90116cdeb8bd3ec3964a08191875973e2`  
		Last Modified: Wed, 11 Oct 2023 02:45:25 GMT  
		Size: 69.3 MB (69325670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59bab6d84ca44bbb60474dcf59c9af4f0f15edbdd64249b0eeaf968aff211f`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f449f4d34d707dbde9cbb245c154c0b2e1d1a2c55d172501f8d7da576866f76f`  
		Last Modified: Wed, 11 Oct 2023 04:06:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2edf76facdd17af03954b607484f7f7b36164a30634d19dd96b7320feb6b5`  
		Last Modified: Wed, 11 Oct 2023 04:06:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802c3686d509915fea71538d2c40c7a48c71719fab6144cb4497b6118b276ab9`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb183ed6cdad781eaba7bd1b4cb443befd9042c8a59450ee41f0245dd0ece4`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec33434b55fade6bcd7f3f0dfc10c981de93dc44bbae2b8702fdb6418a37a65b`  
		Last Modified: Thu, 12 Oct 2023 01:45:38 GMT  
		Size: 1.7 MB (1664788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0833369ef8236fcf99aba2d1fa48788db07662d0a9885a8429d435bf9f2227b2`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore`

```console
$ docker pull caddy@sha256:b859825f1b8093a4b961d02fb945e63f5180c5e07e56ce7495384835c016c47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-windowsservercore` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8169d134dfa19ddbba9eeeb7210c5227c2a61f00906c340474aab1250aba47f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `caddy:2.7-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:278d32be7fb2f9a5e3f48ea6a672747dbb4ad6256e4802aff4a1e11a67e2e518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.5`

```console
$ docker pull caddy@sha256:40d85229ce7874b3b217343f9864a8401aebfb59d5ec9d361f4d984ffa2c1897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7.5` - linux; amd64

```console
$ docker pull caddy@sha256:aaa9d8750860e5b886fab8c4da6842782ec2eb2e963e6d48ad59657fadd9a6aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e21ab2b0efc5ac0207c16134ac96b3779212c692cde05a24f73a68fec756a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:43:13 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:43:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:19:15 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:19:17 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:19:18 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:19:19 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:19:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be51084fb891c6796079e693b73f6f882266a5e66211344173031e2b0c8ffd`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 350.8 KB (350826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d867aa37ac50364bf4082dc48c7d4e1b88ead3164d47855e1bbc2ef3678cfc`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a4bfabc0b0dc6924b7d8aad02805798c86ada09d9d11861f29ed76915f758`  
		Last Modified: Thu, 12 Oct 2023 18:19:43 GMT  
		Size: 14.7 MB (14713998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5` - linux; arm variant v6

```console
$ docker pull caddy@sha256:be2cb3ef217d514df988a7fef43bc11cf8267f3c3eea319a82c6c4c2985cd7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17422254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375c06eba744fadf74e23a036a6af05a75573760968f9d65a405d7401973be3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:59:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 21:59:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 01:39:17 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:39:22 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:39:22 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 01:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1018057a600163b1c1b92c21ade975c631b2f8ccde66d524cfe0ecdac8e1920d`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 347.6 KB (347613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec54680cbf2cb1a25285c82a7888498ab47d03a68db200a160d7162325a5be19`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38012b56d72a4a2c2a42ed660476530218852cf8953587cb803fab0cf7de99c3`  
		Last Modified: Thu, 12 Oct 2023 01:39:46 GMT  
		Size: 13.9 MB (13921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cc67ef274e0b09f75c4adf46397b2b796c00d9d014d1312d53bc3e16fa763bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b853d3cd7e1ec8e5fdb884e061c15e6da29f25d0954bf803f08625dc542bf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:19:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 23:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:03:38 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:03:42 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:03:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66901ba48d0ee53cd827f4eb2cfd8b049cebba8c3d307b69760e1be917f69476`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 344.4 KB (344448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeb3f6febb36993d8a51ad919784fd152aab5f6e17fe00d579916f32e42911`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00371969ebc6f50beb432e93f29b2658ffdbf2de985784e17b0a8e696970a7d`  
		Last Modified: Thu, 12 Oct 2023 18:04:03 GMT  
		Size: 13.9 MB (13903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c5cdeee3505159e6a4ebd367b13f1a6bb32d424327be8ee4a3e09734c5cf63d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6797cb1033afffac8c55f0ee0f0dd9f60e58dc19ef1edc5852606eced4c793b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:16:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 01:16:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 19:45:02 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 80
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 19:45:05 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 19:45:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f21cb0286edf1f5fefb4a859b414a446bb81baa9e8901fc8f4eca55a43aeeec`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 360.6 KB (360643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444b3f9419d06a4b77a65935a3b1c6e657c607bcfb9e3bd1abebe57eae36e6a`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e60671cdfd4ec2cb64a788cecf65bb2166ba5bf3e7bba029ccf0c8c0dbeb3`  
		Last Modified: Thu, 12 Oct 2023 19:45:30 GMT  
		Size: 13.6 MB (13573811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.5-alpine`

```console
$ docker pull caddy@sha256:a6da3a5344175003538ac1cf4ec8a79ef48d525c0841e9cc81a5c0112d52c982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `caddy:2.7.5-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:aaa9d8750860e5b886fab8c4da6842782ec2eb2e963e6d48ad59657fadd9a6aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e21ab2b0efc5ac0207c16134ac96b3779212c692cde05a24f73a68fec756a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:43:13 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:43:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:19:15 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:19:17 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:19:18 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:19:19 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:19:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be51084fb891c6796079e693b73f6f882266a5e66211344173031e2b0c8ffd`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 350.8 KB (350826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d867aa37ac50364bf4082dc48c7d4e1b88ead3164d47855e1bbc2ef3678cfc`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a4bfabc0b0dc6924b7d8aad02805798c86ada09d9d11861f29ed76915f758`  
		Last Modified: Thu, 12 Oct 2023 18:19:43 GMT  
		Size: 14.7 MB (14713998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:be2cb3ef217d514df988a7fef43bc11cf8267f3c3eea319a82c6c4c2985cd7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17422254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375c06eba744fadf74e23a036a6af05a75573760968f9d65a405d7401973be3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:59:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 21:59:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 01:39:17 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:39:22 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:39:22 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 01:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1018057a600163b1c1b92c21ade975c631b2f8ccde66d524cfe0ecdac8e1920d`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 347.6 KB (347613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec54680cbf2cb1a25285c82a7888498ab47d03a68db200a160d7162325a5be19`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38012b56d72a4a2c2a42ed660476530218852cf8953587cb803fab0cf7de99c3`  
		Last Modified: Thu, 12 Oct 2023 01:39:46 GMT  
		Size: 13.9 MB (13921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cc67ef274e0b09f75c4adf46397b2b796c00d9d014d1312d53bc3e16fa763bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b853d3cd7e1ec8e5fdb884e061c15e6da29f25d0954bf803f08625dc542bf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:19:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 23:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:03:38 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:03:42 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:03:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66901ba48d0ee53cd827f4eb2cfd8b049cebba8c3d307b69760e1be917f69476`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 344.4 KB (344448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeb3f6febb36993d8a51ad919784fd152aab5f6e17fe00d579916f32e42911`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00371969ebc6f50beb432e93f29b2658ffdbf2de985784e17b0a8e696970a7d`  
		Last Modified: Thu, 12 Oct 2023 18:04:03 GMT  
		Size: 13.9 MB (13903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c5cdeee3505159e6a4ebd367b13f1a6bb32d424327be8ee4a3e09734c5cf63d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6797cb1033afffac8c55f0ee0f0dd9f60e58dc19ef1edc5852606eced4c793b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:16:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 01:16:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 19:45:02 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 80
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 19:45:05 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 19:45:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f21cb0286edf1f5fefb4a859b414a446bb81baa9e8901fc8f4eca55a43aeeec`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 360.6 KB (360643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444b3f9419d06a4b77a65935a3b1c6e657c607bcfb9e3bd1abebe57eae36e6a`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e60671cdfd4ec2cb64a788cecf65bb2166ba5bf3e7bba029ccf0c8c0dbeb3`  
		Last Modified: Thu, 12 Oct 2023 19:45:30 GMT  
		Size: 13.6 MB (13573811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.5-builder`

```console
$ docker pull caddy@sha256:e2e8d36ca8c3c4366fc1d901bb0114d55e5a6bdb73dceb5a993fc02655995264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7.5-builder` - linux; amd64

```console
$ docker pull caddy@sha256:4306b19982d623e5bda44ecd050491f3f26e18c89d24ca703f293b696d44bd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d9c60a52301fa63992088de297d121e91e89e3971ba8e11ad1d1f0f7a9820`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:54:30 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:54:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:20:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:20:23 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:43:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:43:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:19:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:19:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc37b24bb09971feb8bf4882e861bce9db0c985a16a900adb0dc9de3f854243b`  
		Last Modified: Thu, 28 Sep 2023 22:57:15 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4303e95078c253686dcc16d7717644af63809efcbd753c0a999c9aad3fe72`  
		Last Modified: Tue, 10 Oct 2023 19:26:17 GMT  
		Size: 67.0 MB (67012876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359925be0f358b952dc8be63647139c5aab0fff94f7a070d88cb51dd258f80e5`  
		Last Modified: Tue, 10 Oct 2023 19:26:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fd04581de0d1e57432e3cd2d301b8c86d38131e671e2f9084c4220db3b8a4`  
		Last Modified: Tue, 10 Oct 2023 19:44:17 GMT  
		Size: 5.0 MB (4970359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f405302374c4e7ed3ee716677478b7a65c771aed696a6eae07cacab445c514c6`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 1.3 MB (1302237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8d8c97cfe8c049fd27a671cf8e75310a4c620478a949d0beecf3577e695ae5`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:eba60e558fae5eb5237067ab66dcea5b0c12a3860210e548c2d702c8181969c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75414943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92d489fb77472b86f5254b7c82bedc01dfea7685efa49eb568f03d34718623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:55:22 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:55:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:21 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:49:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:49:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:49:43 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:12:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:12:27 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 01:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 01:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 01:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3da3b9e7a12f6bb6b7f56e9240c2c92ce8c9f5fd5ef3b3063b9a93d454919e`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 284.9 KB (284887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbb7b34bc324d050e49d3dd31294bdde5d6ecda33decf9afe31c11165b138a`  
		Last Modified: Tue, 10 Oct 2023 18:55:32 GMT  
		Size: 65.8 MB (65770135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022f45a9fb1e7649eb4a663acd4ed6437363b4fc6e56f6af3e5f457a5d06ee8`  
		Last Modified: Tue, 10 Oct 2023 18:55:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f1d9e9fe803fc18e89adff41bb7ac628a0499482d0d9b990f99a35dd6d72`  
		Last Modified: Tue, 10 Oct 2023 19:12:49 GMT  
		Size: 5.0 MB (4965397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5054be6311f7b03470317d9f7de58e04e679de2bf5db25ef4c0ef371ff62462`  
		Last Modified: Thu, 12 Oct 2023 01:40:00 GMT  
		Size: 1.2 MB (1248668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2b52d0abb8a046b659afd73ff08c22a087e5dc281a68aa7e1fdb1b48899fe`  
		Last Modified: Thu, 12 Oct 2023 01:39:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9fe2fc9a7aefc762908d8eb62e1f5b715f5c6aa8fbce095cfa2c6d26d462e3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba881a693ec60b5a46375fb85340a3861d008aa7254e7601435adae2d1daf6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:15:15 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:15:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:03 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:58:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:58:20 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:23:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:23:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:03:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:03:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:03:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e0aec75477c9a2cf6993e068fa40a45f0684d622ece61f54e6e02f9adebeb8`  
		Last Modified: Thu, 28 Sep 2023 22:19:29 GMT  
		Size: 284.1 KB (284076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28294fad378329bf4a8672c4c0b712a9e59a45a66612808d85332f4503ebf8f`  
		Last Modified: Tue, 10 Oct 2023 19:05:18 GMT  
		Size: 65.8 MB (65770038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03c9df1b84980cdf17791dc62f86d15d95de066f16d394a456dd8aba48b`  
		Last Modified: Tue, 10 Oct 2023 19:04:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cea91cf5bb06feabb363f5a7b857daa22b1f08afffdfe56760ea0d4e5528cc`  
		Last Modified: Tue, 10 Oct 2023 19:23:34 GMT  
		Size: 4.5 MB (4512286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2b4a58da12fe13357fce681851d77bf6dd233fbd3791fed232ef9d0ef4d52`  
		Last Modified: Thu, 12 Oct 2023 18:04:16 GMT  
		Size: 1.2 MB (1246090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c7342ff285197b8280fd7f6ffd53f282c84c09c6258c8e469f73f113668c`  
		Last Modified: Thu, 12 Oct 2023 18:04:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:afafe5da37d6fc453c6723b1feced43da8d935cfb9d6a99ac4fa46a0d56ca293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73997154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ae4c57df7271ea7d1caabf80c85a272b845d804b2159b225e810bd662b1f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:03:38 GMT
RUN apk add --no-cache ca-certificates
# Fri, 29 Sep 2023 01:40:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:39:56 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:40:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:40:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:40:07 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:05:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:05:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 19:45:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 19:45:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 19:45:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c21914ef412ef71f6092299b025bf4d504a49024701bf684bc9efd218155c63`  
		Last Modified: Fri, 29 Sep 2023 01:03:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b559ff2a6180beeb7515cfd5be18fb2e6dff3732111ac2b0841e36d5ac501`  
		Last Modified: Tue, 10 Oct 2023 19:45:06 GMT  
		Size: 64.1 MB (64110940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b5a6e49d2cdb4e3cfb2aa71d9c6bda6e9d8869367c8a0617db2ba6c1ea01b`  
		Last Modified: Tue, 10 Oct 2023 19:44:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fab64598da5eee75f0f364bf43af2d126525ad1785fd9a0ea5dda73e6406402`  
		Last Modified: Tue, 10 Oct 2023 20:06:14 GMT  
		Size: 5.1 MB (5069056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b277a31c32e84a57ea24d6ef1c227259bbae4aebf8c7656219dd718a05d33292`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a4acb26609b7e59176aadb51d7dcb66727dfbb0d07901022dfd56eac253c9e`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-builder` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:951876270030a4a5404a8bab425d35b64f90babc594bb65c261cc05eab33ed79
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128478401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883908294a37d78f29e796d389d42c83a12c68a6c0f1113bba3bdd9290db5b05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:23:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:23:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:23:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:23:12 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:24:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:24:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:25:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:25:34 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:28:30 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:28:31 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:03:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:03:14 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:42:14 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:42:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fded5ce3c59d7e8d637a5536d6eed085ff6b6a323f42c1df76a7be6e9970ee`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a72a6b595ab9f8f71a34a065e75e609b20ea5e026f901820fce6d3c9134939`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2574f8b7fb0ec5a8c39ee40a8008f0d24c398380247bf7140be1abdede5542b`  
		Last Modified: Wed, 11 Oct 2023 02:46:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c53676fe729ebf5d3c07215d91afa952e6190715f79a7952f4c3aa121231e`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382bb149b70b82f9c2f58ebf6a2672dc4c64460017836d73a5a23b7379ea095`  
		Last Modified: Wed, 11 Oct 2023 02:46:44 GMT  
		Size: 25.6 MB (25557568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a2584f4b3b8f3038fa41c0719005822ab967d85d1231843bd729a7b3d2d60`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058e02ad62f976d823e3035f0578b2868eb09f28986153342a52014cc5c3810`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 284.8 KB (284754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fce039c31b2e60b62a0ede9974b6574519f2e47e1d8f4e09c7a1f30763aee95`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65449f183261f9bbdb731d41f5e6fca94f3e547e8d996133e418773400cfcfe`  
		Last Modified: Wed, 11 Oct 2023 02:46:59 GMT  
		Size: 69.3 MB (69345382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394e07c2ad53e950c47ffb647836822197dc5f8ebe082eaa045854e2b25bafc7`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f5e59c63ef5be894fc498ab0e165faa3129d35a8a8f5173f12c6a4232f588`  
		Last Modified: Wed, 11 Oct 2023 04:06:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c675831130735b443a544dff1b9c188928f34947a5342350ef04eadc0d1ab27`  
		Last Modified: Wed, 11 Oct 2023 04:06:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe7c1d1f5383a4421f2a0e7284e17db440ee5b7be9f487ce9048f76970e7b6`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee998763c3cef90b11adda3322e66e1a89d89409d1ed29dd73a4101fb657e29`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a81b981d5dc89b19acce594b87914fc5bc4777e42b1322ca9b9d4c4b4f179`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.7 MB (1682335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ad6e4e7b1be08f8a79e4d77328648deded93f9ef0d4a1e8202ce4c3a21c67`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-builder` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:04b6c1b2519c8d35d65976c53b4523d7074d53c7b98fa5b29b83c837e021b493
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1956648108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c3e402a7640df51573fae3237803e1e5fabce3d4c88849d9513c716654d474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:19:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:19:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:20:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:20:18 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:20:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:20:42 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:22:59 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:23:01 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:04:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:04:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:43:30 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:43:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60407a49ce6121c65fa6399c333c5227a09518414fd987c460ea29cb441ac5a`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe632e8cddda4e5f347720b87b8b3868e2e2969048761e3b0a40799d33f5f7a`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4384696fc834e9658e7b3e5d1ceb1f8b362db85865daf29521b3c75c6999c046`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794ea611ef69f54d577f90b68e165e40a17e43b6d1d08f59951a38e084ea5fb`  
		Last Modified: Wed, 11 Oct 2023 02:45:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74dc2d701da2bfabc4d44e6a4e6b92912515e2ca1fb053ffcc6b0d5cae2972`  
		Last Modified: Wed, 11 Oct 2023 02:45:08 GMT  
		Size: 25.5 MB (25531724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91612399ba7df8de0a05ad078c3817548f0a3b44516b76565e14a96ea62452e9`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439c7c4353d2432c780827e4926910b19e84fe436d58e0a8129de2f631bd2b8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 264.4 KB (264384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0eaedd98e739ace4b7934261c71292195e461adcc977d02e57604d4a42ee8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f46e84d4d007a200b1d6e7cb5b48db90116cdeb8bd3ec3964a08191875973e2`  
		Last Modified: Wed, 11 Oct 2023 02:45:25 GMT  
		Size: 69.3 MB (69325670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59bab6d84ca44bbb60474dcf59c9af4f0f15edbdd64249b0eeaf968aff211f`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f449f4d34d707dbde9cbb245c154c0b2e1d1a2c55d172501f8d7da576866f76f`  
		Last Modified: Wed, 11 Oct 2023 04:06:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2edf76facdd17af03954b607484f7f7b36164a30634d19dd96b7320feb6b5`  
		Last Modified: Wed, 11 Oct 2023 04:06:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802c3686d509915fea71538d2c40c7a48c71719fab6144cb4497b6118b276ab9`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb183ed6cdad781eaba7bd1b4cb443befd9042c8a59450ee41f0245dd0ece4`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec33434b55fade6bcd7f3f0dfc10c981de93dc44bbae2b8702fdb6418a37a65b`  
		Last Modified: Thu, 12 Oct 2023 01:45:38 GMT  
		Size: 1.7 MB (1664788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0833369ef8236fcf99aba2d1fa48788db07662d0a9885a8429d435bf9f2227b2`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.5-builder-alpine`

```console
$ docker pull caddy@sha256:5eb7fee912aafef316ffeff206621c8ee11c12087512a0be0d301f39820dcb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `caddy:2.7.5-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:4306b19982d623e5bda44ecd050491f3f26e18c89d24ca703f293b696d44bd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d9c60a52301fa63992088de297d121e91e89e3971ba8e11ad1d1f0f7a9820`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:54:30 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:54:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:20:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:20:23 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:43:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:43:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:19:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:19:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc37b24bb09971feb8bf4882e861bce9db0c985a16a900adb0dc9de3f854243b`  
		Last Modified: Thu, 28 Sep 2023 22:57:15 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4303e95078c253686dcc16d7717644af63809efcbd753c0a999c9aad3fe72`  
		Last Modified: Tue, 10 Oct 2023 19:26:17 GMT  
		Size: 67.0 MB (67012876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359925be0f358b952dc8be63647139c5aab0fff94f7a070d88cb51dd258f80e5`  
		Last Modified: Tue, 10 Oct 2023 19:26:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fd04581de0d1e57432e3cd2d301b8c86d38131e671e2f9084c4220db3b8a4`  
		Last Modified: Tue, 10 Oct 2023 19:44:17 GMT  
		Size: 5.0 MB (4970359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f405302374c4e7ed3ee716677478b7a65c771aed696a6eae07cacab445c514c6`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 1.3 MB (1302237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8d8c97cfe8c049fd27a671cf8e75310a4c620478a949d0beecf3577e695ae5`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:eba60e558fae5eb5237067ab66dcea5b0c12a3860210e548c2d702c8181969c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75414943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92d489fb77472b86f5254b7c82bedc01dfea7685efa49eb568f03d34718623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:55:22 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:55:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:21 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:49:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:49:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:49:43 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:12:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:12:27 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 01:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 01:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 01:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3da3b9e7a12f6bb6b7f56e9240c2c92ce8c9f5fd5ef3b3063b9a93d454919e`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 284.9 KB (284887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbb7b34bc324d050e49d3dd31294bdde5d6ecda33decf9afe31c11165b138a`  
		Last Modified: Tue, 10 Oct 2023 18:55:32 GMT  
		Size: 65.8 MB (65770135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022f45a9fb1e7649eb4a663acd4ed6437363b4fc6e56f6af3e5f457a5d06ee8`  
		Last Modified: Tue, 10 Oct 2023 18:55:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f1d9e9fe803fc18e89adff41bb7ac628a0499482d0d9b990f99a35dd6d72`  
		Last Modified: Tue, 10 Oct 2023 19:12:49 GMT  
		Size: 5.0 MB (4965397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5054be6311f7b03470317d9f7de58e04e679de2bf5db25ef4c0ef371ff62462`  
		Last Modified: Thu, 12 Oct 2023 01:40:00 GMT  
		Size: 1.2 MB (1248668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2b52d0abb8a046b659afd73ff08c22a087e5dc281a68aa7e1fdb1b48899fe`  
		Last Modified: Thu, 12 Oct 2023 01:39:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9fe2fc9a7aefc762908d8eb62e1f5b715f5c6aa8fbce095cfa2c6d26d462e3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba881a693ec60b5a46375fb85340a3861d008aa7254e7601435adae2d1daf6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:15:15 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:15:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:03 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:58:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:58:20 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:23:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:23:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:03:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:03:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:03:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e0aec75477c9a2cf6993e068fa40a45f0684d622ece61f54e6e02f9adebeb8`  
		Last Modified: Thu, 28 Sep 2023 22:19:29 GMT  
		Size: 284.1 KB (284076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28294fad378329bf4a8672c4c0b712a9e59a45a66612808d85332f4503ebf8f`  
		Last Modified: Tue, 10 Oct 2023 19:05:18 GMT  
		Size: 65.8 MB (65770038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03c9df1b84980cdf17791dc62f86d15d95de066f16d394a456dd8aba48b`  
		Last Modified: Tue, 10 Oct 2023 19:04:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cea91cf5bb06feabb363f5a7b857daa22b1f08afffdfe56760ea0d4e5528cc`  
		Last Modified: Tue, 10 Oct 2023 19:23:34 GMT  
		Size: 4.5 MB (4512286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2b4a58da12fe13357fce681851d77bf6dd233fbd3791fed232ef9d0ef4d52`  
		Last Modified: Thu, 12 Oct 2023 18:04:16 GMT  
		Size: 1.2 MB (1246090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c7342ff285197b8280fd7f6ffd53f282c84c09c6258c8e469f73f113668c`  
		Last Modified: Thu, 12 Oct 2023 18:04:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:afafe5da37d6fc453c6723b1feced43da8d935cfb9d6a99ac4fa46a0d56ca293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73997154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ae4c57df7271ea7d1caabf80c85a272b845d804b2159b225e810bd662b1f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:03:38 GMT
RUN apk add --no-cache ca-certificates
# Fri, 29 Sep 2023 01:40:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:39:56 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:40:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:40:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:40:07 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:05:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:05:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 19:45:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 19:45:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 19:45:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c21914ef412ef71f6092299b025bf4d504a49024701bf684bc9efd218155c63`  
		Last Modified: Fri, 29 Sep 2023 01:03:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b559ff2a6180beeb7515cfd5be18fb2e6dff3732111ac2b0841e36d5ac501`  
		Last Modified: Tue, 10 Oct 2023 19:45:06 GMT  
		Size: 64.1 MB (64110940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b5a6e49d2cdb4e3cfb2aa71d9c6bda6e9d8869367c8a0617db2ba6c1ea01b`  
		Last Modified: Tue, 10 Oct 2023 19:44:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fab64598da5eee75f0f364bf43af2d126525ad1785fd9a0ea5dda73e6406402`  
		Last Modified: Tue, 10 Oct 2023 20:06:14 GMT  
		Size: 5.1 MB (5069056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b277a31c32e84a57ea24d6ef1c227259bbae4aebf8c7656219dd718a05d33292`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a4acb26609b7e59176aadb51d7dcb66727dfbb0d07901022dfd56eac253c9e`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.5-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:c0740b75861440c921e23bec00c2ce3e14bda7ca7967b2aec7855352ea96cd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `caddy:2.7.5-builder-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:951876270030a4a5404a8bab425d35b64f90babc594bb65c261cc05eab33ed79
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128478401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883908294a37d78f29e796d389d42c83a12c68a6c0f1113bba3bdd9290db5b05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:23:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:23:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:23:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:23:12 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:24:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:24:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:25:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:25:34 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:28:30 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:28:31 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:03:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:03:14 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:42:14 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:42:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fded5ce3c59d7e8d637a5536d6eed085ff6b6a323f42c1df76a7be6e9970ee`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a72a6b595ab9f8f71a34a065e75e609b20ea5e026f901820fce6d3c9134939`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2574f8b7fb0ec5a8c39ee40a8008f0d24c398380247bf7140be1abdede5542b`  
		Last Modified: Wed, 11 Oct 2023 02:46:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c53676fe729ebf5d3c07215d91afa952e6190715f79a7952f4c3aa121231e`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382bb149b70b82f9c2f58ebf6a2672dc4c64460017836d73a5a23b7379ea095`  
		Last Modified: Wed, 11 Oct 2023 02:46:44 GMT  
		Size: 25.6 MB (25557568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a2584f4b3b8f3038fa41c0719005822ab967d85d1231843bd729a7b3d2d60`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058e02ad62f976d823e3035f0578b2868eb09f28986153342a52014cc5c3810`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 284.8 KB (284754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fce039c31b2e60b62a0ede9974b6574519f2e47e1d8f4e09c7a1f30763aee95`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65449f183261f9bbdb731d41f5e6fca94f3e547e8d996133e418773400cfcfe`  
		Last Modified: Wed, 11 Oct 2023 02:46:59 GMT  
		Size: 69.3 MB (69345382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394e07c2ad53e950c47ffb647836822197dc5f8ebe082eaa045854e2b25bafc7`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f5e59c63ef5be894fc498ab0e165faa3129d35a8a8f5173f12c6a4232f588`  
		Last Modified: Wed, 11 Oct 2023 04:06:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c675831130735b443a544dff1b9c188928f34947a5342350ef04eadc0d1ab27`  
		Last Modified: Wed, 11 Oct 2023 04:06:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe7c1d1f5383a4421f2a0e7284e17db440ee5b7be9f487ce9048f76970e7b6`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee998763c3cef90b11adda3322e66e1a89d89409d1ed29dd73a4101fb657e29`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a81b981d5dc89b19acce594b87914fc5bc4777e42b1322ca9b9d4c4b4f179`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.7 MB (1682335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ad6e4e7b1be08f8a79e4d77328648deded93f9ef0d4a1e8202ce4c3a21c67`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.5-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7a4eaeb7416d6a4b442d55eab7e8c7824e36a07baef33353084b943d46b6b7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7.5-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:04b6c1b2519c8d35d65976c53b4523d7074d53c7b98fa5b29b83c837e021b493
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1956648108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c3e402a7640df51573fae3237803e1e5fabce3d4c88849d9513c716654d474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:19:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:19:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:20:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:20:18 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:20:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:20:42 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:22:59 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:23:01 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:04:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:04:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:43:30 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:43:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60407a49ce6121c65fa6399c333c5227a09518414fd987c460ea29cb441ac5a`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe632e8cddda4e5f347720b87b8b3868e2e2969048761e3b0a40799d33f5f7a`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4384696fc834e9658e7b3e5d1ceb1f8b362db85865daf29521b3c75c6999c046`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794ea611ef69f54d577f90b68e165e40a17e43b6d1d08f59951a38e084ea5fb`  
		Last Modified: Wed, 11 Oct 2023 02:45:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74dc2d701da2bfabc4d44e6a4e6b92912515e2ca1fb053ffcc6b0d5cae2972`  
		Last Modified: Wed, 11 Oct 2023 02:45:08 GMT  
		Size: 25.5 MB (25531724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91612399ba7df8de0a05ad078c3817548f0a3b44516b76565e14a96ea62452e9`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439c7c4353d2432c780827e4926910b19e84fe436d58e0a8129de2f631bd2b8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 264.4 KB (264384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0eaedd98e739ace4b7934261c71292195e461adcc977d02e57604d4a42ee8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f46e84d4d007a200b1d6e7cb5b48db90116cdeb8bd3ec3964a08191875973e2`  
		Last Modified: Wed, 11 Oct 2023 02:45:25 GMT  
		Size: 69.3 MB (69325670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59bab6d84ca44bbb60474dcf59c9af4f0f15edbdd64249b0eeaf968aff211f`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f449f4d34d707dbde9cbb245c154c0b2e1d1a2c55d172501f8d7da576866f76f`  
		Last Modified: Wed, 11 Oct 2023 04:06:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2edf76facdd17af03954b607484f7f7b36164a30634d19dd96b7320feb6b5`  
		Last Modified: Wed, 11 Oct 2023 04:06:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802c3686d509915fea71538d2c40c7a48c71719fab6144cb4497b6118b276ab9`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb183ed6cdad781eaba7bd1b4cb443befd9042c8a59450ee41f0245dd0ece4`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec33434b55fade6bcd7f3f0dfc10c981de93dc44bbae2b8702fdb6418a37a65b`  
		Last Modified: Thu, 12 Oct 2023 01:45:38 GMT  
		Size: 1.7 MB (1664788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0833369ef8236fcf99aba2d1fa48788db07662d0a9885a8429d435bf9f2227b2`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.5-windowsservercore`

```console
$ docker pull caddy@sha256:b859825f1b8093a4b961d02fb945e63f5180c5e07e56ce7495384835c016c47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7.5-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.5-windowsservercore` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.5-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8169d134dfa19ddbba9eeeb7210c5227c2a61f00906c340474aab1250aba47f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `caddy:2.7.5-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.5-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:278d32be7fb2f9a5e3f48ea6a672747dbb4ad6256e4802aff4a1e11a67e2e518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `caddy:2.7.5-windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:0157ce2e3977145c950dc562b339351cd37d06abe9ac8bf36b04b1b2f8ce6104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:aaa9d8750860e5b886fab8c4da6842782ec2eb2e963e6d48ad59657fadd9a6aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e21ab2b0efc5ac0207c16134ac96b3779212c692cde05a24f73a68fec756a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:43:13 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:43:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:19:15 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:19:17 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:19:18 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:19:19 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:19:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be51084fb891c6796079e693b73f6f882266a5e66211344173031e2b0c8ffd`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 350.8 KB (350826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d867aa37ac50364bf4082dc48c7d4e1b88ead3164d47855e1bbc2ef3678cfc`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a4bfabc0b0dc6924b7d8aad02805798c86ada09d9d11861f29ed76915f758`  
		Last Modified: Thu, 12 Oct 2023 18:19:43 GMT  
		Size: 14.7 MB (14713998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:be2cb3ef217d514df988a7fef43bc11cf8267f3c3eea319a82c6c4c2985cd7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17422254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375c06eba744fadf74e23a036a6af05a75573760968f9d65a405d7401973be3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:59:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 21:59:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 01:39:17 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:39:22 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:39:22 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 01:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1018057a600163b1c1b92c21ade975c631b2f8ccde66d524cfe0ecdac8e1920d`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 347.6 KB (347613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec54680cbf2cb1a25285c82a7888498ab47d03a68db200a160d7162325a5be19`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38012b56d72a4a2c2a42ed660476530218852cf8953587cb803fab0cf7de99c3`  
		Last Modified: Thu, 12 Oct 2023 01:39:46 GMT  
		Size: 13.9 MB (13921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cc67ef274e0b09f75c4adf46397b2b796c00d9d014d1312d53bc3e16fa763bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b853d3cd7e1ec8e5fdb884e061c15e6da29f25d0954bf803f08625dc542bf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:19:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 23:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:03:38 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:03:42 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:03:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66901ba48d0ee53cd827f4eb2cfd8b049cebba8c3d307b69760e1be917f69476`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 344.4 KB (344448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeb3f6febb36993d8a51ad919784fd152aab5f6e17fe00d579916f32e42911`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00371969ebc6f50beb432e93f29b2658ffdbf2de985784e17b0a8e696970a7d`  
		Last Modified: Thu, 12 Oct 2023 18:04:03 GMT  
		Size: 13.9 MB (13903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c5cdeee3505159e6a4ebd367b13f1a6bb32d424327be8ee4a3e09734c5cf63d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6797cb1033afffac8c55f0ee0f0dd9f60e58dc19ef1edc5852606eced4c793b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:16:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 01:16:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 19:45:02 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 80
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 19:45:05 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 19:45:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f21cb0286edf1f5fefb4a859b414a446bb81baa9e8901fc8f4eca55a43aeeec`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 360.6 KB (360643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444b3f9419d06a4b77a65935a3b1c6e657c607bcfb9e3bd1abebe57eae36e6a`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e60671cdfd4ec2cb64a788cecf65bb2166ba5bf3e7bba029ccf0c8c0dbeb3`  
		Last Modified: Thu, 12 Oct 2023 19:45:30 GMT  
		Size: 13.6 MB (13573811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:65084a14a1557b92af5b8ba6fcba9a7a710ed5caef1e2310f9622166608c9531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba45deaa04c3feac6474c22204ac6f5ebc380b331ff7d585ecd196284459b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:17:03 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 02:17:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Fri, 29 Sep 2023 02:17:06 GMT
ENV CADDY_VERSION=v2.7.4
# Fri, 29 Sep 2023 02:17:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 29 Sep 2023 02:17:13 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 29 Sep 2023 02:17:14 GMT
ENV XDG_DATA_HOME=/data
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 29 Sep 2023 02:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 29 Sep 2023 02:17:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 443
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 443/udp
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 2019
# Fri, 29 Sep 2023 02:17:24 GMT
WORKDIR /srv
# Fri, 29 Sep 2023 02:17:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa65cea7f5d70d1e203b851e43ad676e92f28c930ad32b6691e84ff9b5cda87`  
		Last Modified: Fri, 29 Sep 2023 02:18:03 GMT  
		Size: 362.2 KB (362182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7089a1d537371e29a65d106f43b45f2a0367d4d1db0eb7d6b7099f8ba05645`  
		Last Modified: Fri, 29 Sep 2023 02:18:01 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93ab741fa6270144ea59d6a5fa3c4138286a569f246fdccd829b317b051f3a`  
		Last Modified: Fri, 29 Sep 2023 02:18:05 GMT  
		Size: 13.2 MB (13228998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9e13bd2b56147eecc80f1fe1710e4350ea63d5edfb389fa89e2c6de06c08593a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17721238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f0101e0f893afb763d99b2050dbf4d68a44aae29785af6c05af5a552b0c1a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:19:38 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:19:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 28 Sep 2023 22:19:39 GMT
ENV CADDY_VERSION=v2.7.4
# Thu, 28 Sep 2023 22:19:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_DATA_HOME=/data
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 80
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443/udp
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 2019
# Thu, 28 Sep 2023 22:19:44 GMT
WORKDIR /srv
# Thu, 28 Sep 2023 22:19:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3df874173df47ad0bd0ef67b8ee598c77921810d84a67fd2984c4f8151c91`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a69c42a5c7fc6d73c00c7f6eb68522f3881aae55db4f85a8400e83b678b181`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793016dc78c9794c627c07afcd2fb34af4ee470ee7fef1a1596eff0c59ba6659`  
		Last Modified: Thu, 28 Sep 2023 22:20:16 GMT  
		Size: 14.1 MB (14143684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:493c52db91e0afa1fd7804f775be763188d075a528153780946c65eb91efc83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:4306b19982d623e5bda44ecd050491f3f26e18c89d24ca703f293b696d44bd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d9c60a52301fa63992088de297d121e91e89e3971ba8e11ad1d1f0f7a9820`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:54:30 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:54:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:20:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:20:23 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:43:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:43:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:19:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:19:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc37b24bb09971feb8bf4882e861bce9db0c985a16a900adb0dc9de3f854243b`  
		Last Modified: Thu, 28 Sep 2023 22:57:15 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4303e95078c253686dcc16d7717644af63809efcbd753c0a999c9aad3fe72`  
		Last Modified: Tue, 10 Oct 2023 19:26:17 GMT  
		Size: 67.0 MB (67012876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359925be0f358b952dc8be63647139c5aab0fff94f7a070d88cb51dd258f80e5`  
		Last Modified: Tue, 10 Oct 2023 19:26:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fd04581de0d1e57432e3cd2d301b8c86d38131e671e2f9084c4220db3b8a4`  
		Last Modified: Tue, 10 Oct 2023 19:44:17 GMT  
		Size: 5.0 MB (4970359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f405302374c4e7ed3ee716677478b7a65c771aed696a6eae07cacab445c514c6`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 1.3 MB (1302237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8d8c97cfe8c049fd27a671cf8e75310a4c620478a949d0beecf3577e695ae5`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:eba60e558fae5eb5237067ab66dcea5b0c12a3860210e548c2d702c8181969c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75414943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92d489fb77472b86f5254b7c82bedc01dfea7685efa49eb568f03d34718623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:55:22 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:55:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:21 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:49:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:49:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:49:43 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:12:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:12:27 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 01:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 01:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 01:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3da3b9e7a12f6bb6b7f56e9240c2c92ce8c9f5fd5ef3b3063b9a93d454919e`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 284.9 KB (284887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbb7b34bc324d050e49d3dd31294bdde5d6ecda33decf9afe31c11165b138a`  
		Last Modified: Tue, 10 Oct 2023 18:55:32 GMT  
		Size: 65.8 MB (65770135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022f45a9fb1e7649eb4a663acd4ed6437363b4fc6e56f6af3e5f457a5d06ee8`  
		Last Modified: Tue, 10 Oct 2023 18:55:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f1d9e9fe803fc18e89adff41bb7ac628a0499482d0d9b990f99a35dd6d72`  
		Last Modified: Tue, 10 Oct 2023 19:12:49 GMT  
		Size: 5.0 MB (4965397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5054be6311f7b03470317d9f7de58e04e679de2bf5db25ef4c0ef371ff62462`  
		Last Modified: Thu, 12 Oct 2023 01:40:00 GMT  
		Size: 1.2 MB (1248668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2b52d0abb8a046b659afd73ff08c22a087e5dc281a68aa7e1fdb1b48899fe`  
		Last Modified: Thu, 12 Oct 2023 01:39:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9fe2fc9a7aefc762908d8eb62e1f5b715f5c6aa8fbce095cfa2c6d26d462e3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba881a693ec60b5a46375fb85340a3861d008aa7254e7601435adae2d1daf6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:15:15 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:15:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:03 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:58:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:58:20 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:23:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:23:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:03:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:03:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:03:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e0aec75477c9a2cf6993e068fa40a45f0684d622ece61f54e6e02f9adebeb8`  
		Last Modified: Thu, 28 Sep 2023 22:19:29 GMT  
		Size: 284.1 KB (284076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28294fad378329bf4a8672c4c0b712a9e59a45a66612808d85332f4503ebf8f`  
		Last Modified: Tue, 10 Oct 2023 19:05:18 GMT  
		Size: 65.8 MB (65770038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03c9df1b84980cdf17791dc62f86d15d95de066f16d394a456dd8aba48b`  
		Last Modified: Tue, 10 Oct 2023 19:04:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cea91cf5bb06feabb363f5a7b857daa22b1f08afffdfe56760ea0d4e5528cc`  
		Last Modified: Tue, 10 Oct 2023 19:23:34 GMT  
		Size: 4.5 MB (4512286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2b4a58da12fe13357fce681851d77bf6dd233fbd3791fed232ef9d0ef4d52`  
		Last Modified: Thu, 12 Oct 2023 18:04:16 GMT  
		Size: 1.2 MB (1246090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c7342ff285197b8280fd7f6ffd53f282c84c09c6258c8e469f73f113668c`  
		Last Modified: Thu, 12 Oct 2023 18:04:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:afafe5da37d6fc453c6723b1feced43da8d935cfb9d6a99ac4fa46a0d56ca293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73997154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ae4c57df7271ea7d1caabf80c85a272b845d804b2159b225e810bd662b1f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:03:38 GMT
RUN apk add --no-cache ca-certificates
# Fri, 29 Sep 2023 01:40:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:39:56 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:40:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:40:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:40:07 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:05:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:05:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 19:45:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 19:45:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 19:45:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c21914ef412ef71f6092299b025bf4d504a49024701bf684bc9efd218155c63`  
		Last Modified: Fri, 29 Sep 2023 01:03:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b559ff2a6180beeb7515cfd5be18fb2e6dff3732111ac2b0841e36d5ac501`  
		Last Modified: Tue, 10 Oct 2023 19:45:06 GMT  
		Size: 64.1 MB (64110940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b5a6e49d2cdb4e3cfb2aa71d9c6bda6e9d8869367c8a0617db2ba6c1ea01b`  
		Last Modified: Tue, 10 Oct 2023 19:44:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fab64598da5eee75f0f364bf43af2d126525ad1785fd9a0ea5dda73e6406402`  
		Last Modified: Tue, 10 Oct 2023 20:06:14 GMT  
		Size: 5.1 MB (5069056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b277a31c32e84a57ea24d6ef1c227259bbae4aebf8c7656219dd718a05d33292`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a4acb26609b7e59176aadb51d7dcb66727dfbb0d07901022dfd56eac253c9e`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:8ccaa0a876d91c973bd880880eb16fb0a23ed96189c2b2df3a8c774c109edb07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74214371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210df7ee91e01af6665deb0296b08fe5553d0e0596c0fcc573f087b3da068993`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:13:11 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:13:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:17:44 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:18:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:18:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:18:17 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:46:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:46:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 19:46:41 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 19:46:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 19:46:43 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 19:46:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 19:46:45 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 19:46:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc67971d1767eae5019ffeaf8f893e6d81dbba50bde347da0c0433c56e3f2a3`  
		Last Modified: Thu, 28 Sep 2023 22:18:17 GMT  
		Size: 286.7 KB (286659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caf7fa003bdf7c7611eb2e33a11db077a0f632b70d28f5b73096bf051f25aeb`  
		Last Modified: Tue, 10 Oct 2023 19:28:09 GMT  
		Size: 64.1 MB (64125245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9573c5aef56335266ce720d0812f9a0156f628fbd01ba4a6462be56d8742dc8a`  
		Last Modified: Tue, 10 Oct 2023 19:27:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70c30dd200f1712a117ee42ac94a48f111b3d3e482ec05db53cafffc7b35dcf`  
		Last Modified: Tue, 10 Oct 2023 19:47:06 GMT  
		Size: 5.3 MB (5269226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2504109ddadb5c2133e7cfbb1caebb5de6f6c1effa9742ac36eec52a9751a110`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 1.2 MB (1186172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f92baeaf213968278b040b2fc465a59b7027c402bbc58f9ab15658a19e1341`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:ae945b58f882ac574669765568acbf43619d6da9e312750f5e3f4bf323ff64fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76113604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4b9728b30637022d501d3a2858327e288ef5e7fbc14bdbe43a06d71844717a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:38:54 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:38:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:43:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:43:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:43:39 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:00:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 20:00:02 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 20:00:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 20:00:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 20:00:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721f16693d4788a5add1bd0b22764c8887cdc62b24edf388ae895df440f4aa9`  
		Last Modified: Thu, 28 Sep 2023 21:46:22 GMT  
		Size: 285.1 KB (285095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa850520bfe7c982afe0c271ec09526214f569f386fba4c4fc8e4c4ee1b3b536`  
		Last Modified: Tue, 10 Oct 2023 19:40:41 GMT  
		Size: 66.2 MB (66235247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6466a1a32b54238d2aab33605db66c5f9b58dc02e3d202483ebca7dddea04aa5`  
		Last Modified: Tue, 10 Oct 2023 19:40:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bcbbdd4f9b04ca7467a549aa3d4110cbc2dab3bb78f1643c27992f4c0d82c3`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 5.1 MB (5115210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2e4e8bdf6b9562139094c05c60d87a303098f59919f4c20403ba5d815b300`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 1.3 MB (1262388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca343226e4d88ff4f38e0b18cf13f8a1d73a45cee5de97aed1fc8383b8003ca`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:951876270030a4a5404a8bab425d35b64f90babc594bb65c261cc05eab33ed79
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128478401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883908294a37d78f29e796d389d42c83a12c68a6c0f1113bba3bdd9290db5b05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:23:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:23:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:23:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:23:12 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:24:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:24:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:25:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:25:34 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:28:30 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:28:31 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:03:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:03:14 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:42:14 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:42:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fded5ce3c59d7e8d637a5536d6eed085ff6b6a323f42c1df76a7be6e9970ee`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a72a6b595ab9f8f71a34a065e75e609b20ea5e026f901820fce6d3c9134939`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2574f8b7fb0ec5a8c39ee40a8008f0d24c398380247bf7140be1abdede5542b`  
		Last Modified: Wed, 11 Oct 2023 02:46:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c53676fe729ebf5d3c07215d91afa952e6190715f79a7952f4c3aa121231e`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382bb149b70b82f9c2f58ebf6a2672dc4c64460017836d73a5a23b7379ea095`  
		Last Modified: Wed, 11 Oct 2023 02:46:44 GMT  
		Size: 25.6 MB (25557568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a2584f4b3b8f3038fa41c0719005822ab967d85d1231843bd729a7b3d2d60`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058e02ad62f976d823e3035f0578b2868eb09f28986153342a52014cc5c3810`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 284.8 KB (284754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fce039c31b2e60b62a0ede9974b6574519f2e47e1d8f4e09c7a1f30763aee95`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65449f183261f9bbdb731d41f5e6fca94f3e547e8d996133e418773400cfcfe`  
		Last Modified: Wed, 11 Oct 2023 02:46:59 GMT  
		Size: 69.3 MB (69345382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394e07c2ad53e950c47ffb647836822197dc5f8ebe082eaa045854e2b25bafc7`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f5e59c63ef5be894fc498ab0e165faa3129d35a8a8f5173f12c6a4232f588`  
		Last Modified: Wed, 11 Oct 2023 04:06:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c675831130735b443a544dff1b9c188928f34947a5342350ef04eadc0d1ab27`  
		Last Modified: Wed, 11 Oct 2023 04:06:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe7c1d1f5383a4421f2a0e7284e17db440ee5b7be9f487ce9048f76970e7b6`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee998763c3cef90b11adda3322e66e1a89d89409d1ed29dd73a4101fb657e29`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a81b981d5dc89b19acce594b87914fc5bc4777e42b1322ca9b9d4c4b4f179`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.7 MB (1682335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ad6e4e7b1be08f8a79e4d77328648deded93f9ef0d4a1e8202ce4c3a21c67`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:04b6c1b2519c8d35d65976c53b4523d7074d53c7b98fa5b29b83c837e021b493
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1956648108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c3e402a7640df51573fae3237803e1e5fabce3d4c88849d9513c716654d474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:19:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:19:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:20:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:20:18 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:20:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:20:42 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:22:59 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:23:01 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:04:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:04:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:43:30 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:43:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60407a49ce6121c65fa6399c333c5227a09518414fd987c460ea29cb441ac5a`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe632e8cddda4e5f347720b87b8b3868e2e2969048761e3b0a40799d33f5f7a`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4384696fc834e9658e7b3e5d1ceb1f8b362db85865daf29521b3c75c6999c046`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794ea611ef69f54d577f90b68e165e40a17e43b6d1d08f59951a38e084ea5fb`  
		Last Modified: Wed, 11 Oct 2023 02:45:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74dc2d701da2bfabc4d44e6a4e6b92912515e2ca1fb053ffcc6b0d5cae2972`  
		Last Modified: Wed, 11 Oct 2023 02:45:08 GMT  
		Size: 25.5 MB (25531724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91612399ba7df8de0a05ad078c3817548f0a3b44516b76565e14a96ea62452e9`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439c7c4353d2432c780827e4926910b19e84fe436d58e0a8129de2f631bd2b8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 264.4 KB (264384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0eaedd98e739ace4b7934261c71292195e461adcc977d02e57604d4a42ee8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f46e84d4d007a200b1d6e7cb5b48db90116cdeb8bd3ec3964a08191875973e2`  
		Last Modified: Wed, 11 Oct 2023 02:45:25 GMT  
		Size: 69.3 MB (69325670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59bab6d84ca44bbb60474dcf59c9af4f0f15edbdd64249b0eeaf968aff211f`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f449f4d34d707dbde9cbb245c154c0b2e1d1a2c55d172501f8d7da576866f76f`  
		Last Modified: Wed, 11 Oct 2023 04:06:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2edf76facdd17af03954b607484f7f7b36164a30634d19dd96b7320feb6b5`  
		Last Modified: Wed, 11 Oct 2023 04:06:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802c3686d509915fea71538d2c40c7a48c71719fab6144cb4497b6118b276ab9`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb183ed6cdad781eaba7bd1b4cb443befd9042c8a59450ee41f0245dd0ece4`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec33434b55fade6bcd7f3f0dfc10c981de93dc44bbae2b8702fdb6418a37a65b`  
		Last Modified: Thu, 12 Oct 2023 01:45:38 GMT  
		Size: 1.7 MB (1664788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0833369ef8236fcf99aba2d1fa48788db07662d0a9885a8429d435bf9f2227b2`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:fbf0444d9829e43a97cb98d36ae346b6e11682a766701ff61efad79231ce69d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:4306b19982d623e5bda44ecd050491f3f26e18c89d24ca703f293b696d44bd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d9c60a52301fa63992088de297d121e91e89e3971ba8e11ad1d1f0f7a9820`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:54:30 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:54:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:20:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:20:22 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:20:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:20:23 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:43:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:43:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:19:22 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:19:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:19:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc37b24bb09971feb8bf4882e861bce9db0c985a16a900adb0dc9de3f854243b`  
		Last Modified: Thu, 28 Sep 2023 22:57:15 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4303e95078c253686dcc16d7717644af63809efcbd753c0a999c9aad3fe72`  
		Last Modified: Tue, 10 Oct 2023 19:26:17 GMT  
		Size: 67.0 MB (67012876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359925be0f358b952dc8be63647139c5aab0fff94f7a070d88cb51dd258f80e5`  
		Last Modified: Tue, 10 Oct 2023 19:26:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fd04581de0d1e57432e3cd2d301b8c86d38131e671e2f9084c4220db3b8a4`  
		Last Modified: Tue, 10 Oct 2023 19:44:17 GMT  
		Size: 5.0 MB (4970359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f405302374c4e7ed3ee716677478b7a65c771aed696a6eae07cacab445c514c6`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 1.3 MB (1302237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8d8c97cfe8c049fd27a671cf8e75310a4c620478a949d0beecf3577e695ae5`  
		Last Modified: Thu, 12 Oct 2023 18:19:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:eba60e558fae5eb5237067ab66dcea5b0c12a3860210e548c2d702c8181969c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75414943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92d489fb77472b86f5254b7c82bedc01dfea7685efa49eb568f03d34718623`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:55:22 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:55:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:21 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:49:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:49:42 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:49:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:49:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:49:43 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:12:27 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:12:27 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:39:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 01:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 01:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 01:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3da3b9e7a12f6bb6b7f56e9240c2c92ce8c9f5fd5ef3b3063b9a93d454919e`  
		Last Modified: Thu, 28 Sep 2023 21:58:05 GMT  
		Size: 284.9 KB (284887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbb7b34bc324d050e49d3dd31294bdde5d6ecda33decf9afe31c11165b138a`  
		Last Modified: Tue, 10 Oct 2023 18:55:32 GMT  
		Size: 65.8 MB (65770135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c022f45a9fb1e7649eb4a663acd4ed6437363b4fc6e56f6af3e5f457a5d06ee8`  
		Last Modified: Tue, 10 Oct 2023 18:55:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f1d9e9fe803fc18e89adff41bb7ac628a0499482d0d9b990f99a35dd6d72`  
		Last Modified: Tue, 10 Oct 2023 19:12:49 GMT  
		Size: 5.0 MB (4965397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5054be6311f7b03470317d9f7de58e04e679de2bf5db25ef4c0ef371ff62462`  
		Last Modified: Thu, 12 Oct 2023 01:40:00 GMT  
		Size: 1.2 MB (1248668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2b52d0abb8a046b659afd73ff08c22a087e5dc281a68aa7e1fdb1b48899fe`  
		Last Modified: Thu, 12 Oct 2023 01:39:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9fe2fc9a7aefc762908d8eb62e1f5b715f5c6aa8fbce095cfa2c6d26d462e3af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74712961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba881a693ec60b5a46375fb85340a3861d008aa7254e7601435adae2d1daf6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:15:15 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:15:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:03 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:58:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:58:19 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:58:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:58:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:58:20 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:23:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:23:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 18:03:45 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 18:03:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 18:03:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 18:03:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e0aec75477c9a2cf6993e068fa40a45f0684d622ece61f54e6e02f9adebeb8`  
		Last Modified: Thu, 28 Sep 2023 22:19:29 GMT  
		Size: 284.1 KB (284076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28294fad378329bf4a8672c4c0b712a9e59a45a66612808d85332f4503ebf8f`  
		Last Modified: Tue, 10 Oct 2023 19:05:18 GMT  
		Size: 65.8 MB (65770038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729af03c9df1b84980cdf17791dc62f86d15d95de066f16d394a456dd8aba48b`  
		Last Modified: Tue, 10 Oct 2023 19:04:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cea91cf5bb06feabb363f5a7b857daa22b1f08afffdfe56760ea0d4e5528cc`  
		Last Modified: Tue, 10 Oct 2023 19:23:34 GMT  
		Size: 4.5 MB (4512286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2b4a58da12fe13357fce681851d77bf6dd233fbd3791fed232ef9d0ef4d52`  
		Last Modified: Thu, 12 Oct 2023 18:04:16 GMT  
		Size: 1.2 MB (1246090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1946c7342ff285197b8280fd7f6ffd53f282c84c09c6258c8e469f73f113668c`  
		Last Modified: Thu, 12 Oct 2023 18:04:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:afafe5da37d6fc453c6723b1feced43da8d935cfb9d6a99ac4fa46a0d56ca293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73997154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113ae4c57df7271ea7d1caabf80c85a272b845d804b2159b225e810bd662b1f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:03:38 GMT
RUN apk add --no-cache ca-certificates
# Fri, 29 Sep 2023 01:40:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:39:56 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:40:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:40:06 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:40:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:40:07 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:05:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:05:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 19:45:08 GMT
ENV XCADDY_SETCAP=1
# Thu, 12 Oct 2023 19:45:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 12 Oct 2023 19:45:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 12 Oct 2023 19:45:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c21914ef412ef71f6092299b025bf4d504a49024701bf684bc9efd218155c63`  
		Last Modified: Fri, 29 Sep 2023 01:03:48 GMT  
		Size: 286.3 KB (286306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b559ff2a6180beeb7515cfd5be18fb2e6dff3732111ac2b0841e36d5ac501`  
		Last Modified: Tue, 10 Oct 2023 19:45:06 GMT  
		Size: 64.1 MB (64110940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b5a6e49d2cdb4e3cfb2aa71d9c6bda6e9d8869367c8a0617db2ba6c1ea01b`  
		Last Modified: Tue, 10 Oct 2023 19:44:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fab64598da5eee75f0f364bf43af2d126525ad1785fd9a0ea5dda73e6406402`  
		Last Modified: Tue, 10 Oct 2023 20:06:14 GMT  
		Size: 5.1 MB (5069056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b277a31c32e84a57ea24d6ef1c227259bbae4aebf8c7656219dd718a05d33292`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 1.2 MB (1198456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a4acb26609b7e59176aadb51d7dcb66727dfbb0d07901022dfd56eac253c9e`  
		Last Modified: Thu, 12 Oct 2023 19:45:45 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8ccaa0a876d91c973bd880880eb16fb0a23ed96189c2b2df3a8c774c109edb07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74214371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210df7ee91e01af6665deb0296b08fe5553d0e0596c0fcc573f087b3da068993`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:13:11 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 22:13:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:17:44 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 19:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 19:18:14 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 19:18:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 19:18:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 19:18:17 GMT
WORKDIR /go
# Tue, 10 Oct 2023 19:46:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 19:46:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 19:46:41 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 19:46:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 19:46:43 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 19:46:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 19:46:45 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 19:46:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc67971d1767eae5019ffeaf8f893e6d81dbba50bde347da0c0433c56e3f2a3`  
		Last Modified: Thu, 28 Sep 2023 22:18:17 GMT  
		Size: 286.7 KB (286659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caf7fa003bdf7c7611eb2e33a11db077a0f632b70d28f5b73096bf051f25aeb`  
		Last Modified: Tue, 10 Oct 2023 19:28:09 GMT  
		Size: 64.1 MB (64125245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9573c5aef56335266ce720d0812f9a0156f628fbd01ba4a6462be56d8742dc8a`  
		Last Modified: Tue, 10 Oct 2023 19:27:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70c30dd200f1712a117ee42ac94a48f111b3d3e482ec05db53cafffc7b35dcf`  
		Last Modified: Tue, 10 Oct 2023 19:47:06 GMT  
		Size: 5.3 MB (5269226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2504109ddadb5c2133e7cfbb1caebb5de6f6c1effa9742ac36eec52a9751a110`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 1.2 MB (1186172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f92baeaf213968278b040b2fc465a59b7027c402bbc58f9ab15658a19e1341`  
		Last Modified: Tue, 10 Oct 2023 19:47:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:ae945b58f882ac574669765568acbf43619d6da9e312750f5e3f4bf323ff64fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76113604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4b9728b30637022d501d3a2858327e288ef5e7fbc14bdbe43a06d71844717a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:38:54 GMT
RUN apk add --no-cache ca-certificates
# Thu, 28 Sep 2023 21:38:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:11 GMT
ENV GOLANG_VERSION=1.21.3
# Tue, 10 Oct 2023 18:43:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Oct 2023 18:43:38 GMT
ENV GOPATH=/go
# Tue, 10 Oct 2023 18:43:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 18:43:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 10 Oct 2023 18:43:39 GMT
WORKDIR /go
# Tue, 10 Oct 2023 20:00:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 10 Oct 2023 20:00:02 GMT
ENV CADDY_VERSION=v2.7.4
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Oct 2023 20:00:02 GMT
ENV XCADDY_SETCAP=1
# Tue, 10 Oct 2023 20:00:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 10 Oct 2023 20:00:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 10 Oct 2023 20:00:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721f16693d4788a5add1bd0b22764c8887cdc62b24edf388ae895df440f4aa9`  
		Last Modified: Thu, 28 Sep 2023 21:46:22 GMT  
		Size: 285.1 KB (285095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa850520bfe7c982afe0c271ec09526214f569f386fba4c4fc8e4c4ee1b3b536`  
		Last Modified: Tue, 10 Oct 2023 19:40:41 GMT  
		Size: 66.2 MB (66235247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6466a1a32b54238d2aab33605db66c5f9b58dc02e3d202483ebca7dddea04aa5`  
		Last Modified: Tue, 10 Oct 2023 19:40:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bcbbdd4f9b04ca7467a549aa3d4110cbc2dab3bb78f1643c27992f4c0d82c3`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 5.1 MB (5115210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a2e4e8bdf6b9562139094c05c60d87a303098f59919f4c20403ba5d815b300`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 1.3 MB (1262388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca343226e4d88ff4f38e0b18cf13f8a1d73a45cee5de97aed1fc8383b8003ca`  
		Last Modified: Tue, 10 Oct 2023 20:00:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:c0740b75861440c921e23bec00c2ce3e14bda7ca7967b2aec7855352ea96cd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:951876270030a4a5404a8bab425d35b64f90babc594bb65c261cc05eab33ed79
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128478401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883908294a37d78f29e796d389d42c83a12c68a6c0f1113bba3bdd9290db5b05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:23:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:23:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:23:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:23:12 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:24:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:24:31 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:25:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:25:34 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:28:30 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:28:31 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:03:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:03:14 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:42:14 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:42:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fded5ce3c59d7e8d637a5536d6eed085ff6b6a323f42c1df76a7be6e9970ee`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a72a6b595ab9f8f71a34a065e75e609b20ea5e026f901820fce6d3c9134939`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2574f8b7fb0ec5a8c39ee40a8008f0d24c398380247bf7140be1abdede5542b`  
		Last Modified: Wed, 11 Oct 2023 02:46:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951c53676fe729ebf5d3c07215d91afa952e6190715f79a7952f4c3aa121231e`  
		Last Modified: Wed, 11 Oct 2023 02:46:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382bb149b70b82f9c2f58ebf6a2672dc4c64460017836d73a5a23b7379ea095`  
		Last Modified: Wed, 11 Oct 2023 02:46:44 GMT  
		Size: 25.6 MB (25557568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608a2584f4b3b8f3038fa41c0719005822ab967d85d1231843bd729a7b3d2d60`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1058e02ad62f976d823e3035f0578b2868eb09f28986153342a52014cc5c3810`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 284.8 KB (284754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fce039c31b2e60b62a0ede9974b6574519f2e47e1d8f4e09c7a1f30763aee95`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65449f183261f9bbdb731d41f5e6fca94f3e547e8d996133e418773400cfcfe`  
		Last Modified: Wed, 11 Oct 2023 02:46:59 GMT  
		Size: 69.3 MB (69345382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394e07c2ad53e950c47ffb647836822197dc5f8ebe082eaa045854e2b25bafc7`  
		Last Modified: Wed, 11 Oct 2023 02:46:37 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f5e59c63ef5be894fc498ab0e165faa3129d35a8a8f5173f12c6a4232f588`  
		Last Modified: Wed, 11 Oct 2023 04:06:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c675831130735b443a544dff1b9c188928f34947a5342350ef04eadc0d1ab27`  
		Last Modified: Wed, 11 Oct 2023 04:06:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe7c1d1f5383a4421f2a0e7284e17db440ee5b7be9f487ce9048f76970e7b6`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee998763c3cef90b11adda3322e66e1a89d89409d1ed29dd73a4101fb657e29`  
		Last Modified: Thu, 12 Oct 2023 01:45:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a81b981d5dc89b19acce594b87914fc5bc4777e42b1322ca9b9d4c4b4f179`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.7 MB (1682335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ad6e4e7b1be08f8a79e4d77328648deded93f9ef0d4a1e8202ce4c3a21c67`  
		Last Modified: Thu, 12 Oct 2023 01:45:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7a4eaeb7416d6a4b442d55eab7e8c7824e36a07baef33353084b943d46b6b7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:04b6c1b2519c8d35d65976c53b4523d7074d53c7b98fa5b29b83c837e021b493
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1956648108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c3e402a7640df51573fae3237803e1e5fabce3d4c88849d9513c716654d474`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Oct 2023 02:19:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Oct 2023 02:19:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Oct 2023 02:19:43 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Oct 2023 02:20:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:20:18 GMT
ENV GOPATH=C:\go
# Wed, 11 Oct 2023 02:20:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Oct 2023 02:20:42 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 11 Oct 2023 02:22:59 GMT
RUN $url = 'https://dl.google.com/go/go1.21.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27c8daf157493f288d42a6f38debc6a2cb391f6543139eba9152fceca0be2a10'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:23:01 GMT
WORKDIR C:\go
# Wed, 11 Oct 2023 04:04:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:04:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Thu, 12 Oct 2023 01:43:30 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:43:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 12 Oct 2023 01:43:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 12 Oct 2023 01:43:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60407a49ce6121c65fa6399c333c5227a09518414fd987c460ea29cb441ac5a`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe632e8cddda4e5f347720b87b8b3868e2e2969048761e3b0a40799d33f5f7a`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4384696fc834e9658e7b3e5d1ceb1f8b362db85865daf29521b3c75c6999c046`  
		Last Modified: Wed, 11 Oct 2023 02:45:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794ea611ef69f54d577f90b68e165e40a17e43b6d1d08f59951a38e084ea5fb`  
		Last Modified: Wed, 11 Oct 2023 02:45:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c74dc2d701da2bfabc4d44e6a4e6b92912515e2ca1fb053ffcc6b0d5cae2972`  
		Last Modified: Wed, 11 Oct 2023 02:45:08 GMT  
		Size: 25.5 MB (25531724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91612399ba7df8de0a05ad078c3817548f0a3b44516b76565e14a96ea62452e9`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439c7c4353d2432c780827e4926910b19e84fe436d58e0a8129de2f631bd2b8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 264.4 KB (264384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0eaedd98e739ace4b7934261c71292195e461adcc977d02e57604d4a42ee8`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f46e84d4d007a200b1d6e7cb5b48db90116cdeb8bd3ec3964a08191875973e2`  
		Last Modified: Wed, 11 Oct 2023 02:45:25 GMT  
		Size: 69.3 MB (69325670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f59bab6d84ca44bbb60474dcf59c9af4f0f15edbdd64249b0eeaf968aff211f`  
		Last Modified: Wed, 11 Oct 2023 02:45:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f449f4d34d707dbde9cbb245c154c0b2e1d1a2c55d172501f8d7da576866f76f`  
		Last Modified: Wed, 11 Oct 2023 04:06:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2edf76facdd17af03954b607484f7f7b36164a30634d19dd96b7320feb6b5`  
		Last Modified: Wed, 11 Oct 2023 04:06:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802c3686d509915fea71538d2c40c7a48c71719fab6144cb4497b6118b276ab9`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb183ed6cdad781eaba7bd1b4cb443befd9042c8a59450ee41f0245dd0ece4`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec33434b55fade6bcd7f3f0dfc10c981de93dc44bbae2b8702fdb6418a37a65b`  
		Last Modified: Thu, 12 Oct 2023 01:45:38 GMT  
		Size: 1.7 MB (1664788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0833369ef8236fcf99aba2d1fa48788db07662d0a9885a8429d435bf9f2227b2`  
		Last Modified: Thu, 12 Oct 2023 01:45:37 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:db7fa54ce8d507a6c22cdf0ee9cd5229747d8f552c83912b0c5427b92e6e271c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:aaa9d8750860e5b886fab8c4da6842782ec2eb2e963e6d48ad59657fadd9a6aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e21ab2b0efc5ac0207c16134ac96b3779212c692cde05a24f73a68fec756a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:43:13 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:43:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:19:15 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:19:17 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:19:18 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:19:19 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:19:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be51084fb891c6796079e693b73f6f882266a5e66211344173031e2b0c8ffd`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 350.8 KB (350826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d867aa37ac50364bf4082dc48c7d4e1b88ead3164d47855e1bbc2ef3678cfc`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a4bfabc0b0dc6924b7d8aad02805798c86ada09d9d11861f29ed76915f758`  
		Last Modified: Thu, 12 Oct 2023 18:19:43 GMT  
		Size: 14.7 MB (14713998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:be2cb3ef217d514df988a7fef43bc11cf8267f3c3eea319a82c6c4c2985cd7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17422254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375c06eba744fadf74e23a036a6af05a75573760968f9d65a405d7401973be3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:59:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 21:59:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 01:39:17 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:39:22 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:39:22 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 01:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1018057a600163b1c1b92c21ade975c631b2f8ccde66d524cfe0ecdac8e1920d`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 347.6 KB (347613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec54680cbf2cb1a25285c82a7888498ab47d03a68db200a160d7162325a5be19`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38012b56d72a4a2c2a42ed660476530218852cf8953587cb803fab0cf7de99c3`  
		Last Modified: Thu, 12 Oct 2023 01:39:46 GMT  
		Size: 13.9 MB (13921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cc67ef274e0b09f75c4adf46397b2b796c00d9d014d1312d53bc3e16fa763bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b853d3cd7e1ec8e5fdb884e061c15e6da29f25d0954bf803f08625dc542bf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:19:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 23:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:03:38 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:03:42 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:03:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66901ba48d0ee53cd827f4eb2cfd8b049cebba8c3d307b69760e1be917f69476`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 344.4 KB (344448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeb3f6febb36993d8a51ad919784fd152aab5f6e17fe00d579916f32e42911`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00371969ebc6f50beb432e93f29b2658ffdbf2de985784e17b0a8e696970a7d`  
		Last Modified: Thu, 12 Oct 2023 18:04:03 GMT  
		Size: 13.9 MB (13903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c5cdeee3505159e6a4ebd367b13f1a6bb32d424327be8ee4a3e09734c5cf63d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6797cb1033afffac8c55f0ee0f0dd9f60e58dc19ef1edc5852606eced4c793b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:16:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 01:16:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 19:45:02 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 80
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 19:45:05 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 19:45:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f21cb0286edf1f5fefb4a859b414a446bb81baa9e8901fc8f4eca55a43aeeec`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 360.6 KB (360643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444b3f9419d06a4b77a65935a3b1c6e657c607bcfb9e3bd1abebe57eae36e6a`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e60671cdfd4ec2cb64a788cecf65bb2166ba5bf3e7bba029ccf0c8c0dbeb3`  
		Last Modified: Thu, 12 Oct 2023 19:45:30 GMT  
		Size: 13.6 MB (13573811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:65084a14a1557b92af5b8ba6fcba9a7a710ed5caef1e2310f9622166608c9531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba45deaa04c3feac6474c22204ac6f5ebc380b331ff7d585ecd196284459b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:17:03 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 02:17:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Fri, 29 Sep 2023 02:17:06 GMT
ENV CADDY_VERSION=v2.7.4
# Fri, 29 Sep 2023 02:17:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 29 Sep 2023 02:17:13 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 29 Sep 2023 02:17:14 GMT
ENV XDG_DATA_HOME=/data
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 29 Sep 2023 02:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 29 Sep 2023 02:17:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 443
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 443/udp
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 2019
# Fri, 29 Sep 2023 02:17:24 GMT
WORKDIR /srv
# Fri, 29 Sep 2023 02:17:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa65cea7f5d70d1e203b851e43ad676e92f28c930ad32b6691e84ff9b5cda87`  
		Last Modified: Fri, 29 Sep 2023 02:18:03 GMT  
		Size: 362.2 KB (362182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7089a1d537371e29a65d106f43b45f2a0367d4d1db0eb7d6b7099f8ba05645`  
		Last Modified: Fri, 29 Sep 2023 02:18:01 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93ab741fa6270144ea59d6a5fa3c4138286a569f246fdccd829b317b051f3a`  
		Last Modified: Fri, 29 Sep 2023 02:18:05 GMT  
		Size: 13.2 MB (13228998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:9e13bd2b56147eecc80f1fe1710e4350ea63d5edfb389fa89e2c6de06c08593a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17721238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f0101e0f893afb763d99b2050dbf4d68a44aae29785af6c05af5a552b0c1a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:19:38 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:19:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 28 Sep 2023 22:19:39 GMT
ENV CADDY_VERSION=v2.7.4
# Thu, 28 Sep 2023 22:19:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_DATA_HOME=/data
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 80
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443/udp
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 2019
# Thu, 28 Sep 2023 22:19:44 GMT
WORKDIR /srv
# Thu, 28 Sep 2023 22:19:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3df874173df47ad0bd0ef67b8ee598c77921810d84a67fd2984c4f8151c91`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a69c42a5c7fc6d73c00c7f6eb68522f3881aae55db4f85a8400e83b678b181`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793016dc78c9794c627c07afcd2fb34af4ee470ee7fef1a1596eff0c59ba6659`  
		Last Modified: Thu, 28 Sep 2023 22:20:16 GMT  
		Size: 14.1 MB (14143684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:b859825f1b8093a4b961d02fb945e63f5180c5e07e56ce7495384835c016c47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4974; amd64
	-	windows version 10.0.20348.2031; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:8169d134dfa19ddbba9eeeb7210c5227c2a61f00906c340474aab1250aba47f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull caddy@sha256:77cb1b0b8315f376e69becef400d33c9d8b2a45548714845a821736158771de2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2047649951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3171dc2f25b4435520d8ba983ebf42f070ddec217b0da7677e309cc4cd51b05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 01:36:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:59:19 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:39:06 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:40:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:40:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:40:06 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:40:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:40:08 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:40:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:40:10 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:40:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:40:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:40:12 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:40:13 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:40:14 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:41:01 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:41:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0814e4a0bb8c615854a85a2b60cd043cfd20ad5a5d755acab1b30b18e4bfad3c`  
		Last Modified: Wed, 11 Oct 2023 02:46:41 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c4565a9b36858bc727874537e3c99968438a37e53c13057b0b1a233699d014`  
		Last Modified: Wed, 11 Oct 2023 04:05:44 GMT  
		Size: 472.0 KB (472034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df4a75108d3a33583e7ae61f1a019d4865860820bd89280ba414af94dd3f56e`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee9792a7bf7e1225840c56fb692536bee1743eba0a4da2faff34533f1160f`  
		Last Modified: Thu, 12 Oct 2023 01:44:37 GMT  
		Size: 15.3 MB (15296055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41900185a2519f01b8bd860f70936cee271612c4023512694b105826e0e0251`  
		Last Modified: Thu, 12 Oct 2023 01:44:34 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0f1b69a12cd8550d868156e54168abaa32e1df40ee6eb39bc4e173ce04905e`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca266891343bff15b313846692ba3a41f313d5b228bedde964191332a16dffe`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12539eb7433a69ed67556d91b75b66dfedf0543d3efd7dabe82772437307a6f`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5103f279ed518bcfec88e00183e3222b50c1bc2f0e5b42f043e2198da424de98`  
		Last Modified: Thu, 12 Oct 2023 01:44:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc1cff2dac4308ce732a395ee215e1497d21f737e42e77917debf070afa8d7`  
		Last Modified: Thu, 12 Oct 2023 01:44:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb50f59d2b11532a330925afb6ebd04d9b4708de8b11ae436e258c3764d741`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd11a311e4c0cf49bb544980f2c999751fc5e2fbe80d37b0f719f837abf8c3f`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ccbee9a6b9058ec933797dc1cfed875ceeb0115ce29ee163cd60a66e9f3b2d`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b486fc8ef055010a59374557443d3b713b9e55c1ccd11b7873f47876758976`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41df430d9a95c6000c922dd021b6cb2af0110dcc661ddc37a190a8cf6cd4bb06`  
		Last Modified: Thu, 12 Oct 2023 01:44:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f243061a2e17d508efa4a424310d9ca158ca0cf0f59bd15cac606ab3e74701`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709fff7d020a5d7c2d9e9e9a664c87392e9f9a4f4ced9802e64ca268995e23`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2c7aca9b511bc62340e6e8883d5f625bdccb805c4e897b837b68f3c79964b5`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38802c5a2b45b7029b250d88dac8209405146b0968925d1204cf17f7c3e76d98`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 269.1 KB (269086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376d19318a370d0da2ffcc29b47c2810278efa9d22fb39799c48687dfee0a2d9`  
		Last Modified: Thu, 12 Oct 2023 01:44:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:278d32be7fb2f9a5e3f48ea6a672747dbb4ad6256e4802aff4a1e11a67e2e518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull caddy@sha256:05f529a68927f0acfa7afbc79b7a19541f94430c137612ed344de7a822dcfafb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1875907229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8701a0e5aada270070acddeed89c57e20a5cac8afd88ed58da9557bf01dccb27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 04:02:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 12 Oct 2023 01:41:20 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:41:42 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('3201e91a00d8c49acf6165753df34fccfb9c0eacb610b0dad5e5c465cdaced761b061f0c7fc200ce4e87f4acfbd6421e9b3e0121ba293532f4afdf7c9c9c96a0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 12 Oct 2023 01:41:42 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 12 Oct 2023 01:41:43 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 12 Oct 2023 01:41:44 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:41:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:41:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:41:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:41:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:41:50 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:41:51 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:41:52 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:42:04 GMT
RUN caddy version
# Thu, 12 Oct 2023 01:42:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36616366b0df84f087a09bf19876f3872d839997f2f43e4eb8599861417c06`  
		Last Modified: Wed, 11 Oct 2023 04:06:10 GMT  
		Size: 467.9 KB (467933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db420ca589f10e4f9f5bc9dd6badc855d95c6a598888f2eb77a747eced259557`  
		Last Modified: Thu, 12 Oct 2023 01:45:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5d7433dab05533d906a290a0f42cf31804c132da65c9fd7d4d2c41a64f519`  
		Last Modified: Thu, 12 Oct 2023 01:45:04 GMT  
		Size: 15.3 MB (15284209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62069fdf38bff9495ef2be05d397a55221536f9eec345734d6acec3a6196324f`  
		Last Modified: Thu, 12 Oct 2023 01:45:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e237a4c373c6937b5c51d0a3936152ac2b572fd5a432db3690f4070a7c78327`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73fae1c57e166a2ade87aa32e11980b456658212b296eea0f02ba3ec1c6557b`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000f2101dc464fa43321619c6e65c5b9e62b62755f3b141e69bd31892a253ded`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536723423849b861a08fa490135f690c287be0144267e38fb3e631fb1bddbd2`  
		Last Modified: Thu, 12 Oct 2023 01:44:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f176ef86531863755c3a315ec662b8da324474ae6097d7365dc18b76d61bde5`  
		Last Modified: Thu, 12 Oct 2023 01:44:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3973c168b3a63daa069e3a9870395561709d7b27762ffafb16538c773a16ad29`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a10fbc59abc7ee7cc04a7ff48cc85983728745e91e8ef5fafee0589ba2193`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf033f8ab12414230e08aaada214c761777b0c784908ad2783ee31f8d330d0c9`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e2af83b2af59d76bd9b735c4e71b9492d9dbc120c042b8134ae0a70008f49`  
		Last Modified: Thu, 12 Oct 2023 01:44:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355ed819405072f13996095ae7ec7044017bee81808dea9500459620118c20b`  
		Last Modified: Thu, 12 Oct 2023 01:44:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86117e27425829055f627e6156a4a657d9817cf8d2158f0026752366c9022c`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22fbe71be2fe08164a92f1362959f0a4aba194dcf931945d7bb2ac50e8f6467`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed768b9f807d51e5834f0bc8b2ea4dda09a5139d126f9141cb3db51f781ea541`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fc3c79eda3ddbb39c46b09a4c68137a693a72f8712182d545c546b726027e`  
		Last Modified: Thu, 12 Oct 2023 01:44:55 GMT  
		Size: 289.5 KB (289533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e4b8683a429393010114c6906acced22d65d5167cda2cc55238ae5b9f816c0`  
		Last Modified: Thu, 12 Oct 2023 01:44:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
