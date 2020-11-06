<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2.1.1`](#caddy211)
-	[`caddy:2.1.1-alpine`](#caddy211-alpine)
-	[`caddy:2.1.1-builder`](#caddy211-builder)
-	[`caddy:2.1.1-builder-alpine`](#caddy211-builder-alpine)
-	[`caddy:2.1.1-builder-windowsservercore-1809`](#caddy211-builder-windowsservercore-1809)
-	[`caddy:2.1.1-builder-windowsservercore-ltsc2016`](#caddy211-builder-windowsservercore-ltsc2016)
-	[`caddy:2.1.1-windowsservercore`](#caddy211-windowsservercore)
-	[`caddy:2.1.1-windowsservercore-1809`](#caddy211-windowsservercore-1809)
-	[`caddy:2.1.1-windowsservercore-ltsc2016`](#caddy211-windowsservercore-ltsc2016)
-	[`caddy:2.2.1`](#caddy221)
-	[`caddy:2.2.1-alpine`](#caddy221-alpine)
-	[`caddy:2.2.1-builder`](#caddy221-builder)
-	[`caddy:2.2.1-builder-alpine`](#caddy221-builder-alpine)
-	[`caddy:2.2.1-builder-windowsservercore-1809`](#caddy221-builder-windowsservercore-1809)
-	[`caddy:2.2.1-builder-windowsservercore-ltsc2016`](#caddy221-builder-windowsservercore-ltsc2016)
-	[`caddy:2.2.1-windowsservercore`](#caddy221-windowsservercore)
-	[`caddy:2.2.1-windowsservercore-1809`](#caddy221-windowsservercore-1809)
-	[`caddy:2.2.1-windowsservercore-ltsc2016`](#caddy221-windowsservercore-ltsc2016)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-builder-windowsservercore-ltsc2016`](#caddy2-builder-windowsservercore-ltsc2016)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2-windowsservercore-ltsc2016`](#caddy2-windowsservercore-ltsc2016)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-1809`](#caddybuilder-windowsservercore-1809)
-	[`caddy:builder-windowsservercore-ltsc2016`](#caddybuilder-windowsservercore-ltsc2016)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)
-	[`caddy:windowsservercore-ltsc2016`](#caddywindowsservercore-ltsc2016)

## `caddy:2`

```console
$ docker pull caddy@sha256:b44006ca7a107edd0fca2ff7a70cf75b81b20b61b722dff8a720364a3764ffd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:4ebad49f78a3f98164d89431978046ee6e94f1e8a70454abc7f49ce1a5ee7826
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb0137bab0e21a92b0bc9ec1cc22c259b097d5bf239b161ae1eac0de1833e67`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:33:22 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 04:33:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 04:33:55 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 04:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 04:34:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 04:34:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 04:34:02 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 04:34:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 80
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 443
# Thu, 22 Oct 2020 04:34:06 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 04:34:06 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 04:34:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e2d825895b6421ca5dbd63db0d99f790ef84a84c7bcaff51e60b654397858`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 300.0 KB (299956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaf2e3dee2e74b401fce928bf9502e48df68da4e8c1933bfd6b00b1137529fc`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 5.8 KB (5754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2215cf93250599c5db984cee0fddd5d0cd59ef035ab5a317387b67211bde86d`  
		Last Modified: Thu, 22 Oct 2020 04:35:06 GMT  
		Size: 11.5 MB (11532508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060365e49ba5ee96a2859e269b366f5a5c9f386e5bdbf07d2ef31b1fc6934baa`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:abba73dc860b2f35703cb7d27f08baf5bfc084e18e627b94661d01a8e2befdaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13784259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0aad5a281913821dd39ffed5e144daae22ac81ac4314731395ab65eedde72a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:58:10 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:58:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:58:46 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:58:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:58:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:59:00 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:59:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:59:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:59:03 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:59:08 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:59:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:59:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:59:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:59:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:59:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:59:15 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:59:19 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:59:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:59:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:59:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7369c3ac4b39c55c74e96dd3eb61ac2fa65e5671b1c2acca9697a7c9d20c3cf`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 300.1 KB (300086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8f4045920069dff3382a5993783c5d846d9e28d0f5a63c475ed298fce0abb7`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db6bde4735da15e5db23ad62f3d64d78aed8713a40d12547f5538c15c90f9da`  
		Last Modified: Thu, 22 Oct 2020 03:00:06 GMT  
		Size: 10.9 MB (10876280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a95efd7a14ed98a53a238da45faa7e3b0fdd2a93529b83bfe9d0823dafac67c`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8cf66cbe3c03273ca54bdab908092a6a9b9f02d39595ed15b1111f1465430426
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20723dea614fc40d9f3cb59eddd33bf0e89dfda3f8ed4a7b404ef334632a4b9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:04:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 03:05:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 03:05:45 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 03:05:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 03:05:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 03:05:54 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 03:05:55 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 03:05:56 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 03:05:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 03:06:01 GMT
EXPOSE 80
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 443
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 03:06:03 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 03:06:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a8e7fe5034ac502626b0a921d79be80c092890176e33b236c489d6f00710a2`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 299.2 KB (299211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db75acdaca15b1e81890f29b3b757fcc73e7a69a55f5ed659bf800f6340108`  
		Last Modified: Thu, 22 Oct 2020 03:06:43 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2197c38adf245bca8f229a4cd718c4d0f619a87bae5786572ccdac1a286882c`  
		Last Modified: Thu, 22 Oct 2020 03:06:46 GMT  
		Size: 10.9 MB (10854384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0104bc6a595940856019d00d9ff8e04365338a7964d948b64cc44bf73cc59e`  
		Last Modified: Thu, 22 Oct 2020 03:06:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:da121cf42d1759ed03af3130533d365c365af1d738d550744ad863e05e64cf46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13540356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b4aa38988ab2442575062d99c3cb44976de6c227256c118f35340e7c21c303`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:40:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:40:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:40:57 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:07 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:09 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:10 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:10 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbde357077a97c0f831033bf03c9828203cb7e3e6cb33217ce4d7cfd71c931`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 300.3 KB (300348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a5ab0aa923ce1fe233b904008bbf932c4787f48bcd59f07a85616147b7cbc3`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc398339860cf826624c9c22b5de9b45a193260e2ff24826d210b493483398f`  
		Last Modified: Thu, 22 Oct 2020 02:41:59 GMT  
		Size: 10.5 MB (10527465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6e7d61d1d4a00550447ea1f67edc0463cc527e49356e98959edfafba0df879`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:09208042b4d19d7ed87b51b99dc20b390dab20d9ae7e235a62a3af3aaf472bd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13291756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5c77284adc35481d13003d31a866f637b6eaf9f5764f667e536db79ce23129`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:39:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 13:44:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 13:44:04 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 13:44:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 13:44:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:44:33 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 13:44:37 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 13:44:40 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 13:44:44 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 13:44:48 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 13:44:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 13:44:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 13:45:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 13:45:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 13:45:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 13:45:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 13:45:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 13:45:23 GMT
EXPOSE 80
# Thu, 22 Oct 2020 13:45:26 GMT
EXPOSE 443
# Thu, 22 Oct 2020 13:45:30 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 13:45:35 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 13:45:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a4964211b7ce86541a0c1dad8ef3800ec38a3ca90aff94b76759b4cb8e279`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 302.3 KB (302327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dd938ef3e3eae8509deda8fab9ab5f9344169d912e35a802633e799feed1bb`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe23c296ee12ee12ef84dbabbb4f7bf0362a9a12b684782ebd3f44a97c8fcf8e`  
		Last Modified: Thu, 22 Oct 2020 13:47:55 GMT  
		Size: 10.2 MB (10180223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2f3c084745fecafaa9ff33626a81124f2d70267ceee705da555714238bfa1`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:3e18b421d651721239cb3422bc890d1211535681219b7696816f487b4cebc4ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14074857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d5562f1d148d3d67ff7f5995be8f860553ad0f3d07091335643306b83385e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:41:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:41:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:41 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f988ff23f3cbb35bfed69e33f3b7ee69403bfae4f46363a08eea4830053e9c`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 300.5 KB (300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd6a4e0db99510879c5dfceabd1e629a0692c4544bb0da34971f8722b881e92`  
		Last Modified: Thu, 22 Oct 2020 02:42:09 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e13b938aa802e74610585cabba77d625db4baf219f577a81195c272408c7d3`  
		Last Modified: Thu, 22 Oct 2020 02:42:16 GMT  
		Size: 11.2 MB (11202559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a221fff082950a8a98db12eb99f532a39008f0d6e21684bc1aed06fa1ed2a764`  
		Last Modified: Thu, 22 Oct 2020 02:42:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1`

```console
$ docker pull caddy@sha256:2ba92290b2abd80fc97283c3b3a1636f7614c0a5cd38d1ad318c034055540545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.1.1` - linux; amd64

```console
$ docker pull caddy@sha256:94aab32108ee277eca3476c03eb3cd0c791581ccceef288e4021b4658b6e14e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813d26d5b5f80df7e1a12968331cc52103ef347206fdfe404f095db39538745f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:33:22 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 04:33:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 04:33:24 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 04:33:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 04:33:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:33:30 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 04:33:30 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 04:33:31 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 04:33:31 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 04:33:31 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 04:33:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 04:33:32 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 04:33:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 04:33:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 04:33:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 04:33:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 04:33:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 04:33:34 GMT
EXPOSE 80
# Thu, 22 Oct 2020 04:33:34 GMT
EXPOSE 443
# Thu, 22 Oct 2020 04:33:35 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 04:33:35 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 04:33:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e2d825895b6421ca5dbd63db0d99f790ef84a84c7bcaff51e60b654397858`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 300.0 KB (299956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792a8e39706390221a8cc5927203b39027a0bce4149c60137a8a68c14124a188`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 5.8 KB (5753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e121fa2dd673519fd0bbbe8acae3339d2c242a0d454569905d45fcae45cbd210`  
		Last Modified: Thu, 22 Oct 2020 04:34:50 GMT  
		Size: 13.1 MB (13057360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cabd94ff7acf4922fc1f955d07f4c8a22e63a2cb69ca77d49d20629759e6d7`  
		Last Modified: Thu, 22 Oct 2020 04:34:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; arm variant v6

```console
$ docker pull caddy@sha256:3dcf641ed85190e11d4d2aeee30ce6fd5e12acaf14764d0ecc9c2d43cc5c52f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15322911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dc188cdeb883fd020df45c6c2e4274e437337e1820e0db79e0b0ff14295b34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:58:10 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:58:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 02:58:13 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 02:58:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:58:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:58:22 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:58:23 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:58:23 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:58:24 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:58:25 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 02:58:25 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:58:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:58:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:58:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:58:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:58:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:58:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:58:30 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:58:31 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:58:32 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:58:32 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:58:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7369c3ac4b39c55c74e96dd3eb61ac2fa65e5671b1c2acca9697a7c9d20c3cf`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 300.1 KB (300086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0affadb729cb104658a545e4b2cd1eb71a6f4ca473a7576bb6a65d97de2003ff`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a834360c16db0f4578fa61b1bb8e51d39cfdfa7616b763a7f9080b5f3fd337`  
		Last Modified: Thu, 22 Oct 2020 02:59:55 GMT  
		Size: 12.4 MB (12414928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dea75e2b66ab3649bf01ef2e7accd82012104cf4bc9dd180b75298b9335941`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; arm variant v7

```console
$ docker pull caddy@sha256:3ad6c0a0783ba264b9258c26ecd947b8c1ddd9ce0eedf47bf50e0d92ce26b253
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa5aceec9b3b914788468802d025e1d1f3551a181c58365d22efa3fe8dfb9f3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:04:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 03:05:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 03:05:01 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 03:05:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 03:05:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:05:11 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 03:05:12 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 03:05:13 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 03:05:13 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 03:05:14 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 03:05:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 03:05:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 03:05:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 03:05:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 03:05:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 03:05:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 03:05:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 03:05:22 GMT
EXPOSE 80
# Thu, 22 Oct 2020 03:05:23 GMT
EXPOSE 443
# Thu, 22 Oct 2020 03:05:24 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 03:05:26 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 03:05:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a8e7fe5034ac502626b0a921d79be80c092890176e33b236c489d6f00710a2`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 299.2 KB (299211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac4e817bcf2c7b80f6f6341ad2e45a1a984b272460858c08c1a39ca8acddbe`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4916ca18103e521657f386ae15b838945f507f4e71e7ffb9ae6146a207fc98e4`  
		Last Modified: Thu, 22 Oct 2020 03:06:36 GMT  
		Size: 12.4 MB (12396037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516dbda4db0089c1377a5f56e371ecf8ebada5ddedf4eb445b7b5a00b35837a0`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bed04cea05f8703919db1411fa43db3caf2c5feee4604e432ca3fbb39ba4e9e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15025979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3072bf9e0127310f4d1cc1237287c7562fe9fe90f9e7084ef33d8ebd97fb70`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:40:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:40:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 02:40:09 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 02:40:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:40:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:40:22 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:40:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:40:24 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:40:25 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:40:26 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 02:40:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:40:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:40:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:40:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:40:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:40:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:40:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:40:33 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:40:33 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:40:35 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:40:36 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:40:37 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbde357077a97c0f831033bf03c9828203cb7e3e6cb33217ce4d7cfd71c931`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 300.3 KB (300348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede963cf3892bef49a806e2b2b6cd351a073839746d3ba0040c807c9ede34282`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 5.8 KB (5825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dd5666b9cb9cb79f2931d16947dff6632df90edde47a765a9abb46d21a7f8e`  
		Last Modified: Thu, 22 Oct 2020 02:41:50 GMT  
		Size: 12.0 MB (12013098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ac0780379a69d70077155f92bdaf6679c77647156daf6c6b61784db51baf0b`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; ppc64le

```console
$ docker pull caddy@sha256:013e8f3007f8464b73d523c0620524d183067549b162c35f7c34a104b2e03c19
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7eb13196205b2269a7eba953f625b2a6cb717e66971db551bcc960cd917cc2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:39:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 13:40:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 13:40:25 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 13:40:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 13:41:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:41:08 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 13:41:13 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 13:41:19 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 13:41:26 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 13:41:32 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 13:41:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 13:41:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 13:41:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 13:42:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 13:42:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 13:42:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 13:42:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 13:42:18 GMT
EXPOSE 80
# Thu, 22 Oct 2020 13:42:23 GMT
EXPOSE 443
# Thu, 22 Oct 2020 13:42:29 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 13:42:34 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 13:42:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a4964211b7ce86541a0c1dad8ef3800ec38a3ca90aff94b76759b4cb8e279`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 302.3 KB (302327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d796f3d42ae827c5c6abc4f1d86eb2c77d579b52d88f20195c3480d66f3e0af`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b45c60413a5845a6a452dfc06bfecd19bdcb7111f4c5011c9c273914f54284`  
		Last Modified: Thu, 22 Oct 2020 13:47:26 GMT  
		Size: 11.8 MB (11785457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae3c1c0668096c5f9942efa1b8694a27b599f3996495b052f5cd7f6e0188781`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; s390x

```console
$ docker pull caddy@sha256:937db8998b02f140f7b1dc4d9b6a14ff40db24dfdc22d4b1d1f5d0d0509e67ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a65f150c3943695dbf4e3018205572467467599ba7ea5010e044f5fced62d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:41:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:41:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 02:41:10 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 02:41:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:15 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:15 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:16 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:16 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:20 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f988ff23f3cbb35bfed69e33f3b7ee69403bfae4f46363a08eea4830053e9c`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 300.5 KB (300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb33c2548f9314af36267dc9e886d94ad83d75881e0c93b6931ed52734b7f451`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad254f130346e29cbf490913417f35cf7473184bba1b7ff8d90579f3b2809a29`  
		Last Modified: Thu, 22 Oct 2020 02:42:03 GMT  
		Size: 12.8 MB (12836808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01317e485bb835fdf7067969a86d9fa9679bdd0a1c214931b788e4b8e9388f`  
		Last Modified: Thu, 22 Oct 2020 02:42:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:66f70d738fddf55c60091b6aef8e41b63c76802b802ab717413fe9c818037124
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401370099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1397040752ad41e2b18db058da0b7e519033692fcea840d807a898de17943dde`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 20:55:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 20:55:53 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 20:56:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 20:56:28 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 20:56:29 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 20:56:30 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 20:56:30 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 20:56:31 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 14 Oct 2020 20:56:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:56:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:56:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:56:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:56:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:56:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:56:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:56:37 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:56:38 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:56:39 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:56:55 GMT
RUN caddy version
# Wed, 14 Oct 2020 20:56:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b188d60ff330af293d4e64c0e8d02efc672b84164a7f28c2b88c6fa69e773b`  
		Last Modified: Wed, 14 Oct 2020 21:11:59 GMT  
		Size: 9.2 MB (9238100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7cca4341580aaef49dda3a35fbe74dea069dea552f29d609095c28ae31c7c9`  
		Last Modified: Wed, 14 Oct 2020 21:11:55 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc6acc9f3a56b460718597090a53b19d8ae56936b8c1f305a0fc5b6c8ae834`  
		Last Modified: Wed, 14 Oct 2020 21:12:01 GMT  
		Size: 17.7 MB (17721908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da2dbe8389d72a6c47be48a14049de1017ecd0bfe42e9b39137feb681a86e2`  
		Last Modified: Wed, 14 Oct 2020 21:11:55 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08f4acb6066947f91cc9e9472c80e0f37f13d618d651351b8b3d6efd0d972d9`  
		Last Modified: Wed, 14 Oct 2020 21:11:54 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc07733f0dbd5754df935d2dd9eb9b99ec6a8833f5801ce1d28dfbd5dc06537d`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f794342b0d24d7695630534ed119afcfd13154a5661e49b0fb63a9d09239389`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f8231f3a84092e779185d6075769d2024c8ca7743081f3c9da45468d7f3550`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e35f7ff6908cb027518acbf4190fa1665763a290334d11445f85785ee2b6eb6`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a6ac3896b488a27e5a2289f4a62b934db8638756d02666690ff6e80621f0b3`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fa5374e20ab60dd6a7d2bdd71a4996a10f825e28542c0a038a25b5bc64fc10`  
		Last Modified: Wed, 14 Oct 2020 21:11:49 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f8e08e4c4e4262e9a897ff6a2366db843c277188a19522c2b3a238a70d2e92`  
		Last Modified: Wed, 14 Oct 2020 21:11:49 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309bc178193a0f7b99147d5aabc6bfb9a799756c1893656a74c945570438c75`  
		Last Modified: Wed, 14 Oct 2020 21:11:48 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c0747bfbf50db12f814e3dea2b3a71b1bb951fc8f401365199cf535793880b`  
		Last Modified: Wed, 14 Oct 2020 21:11:49 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492e7f435eff381b7d6b25eb81362a6c0fd4b461ddc05978afdfaf175ff99756`  
		Last Modified: Wed, 14 Oct 2020 21:11:48 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5be9e7e60f33a1a982e2fd5a12de9103b8c6c763d561b14577abf49c36209`  
		Last Modified: Wed, 14 Oct 2020 21:11:45 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705ffea3945c47a37e15327ec3683dbc90a9e05a214b10f7384f782dd4d066c`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59c3c8fe6d1b33da8d76616405e7bf142019d8d8e2a5d372496773d29a50f5`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e00a541946fdd8a1f98a5d34d51dca7bd037860ba1aa2a85c978213e80d25f`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 299.5 KB (299487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17888b1c5a918fe0001ed5ea3f284e619eaa9c54b6de64d7f8def19bc9a4f7f7`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:3df3617581091c8a721884e7886ef930f68708e6be320bd2252ef6f490f2512e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5774462347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc16ee492900dee7e9f4e124e5439d5a2a26376ffe0e4c4b85461f0907b2abf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 20:58:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 20:58:30 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 20:59:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:00:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:00:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:00:03 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:00:04 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:00:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 14 Oct 2020 21:00:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:00:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:00:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:00:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:00:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:00:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:00:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:00:11 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:00:11 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:00:12 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:00:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:00:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0621c6e14481e8b7931a54a60b5f552ab50344f6a75362eb856e08a00a6e121d`  
		Last Modified: Wed, 14 Oct 2020 21:12:28 GMT  
		Size: 9.9 MB (9924480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4a1346a3116e78ed00103d93f985d7f4bf3df06cb8088bca9b316cc656a1b8`  
		Last Modified: Wed, 14 Oct 2020 21:12:24 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828c93647c40ffc8bcbe621b61aef3677861ae673ef3b66ac1792c99c95234d9`  
		Last Modified: Wed, 14 Oct 2020 21:12:30 GMT  
		Size: 22.9 MB (22896440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4726960f8ff938227c56d540f881d9bc18e607f3301cd3cead8b652ec7ef517`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5e13596b93a65158bebc3e1cfb8345e098bd9a27f4171069026fc575224d8`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06356772b928f71cb618db080d52bdca9588cf499ea10913136623ea3c89ac9d`  
		Last Modified: Wed, 14 Oct 2020 21:12:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35687f4e534a86ba4f3538c39b22db8a401bc0335da0a91c471f9eff0e934abd`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0234c902cd868cb06435cb99ba8470182d7955305dd550a6f9e85dfdbf0589`  
		Last Modified: Wed, 14 Oct 2020 21:12:18 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdc33faacf12c704737e72c800eaa28e3da94d8ed7df679e786358a09d471bf`  
		Last Modified: Wed, 14 Oct 2020 21:12:18 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f0814377cdb217e3609cccb0c763feeab8b5f8a35b447a95dfd89ed1cad48`  
		Last Modified: Wed, 14 Oct 2020 21:12:17 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c94837bff217cff65168fc6eebe67956699dbee13427803f6970aa8f224dc10`  
		Last Modified: Wed, 14 Oct 2020 21:12:16 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d2486511a0c9601a2bdd89e2ebd54297bb2c78735b569e84014aa00cfb6d3`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1435a16a8f89084f597da43cb9ce1413ac817712fad3e6683dd165dc7cc36296`  
		Last Modified: Wed, 14 Oct 2020 21:12:14 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9479319b79d0a97d0b6d91034585fb6f52136095829c563c4b36d57bdfe54c23`  
		Last Modified: Wed, 14 Oct 2020 21:12:15 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f84c09f0f902199fdd83bb5ec0da426140430cf1ae9b37d63635d70b45ddad`  
		Last Modified: Wed, 14 Oct 2020 21:12:13 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c89752e1d722e1a2bdb8c5936cbf20f3ca2c699136b1279ac27f93b75110cf`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b75e4a8389cdb23c1d9ebf7fc2e685469542f5e1ac0f7a32e1818e04001d88`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58bcc9da6dff9ee1073dd37c941b628f26ee80400f5a9e8c2bbbd8749815c42`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46327701e2d8e59d0173f0db37999a9d1e633a41f36e739bfe94a37c34406aee`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 269.3 KB (269317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd16f3084947685df6d6043025f0d44efccb637918ffc69bbebafea7e3c94970`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-alpine`

```console
$ docker pull caddy@sha256:acf4730fd996e56a713b99d6f1892b87bf9f95af4ebc5fed53e942986ffbc2cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.1.1-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:94aab32108ee277eca3476c03eb3cd0c791581ccceef288e4021b4658b6e14e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813d26d5b5f80df7e1a12968331cc52103ef347206fdfe404f095db39538745f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:33:22 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 04:33:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 04:33:24 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 04:33:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 04:33:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:33:30 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 04:33:30 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 04:33:31 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 04:33:31 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 04:33:31 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 04:33:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 04:33:32 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 04:33:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 04:33:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 04:33:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 04:33:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 04:33:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 04:33:34 GMT
EXPOSE 80
# Thu, 22 Oct 2020 04:33:34 GMT
EXPOSE 443
# Thu, 22 Oct 2020 04:33:35 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 04:33:35 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 04:33:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e2d825895b6421ca5dbd63db0d99f790ef84a84c7bcaff51e60b654397858`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 300.0 KB (299956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792a8e39706390221a8cc5927203b39027a0bce4149c60137a8a68c14124a188`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 5.8 KB (5753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e121fa2dd673519fd0bbbe8acae3339d2c242a0d454569905d45fcae45cbd210`  
		Last Modified: Thu, 22 Oct 2020 04:34:50 GMT  
		Size: 13.1 MB (13057360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cabd94ff7acf4922fc1f955d07f4c8a22e63a2cb69ca77d49d20629759e6d7`  
		Last Modified: Thu, 22 Oct 2020 04:34:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:3dcf641ed85190e11d4d2aeee30ce6fd5e12acaf14764d0ecc9c2d43cc5c52f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15322911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dc188cdeb883fd020df45c6c2e4274e437337e1820e0db79e0b0ff14295b34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:58:10 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:58:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 02:58:13 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 02:58:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:58:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:58:22 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:58:23 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:58:23 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:58:24 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:58:25 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 02:58:25 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:58:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:58:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:58:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:58:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:58:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:58:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:58:30 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:58:31 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:58:32 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:58:32 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:58:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7369c3ac4b39c55c74e96dd3eb61ac2fa65e5671b1c2acca9697a7c9d20c3cf`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 300.1 KB (300086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0affadb729cb104658a545e4b2cd1eb71a6f4ca473a7576bb6a65d97de2003ff`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a834360c16db0f4578fa61b1bb8e51d39cfdfa7616b763a7f9080b5f3fd337`  
		Last Modified: Thu, 22 Oct 2020 02:59:55 GMT  
		Size: 12.4 MB (12414928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dea75e2b66ab3649bf01ef2e7accd82012104cf4bc9dd180b75298b9335941`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:3ad6c0a0783ba264b9258c26ecd947b8c1ddd9ce0eedf47bf50e0d92ce26b253
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa5aceec9b3b914788468802d025e1d1f3551a181c58365d22efa3fe8dfb9f3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:04:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 03:05:00 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 03:05:01 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 03:05:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 03:05:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:05:11 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 03:05:12 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 03:05:13 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 03:05:13 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 03:05:14 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 03:05:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 03:05:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 03:05:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 03:05:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 03:05:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 03:05:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 03:05:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 03:05:22 GMT
EXPOSE 80
# Thu, 22 Oct 2020 03:05:23 GMT
EXPOSE 443
# Thu, 22 Oct 2020 03:05:24 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 03:05:26 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 03:05:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a8e7fe5034ac502626b0a921d79be80c092890176e33b236c489d6f00710a2`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 299.2 KB (299211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eac4e817bcf2c7b80f6f6341ad2e45a1a984b272460858c08c1a39ca8acddbe`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4916ca18103e521657f386ae15b838945f507f4e71e7ffb9ae6146a207fc98e4`  
		Last Modified: Thu, 22 Oct 2020 03:06:36 GMT  
		Size: 12.4 MB (12396037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516dbda4db0089c1377a5f56e371ecf8ebada5ddedf4eb445b7b5a00b35837a0`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bed04cea05f8703919db1411fa43db3caf2c5feee4604e432ca3fbb39ba4e9e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15025979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3072bf9e0127310f4d1cc1237287c7562fe9fe90f9e7084ef33d8ebd97fb70`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:40:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:40:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 02:40:09 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 02:40:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:40:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:40:22 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:40:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:40:24 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:40:25 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:40:26 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 02:40:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:40:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:40:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:40:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:40:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:40:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:40:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:40:33 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:40:33 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:40:35 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:40:36 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:40:37 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbde357077a97c0f831033bf03c9828203cb7e3e6cb33217ce4d7cfd71c931`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 300.3 KB (300348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede963cf3892bef49a806e2b2b6cd351a073839746d3ba0040c807c9ede34282`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 5.8 KB (5825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dd5666b9cb9cb79f2931d16947dff6632df90edde47a765a9abb46d21a7f8e`  
		Last Modified: Thu, 22 Oct 2020 02:41:50 GMT  
		Size: 12.0 MB (12013098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ac0780379a69d70077155f92bdaf6679c77647156daf6c6b61784db51baf0b`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:013e8f3007f8464b73d523c0620524d183067549b162c35f7c34a104b2e03c19
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7eb13196205b2269a7eba953f625b2a6cb717e66971db551bcc960cd917cc2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:39:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 13:40:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 13:40:25 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 13:40:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 13:41:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:41:08 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 13:41:13 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 13:41:19 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 13:41:26 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 13:41:32 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 13:41:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 13:41:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 13:41:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 13:42:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 13:42:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 13:42:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 13:42:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 13:42:18 GMT
EXPOSE 80
# Thu, 22 Oct 2020 13:42:23 GMT
EXPOSE 443
# Thu, 22 Oct 2020 13:42:29 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 13:42:34 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 13:42:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a4964211b7ce86541a0c1dad8ef3800ec38a3ca90aff94b76759b4cb8e279`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 302.3 KB (302327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d796f3d42ae827c5c6abc4f1d86eb2c77d579b52d88f20195c3480d66f3e0af`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b45c60413a5845a6a452dfc06bfecd19bdcb7111f4c5011c9c273914f54284`  
		Last Modified: Thu, 22 Oct 2020 13:47:26 GMT  
		Size: 11.8 MB (11785457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae3c1c0668096c5f9942efa1b8694a27b599f3996495b052f5cd7f6e0188781`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:937db8998b02f140f7b1dc4d9b6a14ff40db24dfdc22d4b1d1f5d0d0509e67ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a65f150c3943695dbf4e3018205572467467599ba7ea5010e044f5fced62d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:41:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:41:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Thu, 22 Oct 2020 02:41:10 GMT
ENV CADDY_VERSION=v2.1.1
# Thu, 22 Oct 2020 02:41:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:15 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:15 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:16 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:16 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:20 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f988ff23f3cbb35bfed69e33f3b7ee69403bfae4f46363a08eea4830053e9c`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 300.5 KB (300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb33c2548f9314af36267dc9e886d94ad83d75881e0c93b6931ed52734b7f451`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad254f130346e29cbf490913417f35cf7473184bba1b7ff8d90579f3b2809a29`  
		Last Modified: Thu, 22 Oct 2020 02:42:03 GMT  
		Size: 12.8 MB (12836808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01317e485bb835fdf7067969a86d9fa9679bdd0a1c214931b788e4b8e9388f`  
		Last Modified: Thu, 22 Oct 2020 02:42:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-builder`

```console
$ docker pull caddy@sha256:636b254e34130443cc96001408917efd36114fc41cb4ad3536e1c480a1347a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.1.1-builder` - linux; amd64

```console
$ docker pull caddy@sha256:8cdf9805f8ee2effcfbf85d38a73de2e403d76c9776b2f58b5e1bdcf0006c5e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119980569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febc6237a0bf9eedcc6a574d23443701faa31ca65f424315f6bf18e84245a6b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:34:56 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:34:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:34:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:39:34 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:42:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:42:13 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:42:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:42:15 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:18:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:18:02 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:18:02 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 21:18:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:18:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:18:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:18:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7d3d256c8367c41c431143c63d083a25dd62ec9ee9d9773dd9e6c7b70ec9e`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9db76c5a1d06710ed4f3073476b2d883ff8e911f8e47c558bc4a8d1d8663fa`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48409b4593ac14b4d18a7ad560244a8940ea07c979696ee49974119d814de59`  
		Last Modified: Fri, 06 Nov 2020 19:50:32 GMT  
		Size: 107.2 MB (107185138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dae78a39a60068885ae0b61f535b899a1201348f12f94ae869dedee1d48dc0`  
		Last Modified: Fri, 06 Nov 2020 19:49:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a28bc188dc0e57f523fcc33cd05c3a40e99022e7ed703613edc6709f4694d`  
		Last Modified: Fri, 06 Nov 2020 21:18:30 GMT  
		Size: 8.3 MB (8309872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba47cc29a2a07b08764e865981321e8cdf4c203c5b9fdc5d2f60acef03d55de`  
		Last Modified: Fri, 06 Nov 2020 21:18:29 GMT  
		Size: 1.4 MB (1407205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f1af179205f9fd430048ae729134c5828b82b24ac6c53c19f7aa669b43069`  
		Last Modified: Fri, 06 Nov 2020 21:18:29 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6e03ac44e32d0122ec224b4c74ff4e0127a5a40612429b1d6ff28a8c0f71de7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115652045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0222914f93ab21dd162769f1412a248f51fca10be55eb3d7bf12b3d431114bb0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:07:24 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:07:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:56:33 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 18:59:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:59:13 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:59:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:59:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:59:18 GMT
WORKDIR /go
# Fri, 06 Nov 2020 19:22:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 19:22:26 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:22:27 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 19:22:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 19:22:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 19:22:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20cc27a60e8ac1bf56dec787d3d52ba856e657179cfd56050036db79abb4267`  
		Last Modified: Thu, 22 Oct 2020 05:34:55 GMT  
		Size: 281.0 KB (280971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecce92c3d2de40638d73e682dec26c2b79a055e85c8d70b88f4ccb9485bb9c9`  
		Last Modified: Thu, 22 Oct 2020 05:34:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84eb6f64c07ea29969461f90aba8c1beaf51c214bf245baac9ccc85c1d33da`  
		Last Modified: Fri, 06 Nov 2020 19:05:01 GMT  
		Size: 103.5 MB (103512267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf75f59bedadb379f5e8756bc99336e96050855587837452d72eaf918c3b8c`  
		Last Modified: Fri, 06 Nov 2020 19:04:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd9d45b83e45ca8a5cdb6ac3e3b80d78efb0119790a01aa468e1bb0c761463e`  
		Last Modified: Fri, 06 Nov 2020 19:23:25 GMT  
		Size: 7.9 MB (7928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016a22366d0714e29a48006a63b3492a8961d099c64cc358a44411181a3699eb`  
		Last Modified: Fri, 06 Nov 2020 19:23:22 GMT  
		Size: 1.3 MB (1327349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0d1bd89e3d5467a79c8b80301f79bf8033129da43cd4c72e489213f7cbf229`  
		Last Modified: Fri, 06 Nov 2020 19:23:24 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:b258fde47854d7b0285263610f5c6b9ffb6f06f3a780f6cfaa1a2863495b76fd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114436919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ec4c012233a9aefd5e4aa0669e15e3d8e1cfa9cf9d6c0c36fb1a8bff795c05`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:21:35 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:23:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:23:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:43:07 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:45:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:45:16 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:45:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:45:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:45:19 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:27:11 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:27:12 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:27:13 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 20:27:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:27:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:27:18 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:27:19 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b753cfc04fdce9640aac1e7a4b3e7ce15fa60b8e357376e42f294f463a6e890`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 280.1 KB (280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90c422e5e4668cb4140aadb622d734faa93c81cc1e283da9b08bbbc65c45c5`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd774dd42f20c72b2335aa86df0dcc76905d1a383bde3112f60f378ed6d5723c`  
		Last Modified: Fri, 06 Nov 2020 19:51:32 GMT  
		Size: 103.3 MB (103279793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87040eea28146abacdfa46238d6cf7ef9ec51038c04f53bdc9796a19455a82bf`  
		Last Modified: Fri, 06 Nov 2020 19:51:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f628e6ce0af305e50899cbe69dc0cde182ce627be5f4f2f742e4e4d3aa655ddb`  
		Last Modified: Fri, 06 Nov 2020 20:27:58 GMT  
		Size: 7.1 MB (7144806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecae0064d644c67a7e9b4772602b5194d033a53ad75183941bcd7aaef30216f`  
		Last Modified: Fri, 06 Nov 2020 20:27:57 GMT  
		Size: 1.3 MB (1325849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6af0e7d5ff1fe239f9dac42c70236ac44dc14b54544d68bc9198fae3976a731`  
		Last Modified: Fri, 06 Nov 2020 20:27:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:98e85c3ec782158255bf07c86cf4ddc1af17f27714e3db27f96ba9e4813627a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115389072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959b60761716890807f31a405129cd97f761ae14a7a9c45e3dcce972c20196bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:08:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 04:09:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:09:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:22:27 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:24:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:24:21 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:24:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:24:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:24:24 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:09:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:09:09 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:09:09 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 21:09:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:09:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:09:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:09:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4357932f1b6fb010e1461cc5c673712fb832ac44ee627c691db0b64adf95d13`  
		Last Modified: Thu, 22 Oct 2020 04:28:32 GMT  
		Size: 281.2 KB (281230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c013af1878066e59b688e31fd962e7267430963de27c5257241e3c223aa1d6`  
		Last Modified: Thu, 22 Oct 2020 04:28:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77e4c4323cac205b0e0648168654eeab6f1d9ea388b2015cbc59650af632f62`  
		Last Modified: Fri, 06 Nov 2020 19:30:36 GMT  
		Size: 102.6 MB (102590506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68f5aacb416a2fa6d097869ed282ee7821d32ed2a401bb9b859b1ebd97a2122`  
		Last Modified: Fri, 06 Nov 2020 19:29:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eff0fc08530c920c358100c2a0cb516e6786ed8b58dd0e4942511f0742c18d`  
		Last Modified: Fri, 06 Nov 2020 21:09:50 GMT  
		Size: 8.5 MB (8499886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f028f5696a14b2a25eda02fed36563bbd062875533c28bda40befbe94b745bb`  
		Last Modified: Fri, 06 Nov 2020 21:09:49 GMT  
		Size: 1.3 MB (1310181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b381b359844b948cbaf36687576d6edffc27fe51080622429028d41957161`  
		Last Modified: Fri, 06 Nov 2020 21:09:48 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:599fb5e07848cdb565aff8218812de0ab0356ca4f4e494ac54b4b76f3b665ba6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114750254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3220c299d6244b3e456c75c7df025f07001fd35feb0bd0f9e78cecf81f300107`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:27:26 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 13:27:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:27:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:37:07 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 18:39:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:39:50 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:39:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:40:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:40:09 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:49:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:49:53 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:50:02 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 21:50:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:50:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:50:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:50:37 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9900411dc7c8c88618743573bf89478d726007403bd002d8b00d21b7fecd40a`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 283.2 KB (283205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbd106374e3baf7eb8e3d8f7ffd4c364a35e57dcb3a89f8a153327a4c3fa3f9`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b4aa7e1e5dc7bf7676d23c31004345d0d9caccb847a614fdf0c0db9247a1af`  
		Last Modified: Fri, 06 Nov 2020 18:48:27 GMT  
		Size: 101.5 MB (101455314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bbeeae924df02f9094e25dd06eab3287fb50dd3911b39fd970d38a33e8fc59`  
		Last Modified: Fri, 06 Nov 2020 18:48:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2676d8220c83008613c392a60f715be838ffca488f7c01fd29c18983a9b20e`  
		Last Modified: Fri, 06 Nov 2020 21:52:14 GMT  
		Size: 8.9 MB (8920011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62236f2f9f55cef8f0f51973bb8fc73f9ca395d0c6e5cf984f0ee9d8eddd016d`  
		Last Modified: Fri, 06 Nov 2020 21:52:12 GMT  
		Size: 1.3 MB (1287789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cb6b56b91c30f2dd1f54a71d24e3e4a6c8999da1bc1e2537d393fa6a269c8`  
		Last Modified: Fri, 06 Nov 2020 21:52:11 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:b738347a37a68d64dbee00f6d4bf271000afe0693211228649ae5ac8c58ca056
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119637445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007c80af833d86fee3681b4e7735f66fba05e751e43192c9a7797415a3eb58d9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:53:28 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 02:53:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:53:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:27:26 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:30:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:30:13 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:30:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:30:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:30:15 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:39:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:39:47 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:39:47 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 20:39:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:39:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:39:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5139d7663b8674a989574c2161166fb137f26ef16b2f701159c126628be75101`  
		Last Modified: Thu, 22 Oct 2020 02:58:32 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31a06258ad66efe2dedbf67809ebc107a55757b8a4543af77982f55ff6c067`  
		Last Modified: Thu, 22 Oct 2020 02:58:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02a44448cd0d67bcfdbc04c5583bad139970194e2795ad8699b66da2238ed9d`  
		Last Modified: Fri, 06 Nov 2020 19:35:17 GMT  
		Size: 107.0 MB (107048570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810a62791e651c5fd7242cc42273cb38f14590dfb699cef7c9fdb4ba531fa19`  
		Last Modified: Fri, 06 Nov 2020 19:35:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e36381debf2397a3a5b23905fc4109ad02a1675d793b1f222be94936b3e5bf9`  
		Last Modified: Fri, 06 Nov 2020 20:40:38 GMT  
		Size: 8.4 MB (8352213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a7aaf2223f223857df02983b33e17c5c450bbd7109e70f7a6ebf06f070932`  
		Last Modified: Fri, 06 Nov 2020 20:40:36 GMT  
		Size: 1.4 MB (1388754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf7c2cb4c0878e3ae5dd253020a4f3e59eba612bfcd7c8b9ac2d167da983cbd`  
		Last Modified: Fri, 06 Nov 2020 20:40:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:4bca501cd66dbb0f3114b28b14abe636d063dd9b0119af54dcef494a80df8b1e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2552955192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3d49f4bc529f061eb9dd7cea4bb34cec257265b56208df8e5528b0c36c964e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:27:03 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:27:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:28:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:28:38 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:29:02 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:24:16 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:26:41 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.14.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5f58d41f6f22ce13081cc6118b238a2e540dc6168b3b7e26d786f2ec41a65872'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:26:43 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:55:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:55:21 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:55:22 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 19:55:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:55:51 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:55:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23a75d88f9f5980bb112e2c28248975f107144d8d2e40dc4755e2a09f5e56df`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea6d8b9d9b014ffa471b7bb8882ddb7e9d378ddcacc099f0710073bd6361b9`  
		Last Modified: Wed, 14 Oct 2020 12:50:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75c1905c0573cc5706bc066d23624f0e92a8871832c744fbe7eabdcbc6f8a85`  
		Last Modified: Wed, 14 Oct 2020 12:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938695376d9deeba8819539ff3245935c28f93229d1c332bb8b6a16e67013fbc`  
		Last Modified: Wed, 14 Oct 2020 12:50:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41106c6a476cf9666c6d8c3c853c982a841c29db05b3ef8a072baba537b6d74c`  
		Last Modified: Wed, 14 Oct 2020 12:50:48 GMT  
		Size: 34.3 MB (34312667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6d6258831f87f3b455e6316e2bed430465a760272614de7cdd28c7c6e9f3e`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e3f66638c4d5ce9adba16e49844f57efbab1d628d9d6c73133511b7c1c3892`  
		Last Modified: Wed, 14 Oct 2020 12:50:20 GMT  
		Size: 310.5 KB (310525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b65f2758ea5232d6bc01e6875273a27b4aa314da812aea53f2ace147af0f2ee`  
		Last Modified: Fri, 06 Nov 2020 19:36:08 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ffb000b6c530dba17d2dc89d6d422dd685c769460fa9b099632f38ac274eb7`  
		Last Modified: Fri, 06 Nov 2020 19:36:39 GMT  
		Size: 138.1 MB (138068350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed05f7fff3bafb8e4575dbfbc92e610ce6bdd071af7a6ec7b20e2515673cf81a`  
		Last Modified: Fri, 06 Nov 2020 19:36:08 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70ca33e2a730442b4108eeae100870b290e2d0a052447fb9059801468e38ed9`  
		Last Modified: Fri, 06 Nov 2020 20:00:28 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2126c6c5e8fa28835cfc8550d9d5c229c476475c8d698e64baf795a64fd1d48`  
		Last Modified: Fri, 06 Nov 2020 20:00:24 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7fea06a90685518f088281500c07b882bcb8fbe8fa9d1e584af96ee717980e`  
		Last Modified: Fri, 06 Nov 2020 20:00:25 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328fafca0d5cc18716f970b0566b39b44e21b6290756807abce69698af498ee2`  
		Last Modified: Fri, 06 Nov 2020 20:00:24 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a84c7d7085286af149bc562060f751ed259e474c091926f0c60e329d5d357d3`  
		Last Modified: Fri, 06 Nov 2020 20:00:31 GMT  
		Size: 6.2 MB (6158653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daca7754522a4a1e0a75210e76d833ac36b9fbf9346d45ab0918376f91551fe`  
		Last Modified: Fri, 06 Nov 2020 20:00:24 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:bce04d4dc64d43fe52401234630f11d6d789f9362daba179060da98f239c2b17
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5940787096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afdaa0bd8d83a7a2b584382a69ec2f18a666523c1360f1d44b0fd05908e2581`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:31:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:31:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:33:58 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:35:13 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:26:59 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:30:26 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.14.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5f58d41f6f22ce13081cc6118b238a2e540dc6168b3b7e26d786f2ec41a65872'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:30:28 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:55:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:56:00 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:56:01 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 19:56:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:57:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:57:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528ba1d9759adcc464112008fe49672e1f545981d69bab31186587ab32f92138`  
		Last Modified: Wed, 14 Oct 2020 12:51:33 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf4e6180661653575845d30a4d882dea92f395cb540b1cdf91170e9ee58731`  
		Last Modified: Wed, 14 Oct 2020 12:51:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e973f094614bb2cebe16df6f6004c05895ed077151aecdbbd0c476513054fc`  
		Last Modified: Wed, 14 Oct 2020 12:51:25 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089b875ac355097876e23760dd2166f096a8645e312660ffd3c0e617a2df9a0`  
		Last Modified: Wed, 14 Oct 2020 12:51:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a016b666d0691307c6414d84c36eb82de4b2fc4d74dd04c75f632dc3a78c`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 35.0 MB (35016991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4d95d13c0a45aa19a623e51cb112530a589a3a4d15d5c119610f8196912fab`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf8226941bb8f5af9f2be8fdb54da3e3caef344b0061a73e3debde23a55e98f`  
		Last Modified: Wed, 14 Oct 2020 12:51:24 GMT  
		Size: 9.9 MB (9870100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a7b5e81982b422d06b523840fd18e6b6e5b184d47ea305ff904725b3853cb8`  
		Last Modified: Fri, 06 Nov 2020 19:36:52 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427f3b026cc45318f8697c040dd1646b46005eac52b3be81522e34cba785319a`  
		Last Modified: Fri, 06 Nov 2020 19:37:25 GMT  
		Size: 143.2 MB (143230462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813ef258405b5ef014bedde56308d34cacb0b714073d47bf4d8b43c8910ff0d5`  
		Last Modified: Fri, 06 Nov 2020 19:36:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cf5d73a6f4425f1e8af2f834c49c968d643591feda8f8876e0869f62bb7a41`  
		Last Modified: Fri, 06 Nov 2020 20:00:43 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba001530bf09d3a214b5fbaf3bfec24d3d40a280372557ef3870930eed84eb9`  
		Last Modified: Fri, 06 Nov 2020 20:00:40 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeedc424c29cce6cf2f3ceddd9cd56e33e0f19a92c78551c77ce47fcc34e8b57`  
		Last Modified: Fri, 06 Nov 2020 20:00:40 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58bddf0991e8e090179b3140a743325df776a505be211e8a1ae9ede1e34de6b`  
		Last Modified: Fri, 06 Nov 2020 20:00:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b5cc430f866c231661517a4008b761f055ffeb4e2ecc154076c259acec3d35`  
		Last Modified: Fri, 06 Nov 2020 20:00:43 GMT  
		Size: 11.3 MB (11302867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6517d103a658f141c8253a2c02e8f9e360464ce9e118806a2908bdc972b6b4`  
		Last Modified: Fri, 06 Nov 2020 20:00:40 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-builder-alpine`

```console
$ docker pull caddy@sha256:491af2223daa638936bca9f1dbbe14eb3e73a973784401fdab2ec2d220498048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.1.1-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:8cdf9805f8ee2effcfbf85d38a73de2e403d76c9776b2f58b5e1bdcf0006c5e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119980569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febc6237a0bf9eedcc6a574d23443701faa31ca65f424315f6bf18e84245a6b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:34:56 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:34:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:34:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:39:34 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:42:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:42:13 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:42:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:42:15 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:18:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:18:02 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:18:02 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 21:18:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:18:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:18:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:18:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7d3d256c8367c41c431143c63d083a25dd62ec9ee9d9773dd9e6c7b70ec9e`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9db76c5a1d06710ed4f3073476b2d883ff8e911f8e47c558bc4a8d1d8663fa`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48409b4593ac14b4d18a7ad560244a8940ea07c979696ee49974119d814de59`  
		Last Modified: Fri, 06 Nov 2020 19:50:32 GMT  
		Size: 107.2 MB (107185138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dae78a39a60068885ae0b61f535b899a1201348f12f94ae869dedee1d48dc0`  
		Last Modified: Fri, 06 Nov 2020 19:49:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a28bc188dc0e57f523fcc33cd05c3a40e99022e7ed703613edc6709f4694d`  
		Last Modified: Fri, 06 Nov 2020 21:18:30 GMT  
		Size: 8.3 MB (8309872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba47cc29a2a07b08764e865981321e8cdf4c203c5b9fdc5d2f60acef03d55de`  
		Last Modified: Fri, 06 Nov 2020 21:18:29 GMT  
		Size: 1.4 MB (1407205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f1af179205f9fd430048ae729134c5828b82b24ac6c53c19f7aa669b43069`  
		Last Modified: Fri, 06 Nov 2020 21:18:29 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6e03ac44e32d0122ec224b4c74ff4e0127a5a40612429b1d6ff28a8c0f71de7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115652045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0222914f93ab21dd162769f1412a248f51fca10be55eb3d7bf12b3d431114bb0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:07:24 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:07:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:56:33 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 18:59:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:59:13 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:59:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:59:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:59:18 GMT
WORKDIR /go
# Fri, 06 Nov 2020 19:22:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 19:22:26 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:22:27 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 19:22:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 19:22:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 19:22:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20cc27a60e8ac1bf56dec787d3d52ba856e657179cfd56050036db79abb4267`  
		Last Modified: Thu, 22 Oct 2020 05:34:55 GMT  
		Size: 281.0 KB (280971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecce92c3d2de40638d73e682dec26c2b79a055e85c8d70b88f4ccb9485bb9c9`  
		Last Modified: Thu, 22 Oct 2020 05:34:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c84eb6f64c07ea29969461f90aba8c1beaf51c214bf245baac9ccc85c1d33da`  
		Last Modified: Fri, 06 Nov 2020 19:05:01 GMT  
		Size: 103.5 MB (103512267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdf75f59bedadb379f5e8756bc99336e96050855587837452d72eaf918c3b8c`  
		Last Modified: Fri, 06 Nov 2020 19:04:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd9d45b83e45ca8a5cdb6ac3e3b80d78efb0119790a01aa468e1bb0c761463e`  
		Last Modified: Fri, 06 Nov 2020 19:23:25 GMT  
		Size: 7.9 MB (7928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016a22366d0714e29a48006a63b3492a8961d099c64cc358a44411181a3699eb`  
		Last Modified: Fri, 06 Nov 2020 19:23:22 GMT  
		Size: 1.3 MB (1327349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0d1bd89e3d5467a79c8b80301f79bf8033129da43cd4c72e489213f7cbf229`  
		Last Modified: Fri, 06 Nov 2020 19:23:24 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:b258fde47854d7b0285263610f5c6b9ffb6f06f3a780f6cfaa1a2863495b76fd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114436919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ec4c012233a9aefd5e4aa0669e15e3d8e1cfa9cf9d6c0c36fb1a8bff795c05`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:21:35 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:23:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:23:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:43:07 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:45:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:45:16 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:45:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:45:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:45:19 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:27:11 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:27:12 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:27:13 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 20:27:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:27:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:27:18 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:27:19 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b753cfc04fdce9640aac1e7a4b3e7ce15fa60b8e357376e42f294f463a6e890`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 280.1 KB (280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90c422e5e4668cb4140aadb622d734faa93c81cc1e283da9b08bbbc65c45c5`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd774dd42f20c72b2335aa86df0dcc76905d1a383bde3112f60f378ed6d5723c`  
		Last Modified: Fri, 06 Nov 2020 19:51:32 GMT  
		Size: 103.3 MB (103279793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87040eea28146abacdfa46238d6cf7ef9ec51038c04f53bdc9796a19455a82bf`  
		Last Modified: Fri, 06 Nov 2020 19:51:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f628e6ce0af305e50899cbe69dc0cde182ce627be5f4f2f742e4e4d3aa655ddb`  
		Last Modified: Fri, 06 Nov 2020 20:27:58 GMT  
		Size: 7.1 MB (7144806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecae0064d644c67a7e9b4772602b5194d033a53ad75183941bcd7aaef30216f`  
		Last Modified: Fri, 06 Nov 2020 20:27:57 GMT  
		Size: 1.3 MB (1325849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6af0e7d5ff1fe239f9dac42c70236ac44dc14b54544d68bc9198fae3976a731`  
		Last Modified: Fri, 06 Nov 2020 20:27:57 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:98e85c3ec782158255bf07c86cf4ddc1af17f27714e3db27f96ba9e4813627a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115389072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959b60761716890807f31a405129cd97f761ae14a7a9c45e3dcce972c20196bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:08:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 04:09:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:09:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:22:27 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:24:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:24:21 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:24:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:24:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:24:24 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:09:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:09:09 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:09:09 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 21:09:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:09:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:09:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:09:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4357932f1b6fb010e1461cc5c673712fb832ac44ee627c691db0b64adf95d13`  
		Last Modified: Thu, 22 Oct 2020 04:28:32 GMT  
		Size: 281.2 KB (281230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c013af1878066e59b688e31fd962e7267430963de27c5257241e3c223aa1d6`  
		Last Modified: Thu, 22 Oct 2020 04:28:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77e4c4323cac205b0e0648168654eeab6f1d9ea388b2015cbc59650af632f62`  
		Last Modified: Fri, 06 Nov 2020 19:30:36 GMT  
		Size: 102.6 MB (102590506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68f5aacb416a2fa6d097869ed282ee7821d32ed2a401bb9b859b1ebd97a2122`  
		Last Modified: Fri, 06 Nov 2020 19:29:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eff0fc08530c920c358100c2a0cb516e6786ed8b58dd0e4942511f0742c18d`  
		Last Modified: Fri, 06 Nov 2020 21:09:50 GMT  
		Size: 8.5 MB (8499886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f028f5696a14b2a25eda02fed36563bbd062875533c28bda40befbe94b745bb`  
		Last Modified: Fri, 06 Nov 2020 21:09:49 GMT  
		Size: 1.3 MB (1310181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b381b359844b948cbaf36687576d6edffc27fe51080622429028d41957161`  
		Last Modified: Fri, 06 Nov 2020 21:09:48 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:599fb5e07848cdb565aff8218812de0ab0356ca4f4e494ac54b4b76f3b665ba6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114750254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3220c299d6244b3e456c75c7df025f07001fd35feb0bd0f9e78cecf81f300107`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:27:26 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 13:27:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:27:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:37:07 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 18:39:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:39:50 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:39:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:40:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:40:09 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:49:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:49:53 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:50:02 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 21:50:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:50:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:50:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:50:37 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9900411dc7c8c88618743573bf89478d726007403bd002d8b00d21b7fecd40a`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 283.2 KB (283205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbd106374e3baf7eb8e3d8f7ffd4c364a35e57dcb3a89f8a153327a4c3fa3f9`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b4aa7e1e5dc7bf7676d23c31004345d0d9caccb847a614fdf0c0db9247a1af`  
		Last Modified: Fri, 06 Nov 2020 18:48:27 GMT  
		Size: 101.5 MB (101455314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bbeeae924df02f9094e25dd06eab3287fb50dd3911b39fd970d38a33e8fc59`  
		Last Modified: Fri, 06 Nov 2020 18:48:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2676d8220c83008613c392a60f715be838ffca488f7c01fd29c18983a9b20e`  
		Last Modified: Fri, 06 Nov 2020 21:52:14 GMT  
		Size: 8.9 MB (8920011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62236f2f9f55cef8f0f51973bb8fc73f9ca395d0c6e5cf984f0ee9d8eddd016d`  
		Last Modified: Fri, 06 Nov 2020 21:52:12 GMT  
		Size: 1.3 MB (1287789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1cb6b56b91c30f2dd1f54a71d24e3e4a6c8999da1bc1e2537d393fa6a269c8`  
		Last Modified: Fri, 06 Nov 2020 21:52:11 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:b738347a37a68d64dbee00f6d4bf271000afe0693211228649ae5ac8c58ca056
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119637445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007c80af833d86fee3681b4e7735f66fba05e751e43192c9a7797415a3eb58d9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:53:28 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 02:53:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:53:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:27:26 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:30:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.11.src.tar.gz'; 	sha256='1871f3d29b0cf1ebb739c9b134c9bc559282bd3625856e5f12f5aea29ab70f16'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:30:13 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:30:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:30:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:30:15 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:39:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:39:47 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:39:47 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 20:39:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:39:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:39:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5139d7663b8674a989574c2161166fb137f26ef16b2f701159c126628be75101`  
		Last Modified: Thu, 22 Oct 2020 02:58:32 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31a06258ad66efe2dedbf67809ebc107a55757b8a4543af77982f55ff6c067`  
		Last Modified: Thu, 22 Oct 2020 02:58:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02a44448cd0d67bcfdbc04c5583bad139970194e2795ad8699b66da2238ed9d`  
		Last Modified: Fri, 06 Nov 2020 19:35:17 GMT  
		Size: 107.0 MB (107048570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4810a62791e651c5fd7242cc42273cb38f14590dfb699cef7c9fdb4ba531fa19`  
		Last Modified: Fri, 06 Nov 2020 19:35:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e36381debf2397a3a5b23905fc4109ad02a1675d793b1f222be94936b3e5bf9`  
		Last Modified: Fri, 06 Nov 2020 20:40:38 GMT  
		Size: 8.4 MB (8352213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a7aaf2223f223857df02983b33e17c5c450bbd7109e70f7a6ebf06f070932`  
		Last Modified: Fri, 06 Nov 2020 20:40:36 GMT  
		Size: 1.4 MB (1388754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf7c2cb4c0878e3ae5dd253020a4f3e59eba612bfcd7c8b9ac2d167da983cbd`  
		Last Modified: Fri, 06 Nov 2020 20:40:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:17a3059abfe11f58c1ac956339f327d7a94e6b34c596b94014b655661ba6d1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:2.1.1-builder-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:4bca501cd66dbb0f3114b28b14abe636d063dd9b0119af54dcef494a80df8b1e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2552955192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3d49f4bc529f061eb9dd7cea4bb34cec257265b56208df8e5528b0c36c964e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:27:03 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:27:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:28:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:28:38 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:29:02 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:24:16 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:26:41 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.14.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5f58d41f6f22ce13081cc6118b238a2e540dc6168b3b7e26d786f2ec41a65872'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:26:43 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:55:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:55:21 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:55:22 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 19:55:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:55:51 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:55:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23a75d88f9f5980bb112e2c28248975f107144d8d2e40dc4755e2a09f5e56df`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea6d8b9d9b014ffa471b7bb8882ddb7e9d378ddcacc099f0710073bd6361b9`  
		Last Modified: Wed, 14 Oct 2020 12:50:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75c1905c0573cc5706bc066d23624f0e92a8871832c744fbe7eabdcbc6f8a85`  
		Last Modified: Wed, 14 Oct 2020 12:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938695376d9deeba8819539ff3245935c28f93229d1c332bb8b6a16e67013fbc`  
		Last Modified: Wed, 14 Oct 2020 12:50:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41106c6a476cf9666c6d8c3c853c982a841c29db05b3ef8a072baba537b6d74c`  
		Last Modified: Wed, 14 Oct 2020 12:50:48 GMT  
		Size: 34.3 MB (34312667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6d6258831f87f3b455e6316e2bed430465a760272614de7cdd28c7c6e9f3e`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e3f66638c4d5ce9adba16e49844f57efbab1d628d9d6c73133511b7c1c3892`  
		Last Modified: Wed, 14 Oct 2020 12:50:20 GMT  
		Size: 310.5 KB (310525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b65f2758ea5232d6bc01e6875273a27b4aa314da812aea53f2ace147af0f2ee`  
		Last Modified: Fri, 06 Nov 2020 19:36:08 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ffb000b6c530dba17d2dc89d6d422dd685c769460fa9b099632f38ac274eb7`  
		Last Modified: Fri, 06 Nov 2020 19:36:39 GMT  
		Size: 138.1 MB (138068350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed05f7fff3bafb8e4575dbfbc92e610ce6bdd071af7a6ec7b20e2515673cf81a`  
		Last Modified: Fri, 06 Nov 2020 19:36:08 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70ca33e2a730442b4108eeae100870b290e2d0a052447fb9059801468e38ed9`  
		Last Modified: Fri, 06 Nov 2020 20:00:28 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2126c6c5e8fa28835cfc8550d9d5c229c476475c8d698e64baf795a64fd1d48`  
		Last Modified: Fri, 06 Nov 2020 20:00:24 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7fea06a90685518f088281500c07b882bcb8fbe8fa9d1e584af96ee717980e`  
		Last Modified: Fri, 06 Nov 2020 20:00:25 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328fafca0d5cc18716f970b0566b39b44e21b6290756807abce69698af498ee2`  
		Last Modified: Fri, 06 Nov 2020 20:00:24 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a84c7d7085286af149bc562060f751ed259e474c091926f0c60e329d5d357d3`  
		Last Modified: Fri, 06 Nov 2020 20:00:31 GMT  
		Size: 6.2 MB (6158653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5daca7754522a4a1e0a75210e76d833ac36b9fbf9346d45ab0918376f91551fe`  
		Last Modified: Fri, 06 Nov 2020 20:00:24 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:78fd85ed2a26ec60289a288d3e2c20b5e7b62643941ec5aaf8626124422680f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.1.1-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:bce04d4dc64d43fe52401234630f11d6d789f9362daba179060da98f239c2b17
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5940787096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afdaa0bd8d83a7a2b584382a69ec2f18a666523c1360f1d44b0fd05908e2581`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:31:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:31:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:33:58 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:35:13 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:26:59 GMT
ENV GOLANG_VERSION=1.14.11
# Fri, 06 Nov 2020 19:30:26 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.14.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5f58d41f6f22ce13081cc6118b238a2e540dc6168b3b7e26d786f2ec41a65872'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:30:28 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:55:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:56:00 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:56:01 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 06 Nov 2020 19:56:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:57:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:57:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528ba1d9759adcc464112008fe49672e1f545981d69bab31186587ab32f92138`  
		Last Modified: Wed, 14 Oct 2020 12:51:33 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf4e6180661653575845d30a4d882dea92f395cb540b1cdf91170e9ee58731`  
		Last Modified: Wed, 14 Oct 2020 12:51:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e973f094614bb2cebe16df6f6004c05895ed077151aecdbbd0c476513054fc`  
		Last Modified: Wed, 14 Oct 2020 12:51:25 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089b875ac355097876e23760dd2166f096a8645e312660ffd3c0e617a2df9a0`  
		Last Modified: Wed, 14 Oct 2020 12:51:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a016b666d0691307c6414d84c36eb82de4b2fc4d74dd04c75f632dc3a78c`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 35.0 MB (35016991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4d95d13c0a45aa19a623e51cb112530a589a3a4d15d5c119610f8196912fab`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf8226941bb8f5af9f2be8fdb54da3e3caef344b0061a73e3debde23a55e98f`  
		Last Modified: Wed, 14 Oct 2020 12:51:24 GMT  
		Size: 9.9 MB (9870100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a7b5e81982b422d06b523840fd18e6b6e5b184d47ea305ff904725b3853cb8`  
		Last Modified: Fri, 06 Nov 2020 19:36:52 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427f3b026cc45318f8697c040dd1646b46005eac52b3be81522e34cba785319a`  
		Last Modified: Fri, 06 Nov 2020 19:37:25 GMT  
		Size: 143.2 MB (143230462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813ef258405b5ef014bedde56308d34cacb0b714073d47bf4d8b43c8910ff0d5`  
		Last Modified: Fri, 06 Nov 2020 19:36:52 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cf5d73a6f4425f1e8af2f834c49c968d643591feda8f8876e0869f62bb7a41`  
		Last Modified: Fri, 06 Nov 2020 20:00:43 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba001530bf09d3a214b5fbaf3bfec24d3d40a280372557ef3870930eed84eb9`  
		Last Modified: Fri, 06 Nov 2020 20:00:40 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeedc424c29cce6cf2f3ceddd9cd56e33e0f19a92c78551c77ce47fcc34e8b57`  
		Last Modified: Fri, 06 Nov 2020 20:00:40 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58bddf0991e8e090179b3140a743325df776a505be211e8a1ae9ede1e34de6b`  
		Last Modified: Fri, 06 Nov 2020 20:00:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b5cc430f866c231661517a4008b761f055ffeb4e2ecc154076c259acec3d35`  
		Last Modified: Fri, 06 Nov 2020 20:00:43 GMT  
		Size: 11.3 MB (11302867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6517d103a658f141c8253a2c02e8f9e360464ce9e118806a2908bdc972b6b4`  
		Last Modified: Fri, 06 Nov 2020 20:00:40 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-windowsservercore`

```console
$ docker pull caddy@sha256:f896aef1c898fbc3327acd681f132b4ad3ec5ac8ffffbad596a9b8ff1868968c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.1.1-windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:66f70d738fddf55c60091b6aef8e41b63c76802b802ab717413fe9c818037124
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401370099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1397040752ad41e2b18db058da0b7e519033692fcea840d807a898de17943dde`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 20:55:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 20:55:53 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 20:56:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 20:56:28 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 20:56:29 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 20:56:30 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 20:56:30 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 20:56:31 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 14 Oct 2020 20:56:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:56:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:56:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:56:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:56:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:56:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:56:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:56:37 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:56:38 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:56:39 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:56:55 GMT
RUN caddy version
# Wed, 14 Oct 2020 20:56:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b188d60ff330af293d4e64c0e8d02efc672b84164a7f28c2b88c6fa69e773b`  
		Last Modified: Wed, 14 Oct 2020 21:11:59 GMT  
		Size: 9.2 MB (9238100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7cca4341580aaef49dda3a35fbe74dea069dea552f29d609095c28ae31c7c9`  
		Last Modified: Wed, 14 Oct 2020 21:11:55 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc6acc9f3a56b460718597090a53b19d8ae56936b8c1f305a0fc5b6c8ae834`  
		Last Modified: Wed, 14 Oct 2020 21:12:01 GMT  
		Size: 17.7 MB (17721908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da2dbe8389d72a6c47be48a14049de1017ecd0bfe42e9b39137feb681a86e2`  
		Last Modified: Wed, 14 Oct 2020 21:11:55 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08f4acb6066947f91cc9e9472c80e0f37f13d618d651351b8b3d6efd0d972d9`  
		Last Modified: Wed, 14 Oct 2020 21:11:54 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc07733f0dbd5754df935d2dd9eb9b99ec6a8833f5801ce1d28dfbd5dc06537d`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f794342b0d24d7695630534ed119afcfd13154a5661e49b0fb63a9d09239389`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f8231f3a84092e779185d6075769d2024c8ca7743081f3c9da45468d7f3550`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e35f7ff6908cb027518acbf4190fa1665763a290334d11445f85785ee2b6eb6`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a6ac3896b488a27e5a2289f4a62b934db8638756d02666690ff6e80621f0b3`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fa5374e20ab60dd6a7d2bdd71a4996a10f825e28542c0a038a25b5bc64fc10`  
		Last Modified: Wed, 14 Oct 2020 21:11:49 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f8e08e4c4e4262e9a897ff6a2366db843c277188a19522c2b3a238a70d2e92`  
		Last Modified: Wed, 14 Oct 2020 21:11:49 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309bc178193a0f7b99147d5aabc6bfb9a799756c1893656a74c945570438c75`  
		Last Modified: Wed, 14 Oct 2020 21:11:48 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c0747bfbf50db12f814e3dea2b3a71b1bb951fc8f401365199cf535793880b`  
		Last Modified: Wed, 14 Oct 2020 21:11:49 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492e7f435eff381b7d6b25eb81362a6c0fd4b461ddc05978afdfaf175ff99756`  
		Last Modified: Wed, 14 Oct 2020 21:11:48 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5be9e7e60f33a1a982e2fd5a12de9103b8c6c763d561b14577abf49c36209`  
		Last Modified: Wed, 14 Oct 2020 21:11:45 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705ffea3945c47a37e15327ec3683dbc90a9e05a214b10f7384f782dd4d066c`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59c3c8fe6d1b33da8d76616405e7bf142019d8d8e2a5d372496773d29a50f5`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e00a541946fdd8a1f98a5d34d51dca7bd037860ba1aa2a85c978213e80d25f`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 299.5 KB (299487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17888b1c5a918fe0001ed5ea3f284e619eaa9c54b6de64d7f8def19bc9a4f7f7`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:3df3617581091c8a721884e7886ef930f68708e6be320bd2252ef6f490f2512e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5774462347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc16ee492900dee7e9f4e124e5439d5a2a26376ffe0e4c4b85461f0907b2abf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 20:58:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 20:58:30 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 20:59:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:00:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:00:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:00:03 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:00:04 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:00:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 14 Oct 2020 21:00:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:00:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:00:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:00:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:00:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:00:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:00:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:00:11 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:00:11 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:00:12 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:00:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:00:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0621c6e14481e8b7931a54a60b5f552ab50344f6a75362eb856e08a00a6e121d`  
		Last Modified: Wed, 14 Oct 2020 21:12:28 GMT  
		Size: 9.9 MB (9924480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4a1346a3116e78ed00103d93f985d7f4bf3df06cb8088bca9b316cc656a1b8`  
		Last Modified: Wed, 14 Oct 2020 21:12:24 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828c93647c40ffc8bcbe621b61aef3677861ae673ef3b66ac1792c99c95234d9`  
		Last Modified: Wed, 14 Oct 2020 21:12:30 GMT  
		Size: 22.9 MB (22896440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4726960f8ff938227c56d540f881d9bc18e607f3301cd3cead8b652ec7ef517`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5e13596b93a65158bebc3e1cfb8345e098bd9a27f4171069026fc575224d8`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06356772b928f71cb618db080d52bdca9588cf499ea10913136623ea3c89ac9d`  
		Last Modified: Wed, 14 Oct 2020 21:12:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35687f4e534a86ba4f3538c39b22db8a401bc0335da0a91c471f9eff0e934abd`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0234c902cd868cb06435cb99ba8470182d7955305dd550a6f9e85dfdbf0589`  
		Last Modified: Wed, 14 Oct 2020 21:12:18 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdc33faacf12c704737e72c800eaa28e3da94d8ed7df679e786358a09d471bf`  
		Last Modified: Wed, 14 Oct 2020 21:12:18 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f0814377cdb217e3609cccb0c763feeab8b5f8a35b447a95dfd89ed1cad48`  
		Last Modified: Wed, 14 Oct 2020 21:12:17 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c94837bff217cff65168fc6eebe67956699dbee13427803f6970aa8f224dc10`  
		Last Modified: Wed, 14 Oct 2020 21:12:16 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d2486511a0c9601a2bdd89e2ebd54297bb2c78735b569e84014aa00cfb6d3`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1435a16a8f89084f597da43cb9ce1413ac817712fad3e6683dd165dc7cc36296`  
		Last Modified: Wed, 14 Oct 2020 21:12:14 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9479319b79d0a97d0b6d91034585fb6f52136095829c563c4b36d57bdfe54c23`  
		Last Modified: Wed, 14 Oct 2020 21:12:15 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f84c09f0f902199fdd83bb5ec0da426140430cf1ae9b37d63635d70b45ddad`  
		Last Modified: Wed, 14 Oct 2020 21:12:13 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c89752e1d722e1a2bdb8c5936cbf20f3ca2c699136b1279ac27f93b75110cf`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b75e4a8389cdb23c1d9ebf7fc2e685469542f5e1ac0f7a32e1818e04001d88`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58bcc9da6dff9ee1073dd37c941b628f26ee80400f5a9e8c2bbbd8749815c42`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46327701e2d8e59d0173f0db37999a9d1e633a41f36e739bfe94a37c34406aee`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 269.3 KB (269317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd16f3084947685df6d6043025f0d44efccb637918ffc69bbebafea7e3c94970`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-windowsservercore-1809`

```console
$ docker pull caddy@sha256:f2ae6026ebddfb02e729d888f5b5399c0bd6cbb64fe2412afc29ee983cdeaa30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:2.1.1-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:66f70d738fddf55c60091b6aef8e41b63c76802b802ab717413fe9c818037124
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401370099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1397040752ad41e2b18db058da0b7e519033692fcea840d807a898de17943dde`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 20:55:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 20:55:53 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 20:56:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 20:56:28 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 20:56:29 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 20:56:30 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 20:56:30 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 20:56:31 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 14 Oct 2020 20:56:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:56:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:56:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:56:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:56:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:56:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:56:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:56:37 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:56:38 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:56:39 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:56:55 GMT
RUN caddy version
# Wed, 14 Oct 2020 20:56:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b188d60ff330af293d4e64c0e8d02efc672b84164a7f28c2b88c6fa69e773b`  
		Last Modified: Wed, 14 Oct 2020 21:11:59 GMT  
		Size: 9.2 MB (9238100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7cca4341580aaef49dda3a35fbe74dea069dea552f29d609095c28ae31c7c9`  
		Last Modified: Wed, 14 Oct 2020 21:11:55 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc6acc9f3a56b460718597090a53b19d8ae56936b8c1f305a0fc5b6c8ae834`  
		Last Modified: Wed, 14 Oct 2020 21:12:01 GMT  
		Size: 17.7 MB (17721908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da2dbe8389d72a6c47be48a14049de1017ecd0bfe42e9b39137feb681a86e2`  
		Last Modified: Wed, 14 Oct 2020 21:11:55 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08f4acb6066947f91cc9e9472c80e0f37f13d618d651351b8b3d6efd0d972d9`  
		Last Modified: Wed, 14 Oct 2020 21:11:54 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc07733f0dbd5754df935d2dd9eb9b99ec6a8833f5801ce1d28dfbd5dc06537d`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f794342b0d24d7695630534ed119afcfd13154a5661e49b0fb63a9d09239389`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f8231f3a84092e779185d6075769d2024c8ca7743081f3c9da45468d7f3550`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e35f7ff6908cb027518acbf4190fa1665763a290334d11445f85785ee2b6eb6`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a6ac3896b488a27e5a2289f4a62b934db8638756d02666690ff6e80621f0b3`  
		Last Modified: Wed, 14 Oct 2020 21:11:52 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fa5374e20ab60dd6a7d2bdd71a4996a10f825e28542c0a038a25b5bc64fc10`  
		Last Modified: Wed, 14 Oct 2020 21:11:49 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f8e08e4c4e4262e9a897ff6a2366db843c277188a19522c2b3a238a70d2e92`  
		Last Modified: Wed, 14 Oct 2020 21:11:49 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309bc178193a0f7b99147d5aabc6bfb9a799756c1893656a74c945570438c75`  
		Last Modified: Wed, 14 Oct 2020 21:11:48 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c0747bfbf50db12f814e3dea2b3a71b1bb951fc8f401365199cf535793880b`  
		Last Modified: Wed, 14 Oct 2020 21:11:49 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492e7f435eff381b7d6b25eb81362a6c0fd4b461ddc05978afdfaf175ff99756`  
		Last Modified: Wed, 14 Oct 2020 21:11:48 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5be9e7e60f33a1a982e2fd5a12de9103b8c6c763d561b14577abf49c36209`  
		Last Modified: Wed, 14 Oct 2020 21:11:45 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705ffea3945c47a37e15327ec3683dbc90a9e05a214b10f7384f782dd4d066c`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59c3c8fe6d1b33da8d76616405e7bf142019d8d8e2a5d372496773d29a50f5`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e00a541946fdd8a1f98a5d34d51dca7bd037860ba1aa2a85c978213e80d25f`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 299.5 KB (299487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17888b1c5a918fe0001ed5ea3f284e619eaa9c54b6de64d7f8def19bc9a4f7f7`  
		Last Modified: Wed, 14 Oct 2020 21:11:46 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:c300df341bc8b99cf983b6073f4bbf660ec3d1b4047cb274e3e00c5b19e26128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.1.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:3df3617581091c8a721884e7886ef930f68708e6be320bd2252ef6f490f2512e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5774462347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc16ee492900dee7e9f4e124e5439d5a2a26376ffe0e4c4b85461f0907b2abf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 20:58:29 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 20:58:30 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 20:59:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:00:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:00:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:00:03 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:00:04 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:00:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 14 Oct 2020 21:00:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:00:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:00:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:00:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:00:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:00:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:00:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:00:11 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:00:11 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:00:12 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:00:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:00:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0621c6e14481e8b7931a54a60b5f552ab50344f6a75362eb856e08a00a6e121d`  
		Last Modified: Wed, 14 Oct 2020 21:12:28 GMT  
		Size: 9.9 MB (9924480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4a1346a3116e78ed00103d93f985d7f4bf3df06cb8088bca9b316cc656a1b8`  
		Last Modified: Wed, 14 Oct 2020 21:12:24 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828c93647c40ffc8bcbe621b61aef3677861ae673ef3b66ac1792c99c95234d9`  
		Last Modified: Wed, 14 Oct 2020 21:12:30 GMT  
		Size: 22.9 MB (22896440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4726960f8ff938227c56d540f881d9bc18e607f3301cd3cead8b652ec7ef517`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5e13596b93a65158bebc3e1cfb8345e098bd9a27f4171069026fc575224d8`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06356772b928f71cb618db080d52bdca9588cf499ea10913136623ea3c89ac9d`  
		Last Modified: Wed, 14 Oct 2020 21:12:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35687f4e534a86ba4f3538c39b22db8a401bc0335da0a91c471f9eff0e934abd`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0234c902cd868cb06435cb99ba8470182d7955305dd550a6f9e85dfdbf0589`  
		Last Modified: Wed, 14 Oct 2020 21:12:18 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdc33faacf12c704737e72c800eaa28e3da94d8ed7df679e786358a09d471bf`  
		Last Modified: Wed, 14 Oct 2020 21:12:18 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f0814377cdb217e3609cccb0c763feeab8b5f8a35b447a95dfd89ed1cad48`  
		Last Modified: Wed, 14 Oct 2020 21:12:17 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c94837bff217cff65168fc6eebe67956699dbee13427803f6970aa8f224dc10`  
		Last Modified: Wed, 14 Oct 2020 21:12:16 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d2486511a0c9601a2bdd89e2ebd54297bb2c78735b569e84014aa00cfb6d3`  
		Last Modified: Wed, 14 Oct 2020 21:12:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1435a16a8f89084f597da43cb9ce1413ac817712fad3e6683dd165dc7cc36296`  
		Last Modified: Wed, 14 Oct 2020 21:12:14 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9479319b79d0a97d0b6d91034585fb6f52136095829c563c4b36d57bdfe54c23`  
		Last Modified: Wed, 14 Oct 2020 21:12:15 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f84c09f0f902199fdd83bb5ec0da426140430cf1ae9b37d63635d70b45ddad`  
		Last Modified: Wed, 14 Oct 2020 21:12:13 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c89752e1d722e1a2bdb8c5936cbf20f3ca2c699136b1279ac27f93b75110cf`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b75e4a8389cdb23c1d9ebf7fc2e685469542f5e1ac0f7a32e1818e04001d88`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58bcc9da6dff9ee1073dd37c941b628f26ee80400f5a9e8c2bbbd8749815c42`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46327701e2d8e59d0173f0db37999a9d1e633a41f36e739bfe94a37c34406aee`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 269.3 KB (269317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd16f3084947685df6d6043025f0d44efccb637918ffc69bbebafea7e3c94970`  
		Last Modified: Wed, 14 Oct 2020 21:12:11 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1`

```console
$ docker pull caddy@sha256:b44006ca7a107edd0fca2ff7a70cf75b81b20b61b722dff8a720364a3764ffd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.2.1` - linux; amd64

```console
$ docker pull caddy@sha256:4ebad49f78a3f98164d89431978046ee6e94f1e8a70454abc7f49ce1a5ee7826
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb0137bab0e21a92b0bc9ec1cc22c259b097d5bf239b161ae1eac0de1833e67`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:33:22 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 04:33:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 04:33:55 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 04:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 04:34:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 04:34:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 04:34:02 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 04:34:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 80
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 443
# Thu, 22 Oct 2020 04:34:06 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 04:34:06 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 04:34:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e2d825895b6421ca5dbd63db0d99f790ef84a84c7bcaff51e60b654397858`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 300.0 KB (299956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaf2e3dee2e74b401fce928bf9502e48df68da4e8c1933bfd6b00b1137529fc`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 5.8 KB (5754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2215cf93250599c5db984cee0fddd5d0cd59ef035ab5a317387b67211bde86d`  
		Last Modified: Thu, 22 Oct 2020 04:35:06 GMT  
		Size: 11.5 MB (11532508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060365e49ba5ee96a2859e269b366f5a5c9f386e5bdbf07d2ef31b1fc6934baa`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - linux; arm variant v6

```console
$ docker pull caddy@sha256:abba73dc860b2f35703cb7d27f08baf5bfc084e18e627b94661d01a8e2befdaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13784259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0aad5a281913821dd39ffed5e144daae22ac81ac4314731395ab65eedde72a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:58:10 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:58:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:58:46 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:58:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:58:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:59:00 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:59:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:59:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:59:03 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:59:08 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:59:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:59:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:59:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:59:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:59:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:59:15 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:59:19 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:59:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:59:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:59:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7369c3ac4b39c55c74e96dd3eb61ac2fa65e5671b1c2acca9697a7c9d20c3cf`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 300.1 KB (300086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8f4045920069dff3382a5993783c5d846d9e28d0f5a63c475ed298fce0abb7`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db6bde4735da15e5db23ad62f3d64d78aed8713a40d12547f5538c15c90f9da`  
		Last Modified: Thu, 22 Oct 2020 03:00:06 GMT  
		Size: 10.9 MB (10876280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a95efd7a14ed98a53a238da45faa7e3b0fdd2a93529b83bfe9d0823dafac67c`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8cf66cbe3c03273ca54bdab908092a6a9b9f02d39595ed15b1111f1465430426
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20723dea614fc40d9f3cb59eddd33bf0e89dfda3f8ed4a7b404ef334632a4b9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:04:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 03:05:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 03:05:45 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 03:05:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 03:05:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 03:05:54 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 03:05:55 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 03:05:56 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 03:05:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 03:06:01 GMT
EXPOSE 80
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 443
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 03:06:03 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 03:06:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a8e7fe5034ac502626b0a921d79be80c092890176e33b236c489d6f00710a2`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 299.2 KB (299211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db75acdaca15b1e81890f29b3b757fcc73e7a69a55f5ed659bf800f6340108`  
		Last Modified: Thu, 22 Oct 2020 03:06:43 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2197c38adf245bca8f229a4cd718c4d0f619a87bae5786572ccdac1a286882c`  
		Last Modified: Thu, 22 Oct 2020 03:06:46 GMT  
		Size: 10.9 MB (10854384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0104bc6a595940856019d00d9ff8e04365338a7964d948b64cc44bf73cc59e`  
		Last Modified: Thu, 22 Oct 2020 03:06:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:da121cf42d1759ed03af3130533d365c365af1d738d550744ad863e05e64cf46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13540356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b4aa38988ab2442575062d99c3cb44976de6c227256c118f35340e7c21c303`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:40:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:40:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:40:57 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:07 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:09 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:10 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:10 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbde357077a97c0f831033bf03c9828203cb7e3e6cb33217ce4d7cfd71c931`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 300.3 KB (300348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a5ab0aa923ce1fe233b904008bbf932c4787f48bcd59f07a85616147b7cbc3`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc398339860cf826624c9c22b5de9b45a193260e2ff24826d210b493483398f`  
		Last Modified: Thu, 22 Oct 2020 02:41:59 GMT  
		Size: 10.5 MB (10527465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6e7d61d1d4a00550447ea1f67edc0463cc527e49356e98959edfafba0df879`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - linux; ppc64le

```console
$ docker pull caddy@sha256:09208042b4d19d7ed87b51b99dc20b390dab20d9ae7e235a62a3af3aaf472bd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13291756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5c77284adc35481d13003d31a866f637b6eaf9f5764f667e536db79ce23129`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:39:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 13:44:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 13:44:04 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 13:44:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 13:44:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:44:33 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 13:44:37 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 13:44:40 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 13:44:44 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 13:44:48 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 13:44:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 13:44:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 13:45:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 13:45:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 13:45:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 13:45:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 13:45:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 13:45:23 GMT
EXPOSE 80
# Thu, 22 Oct 2020 13:45:26 GMT
EXPOSE 443
# Thu, 22 Oct 2020 13:45:30 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 13:45:35 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 13:45:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a4964211b7ce86541a0c1dad8ef3800ec38a3ca90aff94b76759b4cb8e279`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 302.3 KB (302327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dd938ef3e3eae8509deda8fab9ab5f9344169d912e35a802633e799feed1bb`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe23c296ee12ee12ef84dbabbb4f7bf0362a9a12b684782ebd3f44a97c8fcf8e`  
		Last Modified: Thu, 22 Oct 2020 13:47:55 GMT  
		Size: 10.2 MB (10180223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2f3c084745fecafaa9ff33626a81124f2d70267ceee705da555714238bfa1`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - linux; s390x

```console
$ docker pull caddy@sha256:3e18b421d651721239cb3422bc890d1211535681219b7696816f487b4cebc4ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14074857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d5562f1d148d3d67ff7f5995be8f860553ad0f3d07091335643306b83385e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:41:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:41:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:41 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f988ff23f3cbb35bfed69e33f3b7ee69403bfae4f46363a08eea4830053e9c`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 300.5 KB (300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd6a4e0db99510879c5dfceabd1e629a0692c4544bb0da34971f8722b881e92`  
		Last Modified: Thu, 22 Oct 2020 02:42:09 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e13b938aa802e74610585cabba77d625db4baf219f577a81195c272408c7d3`  
		Last Modified: Thu, 22 Oct 2020 02:42:16 GMT  
		Size: 11.2 MB (11202559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a221fff082950a8a98db12eb99f532a39008f0d6e21684bc1aed06fa1ed2a764`  
		Last Modified: Thu, 22 Oct 2020 02:42:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-alpine`

```console
$ docker pull caddy@sha256:ea06de9c9cb10eacb9f77e50817d2ad8dd63c977549f26c19d57df1a194fefdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.2.1-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:4ebad49f78a3f98164d89431978046ee6e94f1e8a70454abc7f49ce1a5ee7826
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb0137bab0e21a92b0bc9ec1cc22c259b097d5bf239b161ae1eac0de1833e67`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:33:22 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 04:33:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 04:33:55 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 04:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 04:34:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 04:34:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 04:34:02 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 04:34:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 80
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 443
# Thu, 22 Oct 2020 04:34:06 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 04:34:06 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 04:34:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e2d825895b6421ca5dbd63db0d99f790ef84a84c7bcaff51e60b654397858`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 300.0 KB (299956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaf2e3dee2e74b401fce928bf9502e48df68da4e8c1933bfd6b00b1137529fc`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 5.8 KB (5754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2215cf93250599c5db984cee0fddd5d0cd59ef035ab5a317387b67211bde86d`  
		Last Modified: Thu, 22 Oct 2020 04:35:06 GMT  
		Size: 11.5 MB (11532508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060365e49ba5ee96a2859e269b366f5a5c9f386e5bdbf07d2ef31b1fc6934baa`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:abba73dc860b2f35703cb7d27f08baf5bfc084e18e627b94661d01a8e2befdaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13784259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0aad5a281913821dd39ffed5e144daae22ac81ac4314731395ab65eedde72a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:58:10 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:58:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:58:46 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:58:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:58:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:59:00 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:59:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:59:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:59:03 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:59:08 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:59:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:59:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:59:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:59:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:59:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:59:15 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:59:19 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:59:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:59:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:59:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7369c3ac4b39c55c74e96dd3eb61ac2fa65e5671b1c2acca9697a7c9d20c3cf`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 300.1 KB (300086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8f4045920069dff3382a5993783c5d846d9e28d0f5a63c475ed298fce0abb7`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db6bde4735da15e5db23ad62f3d64d78aed8713a40d12547f5538c15c90f9da`  
		Last Modified: Thu, 22 Oct 2020 03:00:06 GMT  
		Size: 10.9 MB (10876280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a95efd7a14ed98a53a238da45faa7e3b0fdd2a93529b83bfe9d0823dafac67c`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8cf66cbe3c03273ca54bdab908092a6a9b9f02d39595ed15b1111f1465430426
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20723dea614fc40d9f3cb59eddd33bf0e89dfda3f8ed4a7b404ef334632a4b9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:04:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 03:05:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 03:05:45 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 03:05:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 03:05:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 03:05:54 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 03:05:55 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 03:05:56 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 03:05:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 03:06:01 GMT
EXPOSE 80
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 443
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 03:06:03 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 03:06:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a8e7fe5034ac502626b0a921d79be80c092890176e33b236c489d6f00710a2`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 299.2 KB (299211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db75acdaca15b1e81890f29b3b757fcc73e7a69a55f5ed659bf800f6340108`  
		Last Modified: Thu, 22 Oct 2020 03:06:43 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2197c38adf245bca8f229a4cd718c4d0f619a87bae5786572ccdac1a286882c`  
		Last Modified: Thu, 22 Oct 2020 03:06:46 GMT  
		Size: 10.9 MB (10854384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0104bc6a595940856019d00d9ff8e04365338a7964d948b64cc44bf73cc59e`  
		Last Modified: Thu, 22 Oct 2020 03:06:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:da121cf42d1759ed03af3130533d365c365af1d738d550744ad863e05e64cf46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13540356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b4aa38988ab2442575062d99c3cb44976de6c227256c118f35340e7c21c303`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:40:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:40:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:40:57 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:07 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:09 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:10 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:10 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbde357077a97c0f831033bf03c9828203cb7e3e6cb33217ce4d7cfd71c931`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 300.3 KB (300348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a5ab0aa923ce1fe233b904008bbf932c4787f48bcd59f07a85616147b7cbc3`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc398339860cf826624c9c22b5de9b45a193260e2ff24826d210b493483398f`  
		Last Modified: Thu, 22 Oct 2020 02:41:59 GMT  
		Size: 10.5 MB (10527465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6e7d61d1d4a00550447ea1f67edc0463cc527e49356e98959edfafba0df879`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:09208042b4d19d7ed87b51b99dc20b390dab20d9ae7e235a62a3af3aaf472bd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13291756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5c77284adc35481d13003d31a866f637b6eaf9f5764f667e536db79ce23129`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:39:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 13:44:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 13:44:04 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 13:44:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 13:44:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:44:33 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 13:44:37 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 13:44:40 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 13:44:44 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 13:44:48 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 13:44:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 13:44:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 13:45:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 13:45:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 13:45:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 13:45:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 13:45:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 13:45:23 GMT
EXPOSE 80
# Thu, 22 Oct 2020 13:45:26 GMT
EXPOSE 443
# Thu, 22 Oct 2020 13:45:30 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 13:45:35 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 13:45:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a4964211b7ce86541a0c1dad8ef3800ec38a3ca90aff94b76759b4cb8e279`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 302.3 KB (302327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dd938ef3e3eae8509deda8fab9ab5f9344169d912e35a802633e799feed1bb`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe23c296ee12ee12ef84dbabbb4f7bf0362a9a12b684782ebd3f44a97c8fcf8e`  
		Last Modified: Thu, 22 Oct 2020 13:47:55 GMT  
		Size: 10.2 MB (10180223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2f3c084745fecafaa9ff33626a81124f2d70267ceee705da555714238bfa1`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:3e18b421d651721239cb3422bc890d1211535681219b7696816f487b4cebc4ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14074857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d5562f1d148d3d67ff7f5995be8f860553ad0f3d07091335643306b83385e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:41:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:41:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:41 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f988ff23f3cbb35bfed69e33f3b7ee69403bfae4f46363a08eea4830053e9c`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 300.5 KB (300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd6a4e0db99510879c5dfceabd1e629a0692c4544bb0da34971f8722b881e92`  
		Last Modified: Thu, 22 Oct 2020 02:42:09 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e13b938aa802e74610585cabba77d625db4baf219f577a81195c272408c7d3`  
		Last Modified: Thu, 22 Oct 2020 02:42:16 GMT  
		Size: 11.2 MB (11202559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a221fff082950a8a98db12eb99f532a39008f0d6e21684bc1aed06fa1ed2a764`  
		Last Modified: Thu, 22 Oct 2020 02:42:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-builder`

```console
$ docker pull caddy@sha256:a3a3208982f94bce254e689780d79e0457b3b76d5b9d854628caf090504a3729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.2.1-builder` - linux; amd64

```console
$ docker pull caddy@sha256:fc73b9cce8ce070df5bd3bf94ff6f0dba5ab3a82359d7313d216b71585946551
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119452255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7c4becdaa4921f4830aa5898531fb59bdb497d37b6a9109fc9d2189b47316d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:34:56 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:34:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:34:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:35:51 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:38:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:38:42 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:38:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:38:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:38:44 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:18:13 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:18:13 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:18:13 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:18:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:18:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:18:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:18:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7d3d256c8367c41c431143c63d083a25dd62ec9ee9d9773dd9e6c7b70ec9e`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9db76c5a1d06710ed4f3073476b2d883ff8e911f8e47c558bc4a8d1d8663fa`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f88ce657dbabff9f6a04034006ee66c6ecfb0d54bb599525d9c8d9ad91a22`  
		Last Modified: Fri, 06 Nov 2020 19:47:52 GMT  
		Size: 106.7 MB (106656837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dc1c79fe7f44761a5d11f6f64f4ec7142a59bf2225b8a1e5554ed551654797`  
		Last Modified: Fri, 06 Nov 2020 19:47:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec1cb62beafb625b4104c718b0c582ffdcc06f9ca5efd25549b3c1905cf16`  
		Last Modified: Fri, 06 Nov 2020 21:18:36 GMT  
		Size: 8.3 MB (8309861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461a7017d5ae9ee39afa73c0013aa3fc8bcb8518db59843e7eff18a067c4142`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 1.4 MB (1407206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd8af862e3e9052217f29783b7f6e65c65f057dd9aa35f585882f13c0b34cde`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89a73c5f4ae51892063fa87a4c7bbcb1311e07f70d70df7e2d8a03c7f61eac7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114664382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e85a7472aacc21b210dfa3f511a5358983fb44fab90d8bd81956f0974cba9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:07:24 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:07:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:53:45 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:56:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:56:20 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:56:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:56:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:56:23 GMT
WORKDIR /go
# Fri, 06 Nov 2020 19:22:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 19:22:55 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:22:56 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:22:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:23:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 19:23:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 19:23:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20cc27a60e8ac1bf56dec787d3d52ba856e657179cfd56050036db79abb4267`  
		Last Modified: Thu, 22 Oct 2020 05:34:55 GMT  
		Size: 281.0 KB (280971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecce92c3d2de40638d73e682dec26c2b79a055e85c8d70b88f4ccb9485bb9c9`  
		Last Modified: Thu, 22 Oct 2020 05:34:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bea26c6de29e9326bc228c64da95fcd54b3d1f9354f1165eafc349994db0f8`  
		Last Modified: Fri, 06 Nov 2020 19:04:15 GMT  
		Size: 102.5 MB (102524592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e5877f5507358b36e32b963095c3caf40f40a6eec614d816a33f2f2ebfd55`  
		Last Modified: Fri, 06 Nov 2020 19:03:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81d2f79a49d963d6cbaa15e2327930649da636b6b369f88d7c19d733c5eb296`  
		Last Modified: Fri, 06 Nov 2020 19:23:35 GMT  
		Size: 7.9 MB (7928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea3d4a6a9133060470b288519140837675e4773f464432a967a4e3a080ac986`  
		Last Modified: Fri, 06 Nov 2020 19:23:34 GMT  
		Size: 1.3 MB (1327357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bf1d579fdbbae7b37fb9ef4d32de07ce43408b789fded70f7baeabe507c78e`  
		Last Modified: Fri, 06 Nov 2020 19:23:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:931f32bb911ba0de19091cc5d1b56e45a88159343a6782497a325539a5f88e3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113487064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8b5eddc6ef348d71b508ab97a7dd567f6a977bac2cdd3828e499bb4440c38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:21:35 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:23:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:23:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:39:15 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:41:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:41:25 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:41:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:41:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:41:29 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:27:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:27:33 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:27:34 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:27:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:27:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:27:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:27:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b753cfc04fdce9640aac1e7a4b3e7ce15fa60b8e357376e42f294f463a6e890`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 280.1 KB (280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90c422e5e4668cb4140aadb622d734faa93c81cc1e283da9b08bbbc65c45c5`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b476d7beedfa2137a0fef6e60a4484b51d77830c70ebcff073ccc374056e2e0c`  
		Last Modified: Fri, 06 Nov 2020 19:49:31 GMT  
		Size: 102.3 MB (102329948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd72c431842e0aeea9c3f8328785176b40806958c71f4fefebd421c3518571`  
		Last Modified: Fri, 06 Nov 2020 19:48:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7315086fe1858140ae2a84a77af42759c8f4e82b0a4df1b0529669c2e6208cc`  
		Last Modified: Fri, 06 Nov 2020 20:28:06 GMT  
		Size: 7.1 MB (7144798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca52434a632fe2aa304e8fd42e54bcf29afa42ffe1b722340860d449685dae`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 1.3 MB (1325846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e36ff02f43b3832542cf4347e8366772d4877647f3fc2c7a0624aa885219ad`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:30fe2a9e24366ead2b615623a7637421e1b02f3f5404268d728e823253d1d889
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114775259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a06ec2afc931f2326cd6e8f7d6ead1bd093d76c1dac1e006111bb4cdc22354`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:08:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 04:09:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:09:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:18:49 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:20:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:20:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:20:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:20:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:20:48 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:09:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:09:26 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:09:26 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:09:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:09:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:09:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:09:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4357932f1b6fb010e1461cc5c673712fb832ac44ee627c691db0b64adf95d13`  
		Last Modified: Thu, 22 Oct 2020 04:28:32 GMT  
		Size: 281.2 KB (281230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c013af1878066e59b688e31fd962e7267430963de27c5257241e3c223aa1d6`  
		Last Modified: Thu, 22 Oct 2020 04:28:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b36744bb2cb0aa83f712639340b2320bd38128965d09ffffa43856a210f9e5`  
		Last Modified: Fri, 06 Nov 2020 19:28:03 GMT  
		Size: 102.0 MB (101976695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620dd3e3aa585cedfbb73c7698bdfc75f79b8a92e0bd7e7d5dcc2041012893be`  
		Last Modified: Fri, 06 Nov 2020 19:27:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803037031a1f00d46e050e3bb3fca389a0ac1939d4cb43c1548f0d72bb47cb5`  
		Last Modified: Fri, 06 Nov 2020 21:10:01 GMT  
		Size: 8.5 MB (8499884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840674c7f6a6769677bea40173b44c0cdf85447290b9521805050cac0b25df6`  
		Last Modified: Fri, 06 Nov 2020 21:09:59 GMT  
		Size: 1.3 MB (1310181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a9e6466e2de25170ecf4a3eb0a32a4dd076dcf8faabf6f80120fc45f1491`  
		Last Modified: Fri, 06 Nov 2020 21:09:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51c882c7f333a86293123c5c9f7dde2e2d733761be27faa8ba679fd25880dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113944446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed252304acf0e273fc3538fbd970d4bfaa5fe502c7fe021fcb299559f389f4be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:27:26 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 13:27:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:27:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:32:30 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:34:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:34:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:34:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:35:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:35:27 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:51:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:51:06 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:51:09 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:51:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:51:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:51:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:51:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9900411dc7c8c88618743573bf89478d726007403bd002d8b00d21b7fecd40a`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 283.2 KB (283205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbd106374e3baf7eb8e3d8f7ffd4c364a35e57dcb3a89f8a153327a4c3fa3f9`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec3950b2a73c219aef5a15211d4abc2d9a5af90823e42083fdace116f7c476`  
		Last Modified: Fri, 06 Nov 2020 18:47:04 GMT  
		Size: 100.6 MB (100649515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccf6cddd12f97382439bc21574bae904a64d8e1f96a30b0ac21e85f7aa112d7`  
		Last Modified: Fri, 06 Nov 2020 18:46:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94e9e52826c34d57af8656e0e5b92258140dd8b57f186db8861f03ef5e4f00`  
		Last Modified: Fri, 06 Nov 2020 21:52:28 GMT  
		Size: 8.9 MB (8920000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75746c400be689f32365c8fb16a86def9e748eaf0507246876dade9fa125e78c`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 1.3 MB (1287791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0695a08f39b4841501692759a1c562a2e2c4c13bac546fbed9a962411082c141`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:b252d4071ae496dbd6a16de864a46fe6d0629a7d35c8b123c58e19261db37455
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118365434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216ff73b58d08ff9b58e775653d0f32630eb7df17076e32df1011ce6bafaed1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:53:28 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 02:53:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:53:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:23:44 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:25:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:26:04 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:26:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:26:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:26:07 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:40:05 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:40:07 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:40:07 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:40:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:40:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:40:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:40:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5139d7663b8674a989574c2161166fb137f26ef16b2f701159c126628be75101`  
		Last Modified: Thu, 22 Oct 2020 02:58:32 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31a06258ad66efe2dedbf67809ebc107a55757b8a4543af77982f55ff6c067`  
		Last Modified: Thu, 22 Oct 2020 02:58:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c878f3bd7fd82dbe36e4d303393019e0703f5e67ebb74f817f7369f072e6532`  
		Last Modified: Fri, 06 Nov 2020 19:34:26 GMT  
		Size: 105.8 MB (105776540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980f7999cd7558faa66bb1ae504f8c1e22e4881e3d71f3fd3aa2a4cb8ca7db13`  
		Last Modified: Fri, 06 Nov 2020 19:34:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85206d14782c0fb54511c935afb74a9e81b7c4bf73176614eadd044297188377`  
		Last Modified: Fri, 06 Nov 2020 20:40:48 GMT  
		Size: 8.4 MB (8352230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5f0e7da5d92511b1993de47afc01232a9b314ea3b5e854b83b0713acab7906`  
		Last Modified: Fri, 06 Nov 2020 20:40:47 GMT  
		Size: 1.4 MB (1388754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bfc26b576e6aeb40246d6645a95abab375e81757ab7a3095af525666ae295a`  
		Last Modified: Fri, 06 Nov 2020 20:40:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:0cc26b33a1fe2b1ae4225a57d25846d69166be17484f8f847a3b835626c2df47
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548826368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5551c0b95fd6fba6bbdbef91ad7fd2edce9814d5127b0dd65274fd6fa964da48`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:27:03 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:27:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:28:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:28:38 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:29:02 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:15:07 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:17:47 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:17:49 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:57:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:57:51 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:57:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:58:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:58:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23a75d88f9f5980bb112e2c28248975f107144d8d2e40dc4755e2a09f5e56df`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea6d8b9d9b014ffa471b7bb8882ddb7e9d378ddcacc099f0710073bd6361b9`  
		Last Modified: Wed, 14 Oct 2020 12:50:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75c1905c0573cc5706bc066d23624f0e92a8871832c744fbe7eabdcbc6f8a85`  
		Last Modified: Wed, 14 Oct 2020 12:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938695376d9deeba8819539ff3245935c28f93229d1c332bb8b6a16e67013fbc`  
		Last Modified: Wed, 14 Oct 2020 12:50:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41106c6a476cf9666c6d8c3c853c982a841c29db05b3ef8a072baba537b6d74c`  
		Last Modified: Wed, 14 Oct 2020 12:50:48 GMT  
		Size: 34.3 MB (34312667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6d6258831f87f3b455e6316e2bed430465a760272614de7cdd28c7c6e9f3e`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e3f66638c4d5ce9adba16e49844f57efbab1d628d9d6c73133511b7c1c3892`  
		Last Modified: Wed, 14 Oct 2020 12:50:20 GMT  
		Size: 310.5 KB (310525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d8771646c530e34e5045246ce3b2ebe859c4f5be8c444ec5dba3c382bee3a`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652b8eae6f5ed9dba044dae68e11cd7a4320ee55b36f6016b2199b9f3316c31a`  
		Last Modified: Fri, 06 Nov 2020 19:34:01 GMT  
		Size: 138.3 MB (138329448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadb866080cf8fd8fb40d4722c8642031ac09e46b3ad9f8029cc13e4531e8d63`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2a55f83bf6210220425240b3a2382a1dcede45856c71588260c441d4d560a`  
		Last Modified: Fri, 06 Nov 2020 20:00:57 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5aeaca4a088d8f8b44454e8a71c131afb3faae25b4a31ffbcbd0e36e46c2a7`  
		Last Modified: Fri, 06 Nov 2020 20:00:55 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a62e98c257ab6518929697507951e1378383d5c25b708c0a5bdc20bb2f4cb`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02e4c481fcbe14f0818df1d4a577730f215914c3f7a4c44f3926c08ec354a2d`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3aba19aa6c0c8a874ce9d79d9e6d91ce5040a8037854a0d8c95fa1cf811030`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.8 MB (1768657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b33a039b5dad3077c7f441fbcd6321bccc7bb5d8d9db0b77f563baa66aab5d`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:91615621bb5d8f928cae33580878a3a0e4c360d2bd1a5078bd5579ffc1f65586
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941036189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69fe55d922052ef8814dc705972036b5fa14d96cea24bb078c82eded58a8536`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:31:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:31:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:33:58 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:35:13 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:18:04 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:21:38 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:21:40 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:58:23 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:58:24 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:58:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:59:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:59:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528ba1d9759adcc464112008fe49672e1f545981d69bab31186587ab32f92138`  
		Last Modified: Wed, 14 Oct 2020 12:51:33 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf4e6180661653575845d30a4d882dea92f395cb540b1cdf91170e9ee58731`  
		Last Modified: Wed, 14 Oct 2020 12:51:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e973f094614bb2cebe16df6f6004c05895ed077151aecdbbd0c476513054fc`  
		Last Modified: Wed, 14 Oct 2020 12:51:25 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089b875ac355097876e23760dd2166f096a8645e312660ffd3c0e617a2df9a0`  
		Last Modified: Wed, 14 Oct 2020 12:51:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a016b666d0691307c6414d84c36eb82de4b2fc4d74dd04c75f632dc3a78c`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 35.0 MB (35016991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4d95d13c0a45aa19a623e51cb112530a589a3a4d15d5c119610f8196912fab`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf8226941bb8f5af9f2be8fdb54da3e3caef344b0061a73e3debde23a55e98f`  
		Last Modified: Wed, 14 Oct 2020 12:51:24 GMT  
		Size: 9.9 MB (9870100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e5f43d50387ad619b863923b75cdf46053a8edd9954ec6e5bcdd6b90719c56`  
		Last Modified: Fri, 06 Nov 2020 19:34:21 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce913b69c36a8d04261681b1d8cde7dd3ec67f8275dc2c21b7b9d42074721ec1`  
		Last Modified: Fri, 06 Nov 2020 19:34:56 GMT  
		Size: 143.5 MB (143487215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75231de833daeca0a14373f4edb90eeaa4ec81d6fe961b4de6529a89c511ca2c`  
		Last Modified: Fri, 06 Nov 2020 19:34:20 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1a4d62df1ffdb8baac455f20994d1992ae918702aeb6c3c3171001c6870a73`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf2e1fbaf300596e6987a1c0f473fc2dde64d5a816b13f3aaf21cf2e4cc3332`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a001d9ed8d402d293907ee530361c27f8b6f076be745516b37580b9fbb73b9c2`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1740d81d6c6721405d45f80726a0ebcd3dc0d0de5da905fb41d182ca78a921ec`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d14e15f1dc7fa0765eb82fe118a91aa20fbef9c5c677cde9a38ddc0890ae260`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 11.3 MB (11295267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb21d7c1a6d233e3c34e5e883d3bc762275075111197136cb6b326f4ea46056`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-builder-alpine`

```console
$ docker pull caddy@sha256:c243e906eda12ce67b24e021caa307808407005fc1a8197284d9b70daaf2a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.2.1-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:fc73b9cce8ce070df5bd3bf94ff6f0dba5ab3a82359d7313d216b71585946551
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119452255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7c4becdaa4921f4830aa5898531fb59bdb497d37b6a9109fc9d2189b47316d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:34:56 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:34:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:34:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:35:51 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:38:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:38:42 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:38:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:38:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:38:44 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:18:13 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:18:13 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:18:13 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:18:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:18:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:18:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:18:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7d3d256c8367c41c431143c63d083a25dd62ec9ee9d9773dd9e6c7b70ec9e`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9db76c5a1d06710ed4f3073476b2d883ff8e911f8e47c558bc4a8d1d8663fa`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f88ce657dbabff9f6a04034006ee66c6ecfb0d54bb599525d9c8d9ad91a22`  
		Last Modified: Fri, 06 Nov 2020 19:47:52 GMT  
		Size: 106.7 MB (106656837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dc1c79fe7f44761a5d11f6f64f4ec7142a59bf2225b8a1e5554ed551654797`  
		Last Modified: Fri, 06 Nov 2020 19:47:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec1cb62beafb625b4104c718b0c582ffdcc06f9ca5efd25549b3c1905cf16`  
		Last Modified: Fri, 06 Nov 2020 21:18:36 GMT  
		Size: 8.3 MB (8309861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461a7017d5ae9ee39afa73c0013aa3fc8bcb8518db59843e7eff18a067c4142`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 1.4 MB (1407206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd8af862e3e9052217f29783b7f6e65c65f057dd9aa35f585882f13c0b34cde`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89a73c5f4ae51892063fa87a4c7bbcb1311e07f70d70df7e2d8a03c7f61eac7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114664382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e85a7472aacc21b210dfa3f511a5358983fb44fab90d8bd81956f0974cba9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:07:24 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:07:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:53:45 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:56:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:56:20 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:56:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:56:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:56:23 GMT
WORKDIR /go
# Fri, 06 Nov 2020 19:22:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 19:22:55 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:22:56 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:22:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:23:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 19:23:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 19:23:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20cc27a60e8ac1bf56dec787d3d52ba856e657179cfd56050036db79abb4267`  
		Last Modified: Thu, 22 Oct 2020 05:34:55 GMT  
		Size: 281.0 KB (280971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecce92c3d2de40638d73e682dec26c2b79a055e85c8d70b88f4ccb9485bb9c9`  
		Last Modified: Thu, 22 Oct 2020 05:34:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bea26c6de29e9326bc228c64da95fcd54b3d1f9354f1165eafc349994db0f8`  
		Last Modified: Fri, 06 Nov 2020 19:04:15 GMT  
		Size: 102.5 MB (102524592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e5877f5507358b36e32b963095c3caf40f40a6eec614d816a33f2f2ebfd55`  
		Last Modified: Fri, 06 Nov 2020 19:03:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81d2f79a49d963d6cbaa15e2327930649da636b6b369f88d7c19d733c5eb296`  
		Last Modified: Fri, 06 Nov 2020 19:23:35 GMT  
		Size: 7.9 MB (7928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea3d4a6a9133060470b288519140837675e4773f464432a967a4e3a080ac986`  
		Last Modified: Fri, 06 Nov 2020 19:23:34 GMT  
		Size: 1.3 MB (1327357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bf1d579fdbbae7b37fb9ef4d32de07ce43408b789fded70f7baeabe507c78e`  
		Last Modified: Fri, 06 Nov 2020 19:23:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:931f32bb911ba0de19091cc5d1b56e45a88159343a6782497a325539a5f88e3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113487064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8b5eddc6ef348d71b508ab97a7dd567f6a977bac2cdd3828e499bb4440c38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:21:35 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:23:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:23:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:39:15 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:41:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:41:25 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:41:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:41:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:41:29 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:27:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:27:33 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:27:34 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:27:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:27:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:27:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:27:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b753cfc04fdce9640aac1e7a4b3e7ce15fa60b8e357376e42f294f463a6e890`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 280.1 KB (280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90c422e5e4668cb4140aadb622d734faa93c81cc1e283da9b08bbbc65c45c5`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b476d7beedfa2137a0fef6e60a4484b51d77830c70ebcff073ccc374056e2e0c`  
		Last Modified: Fri, 06 Nov 2020 19:49:31 GMT  
		Size: 102.3 MB (102329948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd72c431842e0aeea9c3f8328785176b40806958c71f4fefebd421c3518571`  
		Last Modified: Fri, 06 Nov 2020 19:48:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7315086fe1858140ae2a84a77af42759c8f4e82b0a4df1b0529669c2e6208cc`  
		Last Modified: Fri, 06 Nov 2020 20:28:06 GMT  
		Size: 7.1 MB (7144798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca52434a632fe2aa304e8fd42e54bcf29afa42ffe1b722340860d449685dae`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 1.3 MB (1325846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e36ff02f43b3832542cf4347e8366772d4877647f3fc2c7a0624aa885219ad`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:30fe2a9e24366ead2b615623a7637421e1b02f3f5404268d728e823253d1d889
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114775259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a06ec2afc931f2326cd6e8f7d6ead1bd093d76c1dac1e006111bb4cdc22354`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:08:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 04:09:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:09:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:18:49 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:20:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:20:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:20:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:20:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:20:48 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:09:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:09:26 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:09:26 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:09:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:09:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:09:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:09:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4357932f1b6fb010e1461cc5c673712fb832ac44ee627c691db0b64adf95d13`  
		Last Modified: Thu, 22 Oct 2020 04:28:32 GMT  
		Size: 281.2 KB (281230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c013af1878066e59b688e31fd962e7267430963de27c5257241e3c223aa1d6`  
		Last Modified: Thu, 22 Oct 2020 04:28:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b36744bb2cb0aa83f712639340b2320bd38128965d09ffffa43856a210f9e5`  
		Last Modified: Fri, 06 Nov 2020 19:28:03 GMT  
		Size: 102.0 MB (101976695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620dd3e3aa585cedfbb73c7698bdfc75f79b8a92e0bd7e7d5dcc2041012893be`  
		Last Modified: Fri, 06 Nov 2020 19:27:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803037031a1f00d46e050e3bb3fca389a0ac1939d4cb43c1548f0d72bb47cb5`  
		Last Modified: Fri, 06 Nov 2020 21:10:01 GMT  
		Size: 8.5 MB (8499884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840674c7f6a6769677bea40173b44c0cdf85447290b9521805050cac0b25df6`  
		Last Modified: Fri, 06 Nov 2020 21:09:59 GMT  
		Size: 1.3 MB (1310181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a9e6466e2de25170ecf4a3eb0a32a4dd076dcf8faabf6f80120fc45f1491`  
		Last Modified: Fri, 06 Nov 2020 21:09:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51c882c7f333a86293123c5c9f7dde2e2d733761be27faa8ba679fd25880dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113944446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed252304acf0e273fc3538fbd970d4bfaa5fe502c7fe021fcb299559f389f4be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:27:26 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 13:27:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:27:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:32:30 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:34:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:34:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:34:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:35:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:35:27 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:51:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:51:06 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:51:09 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:51:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:51:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:51:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:51:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9900411dc7c8c88618743573bf89478d726007403bd002d8b00d21b7fecd40a`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 283.2 KB (283205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbd106374e3baf7eb8e3d8f7ffd4c364a35e57dcb3a89f8a153327a4c3fa3f9`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec3950b2a73c219aef5a15211d4abc2d9a5af90823e42083fdace116f7c476`  
		Last Modified: Fri, 06 Nov 2020 18:47:04 GMT  
		Size: 100.6 MB (100649515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccf6cddd12f97382439bc21574bae904a64d8e1f96a30b0ac21e85f7aa112d7`  
		Last Modified: Fri, 06 Nov 2020 18:46:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94e9e52826c34d57af8656e0e5b92258140dd8b57f186db8861f03ef5e4f00`  
		Last Modified: Fri, 06 Nov 2020 21:52:28 GMT  
		Size: 8.9 MB (8920000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75746c400be689f32365c8fb16a86def9e748eaf0507246876dade9fa125e78c`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 1.3 MB (1287791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0695a08f39b4841501692759a1c562a2e2c4c13bac546fbed9a962411082c141`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:b252d4071ae496dbd6a16de864a46fe6d0629a7d35c8b123c58e19261db37455
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118365434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216ff73b58d08ff9b58e775653d0f32630eb7df17076e32df1011ce6bafaed1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:53:28 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 02:53:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:53:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:23:44 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:25:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:26:04 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:26:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:26:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:26:07 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:40:05 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:40:07 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:40:07 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:40:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:40:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:40:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:40:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5139d7663b8674a989574c2161166fb137f26ef16b2f701159c126628be75101`  
		Last Modified: Thu, 22 Oct 2020 02:58:32 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31a06258ad66efe2dedbf67809ebc107a55757b8a4543af77982f55ff6c067`  
		Last Modified: Thu, 22 Oct 2020 02:58:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c878f3bd7fd82dbe36e4d303393019e0703f5e67ebb74f817f7369f072e6532`  
		Last Modified: Fri, 06 Nov 2020 19:34:26 GMT  
		Size: 105.8 MB (105776540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980f7999cd7558faa66bb1ae504f8c1e22e4881e3d71f3fd3aa2a4cb8ca7db13`  
		Last Modified: Fri, 06 Nov 2020 19:34:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85206d14782c0fb54511c935afb74a9e81b7c4bf73176614eadd044297188377`  
		Last Modified: Fri, 06 Nov 2020 20:40:48 GMT  
		Size: 8.4 MB (8352230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5f0e7da5d92511b1993de47afc01232a9b314ea3b5e854b83b0713acab7906`  
		Last Modified: Fri, 06 Nov 2020 20:40:47 GMT  
		Size: 1.4 MB (1388754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bfc26b576e6aeb40246d6645a95abab375e81757ab7a3095af525666ae295a`  
		Last Modified: Fri, 06 Nov 2020 20:40:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:b38981e5323bcf982907423ded683b2c6f8548a129819434392a2413e15fc1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:2.2.1-builder-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:0cc26b33a1fe2b1ae4225a57d25846d69166be17484f8f847a3b835626c2df47
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548826368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5551c0b95fd6fba6bbdbef91ad7fd2edce9814d5127b0dd65274fd6fa964da48`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:27:03 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:27:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:28:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:28:38 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:29:02 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:15:07 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:17:47 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:17:49 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:57:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:57:51 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:57:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:58:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:58:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23a75d88f9f5980bb112e2c28248975f107144d8d2e40dc4755e2a09f5e56df`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea6d8b9d9b014ffa471b7bb8882ddb7e9d378ddcacc099f0710073bd6361b9`  
		Last Modified: Wed, 14 Oct 2020 12:50:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75c1905c0573cc5706bc066d23624f0e92a8871832c744fbe7eabdcbc6f8a85`  
		Last Modified: Wed, 14 Oct 2020 12:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938695376d9deeba8819539ff3245935c28f93229d1c332bb8b6a16e67013fbc`  
		Last Modified: Wed, 14 Oct 2020 12:50:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41106c6a476cf9666c6d8c3c853c982a841c29db05b3ef8a072baba537b6d74c`  
		Last Modified: Wed, 14 Oct 2020 12:50:48 GMT  
		Size: 34.3 MB (34312667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6d6258831f87f3b455e6316e2bed430465a760272614de7cdd28c7c6e9f3e`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e3f66638c4d5ce9adba16e49844f57efbab1d628d9d6c73133511b7c1c3892`  
		Last Modified: Wed, 14 Oct 2020 12:50:20 GMT  
		Size: 310.5 KB (310525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d8771646c530e34e5045246ce3b2ebe859c4f5be8c444ec5dba3c382bee3a`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652b8eae6f5ed9dba044dae68e11cd7a4320ee55b36f6016b2199b9f3316c31a`  
		Last Modified: Fri, 06 Nov 2020 19:34:01 GMT  
		Size: 138.3 MB (138329448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadb866080cf8fd8fb40d4722c8642031ac09e46b3ad9f8029cc13e4531e8d63`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2a55f83bf6210220425240b3a2382a1dcede45856c71588260c441d4d560a`  
		Last Modified: Fri, 06 Nov 2020 20:00:57 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5aeaca4a088d8f8b44454e8a71c131afb3faae25b4a31ffbcbd0e36e46c2a7`  
		Last Modified: Fri, 06 Nov 2020 20:00:55 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a62e98c257ab6518929697507951e1378383d5c25b708c0a5bdc20bb2f4cb`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02e4c481fcbe14f0818df1d4a577730f215914c3f7a4c44f3926c08ec354a2d`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3aba19aa6c0c8a874ce9d79d9e6d91ce5040a8037854a0d8c95fa1cf811030`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.8 MB (1768657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b33a039b5dad3077c7f441fbcd6321bccc7bb5d8d9db0b77f563baa66aab5d`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:2689ae5b16484bd1a074522d9ae004e9664036b4043a3bafe8443620784dbb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.2.1-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:91615621bb5d8f928cae33580878a3a0e4c360d2bd1a5078bd5579ffc1f65586
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941036189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69fe55d922052ef8814dc705972036b5fa14d96cea24bb078c82eded58a8536`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:31:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:31:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:33:58 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:35:13 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:18:04 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:21:38 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:21:40 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:58:23 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:58:24 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:58:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:59:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:59:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528ba1d9759adcc464112008fe49672e1f545981d69bab31186587ab32f92138`  
		Last Modified: Wed, 14 Oct 2020 12:51:33 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf4e6180661653575845d30a4d882dea92f395cb540b1cdf91170e9ee58731`  
		Last Modified: Wed, 14 Oct 2020 12:51:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e973f094614bb2cebe16df6f6004c05895ed077151aecdbbd0c476513054fc`  
		Last Modified: Wed, 14 Oct 2020 12:51:25 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089b875ac355097876e23760dd2166f096a8645e312660ffd3c0e617a2df9a0`  
		Last Modified: Wed, 14 Oct 2020 12:51:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a016b666d0691307c6414d84c36eb82de4b2fc4d74dd04c75f632dc3a78c`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 35.0 MB (35016991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4d95d13c0a45aa19a623e51cb112530a589a3a4d15d5c119610f8196912fab`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf8226941bb8f5af9f2be8fdb54da3e3caef344b0061a73e3debde23a55e98f`  
		Last Modified: Wed, 14 Oct 2020 12:51:24 GMT  
		Size: 9.9 MB (9870100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e5f43d50387ad619b863923b75cdf46053a8edd9954ec6e5bcdd6b90719c56`  
		Last Modified: Fri, 06 Nov 2020 19:34:21 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce913b69c36a8d04261681b1d8cde7dd3ec67f8275dc2c21b7b9d42074721ec1`  
		Last Modified: Fri, 06 Nov 2020 19:34:56 GMT  
		Size: 143.5 MB (143487215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75231de833daeca0a14373f4edb90eeaa4ec81d6fe961b4de6529a89c511ca2c`  
		Last Modified: Fri, 06 Nov 2020 19:34:20 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1a4d62df1ffdb8baac455f20994d1992ae918702aeb6c3c3171001c6870a73`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf2e1fbaf300596e6987a1c0f473fc2dde64d5a816b13f3aaf21cf2e4cc3332`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a001d9ed8d402d293907ee530361c27f8b6f076be745516b37580b9fbb73b9c2`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1740d81d6c6721405d45f80726a0ebcd3dc0d0de5da905fb41d182ca78a921ec`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d14e15f1dc7fa0765eb82fe118a91aa20fbef9c5c677cde9a38ddc0890ae260`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 11.3 MB (11295267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb21d7c1a6d233e3c34e5e883d3bc762275075111197136cb6b326f4ea46056`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-windowsservercore`

```console
$ docker pull caddy@sha256:0cc9e18409440159fbf2ac241bce180b0214fc5d2358aa87fedf1189394d7469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.2.1-windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d720e5ab1579e03c0f86de11950434367743bdf8212a4501cd971c29d16942a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:2.2.1-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:155acd240efff18a38a7aff934be0f6976aeb1c76139025671c9833ed160c840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:ea06de9c9cb10eacb9f77e50817d2ad8dd63c977549f26c19d57df1a194fefdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:4ebad49f78a3f98164d89431978046ee6e94f1e8a70454abc7f49ce1a5ee7826
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb0137bab0e21a92b0bc9ec1cc22c259b097d5bf239b161ae1eac0de1833e67`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:33:22 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 04:33:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 04:33:55 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 04:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 04:34:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 04:34:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 04:34:02 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 04:34:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 80
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 443
# Thu, 22 Oct 2020 04:34:06 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 04:34:06 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 04:34:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e2d825895b6421ca5dbd63db0d99f790ef84a84c7bcaff51e60b654397858`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 300.0 KB (299956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaf2e3dee2e74b401fce928bf9502e48df68da4e8c1933bfd6b00b1137529fc`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 5.8 KB (5754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2215cf93250599c5db984cee0fddd5d0cd59ef035ab5a317387b67211bde86d`  
		Last Modified: Thu, 22 Oct 2020 04:35:06 GMT  
		Size: 11.5 MB (11532508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060365e49ba5ee96a2859e269b366f5a5c9f386e5bdbf07d2ef31b1fc6934baa`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:abba73dc860b2f35703cb7d27f08baf5bfc084e18e627b94661d01a8e2befdaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13784259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0aad5a281913821dd39ffed5e144daae22ac81ac4314731395ab65eedde72a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:58:10 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:58:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:58:46 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:58:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:58:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:59:00 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:59:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:59:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:59:03 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:59:08 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:59:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:59:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:59:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:59:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:59:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:59:15 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:59:19 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:59:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:59:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:59:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7369c3ac4b39c55c74e96dd3eb61ac2fa65e5671b1c2acca9697a7c9d20c3cf`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 300.1 KB (300086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8f4045920069dff3382a5993783c5d846d9e28d0f5a63c475ed298fce0abb7`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db6bde4735da15e5db23ad62f3d64d78aed8713a40d12547f5538c15c90f9da`  
		Last Modified: Thu, 22 Oct 2020 03:00:06 GMT  
		Size: 10.9 MB (10876280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a95efd7a14ed98a53a238da45faa7e3b0fdd2a93529b83bfe9d0823dafac67c`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8cf66cbe3c03273ca54bdab908092a6a9b9f02d39595ed15b1111f1465430426
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20723dea614fc40d9f3cb59eddd33bf0e89dfda3f8ed4a7b404ef334632a4b9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:04:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 03:05:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 03:05:45 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 03:05:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 03:05:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 03:05:54 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 03:05:55 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 03:05:56 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 03:05:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 03:06:01 GMT
EXPOSE 80
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 443
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 03:06:03 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 03:06:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a8e7fe5034ac502626b0a921d79be80c092890176e33b236c489d6f00710a2`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 299.2 KB (299211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db75acdaca15b1e81890f29b3b757fcc73e7a69a55f5ed659bf800f6340108`  
		Last Modified: Thu, 22 Oct 2020 03:06:43 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2197c38adf245bca8f229a4cd718c4d0f619a87bae5786572ccdac1a286882c`  
		Last Modified: Thu, 22 Oct 2020 03:06:46 GMT  
		Size: 10.9 MB (10854384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0104bc6a595940856019d00d9ff8e04365338a7964d948b64cc44bf73cc59e`  
		Last Modified: Thu, 22 Oct 2020 03:06:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:da121cf42d1759ed03af3130533d365c365af1d738d550744ad863e05e64cf46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13540356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b4aa38988ab2442575062d99c3cb44976de6c227256c118f35340e7c21c303`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:40:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:40:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:40:57 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:07 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:09 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:10 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:10 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbde357077a97c0f831033bf03c9828203cb7e3e6cb33217ce4d7cfd71c931`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 300.3 KB (300348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a5ab0aa923ce1fe233b904008bbf932c4787f48bcd59f07a85616147b7cbc3`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc398339860cf826624c9c22b5de9b45a193260e2ff24826d210b493483398f`  
		Last Modified: Thu, 22 Oct 2020 02:41:59 GMT  
		Size: 10.5 MB (10527465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6e7d61d1d4a00550447ea1f67edc0463cc527e49356e98959edfafba0df879`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:09208042b4d19d7ed87b51b99dc20b390dab20d9ae7e235a62a3af3aaf472bd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13291756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5c77284adc35481d13003d31a866f637b6eaf9f5764f667e536db79ce23129`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:39:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 13:44:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 13:44:04 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 13:44:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 13:44:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:44:33 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 13:44:37 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 13:44:40 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 13:44:44 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 13:44:48 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 13:44:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 13:44:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 13:45:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 13:45:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 13:45:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 13:45:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 13:45:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 13:45:23 GMT
EXPOSE 80
# Thu, 22 Oct 2020 13:45:26 GMT
EXPOSE 443
# Thu, 22 Oct 2020 13:45:30 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 13:45:35 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 13:45:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a4964211b7ce86541a0c1dad8ef3800ec38a3ca90aff94b76759b4cb8e279`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 302.3 KB (302327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dd938ef3e3eae8509deda8fab9ab5f9344169d912e35a802633e799feed1bb`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe23c296ee12ee12ef84dbabbb4f7bf0362a9a12b684782ebd3f44a97c8fcf8e`  
		Last Modified: Thu, 22 Oct 2020 13:47:55 GMT  
		Size: 10.2 MB (10180223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2f3c084745fecafaa9ff33626a81124f2d70267ceee705da555714238bfa1`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:3e18b421d651721239cb3422bc890d1211535681219b7696816f487b4cebc4ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14074857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d5562f1d148d3d67ff7f5995be8f860553ad0f3d07091335643306b83385e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:41:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:41:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:41 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f988ff23f3cbb35bfed69e33f3b7ee69403bfae4f46363a08eea4830053e9c`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 300.5 KB (300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd6a4e0db99510879c5dfceabd1e629a0692c4544bb0da34971f8722b881e92`  
		Last Modified: Thu, 22 Oct 2020 02:42:09 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e13b938aa802e74610585cabba77d625db4baf219f577a81195c272408c7d3`  
		Last Modified: Thu, 22 Oct 2020 02:42:16 GMT  
		Size: 11.2 MB (11202559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a221fff082950a8a98db12eb99f532a39008f0d6e21684bc1aed06fa1ed2a764`  
		Last Modified: Thu, 22 Oct 2020 02:42:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:a3a3208982f94bce254e689780d79e0457b3b76d5b9d854628caf090504a3729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:fc73b9cce8ce070df5bd3bf94ff6f0dba5ab3a82359d7313d216b71585946551
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119452255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7c4becdaa4921f4830aa5898531fb59bdb497d37b6a9109fc9d2189b47316d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:34:56 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:34:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:34:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:35:51 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:38:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:38:42 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:38:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:38:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:38:44 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:18:13 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:18:13 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:18:13 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:18:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:18:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:18:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:18:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7d3d256c8367c41c431143c63d083a25dd62ec9ee9d9773dd9e6c7b70ec9e`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9db76c5a1d06710ed4f3073476b2d883ff8e911f8e47c558bc4a8d1d8663fa`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f88ce657dbabff9f6a04034006ee66c6ecfb0d54bb599525d9c8d9ad91a22`  
		Last Modified: Fri, 06 Nov 2020 19:47:52 GMT  
		Size: 106.7 MB (106656837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dc1c79fe7f44761a5d11f6f64f4ec7142a59bf2225b8a1e5554ed551654797`  
		Last Modified: Fri, 06 Nov 2020 19:47:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec1cb62beafb625b4104c718b0c582ffdcc06f9ca5efd25549b3c1905cf16`  
		Last Modified: Fri, 06 Nov 2020 21:18:36 GMT  
		Size: 8.3 MB (8309861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461a7017d5ae9ee39afa73c0013aa3fc8bcb8518db59843e7eff18a067c4142`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 1.4 MB (1407206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd8af862e3e9052217f29783b7f6e65c65f057dd9aa35f585882f13c0b34cde`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89a73c5f4ae51892063fa87a4c7bbcb1311e07f70d70df7e2d8a03c7f61eac7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114664382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e85a7472aacc21b210dfa3f511a5358983fb44fab90d8bd81956f0974cba9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:07:24 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:07:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:53:45 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:56:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:56:20 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:56:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:56:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:56:23 GMT
WORKDIR /go
# Fri, 06 Nov 2020 19:22:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 19:22:55 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:22:56 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:22:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:23:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 19:23:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 19:23:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20cc27a60e8ac1bf56dec787d3d52ba856e657179cfd56050036db79abb4267`  
		Last Modified: Thu, 22 Oct 2020 05:34:55 GMT  
		Size: 281.0 KB (280971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecce92c3d2de40638d73e682dec26c2b79a055e85c8d70b88f4ccb9485bb9c9`  
		Last Modified: Thu, 22 Oct 2020 05:34:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bea26c6de29e9326bc228c64da95fcd54b3d1f9354f1165eafc349994db0f8`  
		Last Modified: Fri, 06 Nov 2020 19:04:15 GMT  
		Size: 102.5 MB (102524592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e5877f5507358b36e32b963095c3caf40f40a6eec614d816a33f2f2ebfd55`  
		Last Modified: Fri, 06 Nov 2020 19:03:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81d2f79a49d963d6cbaa15e2327930649da636b6b369f88d7c19d733c5eb296`  
		Last Modified: Fri, 06 Nov 2020 19:23:35 GMT  
		Size: 7.9 MB (7928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea3d4a6a9133060470b288519140837675e4773f464432a967a4e3a080ac986`  
		Last Modified: Fri, 06 Nov 2020 19:23:34 GMT  
		Size: 1.3 MB (1327357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bf1d579fdbbae7b37fb9ef4d32de07ce43408b789fded70f7baeabe507c78e`  
		Last Modified: Fri, 06 Nov 2020 19:23:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:931f32bb911ba0de19091cc5d1b56e45a88159343a6782497a325539a5f88e3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113487064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8b5eddc6ef348d71b508ab97a7dd567f6a977bac2cdd3828e499bb4440c38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:21:35 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:23:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:23:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:39:15 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:41:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:41:25 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:41:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:41:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:41:29 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:27:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:27:33 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:27:34 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:27:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:27:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:27:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:27:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b753cfc04fdce9640aac1e7a4b3e7ce15fa60b8e357376e42f294f463a6e890`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 280.1 KB (280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90c422e5e4668cb4140aadb622d734faa93c81cc1e283da9b08bbbc65c45c5`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b476d7beedfa2137a0fef6e60a4484b51d77830c70ebcff073ccc374056e2e0c`  
		Last Modified: Fri, 06 Nov 2020 19:49:31 GMT  
		Size: 102.3 MB (102329948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd72c431842e0aeea9c3f8328785176b40806958c71f4fefebd421c3518571`  
		Last Modified: Fri, 06 Nov 2020 19:48:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7315086fe1858140ae2a84a77af42759c8f4e82b0a4df1b0529669c2e6208cc`  
		Last Modified: Fri, 06 Nov 2020 20:28:06 GMT  
		Size: 7.1 MB (7144798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca52434a632fe2aa304e8fd42e54bcf29afa42ffe1b722340860d449685dae`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 1.3 MB (1325846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e36ff02f43b3832542cf4347e8366772d4877647f3fc2c7a0624aa885219ad`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:30fe2a9e24366ead2b615623a7637421e1b02f3f5404268d728e823253d1d889
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114775259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a06ec2afc931f2326cd6e8f7d6ead1bd093d76c1dac1e006111bb4cdc22354`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:08:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 04:09:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:09:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:18:49 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:20:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:20:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:20:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:20:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:20:48 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:09:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:09:26 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:09:26 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:09:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:09:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:09:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:09:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4357932f1b6fb010e1461cc5c673712fb832ac44ee627c691db0b64adf95d13`  
		Last Modified: Thu, 22 Oct 2020 04:28:32 GMT  
		Size: 281.2 KB (281230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c013af1878066e59b688e31fd962e7267430963de27c5257241e3c223aa1d6`  
		Last Modified: Thu, 22 Oct 2020 04:28:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b36744bb2cb0aa83f712639340b2320bd38128965d09ffffa43856a210f9e5`  
		Last Modified: Fri, 06 Nov 2020 19:28:03 GMT  
		Size: 102.0 MB (101976695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620dd3e3aa585cedfbb73c7698bdfc75f79b8a92e0bd7e7d5dcc2041012893be`  
		Last Modified: Fri, 06 Nov 2020 19:27:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803037031a1f00d46e050e3bb3fca389a0ac1939d4cb43c1548f0d72bb47cb5`  
		Last Modified: Fri, 06 Nov 2020 21:10:01 GMT  
		Size: 8.5 MB (8499884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840674c7f6a6769677bea40173b44c0cdf85447290b9521805050cac0b25df6`  
		Last Modified: Fri, 06 Nov 2020 21:09:59 GMT  
		Size: 1.3 MB (1310181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a9e6466e2de25170ecf4a3eb0a32a4dd076dcf8faabf6f80120fc45f1491`  
		Last Modified: Fri, 06 Nov 2020 21:09:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51c882c7f333a86293123c5c9f7dde2e2d733761be27faa8ba679fd25880dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113944446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed252304acf0e273fc3538fbd970d4bfaa5fe502c7fe021fcb299559f389f4be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:27:26 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 13:27:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:27:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:32:30 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:34:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:34:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:34:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:35:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:35:27 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:51:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:51:06 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:51:09 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:51:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:51:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:51:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:51:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9900411dc7c8c88618743573bf89478d726007403bd002d8b00d21b7fecd40a`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 283.2 KB (283205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbd106374e3baf7eb8e3d8f7ffd4c364a35e57dcb3a89f8a153327a4c3fa3f9`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec3950b2a73c219aef5a15211d4abc2d9a5af90823e42083fdace116f7c476`  
		Last Modified: Fri, 06 Nov 2020 18:47:04 GMT  
		Size: 100.6 MB (100649515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccf6cddd12f97382439bc21574bae904a64d8e1f96a30b0ac21e85f7aa112d7`  
		Last Modified: Fri, 06 Nov 2020 18:46:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94e9e52826c34d57af8656e0e5b92258140dd8b57f186db8861f03ef5e4f00`  
		Last Modified: Fri, 06 Nov 2020 21:52:28 GMT  
		Size: 8.9 MB (8920000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75746c400be689f32365c8fb16a86def9e748eaf0507246876dade9fa125e78c`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 1.3 MB (1287791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0695a08f39b4841501692759a1c562a2e2c4c13bac546fbed9a962411082c141`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:b252d4071ae496dbd6a16de864a46fe6d0629a7d35c8b123c58e19261db37455
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118365434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216ff73b58d08ff9b58e775653d0f32630eb7df17076e32df1011ce6bafaed1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:53:28 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 02:53:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:53:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:23:44 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:25:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:26:04 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:26:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:26:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:26:07 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:40:05 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:40:07 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:40:07 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:40:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:40:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:40:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:40:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5139d7663b8674a989574c2161166fb137f26ef16b2f701159c126628be75101`  
		Last Modified: Thu, 22 Oct 2020 02:58:32 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31a06258ad66efe2dedbf67809ebc107a55757b8a4543af77982f55ff6c067`  
		Last Modified: Thu, 22 Oct 2020 02:58:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c878f3bd7fd82dbe36e4d303393019e0703f5e67ebb74f817f7369f072e6532`  
		Last Modified: Fri, 06 Nov 2020 19:34:26 GMT  
		Size: 105.8 MB (105776540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980f7999cd7558faa66bb1ae504f8c1e22e4881e3d71f3fd3aa2a4cb8ca7db13`  
		Last Modified: Fri, 06 Nov 2020 19:34:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85206d14782c0fb54511c935afb74a9e81b7c4bf73176614eadd044297188377`  
		Last Modified: Fri, 06 Nov 2020 20:40:48 GMT  
		Size: 8.4 MB (8352230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5f0e7da5d92511b1993de47afc01232a9b314ea3b5e854b83b0713acab7906`  
		Last Modified: Fri, 06 Nov 2020 20:40:47 GMT  
		Size: 1.4 MB (1388754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bfc26b576e6aeb40246d6645a95abab375e81757ab7a3095af525666ae295a`  
		Last Modified: Fri, 06 Nov 2020 20:40:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:0cc26b33a1fe2b1ae4225a57d25846d69166be17484f8f847a3b835626c2df47
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548826368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5551c0b95fd6fba6bbdbef91ad7fd2edce9814d5127b0dd65274fd6fa964da48`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:27:03 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:27:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:28:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:28:38 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:29:02 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:15:07 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:17:47 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:17:49 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:57:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:57:51 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:57:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:58:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:58:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23a75d88f9f5980bb112e2c28248975f107144d8d2e40dc4755e2a09f5e56df`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea6d8b9d9b014ffa471b7bb8882ddb7e9d378ddcacc099f0710073bd6361b9`  
		Last Modified: Wed, 14 Oct 2020 12:50:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75c1905c0573cc5706bc066d23624f0e92a8871832c744fbe7eabdcbc6f8a85`  
		Last Modified: Wed, 14 Oct 2020 12:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938695376d9deeba8819539ff3245935c28f93229d1c332bb8b6a16e67013fbc`  
		Last Modified: Wed, 14 Oct 2020 12:50:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41106c6a476cf9666c6d8c3c853c982a841c29db05b3ef8a072baba537b6d74c`  
		Last Modified: Wed, 14 Oct 2020 12:50:48 GMT  
		Size: 34.3 MB (34312667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6d6258831f87f3b455e6316e2bed430465a760272614de7cdd28c7c6e9f3e`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e3f66638c4d5ce9adba16e49844f57efbab1d628d9d6c73133511b7c1c3892`  
		Last Modified: Wed, 14 Oct 2020 12:50:20 GMT  
		Size: 310.5 KB (310525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d8771646c530e34e5045246ce3b2ebe859c4f5be8c444ec5dba3c382bee3a`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652b8eae6f5ed9dba044dae68e11cd7a4320ee55b36f6016b2199b9f3316c31a`  
		Last Modified: Fri, 06 Nov 2020 19:34:01 GMT  
		Size: 138.3 MB (138329448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadb866080cf8fd8fb40d4722c8642031ac09e46b3ad9f8029cc13e4531e8d63`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2a55f83bf6210220425240b3a2382a1dcede45856c71588260c441d4d560a`  
		Last Modified: Fri, 06 Nov 2020 20:00:57 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5aeaca4a088d8f8b44454e8a71c131afb3faae25b4a31ffbcbd0e36e46c2a7`  
		Last Modified: Fri, 06 Nov 2020 20:00:55 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a62e98c257ab6518929697507951e1378383d5c25b708c0a5bdc20bb2f4cb`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02e4c481fcbe14f0818df1d4a577730f215914c3f7a4c44f3926c08ec354a2d`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3aba19aa6c0c8a874ce9d79d9e6d91ce5040a8037854a0d8c95fa1cf811030`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.8 MB (1768657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b33a039b5dad3077c7f441fbcd6321bccc7bb5d8d9db0b77f563baa66aab5d`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:91615621bb5d8f928cae33580878a3a0e4c360d2bd1a5078bd5579ffc1f65586
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941036189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69fe55d922052ef8814dc705972036b5fa14d96cea24bb078c82eded58a8536`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:31:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:31:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:33:58 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:35:13 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:18:04 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:21:38 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:21:40 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:58:23 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:58:24 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:58:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:59:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:59:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528ba1d9759adcc464112008fe49672e1f545981d69bab31186587ab32f92138`  
		Last Modified: Wed, 14 Oct 2020 12:51:33 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf4e6180661653575845d30a4d882dea92f395cb540b1cdf91170e9ee58731`  
		Last Modified: Wed, 14 Oct 2020 12:51:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e973f094614bb2cebe16df6f6004c05895ed077151aecdbbd0c476513054fc`  
		Last Modified: Wed, 14 Oct 2020 12:51:25 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089b875ac355097876e23760dd2166f096a8645e312660ffd3c0e617a2df9a0`  
		Last Modified: Wed, 14 Oct 2020 12:51:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a016b666d0691307c6414d84c36eb82de4b2fc4d74dd04c75f632dc3a78c`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 35.0 MB (35016991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4d95d13c0a45aa19a623e51cb112530a589a3a4d15d5c119610f8196912fab`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf8226941bb8f5af9f2be8fdb54da3e3caef344b0061a73e3debde23a55e98f`  
		Last Modified: Wed, 14 Oct 2020 12:51:24 GMT  
		Size: 9.9 MB (9870100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e5f43d50387ad619b863923b75cdf46053a8edd9954ec6e5bcdd6b90719c56`  
		Last Modified: Fri, 06 Nov 2020 19:34:21 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce913b69c36a8d04261681b1d8cde7dd3ec67f8275dc2c21b7b9d42074721ec1`  
		Last Modified: Fri, 06 Nov 2020 19:34:56 GMT  
		Size: 143.5 MB (143487215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75231de833daeca0a14373f4edb90eeaa4ec81d6fe961b4de6529a89c511ca2c`  
		Last Modified: Fri, 06 Nov 2020 19:34:20 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1a4d62df1ffdb8baac455f20994d1992ae918702aeb6c3c3171001c6870a73`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf2e1fbaf300596e6987a1c0f473fc2dde64d5a816b13f3aaf21cf2e4cc3332`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a001d9ed8d402d293907ee530361c27f8b6f076be745516b37580b9fbb73b9c2`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1740d81d6c6721405d45f80726a0ebcd3dc0d0de5da905fb41d182ca78a921ec`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d14e15f1dc7fa0765eb82fe118a91aa20fbef9c5c677cde9a38ddc0890ae260`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 11.3 MB (11295267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb21d7c1a6d233e3c34e5e883d3bc762275075111197136cb6b326f4ea46056`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:c243e906eda12ce67b24e021caa307808407005fc1a8197284d9b70daaf2a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:fc73b9cce8ce070df5bd3bf94ff6f0dba5ab3a82359d7313d216b71585946551
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119452255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7c4becdaa4921f4830aa5898531fb59bdb497d37b6a9109fc9d2189b47316d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:34:56 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:34:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:34:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:35:51 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:38:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:38:42 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:38:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:38:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:38:44 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:18:13 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:18:13 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:18:13 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:18:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:18:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:18:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:18:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7d3d256c8367c41c431143c63d083a25dd62ec9ee9d9773dd9e6c7b70ec9e`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9db76c5a1d06710ed4f3073476b2d883ff8e911f8e47c558bc4a8d1d8663fa`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f88ce657dbabff9f6a04034006ee66c6ecfb0d54bb599525d9c8d9ad91a22`  
		Last Modified: Fri, 06 Nov 2020 19:47:52 GMT  
		Size: 106.7 MB (106656837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dc1c79fe7f44761a5d11f6f64f4ec7142a59bf2225b8a1e5554ed551654797`  
		Last Modified: Fri, 06 Nov 2020 19:47:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec1cb62beafb625b4104c718b0c582ffdcc06f9ca5efd25549b3c1905cf16`  
		Last Modified: Fri, 06 Nov 2020 21:18:36 GMT  
		Size: 8.3 MB (8309861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461a7017d5ae9ee39afa73c0013aa3fc8bcb8518db59843e7eff18a067c4142`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 1.4 MB (1407206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd8af862e3e9052217f29783b7f6e65c65f057dd9aa35f585882f13c0b34cde`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89a73c5f4ae51892063fa87a4c7bbcb1311e07f70d70df7e2d8a03c7f61eac7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114664382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e85a7472aacc21b210dfa3f511a5358983fb44fab90d8bd81956f0974cba9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:07:24 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:07:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:53:45 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:56:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:56:20 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:56:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:56:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:56:23 GMT
WORKDIR /go
# Fri, 06 Nov 2020 19:22:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 19:22:55 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:22:56 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:22:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:23:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 19:23:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 19:23:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20cc27a60e8ac1bf56dec787d3d52ba856e657179cfd56050036db79abb4267`  
		Last Modified: Thu, 22 Oct 2020 05:34:55 GMT  
		Size: 281.0 KB (280971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecce92c3d2de40638d73e682dec26c2b79a055e85c8d70b88f4ccb9485bb9c9`  
		Last Modified: Thu, 22 Oct 2020 05:34:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bea26c6de29e9326bc228c64da95fcd54b3d1f9354f1165eafc349994db0f8`  
		Last Modified: Fri, 06 Nov 2020 19:04:15 GMT  
		Size: 102.5 MB (102524592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e5877f5507358b36e32b963095c3caf40f40a6eec614d816a33f2f2ebfd55`  
		Last Modified: Fri, 06 Nov 2020 19:03:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81d2f79a49d963d6cbaa15e2327930649da636b6b369f88d7c19d733c5eb296`  
		Last Modified: Fri, 06 Nov 2020 19:23:35 GMT  
		Size: 7.9 MB (7928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea3d4a6a9133060470b288519140837675e4773f464432a967a4e3a080ac986`  
		Last Modified: Fri, 06 Nov 2020 19:23:34 GMT  
		Size: 1.3 MB (1327357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bf1d579fdbbae7b37fb9ef4d32de07ce43408b789fded70f7baeabe507c78e`  
		Last Modified: Fri, 06 Nov 2020 19:23:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:931f32bb911ba0de19091cc5d1b56e45a88159343a6782497a325539a5f88e3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113487064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8b5eddc6ef348d71b508ab97a7dd567f6a977bac2cdd3828e499bb4440c38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:21:35 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:23:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:23:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:39:15 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:41:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:41:25 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:41:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:41:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:41:29 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:27:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:27:33 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:27:34 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:27:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:27:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:27:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:27:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b753cfc04fdce9640aac1e7a4b3e7ce15fa60b8e357376e42f294f463a6e890`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 280.1 KB (280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90c422e5e4668cb4140aadb622d734faa93c81cc1e283da9b08bbbc65c45c5`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b476d7beedfa2137a0fef6e60a4484b51d77830c70ebcff073ccc374056e2e0c`  
		Last Modified: Fri, 06 Nov 2020 19:49:31 GMT  
		Size: 102.3 MB (102329948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd72c431842e0aeea9c3f8328785176b40806958c71f4fefebd421c3518571`  
		Last Modified: Fri, 06 Nov 2020 19:48:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7315086fe1858140ae2a84a77af42759c8f4e82b0a4df1b0529669c2e6208cc`  
		Last Modified: Fri, 06 Nov 2020 20:28:06 GMT  
		Size: 7.1 MB (7144798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca52434a632fe2aa304e8fd42e54bcf29afa42ffe1b722340860d449685dae`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 1.3 MB (1325846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e36ff02f43b3832542cf4347e8366772d4877647f3fc2c7a0624aa885219ad`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:30fe2a9e24366ead2b615623a7637421e1b02f3f5404268d728e823253d1d889
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114775259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a06ec2afc931f2326cd6e8f7d6ead1bd093d76c1dac1e006111bb4cdc22354`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:08:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 04:09:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:09:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:18:49 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:20:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:20:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:20:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:20:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:20:48 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:09:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:09:26 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:09:26 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:09:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:09:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:09:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:09:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4357932f1b6fb010e1461cc5c673712fb832ac44ee627c691db0b64adf95d13`  
		Last Modified: Thu, 22 Oct 2020 04:28:32 GMT  
		Size: 281.2 KB (281230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c013af1878066e59b688e31fd962e7267430963de27c5257241e3c223aa1d6`  
		Last Modified: Thu, 22 Oct 2020 04:28:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b36744bb2cb0aa83f712639340b2320bd38128965d09ffffa43856a210f9e5`  
		Last Modified: Fri, 06 Nov 2020 19:28:03 GMT  
		Size: 102.0 MB (101976695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620dd3e3aa585cedfbb73c7698bdfc75f79b8a92e0bd7e7d5dcc2041012893be`  
		Last Modified: Fri, 06 Nov 2020 19:27:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803037031a1f00d46e050e3bb3fca389a0ac1939d4cb43c1548f0d72bb47cb5`  
		Last Modified: Fri, 06 Nov 2020 21:10:01 GMT  
		Size: 8.5 MB (8499884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840674c7f6a6769677bea40173b44c0cdf85447290b9521805050cac0b25df6`  
		Last Modified: Fri, 06 Nov 2020 21:09:59 GMT  
		Size: 1.3 MB (1310181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a9e6466e2de25170ecf4a3eb0a32a4dd076dcf8faabf6f80120fc45f1491`  
		Last Modified: Fri, 06 Nov 2020 21:09:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51c882c7f333a86293123c5c9f7dde2e2d733761be27faa8ba679fd25880dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113944446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed252304acf0e273fc3538fbd970d4bfaa5fe502c7fe021fcb299559f389f4be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:27:26 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 13:27:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:27:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:32:30 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:34:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:34:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:34:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:35:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:35:27 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:51:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:51:06 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:51:09 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:51:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:51:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:51:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:51:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9900411dc7c8c88618743573bf89478d726007403bd002d8b00d21b7fecd40a`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 283.2 KB (283205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbd106374e3baf7eb8e3d8f7ffd4c364a35e57dcb3a89f8a153327a4c3fa3f9`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec3950b2a73c219aef5a15211d4abc2d9a5af90823e42083fdace116f7c476`  
		Last Modified: Fri, 06 Nov 2020 18:47:04 GMT  
		Size: 100.6 MB (100649515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccf6cddd12f97382439bc21574bae904a64d8e1f96a30b0ac21e85f7aa112d7`  
		Last Modified: Fri, 06 Nov 2020 18:46:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94e9e52826c34d57af8656e0e5b92258140dd8b57f186db8861f03ef5e4f00`  
		Last Modified: Fri, 06 Nov 2020 21:52:28 GMT  
		Size: 8.9 MB (8920000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75746c400be689f32365c8fb16a86def9e748eaf0507246876dade9fa125e78c`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 1.3 MB (1287791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0695a08f39b4841501692759a1c562a2e2c4c13bac546fbed9a962411082c141`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:b252d4071ae496dbd6a16de864a46fe6d0629a7d35c8b123c58e19261db37455
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118365434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216ff73b58d08ff9b58e775653d0f32630eb7df17076e32df1011ce6bafaed1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:53:28 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 02:53:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:53:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:23:44 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:25:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:26:04 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:26:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:26:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:26:07 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:40:05 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:40:07 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:40:07 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:40:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:40:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:40:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:40:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5139d7663b8674a989574c2161166fb137f26ef16b2f701159c126628be75101`  
		Last Modified: Thu, 22 Oct 2020 02:58:32 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31a06258ad66efe2dedbf67809ebc107a55757b8a4543af77982f55ff6c067`  
		Last Modified: Thu, 22 Oct 2020 02:58:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c878f3bd7fd82dbe36e4d303393019e0703f5e67ebb74f817f7369f072e6532`  
		Last Modified: Fri, 06 Nov 2020 19:34:26 GMT  
		Size: 105.8 MB (105776540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980f7999cd7558faa66bb1ae504f8c1e22e4881e3d71f3fd3aa2a4cb8ca7db13`  
		Last Modified: Fri, 06 Nov 2020 19:34:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85206d14782c0fb54511c935afb74a9e81b7c4bf73176614eadd044297188377`  
		Last Modified: Fri, 06 Nov 2020 20:40:48 GMT  
		Size: 8.4 MB (8352230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5f0e7da5d92511b1993de47afc01232a9b314ea3b5e854b83b0713acab7906`  
		Last Modified: Fri, 06 Nov 2020 20:40:47 GMT  
		Size: 1.4 MB (1388754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bfc26b576e6aeb40246d6645a95abab375e81757ab7a3095af525666ae295a`  
		Last Modified: Fri, 06 Nov 2020 20:40:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:b38981e5323bcf982907423ded683b2c6f8548a129819434392a2413e15fc1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:0cc26b33a1fe2b1ae4225a57d25846d69166be17484f8f847a3b835626c2df47
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548826368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5551c0b95fd6fba6bbdbef91ad7fd2edce9814d5127b0dd65274fd6fa964da48`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:27:03 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:27:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:28:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:28:38 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:29:02 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:15:07 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:17:47 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:17:49 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:57:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:57:51 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:57:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:58:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:58:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23a75d88f9f5980bb112e2c28248975f107144d8d2e40dc4755e2a09f5e56df`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea6d8b9d9b014ffa471b7bb8882ddb7e9d378ddcacc099f0710073bd6361b9`  
		Last Modified: Wed, 14 Oct 2020 12:50:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75c1905c0573cc5706bc066d23624f0e92a8871832c744fbe7eabdcbc6f8a85`  
		Last Modified: Wed, 14 Oct 2020 12:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938695376d9deeba8819539ff3245935c28f93229d1c332bb8b6a16e67013fbc`  
		Last Modified: Wed, 14 Oct 2020 12:50:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41106c6a476cf9666c6d8c3c853c982a841c29db05b3ef8a072baba537b6d74c`  
		Last Modified: Wed, 14 Oct 2020 12:50:48 GMT  
		Size: 34.3 MB (34312667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6d6258831f87f3b455e6316e2bed430465a760272614de7cdd28c7c6e9f3e`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e3f66638c4d5ce9adba16e49844f57efbab1d628d9d6c73133511b7c1c3892`  
		Last Modified: Wed, 14 Oct 2020 12:50:20 GMT  
		Size: 310.5 KB (310525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d8771646c530e34e5045246ce3b2ebe859c4f5be8c444ec5dba3c382bee3a`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652b8eae6f5ed9dba044dae68e11cd7a4320ee55b36f6016b2199b9f3316c31a`  
		Last Modified: Fri, 06 Nov 2020 19:34:01 GMT  
		Size: 138.3 MB (138329448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadb866080cf8fd8fb40d4722c8642031ac09e46b3ad9f8029cc13e4531e8d63`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2a55f83bf6210220425240b3a2382a1dcede45856c71588260c441d4d560a`  
		Last Modified: Fri, 06 Nov 2020 20:00:57 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5aeaca4a088d8f8b44454e8a71c131afb3faae25b4a31ffbcbd0e36e46c2a7`  
		Last Modified: Fri, 06 Nov 2020 20:00:55 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a62e98c257ab6518929697507951e1378383d5c25b708c0a5bdc20bb2f4cb`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02e4c481fcbe14f0818df1d4a577730f215914c3f7a4c44f3926c08ec354a2d`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3aba19aa6c0c8a874ce9d79d9e6d91ce5040a8037854a0d8c95fa1cf811030`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.8 MB (1768657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b33a039b5dad3077c7f441fbcd6321bccc7bb5d8d9db0b77f563baa66aab5d`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:2689ae5b16484bd1a074522d9ae004e9664036b4043a3bafe8443620784dbb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:91615621bb5d8f928cae33580878a3a0e4c360d2bd1a5078bd5579ffc1f65586
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941036189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69fe55d922052ef8814dc705972036b5fa14d96cea24bb078c82eded58a8536`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:31:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:31:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:33:58 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:35:13 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:18:04 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:21:38 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:21:40 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:58:23 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:58:24 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:58:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:59:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:59:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528ba1d9759adcc464112008fe49672e1f545981d69bab31186587ab32f92138`  
		Last Modified: Wed, 14 Oct 2020 12:51:33 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf4e6180661653575845d30a4d882dea92f395cb540b1cdf91170e9ee58731`  
		Last Modified: Wed, 14 Oct 2020 12:51:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e973f094614bb2cebe16df6f6004c05895ed077151aecdbbd0c476513054fc`  
		Last Modified: Wed, 14 Oct 2020 12:51:25 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089b875ac355097876e23760dd2166f096a8645e312660ffd3c0e617a2df9a0`  
		Last Modified: Wed, 14 Oct 2020 12:51:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a016b666d0691307c6414d84c36eb82de4b2fc4d74dd04c75f632dc3a78c`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 35.0 MB (35016991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4d95d13c0a45aa19a623e51cb112530a589a3a4d15d5c119610f8196912fab`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf8226941bb8f5af9f2be8fdb54da3e3caef344b0061a73e3debde23a55e98f`  
		Last Modified: Wed, 14 Oct 2020 12:51:24 GMT  
		Size: 9.9 MB (9870100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e5f43d50387ad619b863923b75cdf46053a8edd9954ec6e5bcdd6b90719c56`  
		Last Modified: Fri, 06 Nov 2020 19:34:21 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce913b69c36a8d04261681b1d8cde7dd3ec67f8275dc2c21b7b9d42074721ec1`  
		Last Modified: Fri, 06 Nov 2020 19:34:56 GMT  
		Size: 143.5 MB (143487215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75231de833daeca0a14373f4edb90eeaa4ec81d6fe961b4de6529a89c511ca2c`  
		Last Modified: Fri, 06 Nov 2020 19:34:20 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1a4d62df1ffdb8baac455f20994d1992ae918702aeb6c3c3171001c6870a73`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf2e1fbaf300596e6987a1c0f473fc2dde64d5a816b13f3aaf21cf2e4cc3332`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a001d9ed8d402d293907ee530361c27f8b6f076be745516b37580b9fbb73b9c2`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1740d81d6c6721405d45f80726a0ebcd3dc0d0de5da905fb41d182ca78a921ec`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d14e15f1dc7fa0765eb82fe118a91aa20fbef9c5c677cde9a38ddc0890ae260`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 11.3 MB (11295267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb21d7c1a6d233e3c34e5e883d3bc762275075111197136cb6b326f4ea46056`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:0cc9e18409440159fbf2ac241bce180b0214fc5d2358aa87fedf1189394d7469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d720e5ab1579e03c0f86de11950434367743bdf8212a4501cd971c29d16942a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:155acd240efff18a38a7aff934be0f6976aeb1c76139025671c9833ed160c840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:ea06de9c9cb10eacb9f77e50817d2ad8dd63c977549f26c19d57df1a194fefdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:4ebad49f78a3f98164d89431978046ee6e94f1e8a70454abc7f49ce1a5ee7826
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb0137bab0e21a92b0bc9ec1cc22c259b097d5bf239b161ae1eac0de1833e67`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:33:22 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 04:33:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 04:33:55 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 04:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 04:34:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 04:34:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 04:34:02 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 04:34:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 80
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 443
# Thu, 22 Oct 2020 04:34:06 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 04:34:06 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 04:34:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e2d825895b6421ca5dbd63db0d99f790ef84a84c7bcaff51e60b654397858`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 300.0 KB (299956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaf2e3dee2e74b401fce928bf9502e48df68da4e8c1933bfd6b00b1137529fc`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 5.8 KB (5754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2215cf93250599c5db984cee0fddd5d0cd59ef035ab5a317387b67211bde86d`  
		Last Modified: Thu, 22 Oct 2020 04:35:06 GMT  
		Size: 11.5 MB (11532508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060365e49ba5ee96a2859e269b366f5a5c9f386e5bdbf07d2ef31b1fc6934baa`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:abba73dc860b2f35703cb7d27f08baf5bfc084e18e627b94661d01a8e2befdaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13784259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0aad5a281913821dd39ffed5e144daae22ac81ac4314731395ab65eedde72a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:58:10 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:58:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:58:46 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:58:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:58:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:59:00 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:59:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:59:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:59:03 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:59:08 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:59:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:59:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:59:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:59:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:59:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:59:15 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:59:19 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:59:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:59:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:59:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7369c3ac4b39c55c74e96dd3eb61ac2fa65e5671b1c2acca9697a7c9d20c3cf`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 300.1 KB (300086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8f4045920069dff3382a5993783c5d846d9e28d0f5a63c475ed298fce0abb7`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db6bde4735da15e5db23ad62f3d64d78aed8713a40d12547f5538c15c90f9da`  
		Last Modified: Thu, 22 Oct 2020 03:00:06 GMT  
		Size: 10.9 MB (10876280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a95efd7a14ed98a53a238da45faa7e3b0fdd2a93529b83bfe9d0823dafac67c`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8cf66cbe3c03273ca54bdab908092a6a9b9f02d39595ed15b1111f1465430426
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20723dea614fc40d9f3cb59eddd33bf0e89dfda3f8ed4a7b404ef334632a4b9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:04:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 03:05:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 03:05:45 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 03:05:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 03:05:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 03:05:54 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 03:05:55 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 03:05:56 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 03:05:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 03:06:01 GMT
EXPOSE 80
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 443
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 03:06:03 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 03:06:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a8e7fe5034ac502626b0a921d79be80c092890176e33b236c489d6f00710a2`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 299.2 KB (299211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db75acdaca15b1e81890f29b3b757fcc73e7a69a55f5ed659bf800f6340108`  
		Last Modified: Thu, 22 Oct 2020 03:06:43 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2197c38adf245bca8f229a4cd718c4d0f619a87bae5786572ccdac1a286882c`  
		Last Modified: Thu, 22 Oct 2020 03:06:46 GMT  
		Size: 10.9 MB (10854384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0104bc6a595940856019d00d9ff8e04365338a7964d948b64cc44bf73cc59e`  
		Last Modified: Thu, 22 Oct 2020 03:06:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:da121cf42d1759ed03af3130533d365c365af1d738d550744ad863e05e64cf46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13540356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b4aa38988ab2442575062d99c3cb44976de6c227256c118f35340e7c21c303`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:40:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:40:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:40:57 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:07 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:09 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:10 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:10 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbde357077a97c0f831033bf03c9828203cb7e3e6cb33217ce4d7cfd71c931`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 300.3 KB (300348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a5ab0aa923ce1fe233b904008bbf932c4787f48bcd59f07a85616147b7cbc3`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc398339860cf826624c9c22b5de9b45a193260e2ff24826d210b493483398f`  
		Last Modified: Thu, 22 Oct 2020 02:41:59 GMT  
		Size: 10.5 MB (10527465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6e7d61d1d4a00550447ea1f67edc0463cc527e49356e98959edfafba0df879`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:09208042b4d19d7ed87b51b99dc20b390dab20d9ae7e235a62a3af3aaf472bd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13291756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5c77284adc35481d13003d31a866f637b6eaf9f5764f667e536db79ce23129`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:39:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 13:44:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 13:44:04 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 13:44:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 13:44:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:44:33 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 13:44:37 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 13:44:40 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 13:44:44 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 13:44:48 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 13:44:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 13:44:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 13:45:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 13:45:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 13:45:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 13:45:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 13:45:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 13:45:23 GMT
EXPOSE 80
# Thu, 22 Oct 2020 13:45:26 GMT
EXPOSE 443
# Thu, 22 Oct 2020 13:45:30 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 13:45:35 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 13:45:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a4964211b7ce86541a0c1dad8ef3800ec38a3ca90aff94b76759b4cb8e279`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 302.3 KB (302327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dd938ef3e3eae8509deda8fab9ab5f9344169d912e35a802633e799feed1bb`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe23c296ee12ee12ef84dbabbb4f7bf0362a9a12b684782ebd3f44a97c8fcf8e`  
		Last Modified: Thu, 22 Oct 2020 13:47:55 GMT  
		Size: 10.2 MB (10180223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2f3c084745fecafaa9ff33626a81124f2d70267ceee705da555714238bfa1`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:3e18b421d651721239cb3422bc890d1211535681219b7696816f487b4cebc4ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14074857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d5562f1d148d3d67ff7f5995be8f860553ad0f3d07091335643306b83385e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:41:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:41:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:41 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f988ff23f3cbb35bfed69e33f3b7ee69403bfae4f46363a08eea4830053e9c`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 300.5 KB (300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd6a4e0db99510879c5dfceabd1e629a0692c4544bb0da34971f8722b881e92`  
		Last Modified: Thu, 22 Oct 2020 02:42:09 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e13b938aa802e74610585cabba77d625db4baf219f577a81195c272408c7d3`  
		Last Modified: Thu, 22 Oct 2020 02:42:16 GMT  
		Size: 11.2 MB (11202559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a221fff082950a8a98db12eb99f532a39008f0d6e21684bc1aed06fa1ed2a764`  
		Last Modified: Thu, 22 Oct 2020 02:42:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:a3a3208982f94bce254e689780d79e0457b3b76d5b9d854628caf090504a3729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:fc73b9cce8ce070df5bd3bf94ff6f0dba5ab3a82359d7313d216b71585946551
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119452255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7c4becdaa4921f4830aa5898531fb59bdb497d37b6a9109fc9d2189b47316d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:34:56 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:34:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:34:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:35:51 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:38:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:38:42 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:38:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:38:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:38:44 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:18:13 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:18:13 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:18:13 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:18:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:18:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:18:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:18:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7d3d256c8367c41c431143c63d083a25dd62ec9ee9d9773dd9e6c7b70ec9e`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9db76c5a1d06710ed4f3073476b2d883ff8e911f8e47c558bc4a8d1d8663fa`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f88ce657dbabff9f6a04034006ee66c6ecfb0d54bb599525d9c8d9ad91a22`  
		Last Modified: Fri, 06 Nov 2020 19:47:52 GMT  
		Size: 106.7 MB (106656837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dc1c79fe7f44761a5d11f6f64f4ec7142a59bf2225b8a1e5554ed551654797`  
		Last Modified: Fri, 06 Nov 2020 19:47:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec1cb62beafb625b4104c718b0c582ffdcc06f9ca5efd25549b3c1905cf16`  
		Last Modified: Fri, 06 Nov 2020 21:18:36 GMT  
		Size: 8.3 MB (8309861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461a7017d5ae9ee39afa73c0013aa3fc8bcb8518db59843e7eff18a067c4142`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 1.4 MB (1407206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd8af862e3e9052217f29783b7f6e65c65f057dd9aa35f585882f13c0b34cde`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89a73c5f4ae51892063fa87a4c7bbcb1311e07f70d70df7e2d8a03c7f61eac7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114664382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e85a7472aacc21b210dfa3f511a5358983fb44fab90d8bd81956f0974cba9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:07:24 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:07:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:53:45 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:56:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:56:20 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:56:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:56:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:56:23 GMT
WORKDIR /go
# Fri, 06 Nov 2020 19:22:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 19:22:55 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:22:56 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:22:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:23:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 19:23:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 19:23:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20cc27a60e8ac1bf56dec787d3d52ba856e657179cfd56050036db79abb4267`  
		Last Modified: Thu, 22 Oct 2020 05:34:55 GMT  
		Size: 281.0 KB (280971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecce92c3d2de40638d73e682dec26c2b79a055e85c8d70b88f4ccb9485bb9c9`  
		Last Modified: Thu, 22 Oct 2020 05:34:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bea26c6de29e9326bc228c64da95fcd54b3d1f9354f1165eafc349994db0f8`  
		Last Modified: Fri, 06 Nov 2020 19:04:15 GMT  
		Size: 102.5 MB (102524592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e5877f5507358b36e32b963095c3caf40f40a6eec614d816a33f2f2ebfd55`  
		Last Modified: Fri, 06 Nov 2020 19:03:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81d2f79a49d963d6cbaa15e2327930649da636b6b369f88d7c19d733c5eb296`  
		Last Modified: Fri, 06 Nov 2020 19:23:35 GMT  
		Size: 7.9 MB (7928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea3d4a6a9133060470b288519140837675e4773f464432a967a4e3a080ac986`  
		Last Modified: Fri, 06 Nov 2020 19:23:34 GMT  
		Size: 1.3 MB (1327357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bf1d579fdbbae7b37fb9ef4d32de07ce43408b789fded70f7baeabe507c78e`  
		Last Modified: Fri, 06 Nov 2020 19:23:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:931f32bb911ba0de19091cc5d1b56e45a88159343a6782497a325539a5f88e3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113487064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8b5eddc6ef348d71b508ab97a7dd567f6a977bac2cdd3828e499bb4440c38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:21:35 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:23:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:23:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:39:15 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:41:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:41:25 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:41:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:41:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:41:29 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:27:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:27:33 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:27:34 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:27:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:27:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:27:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:27:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b753cfc04fdce9640aac1e7a4b3e7ce15fa60b8e357376e42f294f463a6e890`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 280.1 KB (280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90c422e5e4668cb4140aadb622d734faa93c81cc1e283da9b08bbbc65c45c5`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b476d7beedfa2137a0fef6e60a4484b51d77830c70ebcff073ccc374056e2e0c`  
		Last Modified: Fri, 06 Nov 2020 19:49:31 GMT  
		Size: 102.3 MB (102329948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd72c431842e0aeea9c3f8328785176b40806958c71f4fefebd421c3518571`  
		Last Modified: Fri, 06 Nov 2020 19:48:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7315086fe1858140ae2a84a77af42759c8f4e82b0a4df1b0529669c2e6208cc`  
		Last Modified: Fri, 06 Nov 2020 20:28:06 GMT  
		Size: 7.1 MB (7144798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca52434a632fe2aa304e8fd42e54bcf29afa42ffe1b722340860d449685dae`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 1.3 MB (1325846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e36ff02f43b3832542cf4347e8366772d4877647f3fc2c7a0624aa885219ad`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:30fe2a9e24366ead2b615623a7637421e1b02f3f5404268d728e823253d1d889
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114775259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a06ec2afc931f2326cd6e8f7d6ead1bd093d76c1dac1e006111bb4cdc22354`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:08:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 04:09:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:09:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:18:49 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:20:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:20:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:20:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:20:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:20:48 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:09:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:09:26 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:09:26 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:09:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:09:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:09:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:09:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4357932f1b6fb010e1461cc5c673712fb832ac44ee627c691db0b64adf95d13`  
		Last Modified: Thu, 22 Oct 2020 04:28:32 GMT  
		Size: 281.2 KB (281230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c013af1878066e59b688e31fd962e7267430963de27c5257241e3c223aa1d6`  
		Last Modified: Thu, 22 Oct 2020 04:28:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b36744bb2cb0aa83f712639340b2320bd38128965d09ffffa43856a210f9e5`  
		Last Modified: Fri, 06 Nov 2020 19:28:03 GMT  
		Size: 102.0 MB (101976695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620dd3e3aa585cedfbb73c7698bdfc75f79b8a92e0bd7e7d5dcc2041012893be`  
		Last Modified: Fri, 06 Nov 2020 19:27:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803037031a1f00d46e050e3bb3fca389a0ac1939d4cb43c1548f0d72bb47cb5`  
		Last Modified: Fri, 06 Nov 2020 21:10:01 GMT  
		Size: 8.5 MB (8499884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840674c7f6a6769677bea40173b44c0cdf85447290b9521805050cac0b25df6`  
		Last Modified: Fri, 06 Nov 2020 21:09:59 GMT  
		Size: 1.3 MB (1310181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a9e6466e2de25170ecf4a3eb0a32a4dd076dcf8faabf6f80120fc45f1491`  
		Last Modified: Fri, 06 Nov 2020 21:09:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51c882c7f333a86293123c5c9f7dde2e2d733761be27faa8ba679fd25880dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113944446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed252304acf0e273fc3538fbd970d4bfaa5fe502c7fe021fcb299559f389f4be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:27:26 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 13:27:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:27:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:32:30 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:34:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:34:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:34:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:35:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:35:27 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:51:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:51:06 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:51:09 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:51:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:51:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:51:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:51:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9900411dc7c8c88618743573bf89478d726007403bd002d8b00d21b7fecd40a`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 283.2 KB (283205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbd106374e3baf7eb8e3d8f7ffd4c364a35e57dcb3a89f8a153327a4c3fa3f9`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec3950b2a73c219aef5a15211d4abc2d9a5af90823e42083fdace116f7c476`  
		Last Modified: Fri, 06 Nov 2020 18:47:04 GMT  
		Size: 100.6 MB (100649515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccf6cddd12f97382439bc21574bae904a64d8e1f96a30b0ac21e85f7aa112d7`  
		Last Modified: Fri, 06 Nov 2020 18:46:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94e9e52826c34d57af8656e0e5b92258140dd8b57f186db8861f03ef5e4f00`  
		Last Modified: Fri, 06 Nov 2020 21:52:28 GMT  
		Size: 8.9 MB (8920000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75746c400be689f32365c8fb16a86def9e748eaf0507246876dade9fa125e78c`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 1.3 MB (1287791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0695a08f39b4841501692759a1c562a2e2c4c13bac546fbed9a962411082c141`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:b252d4071ae496dbd6a16de864a46fe6d0629a7d35c8b123c58e19261db37455
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118365434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216ff73b58d08ff9b58e775653d0f32630eb7df17076e32df1011ce6bafaed1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:53:28 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 02:53:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:53:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:23:44 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:25:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:26:04 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:26:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:26:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:26:07 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:40:05 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:40:07 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:40:07 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:40:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:40:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:40:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:40:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5139d7663b8674a989574c2161166fb137f26ef16b2f701159c126628be75101`  
		Last Modified: Thu, 22 Oct 2020 02:58:32 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31a06258ad66efe2dedbf67809ebc107a55757b8a4543af77982f55ff6c067`  
		Last Modified: Thu, 22 Oct 2020 02:58:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c878f3bd7fd82dbe36e4d303393019e0703f5e67ebb74f817f7369f072e6532`  
		Last Modified: Fri, 06 Nov 2020 19:34:26 GMT  
		Size: 105.8 MB (105776540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980f7999cd7558faa66bb1ae504f8c1e22e4881e3d71f3fd3aa2a4cb8ca7db13`  
		Last Modified: Fri, 06 Nov 2020 19:34:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85206d14782c0fb54511c935afb74a9e81b7c4bf73176614eadd044297188377`  
		Last Modified: Fri, 06 Nov 2020 20:40:48 GMT  
		Size: 8.4 MB (8352230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5f0e7da5d92511b1993de47afc01232a9b314ea3b5e854b83b0713acab7906`  
		Last Modified: Fri, 06 Nov 2020 20:40:47 GMT  
		Size: 1.4 MB (1388754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bfc26b576e6aeb40246d6645a95abab375e81757ab7a3095af525666ae295a`  
		Last Modified: Fri, 06 Nov 2020 20:40:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:0cc26b33a1fe2b1ae4225a57d25846d69166be17484f8f847a3b835626c2df47
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548826368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5551c0b95fd6fba6bbdbef91ad7fd2edce9814d5127b0dd65274fd6fa964da48`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:27:03 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:27:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:28:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:28:38 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:29:02 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:15:07 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:17:47 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:17:49 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:57:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:57:51 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:57:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:58:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:58:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23a75d88f9f5980bb112e2c28248975f107144d8d2e40dc4755e2a09f5e56df`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea6d8b9d9b014ffa471b7bb8882ddb7e9d378ddcacc099f0710073bd6361b9`  
		Last Modified: Wed, 14 Oct 2020 12:50:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75c1905c0573cc5706bc066d23624f0e92a8871832c744fbe7eabdcbc6f8a85`  
		Last Modified: Wed, 14 Oct 2020 12:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938695376d9deeba8819539ff3245935c28f93229d1c332bb8b6a16e67013fbc`  
		Last Modified: Wed, 14 Oct 2020 12:50:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41106c6a476cf9666c6d8c3c853c982a841c29db05b3ef8a072baba537b6d74c`  
		Last Modified: Wed, 14 Oct 2020 12:50:48 GMT  
		Size: 34.3 MB (34312667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6d6258831f87f3b455e6316e2bed430465a760272614de7cdd28c7c6e9f3e`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e3f66638c4d5ce9adba16e49844f57efbab1d628d9d6c73133511b7c1c3892`  
		Last Modified: Wed, 14 Oct 2020 12:50:20 GMT  
		Size: 310.5 KB (310525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d8771646c530e34e5045246ce3b2ebe859c4f5be8c444ec5dba3c382bee3a`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652b8eae6f5ed9dba044dae68e11cd7a4320ee55b36f6016b2199b9f3316c31a`  
		Last Modified: Fri, 06 Nov 2020 19:34:01 GMT  
		Size: 138.3 MB (138329448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadb866080cf8fd8fb40d4722c8642031ac09e46b3ad9f8029cc13e4531e8d63`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2a55f83bf6210220425240b3a2382a1dcede45856c71588260c441d4d560a`  
		Last Modified: Fri, 06 Nov 2020 20:00:57 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5aeaca4a088d8f8b44454e8a71c131afb3faae25b4a31ffbcbd0e36e46c2a7`  
		Last Modified: Fri, 06 Nov 2020 20:00:55 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a62e98c257ab6518929697507951e1378383d5c25b708c0a5bdc20bb2f4cb`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02e4c481fcbe14f0818df1d4a577730f215914c3f7a4c44f3926c08ec354a2d`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3aba19aa6c0c8a874ce9d79d9e6d91ce5040a8037854a0d8c95fa1cf811030`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.8 MB (1768657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b33a039b5dad3077c7f441fbcd6321bccc7bb5d8d9db0b77f563baa66aab5d`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:91615621bb5d8f928cae33580878a3a0e4c360d2bd1a5078bd5579ffc1f65586
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941036189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69fe55d922052ef8814dc705972036b5fa14d96cea24bb078c82eded58a8536`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:31:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:31:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:33:58 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:35:13 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:18:04 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:21:38 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:21:40 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:58:23 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:58:24 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:58:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:59:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:59:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528ba1d9759adcc464112008fe49672e1f545981d69bab31186587ab32f92138`  
		Last Modified: Wed, 14 Oct 2020 12:51:33 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf4e6180661653575845d30a4d882dea92f395cb540b1cdf91170e9ee58731`  
		Last Modified: Wed, 14 Oct 2020 12:51:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e973f094614bb2cebe16df6f6004c05895ed077151aecdbbd0c476513054fc`  
		Last Modified: Wed, 14 Oct 2020 12:51:25 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089b875ac355097876e23760dd2166f096a8645e312660ffd3c0e617a2df9a0`  
		Last Modified: Wed, 14 Oct 2020 12:51:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a016b666d0691307c6414d84c36eb82de4b2fc4d74dd04c75f632dc3a78c`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 35.0 MB (35016991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4d95d13c0a45aa19a623e51cb112530a589a3a4d15d5c119610f8196912fab`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf8226941bb8f5af9f2be8fdb54da3e3caef344b0061a73e3debde23a55e98f`  
		Last Modified: Wed, 14 Oct 2020 12:51:24 GMT  
		Size: 9.9 MB (9870100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e5f43d50387ad619b863923b75cdf46053a8edd9954ec6e5bcdd6b90719c56`  
		Last Modified: Fri, 06 Nov 2020 19:34:21 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce913b69c36a8d04261681b1d8cde7dd3ec67f8275dc2c21b7b9d42074721ec1`  
		Last Modified: Fri, 06 Nov 2020 19:34:56 GMT  
		Size: 143.5 MB (143487215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75231de833daeca0a14373f4edb90eeaa4ec81d6fe961b4de6529a89c511ca2c`  
		Last Modified: Fri, 06 Nov 2020 19:34:20 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1a4d62df1ffdb8baac455f20994d1992ae918702aeb6c3c3171001c6870a73`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf2e1fbaf300596e6987a1c0f473fc2dde64d5a816b13f3aaf21cf2e4cc3332`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a001d9ed8d402d293907ee530361c27f8b6f076be745516b37580b9fbb73b9c2`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1740d81d6c6721405d45f80726a0ebcd3dc0d0de5da905fb41d182ca78a921ec`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d14e15f1dc7fa0765eb82fe118a91aa20fbef9c5c677cde9a38ddc0890ae260`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 11.3 MB (11295267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb21d7c1a6d233e3c34e5e883d3bc762275075111197136cb6b326f4ea46056`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:c243e906eda12ce67b24e021caa307808407005fc1a8197284d9b70daaf2a0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:fc73b9cce8ce070df5bd3bf94ff6f0dba5ab3a82359d7313d216b71585946551
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119452255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7c4becdaa4921f4830aa5898531fb59bdb497d37b6a9109fc9d2189b47316d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:34:56 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:34:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:34:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:35:51 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:38:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:38:42 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:38:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:38:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:38:44 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:18:13 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:18:13 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:18:13 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:18:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:18:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:18:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:18:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7d3d256c8367c41c431143c63d083a25dd62ec9ee9d9773dd9e6c7b70ec9e`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 280.8 KB (280812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9db76c5a1d06710ed4f3073476b2d883ff8e911f8e47c558bc4a8d1d8663fa`  
		Last Modified: Thu, 22 Oct 2020 03:43:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193f88ce657dbabff9f6a04034006ee66c6ecfb0d54bb599525d9c8d9ad91a22`  
		Last Modified: Fri, 06 Nov 2020 19:47:52 GMT  
		Size: 106.7 MB (106656837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dc1c79fe7f44761a5d11f6f64f4ec7142a59bf2225b8a1e5554ed551654797`  
		Last Modified: Fri, 06 Nov 2020 19:47:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec1cb62beafb625b4104c718b0c582ffdcc06f9ca5efd25549b3c1905cf16`  
		Last Modified: Fri, 06 Nov 2020 21:18:36 GMT  
		Size: 8.3 MB (8309861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d461a7017d5ae9ee39afa73c0013aa3fc8bcb8518db59843e7eff18a067c4142`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 1.4 MB (1407206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd8af862e3e9052217f29783b7f6e65c65f057dd9aa35f585882f13c0b34cde`  
		Last Modified: Fri, 06 Nov 2020 21:18:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89a73c5f4ae51892063fa87a4c7bbcb1311e07f70d70df7e2d8a03c7f61eac7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114664382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6e85a7472aacc21b210dfa3f511a5358983fb44fab90d8bd81956f0974cba9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:07:24 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:07:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:53:45 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:56:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:56:20 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:56:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:56:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:56:23 GMT
WORKDIR /go
# Fri, 06 Nov 2020 19:22:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 19:22:55 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:22:56 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:22:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:23:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 19:23:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 19:23:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20cc27a60e8ac1bf56dec787d3d52ba856e657179cfd56050036db79abb4267`  
		Last Modified: Thu, 22 Oct 2020 05:34:55 GMT  
		Size: 281.0 KB (280971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecce92c3d2de40638d73e682dec26c2b79a055e85c8d70b88f4ccb9485bb9c9`  
		Last Modified: Thu, 22 Oct 2020 05:34:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bea26c6de29e9326bc228c64da95fcd54b3d1f9354f1165eafc349994db0f8`  
		Last Modified: Fri, 06 Nov 2020 19:04:15 GMT  
		Size: 102.5 MB (102524592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e5877f5507358b36e32b963095c3caf40f40a6eec614d816a33f2f2ebfd55`  
		Last Modified: Fri, 06 Nov 2020 19:03:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81d2f79a49d963d6cbaa15e2327930649da636b6b369f88d7c19d733c5eb296`  
		Last Modified: Fri, 06 Nov 2020 19:23:35 GMT  
		Size: 7.9 MB (7928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea3d4a6a9133060470b288519140837675e4773f464432a967a4e3a080ac986`  
		Last Modified: Fri, 06 Nov 2020 19:23:34 GMT  
		Size: 1.3 MB (1327357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bf1d579fdbbae7b37fb9ef4d32de07ce43408b789fded70f7baeabe507c78e`  
		Last Modified: Fri, 06 Nov 2020 19:23:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:931f32bb911ba0de19091cc5d1b56e45a88159343a6782497a325539a5f88e3a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113487064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8b5eddc6ef348d71b508ab97a7dd567f6a977bac2cdd3828e499bb4440c38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:21:35 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 03:23:06 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:23:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:39:15 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:41:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:41:25 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:41:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:41:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:41:29 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:27:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:27:33 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:27:34 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:27:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:27:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:27:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:27:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b753cfc04fdce9640aac1e7a4b3e7ce15fa60b8e357376e42f294f463a6e890`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 280.1 KB (280084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e90c422e5e4668cb4140aadb622d734faa93c81cc1e283da9b08bbbc65c45c5`  
		Last Modified: Thu, 22 Oct 2020 05:59:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b476d7beedfa2137a0fef6e60a4484b51d77830c70ebcff073ccc374056e2e0c`  
		Last Modified: Fri, 06 Nov 2020 19:49:31 GMT  
		Size: 102.3 MB (102329948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd72c431842e0aeea9c3f8328785176b40806958c71f4fefebd421c3518571`  
		Last Modified: Fri, 06 Nov 2020 19:48:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7315086fe1858140ae2a84a77af42759c8f4e82b0a4df1b0529669c2e6208cc`  
		Last Modified: Fri, 06 Nov 2020 20:28:06 GMT  
		Size: 7.1 MB (7144798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca52434a632fe2aa304e8fd42e54bcf29afa42ffe1b722340860d449685dae`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 1.3 MB (1325846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e36ff02f43b3832542cf4347e8366772d4877647f3fc2c7a0624aa885219ad`  
		Last Modified: Fri, 06 Nov 2020 20:28:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:30fe2a9e24366ead2b615623a7637421e1b02f3f5404268d728e823253d1d889
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114775259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a06ec2afc931f2326cd6e8f7d6ead1bd093d76c1dac1e006111bb4cdc22354`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:08:19 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 04:09:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:09:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:18:49 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:20:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:20:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:20:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:20:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:20:48 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:09:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:09:26 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:09:26 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:09:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:09:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:09:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:09:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4357932f1b6fb010e1461cc5c673712fb832ac44ee627c691db0b64adf95d13`  
		Last Modified: Thu, 22 Oct 2020 04:28:32 GMT  
		Size: 281.2 KB (281230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c013af1878066e59b688e31fd962e7267430963de27c5257241e3c223aa1d6`  
		Last Modified: Thu, 22 Oct 2020 04:28:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b36744bb2cb0aa83f712639340b2320bd38128965d09ffffa43856a210f9e5`  
		Last Modified: Fri, 06 Nov 2020 19:28:03 GMT  
		Size: 102.0 MB (101976695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620dd3e3aa585cedfbb73c7698bdfc75f79b8a92e0bd7e7d5dcc2041012893be`  
		Last Modified: Fri, 06 Nov 2020 19:27:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803037031a1f00d46e050e3bb3fca389a0ac1939d4cb43c1548f0d72bb47cb5`  
		Last Modified: Fri, 06 Nov 2020 21:10:01 GMT  
		Size: 8.5 MB (8499884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840674c7f6a6769677bea40173b44c0cdf85447290b9521805050cac0b25df6`  
		Last Modified: Fri, 06 Nov 2020 21:09:59 GMT  
		Size: 1.3 MB (1310181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a9e6466e2de25170ecf4a3eb0a32a4dd076dcf8faabf6f80120fc45f1491`  
		Last Modified: Fri, 06 Nov 2020 21:09:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51c882c7f333a86293123c5c9f7dde2e2d733761be27faa8ba679fd25880dec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113944446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed252304acf0e273fc3538fbd970d4bfaa5fe502c7fe021fcb299559f389f4be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:27:26 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 13:27:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:27:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:32:30 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 18:34:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 18:34:46 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 18:34:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 18:35:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 18:35:27 GMT
WORKDIR /go
# Fri, 06 Nov 2020 21:51:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 21:51:06 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 21:51:09 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 21:51:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 21:51:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 21:51:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 21:51:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9900411dc7c8c88618743573bf89478d726007403bd002d8b00d21b7fecd40a`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 283.2 KB (283205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbd106374e3baf7eb8e3d8f7ffd4c364a35e57dcb3a89f8a153327a4c3fa3f9`  
		Last Modified: Thu, 22 Oct 2020 13:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec3950b2a73c219aef5a15211d4abc2d9a5af90823e42083fdace116f7c476`  
		Last Modified: Fri, 06 Nov 2020 18:47:04 GMT  
		Size: 100.6 MB (100649515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccf6cddd12f97382439bc21574bae904a64d8e1f96a30b0ac21e85f7aa112d7`  
		Last Modified: Fri, 06 Nov 2020 18:46:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb94e9e52826c34d57af8656e0e5b92258140dd8b57f186db8861f03ef5e4f00`  
		Last Modified: Fri, 06 Nov 2020 21:52:28 GMT  
		Size: 8.9 MB (8920000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75746c400be689f32365c8fb16a86def9e748eaf0507246876dade9fa125e78c`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 1.3 MB (1287791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0695a08f39b4841501692759a1c562a2e2c4c13bac546fbed9a962411082c141`  
		Last Modified: Fri, 06 Nov 2020 21:52:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:b252d4071ae496dbd6a16de864a46fe6d0629a7d35c8b123c58e19261db37455
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118365434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216ff73b58d08ff9b58e775653d0f32630eb7df17076e32df1011ce6bafaed1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:53:28 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 22 Oct 2020 02:53:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:53:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:23:44 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:25:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.4.src.tar.gz'; 	sha256='063da6a9a4186b8118a0e584532c8c94e65582e2cd951ed078bfd595d27d2367'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 06 Nov 2020 19:26:04 GMT
ENV GOPATH=/go
# Fri, 06 Nov 2020 19:26:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:26:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 06 Nov 2020 19:26:07 GMT
WORKDIR /go
# Fri, 06 Nov 2020 20:40:05 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 06 Nov 2020 20:40:07 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 20:40:07 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 20:40:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 20:40:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 06 Nov 2020 20:40:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 06 Nov 2020 20:40:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5139d7663b8674a989574c2161166fb137f26ef16b2f701159c126628be75101`  
		Last Modified: Thu, 22 Oct 2020 02:58:32 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31a06258ad66efe2dedbf67809ebc107a55757b8a4543af77982f55ff6c067`  
		Last Modified: Thu, 22 Oct 2020 02:58:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c878f3bd7fd82dbe36e4d303393019e0703f5e67ebb74f817f7369f072e6532`  
		Last Modified: Fri, 06 Nov 2020 19:34:26 GMT  
		Size: 105.8 MB (105776540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980f7999cd7558faa66bb1ae504f8c1e22e4881e3d71f3fd3aa2a4cb8ca7db13`  
		Last Modified: Fri, 06 Nov 2020 19:34:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85206d14782c0fb54511c935afb74a9e81b7c4bf73176614eadd044297188377`  
		Last Modified: Fri, 06 Nov 2020 20:40:48 GMT  
		Size: 8.4 MB (8352230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5f0e7da5d92511b1993de47afc01232a9b314ea3b5e854b83b0713acab7906`  
		Last Modified: Fri, 06 Nov 2020 20:40:47 GMT  
		Size: 1.4 MB (1388754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bfc26b576e6aeb40246d6645a95abab375e81757ab7a3095af525666ae295a`  
		Last Modified: Fri, 06 Nov 2020 20:40:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:b38981e5323bcf982907423ded683b2c6f8548a129819434392a2413e15fc1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:0cc26b33a1fe2b1ae4225a57d25846d69166be17484f8f847a3b835626c2df47
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548826368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5551c0b95fd6fba6bbdbef91ad7fd2edce9814d5127b0dd65274fd6fa964da48`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:27:03 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:27:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:27:05 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:28:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:28:38 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:29:02 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:15:07 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:17:47 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:17:49 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:57:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:57:51 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:57:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:58:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:58:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23a75d88f9f5980bb112e2c28248975f107144d8d2e40dc4755e2a09f5e56df`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bea6d8b9d9b014ffa471b7bb8882ddb7e9d378ddcacc099f0710073bd6361b9`  
		Last Modified: Wed, 14 Oct 2020 12:50:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75c1905c0573cc5706bc066d23624f0e92a8871832c744fbe7eabdcbc6f8a85`  
		Last Modified: Wed, 14 Oct 2020 12:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938695376d9deeba8819539ff3245935c28f93229d1c332bb8b6a16e67013fbc`  
		Last Modified: Wed, 14 Oct 2020 12:50:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41106c6a476cf9666c6d8c3c853c982a841c29db05b3ef8a072baba537b6d74c`  
		Last Modified: Wed, 14 Oct 2020 12:50:48 GMT  
		Size: 34.3 MB (34312667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6d6258831f87f3b455e6316e2bed430465a760272614de7cdd28c7c6e9f3e`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e3f66638c4d5ce9adba16e49844f57efbab1d628d9d6c73133511b7c1c3892`  
		Last Modified: Wed, 14 Oct 2020 12:50:20 GMT  
		Size: 310.5 KB (310525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d8771646c530e34e5045246ce3b2ebe859c4f5be8c444ec5dba3c382bee3a`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652b8eae6f5ed9dba044dae68e11cd7a4320ee55b36f6016b2199b9f3316c31a`  
		Last Modified: Fri, 06 Nov 2020 19:34:01 GMT  
		Size: 138.3 MB (138329448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadb866080cf8fd8fb40d4722c8642031ac09e46b3ad9f8029cc13e4531e8d63`  
		Last Modified: Fri, 06 Nov 2020 19:33:33 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2a55f83bf6210220425240b3a2382a1dcede45856c71588260c441d4d560a`  
		Last Modified: Fri, 06 Nov 2020 20:00:57 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5aeaca4a088d8f8b44454e8a71c131afb3faae25b4a31ffbcbd0e36e46c2a7`  
		Last Modified: Fri, 06 Nov 2020 20:00:55 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a62e98c257ab6518929697507951e1378383d5c25b708c0a5bdc20bb2f4cb`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02e4c481fcbe14f0818df1d4a577730f215914c3f7a4c44f3926c08ec354a2d`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3aba19aa6c0c8a874ce9d79d9e6d91ce5040a8037854a0d8c95fa1cf811030`  
		Last Modified: Fri, 06 Nov 2020 20:00:54 GMT  
		Size: 1.8 MB (1768657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b33a039b5dad3077c7f441fbcd6321bccc7bb5d8d9db0b77f563baa66aab5d`  
		Last Modified: Fri, 06 Nov 2020 20:00:53 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:2689ae5b16484bd1a074522d9ae004e9664036b4043a3bafe8443620784dbb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:builder-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:91615621bb5d8f928cae33580878a3a0e4c360d2bd1a5078bd5579ffc1f65586
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941036189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69fe55d922052ef8814dc705972036b5fa14d96cea24bb078c82eded58a8536`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 12:31:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Oct 2020 12:31:46 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Oct 2020 12:31:47 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Oct 2020 12:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:33:58 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Oct 2020 12:35:13 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Nov 2020 19:18:04 GMT
ENV GOLANG_VERSION=1.15.4
# Fri, 06 Nov 2020 19:21:38 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3593204e3851be577e4209900ece031b36f1e9ce1671f3f3221c9af7a090a941'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Nov 2020 19:21:40 GMT
WORKDIR C:\gopath
# Fri, 06 Nov 2020 19:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Nov 2020 19:58:23 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 06 Nov 2020 19:58:24 GMT
ENV CADDY_VERSION=v2.2.1
# Fri, 06 Nov 2020 19:58:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Nov 2020 19:59:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 06 Nov 2020 19:59:43 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528ba1d9759adcc464112008fe49672e1f545981d69bab31186587ab32f92138`  
		Last Modified: Wed, 14 Oct 2020 12:51:33 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf4e6180661653575845d30a4d882dea92f395cb540b1cdf91170e9ee58731`  
		Last Modified: Wed, 14 Oct 2020 12:51:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e973f094614bb2cebe16df6f6004c05895ed077151aecdbbd0c476513054fc`  
		Last Modified: Wed, 14 Oct 2020 12:51:25 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089b875ac355097876e23760dd2166f096a8645e312660ffd3c0e617a2df9a0`  
		Last Modified: Wed, 14 Oct 2020 12:51:29 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a016b666d0691307c6414d84c36eb82de4b2fc4d74dd04c75f632dc3a78c`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 35.0 MB (35016991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4d95d13c0a45aa19a623e51cb112530a589a3a4d15d5c119610f8196912fab`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf8226941bb8f5af9f2be8fdb54da3e3caef344b0061a73e3debde23a55e98f`  
		Last Modified: Wed, 14 Oct 2020 12:51:24 GMT  
		Size: 9.9 MB (9870100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e5f43d50387ad619b863923b75cdf46053a8edd9954ec6e5bcdd6b90719c56`  
		Last Modified: Fri, 06 Nov 2020 19:34:21 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce913b69c36a8d04261681b1d8cde7dd3ec67f8275dc2c21b7b9d42074721ec1`  
		Last Modified: Fri, 06 Nov 2020 19:34:56 GMT  
		Size: 143.5 MB (143487215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75231de833daeca0a14373f4edb90eeaa4ec81d6fe961b4de6529a89c511ca2c`  
		Last Modified: Fri, 06 Nov 2020 19:34:20 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1a4d62df1ffdb8baac455f20994d1992ae918702aeb6c3c3171001c6870a73`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf2e1fbaf300596e6987a1c0f473fc2dde64d5a816b13f3aaf21cf2e4cc3332`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a001d9ed8d402d293907ee530361c27f8b6f076be745516b37580b9fbb73b9c2`  
		Last Modified: Fri, 06 Nov 2020 20:01:12 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1740d81d6c6721405d45f80726a0ebcd3dc0d0de5da905fb41d182ca78a921ec`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d14e15f1dc7fa0765eb82fe118a91aa20fbef9c5c677cde9a38ddc0890ae260`  
		Last Modified: Fri, 06 Nov 2020 20:01:15 GMT  
		Size: 11.3 MB (11295267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb21d7c1a6d233e3c34e5e883d3bc762275075111197136cb6b326f4ea46056`  
		Last Modified: Fri, 06 Nov 2020 20:01:13 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:b44006ca7a107edd0fca2ff7a70cf75b81b20b61b722dff8a720364a3764ffd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:4ebad49f78a3f98164d89431978046ee6e94f1e8a70454abc7f49ce1a5ee7826
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb0137bab0e21a92b0bc9ec1cc22c259b097d5bf239b161ae1eac0de1833e67`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:33:22 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 04:33:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 04:33:55 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 04:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 04:34:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 04:34:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 04:34:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 04:34:02 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 04:34:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 04:34:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 04:34:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 04:34:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 80
# Thu, 22 Oct 2020 04:34:05 GMT
EXPOSE 443
# Thu, 22 Oct 2020 04:34:06 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 04:34:06 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 04:34:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e2d825895b6421ca5dbd63db0d99f790ef84a84c7bcaff51e60b654397858`  
		Last Modified: Thu, 22 Oct 2020 04:34:47 GMT  
		Size: 300.0 KB (299956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaf2e3dee2e74b401fce928bf9502e48df68da4e8c1933bfd6b00b1137529fc`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 5.8 KB (5754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2215cf93250599c5db984cee0fddd5d0cd59ef035ab5a317387b67211bde86d`  
		Last Modified: Thu, 22 Oct 2020 04:35:06 GMT  
		Size: 11.5 MB (11532508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060365e49ba5ee96a2859e269b366f5a5c9f386e5bdbf07d2ef31b1fc6934baa`  
		Last Modified: Thu, 22 Oct 2020 04:35:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:abba73dc860b2f35703cb7d27f08baf5bfc084e18e627b94661d01a8e2befdaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13784259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0aad5a281913821dd39ffed5e144daae22ac81ac4314731395ab65eedde72a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:58:10 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:58:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:58:46 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:58:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:58:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:59:00 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:59:01 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:59:01 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:59:03 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:59:08 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:59:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:59:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:59:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:59:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:59:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:59:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:59:15 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:59:19 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:59:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:59:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:59:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7369c3ac4b39c55c74e96dd3eb61ac2fa65e5671b1c2acca9697a7c9d20c3cf`  
		Last Modified: Thu, 22 Oct 2020 02:59:49 GMT  
		Size: 300.1 KB (300086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8f4045920069dff3382a5993783c5d846d9e28d0f5a63c475ed298fce0abb7`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db6bde4735da15e5db23ad62f3d64d78aed8713a40d12547f5538c15c90f9da`  
		Last Modified: Thu, 22 Oct 2020 03:00:06 GMT  
		Size: 10.9 MB (10876280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a95efd7a14ed98a53a238da45faa7e3b0fdd2a93529b83bfe9d0823dafac67c`  
		Last Modified: Thu, 22 Oct 2020 03:00:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8cf66cbe3c03273ca54bdab908092a6a9b9f02d39595ed15b1111f1465430426
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13565251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20723dea614fc40d9f3cb59eddd33bf0e89dfda3f8ed4a7b404ef334632a4b9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:04:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 03:05:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 03:05:45 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 03:05:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 03:05:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 03:05:53 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 03:05:54 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 03:05:55 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 03:05:56 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 03:05:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 03:05:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 03:05:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 03:06:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 03:06:01 GMT
EXPOSE 80
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 443
# Thu, 22 Oct 2020 03:06:02 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 03:06:03 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 03:06:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a8e7fe5034ac502626b0a921d79be80c092890176e33b236c489d6f00710a2`  
		Last Modified: Thu, 22 Oct 2020 03:06:32 GMT  
		Size: 299.2 KB (299211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db75acdaca15b1e81890f29b3b757fcc73e7a69a55f5ed659bf800f6340108`  
		Last Modified: Thu, 22 Oct 2020 03:06:43 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2197c38adf245bca8f229a4cd718c4d0f619a87bae5786572ccdac1a286882c`  
		Last Modified: Thu, 22 Oct 2020 03:06:46 GMT  
		Size: 10.9 MB (10854384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0104bc6a595940856019d00d9ff8e04365338a7964d948b64cc44bf73cc59e`  
		Last Modified: Thu, 22 Oct 2020 03:06:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:da121cf42d1759ed03af3130533d365c365af1d738d550744ad863e05e64cf46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13540356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b4aa38988ab2442575062d99c3cb44976de6c227256c118f35340e7c21c303`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:40:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:40:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:40:57 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:07 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:09 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:10 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:10 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:19 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:20 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:21 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dbde357077a97c0f831033bf03c9828203cb7e3e6cb33217ce4d7cfd71c931`  
		Last Modified: Thu, 22 Oct 2020 02:41:47 GMT  
		Size: 300.3 KB (300348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a5ab0aa923ce1fe233b904008bbf932c4787f48bcd59f07a85616147b7cbc3`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc398339860cf826624c9c22b5de9b45a193260e2ff24826d210b493483398f`  
		Last Modified: Thu, 22 Oct 2020 02:41:59 GMT  
		Size: 10.5 MB (10527465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6e7d61d1d4a00550447ea1f67edc0463cc527e49356e98959edfafba0df879`  
		Last Modified: Thu, 22 Oct 2020 02:41:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:09208042b4d19d7ed87b51b99dc20b390dab20d9ae7e235a62a3af3aaf472bd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13291756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5c77284adc35481d13003d31a866f637b6eaf9f5764f667e536db79ce23129`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 13:39:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 13:44:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 13:44:04 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 13:44:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 13:44:29 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 13:44:33 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 13:44:37 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 13:44:40 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 13:44:44 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 13:44:48 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 13:44:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 13:44:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 13:45:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 13:45:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 13:45:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 13:45:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 13:45:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 13:45:23 GMT
EXPOSE 80
# Thu, 22 Oct 2020 13:45:26 GMT
EXPOSE 443
# Thu, 22 Oct 2020 13:45:30 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 13:45:35 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 13:45:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a4964211b7ce86541a0c1dad8ef3800ec38a3ca90aff94b76759b4cb8e279`  
		Last Modified: Thu, 22 Oct 2020 13:47:22 GMT  
		Size: 302.3 KB (302327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dd938ef3e3eae8509deda8fab9ab5f9344169d912e35a802633e799feed1bb`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe23c296ee12ee12ef84dbabbb4f7bf0362a9a12b684782ebd3f44a97c8fcf8e`  
		Last Modified: Thu, 22 Oct 2020 13:47:55 GMT  
		Size: 10.2 MB (10180223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2f3c084745fecafaa9ff33626a81124f2d70267ceee705da555714238bfa1`  
		Last Modified: Thu, 22 Oct 2020 13:47:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:3e18b421d651721239cb3422bc890d1211535681219b7696816f487b4cebc4ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14074857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d5562f1d148d3d67ff7f5995be8f860553ad0f3d07091335643306b83385e1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:41:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 22 Oct 2020 02:41:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Thu, 22 Oct 2020 02:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Thu, 22 Oct 2020 02:41:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 22 Oct 2020 02:41:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 22 Oct 2020 02:41:36 GMT
ENV XDG_DATA_HOME=/data
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/config]
# Thu, 22 Oct 2020 02:41:37 GMT
VOLUME [/data]
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Thu, 22 Oct 2020 02:41:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 22 Oct 2020 02:41:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 22 Oct 2020 02:41:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 80
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 443
# Thu, 22 Oct 2020 02:41:40 GMT
EXPOSE 2019
# Thu, 22 Oct 2020 02:41:41 GMT
WORKDIR /srv
# Thu, 22 Oct 2020 02:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f988ff23f3cbb35bfed69e33f3b7ee69403bfae4f46363a08eea4830053e9c`  
		Last Modified: Thu, 22 Oct 2020 02:42:01 GMT  
		Size: 300.5 KB (300481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd6a4e0db99510879c5dfceabd1e629a0692c4544bb0da34971f8722b881e92`  
		Last Modified: Thu, 22 Oct 2020 02:42:09 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e13b938aa802e74610585cabba77d625db4baf219f577a81195c272408c7d3`  
		Last Modified: Thu, 22 Oct 2020 02:42:16 GMT  
		Size: 11.2 MB (11202559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a221fff082950a8a98db12eb99f532a39008f0d6e21684bc1aed06fa1ed2a764`  
		Last Modified: Thu, 22 Oct 2020 02:42:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:0cc9e18409440159fbf2ac241bce180b0214fc5d2358aa87fedf1189394d7469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:d720e5ab1579e03c0f86de11950434367743bdf8212a4501cd971c29d16942a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:155acd240efff18a38a7aff934be0f6976aeb1c76139025671c9833ed160c840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
