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
-	[`caddy:2.7.3`](#caddy273)
-	[`caddy:2.7.3-alpine`](#caddy273-alpine)
-	[`caddy:2.7.3-builder`](#caddy273-builder)
-	[`caddy:2.7.3-builder-alpine`](#caddy273-builder-alpine)
-	[`caddy:2.7.3-builder-windowsservercore-1809`](#caddy273-builder-windowsservercore-1809)
-	[`caddy:2.7.3-builder-windowsservercore-ltsc2022`](#caddy273-builder-windowsservercore-ltsc2022)
-	[`caddy:2.7.3-windowsservercore`](#caddy273-windowsservercore)
-	[`caddy:2.7.3-windowsservercore-1809`](#caddy273-windowsservercore-1809)
-	[`caddy:2.7.3-windowsservercore-ltsc2022`](#caddy273-windowsservercore-ltsc2022)
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
$ docker pull caddy@sha256:0da93d63c5b3af38288e909b953bd8cdcf12537c27ff219aac46c6a01775cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:f9824933254e3e43e0508670ee9bdcde704621017e95119a05317383b1878f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18631102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e9fe28a35a7bd46854ffa0afa91435071afeabac2784f8730569278d8bc9a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:09:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:20:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:20:15 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:20:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aa7b81ef11c65f43b0b58323a33dd9e07eb785529f0d75b452f87a309db00c`  
		Last Modified: Mon, 07 Aug 2023 20:09:40 GMT  
		Size: 350.8 KB (350844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b3b3e68e52dc5ab939c72a9bbac39cff4bef4b87de399ddf28657471df6845`  
		Last Modified: Mon, 14 Aug 2023 18:20:42 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e6a3c74b422682f93a437993c6365f8008e89737276364fd12ea870022f03`  
		Last Modified: Mon, 14 Aug 2023 18:20:45 GMT  
		Size: 14.9 MB (14871143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dc698bd1b82521df87ea42fbf48c98d10133ec962497ac80527b65769ceb6a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17690701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3775ac20cca67f4d547f26f5984a989b9407b0c4129fd6cd86dbb3359249acd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:38:27 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:49:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:49:14 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:49:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:49:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:49:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ef460a93549b8a3e73f6a515bccad93512788d1e8f095e7230ba41967c25a`  
		Last Modified: Wed, 09 Aug 2023 03:38:53 GMT  
		Size: 347.7 KB (347686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aae78767a581df85fd1a51ccd646619aec320896ca016ef0f05a41b16bcbfe`  
		Last Modified: Mon, 14 Aug 2023 17:49:36 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5244db1c019e66038874df2b8b92c74437f6d355802bfccada90c9d8bd8d29`  
		Last Modified: Mon, 14 Aug 2023 17:49:38 GMT  
		Size: 14.2 MB (14190701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e9cb1245e1c134e25a0ec0803e5132ba9ba92d0a4ad85db3f73bd2c3188cf70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17414619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6e2a1f4c707dc77276814a27ac22a7b5de268780603d8e08324130e1fc563`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:57:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:57:17 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:57:21 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:57:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a47b73e04459258b08555443754e92e2db20bde113c58ca18e1a6f07878f72`  
		Last Modified: Tue, 08 Aug 2023 01:52:05 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1b3e18d5e992f1805072b2d52405d575830bdce21726ef99dea99e31d8277`  
		Last Modified: Mon, 14 Aug 2023 17:57:42 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2b7485982d191f9dc0498d5b940d14df575f36ca66876b92d3ca09ff9386b2`  
		Last Modified: Mon, 14 Aug 2023 17:57:48 GMT  
		Size: 14.2 MB (14163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:db04154ce5f7a7f4d058567375880cdc6b1a3675095ad576f9886f39f1374afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731c0ae21a974e5708c4a8006250893bca5a2ecad43babf2a0a95a60fc61d6cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:09:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:39:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:39:19 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:39:22 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a699f78cfb85f60e17fc7c13495876ea0cb4495bbe39e8c65f3e8559b0d7169`  
		Last Modified: Mon, 07 Aug 2023 21:09:34 GMT  
		Size: 360.6 KB (360642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7488af8b96c79b6db13955a0302653c4e9f314d0833201984ae06c1ed697f06`  
		Last Modified: Mon, 14 Aug 2023 17:39:41 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9600da6e7e51b9083b29f3c7de592fa45e7765ca5ffe8d2abf7cc99c50578fe`  
		Last Modified: Mon, 14 Aug 2023 17:39:43 GMT  
		Size: 13.6 MB (13630728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:dfe8f314baac04dac7b7d48bdd1999aedd42d82f792d5a921be7b9a38adbcc07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17021924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09511fed803e1230efcb1c914154726b2f232029c67b0c681319b2eb6ee73a3c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:44:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:18:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:18:00 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:18:05 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:10 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:11 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:18:11 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:18:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f40714f45e39ac41e865ccbf2877db62255ce5a5c36a47eadf00b9d174f042`  
		Last Modified: Tue, 08 Aug 2023 00:45:18 GMT  
		Size: 362.2 KB (362173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d19953b5eb53ddaa0e25905527dc138e0c4111467bb7d71f81fa94976091351`  
		Last Modified: Mon, 14 Aug 2023 18:18:54 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff11295d70af9c740cf7afdb57754d70bffd7cd42271ba1a6de34195de6b249`  
		Last Modified: Mon, 14 Aug 2023 18:18:58 GMT  
		Size: 13.3 MB (13305991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:3b3d4b80e160105a760ad62b32c497245d69676e6053c2a7b61bc5c6fc178fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17984968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a63d05bc7601e47460ff86bc91380fd9407c0b4886b80836ac3aadb436f68e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:14:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:41:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:41:39 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:41:44 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:41:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df19abd0ca1d4a821a4174a2c0831a57d6fd584073f056abcae085a51f0b3848`  
		Last Modified: Mon, 07 Aug 2023 20:14:50 GMT  
		Size: 354.9 KB (354950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308478977890baa82477ee70a3065fb9da2080efcc95facf1a87ac021b06a8e9`  
		Last Modified: Mon, 14 Aug 2023 17:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fe1cbba37a3c1c2f6ba50e59e5c238c8d83ffca820ef709108b9e3253af757`  
		Last Modified: Mon, 14 Aug 2023 17:42:19 GMT  
		Size: 14.4 MB (14408320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:60de297131e676c0d87d7aacaa4fbd5a883abb5818977670f7024b89ebe1d7bb
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
$ docker pull caddy@sha256:f9824933254e3e43e0508670ee9bdcde704621017e95119a05317383b1878f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18631102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e9fe28a35a7bd46854ffa0afa91435071afeabac2784f8730569278d8bc9a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:09:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:20:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:20:15 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:20:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aa7b81ef11c65f43b0b58323a33dd9e07eb785529f0d75b452f87a309db00c`  
		Last Modified: Mon, 07 Aug 2023 20:09:40 GMT  
		Size: 350.8 KB (350844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b3b3e68e52dc5ab939c72a9bbac39cff4bef4b87de399ddf28657471df6845`  
		Last Modified: Mon, 14 Aug 2023 18:20:42 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e6a3c74b422682f93a437993c6365f8008e89737276364fd12ea870022f03`  
		Last Modified: Mon, 14 Aug 2023 18:20:45 GMT  
		Size: 14.9 MB (14871143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dc698bd1b82521df87ea42fbf48c98d10133ec962497ac80527b65769ceb6a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17690701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3775ac20cca67f4d547f26f5984a989b9407b0c4129fd6cd86dbb3359249acd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:38:27 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:49:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:49:14 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:49:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:49:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:49:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ef460a93549b8a3e73f6a515bccad93512788d1e8f095e7230ba41967c25a`  
		Last Modified: Wed, 09 Aug 2023 03:38:53 GMT  
		Size: 347.7 KB (347686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aae78767a581df85fd1a51ccd646619aec320896ca016ef0f05a41b16bcbfe`  
		Last Modified: Mon, 14 Aug 2023 17:49:36 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5244db1c019e66038874df2b8b92c74437f6d355802bfccada90c9d8bd8d29`  
		Last Modified: Mon, 14 Aug 2023 17:49:38 GMT  
		Size: 14.2 MB (14190701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e9cb1245e1c134e25a0ec0803e5132ba9ba92d0a4ad85db3f73bd2c3188cf70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17414619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6e2a1f4c707dc77276814a27ac22a7b5de268780603d8e08324130e1fc563`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:57:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:57:17 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:57:21 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:57:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a47b73e04459258b08555443754e92e2db20bde113c58ca18e1a6f07878f72`  
		Last Modified: Tue, 08 Aug 2023 01:52:05 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1b3e18d5e992f1805072b2d52405d575830bdce21726ef99dea99e31d8277`  
		Last Modified: Mon, 14 Aug 2023 17:57:42 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2b7485982d191f9dc0498d5b940d14df575f36ca66876b92d3ca09ff9386b2`  
		Last Modified: Mon, 14 Aug 2023 17:57:48 GMT  
		Size: 14.2 MB (14163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:db04154ce5f7a7f4d058567375880cdc6b1a3675095ad576f9886f39f1374afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731c0ae21a974e5708c4a8006250893bca5a2ecad43babf2a0a95a60fc61d6cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:09:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:39:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:39:19 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:39:22 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a699f78cfb85f60e17fc7c13495876ea0cb4495bbe39e8c65f3e8559b0d7169`  
		Last Modified: Mon, 07 Aug 2023 21:09:34 GMT  
		Size: 360.6 KB (360642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7488af8b96c79b6db13955a0302653c4e9f314d0833201984ae06c1ed697f06`  
		Last Modified: Mon, 14 Aug 2023 17:39:41 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9600da6e7e51b9083b29f3c7de592fa45e7765ca5ffe8d2abf7cc99c50578fe`  
		Last Modified: Mon, 14 Aug 2023 17:39:43 GMT  
		Size: 13.6 MB (13630728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:dfe8f314baac04dac7b7d48bdd1999aedd42d82f792d5a921be7b9a38adbcc07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17021924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09511fed803e1230efcb1c914154726b2f232029c67b0c681319b2eb6ee73a3c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:44:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:18:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:18:00 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:18:05 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:10 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:11 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:18:11 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:18:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f40714f45e39ac41e865ccbf2877db62255ce5a5c36a47eadf00b9d174f042`  
		Last Modified: Tue, 08 Aug 2023 00:45:18 GMT  
		Size: 362.2 KB (362173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d19953b5eb53ddaa0e25905527dc138e0c4111467bb7d71f81fa94976091351`  
		Last Modified: Mon, 14 Aug 2023 18:18:54 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff11295d70af9c740cf7afdb57754d70bffd7cd42271ba1a6de34195de6b249`  
		Last Modified: Mon, 14 Aug 2023 18:18:58 GMT  
		Size: 13.3 MB (13305991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:3b3d4b80e160105a760ad62b32c497245d69676e6053c2a7b61bc5c6fc178fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17984968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a63d05bc7601e47460ff86bc91380fd9407c0b4886b80836ac3aadb436f68e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:14:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:41:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:41:39 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:41:44 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:41:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df19abd0ca1d4a821a4174a2c0831a57d6fd584073f056abcae085a51f0b3848`  
		Last Modified: Mon, 07 Aug 2023 20:14:50 GMT  
		Size: 354.9 KB (354950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308478977890baa82477ee70a3065fb9da2080efcc95facf1a87ac021b06a8e9`  
		Last Modified: Mon, 14 Aug 2023 17:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fe1cbba37a3c1c2f6ba50e59e5c238c8d83ffca820ef709108b9e3253af757`  
		Last Modified: Mon, 14 Aug 2023 17:42:19 GMT  
		Size: 14.4 MB (14408320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:72235016961770347eb1ca2771c13e5e406c0091e3584d0bc7dd6ffbd481abd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:7a4a3476f0991b84458cf29307f0c064e6b5fdd6af0019dc36a76576dc0721f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110902575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e1c25fbce7e1bbf91803ddf419d9de799552698d44cac3fe01a21c05cd3f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:36:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 09 Aug 2023 04:41:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:41:57 GMT
ENV GOLANG_VERSION=1.20.7
# Wed, 09 Aug 2023 04:43:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 09 Aug 2023 04:43:29 GMT
ENV GOPATH=/go
# Wed, 09 Aug 2023 04:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:43:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 09 Aug 2023 04:43:30 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:26:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:21 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:20:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:20:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:20:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d48a809fc2256f8aa0aeee47998488d64409855adba00a7cb3007ab9f3286e`  
		Last Modified: Wed, 09 Aug 2023 03:37:02 GMT  
		Size: 284.7 KB (284693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e790db5857269a95a948a96f0e3304c851351e588262d58504700b2e73fb7fe`  
		Last Modified: Wed, 09 Aug 2023 04:47:32 GMT  
		Size: 101.0 MB (100954810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f4e1a48a681e22437b6c14b04a4e287386f50f1be21ef490a1e28fd276a91`  
		Last Modified: Wed, 09 Aug 2023 04:47:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a272b880a0f8927853947bb9b16e005e2824b1685a89cc015f4e4694c441ed0e`  
		Last Modified: Wed, 09 Aug 2023 10:26:35 GMT  
		Size: 5.0 MB (4958652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636df467d23fd7ec3f363a1403da4b23c878bb239a4a4b9fdbf55f0189f9cbb1`  
		Last Modified: Mon, 14 Aug 2023 18:20:59 GMT  
		Size: 1.3 MB (1302244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afb5bd80935e22cbe3f7bb67cae35b420386beb37b9390eeab25fcef89b65d7`  
		Last Modified: Mon, 14 Aug 2023 18:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:289b1f78db36a7524bbae6562b80b29fe5585984effd44a3e22146fcbf4ab824
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108301221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac734398939dbe1f4c664f493d34b5353c438189c6b58b3e6e4d92186a8f80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:12:05 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:12:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:40 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:14:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:14:36 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:14:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:14:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:14:37 GMT
WORKDIR /go
# Wed, 09 Aug 2023 03:38:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:49:20 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:49:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:49:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8564ce36feee688566265012773f1c8c7c046ceefe86ca763eb702682f4e6e75`  
		Last Modified: Tue, 08 Aug 2023 23:15:06 GMT  
		Size: 284.9 KB (284876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b139603b026cc15bf570c9cf012fc165cb74821883c7c7c534fe6ed189b5a2`  
		Last Modified: Tue, 08 Aug 2023 23:16:29 GMT  
		Size: 98.7 MB (98671161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b2f37c2778ffd2e158ad31438d6802c214dfa5d79e06dc9af2d8320828e148`  
		Last Modified: Tue, 08 Aug 2023 23:16:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22c305527b162efa854ac3e1963e59e7fb8f2c71838222c56462b9809481ed`  
		Last Modified: Wed, 09 Aug 2023 03:39:10 GMT  
		Size: 5.0 MB (4951147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5520daf22ad222fbe3c81bbd6afa0c912b3817f0f432a35a939f9870a8512af`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 1.2 MB (1248666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f8fe3942ebea0d37a8324080324eb0bca35e859273e7bac44381e31a0fa714`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:dcbac62a4e9d8d10345a7f20ac37a814b45633ed4b050a14fa20aef08590597a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107386270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee903aaec70e29acbd506823b19cc477dc7788e545d1b88316b9ec0e9c154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:39:47 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 01:39:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:40:29 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 01:42:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 01:42:12 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 01:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:42:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 01:42:13 GMT
WORKDIR /go
# Tue, 08 Aug 2023 01:51:50 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:57:24 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:57:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:57:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:57:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47bd95d78f565e902bafd0264a979eb4f6f71e22c0464011bf9db6feb0579e6`  
		Last Modified: Tue, 08 Aug 2023 01:48:34 GMT  
		Size: 284.1 KB (284073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a674106498848b269b5cb69fb938d3dc97247d02cb1aa3927b7a7469724e950`  
		Last Modified: Tue, 08 Aug 2023 01:49:43 GMT  
		Size: 98.5 MB (98454659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1902a68db0b07b05ab7d2f3e48ca8f1d22951b498f6ff9027bdc91a5e7e830`  
		Last Modified: Tue, 08 Aug 2023 01:49:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf1886c556e441f6f89cd1cb00e1b950d9d8fcad8812a988fbb59caf0b0ba5`  
		Last Modified: Tue, 08 Aug 2023 01:52:22 GMT  
		Size: 4.5 MB (4501403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28b1afe92de619aa5de35a2f610dc68af6b39c6cd300ef8426738a739366a2`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 1.2 MB (1246092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe75fd67d7668d6aeca167419514f45cb72ec61bd61a9fc32e25b5c928dba6`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ad7390f7aa878bd4d6750dab9611c7397630fc15a7f80304eea3d3f64dcfe4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105987240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79cdcd45a4a61e8fe257b7917335ede1523a72d1c2ef2eb9115783a5379f5ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:10:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:10:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:53 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:11:59 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:11:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:12:00 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:10:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:39:25 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54e960e981301b0098c80d2e61d694333b5ab480a007a3a8d0fa629662d377`  
		Last Modified: Tue, 08 Aug 2023 23:14:21 GMT  
		Size: 286.3 KB (286298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ccffba14f84f51f896ae916a3dd045a0b0d08dc27d53f7d6a9dc5687c3501`  
		Last Modified: Tue, 08 Aug 2023 23:15:23 GMT  
		Size: 96.1 MB (96117263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d452dd4d3acc29d43b0be67bcc0c121814601787c7fd45e8260687d2cc8983`  
		Last Modified: Tue, 08 Aug 2023 23:15:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d371a704ab9a071c89db966e268fe56aad2288363a849d10eb032d47cd10848b`  
		Last Modified: Wed, 09 Aug 2023 10:10:48 GMT  
		Size: 5.1 MB (5053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e38cf28101c20845f7f103114793f73691285da6ac006db5cb28c20bc8000`  
		Last Modified: Mon, 14 Aug 2023 17:39:55 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d1b8334b836b303a87ddda4bfba4af764950afa40c2c263cca11ed8b53a8c6`  
		Last Modified: Mon, 14 Aug 2023 17:39:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4434838c3cf5a9e2e8050d86c8cfc927ad8bb46c478811a034b9a51ad2e4879c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106661395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eae15fb81c48d690da2ae88d171f0c7398deaed959011a96133cdd3836caf97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:25:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 00:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:26:56 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 00:29:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 00:29:34 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 00:29:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:29:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 00:29:36 GMT
WORKDIR /go
# Tue, 08 Aug 2023 00:44:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:18:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:18:18 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:18:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:18:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:18:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:18:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966ad2cdd35689da92e7c8fd39bd37cd6080c484e6ccaf00672c154cd4f6c2a`  
		Last Modified: Tue, 08 Aug 2023 00:39:35 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7816c9df7e6881fdd62dfcc6d743edcc2c3ca9220542437a2e5fdcfa0e4548`  
		Last Modified: Tue, 08 Aug 2023 00:41:09 GMT  
		Size: 96.6 MB (96591770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d34a514a03c5af8a03dfe8c4fbfd50b2ec61591d24080f8be8bf722904f541`  
		Last Modified: Tue, 08 Aug 2023 00:40:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802af1410e20c34900a811878ca2fa2e5dc79daeb92a53b94588831011ad81fc`  
		Last Modified: Tue, 08 Aug 2023 00:45:40 GMT  
		Size: 5.2 MB (5249966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9d8614d3da52c8737c0b4449e6e9e688fc7353d31f0246eb31e74f676c1a2`  
		Last Modified: Mon, 14 Aug 2023 18:19:17 GMT  
		Size: 1.2 MB (1186181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aa14602d0d570f4ade4524880d76ae39c401058848761634a02d8513598058`  
		Last Modified: Mon, 14 Aug 2023 18:19:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:4c76dac9b235685647bce5e644408f9537fd2a98243936db0666252a4ec24739
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110727449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe6eea8994d5e82ec6e85ed4c441f0a89b9cb461829805dd3eeb9d892d49a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:19:41 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Aug 2023 20:19:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:21:06 GMT
ENV GOLANG_VERSION=1.20.7
# Mon, 07 Aug 2023 20:23:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Mon, 07 Aug 2023 20:23:05 GMT
ENV GOPATH=/go
# Mon, 07 Aug 2023 20:23:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:23:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Mon, 07 Aug 2023 20:23:06 GMT
WORKDIR /go
# Tue, 08 Aug 2023 05:25:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:41:51 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:41:52 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:41:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:41:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:41:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec90be18226e5c99d10161aed1a143f4134093c55b4d6979bbdbbe4b0683eb11`  
		Last Modified: Mon, 07 Aug 2023 20:30:59 GMT  
		Size: 285.1 KB (285089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c751f85e4ba6e9bbada0b11691d914b2ec2c689bb0dca6b9cbe994488d0e3e`  
		Last Modified: Mon, 07 Aug 2023 20:31:56 GMT  
		Size: 100.9 MB (100865267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d202223222826c8580d85b8d7dd6baa8ed1cad84ba5cf47dab23eaeeae7e9`  
		Last Modified: Mon, 07 Aug 2023 20:31:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359ada615d16e203e1d40a49b896060013c2952c2982ae73b141cc291305a4c`  
		Last Modified: Tue, 08 Aug 2023 05:25:47 GMT  
		Size: 5.1 MB (5099943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1039996d136f688a91d291dcf3dbb995607af1f245f1741d8ad0c5f73cec1b01`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e7bfc7e0d6b6a7f70b22841fe42427f0fb6372b17c71c8063c50d7c8e73c1`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:d2986a3c3acb890096b8f22fe47d163b679506c701409f0f96ef55f0370c6e49
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2132346458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb468ba68962f7df97763531c45fe07444d56eeed51c25ca5019d9f06b5d07b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:39:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:39:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:41:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:41:12 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:42:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:53:35 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:56:38 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:56:40 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:20:56 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:57 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594083c5c2094c95b4e52723d54c14e0d70881f4f176720c3170012275accc3b`  
		Last Modified: Thu, 10 Aug 2023 01:02:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e2c2a5b75ced3a3a50be088c4a6c2d7df926b1fe6515b2d0c021312e3642f4`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d28688050deeec928289543beadf5c75bb2a8246576cb7c066e23818016217`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e5fbc50e7e0fefb7c9e349038ecb00ed5c000bcab8c4d82b1e1000c4273c01`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544e07bd9df923e11e09c7dc042da614f2f14589eb6fa79005ebbbf2731e97d`  
		Last Modified: Thu, 10 Aug 2023 01:02:57 GMT  
		Size: 25.6 MB (25560980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a82506c4fcec2bd90ae77756e5b03788e30c89f1a3820aa0b6a7ae6ad58ae`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcfb422b104764156fc5ba099b5e3ae9fa9f760fd2db1c21acd8969b3d73de`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 220.8 KB (220796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6aa0a5a1689ed800c4ef72c1b9febf207840fd2c6abfe4bb460e2e2bfb0b0`  
		Last Modified: Thu, 10 Aug 2023 01:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d3379322a67b2413189cc2b779d22cb4093124343c8bb17fdf720b7b49fda`  
		Last Modified: Thu, 10 Aug 2023 01:05:25 GMT  
		Size: 108.9 MB (108911716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60ccf92610ddbc47a05664785c95215a123e8930afbf6e3e2cefc80e693fd2`  
		Last Modified: Thu, 10 Aug 2023 01:05:04 GMT  
		Size: 1.5 KB (1468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c7d6253e62d61e5e0d2ad331a96cff5175f6c608b2ab4657825b3e3b4b4d0`  
		Last Modified: Thu, 10 Aug 2023 03:08:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7441bd899a1ec2037a7dc63ed24148f4362550631136f0b286d1980977fbfcfa`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60695a3cfa3d46aac3798546808cbe211d637be2b7c2af5f9d90d79eb10d544a`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636dfb4139d7b40d2a0cfa8fa63fa590d61d8627017a87a8a517c9c229fdda5b`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d287a3e1b6a016ab5e21634424eddc049708da3cc46e37cc8444f8f20d9ba206`  
		Last Modified: Mon, 14 Aug 2023 18:24:03 GMT  
		Size: 1.7 MB (1679974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cfbbc308f7ee8ad386b267faba56ca74b5aff7b32f0b71f6d94c29f5febe43`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:2bf33a1b3b64f1ffe31a0ea39e974e24ae1e5d17a1d1f0d3d2c744f8f612a8a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1933831109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2a69ae1b3bbd9a3aefa279d32b203c5ef28dee21038b8b203d78518899270`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:36:23 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:36:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:36:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:36:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:37:00 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:37:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:50:52 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:53:17 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:53:18 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:06:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:22:09 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:22:10 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:22:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877256a6389e5e2563da79ad5bd201e7ee136abf14ff7cb0d4efbf3b24e5f127`  
		Last Modified: Thu, 10 Aug 2023 01:02:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a39df29b3c0b2f7e691c47273110db4a46e5c8e299f6bb95f77a9c61f79872`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8574d63bce1547e3177d0b76237a782a9b016d4880375dcd1a7b6a1c5dee3dc`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef34b3c96316bcdd92e24c8c4eebdc3a35f245c013ef87edfae0dde091a305`  
		Last Modified: Thu, 10 Aug 2023 01:02:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a481babc5b629f694446a96dba8d77c020257c98334c605aff94162b9a917279`  
		Last Modified: Thu, 10 Aug 2023 01:02:23 GMT  
		Size: 25.6 MB (25554169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281178ea1c103ff07ea7e4fb647eb0dbe4f865742da6ef9944e04f37974fc27c`  
		Last Modified: Thu, 10 Aug 2023 01:02:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5d34adf2aacfe87580143f3e17c635dc8dbd4068377b79b35d665f49bbad9`  
		Last Modified: Thu, 10 Aug 2023 01:02:16 GMT  
		Size: 275.9 KB (275946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02a2e79b5a05c2145c733eefb2add45d1ebefb7a16b93c321f5883c8ced6f1a`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd9991b8cfbc481c153abf1625143209f4c4fd40d9443a5a19f4e3613336ad2`  
		Last Modified: Thu, 10 Aug 2023 01:04:53 GMT  
		Size: 108.9 MB (108927695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dc6778f41c3c7d50b8e71668e22880153d6c6794f24c4661fc3d6aa089d0a5`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5985f015e143065716f5aabf0ecaed537103c5ec07e6c57360204a7787d02`  
		Last Modified: Thu, 10 Aug 2023 03:08:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c565e57b551adf88d5e29bd1458eb8f35437ae3145eba3114c3e38a14420307`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93046b7cb08612cc9fda41d92a61df03529a75e7d266f85a0529c5e88f7d06eb`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a40abe5aa831ec7c89060659309bccacad929792153b60f544eec13c1b6394`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8095d427fe41dd6d758aae45f422bddef28912086c3a3f7797f231535d73ca69`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.7 MB (1690912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8e6227140a7a352f358e4d9e7deab69dc502cd45903e2458244037b6bb36df`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:d8bcb1d79bd1a9970df74b9b92ced472e5ee3d2f17f16bdb9383d6f8e00bacc0
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
$ docker pull caddy@sha256:7a4a3476f0991b84458cf29307f0c064e6b5fdd6af0019dc36a76576dc0721f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110902575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e1c25fbce7e1bbf91803ddf419d9de799552698d44cac3fe01a21c05cd3f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:36:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 09 Aug 2023 04:41:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:41:57 GMT
ENV GOLANG_VERSION=1.20.7
# Wed, 09 Aug 2023 04:43:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 09 Aug 2023 04:43:29 GMT
ENV GOPATH=/go
# Wed, 09 Aug 2023 04:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:43:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 09 Aug 2023 04:43:30 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:26:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:21 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:20:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:20:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:20:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d48a809fc2256f8aa0aeee47998488d64409855adba00a7cb3007ab9f3286e`  
		Last Modified: Wed, 09 Aug 2023 03:37:02 GMT  
		Size: 284.7 KB (284693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e790db5857269a95a948a96f0e3304c851351e588262d58504700b2e73fb7fe`  
		Last Modified: Wed, 09 Aug 2023 04:47:32 GMT  
		Size: 101.0 MB (100954810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f4e1a48a681e22437b6c14b04a4e287386f50f1be21ef490a1e28fd276a91`  
		Last Modified: Wed, 09 Aug 2023 04:47:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a272b880a0f8927853947bb9b16e005e2824b1685a89cc015f4e4694c441ed0e`  
		Last Modified: Wed, 09 Aug 2023 10:26:35 GMT  
		Size: 5.0 MB (4958652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636df467d23fd7ec3f363a1403da4b23c878bb239a4a4b9fdbf55f0189f9cbb1`  
		Last Modified: Mon, 14 Aug 2023 18:20:59 GMT  
		Size: 1.3 MB (1302244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afb5bd80935e22cbe3f7bb67cae35b420386beb37b9390eeab25fcef89b65d7`  
		Last Modified: Mon, 14 Aug 2023 18:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:289b1f78db36a7524bbae6562b80b29fe5585984effd44a3e22146fcbf4ab824
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108301221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac734398939dbe1f4c664f493d34b5353c438189c6b58b3e6e4d92186a8f80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:12:05 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:12:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:40 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:14:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:14:36 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:14:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:14:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:14:37 GMT
WORKDIR /go
# Wed, 09 Aug 2023 03:38:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:49:20 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:49:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:49:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8564ce36feee688566265012773f1c8c7c046ceefe86ca763eb702682f4e6e75`  
		Last Modified: Tue, 08 Aug 2023 23:15:06 GMT  
		Size: 284.9 KB (284876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b139603b026cc15bf570c9cf012fc165cb74821883c7c7c534fe6ed189b5a2`  
		Last Modified: Tue, 08 Aug 2023 23:16:29 GMT  
		Size: 98.7 MB (98671161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b2f37c2778ffd2e158ad31438d6802c214dfa5d79e06dc9af2d8320828e148`  
		Last Modified: Tue, 08 Aug 2023 23:16:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22c305527b162efa854ac3e1963e59e7fb8f2c71838222c56462b9809481ed`  
		Last Modified: Wed, 09 Aug 2023 03:39:10 GMT  
		Size: 5.0 MB (4951147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5520daf22ad222fbe3c81bbd6afa0c912b3817f0f432a35a939f9870a8512af`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 1.2 MB (1248666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f8fe3942ebea0d37a8324080324eb0bca35e859273e7bac44381e31a0fa714`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:dcbac62a4e9d8d10345a7f20ac37a814b45633ed4b050a14fa20aef08590597a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107386270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee903aaec70e29acbd506823b19cc477dc7788e545d1b88316b9ec0e9c154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:39:47 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 01:39:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:40:29 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 01:42:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 01:42:12 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 01:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:42:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 01:42:13 GMT
WORKDIR /go
# Tue, 08 Aug 2023 01:51:50 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:57:24 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:57:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:57:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:57:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47bd95d78f565e902bafd0264a979eb4f6f71e22c0464011bf9db6feb0579e6`  
		Last Modified: Tue, 08 Aug 2023 01:48:34 GMT  
		Size: 284.1 KB (284073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a674106498848b269b5cb69fb938d3dc97247d02cb1aa3927b7a7469724e950`  
		Last Modified: Tue, 08 Aug 2023 01:49:43 GMT  
		Size: 98.5 MB (98454659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1902a68db0b07b05ab7d2f3e48ca8f1d22951b498f6ff9027bdc91a5e7e830`  
		Last Modified: Tue, 08 Aug 2023 01:49:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf1886c556e441f6f89cd1cb00e1b950d9d8fcad8812a988fbb59caf0b0ba5`  
		Last Modified: Tue, 08 Aug 2023 01:52:22 GMT  
		Size: 4.5 MB (4501403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28b1afe92de619aa5de35a2f610dc68af6b39c6cd300ef8426738a739366a2`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 1.2 MB (1246092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe75fd67d7668d6aeca167419514f45cb72ec61bd61a9fc32e25b5c928dba6`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ad7390f7aa878bd4d6750dab9611c7397630fc15a7f80304eea3d3f64dcfe4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105987240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79cdcd45a4a61e8fe257b7917335ede1523a72d1c2ef2eb9115783a5379f5ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:10:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:10:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:53 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:11:59 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:11:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:12:00 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:10:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:39:25 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54e960e981301b0098c80d2e61d694333b5ab480a007a3a8d0fa629662d377`  
		Last Modified: Tue, 08 Aug 2023 23:14:21 GMT  
		Size: 286.3 KB (286298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ccffba14f84f51f896ae916a3dd045a0b0d08dc27d53f7d6a9dc5687c3501`  
		Last Modified: Tue, 08 Aug 2023 23:15:23 GMT  
		Size: 96.1 MB (96117263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d452dd4d3acc29d43b0be67bcc0c121814601787c7fd45e8260687d2cc8983`  
		Last Modified: Tue, 08 Aug 2023 23:15:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d371a704ab9a071c89db966e268fe56aad2288363a849d10eb032d47cd10848b`  
		Last Modified: Wed, 09 Aug 2023 10:10:48 GMT  
		Size: 5.1 MB (5053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e38cf28101c20845f7f103114793f73691285da6ac006db5cb28c20bc8000`  
		Last Modified: Mon, 14 Aug 2023 17:39:55 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d1b8334b836b303a87ddda4bfba4af764950afa40c2c263cca11ed8b53a8c6`  
		Last Modified: Mon, 14 Aug 2023 17:39:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4434838c3cf5a9e2e8050d86c8cfc927ad8bb46c478811a034b9a51ad2e4879c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106661395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eae15fb81c48d690da2ae88d171f0c7398deaed959011a96133cdd3836caf97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:25:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 00:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:26:56 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 00:29:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 00:29:34 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 00:29:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:29:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 00:29:36 GMT
WORKDIR /go
# Tue, 08 Aug 2023 00:44:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:18:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:18:18 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:18:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:18:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:18:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:18:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966ad2cdd35689da92e7c8fd39bd37cd6080c484e6ccaf00672c154cd4f6c2a`  
		Last Modified: Tue, 08 Aug 2023 00:39:35 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7816c9df7e6881fdd62dfcc6d743edcc2c3ca9220542437a2e5fdcfa0e4548`  
		Last Modified: Tue, 08 Aug 2023 00:41:09 GMT  
		Size: 96.6 MB (96591770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d34a514a03c5af8a03dfe8c4fbfd50b2ec61591d24080f8be8bf722904f541`  
		Last Modified: Tue, 08 Aug 2023 00:40:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802af1410e20c34900a811878ca2fa2e5dc79daeb92a53b94588831011ad81fc`  
		Last Modified: Tue, 08 Aug 2023 00:45:40 GMT  
		Size: 5.2 MB (5249966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9d8614d3da52c8737c0b4449e6e9e688fc7353d31f0246eb31e74f676c1a2`  
		Last Modified: Mon, 14 Aug 2023 18:19:17 GMT  
		Size: 1.2 MB (1186181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aa14602d0d570f4ade4524880d76ae39c401058848761634a02d8513598058`  
		Last Modified: Mon, 14 Aug 2023 18:19:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4c76dac9b235685647bce5e644408f9537fd2a98243936db0666252a4ec24739
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110727449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe6eea8994d5e82ec6e85ed4c441f0a89b9cb461829805dd3eeb9d892d49a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:19:41 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Aug 2023 20:19:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:21:06 GMT
ENV GOLANG_VERSION=1.20.7
# Mon, 07 Aug 2023 20:23:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Mon, 07 Aug 2023 20:23:05 GMT
ENV GOPATH=/go
# Mon, 07 Aug 2023 20:23:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:23:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Mon, 07 Aug 2023 20:23:06 GMT
WORKDIR /go
# Tue, 08 Aug 2023 05:25:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:41:51 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:41:52 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:41:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:41:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:41:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec90be18226e5c99d10161aed1a143f4134093c55b4d6979bbdbbe4b0683eb11`  
		Last Modified: Mon, 07 Aug 2023 20:30:59 GMT  
		Size: 285.1 KB (285089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c751f85e4ba6e9bbada0b11691d914b2ec2c689bb0dca6b9cbe994488d0e3e`  
		Last Modified: Mon, 07 Aug 2023 20:31:56 GMT  
		Size: 100.9 MB (100865267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d202223222826c8580d85b8d7dd6baa8ed1cad84ba5cf47dab23eaeeae7e9`  
		Last Modified: Mon, 07 Aug 2023 20:31:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359ada615d16e203e1d40a49b896060013c2952c2982ae73b141cc291305a4c`  
		Last Modified: Tue, 08 Aug 2023 05:25:47 GMT  
		Size: 5.1 MB (5099943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1039996d136f688a91d291dcf3dbb995607af1f245f1741d8ad0c5f73cec1b01`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e7bfc7e0d6b6a7f70b22841fe42427f0fb6372b17c71c8063c50d7c8e73c1`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ca7c5b253f237a6f0d30748de0cb616efd5040889648b19dbf2d86855990a759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:d2986a3c3acb890096b8f22fe47d163b679506c701409f0f96ef55f0370c6e49
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2132346458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb468ba68962f7df97763531c45fe07444d56eeed51c25ca5019d9f06b5d07b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:39:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:39:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:41:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:41:12 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:42:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:53:35 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:56:38 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:56:40 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:20:56 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:57 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594083c5c2094c95b4e52723d54c14e0d70881f4f176720c3170012275accc3b`  
		Last Modified: Thu, 10 Aug 2023 01:02:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e2c2a5b75ced3a3a50be088c4a6c2d7df926b1fe6515b2d0c021312e3642f4`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d28688050deeec928289543beadf5c75bb2a8246576cb7c066e23818016217`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e5fbc50e7e0fefb7c9e349038ecb00ed5c000bcab8c4d82b1e1000c4273c01`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544e07bd9df923e11e09c7dc042da614f2f14589eb6fa79005ebbbf2731e97d`  
		Last Modified: Thu, 10 Aug 2023 01:02:57 GMT  
		Size: 25.6 MB (25560980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a82506c4fcec2bd90ae77756e5b03788e30c89f1a3820aa0b6a7ae6ad58ae`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcfb422b104764156fc5ba099b5e3ae9fa9f760fd2db1c21acd8969b3d73de`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 220.8 KB (220796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6aa0a5a1689ed800c4ef72c1b9febf207840fd2c6abfe4bb460e2e2bfb0b0`  
		Last Modified: Thu, 10 Aug 2023 01:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d3379322a67b2413189cc2b779d22cb4093124343c8bb17fdf720b7b49fda`  
		Last Modified: Thu, 10 Aug 2023 01:05:25 GMT  
		Size: 108.9 MB (108911716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60ccf92610ddbc47a05664785c95215a123e8930afbf6e3e2cefc80e693fd2`  
		Last Modified: Thu, 10 Aug 2023 01:05:04 GMT  
		Size: 1.5 KB (1468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c7d6253e62d61e5e0d2ad331a96cff5175f6c608b2ab4657825b3e3b4b4d0`  
		Last Modified: Thu, 10 Aug 2023 03:08:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7441bd899a1ec2037a7dc63ed24148f4362550631136f0b286d1980977fbfcfa`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60695a3cfa3d46aac3798546808cbe211d637be2b7c2af5f9d90d79eb10d544a`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636dfb4139d7b40d2a0cfa8fa63fa590d61d8627017a87a8a517c9c229fdda5b`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d287a3e1b6a016ab5e21634424eddc049708da3cc46e37cc8444f8f20d9ba206`  
		Last Modified: Mon, 14 Aug 2023 18:24:03 GMT  
		Size: 1.7 MB (1679974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cfbbc308f7ee8ad386b267faba56ca74b5aff7b32f0b71f6d94c29f5febe43`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:24c81ff6d1a33b0f08066917fb05c2a4c782bb2cd6bd1ba0217709e1e10be849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:2bf33a1b3b64f1ffe31a0ea39e974e24ae1e5d17a1d1f0d3d2c744f8f612a8a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1933831109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2a69ae1b3bbd9a3aefa279d32b203c5ef28dee21038b8b203d78518899270`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:36:23 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:36:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:36:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:36:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:37:00 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:37:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:50:52 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:53:17 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:53:18 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:06:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:22:09 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:22:10 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:22:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877256a6389e5e2563da79ad5bd201e7ee136abf14ff7cb0d4efbf3b24e5f127`  
		Last Modified: Thu, 10 Aug 2023 01:02:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a39df29b3c0b2f7e691c47273110db4a46e5c8e299f6bb95f77a9c61f79872`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8574d63bce1547e3177d0b76237a782a9b016d4880375dcd1a7b6a1c5dee3dc`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef34b3c96316bcdd92e24c8c4eebdc3a35f245c013ef87edfae0dde091a305`  
		Last Modified: Thu, 10 Aug 2023 01:02:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a481babc5b629f694446a96dba8d77c020257c98334c605aff94162b9a917279`  
		Last Modified: Thu, 10 Aug 2023 01:02:23 GMT  
		Size: 25.6 MB (25554169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281178ea1c103ff07ea7e4fb647eb0dbe4f865742da6ef9944e04f37974fc27c`  
		Last Modified: Thu, 10 Aug 2023 01:02:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5d34adf2aacfe87580143f3e17c635dc8dbd4068377b79b35d665f49bbad9`  
		Last Modified: Thu, 10 Aug 2023 01:02:16 GMT  
		Size: 275.9 KB (275946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02a2e79b5a05c2145c733eefb2add45d1ebefb7a16b93c321f5883c8ced6f1a`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd9991b8cfbc481c153abf1625143209f4c4fd40d9443a5a19f4e3613336ad2`  
		Last Modified: Thu, 10 Aug 2023 01:04:53 GMT  
		Size: 108.9 MB (108927695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dc6778f41c3c7d50b8e71668e22880153d6c6794f24c4661fc3d6aa089d0a5`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5985f015e143065716f5aabf0ecaed537103c5ec07e6c57360204a7787d02`  
		Last Modified: Thu, 10 Aug 2023 03:08:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c565e57b551adf88d5e29bd1458eb8f35437ae3145eba3114c3e38a14420307`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93046b7cb08612cc9fda41d92a61df03529a75e7d266f85a0529c5e88f7d06eb`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a40abe5aa831ec7c89060659309bccacad929792153b60f544eec13c1b6394`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8095d427fe41dd6d758aae45f422bddef28912086c3a3f7797f231535d73ca69`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.7 MB (1690912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8e6227140a7a352f358e4d9e7deab69dc502cd45903e2458244037b6bb36df`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:341d22d35fd224792f17980a37766d5750ea277b08390b43e7a926c46e16b24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:663d23efed0fab8de5c0b9b2fc5e4ec761e9837c1e3bf6fdf4a66299b137bd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:845b1d612d896dd66d62dedbd373308f5c6df2dbb0b3e24b8bf890f2e255720d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7`

```console
$ docker pull caddy@sha256:0da93d63c5b3af38288e909b953bd8cdcf12537c27ff219aac46c6a01775cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7` - linux; amd64

```console
$ docker pull caddy@sha256:f9824933254e3e43e0508670ee9bdcde704621017e95119a05317383b1878f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18631102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e9fe28a35a7bd46854ffa0afa91435071afeabac2784f8730569278d8bc9a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:09:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:20:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:20:15 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:20:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aa7b81ef11c65f43b0b58323a33dd9e07eb785529f0d75b452f87a309db00c`  
		Last Modified: Mon, 07 Aug 2023 20:09:40 GMT  
		Size: 350.8 KB (350844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b3b3e68e52dc5ab939c72a9bbac39cff4bef4b87de399ddf28657471df6845`  
		Last Modified: Mon, 14 Aug 2023 18:20:42 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e6a3c74b422682f93a437993c6365f8008e89737276364fd12ea870022f03`  
		Last Modified: Mon, 14 Aug 2023 18:20:45 GMT  
		Size: 14.9 MB (14871143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dc698bd1b82521df87ea42fbf48c98d10133ec962497ac80527b65769ceb6a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17690701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3775ac20cca67f4d547f26f5984a989b9407b0c4129fd6cd86dbb3359249acd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:38:27 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:49:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:49:14 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:49:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:49:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:49:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ef460a93549b8a3e73f6a515bccad93512788d1e8f095e7230ba41967c25a`  
		Last Modified: Wed, 09 Aug 2023 03:38:53 GMT  
		Size: 347.7 KB (347686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aae78767a581df85fd1a51ccd646619aec320896ca016ef0f05a41b16bcbfe`  
		Last Modified: Mon, 14 Aug 2023 17:49:36 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5244db1c019e66038874df2b8b92c74437f6d355802bfccada90c9d8bd8d29`  
		Last Modified: Mon, 14 Aug 2023 17:49:38 GMT  
		Size: 14.2 MB (14190701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e9cb1245e1c134e25a0ec0803e5132ba9ba92d0a4ad85db3f73bd2c3188cf70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17414619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6e2a1f4c707dc77276814a27ac22a7b5de268780603d8e08324130e1fc563`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:57:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:57:17 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:57:21 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:57:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a47b73e04459258b08555443754e92e2db20bde113c58ca18e1a6f07878f72`  
		Last Modified: Tue, 08 Aug 2023 01:52:05 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1b3e18d5e992f1805072b2d52405d575830bdce21726ef99dea99e31d8277`  
		Last Modified: Mon, 14 Aug 2023 17:57:42 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2b7485982d191f9dc0498d5b940d14df575f36ca66876b92d3ca09ff9386b2`  
		Last Modified: Mon, 14 Aug 2023 17:57:48 GMT  
		Size: 14.2 MB (14163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:db04154ce5f7a7f4d058567375880cdc6b1a3675095ad576f9886f39f1374afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731c0ae21a974e5708c4a8006250893bca5a2ecad43babf2a0a95a60fc61d6cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:09:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:39:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:39:19 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:39:22 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a699f78cfb85f60e17fc7c13495876ea0cb4495bbe39e8c65f3e8559b0d7169`  
		Last Modified: Mon, 07 Aug 2023 21:09:34 GMT  
		Size: 360.6 KB (360642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7488af8b96c79b6db13955a0302653c4e9f314d0833201984ae06c1ed697f06`  
		Last Modified: Mon, 14 Aug 2023 17:39:41 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9600da6e7e51b9083b29f3c7de592fa45e7765ca5ffe8d2abf7cc99c50578fe`  
		Last Modified: Mon, 14 Aug 2023 17:39:43 GMT  
		Size: 13.6 MB (13630728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; ppc64le

```console
$ docker pull caddy@sha256:dfe8f314baac04dac7b7d48bdd1999aedd42d82f792d5a921be7b9a38adbcc07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17021924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09511fed803e1230efcb1c914154726b2f232029c67b0c681319b2eb6ee73a3c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:44:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:18:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:18:00 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:18:05 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:10 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:11 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:18:11 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:18:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f40714f45e39ac41e865ccbf2877db62255ce5a5c36a47eadf00b9d174f042`  
		Last Modified: Tue, 08 Aug 2023 00:45:18 GMT  
		Size: 362.2 KB (362173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d19953b5eb53ddaa0e25905527dc138e0c4111467bb7d71f81fa94976091351`  
		Last Modified: Mon, 14 Aug 2023 18:18:54 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff11295d70af9c740cf7afdb57754d70bffd7cd42271ba1a6de34195de6b249`  
		Last Modified: Mon, 14 Aug 2023 18:18:58 GMT  
		Size: 13.3 MB (13305991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; s390x

```console
$ docker pull caddy@sha256:3b3d4b80e160105a760ad62b32c497245d69676e6053c2a7b61bc5c6fc178fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17984968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a63d05bc7601e47460ff86bc91380fd9407c0b4886b80836ac3aadb436f68e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:14:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:41:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:41:39 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:41:44 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:41:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df19abd0ca1d4a821a4174a2c0831a57d6fd584073f056abcae085a51f0b3848`  
		Last Modified: Mon, 07 Aug 2023 20:14:50 GMT  
		Size: 354.9 KB (354950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308478977890baa82477ee70a3065fb9da2080efcc95facf1a87ac021b06a8e9`  
		Last Modified: Mon, 14 Aug 2023 17:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fe1cbba37a3c1c2f6ba50e59e5c238c8d83ffca820ef709108b9e3253af757`  
		Last Modified: Mon, 14 Aug 2023 17:42:19 GMT  
		Size: 14.4 MB (14408320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-alpine`

```console
$ docker pull caddy@sha256:60de297131e676c0d87d7aacaa4fbd5a883abb5818977670f7024b89ebe1d7bb
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
$ docker pull caddy@sha256:f9824933254e3e43e0508670ee9bdcde704621017e95119a05317383b1878f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18631102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e9fe28a35a7bd46854ffa0afa91435071afeabac2784f8730569278d8bc9a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:09:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:20:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:20:15 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:20:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aa7b81ef11c65f43b0b58323a33dd9e07eb785529f0d75b452f87a309db00c`  
		Last Modified: Mon, 07 Aug 2023 20:09:40 GMT  
		Size: 350.8 KB (350844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b3b3e68e52dc5ab939c72a9bbac39cff4bef4b87de399ddf28657471df6845`  
		Last Modified: Mon, 14 Aug 2023 18:20:42 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e6a3c74b422682f93a437993c6365f8008e89737276364fd12ea870022f03`  
		Last Modified: Mon, 14 Aug 2023 18:20:45 GMT  
		Size: 14.9 MB (14871143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dc698bd1b82521df87ea42fbf48c98d10133ec962497ac80527b65769ceb6a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17690701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3775ac20cca67f4d547f26f5984a989b9407b0c4129fd6cd86dbb3359249acd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:38:27 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:49:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:49:14 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:49:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:49:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:49:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ef460a93549b8a3e73f6a515bccad93512788d1e8f095e7230ba41967c25a`  
		Last Modified: Wed, 09 Aug 2023 03:38:53 GMT  
		Size: 347.7 KB (347686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aae78767a581df85fd1a51ccd646619aec320896ca016ef0f05a41b16bcbfe`  
		Last Modified: Mon, 14 Aug 2023 17:49:36 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5244db1c019e66038874df2b8b92c74437f6d355802bfccada90c9d8bd8d29`  
		Last Modified: Mon, 14 Aug 2023 17:49:38 GMT  
		Size: 14.2 MB (14190701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e9cb1245e1c134e25a0ec0803e5132ba9ba92d0a4ad85db3f73bd2c3188cf70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17414619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6e2a1f4c707dc77276814a27ac22a7b5de268780603d8e08324130e1fc563`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:57:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:57:17 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:57:21 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:57:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a47b73e04459258b08555443754e92e2db20bde113c58ca18e1a6f07878f72`  
		Last Modified: Tue, 08 Aug 2023 01:52:05 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1b3e18d5e992f1805072b2d52405d575830bdce21726ef99dea99e31d8277`  
		Last Modified: Mon, 14 Aug 2023 17:57:42 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2b7485982d191f9dc0498d5b940d14df575f36ca66876b92d3ca09ff9386b2`  
		Last Modified: Mon, 14 Aug 2023 17:57:48 GMT  
		Size: 14.2 MB (14163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:db04154ce5f7a7f4d058567375880cdc6b1a3675095ad576f9886f39f1374afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731c0ae21a974e5708c4a8006250893bca5a2ecad43babf2a0a95a60fc61d6cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:09:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:39:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:39:19 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:39:22 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a699f78cfb85f60e17fc7c13495876ea0cb4495bbe39e8c65f3e8559b0d7169`  
		Last Modified: Mon, 07 Aug 2023 21:09:34 GMT  
		Size: 360.6 KB (360642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7488af8b96c79b6db13955a0302653c4e9f314d0833201984ae06c1ed697f06`  
		Last Modified: Mon, 14 Aug 2023 17:39:41 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9600da6e7e51b9083b29f3c7de592fa45e7765ca5ffe8d2abf7cc99c50578fe`  
		Last Modified: Mon, 14 Aug 2023 17:39:43 GMT  
		Size: 13.6 MB (13630728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:dfe8f314baac04dac7b7d48bdd1999aedd42d82f792d5a921be7b9a38adbcc07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17021924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09511fed803e1230efcb1c914154726b2f232029c67b0c681319b2eb6ee73a3c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:44:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:18:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:18:00 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:18:05 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:10 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:11 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:18:11 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:18:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f40714f45e39ac41e865ccbf2877db62255ce5a5c36a47eadf00b9d174f042`  
		Last Modified: Tue, 08 Aug 2023 00:45:18 GMT  
		Size: 362.2 KB (362173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d19953b5eb53ddaa0e25905527dc138e0c4111467bb7d71f81fa94976091351`  
		Last Modified: Mon, 14 Aug 2023 18:18:54 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff11295d70af9c740cf7afdb57754d70bffd7cd42271ba1a6de34195de6b249`  
		Last Modified: Mon, 14 Aug 2023 18:18:58 GMT  
		Size: 13.3 MB (13305991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:3b3d4b80e160105a760ad62b32c497245d69676e6053c2a7b61bc5c6fc178fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17984968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a63d05bc7601e47460ff86bc91380fd9407c0b4886b80836ac3aadb436f68e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:14:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:41:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:41:39 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:41:44 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:41:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df19abd0ca1d4a821a4174a2c0831a57d6fd584073f056abcae085a51f0b3848`  
		Last Modified: Mon, 07 Aug 2023 20:14:50 GMT  
		Size: 354.9 KB (354950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308478977890baa82477ee70a3065fb9da2080efcc95facf1a87ac021b06a8e9`  
		Last Modified: Mon, 14 Aug 2023 17:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fe1cbba37a3c1c2f6ba50e59e5c238c8d83ffca820ef709108b9e3253af757`  
		Last Modified: Mon, 14 Aug 2023 17:42:19 GMT  
		Size: 14.4 MB (14408320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder`

```console
$ docker pull caddy@sha256:72235016961770347eb1ca2771c13e5e406c0091e3584d0bc7dd6ffbd481abd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7-builder` - linux; amd64

```console
$ docker pull caddy@sha256:7a4a3476f0991b84458cf29307f0c064e6b5fdd6af0019dc36a76576dc0721f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110902575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e1c25fbce7e1bbf91803ddf419d9de799552698d44cac3fe01a21c05cd3f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:36:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 09 Aug 2023 04:41:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:41:57 GMT
ENV GOLANG_VERSION=1.20.7
# Wed, 09 Aug 2023 04:43:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 09 Aug 2023 04:43:29 GMT
ENV GOPATH=/go
# Wed, 09 Aug 2023 04:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:43:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 09 Aug 2023 04:43:30 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:26:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:21 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:20:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:20:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:20:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d48a809fc2256f8aa0aeee47998488d64409855adba00a7cb3007ab9f3286e`  
		Last Modified: Wed, 09 Aug 2023 03:37:02 GMT  
		Size: 284.7 KB (284693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e790db5857269a95a948a96f0e3304c851351e588262d58504700b2e73fb7fe`  
		Last Modified: Wed, 09 Aug 2023 04:47:32 GMT  
		Size: 101.0 MB (100954810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f4e1a48a681e22437b6c14b04a4e287386f50f1be21ef490a1e28fd276a91`  
		Last Modified: Wed, 09 Aug 2023 04:47:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a272b880a0f8927853947bb9b16e005e2824b1685a89cc015f4e4694c441ed0e`  
		Last Modified: Wed, 09 Aug 2023 10:26:35 GMT  
		Size: 5.0 MB (4958652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636df467d23fd7ec3f363a1403da4b23c878bb239a4a4b9fdbf55f0189f9cbb1`  
		Last Modified: Mon, 14 Aug 2023 18:20:59 GMT  
		Size: 1.3 MB (1302244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afb5bd80935e22cbe3f7bb67cae35b420386beb37b9390eeab25fcef89b65d7`  
		Last Modified: Mon, 14 Aug 2023 18:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:289b1f78db36a7524bbae6562b80b29fe5585984effd44a3e22146fcbf4ab824
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108301221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac734398939dbe1f4c664f493d34b5353c438189c6b58b3e6e4d92186a8f80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:12:05 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:12:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:40 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:14:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:14:36 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:14:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:14:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:14:37 GMT
WORKDIR /go
# Wed, 09 Aug 2023 03:38:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:49:20 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:49:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:49:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8564ce36feee688566265012773f1c8c7c046ceefe86ca763eb702682f4e6e75`  
		Last Modified: Tue, 08 Aug 2023 23:15:06 GMT  
		Size: 284.9 KB (284876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b139603b026cc15bf570c9cf012fc165cb74821883c7c7c534fe6ed189b5a2`  
		Last Modified: Tue, 08 Aug 2023 23:16:29 GMT  
		Size: 98.7 MB (98671161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b2f37c2778ffd2e158ad31438d6802c214dfa5d79e06dc9af2d8320828e148`  
		Last Modified: Tue, 08 Aug 2023 23:16:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22c305527b162efa854ac3e1963e59e7fb8f2c71838222c56462b9809481ed`  
		Last Modified: Wed, 09 Aug 2023 03:39:10 GMT  
		Size: 5.0 MB (4951147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5520daf22ad222fbe3c81bbd6afa0c912b3817f0f432a35a939f9870a8512af`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 1.2 MB (1248666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f8fe3942ebea0d37a8324080324eb0bca35e859273e7bac44381e31a0fa714`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:dcbac62a4e9d8d10345a7f20ac37a814b45633ed4b050a14fa20aef08590597a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107386270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee903aaec70e29acbd506823b19cc477dc7788e545d1b88316b9ec0e9c154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:39:47 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 01:39:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:40:29 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 01:42:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 01:42:12 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 01:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:42:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 01:42:13 GMT
WORKDIR /go
# Tue, 08 Aug 2023 01:51:50 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:57:24 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:57:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:57:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:57:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47bd95d78f565e902bafd0264a979eb4f6f71e22c0464011bf9db6feb0579e6`  
		Last Modified: Tue, 08 Aug 2023 01:48:34 GMT  
		Size: 284.1 KB (284073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a674106498848b269b5cb69fb938d3dc97247d02cb1aa3927b7a7469724e950`  
		Last Modified: Tue, 08 Aug 2023 01:49:43 GMT  
		Size: 98.5 MB (98454659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1902a68db0b07b05ab7d2f3e48ca8f1d22951b498f6ff9027bdc91a5e7e830`  
		Last Modified: Tue, 08 Aug 2023 01:49:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf1886c556e441f6f89cd1cb00e1b950d9d8fcad8812a988fbb59caf0b0ba5`  
		Last Modified: Tue, 08 Aug 2023 01:52:22 GMT  
		Size: 4.5 MB (4501403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28b1afe92de619aa5de35a2f610dc68af6b39c6cd300ef8426738a739366a2`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 1.2 MB (1246092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe75fd67d7668d6aeca167419514f45cb72ec61bd61a9fc32e25b5c928dba6`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ad7390f7aa878bd4d6750dab9611c7397630fc15a7f80304eea3d3f64dcfe4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105987240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79cdcd45a4a61e8fe257b7917335ede1523a72d1c2ef2eb9115783a5379f5ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:10:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:10:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:53 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:11:59 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:11:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:12:00 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:10:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:39:25 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54e960e981301b0098c80d2e61d694333b5ab480a007a3a8d0fa629662d377`  
		Last Modified: Tue, 08 Aug 2023 23:14:21 GMT  
		Size: 286.3 KB (286298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ccffba14f84f51f896ae916a3dd045a0b0d08dc27d53f7d6a9dc5687c3501`  
		Last Modified: Tue, 08 Aug 2023 23:15:23 GMT  
		Size: 96.1 MB (96117263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d452dd4d3acc29d43b0be67bcc0c121814601787c7fd45e8260687d2cc8983`  
		Last Modified: Tue, 08 Aug 2023 23:15:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d371a704ab9a071c89db966e268fe56aad2288363a849d10eb032d47cd10848b`  
		Last Modified: Wed, 09 Aug 2023 10:10:48 GMT  
		Size: 5.1 MB (5053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e38cf28101c20845f7f103114793f73691285da6ac006db5cb28c20bc8000`  
		Last Modified: Mon, 14 Aug 2023 17:39:55 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d1b8334b836b303a87ddda4bfba4af764950afa40c2c263cca11ed8b53a8c6`  
		Last Modified: Mon, 14 Aug 2023 17:39:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4434838c3cf5a9e2e8050d86c8cfc927ad8bb46c478811a034b9a51ad2e4879c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106661395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eae15fb81c48d690da2ae88d171f0c7398deaed959011a96133cdd3836caf97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:25:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 00:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:26:56 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 00:29:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 00:29:34 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 00:29:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:29:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 00:29:36 GMT
WORKDIR /go
# Tue, 08 Aug 2023 00:44:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:18:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:18:18 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:18:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:18:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:18:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:18:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966ad2cdd35689da92e7c8fd39bd37cd6080c484e6ccaf00672c154cd4f6c2a`  
		Last Modified: Tue, 08 Aug 2023 00:39:35 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7816c9df7e6881fdd62dfcc6d743edcc2c3ca9220542437a2e5fdcfa0e4548`  
		Last Modified: Tue, 08 Aug 2023 00:41:09 GMT  
		Size: 96.6 MB (96591770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d34a514a03c5af8a03dfe8c4fbfd50b2ec61591d24080f8be8bf722904f541`  
		Last Modified: Tue, 08 Aug 2023 00:40:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802af1410e20c34900a811878ca2fa2e5dc79daeb92a53b94588831011ad81fc`  
		Last Modified: Tue, 08 Aug 2023 00:45:40 GMT  
		Size: 5.2 MB (5249966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9d8614d3da52c8737c0b4449e6e9e688fc7353d31f0246eb31e74f676c1a2`  
		Last Modified: Mon, 14 Aug 2023 18:19:17 GMT  
		Size: 1.2 MB (1186181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aa14602d0d570f4ade4524880d76ae39c401058848761634a02d8513598058`  
		Last Modified: Mon, 14 Aug 2023 18:19:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; s390x

```console
$ docker pull caddy@sha256:4c76dac9b235685647bce5e644408f9537fd2a98243936db0666252a4ec24739
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110727449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe6eea8994d5e82ec6e85ed4c441f0a89b9cb461829805dd3eeb9d892d49a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:19:41 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Aug 2023 20:19:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:21:06 GMT
ENV GOLANG_VERSION=1.20.7
# Mon, 07 Aug 2023 20:23:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Mon, 07 Aug 2023 20:23:05 GMT
ENV GOPATH=/go
# Mon, 07 Aug 2023 20:23:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:23:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Mon, 07 Aug 2023 20:23:06 GMT
WORKDIR /go
# Tue, 08 Aug 2023 05:25:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:41:51 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:41:52 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:41:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:41:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:41:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec90be18226e5c99d10161aed1a143f4134093c55b4d6979bbdbbe4b0683eb11`  
		Last Modified: Mon, 07 Aug 2023 20:30:59 GMT  
		Size: 285.1 KB (285089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c751f85e4ba6e9bbada0b11691d914b2ec2c689bb0dca6b9cbe994488d0e3e`  
		Last Modified: Mon, 07 Aug 2023 20:31:56 GMT  
		Size: 100.9 MB (100865267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d202223222826c8580d85b8d7dd6baa8ed1cad84ba5cf47dab23eaeeae7e9`  
		Last Modified: Mon, 07 Aug 2023 20:31:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359ada615d16e203e1d40a49b896060013c2952c2982ae73b141cc291305a4c`  
		Last Modified: Tue, 08 Aug 2023 05:25:47 GMT  
		Size: 5.1 MB (5099943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1039996d136f688a91d291dcf3dbb995607af1f245f1741d8ad0c5f73cec1b01`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e7bfc7e0d6b6a7f70b22841fe42427f0fb6372b17c71c8063c50d7c8e73c1`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:d2986a3c3acb890096b8f22fe47d163b679506c701409f0f96ef55f0370c6e49
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2132346458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb468ba68962f7df97763531c45fe07444d56eeed51c25ca5019d9f06b5d07b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:39:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:39:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:41:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:41:12 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:42:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:53:35 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:56:38 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:56:40 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:20:56 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:57 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594083c5c2094c95b4e52723d54c14e0d70881f4f176720c3170012275accc3b`  
		Last Modified: Thu, 10 Aug 2023 01:02:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e2c2a5b75ced3a3a50be088c4a6c2d7df926b1fe6515b2d0c021312e3642f4`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d28688050deeec928289543beadf5c75bb2a8246576cb7c066e23818016217`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e5fbc50e7e0fefb7c9e349038ecb00ed5c000bcab8c4d82b1e1000c4273c01`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544e07bd9df923e11e09c7dc042da614f2f14589eb6fa79005ebbbf2731e97d`  
		Last Modified: Thu, 10 Aug 2023 01:02:57 GMT  
		Size: 25.6 MB (25560980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a82506c4fcec2bd90ae77756e5b03788e30c89f1a3820aa0b6a7ae6ad58ae`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcfb422b104764156fc5ba099b5e3ae9fa9f760fd2db1c21acd8969b3d73de`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 220.8 KB (220796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6aa0a5a1689ed800c4ef72c1b9febf207840fd2c6abfe4bb460e2e2bfb0b0`  
		Last Modified: Thu, 10 Aug 2023 01:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d3379322a67b2413189cc2b779d22cb4093124343c8bb17fdf720b7b49fda`  
		Last Modified: Thu, 10 Aug 2023 01:05:25 GMT  
		Size: 108.9 MB (108911716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60ccf92610ddbc47a05664785c95215a123e8930afbf6e3e2cefc80e693fd2`  
		Last Modified: Thu, 10 Aug 2023 01:05:04 GMT  
		Size: 1.5 KB (1468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c7d6253e62d61e5e0d2ad331a96cff5175f6c608b2ab4657825b3e3b4b4d0`  
		Last Modified: Thu, 10 Aug 2023 03:08:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7441bd899a1ec2037a7dc63ed24148f4362550631136f0b286d1980977fbfcfa`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60695a3cfa3d46aac3798546808cbe211d637be2b7c2af5f9d90d79eb10d544a`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636dfb4139d7b40d2a0cfa8fa63fa590d61d8627017a87a8a517c9c229fdda5b`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d287a3e1b6a016ab5e21634424eddc049708da3cc46e37cc8444f8f20d9ba206`  
		Last Modified: Mon, 14 Aug 2023 18:24:03 GMT  
		Size: 1.7 MB (1679974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cfbbc308f7ee8ad386b267faba56ca74b5aff7b32f0b71f6d94c29f5febe43`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:2bf33a1b3b64f1ffe31a0ea39e974e24ae1e5d17a1d1f0d3d2c744f8f612a8a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1933831109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2a69ae1b3bbd9a3aefa279d32b203c5ef28dee21038b8b203d78518899270`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:36:23 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:36:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:36:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:36:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:37:00 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:37:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:50:52 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:53:17 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:53:18 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:06:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:22:09 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:22:10 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:22:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877256a6389e5e2563da79ad5bd201e7ee136abf14ff7cb0d4efbf3b24e5f127`  
		Last Modified: Thu, 10 Aug 2023 01:02:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a39df29b3c0b2f7e691c47273110db4a46e5c8e299f6bb95f77a9c61f79872`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8574d63bce1547e3177d0b76237a782a9b016d4880375dcd1a7b6a1c5dee3dc`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef34b3c96316bcdd92e24c8c4eebdc3a35f245c013ef87edfae0dde091a305`  
		Last Modified: Thu, 10 Aug 2023 01:02:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a481babc5b629f694446a96dba8d77c020257c98334c605aff94162b9a917279`  
		Last Modified: Thu, 10 Aug 2023 01:02:23 GMT  
		Size: 25.6 MB (25554169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281178ea1c103ff07ea7e4fb647eb0dbe4f865742da6ef9944e04f37974fc27c`  
		Last Modified: Thu, 10 Aug 2023 01:02:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5d34adf2aacfe87580143f3e17c635dc8dbd4068377b79b35d665f49bbad9`  
		Last Modified: Thu, 10 Aug 2023 01:02:16 GMT  
		Size: 275.9 KB (275946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02a2e79b5a05c2145c733eefb2add45d1ebefb7a16b93c321f5883c8ced6f1a`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd9991b8cfbc481c153abf1625143209f4c4fd40d9443a5a19f4e3613336ad2`  
		Last Modified: Thu, 10 Aug 2023 01:04:53 GMT  
		Size: 108.9 MB (108927695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dc6778f41c3c7d50b8e71668e22880153d6c6794f24c4661fc3d6aa089d0a5`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5985f015e143065716f5aabf0ecaed537103c5ec07e6c57360204a7787d02`  
		Last Modified: Thu, 10 Aug 2023 03:08:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c565e57b551adf88d5e29bd1458eb8f35437ae3145eba3114c3e38a14420307`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93046b7cb08612cc9fda41d92a61df03529a75e7d266f85a0529c5e88f7d06eb`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a40abe5aa831ec7c89060659309bccacad929792153b60f544eec13c1b6394`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8095d427fe41dd6d758aae45f422bddef28912086c3a3f7797f231535d73ca69`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.7 MB (1690912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8e6227140a7a352f358e4d9e7deab69dc502cd45903e2458244037b6bb36df`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:d8bcb1d79bd1a9970df74b9b92ced472e5ee3d2f17f16bdb9383d6f8e00bacc0
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
$ docker pull caddy@sha256:7a4a3476f0991b84458cf29307f0c064e6b5fdd6af0019dc36a76576dc0721f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110902575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e1c25fbce7e1bbf91803ddf419d9de799552698d44cac3fe01a21c05cd3f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:36:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 09 Aug 2023 04:41:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:41:57 GMT
ENV GOLANG_VERSION=1.20.7
# Wed, 09 Aug 2023 04:43:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 09 Aug 2023 04:43:29 GMT
ENV GOPATH=/go
# Wed, 09 Aug 2023 04:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:43:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 09 Aug 2023 04:43:30 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:26:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:21 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:20:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:20:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:20:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d48a809fc2256f8aa0aeee47998488d64409855adba00a7cb3007ab9f3286e`  
		Last Modified: Wed, 09 Aug 2023 03:37:02 GMT  
		Size: 284.7 KB (284693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e790db5857269a95a948a96f0e3304c851351e588262d58504700b2e73fb7fe`  
		Last Modified: Wed, 09 Aug 2023 04:47:32 GMT  
		Size: 101.0 MB (100954810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f4e1a48a681e22437b6c14b04a4e287386f50f1be21ef490a1e28fd276a91`  
		Last Modified: Wed, 09 Aug 2023 04:47:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a272b880a0f8927853947bb9b16e005e2824b1685a89cc015f4e4694c441ed0e`  
		Last Modified: Wed, 09 Aug 2023 10:26:35 GMT  
		Size: 5.0 MB (4958652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636df467d23fd7ec3f363a1403da4b23c878bb239a4a4b9fdbf55f0189f9cbb1`  
		Last Modified: Mon, 14 Aug 2023 18:20:59 GMT  
		Size: 1.3 MB (1302244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afb5bd80935e22cbe3f7bb67cae35b420386beb37b9390eeab25fcef89b65d7`  
		Last Modified: Mon, 14 Aug 2023 18:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:289b1f78db36a7524bbae6562b80b29fe5585984effd44a3e22146fcbf4ab824
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108301221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac734398939dbe1f4c664f493d34b5353c438189c6b58b3e6e4d92186a8f80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:12:05 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:12:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:40 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:14:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:14:36 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:14:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:14:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:14:37 GMT
WORKDIR /go
# Wed, 09 Aug 2023 03:38:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:49:20 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:49:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:49:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8564ce36feee688566265012773f1c8c7c046ceefe86ca763eb702682f4e6e75`  
		Last Modified: Tue, 08 Aug 2023 23:15:06 GMT  
		Size: 284.9 KB (284876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b139603b026cc15bf570c9cf012fc165cb74821883c7c7c534fe6ed189b5a2`  
		Last Modified: Tue, 08 Aug 2023 23:16:29 GMT  
		Size: 98.7 MB (98671161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b2f37c2778ffd2e158ad31438d6802c214dfa5d79e06dc9af2d8320828e148`  
		Last Modified: Tue, 08 Aug 2023 23:16:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22c305527b162efa854ac3e1963e59e7fb8f2c71838222c56462b9809481ed`  
		Last Modified: Wed, 09 Aug 2023 03:39:10 GMT  
		Size: 5.0 MB (4951147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5520daf22ad222fbe3c81bbd6afa0c912b3817f0f432a35a939f9870a8512af`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 1.2 MB (1248666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f8fe3942ebea0d37a8324080324eb0bca35e859273e7bac44381e31a0fa714`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:dcbac62a4e9d8d10345a7f20ac37a814b45633ed4b050a14fa20aef08590597a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107386270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee903aaec70e29acbd506823b19cc477dc7788e545d1b88316b9ec0e9c154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:39:47 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 01:39:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:40:29 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 01:42:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 01:42:12 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 01:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:42:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 01:42:13 GMT
WORKDIR /go
# Tue, 08 Aug 2023 01:51:50 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:57:24 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:57:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:57:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:57:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47bd95d78f565e902bafd0264a979eb4f6f71e22c0464011bf9db6feb0579e6`  
		Last Modified: Tue, 08 Aug 2023 01:48:34 GMT  
		Size: 284.1 KB (284073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a674106498848b269b5cb69fb938d3dc97247d02cb1aa3927b7a7469724e950`  
		Last Modified: Tue, 08 Aug 2023 01:49:43 GMT  
		Size: 98.5 MB (98454659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1902a68db0b07b05ab7d2f3e48ca8f1d22951b498f6ff9027bdc91a5e7e830`  
		Last Modified: Tue, 08 Aug 2023 01:49:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf1886c556e441f6f89cd1cb00e1b950d9d8fcad8812a988fbb59caf0b0ba5`  
		Last Modified: Tue, 08 Aug 2023 01:52:22 GMT  
		Size: 4.5 MB (4501403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28b1afe92de619aa5de35a2f610dc68af6b39c6cd300ef8426738a739366a2`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 1.2 MB (1246092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe75fd67d7668d6aeca167419514f45cb72ec61bd61a9fc32e25b5c928dba6`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ad7390f7aa878bd4d6750dab9611c7397630fc15a7f80304eea3d3f64dcfe4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105987240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79cdcd45a4a61e8fe257b7917335ede1523a72d1c2ef2eb9115783a5379f5ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:10:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:10:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:53 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:11:59 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:11:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:12:00 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:10:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:39:25 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54e960e981301b0098c80d2e61d694333b5ab480a007a3a8d0fa629662d377`  
		Last Modified: Tue, 08 Aug 2023 23:14:21 GMT  
		Size: 286.3 KB (286298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ccffba14f84f51f896ae916a3dd045a0b0d08dc27d53f7d6a9dc5687c3501`  
		Last Modified: Tue, 08 Aug 2023 23:15:23 GMT  
		Size: 96.1 MB (96117263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d452dd4d3acc29d43b0be67bcc0c121814601787c7fd45e8260687d2cc8983`  
		Last Modified: Tue, 08 Aug 2023 23:15:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d371a704ab9a071c89db966e268fe56aad2288363a849d10eb032d47cd10848b`  
		Last Modified: Wed, 09 Aug 2023 10:10:48 GMT  
		Size: 5.1 MB (5053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e38cf28101c20845f7f103114793f73691285da6ac006db5cb28c20bc8000`  
		Last Modified: Mon, 14 Aug 2023 17:39:55 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d1b8334b836b303a87ddda4bfba4af764950afa40c2c263cca11ed8b53a8c6`  
		Last Modified: Mon, 14 Aug 2023 17:39:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4434838c3cf5a9e2e8050d86c8cfc927ad8bb46c478811a034b9a51ad2e4879c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106661395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eae15fb81c48d690da2ae88d171f0c7398deaed959011a96133cdd3836caf97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:25:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 00:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:26:56 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 00:29:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 00:29:34 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 00:29:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:29:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 00:29:36 GMT
WORKDIR /go
# Tue, 08 Aug 2023 00:44:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:18:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:18:18 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:18:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:18:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:18:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:18:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966ad2cdd35689da92e7c8fd39bd37cd6080c484e6ccaf00672c154cd4f6c2a`  
		Last Modified: Tue, 08 Aug 2023 00:39:35 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7816c9df7e6881fdd62dfcc6d743edcc2c3ca9220542437a2e5fdcfa0e4548`  
		Last Modified: Tue, 08 Aug 2023 00:41:09 GMT  
		Size: 96.6 MB (96591770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d34a514a03c5af8a03dfe8c4fbfd50b2ec61591d24080f8be8bf722904f541`  
		Last Modified: Tue, 08 Aug 2023 00:40:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802af1410e20c34900a811878ca2fa2e5dc79daeb92a53b94588831011ad81fc`  
		Last Modified: Tue, 08 Aug 2023 00:45:40 GMT  
		Size: 5.2 MB (5249966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9d8614d3da52c8737c0b4449e6e9e688fc7353d31f0246eb31e74f676c1a2`  
		Last Modified: Mon, 14 Aug 2023 18:19:17 GMT  
		Size: 1.2 MB (1186181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aa14602d0d570f4ade4524880d76ae39c401058848761634a02d8513598058`  
		Last Modified: Mon, 14 Aug 2023 18:19:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4c76dac9b235685647bce5e644408f9537fd2a98243936db0666252a4ec24739
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110727449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe6eea8994d5e82ec6e85ed4c441f0a89b9cb461829805dd3eeb9d892d49a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:19:41 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Aug 2023 20:19:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:21:06 GMT
ENV GOLANG_VERSION=1.20.7
# Mon, 07 Aug 2023 20:23:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Mon, 07 Aug 2023 20:23:05 GMT
ENV GOPATH=/go
# Mon, 07 Aug 2023 20:23:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:23:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Mon, 07 Aug 2023 20:23:06 GMT
WORKDIR /go
# Tue, 08 Aug 2023 05:25:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:41:51 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:41:52 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:41:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:41:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:41:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec90be18226e5c99d10161aed1a143f4134093c55b4d6979bbdbbe4b0683eb11`  
		Last Modified: Mon, 07 Aug 2023 20:30:59 GMT  
		Size: 285.1 KB (285089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c751f85e4ba6e9bbada0b11691d914b2ec2c689bb0dca6b9cbe994488d0e3e`  
		Last Modified: Mon, 07 Aug 2023 20:31:56 GMT  
		Size: 100.9 MB (100865267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d202223222826c8580d85b8d7dd6baa8ed1cad84ba5cf47dab23eaeeae7e9`  
		Last Modified: Mon, 07 Aug 2023 20:31:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359ada615d16e203e1d40a49b896060013c2952c2982ae73b141cc291305a4c`  
		Last Modified: Tue, 08 Aug 2023 05:25:47 GMT  
		Size: 5.1 MB (5099943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1039996d136f688a91d291dcf3dbb995607af1f245f1741d8ad0c5f73cec1b01`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e7bfc7e0d6b6a7f70b22841fe42427f0fb6372b17c71c8063c50d7c8e73c1`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ca7c5b253f237a6f0d30748de0cb616efd5040889648b19dbf2d86855990a759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:d2986a3c3acb890096b8f22fe47d163b679506c701409f0f96ef55f0370c6e49
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2132346458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb468ba68962f7df97763531c45fe07444d56eeed51c25ca5019d9f06b5d07b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:39:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:39:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:41:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:41:12 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:42:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:53:35 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:56:38 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:56:40 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:20:56 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:57 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594083c5c2094c95b4e52723d54c14e0d70881f4f176720c3170012275accc3b`  
		Last Modified: Thu, 10 Aug 2023 01:02:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e2c2a5b75ced3a3a50be088c4a6c2d7df926b1fe6515b2d0c021312e3642f4`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d28688050deeec928289543beadf5c75bb2a8246576cb7c066e23818016217`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e5fbc50e7e0fefb7c9e349038ecb00ed5c000bcab8c4d82b1e1000c4273c01`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544e07bd9df923e11e09c7dc042da614f2f14589eb6fa79005ebbbf2731e97d`  
		Last Modified: Thu, 10 Aug 2023 01:02:57 GMT  
		Size: 25.6 MB (25560980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a82506c4fcec2bd90ae77756e5b03788e30c89f1a3820aa0b6a7ae6ad58ae`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcfb422b104764156fc5ba099b5e3ae9fa9f760fd2db1c21acd8969b3d73de`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 220.8 KB (220796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6aa0a5a1689ed800c4ef72c1b9febf207840fd2c6abfe4bb460e2e2bfb0b0`  
		Last Modified: Thu, 10 Aug 2023 01:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d3379322a67b2413189cc2b779d22cb4093124343c8bb17fdf720b7b49fda`  
		Last Modified: Thu, 10 Aug 2023 01:05:25 GMT  
		Size: 108.9 MB (108911716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60ccf92610ddbc47a05664785c95215a123e8930afbf6e3e2cefc80e693fd2`  
		Last Modified: Thu, 10 Aug 2023 01:05:04 GMT  
		Size: 1.5 KB (1468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c7d6253e62d61e5e0d2ad331a96cff5175f6c608b2ab4657825b3e3b4b4d0`  
		Last Modified: Thu, 10 Aug 2023 03:08:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7441bd899a1ec2037a7dc63ed24148f4362550631136f0b286d1980977fbfcfa`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60695a3cfa3d46aac3798546808cbe211d637be2b7c2af5f9d90d79eb10d544a`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636dfb4139d7b40d2a0cfa8fa63fa590d61d8627017a87a8a517c9c229fdda5b`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d287a3e1b6a016ab5e21634424eddc049708da3cc46e37cc8444f8f20d9ba206`  
		Last Modified: Mon, 14 Aug 2023 18:24:03 GMT  
		Size: 1.7 MB (1679974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cfbbc308f7ee8ad386b267faba56ca74b5aff7b32f0b71f6d94c29f5febe43`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:24c81ff6d1a33b0f08066917fb05c2a4c782bb2cd6bd1ba0217709e1e10be849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:2bf33a1b3b64f1ffe31a0ea39e974e24ae1e5d17a1d1f0d3d2c744f8f612a8a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1933831109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2a69ae1b3bbd9a3aefa279d32b203c5ef28dee21038b8b203d78518899270`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:36:23 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:36:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:36:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:36:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:37:00 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:37:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:50:52 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:53:17 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:53:18 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:06:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:22:09 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:22:10 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:22:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877256a6389e5e2563da79ad5bd201e7ee136abf14ff7cb0d4efbf3b24e5f127`  
		Last Modified: Thu, 10 Aug 2023 01:02:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a39df29b3c0b2f7e691c47273110db4a46e5c8e299f6bb95f77a9c61f79872`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8574d63bce1547e3177d0b76237a782a9b016d4880375dcd1a7b6a1c5dee3dc`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef34b3c96316bcdd92e24c8c4eebdc3a35f245c013ef87edfae0dde091a305`  
		Last Modified: Thu, 10 Aug 2023 01:02:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a481babc5b629f694446a96dba8d77c020257c98334c605aff94162b9a917279`  
		Last Modified: Thu, 10 Aug 2023 01:02:23 GMT  
		Size: 25.6 MB (25554169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281178ea1c103ff07ea7e4fb647eb0dbe4f865742da6ef9944e04f37974fc27c`  
		Last Modified: Thu, 10 Aug 2023 01:02:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5d34adf2aacfe87580143f3e17c635dc8dbd4068377b79b35d665f49bbad9`  
		Last Modified: Thu, 10 Aug 2023 01:02:16 GMT  
		Size: 275.9 KB (275946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02a2e79b5a05c2145c733eefb2add45d1ebefb7a16b93c321f5883c8ced6f1a`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd9991b8cfbc481c153abf1625143209f4c4fd40d9443a5a19f4e3613336ad2`  
		Last Modified: Thu, 10 Aug 2023 01:04:53 GMT  
		Size: 108.9 MB (108927695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dc6778f41c3c7d50b8e71668e22880153d6c6794f24c4661fc3d6aa089d0a5`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5985f015e143065716f5aabf0ecaed537103c5ec07e6c57360204a7787d02`  
		Last Modified: Thu, 10 Aug 2023 03:08:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c565e57b551adf88d5e29bd1458eb8f35437ae3145eba3114c3e38a14420307`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93046b7cb08612cc9fda41d92a61df03529a75e7d266f85a0529c5e88f7d06eb`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a40abe5aa831ec7c89060659309bccacad929792153b60f544eec13c1b6394`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8095d427fe41dd6d758aae45f422bddef28912086c3a3f7797f231535d73ca69`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.7 MB (1690912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8e6227140a7a352f358e4d9e7deab69dc502cd45903e2458244037b6bb36df`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore`

```console
$ docker pull caddy@sha256:341d22d35fd224792f17980a37766d5750ea277b08390b43e7a926c46e16b24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7-windowsservercore` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-windowsservercore` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-1809`

```console
$ docker pull caddy@sha256:663d23efed0fab8de5c0b9b2fc5e4ec761e9837c1e3bf6fdf4a66299b137bd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `caddy:2.7-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:845b1d612d896dd66d62dedbd373308f5c6df2dbb0b3e24b8bf890f2e255720d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.3`

```console
$ docker pull caddy@sha256:0da93d63c5b3af38288e909b953bd8cdcf12537c27ff219aac46c6a01775cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7.3` - linux; amd64

```console
$ docker pull caddy@sha256:f9824933254e3e43e0508670ee9bdcde704621017e95119a05317383b1878f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18631102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e9fe28a35a7bd46854ffa0afa91435071afeabac2784f8730569278d8bc9a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:09:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:20:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:20:15 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:20:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aa7b81ef11c65f43b0b58323a33dd9e07eb785529f0d75b452f87a309db00c`  
		Last Modified: Mon, 07 Aug 2023 20:09:40 GMT  
		Size: 350.8 KB (350844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b3b3e68e52dc5ab939c72a9bbac39cff4bef4b87de399ddf28657471df6845`  
		Last Modified: Mon, 14 Aug 2023 18:20:42 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e6a3c74b422682f93a437993c6365f8008e89737276364fd12ea870022f03`  
		Last Modified: Mon, 14 Aug 2023 18:20:45 GMT  
		Size: 14.9 MB (14871143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dc698bd1b82521df87ea42fbf48c98d10133ec962497ac80527b65769ceb6a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17690701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3775ac20cca67f4d547f26f5984a989b9407b0c4129fd6cd86dbb3359249acd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:38:27 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:49:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:49:14 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:49:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:49:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:49:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ef460a93549b8a3e73f6a515bccad93512788d1e8f095e7230ba41967c25a`  
		Last Modified: Wed, 09 Aug 2023 03:38:53 GMT  
		Size: 347.7 KB (347686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aae78767a581df85fd1a51ccd646619aec320896ca016ef0f05a41b16bcbfe`  
		Last Modified: Mon, 14 Aug 2023 17:49:36 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5244db1c019e66038874df2b8b92c74437f6d355802bfccada90c9d8bd8d29`  
		Last Modified: Mon, 14 Aug 2023 17:49:38 GMT  
		Size: 14.2 MB (14190701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e9cb1245e1c134e25a0ec0803e5132ba9ba92d0a4ad85db3f73bd2c3188cf70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17414619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6e2a1f4c707dc77276814a27ac22a7b5de268780603d8e08324130e1fc563`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:57:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:57:17 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:57:21 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:57:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a47b73e04459258b08555443754e92e2db20bde113c58ca18e1a6f07878f72`  
		Last Modified: Tue, 08 Aug 2023 01:52:05 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1b3e18d5e992f1805072b2d52405d575830bdce21726ef99dea99e31d8277`  
		Last Modified: Mon, 14 Aug 2023 17:57:42 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2b7485982d191f9dc0498d5b940d14df575f36ca66876b92d3ca09ff9386b2`  
		Last Modified: Mon, 14 Aug 2023 17:57:48 GMT  
		Size: 14.2 MB (14163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:db04154ce5f7a7f4d058567375880cdc6b1a3675095ad576f9886f39f1374afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731c0ae21a974e5708c4a8006250893bca5a2ecad43babf2a0a95a60fc61d6cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:09:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:39:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:39:19 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:39:22 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a699f78cfb85f60e17fc7c13495876ea0cb4495bbe39e8c65f3e8559b0d7169`  
		Last Modified: Mon, 07 Aug 2023 21:09:34 GMT  
		Size: 360.6 KB (360642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7488af8b96c79b6db13955a0302653c4e9f314d0833201984ae06c1ed697f06`  
		Last Modified: Mon, 14 Aug 2023 17:39:41 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9600da6e7e51b9083b29f3c7de592fa45e7765ca5ffe8d2abf7cc99c50578fe`  
		Last Modified: Mon, 14 Aug 2023 17:39:43 GMT  
		Size: 13.6 MB (13630728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3` - linux; ppc64le

```console
$ docker pull caddy@sha256:dfe8f314baac04dac7b7d48bdd1999aedd42d82f792d5a921be7b9a38adbcc07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17021924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09511fed803e1230efcb1c914154726b2f232029c67b0c681319b2eb6ee73a3c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:44:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:18:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:18:00 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:18:05 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:10 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:11 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:18:11 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:18:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f40714f45e39ac41e865ccbf2877db62255ce5a5c36a47eadf00b9d174f042`  
		Last Modified: Tue, 08 Aug 2023 00:45:18 GMT  
		Size: 362.2 KB (362173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d19953b5eb53ddaa0e25905527dc138e0c4111467bb7d71f81fa94976091351`  
		Last Modified: Mon, 14 Aug 2023 18:18:54 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff11295d70af9c740cf7afdb57754d70bffd7cd42271ba1a6de34195de6b249`  
		Last Modified: Mon, 14 Aug 2023 18:18:58 GMT  
		Size: 13.3 MB (13305991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3` - linux; s390x

```console
$ docker pull caddy@sha256:3b3d4b80e160105a760ad62b32c497245d69676e6053c2a7b61bc5c6fc178fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17984968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a63d05bc7601e47460ff86bc91380fd9407c0b4886b80836ac3aadb436f68e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:14:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:41:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:41:39 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:41:44 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:41:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df19abd0ca1d4a821a4174a2c0831a57d6fd584073f056abcae085a51f0b3848`  
		Last Modified: Mon, 07 Aug 2023 20:14:50 GMT  
		Size: 354.9 KB (354950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308478977890baa82477ee70a3065fb9da2080efcc95facf1a87ac021b06a8e9`  
		Last Modified: Mon, 14 Aug 2023 17:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fe1cbba37a3c1c2f6ba50e59e5c238c8d83ffca820ef709108b9e3253af757`  
		Last Modified: Mon, 14 Aug 2023 17:42:19 GMT  
		Size: 14.4 MB (14408320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.3-alpine`

```console
$ docker pull caddy@sha256:60de297131e676c0d87d7aacaa4fbd5a883abb5818977670f7024b89ebe1d7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.7.3-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:f9824933254e3e43e0508670ee9bdcde704621017e95119a05317383b1878f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18631102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e9fe28a35a7bd46854ffa0afa91435071afeabac2784f8730569278d8bc9a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:09:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:20:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:20:15 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:20:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aa7b81ef11c65f43b0b58323a33dd9e07eb785529f0d75b452f87a309db00c`  
		Last Modified: Mon, 07 Aug 2023 20:09:40 GMT  
		Size: 350.8 KB (350844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b3b3e68e52dc5ab939c72a9bbac39cff4bef4b87de399ddf28657471df6845`  
		Last Modified: Mon, 14 Aug 2023 18:20:42 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e6a3c74b422682f93a437993c6365f8008e89737276364fd12ea870022f03`  
		Last Modified: Mon, 14 Aug 2023 18:20:45 GMT  
		Size: 14.9 MB (14871143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dc698bd1b82521df87ea42fbf48c98d10133ec962497ac80527b65769ceb6a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17690701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3775ac20cca67f4d547f26f5984a989b9407b0c4129fd6cd86dbb3359249acd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:38:27 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:49:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:49:14 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:49:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:49:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:49:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ef460a93549b8a3e73f6a515bccad93512788d1e8f095e7230ba41967c25a`  
		Last Modified: Wed, 09 Aug 2023 03:38:53 GMT  
		Size: 347.7 KB (347686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aae78767a581df85fd1a51ccd646619aec320896ca016ef0f05a41b16bcbfe`  
		Last Modified: Mon, 14 Aug 2023 17:49:36 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5244db1c019e66038874df2b8b92c74437f6d355802bfccada90c9d8bd8d29`  
		Last Modified: Mon, 14 Aug 2023 17:49:38 GMT  
		Size: 14.2 MB (14190701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e9cb1245e1c134e25a0ec0803e5132ba9ba92d0a4ad85db3f73bd2c3188cf70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17414619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6e2a1f4c707dc77276814a27ac22a7b5de268780603d8e08324130e1fc563`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:57:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:57:17 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:57:21 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:57:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a47b73e04459258b08555443754e92e2db20bde113c58ca18e1a6f07878f72`  
		Last Modified: Tue, 08 Aug 2023 01:52:05 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1b3e18d5e992f1805072b2d52405d575830bdce21726ef99dea99e31d8277`  
		Last Modified: Mon, 14 Aug 2023 17:57:42 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2b7485982d191f9dc0498d5b940d14df575f36ca66876b92d3ca09ff9386b2`  
		Last Modified: Mon, 14 Aug 2023 17:57:48 GMT  
		Size: 14.2 MB (14163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:db04154ce5f7a7f4d058567375880cdc6b1a3675095ad576f9886f39f1374afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731c0ae21a974e5708c4a8006250893bca5a2ecad43babf2a0a95a60fc61d6cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:09:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:39:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:39:19 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:39:22 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a699f78cfb85f60e17fc7c13495876ea0cb4495bbe39e8c65f3e8559b0d7169`  
		Last Modified: Mon, 07 Aug 2023 21:09:34 GMT  
		Size: 360.6 KB (360642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7488af8b96c79b6db13955a0302653c4e9f314d0833201984ae06c1ed697f06`  
		Last Modified: Mon, 14 Aug 2023 17:39:41 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9600da6e7e51b9083b29f3c7de592fa45e7765ca5ffe8d2abf7cc99c50578fe`  
		Last Modified: Mon, 14 Aug 2023 17:39:43 GMT  
		Size: 13.6 MB (13630728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:dfe8f314baac04dac7b7d48bdd1999aedd42d82f792d5a921be7b9a38adbcc07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17021924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09511fed803e1230efcb1c914154726b2f232029c67b0c681319b2eb6ee73a3c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:44:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:18:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:18:00 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:18:05 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:10 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:11 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:18:11 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:18:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f40714f45e39ac41e865ccbf2877db62255ce5a5c36a47eadf00b9d174f042`  
		Last Modified: Tue, 08 Aug 2023 00:45:18 GMT  
		Size: 362.2 KB (362173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d19953b5eb53ddaa0e25905527dc138e0c4111467bb7d71f81fa94976091351`  
		Last Modified: Mon, 14 Aug 2023 18:18:54 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff11295d70af9c740cf7afdb57754d70bffd7cd42271ba1a6de34195de6b249`  
		Last Modified: Mon, 14 Aug 2023 18:18:58 GMT  
		Size: 13.3 MB (13305991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:3b3d4b80e160105a760ad62b32c497245d69676e6053c2a7b61bc5c6fc178fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17984968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a63d05bc7601e47460ff86bc91380fd9407c0b4886b80836ac3aadb436f68e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:14:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:41:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:41:39 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:41:44 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:41:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df19abd0ca1d4a821a4174a2c0831a57d6fd584073f056abcae085a51f0b3848`  
		Last Modified: Mon, 07 Aug 2023 20:14:50 GMT  
		Size: 354.9 KB (354950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308478977890baa82477ee70a3065fb9da2080efcc95facf1a87ac021b06a8e9`  
		Last Modified: Mon, 14 Aug 2023 17:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fe1cbba37a3c1c2f6ba50e59e5c238c8d83ffca820ef709108b9e3253af757`  
		Last Modified: Mon, 14 Aug 2023 17:42:19 GMT  
		Size: 14.4 MB (14408320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.3-builder`

```console
$ docker pull caddy@sha256:72235016961770347eb1ca2771c13e5e406c0091e3584d0bc7dd6ffbd481abd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7.3-builder` - linux; amd64

```console
$ docker pull caddy@sha256:7a4a3476f0991b84458cf29307f0c064e6b5fdd6af0019dc36a76576dc0721f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110902575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e1c25fbce7e1bbf91803ddf419d9de799552698d44cac3fe01a21c05cd3f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:36:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 09 Aug 2023 04:41:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:41:57 GMT
ENV GOLANG_VERSION=1.20.7
# Wed, 09 Aug 2023 04:43:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 09 Aug 2023 04:43:29 GMT
ENV GOPATH=/go
# Wed, 09 Aug 2023 04:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:43:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 09 Aug 2023 04:43:30 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:26:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:21 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:20:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:20:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:20:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d48a809fc2256f8aa0aeee47998488d64409855adba00a7cb3007ab9f3286e`  
		Last Modified: Wed, 09 Aug 2023 03:37:02 GMT  
		Size: 284.7 KB (284693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e790db5857269a95a948a96f0e3304c851351e588262d58504700b2e73fb7fe`  
		Last Modified: Wed, 09 Aug 2023 04:47:32 GMT  
		Size: 101.0 MB (100954810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f4e1a48a681e22437b6c14b04a4e287386f50f1be21ef490a1e28fd276a91`  
		Last Modified: Wed, 09 Aug 2023 04:47:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a272b880a0f8927853947bb9b16e005e2824b1685a89cc015f4e4694c441ed0e`  
		Last Modified: Wed, 09 Aug 2023 10:26:35 GMT  
		Size: 5.0 MB (4958652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636df467d23fd7ec3f363a1403da4b23c878bb239a4a4b9fdbf55f0189f9cbb1`  
		Last Modified: Mon, 14 Aug 2023 18:20:59 GMT  
		Size: 1.3 MB (1302244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afb5bd80935e22cbe3f7bb67cae35b420386beb37b9390eeab25fcef89b65d7`  
		Last Modified: Mon, 14 Aug 2023 18:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:289b1f78db36a7524bbae6562b80b29fe5585984effd44a3e22146fcbf4ab824
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108301221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac734398939dbe1f4c664f493d34b5353c438189c6b58b3e6e4d92186a8f80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:12:05 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:12:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:40 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:14:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:14:36 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:14:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:14:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:14:37 GMT
WORKDIR /go
# Wed, 09 Aug 2023 03:38:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:49:20 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:49:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:49:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8564ce36feee688566265012773f1c8c7c046ceefe86ca763eb702682f4e6e75`  
		Last Modified: Tue, 08 Aug 2023 23:15:06 GMT  
		Size: 284.9 KB (284876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b139603b026cc15bf570c9cf012fc165cb74821883c7c7c534fe6ed189b5a2`  
		Last Modified: Tue, 08 Aug 2023 23:16:29 GMT  
		Size: 98.7 MB (98671161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b2f37c2778ffd2e158ad31438d6802c214dfa5d79e06dc9af2d8320828e148`  
		Last Modified: Tue, 08 Aug 2023 23:16:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22c305527b162efa854ac3e1963e59e7fb8f2c71838222c56462b9809481ed`  
		Last Modified: Wed, 09 Aug 2023 03:39:10 GMT  
		Size: 5.0 MB (4951147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5520daf22ad222fbe3c81bbd6afa0c912b3817f0f432a35a939f9870a8512af`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 1.2 MB (1248666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f8fe3942ebea0d37a8324080324eb0bca35e859273e7bac44381e31a0fa714`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:dcbac62a4e9d8d10345a7f20ac37a814b45633ed4b050a14fa20aef08590597a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107386270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee903aaec70e29acbd506823b19cc477dc7788e545d1b88316b9ec0e9c154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:39:47 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 01:39:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:40:29 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 01:42:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 01:42:12 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 01:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:42:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 01:42:13 GMT
WORKDIR /go
# Tue, 08 Aug 2023 01:51:50 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:57:24 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:57:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:57:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:57:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47bd95d78f565e902bafd0264a979eb4f6f71e22c0464011bf9db6feb0579e6`  
		Last Modified: Tue, 08 Aug 2023 01:48:34 GMT  
		Size: 284.1 KB (284073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a674106498848b269b5cb69fb938d3dc97247d02cb1aa3927b7a7469724e950`  
		Last Modified: Tue, 08 Aug 2023 01:49:43 GMT  
		Size: 98.5 MB (98454659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1902a68db0b07b05ab7d2f3e48ca8f1d22951b498f6ff9027bdc91a5e7e830`  
		Last Modified: Tue, 08 Aug 2023 01:49:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf1886c556e441f6f89cd1cb00e1b950d9d8fcad8812a988fbb59caf0b0ba5`  
		Last Modified: Tue, 08 Aug 2023 01:52:22 GMT  
		Size: 4.5 MB (4501403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28b1afe92de619aa5de35a2f610dc68af6b39c6cd300ef8426738a739366a2`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 1.2 MB (1246092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe75fd67d7668d6aeca167419514f45cb72ec61bd61a9fc32e25b5c928dba6`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ad7390f7aa878bd4d6750dab9611c7397630fc15a7f80304eea3d3f64dcfe4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105987240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79cdcd45a4a61e8fe257b7917335ede1523a72d1c2ef2eb9115783a5379f5ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:10:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:10:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:53 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:11:59 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:11:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:12:00 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:10:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:39:25 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54e960e981301b0098c80d2e61d694333b5ab480a007a3a8d0fa629662d377`  
		Last Modified: Tue, 08 Aug 2023 23:14:21 GMT  
		Size: 286.3 KB (286298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ccffba14f84f51f896ae916a3dd045a0b0d08dc27d53f7d6a9dc5687c3501`  
		Last Modified: Tue, 08 Aug 2023 23:15:23 GMT  
		Size: 96.1 MB (96117263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d452dd4d3acc29d43b0be67bcc0c121814601787c7fd45e8260687d2cc8983`  
		Last Modified: Tue, 08 Aug 2023 23:15:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d371a704ab9a071c89db966e268fe56aad2288363a849d10eb032d47cd10848b`  
		Last Modified: Wed, 09 Aug 2023 10:10:48 GMT  
		Size: 5.1 MB (5053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e38cf28101c20845f7f103114793f73691285da6ac006db5cb28c20bc8000`  
		Last Modified: Mon, 14 Aug 2023 17:39:55 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d1b8334b836b303a87ddda4bfba4af764950afa40c2c263cca11ed8b53a8c6`  
		Last Modified: Mon, 14 Aug 2023 17:39:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4434838c3cf5a9e2e8050d86c8cfc927ad8bb46c478811a034b9a51ad2e4879c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106661395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eae15fb81c48d690da2ae88d171f0c7398deaed959011a96133cdd3836caf97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:25:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 00:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:26:56 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 00:29:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 00:29:34 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 00:29:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:29:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 00:29:36 GMT
WORKDIR /go
# Tue, 08 Aug 2023 00:44:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:18:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:18:18 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:18:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:18:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:18:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:18:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966ad2cdd35689da92e7c8fd39bd37cd6080c484e6ccaf00672c154cd4f6c2a`  
		Last Modified: Tue, 08 Aug 2023 00:39:35 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7816c9df7e6881fdd62dfcc6d743edcc2c3ca9220542437a2e5fdcfa0e4548`  
		Last Modified: Tue, 08 Aug 2023 00:41:09 GMT  
		Size: 96.6 MB (96591770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d34a514a03c5af8a03dfe8c4fbfd50b2ec61591d24080f8be8bf722904f541`  
		Last Modified: Tue, 08 Aug 2023 00:40:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802af1410e20c34900a811878ca2fa2e5dc79daeb92a53b94588831011ad81fc`  
		Last Modified: Tue, 08 Aug 2023 00:45:40 GMT  
		Size: 5.2 MB (5249966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9d8614d3da52c8737c0b4449e6e9e688fc7353d31f0246eb31e74f676c1a2`  
		Last Modified: Mon, 14 Aug 2023 18:19:17 GMT  
		Size: 1.2 MB (1186181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aa14602d0d570f4ade4524880d76ae39c401058848761634a02d8513598058`  
		Last Modified: Mon, 14 Aug 2023 18:19:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder` - linux; s390x

```console
$ docker pull caddy@sha256:4c76dac9b235685647bce5e644408f9537fd2a98243936db0666252a4ec24739
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110727449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe6eea8994d5e82ec6e85ed4c441f0a89b9cb461829805dd3eeb9d892d49a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:19:41 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Aug 2023 20:19:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:21:06 GMT
ENV GOLANG_VERSION=1.20.7
# Mon, 07 Aug 2023 20:23:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Mon, 07 Aug 2023 20:23:05 GMT
ENV GOPATH=/go
# Mon, 07 Aug 2023 20:23:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:23:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Mon, 07 Aug 2023 20:23:06 GMT
WORKDIR /go
# Tue, 08 Aug 2023 05:25:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:41:51 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:41:52 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:41:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:41:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:41:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec90be18226e5c99d10161aed1a143f4134093c55b4d6979bbdbbe4b0683eb11`  
		Last Modified: Mon, 07 Aug 2023 20:30:59 GMT  
		Size: 285.1 KB (285089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c751f85e4ba6e9bbada0b11691d914b2ec2c689bb0dca6b9cbe994488d0e3e`  
		Last Modified: Mon, 07 Aug 2023 20:31:56 GMT  
		Size: 100.9 MB (100865267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d202223222826c8580d85b8d7dd6baa8ed1cad84ba5cf47dab23eaeeae7e9`  
		Last Modified: Mon, 07 Aug 2023 20:31:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359ada615d16e203e1d40a49b896060013c2952c2982ae73b141cc291305a4c`  
		Last Modified: Tue, 08 Aug 2023 05:25:47 GMT  
		Size: 5.1 MB (5099943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1039996d136f688a91d291dcf3dbb995607af1f245f1741d8ad0c5f73cec1b01`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e7bfc7e0d6b6a7f70b22841fe42427f0fb6372b17c71c8063c50d7c8e73c1`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:d2986a3c3acb890096b8f22fe47d163b679506c701409f0f96ef55f0370c6e49
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2132346458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb468ba68962f7df97763531c45fe07444d56eeed51c25ca5019d9f06b5d07b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:39:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:39:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:41:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:41:12 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:42:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:53:35 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:56:38 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:56:40 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:20:56 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:57 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594083c5c2094c95b4e52723d54c14e0d70881f4f176720c3170012275accc3b`  
		Last Modified: Thu, 10 Aug 2023 01:02:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e2c2a5b75ced3a3a50be088c4a6c2d7df926b1fe6515b2d0c021312e3642f4`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d28688050deeec928289543beadf5c75bb2a8246576cb7c066e23818016217`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e5fbc50e7e0fefb7c9e349038ecb00ed5c000bcab8c4d82b1e1000c4273c01`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544e07bd9df923e11e09c7dc042da614f2f14589eb6fa79005ebbbf2731e97d`  
		Last Modified: Thu, 10 Aug 2023 01:02:57 GMT  
		Size: 25.6 MB (25560980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a82506c4fcec2bd90ae77756e5b03788e30c89f1a3820aa0b6a7ae6ad58ae`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcfb422b104764156fc5ba099b5e3ae9fa9f760fd2db1c21acd8969b3d73de`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 220.8 KB (220796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6aa0a5a1689ed800c4ef72c1b9febf207840fd2c6abfe4bb460e2e2bfb0b0`  
		Last Modified: Thu, 10 Aug 2023 01:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d3379322a67b2413189cc2b779d22cb4093124343c8bb17fdf720b7b49fda`  
		Last Modified: Thu, 10 Aug 2023 01:05:25 GMT  
		Size: 108.9 MB (108911716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60ccf92610ddbc47a05664785c95215a123e8930afbf6e3e2cefc80e693fd2`  
		Last Modified: Thu, 10 Aug 2023 01:05:04 GMT  
		Size: 1.5 KB (1468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c7d6253e62d61e5e0d2ad331a96cff5175f6c608b2ab4657825b3e3b4b4d0`  
		Last Modified: Thu, 10 Aug 2023 03:08:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7441bd899a1ec2037a7dc63ed24148f4362550631136f0b286d1980977fbfcfa`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60695a3cfa3d46aac3798546808cbe211d637be2b7c2af5f9d90d79eb10d544a`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636dfb4139d7b40d2a0cfa8fa63fa590d61d8627017a87a8a517c9c229fdda5b`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d287a3e1b6a016ab5e21634424eddc049708da3cc46e37cc8444f8f20d9ba206`  
		Last Modified: Mon, 14 Aug 2023 18:24:03 GMT  
		Size: 1.7 MB (1679974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cfbbc308f7ee8ad386b267faba56ca74b5aff7b32f0b71f6d94c29f5febe43`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:2bf33a1b3b64f1ffe31a0ea39e974e24ae1e5d17a1d1f0d3d2c744f8f612a8a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1933831109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2a69ae1b3bbd9a3aefa279d32b203c5ef28dee21038b8b203d78518899270`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:36:23 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:36:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:36:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:36:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:37:00 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:37:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:50:52 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:53:17 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:53:18 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:06:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:22:09 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:22:10 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:22:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877256a6389e5e2563da79ad5bd201e7ee136abf14ff7cb0d4efbf3b24e5f127`  
		Last Modified: Thu, 10 Aug 2023 01:02:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a39df29b3c0b2f7e691c47273110db4a46e5c8e299f6bb95f77a9c61f79872`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8574d63bce1547e3177d0b76237a782a9b016d4880375dcd1a7b6a1c5dee3dc`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef34b3c96316bcdd92e24c8c4eebdc3a35f245c013ef87edfae0dde091a305`  
		Last Modified: Thu, 10 Aug 2023 01:02:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a481babc5b629f694446a96dba8d77c020257c98334c605aff94162b9a917279`  
		Last Modified: Thu, 10 Aug 2023 01:02:23 GMT  
		Size: 25.6 MB (25554169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281178ea1c103ff07ea7e4fb647eb0dbe4f865742da6ef9944e04f37974fc27c`  
		Last Modified: Thu, 10 Aug 2023 01:02:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5d34adf2aacfe87580143f3e17c635dc8dbd4068377b79b35d665f49bbad9`  
		Last Modified: Thu, 10 Aug 2023 01:02:16 GMT  
		Size: 275.9 KB (275946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02a2e79b5a05c2145c733eefb2add45d1ebefb7a16b93c321f5883c8ced6f1a`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd9991b8cfbc481c153abf1625143209f4c4fd40d9443a5a19f4e3613336ad2`  
		Last Modified: Thu, 10 Aug 2023 01:04:53 GMT  
		Size: 108.9 MB (108927695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dc6778f41c3c7d50b8e71668e22880153d6c6794f24c4661fc3d6aa089d0a5`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5985f015e143065716f5aabf0ecaed537103c5ec07e6c57360204a7787d02`  
		Last Modified: Thu, 10 Aug 2023 03:08:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c565e57b551adf88d5e29bd1458eb8f35437ae3145eba3114c3e38a14420307`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93046b7cb08612cc9fda41d92a61df03529a75e7d266f85a0529c5e88f7d06eb`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a40abe5aa831ec7c89060659309bccacad929792153b60f544eec13c1b6394`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8095d427fe41dd6d758aae45f422bddef28912086c3a3f7797f231535d73ca69`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.7 MB (1690912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8e6227140a7a352f358e4d9e7deab69dc502cd45903e2458244037b6bb36df`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.3-builder-alpine`

```console
$ docker pull caddy@sha256:d8bcb1d79bd1a9970df74b9b92ced472e5ee3d2f17f16bdb9383d6f8e00bacc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.7.3-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:7a4a3476f0991b84458cf29307f0c064e6b5fdd6af0019dc36a76576dc0721f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110902575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e1c25fbce7e1bbf91803ddf419d9de799552698d44cac3fe01a21c05cd3f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:36:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 09 Aug 2023 04:41:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:41:57 GMT
ENV GOLANG_VERSION=1.20.7
# Wed, 09 Aug 2023 04:43:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 09 Aug 2023 04:43:29 GMT
ENV GOPATH=/go
# Wed, 09 Aug 2023 04:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:43:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 09 Aug 2023 04:43:30 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:26:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:21 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:20:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:20:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:20:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d48a809fc2256f8aa0aeee47998488d64409855adba00a7cb3007ab9f3286e`  
		Last Modified: Wed, 09 Aug 2023 03:37:02 GMT  
		Size: 284.7 KB (284693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e790db5857269a95a948a96f0e3304c851351e588262d58504700b2e73fb7fe`  
		Last Modified: Wed, 09 Aug 2023 04:47:32 GMT  
		Size: 101.0 MB (100954810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f4e1a48a681e22437b6c14b04a4e287386f50f1be21ef490a1e28fd276a91`  
		Last Modified: Wed, 09 Aug 2023 04:47:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a272b880a0f8927853947bb9b16e005e2824b1685a89cc015f4e4694c441ed0e`  
		Last Modified: Wed, 09 Aug 2023 10:26:35 GMT  
		Size: 5.0 MB (4958652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636df467d23fd7ec3f363a1403da4b23c878bb239a4a4b9fdbf55f0189f9cbb1`  
		Last Modified: Mon, 14 Aug 2023 18:20:59 GMT  
		Size: 1.3 MB (1302244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afb5bd80935e22cbe3f7bb67cae35b420386beb37b9390eeab25fcef89b65d7`  
		Last Modified: Mon, 14 Aug 2023 18:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:289b1f78db36a7524bbae6562b80b29fe5585984effd44a3e22146fcbf4ab824
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108301221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac734398939dbe1f4c664f493d34b5353c438189c6b58b3e6e4d92186a8f80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:12:05 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:12:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:40 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:14:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:14:36 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:14:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:14:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:14:37 GMT
WORKDIR /go
# Wed, 09 Aug 2023 03:38:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:49:20 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:49:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:49:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8564ce36feee688566265012773f1c8c7c046ceefe86ca763eb702682f4e6e75`  
		Last Modified: Tue, 08 Aug 2023 23:15:06 GMT  
		Size: 284.9 KB (284876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b139603b026cc15bf570c9cf012fc165cb74821883c7c7c534fe6ed189b5a2`  
		Last Modified: Tue, 08 Aug 2023 23:16:29 GMT  
		Size: 98.7 MB (98671161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b2f37c2778ffd2e158ad31438d6802c214dfa5d79e06dc9af2d8320828e148`  
		Last Modified: Tue, 08 Aug 2023 23:16:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22c305527b162efa854ac3e1963e59e7fb8f2c71838222c56462b9809481ed`  
		Last Modified: Wed, 09 Aug 2023 03:39:10 GMT  
		Size: 5.0 MB (4951147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5520daf22ad222fbe3c81bbd6afa0c912b3817f0f432a35a939f9870a8512af`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 1.2 MB (1248666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f8fe3942ebea0d37a8324080324eb0bca35e859273e7bac44381e31a0fa714`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:dcbac62a4e9d8d10345a7f20ac37a814b45633ed4b050a14fa20aef08590597a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107386270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee903aaec70e29acbd506823b19cc477dc7788e545d1b88316b9ec0e9c154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:39:47 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 01:39:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:40:29 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 01:42:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 01:42:12 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 01:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:42:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 01:42:13 GMT
WORKDIR /go
# Tue, 08 Aug 2023 01:51:50 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:57:24 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:57:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:57:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:57:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47bd95d78f565e902bafd0264a979eb4f6f71e22c0464011bf9db6feb0579e6`  
		Last Modified: Tue, 08 Aug 2023 01:48:34 GMT  
		Size: 284.1 KB (284073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a674106498848b269b5cb69fb938d3dc97247d02cb1aa3927b7a7469724e950`  
		Last Modified: Tue, 08 Aug 2023 01:49:43 GMT  
		Size: 98.5 MB (98454659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1902a68db0b07b05ab7d2f3e48ca8f1d22951b498f6ff9027bdc91a5e7e830`  
		Last Modified: Tue, 08 Aug 2023 01:49:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf1886c556e441f6f89cd1cb00e1b950d9d8fcad8812a988fbb59caf0b0ba5`  
		Last Modified: Tue, 08 Aug 2023 01:52:22 GMT  
		Size: 4.5 MB (4501403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28b1afe92de619aa5de35a2f610dc68af6b39c6cd300ef8426738a739366a2`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 1.2 MB (1246092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe75fd67d7668d6aeca167419514f45cb72ec61bd61a9fc32e25b5c928dba6`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ad7390f7aa878bd4d6750dab9611c7397630fc15a7f80304eea3d3f64dcfe4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105987240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79cdcd45a4a61e8fe257b7917335ede1523a72d1c2ef2eb9115783a5379f5ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:10:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:10:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:53 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:11:59 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:11:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:12:00 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:10:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:39:25 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54e960e981301b0098c80d2e61d694333b5ab480a007a3a8d0fa629662d377`  
		Last Modified: Tue, 08 Aug 2023 23:14:21 GMT  
		Size: 286.3 KB (286298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ccffba14f84f51f896ae916a3dd045a0b0d08dc27d53f7d6a9dc5687c3501`  
		Last Modified: Tue, 08 Aug 2023 23:15:23 GMT  
		Size: 96.1 MB (96117263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d452dd4d3acc29d43b0be67bcc0c121814601787c7fd45e8260687d2cc8983`  
		Last Modified: Tue, 08 Aug 2023 23:15:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d371a704ab9a071c89db966e268fe56aad2288363a849d10eb032d47cd10848b`  
		Last Modified: Wed, 09 Aug 2023 10:10:48 GMT  
		Size: 5.1 MB (5053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e38cf28101c20845f7f103114793f73691285da6ac006db5cb28c20bc8000`  
		Last Modified: Mon, 14 Aug 2023 17:39:55 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d1b8334b836b303a87ddda4bfba4af764950afa40c2c263cca11ed8b53a8c6`  
		Last Modified: Mon, 14 Aug 2023 17:39:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4434838c3cf5a9e2e8050d86c8cfc927ad8bb46c478811a034b9a51ad2e4879c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106661395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eae15fb81c48d690da2ae88d171f0c7398deaed959011a96133cdd3836caf97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:25:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 00:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:26:56 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 00:29:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 00:29:34 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 00:29:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:29:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 00:29:36 GMT
WORKDIR /go
# Tue, 08 Aug 2023 00:44:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:18:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:18:18 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:18:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:18:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:18:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:18:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966ad2cdd35689da92e7c8fd39bd37cd6080c484e6ccaf00672c154cd4f6c2a`  
		Last Modified: Tue, 08 Aug 2023 00:39:35 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7816c9df7e6881fdd62dfcc6d743edcc2c3ca9220542437a2e5fdcfa0e4548`  
		Last Modified: Tue, 08 Aug 2023 00:41:09 GMT  
		Size: 96.6 MB (96591770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d34a514a03c5af8a03dfe8c4fbfd50b2ec61591d24080f8be8bf722904f541`  
		Last Modified: Tue, 08 Aug 2023 00:40:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802af1410e20c34900a811878ca2fa2e5dc79daeb92a53b94588831011ad81fc`  
		Last Modified: Tue, 08 Aug 2023 00:45:40 GMT  
		Size: 5.2 MB (5249966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9d8614d3da52c8737c0b4449e6e9e688fc7353d31f0246eb31e74f676c1a2`  
		Last Modified: Mon, 14 Aug 2023 18:19:17 GMT  
		Size: 1.2 MB (1186181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aa14602d0d570f4ade4524880d76ae39c401058848761634a02d8513598058`  
		Last Modified: Mon, 14 Aug 2023 18:19:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4c76dac9b235685647bce5e644408f9537fd2a98243936db0666252a4ec24739
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110727449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe6eea8994d5e82ec6e85ed4c441f0a89b9cb461829805dd3eeb9d892d49a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:19:41 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Aug 2023 20:19:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:21:06 GMT
ENV GOLANG_VERSION=1.20.7
# Mon, 07 Aug 2023 20:23:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Mon, 07 Aug 2023 20:23:05 GMT
ENV GOPATH=/go
# Mon, 07 Aug 2023 20:23:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:23:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Mon, 07 Aug 2023 20:23:06 GMT
WORKDIR /go
# Tue, 08 Aug 2023 05:25:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:41:51 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:41:52 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:41:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:41:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:41:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec90be18226e5c99d10161aed1a143f4134093c55b4d6979bbdbbe4b0683eb11`  
		Last Modified: Mon, 07 Aug 2023 20:30:59 GMT  
		Size: 285.1 KB (285089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c751f85e4ba6e9bbada0b11691d914b2ec2c689bb0dca6b9cbe994488d0e3e`  
		Last Modified: Mon, 07 Aug 2023 20:31:56 GMT  
		Size: 100.9 MB (100865267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d202223222826c8580d85b8d7dd6baa8ed1cad84ba5cf47dab23eaeeae7e9`  
		Last Modified: Mon, 07 Aug 2023 20:31:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359ada615d16e203e1d40a49b896060013c2952c2982ae73b141cc291305a4c`  
		Last Modified: Tue, 08 Aug 2023 05:25:47 GMT  
		Size: 5.1 MB (5099943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1039996d136f688a91d291dcf3dbb995607af1f245f1741d8ad0c5f73cec1b01`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e7bfc7e0d6b6a7f70b22841fe42427f0fb6372b17c71c8063c50d7c8e73c1`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.3-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ca7c5b253f237a6f0d30748de0cb616efd5040889648b19dbf2d86855990a759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `caddy:2.7.3-builder-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:d2986a3c3acb890096b8f22fe47d163b679506c701409f0f96ef55f0370c6e49
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2132346458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb468ba68962f7df97763531c45fe07444d56eeed51c25ca5019d9f06b5d07b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:39:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:39:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:41:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:41:12 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:42:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:53:35 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:56:38 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:56:40 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:20:56 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:57 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594083c5c2094c95b4e52723d54c14e0d70881f4f176720c3170012275accc3b`  
		Last Modified: Thu, 10 Aug 2023 01:02:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e2c2a5b75ced3a3a50be088c4a6c2d7df926b1fe6515b2d0c021312e3642f4`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d28688050deeec928289543beadf5c75bb2a8246576cb7c066e23818016217`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e5fbc50e7e0fefb7c9e349038ecb00ed5c000bcab8c4d82b1e1000c4273c01`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544e07bd9df923e11e09c7dc042da614f2f14589eb6fa79005ebbbf2731e97d`  
		Last Modified: Thu, 10 Aug 2023 01:02:57 GMT  
		Size: 25.6 MB (25560980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a82506c4fcec2bd90ae77756e5b03788e30c89f1a3820aa0b6a7ae6ad58ae`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcfb422b104764156fc5ba099b5e3ae9fa9f760fd2db1c21acd8969b3d73de`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 220.8 KB (220796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6aa0a5a1689ed800c4ef72c1b9febf207840fd2c6abfe4bb460e2e2bfb0b0`  
		Last Modified: Thu, 10 Aug 2023 01:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d3379322a67b2413189cc2b779d22cb4093124343c8bb17fdf720b7b49fda`  
		Last Modified: Thu, 10 Aug 2023 01:05:25 GMT  
		Size: 108.9 MB (108911716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60ccf92610ddbc47a05664785c95215a123e8930afbf6e3e2cefc80e693fd2`  
		Last Modified: Thu, 10 Aug 2023 01:05:04 GMT  
		Size: 1.5 KB (1468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c7d6253e62d61e5e0d2ad331a96cff5175f6c608b2ab4657825b3e3b4b4d0`  
		Last Modified: Thu, 10 Aug 2023 03:08:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7441bd899a1ec2037a7dc63ed24148f4362550631136f0b286d1980977fbfcfa`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60695a3cfa3d46aac3798546808cbe211d637be2b7c2af5f9d90d79eb10d544a`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636dfb4139d7b40d2a0cfa8fa63fa590d61d8627017a87a8a517c9c229fdda5b`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d287a3e1b6a016ab5e21634424eddc049708da3cc46e37cc8444f8f20d9ba206`  
		Last Modified: Mon, 14 Aug 2023 18:24:03 GMT  
		Size: 1.7 MB (1679974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cfbbc308f7ee8ad386b267faba56ca74b5aff7b32f0b71f6d94c29f5febe43`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.3-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:24c81ff6d1a33b0f08066917fb05c2a4c782bb2cd6bd1ba0217709e1e10be849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7.3-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:2bf33a1b3b64f1ffe31a0ea39e974e24ae1e5d17a1d1f0d3d2c744f8f612a8a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1933831109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2a69ae1b3bbd9a3aefa279d32b203c5ef28dee21038b8b203d78518899270`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:36:23 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:36:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:36:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:36:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:37:00 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:37:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:50:52 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:53:17 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:53:18 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:06:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:22:09 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:22:10 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:22:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877256a6389e5e2563da79ad5bd201e7ee136abf14ff7cb0d4efbf3b24e5f127`  
		Last Modified: Thu, 10 Aug 2023 01:02:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a39df29b3c0b2f7e691c47273110db4a46e5c8e299f6bb95f77a9c61f79872`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8574d63bce1547e3177d0b76237a782a9b016d4880375dcd1a7b6a1c5dee3dc`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef34b3c96316bcdd92e24c8c4eebdc3a35f245c013ef87edfae0dde091a305`  
		Last Modified: Thu, 10 Aug 2023 01:02:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a481babc5b629f694446a96dba8d77c020257c98334c605aff94162b9a917279`  
		Last Modified: Thu, 10 Aug 2023 01:02:23 GMT  
		Size: 25.6 MB (25554169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281178ea1c103ff07ea7e4fb647eb0dbe4f865742da6ef9944e04f37974fc27c`  
		Last Modified: Thu, 10 Aug 2023 01:02:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5d34adf2aacfe87580143f3e17c635dc8dbd4068377b79b35d665f49bbad9`  
		Last Modified: Thu, 10 Aug 2023 01:02:16 GMT  
		Size: 275.9 KB (275946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02a2e79b5a05c2145c733eefb2add45d1ebefb7a16b93c321f5883c8ced6f1a`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd9991b8cfbc481c153abf1625143209f4c4fd40d9443a5a19f4e3613336ad2`  
		Last Modified: Thu, 10 Aug 2023 01:04:53 GMT  
		Size: 108.9 MB (108927695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dc6778f41c3c7d50b8e71668e22880153d6c6794f24c4661fc3d6aa089d0a5`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5985f015e143065716f5aabf0ecaed537103c5ec07e6c57360204a7787d02`  
		Last Modified: Thu, 10 Aug 2023 03:08:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c565e57b551adf88d5e29bd1458eb8f35437ae3145eba3114c3e38a14420307`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93046b7cb08612cc9fda41d92a61df03529a75e7d266f85a0529c5e88f7d06eb`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a40abe5aa831ec7c89060659309bccacad929792153b60f544eec13c1b6394`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8095d427fe41dd6d758aae45f422bddef28912086c3a3f7797f231535d73ca69`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.7 MB (1690912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8e6227140a7a352f358e4d9e7deab69dc502cd45903e2458244037b6bb36df`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.3-windowsservercore`

```console
$ docker pull caddy@sha256:341d22d35fd224792f17980a37766d5750ea277b08390b43e7a926c46e16b24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7.3-windowsservercore` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.3-windowsservercore` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.3-windowsservercore-1809`

```console
$ docker pull caddy@sha256:663d23efed0fab8de5c0b9b2fc5e4ec761e9837c1e3bf6fdf4a66299b137bd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `caddy:2.7.3-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.3-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:845b1d612d896dd66d62dedbd373308f5c6df2dbb0b3e24b8bf890f2e255720d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `caddy:2.7.3-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:60de297131e676c0d87d7aacaa4fbd5a883abb5818977670f7024b89ebe1d7bb
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
$ docker pull caddy@sha256:f9824933254e3e43e0508670ee9bdcde704621017e95119a05317383b1878f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18631102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e9fe28a35a7bd46854ffa0afa91435071afeabac2784f8730569278d8bc9a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:09:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:20:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:20:15 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:20:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aa7b81ef11c65f43b0b58323a33dd9e07eb785529f0d75b452f87a309db00c`  
		Last Modified: Mon, 07 Aug 2023 20:09:40 GMT  
		Size: 350.8 KB (350844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b3b3e68e52dc5ab939c72a9bbac39cff4bef4b87de399ddf28657471df6845`  
		Last Modified: Mon, 14 Aug 2023 18:20:42 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e6a3c74b422682f93a437993c6365f8008e89737276364fd12ea870022f03`  
		Last Modified: Mon, 14 Aug 2023 18:20:45 GMT  
		Size: 14.9 MB (14871143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dc698bd1b82521df87ea42fbf48c98d10133ec962497ac80527b65769ceb6a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17690701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3775ac20cca67f4d547f26f5984a989b9407b0c4129fd6cd86dbb3359249acd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:38:27 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:49:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:49:14 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:49:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:49:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:49:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ef460a93549b8a3e73f6a515bccad93512788d1e8f095e7230ba41967c25a`  
		Last Modified: Wed, 09 Aug 2023 03:38:53 GMT  
		Size: 347.7 KB (347686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aae78767a581df85fd1a51ccd646619aec320896ca016ef0f05a41b16bcbfe`  
		Last Modified: Mon, 14 Aug 2023 17:49:36 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5244db1c019e66038874df2b8b92c74437f6d355802bfccada90c9d8bd8d29`  
		Last Modified: Mon, 14 Aug 2023 17:49:38 GMT  
		Size: 14.2 MB (14190701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e9cb1245e1c134e25a0ec0803e5132ba9ba92d0a4ad85db3f73bd2c3188cf70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17414619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6e2a1f4c707dc77276814a27ac22a7b5de268780603d8e08324130e1fc563`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:57:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:57:17 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:57:21 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:57:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a47b73e04459258b08555443754e92e2db20bde113c58ca18e1a6f07878f72`  
		Last Modified: Tue, 08 Aug 2023 01:52:05 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1b3e18d5e992f1805072b2d52405d575830bdce21726ef99dea99e31d8277`  
		Last Modified: Mon, 14 Aug 2023 17:57:42 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2b7485982d191f9dc0498d5b940d14df575f36ca66876b92d3ca09ff9386b2`  
		Last Modified: Mon, 14 Aug 2023 17:57:48 GMT  
		Size: 14.2 MB (14163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:db04154ce5f7a7f4d058567375880cdc6b1a3675095ad576f9886f39f1374afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731c0ae21a974e5708c4a8006250893bca5a2ecad43babf2a0a95a60fc61d6cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:09:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:39:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:39:19 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:39:22 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a699f78cfb85f60e17fc7c13495876ea0cb4495bbe39e8c65f3e8559b0d7169`  
		Last Modified: Mon, 07 Aug 2023 21:09:34 GMT  
		Size: 360.6 KB (360642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7488af8b96c79b6db13955a0302653c4e9f314d0833201984ae06c1ed697f06`  
		Last Modified: Mon, 14 Aug 2023 17:39:41 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9600da6e7e51b9083b29f3c7de592fa45e7765ca5ffe8d2abf7cc99c50578fe`  
		Last Modified: Mon, 14 Aug 2023 17:39:43 GMT  
		Size: 13.6 MB (13630728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:dfe8f314baac04dac7b7d48bdd1999aedd42d82f792d5a921be7b9a38adbcc07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17021924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09511fed803e1230efcb1c914154726b2f232029c67b0c681319b2eb6ee73a3c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:44:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:18:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:18:00 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:18:05 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:10 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:11 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:18:11 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:18:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f40714f45e39ac41e865ccbf2877db62255ce5a5c36a47eadf00b9d174f042`  
		Last Modified: Tue, 08 Aug 2023 00:45:18 GMT  
		Size: 362.2 KB (362173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d19953b5eb53ddaa0e25905527dc138e0c4111467bb7d71f81fa94976091351`  
		Last Modified: Mon, 14 Aug 2023 18:18:54 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff11295d70af9c740cf7afdb57754d70bffd7cd42271ba1a6de34195de6b249`  
		Last Modified: Mon, 14 Aug 2023 18:18:58 GMT  
		Size: 13.3 MB (13305991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:3b3d4b80e160105a760ad62b32c497245d69676e6053c2a7b61bc5c6fc178fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17984968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a63d05bc7601e47460ff86bc91380fd9407c0b4886b80836ac3aadb436f68e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:14:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:41:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:41:39 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:41:44 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:41:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df19abd0ca1d4a821a4174a2c0831a57d6fd584073f056abcae085a51f0b3848`  
		Last Modified: Mon, 07 Aug 2023 20:14:50 GMT  
		Size: 354.9 KB (354950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308478977890baa82477ee70a3065fb9da2080efcc95facf1a87ac021b06a8e9`  
		Last Modified: Mon, 14 Aug 2023 17:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fe1cbba37a3c1c2f6ba50e59e5c238c8d83ffca820ef709108b9e3253af757`  
		Last Modified: Mon, 14 Aug 2023 17:42:19 GMT  
		Size: 14.4 MB (14408320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:72235016961770347eb1ca2771c13e5e406c0091e3584d0bc7dd6ffbd481abd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:7a4a3476f0991b84458cf29307f0c064e6b5fdd6af0019dc36a76576dc0721f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110902575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e1c25fbce7e1bbf91803ddf419d9de799552698d44cac3fe01a21c05cd3f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:36:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 09 Aug 2023 04:41:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:41:57 GMT
ENV GOLANG_VERSION=1.20.7
# Wed, 09 Aug 2023 04:43:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 09 Aug 2023 04:43:29 GMT
ENV GOPATH=/go
# Wed, 09 Aug 2023 04:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:43:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 09 Aug 2023 04:43:30 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:26:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:21 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:20:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:20:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:20:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d48a809fc2256f8aa0aeee47998488d64409855adba00a7cb3007ab9f3286e`  
		Last Modified: Wed, 09 Aug 2023 03:37:02 GMT  
		Size: 284.7 KB (284693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e790db5857269a95a948a96f0e3304c851351e588262d58504700b2e73fb7fe`  
		Last Modified: Wed, 09 Aug 2023 04:47:32 GMT  
		Size: 101.0 MB (100954810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f4e1a48a681e22437b6c14b04a4e287386f50f1be21ef490a1e28fd276a91`  
		Last Modified: Wed, 09 Aug 2023 04:47:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a272b880a0f8927853947bb9b16e005e2824b1685a89cc015f4e4694c441ed0e`  
		Last Modified: Wed, 09 Aug 2023 10:26:35 GMT  
		Size: 5.0 MB (4958652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636df467d23fd7ec3f363a1403da4b23c878bb239a4a4b9fdbf55f0189f9cbb1`  
		Last Modified: Mon, 14 Aug 2023 18:20:59 GMT  
		Size: 1.3 MB (1302244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afb5bd80935e22cbe3f7bb67cae35b420386beb37b9390eeab25fcef89b65d7`  
		Last Modified: Mon, 14 Aug 2023 18:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:289b1f78db36a7524bbae6562b80b29fe5585984effd44a3e22146fcbf4ab824
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108301221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac734398939dbe1f4c664f493d34b5353c438189c6b58b3e6e4d92186a8f80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:12:05 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:12:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:40 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:14:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:14:36 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:14:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:14:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:14:37 GMT
WORKDIR /go
# Wed, 09 Aug 2023 03:38:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:49:20 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:49:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:49:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8564ce36feee688566265012773f1c8c7c046ceefe86ca763eb702682f4e6e75`  
		Last Modified: Tue, 08 Aug 2023 23:15:06 GMT  
		Size: 284.9 KB (284876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b139603b026cc15bf570c9cf012fc165cb74821883c7c7c534fe6ed189b5a2`  
		Last Modified: Tue, 08 Aug 2023 23:16:29 GMT  
		Size: 98.7 MB (98671161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b2f37c2778ffd2e158ad31438d6802c214dfa5d79e06dc9af2d8320828e148`  
		Last Modified: Tue, 08 Aug 2023 23:16:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22c305527b162efa854ac3e1963e59e7fb8f2c71838222c56462b9809481ed`  
		Last Modified: Wed, 09 Aug 2023 03:39:10 GMT  
		Size: 5.0 MB (4951147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5520daf22ad222fbe3c81bbd6afa0c912b3817f0f432a35a939f9870a8512af`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 1.2 MB (1248666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f8fe3942ebea0d37a8324080324eb0bca35e859273e7bac44381e31a0fa714`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:dcbac62a4e9d8d10345a7f20ac37a814b45633ed4b050a14fa20aef08590597a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107386270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee903aaec70e29acbd506823b19cc477dc7788e545d1b88316b9ec0e9c154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:39:47 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 01:39:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:40:29 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 01:42:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 01:42:12 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 01:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:42:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 01:42:13 GMT
WORKDIR /go
# Tue, 08 Aug 2023 01:51:50 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:57:24 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:57:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:57:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:57:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47bd95d78f565e902bafd0264a979eb4f6f71e22c0464011bf9db6feb0579e6`  
		Last Modified: Tue, 08 Aug 2023 01:48:34 GMT  
		Size: 284.1 KB (284073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a674106498848b269b5cb69fb938d3dc97247d02cb1aa3927b7a7469724e950`  
		Last Modified: Tue, 08 Aug 2023 01:49:43 GMT  
		Size: 98.5 MB (98454659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1902a68db0b07b05ab7d2f3e48ca8f1d22951b498f6ff9027bdc91a5e7e830`  
		Last Modified: Tue, 08 Aug 2023 01:49:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf1886c556e441f6f89cd1cb00e1b950d9d8fcad8812a988fbb59caf0b0ba5`  
		Last Modified: Tue, 08 Aug 2023 01:52:22 GMT  
		Size: 4.5 MB (4501403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28b1afe92de619aa5de35a2f610dc68af6b39c6cd300ef8426738a739366a2`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 1.2 MB (1246092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe75fd67d7668d6aeca167419514f45cb72ec61bd61a9fc32e25b5c928dba6`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ad7390f7aa878bd4d6750dab9611c7397630fc15a7f80304eea3d3f64dcfe4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105987240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79cdcd45a4a61e8fe257b7917335ede1523a72d1c2ef2eb9115783a5379f5ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:10:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:10:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:53 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:11:59 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:11:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:12:00 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:10:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:39:25 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54e960e981301b0098c80d2e61d694333b5ab480a007a3a8d0fa629662d377`  
		Last Modified: Tue, 08 Aug 2023 23:14:21 GMT  
		Size: 286.3 KB (286298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ccffba14f84f51f896ae916a3dd045a0b0d08dc27d53f7d6a9dc5687c3501`  
		Last Modified: Tue, 08 Aug 2023 23:15:23 GMT  
		Size: 96.1 MB (96117263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d452dd4d3acc29d43b0be67bcc0c121814601787c7fd45e8260687d2cc8983`  
		Last Modified: Tue, 08 Aug 2023 23:15:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d371a704ab9a071c89db966e268fe56aad2288363a849d10eb032d47cd10848b`  
		Last Modified: Wed, 09 Aug 2023 10:10:48 GMT  
		Size: 5.1 MB (5053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e38cf28101c20845f7f103114793f73691285da6ac006db5cb28c20bc8000`  
		Last Modified: Mon, 14 Aug 2023 17:39:55 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d1b8334b836b303a87ddda4bfba4af764950afa40c2c263cca11ed8b53a8c6`  
		Last Modified: Mon, 14 Aug 2023 17:39:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4434838c3cf5a9e2e8050d86c8cfc927ad8bb46c478811a034b9a51ad2e4879c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106661395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eae15fb81c48d690da2ae88d171f0c7398deaed959011a96133cdd3836caf97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:25:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 00:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:26:56 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 00:29:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 00:29:34 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 00:29:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:29:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 00:29:36 GMT
WORKDIR /go
# Tue, 08 Aug 2023 00:44:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:18:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:18:18 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:18:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:18:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:18:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:18:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966ad2cdd35689da92e7c8fd39bd37cd6080c484e6ccaf00672c154cd4f6c2a`  
		Last Modified: Tue, 08 Aug 2023 00:39:35 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7816c9df7e6881fdd62dfcc6d743edcc2c3ca9220542437a2e5fdcfa0e4548`  
		Last Modified: Tue, 08 Aug 2023 00:41:09 GMT  
		Size: 96.6 MB (96591770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d34a514a03c5af8a03dfe8c4fbfd50b2ec61591d24080f8be8bf722904f541`  
		Last Modified: Tue, 08 Aug 2023 00:40:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802af1410e20c34900a811878ca2fa2e5dc79daeb92a53b94588831011ad81fc`  
		Last Modified: Tue, 08 Aug 2023 00:45:40 GMT  
		Size: 5.2 MB (5249966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9d8614d3da52c8737c0b4449e6e9e688fc7353d31f0246eb31e74f676c1a2`  
		Last Modified: Mon, 14 Aug 2023 18:19:17 GMT  
		Size: 1.2 MB (1186181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aa14602d0d570f4ade4524880d76ae39c401058848761634a02d8513598058`  
		Last Modified: Mon, 14 Aug 2023 18:19:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:4c76dac9b235685647bce5e644408f9537fd2a98243936db0666252a4ec24739
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110727449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe6eea8994d5e82ec6e85ed4c441f0a89b9cb461829805dd3eeb9d892d49a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:19:41 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Aug 2023 20:19:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:21:06 GMT
ENV GOLANG_VERSION=1.20.7
# Mon, 07 Aug 2023 20:23:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Mon, 07 Aug 2023 20:23:05 GMT
ENV GOPATH=/go
# Mon, 07 Aug 2023 20:23:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:23:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Mon, 07 Aug 2023 20:23:06 GMT
WORKDIR /go
# Tue, 08 Aug 2023 05:25:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:41:51 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:41:52 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:41:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:41:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:41:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec90be18226e5c99d10161aed1a143f4134093c55b4d6979bbdbbe4b0683eb11`  
		Last Modified: Mon, 07 Aug 2023 20:30:59 GMT  
		Size: 285.1 KB (285089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c751f85e4ba6e9bbada0b11691d914b2ec2c689bb0dca6b9cbe994488d0e3e`  
		Last Modified: Mon, 07 Aug 2023 20:31:56 GMT  
		Size: 100.9 MB (100865267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d202223222826c8580d85b8d7dd6baa8ed1cad84ba5cf47dab23eaeeae7e9`  
		Last Modified: Mon, 07 Aug 2023 20:31:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359ada615d16e203e1d40a49b896060013c2952c2982ae73b141cc291305a4c`  
		Last Modified: Tue, 08 Aug 2023 05:25:47 GMT  
		Size: 5.1 MB (5099943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1039996d136f688a91d291dcf3dbb995607af1f245f1741d8ad0c5f73cec1b01`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e7bfc7e0d6b6a7f70b22841fe42427f0fb6372b17c71c8063c50d7c8e73c1`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:d2986a3c3acb890096b8f22fe47d163b679506c701409f0f96ef55f0370c6e49
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2132346458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb468ba68962f7df97763531c45fe07444d56eeed51c25ca5019d9f06b5d07b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:39:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:39:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:41:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:41:12 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:42:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:53:35 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:56:38 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:56:40 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:20:56 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:57 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594083c5c2094c95b4e52723d54c14e0d70881f4f176720c3170012275accc3b`  
		Last Modified: Thu, 10 Aug 2023 01:02:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e2c2a5b75ced3a3a50be088c4a6c2d7df926b1fe6515b2d0c021312e3642f4`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d28688050deeec928289543beadf5c75bb2a8246576cb7c066e23818016217`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e5fbc50e7e0fefb7c9e349038ecb00ed5c000bcab8c4d82b1e1000c4273c01`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544e07bd9df923e11e09c7dc042da614f2f14589eb6fa79005ebbbf2731e97d`  
		Last Modified: Thu, 10 Aug 2023 01:02:57 GMT  
		Size: 25.6 MB (25560980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a82506c4fcec2bd90ae77756e5b03788e30c89f1a3820aa0b6a7ae6ad58ae`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcfb422b104764156fc5ba099b5e3ae9fa9f760fd2db1c21acd8969b3d73de`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 220.8 KB (220796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6aa0a5a1689ed800c4ef72c1b9febf207840fd2c6abfe4bb460e2e2bfb0b0`  
		Last Modified: Thu, 10 Aug 2023 01:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d3379322a67b2413189cc2b779d22cb4093124343c8bb17fdf720b7b49fda`  
		Last Modified: Thu, 10 Aug 2023 01:05:25 GMT  
		Size: 108.9 MB (108911716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60ccf92610ddbc47a05664785c95215a123e8930afbf6e3e2cefc80e693fd2`  
		Last Modified: Thu, 10 Aug 2023 01:05:04 GMT  
		Size: 1.5 KB (1468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c7d6253e62d61e5e0d2ad331a96cff5175f6c608b2ab4657825b3e3b4b4d0`  
		Last Modified: Thu, 10 Aug 2023 03:08:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7441bd899a1ec2037a7dc63ed24148f4362550631136f0b286d1980977fbfcfa`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60695a3cfa3d46aac3798546808cbe211d637be2b7c2af5f9d90d79eb10d544a`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636dfb4139d7b40d2a0cfa8fa63fa590d61d8627017a87a8a517c9c229fdda5b`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d287a3e1b6a016ab5e21634424eddc049708da3cc46e37cc8444f8f20d9ba206`  
		Last Modified: Mon, 14 Aug 2023 18:24:03 GMT  
		Size: 1.7 MB (1679974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cfbbc308f7ee8ad386b267faba56ca74b5aff7b32f0b71f6d94c29f5febe43`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:2bf33a1b3b64f1ffe31a0ea39e974e24ae1e5d17a1d1f0d3d2c744f8f612a8a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1933831109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2a69ae1b3bbd9a3aefa279d32b203c5ef28dee21038b8b203d78518899270`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:36:23 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:36:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:36:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:36:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:37:00 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:37:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:50:52 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:53:17 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:53:18 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:06:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:22:09 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:22:10 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:22:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877256a6389e5e2563da79ad5bd201e7ee136abf14ff7cb0d4efbf3b24e5f127`  
		Last Modified: Thu, 10 Aug 2023 01:02:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a39df29b3c0b2f7e691c47273110db4a46e5c8e299f6bb95f77a9c61f79872`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8574d63bce1547e3177d0b76237a782a9b016d4880375dcd1a7b6a1c5dee3dc`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef34b3c96316bcdd92e24c8c4eebdc3a35f245c013ef87edfae0dde091a305`  
		Last Modified: Thu, 10 Aug 2023 01:02:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a481babc5b629f694446a96dba8d77c020257c98334c605aff94162b9a917279`  
		Last Modified: Thu, 10 Aug 2023 01:02:23 GMT  
		Size: 25.6 MB (25554169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281178ea1c103ff07ea7e4fb647eb0dbe4f865742da6ef9944e04f37974fc27c`  
		Last Modified: Thu, 10 Aug 2023 01:02:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5d34adf2aacfe87580143f3e17c635dc8dbd4068377b79b35d665f49bbad9`  
		Last Modified: Thu, 10 Aug 2023 01:02:16 GMT  
		Size: 275.9 KB (275946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02a2e79b5a05c2145c733eefb2add45d1ebefb7a16b93c321f5883c8ced6f1a`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd9991b8cfbc481c153abf1625143209f4c4fd40d9443a5a19f4e3613336ad2`  
		Last Modified: Thu, 10 Aug 2023 01:04:53 GMT  
		Size: 108.9 MB (108927695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dc6778f41c3c7d50b8e71668e22880153d6c6794f24c4661fc3d6aa089d0a5`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5985f015e143065716f5aabf0ecaed537103c5ec07e6c57360204a7787d02`  
		Last Modified: Thu, 10 Aug 2023 03:08:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c565e57b551adf88d5e29bd1458eb8f35437ae3145eba3114c3e38a14420307`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93046b7cb08612cc9fda41d92a61df03529a75e7d266f85a0529c5e88f7d06eb`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a40abe5aa831ec7c89060659309bccacad929792153b60f544eec13c1b6394`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8095d427fe41dd6d758aae45f422bddef28912086c3a3f7797f231535d73ca69`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.7 MB (1690912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8e6227140a7a352f358e4d9e7deab69dc502cd45903e2458244037b6bb36df`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:d8bcb1d79bd1a9970df74b9b92ced472e5ee3d2f17f16bdb9383d6f8e00bacc0
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
$ docker pull caddy@sha256:7a4a3476f0991b84458cf29307f0c064e6b5fdd6af0019dc36a76576dc0721f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110902575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487e1c25fbce7e1bbf91803ddf419d9de799552698d44cac3fe01a21c05cd3f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:36:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 09 Aug 2023 04:41:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:41:57 GMT
ENV GOLANG_VERSION=1.20.7
# Wed, 09 Aug 2023 04:43:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 09 Aug 2023 04:43:29 GMT
ENV GOPATH=/go
# Wed, 09 Aug 2023 04:43:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Aug 2023 04:43:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 09 Aug 2023 04:43:30 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:26:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:21 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:20:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:20:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:20:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:20:23 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d48a809fc2256f8aa0aeee47998488d64409855adba00a7cb3007ab9f3286e`  
		Last Modified: Wed, 09 Aug 2023 03:37:02 GMT  
		Size: 284.7 KB (284693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e790db5857269a95a948a96f0e3304c851351e588262d58504700b2e73fb7fe`  
		Last Modified: Wed, 09 Aug 2023 04:47:32 GMT  
		Size: 101.0 MB (100954810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f4e1a48a681e22437b6c14b04a4e287386f50f1be21ef490a1e28fd276a91`  
		Last Modified: Wed, 09 Aug 2023 04:47:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a272b880a0f8927853947bb9b16e005e2824b1685a89cc015f4e4694c441ed0e`  
		Last Modified: Wed, 09 Aug 2023 10:26:35 GMT  
		Size: 5.0 MB (4958652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636df467d23fd7ec3f363a1403da4b23c878bb239a4a4b9fdbf55f0189f9cbb1`  
		Last Modified: Mon, 14 Aug 2023 18:20:59 GMT  
		Size: 1.3 MB (1302244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afb5bd80935e22cbe3f7bb67cae35b420386beb37b9390eeab25fcef89b65d7`  
		Last Modified: Mon, 14 Aug 2023 18:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:289b1f78db36a7524bbae6562b80b29fe5585984effd44a3e22146fcbf4ab824
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108301221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac734398939dbe1f4c664f493d34b5353c438189c6b58b3e6e4d92186a8f80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:12:05 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:12:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:40 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:14:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:14:36 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:14:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:14:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:14:37 GMT
WORKDIR /go
# Wed, 09 Aug 2023 03:38:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:49:20 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:49:20 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:49:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:49:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:49:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8564ce36feee688566265012773f1c8c7c046ceefe86ca763eb702682f4e6e75`  
		Last Modified: Tue, 08 Aug 2023 23:15:06 GMT  
		Size: 284.9 KB (284876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b139603b026cc15bf570c9cf012fc165cb74821883c7c7c534fe6ed189b5a2`  
		Last Modified: Tue, 08 Aug 2023 23:16:29 GMT  
		Size: 98.7 MB (98671161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b2f37c2778ffd2e158ad31438d6802c214dfa5d79e06dc9af2d8320828e148`  
		Last Modified: Tue, 08 Aug 2023 23:16:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22c305527b162efa854ac3e1963e59e7fb8f2c71838222c56462b9809481ed`  
		Last Modified: Wed, 09 Aug 2023 03:39:10 GMT  
		Size: 5.0 MB (4951147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5520daf22ad222fbe3c81bbd6afa0c912b3817f0f432a35a939f9870a8512af`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 1.2 MB (1248666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f8fe3942ebea0d37a8324080324eb0bca35e859273e7bac44381e31a0fa714`  
		Last Modified: Mon, 14 Aug 2023 17:49:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:dcbac62a4e9d8d10345a7f20ac37a814b45633ed4b050a14fa20aef08590597a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107386270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adee903aaec70e29acbd506823b19cc477dc7788e545d1b88316b9ec0e9c154`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:39:47 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 01:39:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:40:29 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 01:42:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 01:42:12 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 01:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 01:42:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 01:42:13 GMT
WORKDIR /go
# Tue, 08 Aug 2023 01:51:50 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:57:24 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:57:24 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:57:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:57:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:57:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47bd95d78f565e902bafd0264a979eb4f6f71e22c0464011bf9db6feb0579e6`  
		Last Modified: Tue, 08 Aug 2023 01:48:34 GMT  
		Size: 284.1 KB (284073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a674106498848b269b5cb69fb938d3dc97247d02cb1aa3927b7a7469724e950`  
		Last Modified: Tue, 08 Aug 2023 01:49:43 GMT  
		Size: 98.5 MB (98454659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1902a68db0b07b05ab7d2f3e48ca8f1d22951b498f6ff9027bdc91a5e7e830`  
		Last Modified: Tue, 08 Aug 2023 01:49:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf1886c556e441f6f89cd1cb00e1b950d9d8fcad8812a988fbb59caf0b0ba5`  
		Last Modified: Tue, 08 Aug 2023 01:52:22 GMT  
		Size: 4.5 MB (4501403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28b1afe92de619aa5de35a2f610dc68af6b39c6cd300ef8426738a739366a2`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 1.2 MB (1246092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe75fd67d7668d6aeca167419514f45cb72ec61bd61a9fc32e25b5c928dba6`  
		Last Modified: Mon, 14 Aug 2023 17:58:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ad7390f7aa878bd4d6750dab9611c7397630fc15a7f80304eea3d3f64dcfe4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105987240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79cdcd45a4a61e8fe257b7917335ede1523a72d1c2ef2eb9115783a5379f5ea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:10:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 23:10:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:10:53 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 23:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 23:11:59 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 23:11:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 23:12:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 23:12:00 GMT
WORKDIR /go
# Wed, 09 Aug 2023 10:10:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:39:25 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:39:25 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:39:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:39:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:39:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54e960e981301b0098c80d2e61d694333b5ab480a007a3a8d0fa629662d377`  
		Last Modified: Tue, 08 Aug 2023 23:14:21 GMT  
		Size: 286.3 KB (286298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ccffba14f84f51f896ae916a3dd045a0b0d08dc27d53f7d6a9dc5687c3501`  
		Last Modified: Tue, 08 Aug 2023 23:15:23 GMT  
		Size: 96.1 MB (96117263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d452dd4d3acc29d43b0be67bcc0c121814601787c7fd45e8260687d2cc8983`  
		Last Modified: Tue, 08 Aug 2023 23:15:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d371a704ab9a071c89db966e268fe56aad2288363a849d10eb032d47cd10848b`  
		Last Modified: Wed, 09 Aug 2023 10:10:48 GMT  
		Size: 5.1 MB (5053901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e38cf28101c20845f7f103114793f73691285da6ac006db5cb28c20bc8000`  
		Last Modified: Mon, 14 Aug 2023 17:39:55 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d1b8334b836b303a87ddda4bfba4af764950afa40c2c263cca11ed8b53a8c6`  
		Last Modified: Mon, 14 Aug 2023 17:39:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4434838c3cf5a9e2e8050d86c8cfc927ad8bb46c478811a034b9a51ad2e4879c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106661395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eae15fb81c48d690da2ae88d171f0c7398deaed959011a96133cdd3836caf97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:25:24 GMT
RUN apk add --no-cache ca-certificates
# Tue, 08 Aug 2023 00:25:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:26:56 GMT
ENV GOLANG_VERSION=1.20.7
# Tue, 08 Aug 2023 00:29:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 08 Aug 2023 00:29:34 GMT
ENV GOPATH=/go
# Tue, 08 Aug 2023 00:29:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 00:29:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 08 Aug 2023 00:29:36 GMT
WORKDIR /go
# Tue, 08 Aug 2023 00:44:40 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 18:18:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:18:18 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:18:21 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 18:18:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 18:18:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 18:18:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966ad2cdd35689da92e7c8fd39bd37cd6080c484e6ccaf00672c154cd4f6c2a`  
		Last Modified: Tue, 08 Aug 2023 00:39:35 GMT  
		Size: 286.7 KB (286662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7816c9df7e6881fdd62dfcc6d743edcc2c3ca9220542437a2e5fdcfa0e4548`  
		Last Modified: Tue, 08 Aug 2023 00:41:09 GMT  
		Size: 96.6 MB (96591770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d34a514a03c5af8a03dfe8c4fbfd50b2ec61591d24080f8be8bf722904f541`  
		Last Modified: Tue, 08 Aug 2023 00:40:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802af1410e20c34900a811878ca2fa2e5dc79daeb92a53b94588831011ad81fc`  
		Last Modified: Tue, 08 Aug 2023 00:45:40 GMT  
		Size: 5.2 MB (5249966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9d8614d3da52c8737c0b4449e6e9e688fc7353d31f0246eb31e74f676c1a2`  
		Last Modified: Mon, 14 Aug 2023 18:19:17 GMT  
		Size: 1.2 MB (1186181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aa14602d0d570f4ade4524880d76ae39c401058848761634a02d8513598058`  
		Last Modified: Mon, 14 Aug 2023 18:19:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4c76dac9b235685647bce5e644408f9537fd2a98243936db0666252a4ec24739
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110727449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe6eea8994d5e82ec6e85ed4c441f0a89b9cb461829805dd3eeb9d892d49a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:19:41 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Aug 2023 20:19:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:21:06 GMT
ENV GOLANG_VERSION=1.20.7
# Mon, 07 Aug 2023 20:23:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.20.7.src.tar.gz'; 		sha256='2c5ee9c9ec1e733b0dbbc2bdfed3f62306e51d8172bf38f4f4e542b27520f597'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Mon, 07 Aug 2023 20:23:05 GMT
ENV GOPATH=/go
# Mon, 07 Aug 2023 20:23:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Aug 2023 20:23:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Mon, 07 Aug 2023 20:23:06 GMT
WORKDIR /go
# Tue, 08 Aug 2023 05:25:17 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Mon, 14 Aug 2023 17:41:51 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 17:41:52 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 17:41:52 GMT
ENV XCADDY_SETCAP=1
# Mon, 14 Aug 2023 17:41:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 14 Aug 2023 17:41:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 14 Aug 2023 17:41:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec90be18226e5c99d10161aed1a143f4134093c55b4d6979bbdbbe4b0683eb11`  
		Last Modified: Mon, 07 Aug 2023 20:30:59 GMT  
		Size: 285.1 KB (285089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c751f85e4ba6e9bbada0b11691d914b2ec2c689bb0dca6b9cbe994488d0e3e`  
		Last Modified: Mon, 07 Aug 2023 20:31:56 GMT  
		Size: 100.9 MB (100865267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2d202223222826c8580d85b8d7dd6baa8ed1cad84ba5cf47dab23eaeeae7e9`  
		Last Modified: Mon, 07 Aug 2023 20:31:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359ada615d16e203e1d40a49b896060013c2952c2982ae73b141cc291305a4c`  
		Last Modified: Tue, 08 Aug 2023 05:25:47 GMT  
		Size: 5.1 MB (5099943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1039996d136f688a91d291dcf3dbb995607af1f245f1741d8ad0c5f73cec1b01`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e7bfc7e0d6b6a7f70b22841fe42427f0fb6372b17c71c8063c50d7c8e73c1`  
		Last Modified: Mon, 14 Aug 2023 17:42:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ca7c5b253f237a6f0d30748de0cb616efd5040889648b19dbf2d86855990a759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:d2986a3c3acb890096b8f22fe47d163b679506c701409f0f96ef55f0370c6e49
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2132346458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb468ba68962f7df97763531c45fe07444d56eeed51c25ca5019d9f06b5d07b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:39:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:39:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:39:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:41:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:41:12 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:42:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:53:35 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:56:38 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:56:40 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:20:56 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:20:57 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594083c5c2094c95b4e52723d54c14e0d70881f4f176720c3170012275accc3b`  
		Last Modified: Thu, 10 Aug 2023 01:02:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e2c2a5b75ced3a3a50be088c4a6c2d7df926b1fe6515b2d0c021312e3642f4`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d28688050deeec928289543beadf5c75bb2a8246576cb7c066e23818016217`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e5fbc50e7e0fefb7c9e349038ecb00ed5c000bcab8c4d82b1e1000c4273c01`  
		Last Modified: Thu, 10 Aug 2023 01:02:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544e07bd9df923e11e09c7dc042da614f2f14589eb6fa79005ebbbf2731e97d`  
		Last Modified: Thu, 10 Aug 2023 01:02:57 GMT  
		Size: 25.6 MB (25560980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a82506c4fcec2bd90ae77756e5b03788e30c89f1a3820aa0b6a7ae6ad58ae`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bcfb422b104764156fc5ba099b5e3ae9fa9f760fd2db1c21acd8969b3d73de`  
		Last Modified: Thu, 10 Aug 2023 01:02:50 GMT  
		Size: 220.8 KB (220796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6aa0a5a1689ed800c4ef72c1b9febf207840fd2c6abfe4bb460e2e2bfb0b0`  
		Last Modified: Thu, 10 Aug 2023 01:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d3379322a67b2413189cc2b779d22cb4093124343c8bb17fdf720b7b49fda`  
		Last Modified: Thu, 10 Aug 2023 01:05:25 GMT  
		Size: 108.9 MB (108911716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60ccf92610ddbc47a05664785c95215a123e8930afbf6e3e2cefc80e693fd2`  
		Last Modified: Thu, 10 Aug 2023 01:05:04 GMT  
		Size: 1.5 KB (1468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2c7d6253e62d61e5e0d2ad331a96cff5175f6c608b2ab4657825b3e3b4b4d0`  
		Last Modified: Thu, 10 Aug 2023 03:08:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7441bd899a1ec2037a7dc63ed24148f4362550631136f0b286d1980977fbfcfa`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60695a3cfa3d46aac3798546808cbe211d637be2b7c2af5f9d90d79eb10d544a`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636dfb4139d7b40d2a0cfa8fa63fa590d61d8627017a87a8a517c9c229fdda5b`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d287a3e1b6a016ab5e21634424eddc049708da3cc46e37cc8444f8f20d9ba206`  
		Last Modified: Mon, 14 Aug 2023 18:24:03 GMT  
		Size: 1.7 MB (1679974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cfbbc308f7ee8ad386b267faba56ca74b5aff7b32f0b71f6d94c29f5febe43`  
		Last Modified: Mon, 14 Aug 2023 18:24:02 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:24c81ff6d1a33b0f08066917fb05c2a4c782bb2cd6bd1ba0217709e1e10be849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:2bf33a1b3b64f1ffe31a0ea39e974e24ae1e5d17a1d1f0d3d2c744f8f612a8a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1933831109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2a69ae1b3bbd9a3aefa279d32b203c5ef28dee21038b8b203d78518899270`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:36:23 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:36:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:36:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:36:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:37:00 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:37:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:50:52 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:53:17 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:53:18 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:06:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:22:09 GMT
ENV XCADDY_VERSION=v0.3.5
# Mon, 14 Aug 2023 18:22:10 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:22:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 14 Aug 2023 18:22:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 14 Aug 2023 18:22:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877256a6389e5e2563da79ad5bd201e7ee136abf14ff7cb0d4efbf3b24e5f127`  
		Last Modified: Thu, 10 Aug 2023 01:02:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a39df29b3c0b2f7e691c47273110db4a46e5c8e299f6bb95f77a9c61f79872`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8574d63bce1547e3177d0b76237a782a9b016d4880375dcd1a7b6a1c5dee3dc`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef34b3c96316bcdd92e24c8c4eebdc3a35f245c013ef87edfae0dde091a305`  
		Last Modified: Thu, 10 Aug 2023 01:02:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a481babc5b629f694446a96dba8d77c020257c98334c605aff94162b9a917279`  
		Last Modified: Thu, 10 Aug 2023 01:02:23 GMT  
		Size: 25.6 MB (25554169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281178ea1c103ff07ea7e4fb647eb0dbe4f865742da6ef9944e04f37974fc27c`  
		Last Modified: Thu, 10 Aug 2023 01:02:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5d34adf2aacfe87580143f3e17c635dc8dbd4068377b79b35d665f49bbad9`  
		Last Modified: Thu, 10 Aug 2023 01:02:16 GMT  
		Size: 275.9 KB (275946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02a2e79b5a05c2145c733eefb2add45d1ebefb7a16b93c321f5883c8ced6f1a`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd9991b8cfbc481c153abf1625143209f4c4fd40d9443a5a19f4e3613336ad2`  
		Last Modified: Thu, 10 Aug 2023 01:04:53 GMT  
		Size: 108.9 MB (108927695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dc6778f41c3c7d50b8e71668e22880153d6c6794f24c4661fc3d6aa089d0a5`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5985f015e143065716f5aabf0ecaed537103c5ec07e6c57360204a7787d02`  
		Last Modified: Thu, 10 Aug 2023 03:08:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c565e57b551adf88d5e29bd1458eb8f35437ae3145eba3114c3e38a14420307`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93046b7cb08612cc9fda41d92a61df03529a75e7d266f85a0529c5e88f7d06eb`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a40abe5aa831ec7c89060659309bccacad929792153b60f544eec13c1b6394`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8095d427fe41dd6d758aae45f422bddef28912086c3a3f7797f231535d73ca69`  
		Last Modified: Mon, 14 Aug 2023 18:24:19 GMT  
		Size: 1.7 MB (1690912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8e6227140a7a352f358e4d9e7deab69dc502cd45903e2458244037b6bb36df`  
		Last Modified: Mon, 14 Aug 2023 18:24:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:0da93d63c5b3af38288e909b953bd8cdcf12537c27ff219aac46c6a01775cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:f9824933254e3e43e0508670ee9bdcde704621017e95119a05317383b1878f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18631102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4e9fe28a35a7bd46854ffa0afa91435071afeabac2784f8730569278d8bc9a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:09:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:20:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:20:15 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:20:17 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:20:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aa7b81ef11c65f43b0b58323a33dd9e07eb785529f0d75b452f87a309db00c`  
		Last Modified: Mon, 07 Aug 2023 20:09:40 GMT  
		Size: 350.8 KB (350844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b3b3e68e52dc5ab939c72a9bbac39cff4bef4b87de399ddf28657471df6845`  
		Last Modified: Mon, 14 Aug 2023 18:20:42 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e6a3c74b422682f93a437993c6365f8008e89737276364fd12ea870022f03`  
		Last Modified: Mon, 14 Aug 2023 18:20:45 GMT  
		Size: 14.9 MB (14871143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dc698bd1b82521df87ea42fbf48c98d10133ec962497ac80527b65769ceb6a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17690701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3775ac20cca67f4d547f26f5984a989b9407b0c4129fd6cd86dbb3359249acd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:38:27 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:49:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:49:14 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:49:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:49:16 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:49:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:49:17 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:49:18 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:49:18 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:49:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ef460a93549b8a3e73f6a515bccad93512788d1e8f095e7230ba41967c25a`  
		Last Modified: Wed, 09 Aug 2023 03:38:53 GMT  
		Size: 347.7 KB (347686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aae78767a581df85fd1a51ccd646619aec320896ca016ef0f05a41b16bcbfe`  
		Last Modified: Mon, 14 Aug 2023 17:49:36 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5244db1c019e66038874df2b8b92c74437f6d355802bfccada90c9d8bd8d29`  
		Last Modified: Mon, 14 Aug 2023 17:49:38 GMT  
		Size: 14.2 MB (14190701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e9cb1245e1c134e25a0ec0803e5132ba9ba92d0a4ad85db3f73bd2c3188cf70e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17414619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6e2a1f4c707dc77276814a27ac22a7b5de268780603d8e08324130e1fc563`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:57:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:57:17 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:57:20 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:57:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:57:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:57:21 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:57:21 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:57:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a47b73e04459258b08555443754e92e2db20bde113c58ca18e1a6f07878f72`  
		Last Modified: Tue, 08 Aug 2023 01:52:05 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1b3e18d5e992f1805072b2d52405d575830bdce21726ef99dea99e31d8277`  
		Last Modified: Mon, 14 Aug 2023 17:57:42 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2b7485982d191f9dc0498d5b940d14df575f36ca66876b92d3ca09ff9386b2`  
		Last Modified: Mon, 14 Aug 2023 17:57:48 GMT  
		Size: 14.2 MB (14163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:db04154ce5f7a7f4d058567375880cdc6b1a3675095ad576f9886f39f1374afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17329640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731c0ae21a974e5708c4a8006250893bca5a2ecad43babf2a0a95a60fc61d6cd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:09:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:39:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:39:19 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:39:21 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:39:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:39:22 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:39:22 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a699f78cfb85f60e17fc7c13495876ea0cb4495bbe39e8c65f3e8559b0d7169`  
		Last Modified: Mon, 07 Aug 2023 21:09:34 GMT  
		Size: 360.6 KB (360642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7488af8b96c79b6db13955a0302653c4e9f314d0833201984ae06c1ed697f06`  
		Last Modified: Mon, 14 Aug 2023 17:39:41 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9600da6e7e51b9083b29f3c7de592fa45e7765ca5ffe8d2abf7cc99c50578fe`  
		Last Modified: Mon, 14 Aug 2023 17:39:43 GMT  
		Size: 13.6 MB (13630728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:dfe8f314baac04dac7b7d48bdd1999aedd42d82f792d5a921be7b9a38adbcc07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17021924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09511fed803e1230efcb1c914154726b2f232029c67b0c681319b2eb6ee73a3c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:44:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 18:18:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 18:18:00 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 18:18:05 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 18:18:05 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:09 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:10 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:11 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:18:11 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 18:18:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f40714f45e39ac41e865ccbf2877db62255ce5a5c36a47eadf00b9d174f042`  
		Last Modified: Tue, 08 Aug 2023 00:45:18 GMT  
		Size: 362.2 KB (362173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d19953b5eb53ddaa0e25905527dc138e0c4111467bb7d71f81fa94976091351`  
		Last Modified: Mon, 14 Aug 2023 18:18:54 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff11295d70af9c740cf7afdb57754d70bffd7cd42271ba1a6de34195de6b249`  
		Last Modified: Mon, 14 Aug 2023 18:18:58 GMT  
		Size: 13.3 MB (13305991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:3b3d4b80e160105a760ad62b32c497245d69676e6053c2a7b61bc5c6fc178fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17984968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a63d05bc7601e47460ff86bc91380fd9407c0b4886b80836ac3aadb436f68e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:14:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Mon, 14 Aug 2023 17:41:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Mon, 14 Aug 2023 17:41:39 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 17:41:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ae7a367be45f5cdaa9e5fd082e225dd84f291a6fb1fe2fefa05b9958461e0967d02de23c9147c8e8ebdc4c91b352e887c1c95b06a64fde6be69a5a32fc459d5e' ;; 		armhf)   binArch='armv6'; checksum='d6744a5e835b08208f5bfcd17525ace7b77420bca575126831f0c27100bc2b5f1ce5dcc08585e90bc8e45261d1bacd2ee37d0b1ac7bd57525e953f2a383f2820' ;; 		armv7)   binArch='armv7'; checksum='eed7a8e99dd0802b195986e077a0607536680fc22d735bde2a2773becdd2ab1063754940264dc0f1c1ca81d8d8647e0924a16aead067f1c73c5c372de9320e5c' ;; 		aarch64) binArch='arm64'; checksum='258429b3e7fe821c132f4d455a69c2d230a3f90d18bfebdbf7e9676099e7c6dc1a12af7e0b526b8f6b044cb10fe2aab12e449e529e5ed316b7e5b8433e1b353a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='af49e94af887ef9090ff664877fdb462f33a129f6565504d7cc4b6e3c2995dd4b1b831338809b2450edfea292defa05711beb7cae35331995117258650e17de1' ;; 		s390x)   binArch='s390x'; checksum='81a2bd1e27bf1793c1979009973b468bfc4d05486888ad0376f0e425ef28812e3149f1f7f60dc924d914af6e8ee7ac90c7e1a9c8dd20c2c370f7063c3fa5049a' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 14 Aug 2023 17:41:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 17:41:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 17:41:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 80
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 17:41:44 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 17:41:44 GMT
WORKDIR /srv
# Mon, 14 Aug 2023 17:41:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df19abd0ca1d4a821a4174a2c0831a57d6fd584073f056abcae085a51f0b3848`  
		Last Modified: Mon, 07 Aug 2023 20:14:50 GMT  
		Size: 354.9 KB (354950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308478977890baa82477ee70a3065fb9da2080efcc95facf1a87ac021b06a8e9`  
		Last Modified: Mon, 14 Aug 2023 17:42:17 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fe1cbba37a3c1c2f6ba50e59e5c238c8d83ffca820ef709108b9e3253af757`  
		Last Modified: Mon, 14 Aug 2023 17:42:19 GMT  
		Size: 14.4 MB (14408320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:341d22d35fd224792f17980a37766d5750ea277b08390b43e7a926c46e16b24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4737; amd64
	-	windows version 10.0.20348.1906; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:663d23efed0fab8de5c0b9b2fc5e4ec761e9837c1e3bf6fdf4a66299b137bd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:47322cc21f5e691fbb98548569286dcfacb923408c0dd7bf5bddbb5c1fcaebf4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011989115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576059265fa95c1566183e0a1a17e8b504a8655b7978c401d43bafba04adb5f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:16:58 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:16:59 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:18:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:18:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:18:07 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:18:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:18:09 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:18:10 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:18:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:18:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:18:13 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:18:14 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:18:15 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:18:16 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:19:08 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:19:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d698e8ba8bfd4c31116f0d2c87cfcf2ff17baa1a5c678b116b3aa1ac8ed73d`  
		Last Modified: Mon, 14 Aug 2023 18:23:17 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1870b6ad177365c777c827cd33443816f786b5bfbc9c2f574ae98e817d65c006`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f2ff2c143e53ae2a636032080f5be89642ad59acabe72e5d1f77c7c524b6b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:20 GMT  
		Size: 15.3 MB (15255112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f1046f2f8293851eb91a062983b6c0154ba1467a8b45ea728aeae1affbb52d`  
		Last Modified: Mon, 14 Aug 2023 18:23:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f000ab65fcbe8c9afe009fb3e2a2dd2fca98cbfad62a58729708013464e1495`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979194b0ca28f4ab58cea0708527f1d19410ef0a305700d8a7fe6054d5e835d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda616cdf789d3c189694001b0f218768f325a6ed26d5c2b26188c69d22473c9`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23dc27e20741fbb9c20f1cb51f126fe5cfa8d4dedae3c72b4d7d6684ab5b6`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f86752d97738add39acf4651f7f1ac9aca80c27d4c1995a6db7d87f8ade6f`  
		Last Modified: Mon, 14 Aug 2023 18:23:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfd72013c1683f5dc7ac05a720ad9bf40944c93b5e98e9212fea88c42e19c4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af48796e0134c51f56a5e2e8e884fc1665f27fdb73e3469662ca0ac777cf932`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3f9b2aa10914ea99a2b65bc158407f65d05ba33c042fc77ba38d0fe95b05d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b55eba97d92b1d2472f8a50d7cdb157b20280acbc2b506fc5030a44c99554`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14f918723da99c579f15210e9aaaa3b3ac7bf17a33c0d843a8e42e808d6b384`  
		Last Modified: Mon, 14 Aug 2023 18:23:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaa5419266ef267ae421f3982452d76233cd31bdd4ded0562ae14e6f6586754`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc9a8c622cf5d2fca3b0a13ba5eba7230674025e944a043e68372dce0ef2e29`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c56862a70d6c8cbd3434eed37d1dc8184620ff43221b001fa81eb4dcf5bb7ad`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362a92c5885a5983549b0fe1043c611eb700900bd1d7a183c01284e3d943d255`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 272.7 KB (272666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac329e4dbab5d638cd6e6b30cc50bbd8eb47a2d5df7c211ea40d1a81996755d`  
		Last Modified: Mon, 14 Aug 2023 18:23:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:845b1d612d896dd66d62dedbd373308f5c6df2dbb0b3e24b8bf890f2e255720d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:a657ae6901f69899b28bd0cf8ad59d1766aba69cb98ae614192bc22b0f24b3fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1813357441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e6cefeea4ee50594083f268a625b88021c6547848436664f910f0b2c22eccc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Aug 2023 18:19:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 14 Aug 2023 18:19:51 GMT
ENV CADDY_VERSION=v2.7.3
# Mon, 14 Aug 2023 18:20:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.3/caddy_2.7.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('554be2303ba3455085719a19c453290f1654e9ca8bb1cff3556153a6c6eb6ddd04c430f853d98dd1eee5187d4e341bda52baaa9e8e6617e75a447801af1f2fa0')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 14 Aug 2023 18:20:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 14 Aug 2023 18:20:19 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 14 Aug 2023 18:20:20 GMT
LABEL org.opencontainers.image.version=v2.7.3
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 14 Aug 2023 18:20:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 14 Aug 2023 18:20:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 14 Aug 2023 18:20:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 14 Aug 2023 18:20:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 14 Aug 2023 18:20:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 14 Aug 2023 18:20:26 GMT
EXPOSE 80
# Mon, 14 Aug 2023 18:20:27 GMT
EXPOSE 443
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 443/udp
# Mon, 14 Aug 2023 18:20:28 GMT
EXPOSE 2019
# Mon, 14 Aug 2023 18:20:44 GMT
RUN caddy version
# Mon, 14 Aug 2023 18:20:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c23e01ee014d9e05e276268c94980b00a0720fcb5488a368b20ee74701ed78`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 461.2 KB (461170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbc5a9b39a761a1406b4c68ee24d23ee9735ef7a5593e7517f3c3fdfc10b4b2`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a61905de89a3fb6d7b9f2131aa234001284c9b27584048e89f18fd2b08032e2`  
		Last Modified: Mon, 14 Aug 2023 18:23:45 GMT  
		Size: 15.2 MB (15227866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1c306c1b438f92a876a196824d5428187d3b9de213f268705305da7f20f96`  
		Last Modified: Mon, 14 Aug 2023 18:23:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dedf34b6dbd43467a693874b02eb95e2bf274da111c6a64035962099c80c6e9`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974d426bfc01aca3d82b93c3a166e8aaf90a4d365ca80babee2ddf74f2874565`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621f90b294f8f5200492f50fe0c794ffe46cb39d7c4094f52e4a6185886afebb`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85ba8d7965b92350e0e7b79420c00f4cbd5fa39a275450aaf3a9742ab01d5`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abe5beb445741f1611f5d48d2f7303249e298a97ac62fc36a669728219f395`  
		Last Modified: Mon, 14 Aug 2023 18:23:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342e4138d288aa1d612f386cdea6d6b92415beb2517401eea5397cf4183dd4b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc74cab3a566d84da6983f3c1275f1bd645f38bf392228e22d0fe1be870f75`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4290d1ac7f9298c4f750242024411b1d857b05d8e487b24d8551bc58f7c1973`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba3dec98f5b3502a8b11906c0c1d2a1f320ed0e9ab43e6d52128b59c2b40c4`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06037de139f380a81e177108f60a08bae7d9b27a15492f38839da24ee01c8dfc`  
		Last Modified: Mon, 14 Aug 2023 18:23:38 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbcefa9c20467ffffd9b0fc73660e841a970ba7a7d4bdfa6adf191c1d42ad4e`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a253ba835fdedc409ab08f12eb8ea8880e5d6e64feaa95740c3b9df05e0bf1`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd67169ada5f0c53572ccd6f34c0ac13235bbd84e264ab5cc8a89b203b274d3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daab359f78cf73590c35326769d9ce41bf8884d939bc822bca77fb073501b3`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 280.6 KB (280586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b44d3b6f819726009da651171190271f7a4e56c2a1d9bacfd9bd73a4fec6788`  
		Last Modified: Mon, 14 Aug 2023 18:23:36 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
