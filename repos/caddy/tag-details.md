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
$ docker pull caddy@sha256:6d45511406faf9fe59e433a6b907a6cf136e7200435545dc0c47e04e6e4e27df
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
$ docker pull caddy@sha256:63fe670997595a40c2f8c81f38cf634a430587648769244325baf4a21be3010c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fd2a84cc279dbdc53de15daeae84bd726376c255582d12f3d2a3fa105150c9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:27:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:19:42 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:19:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:19:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:19:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:19:47 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:19:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed237faf7b90187b720d5e863fb021a1ca678304744dad14ff8ad6434e4e1da`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 300.0 KB (299981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5bea3a62f2eb8bdd91cf1d01de5e62aa88dbcd8e5834f5dd686a4f1a482531`  
		Last Modified: Fri, 25 Sep 2020 22:28:09 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69398e09bae2fd51db197ec44792b08ec525846a197c98f0b59c7b2f0f9d627`  
		Last Modified: Wed, 14 Oct 2020 19:20:12 GMT  
		Size: 11.5 MB (11532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae648b058e6f63bcb417b92a4c41d61b2af30d50a970bd8d4b959e38bc7415`  
		Last Modified: Wed, 14 Oct 2020 19:20:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:7b5920e4a82b1bf465e06b3cf4893ee2e986063812e261bfa462dc7dda7a2d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13785708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d200bf3c822897c2bfe0d920d00e46b8125144c5947c88455acac1900bb34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:50:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:49:50 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:50:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:51:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:51:09 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:51:16 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:51:23 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:51:29 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:51:35 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:51:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:51:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:51:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:52:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:52:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:52:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:52:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:52:35 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:52:42 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:52:50 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:52:56 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:53:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a5a47b7ff29cc165cee9824ba874fa6cb56d737ce18f841fc3ed5e937cb75`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 300.1 KB (300144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdf9fef63ad932b076740c7fd4eac18d505c2e815b2b27093fae4a1037c1f83`  
		Last Modified: Fri, 25 Sep 2020 22:51:18 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481612b82405dab13f0ff7160cd02b31cafd7702962e9574045583eaed3fc7fe`  
		Last Modified: Wed, 14 Oct 2020 19:55:07 GMT  
		Size: 10.9 MB (10876291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c736385a37cc7654340f9f0217853549d57059a6fa720033afa8d97dea203`  
		Last Modified: Wed, 14 Oct 2020 19:54:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8b43c89dba95e29c51ac668ab67a77e739e67a469eef340fc8d3a7061adeb4b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13566363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01501010b8089fb9a9538277b4324106cc9891e2c01901d93699d43f832e96`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:58:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:58:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:59:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:59:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:59:51 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:00:01 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:00:10 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:00:22 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:00:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:00:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:01:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:01:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:01:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:01:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:01:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:02:02 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:02:17 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:02:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:02:41 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:02:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2aa34f01f2f9112772fdaebe7083b7dcdb4313768e0d6533a3e5b99597c98d`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 299.2 KB (299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f21378d6028fa7cda0d5b592cd8b633c405139cc47eee9863c2b21da4378b`  
		Last Modified: Fri, 25 Sep 2020 22:59:48 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c6573f114e083e57fdf28ed5339e567f2b1c3d13fda1b3b7d806e00f661128`  
		Last Modified: Wed, 14 Oct 2020 20:05:08 GMT  
		Size: 10.9 MB (10854375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660847f79f32b467c1ddaddb5a8306182d9f54c5fe1c2ee2aadd747cf78ed875`  
		Last Modified: Wed, 14 Oct 2020 20:05:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:085d496dad79fa71008de50e50f06591ab871b8f4711510a759b48a560bfe3aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13541809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e9fbe7d7a3cb53f7c6ee613e9c0ac1c82dbdfabb2a5e00cc6e577529e55b14`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:40:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:40:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:40:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:40:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:40:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:40:47 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:40:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:40:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:40:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:40:52 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:40:53 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:40:54 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:40:54 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:40:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f33282aee1a51127f669c7222e26bd0d5107b28d68819a6ead7f68076a73dc`  
		Last Modified: Mon, 15 Jun 2020 20:44:05 GMT  
		Size: 300.4 KB (300393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bbc79642b3dde186ddb45804729b84a8d010ca521d5c376311e2f613371675`  
		Last Modified: Fri, 25 Sep 2020 22:41:23 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f032bb954a154a6fcad58e71dc4fb90dabf12cf1ab3662992264236e3c2bd6e4`  
		Last Modified: Wed, 14 Oct 2020 19:41:31 GMT  
		Size: 10.5 MB (10527467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f62f208da9abbd187aaf41377a50af8149a6e8483fc0e04f5f5f507e4be7e`  
		Last Modified: Wed, 14 Oct 2020 19:41:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:a2f3a819439235784bf7fc8e3826e21acd4ed1825eaaf18e8d159e10e78c0f4d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13293783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12253d19d51ce81473f3f6884026957b92da390eaa7ede0fc8cb5d02f9281359`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 20:49:29 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:49:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 20:50:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 20:50:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 20:50:15 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:50:20 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:50:30 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:50:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:50:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:50:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:51:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:51:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:51:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:51:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:51:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:51:55 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:52:05 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:52:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:52:19 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:52:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b28df4c8a155654ad705e08f459bd177acc1005644ce2173ac62e954d6d4d2`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 302.4 KB (302369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899a5c1a337a29052e5f09180d092a86821dcf3d513b96fdf5db876ec3d6368`  
		Last Modified: Fri, 25 Sep 2020 22:45:34 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eb1518aae776833158c987ae4ac7c130ea2bfa680a61f757641ec0c57aab0c`  
		Last Modified: Wed, 14 Oct 2020 20:53:43 GMT  
		Size: 10.2 MB (10180227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18486e268d34e22c2aaac813d9e42b8401140f0fc8fd5a10b91ce37051de9b79`  
		Last Modified: Wed, 14 Oct 2020 20:53:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:9cb650ded68dd03f834621e7bea5b3411e6ac5b1162dbb759fef8acbf6404306
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14075256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54b98421e83dd9ca78953845196b424f44e37cdc25856a0fd9e7e0a38db7190`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:41:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:41:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:41:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:41:40 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc47bdcaea173dfb029a09265c41846030477dc696b22fed52acad2b2078bb7`  
		Last Modified: Mon, 15 Jun 2020 20:44:21 GMT  
		Size: 300.5 KB (300524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b62d245db5345045e7a29f409c7a0109545e93366793659a9538d863745398`  
		Last Modified: Fri, 25 Sep 2020 22:42:24 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec4c67136f6b42bf7c9ffc1b3d6ae4f4f6f8ae1c3da947aaac8391f8c0437f`  
		Last Modified: Wed, 14 Oct 2020 19:42:08 GMT  
		Size: 11.2 MB (11202554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15a505e0b8040884a4e54d19382378931d39e70eb5fddc880f5771f796b06b8`  
		Last Modified: Wed, 14 Oct 2020 19:42:07 GMT  
		Size: 153.0 B  
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
$ docker pull caddy@sha256:f050e6416ebb267214c73f125d8ab52e8adac486e9750af5aaf4c7977f068935
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
$ docker pull caddy@sha256:80d608bfebf1d919d7613d401af6004ba74a3be96867e1a25d9ab35a2da6714f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd8ade3df48988e09df79afd3361daa868169892daa8efc4b9b88028fada48a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:27:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:27:13 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:27:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:27:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:27:16 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:27:16 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:27:16 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:27:17 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:27:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:27:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:27:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:27:18 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:27:18 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:27:19 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:27:19 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:27:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed237faf7b90187b720d5e863fb021a1ca678304744dad14ff8ad6434e4e1da`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 300.0 KB (299981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff8cd7408716264fcaa599bf31e94490e2cf2281ce3d87c7376ecaabf995f2c`  
		Last Modified: Fri, 25 Sep 2020 22:27:59 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445f33e99ec338357aded23d1cf928a75a2ce5f6c840c49fc4a9469c0de07700`  
		Last Modified: Fri, 25 Sep 2020 22:28:01 GMT  
		Size: 13.1 MB (13057337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2107641907cbbc1ab9d5f92fc706779dfb06fa4f287e29f0e0731d27efab1d`  
		Last Modified: Fri, 25 Sep 2020 22:27:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6a6e8e419c6b07de12627d56e57d7526bbf0b7e0ed6444059310741aa823bf85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15324347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32588090d7bb2509380b4739113c43093f60dba0016465ed03143ef0225790e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:49:30 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:49:30 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:49:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:49:37 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:49:37 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:49:38 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:49:39 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:49:39 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:49:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:49:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:49:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:49:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:49:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:49:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:49:45 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:49:46 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:49:46 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:49:47 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:49:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a5a47b7ff29cc165cee9824ba874fa6cb56d737ce18f841fc3ed5e937cb75`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 300.1 KB (300144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f230a7df78269514af68ed5207d0d2ade5646619012a49f07564abd097a4f43`  
		Last Modified: Fri, 25 Sep 2020 22:51:00 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9826d83e7a201860c01ef0c6b537b3c7b672a109e04dc5e37b58051a7173ec21`  
		Last Modified: Fri, 25 Sep 2020 22:51:05 GMT  
		Size: 12.4 MB (12414930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20425603e5d968a6603537e218e4cc64a53b97498cbaf265bd952b931f6bbea`  
		Last Modified: Fri, 25 Sep 2020 22:51:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; arm variant v7

```console
$ docker pull caddy@sha256:b1d5c01fc7bfacc51f7d10dcdcb0b6b8de3aac2df9bfd8db586d207d88f2a833
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a694089ff1fc1cffa1e5ea27b0ae3f3cf3c40ee1d21bcf6e9eb7ea94352b4fe`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:57:50 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:57:50 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:57:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:57:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:57:57 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:57:58 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:57:59 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:57:59 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:58:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:58:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:58:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:58:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:58:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:58:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:58:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:58:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:58:06 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:58:07 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:58:07 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:58:08 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:58:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2aa34f01f2f9112772fdaebe7083b7dcdb4313768e0d6533a3e5b99597c98d`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 299.2 KB (299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815fe644041cd1e2a8be930b155833108c9af6b9214feb5b1c2f3b1710842af`  
		Last Modified: Fri, 25 Sep 2020 22:59:26 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c03433041ed8c869ebfd10d91d6673d1892324cbad0cdf2bdfb7eedc084a9d`  
		Last Modified: Fri, 25 Sep 2020 22:59:30 GMT  
		Size: 12.4 MB (12396043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8766336719d6750ac25a3c3bb665a18388a58138b4cdf8792ffc8aeb49c0099f`  
		Last Modified: Fri, 25 Sep 2020 22:59:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:04c78db76cedc0f3b4c2133fdc640dd69b1d9899b74b006c122f18352ab5fb1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15027441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe2123125accfb26638d3d060043f8032c66ff423f24993e350219facbf429c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:39:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:39:36 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:39:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:39:42 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:39:43 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:39:43 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:39:44 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:39:45 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:39:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:39:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:39:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:39:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:39:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:39:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:39:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:39:50 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:39:50 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:39:51 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:39:52 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:39:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f33282aee1a51127f669c7222e26bd0d5107b28d68819a6ead7f68076a73dc`  
		Last Modified: Mon, 15 Jun 2020 20:44:05 GMT  
		Size: 300.4 KB (300393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7ce2e195b05936e35a055c73bad445ca921206fd8c0c018f8a9b882488ec1a`  
		Last Modified: Fri, 25 Sep 2020 22:41:07 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0170c97deb56c282ca48bf564346008e7f0e44767d6e54a3cc25403771f36957`  
		Last Modified: Fri, 25 Sep 2020 22:41:10 GMT  
		Size: 12.0 MB (12013100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8f581aff5bd1747039f52bd705bbe5482b368537c82ea8d9ec22c966a97dbc`  
		Last Modified: Fri, 25 Sep 2020 22:41:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; ppc64le

```console
$ docker pull caddy@sha256:d5fc341e5909164e6d09c5aa91ffea06ecdec40e4ece378e4d20a05ca1ac2d38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14899023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67135043576dd821b2eebd66491f6bdf03d306dd63f80ae70348a3a44d12f63`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:34:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:34:28 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:34:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:35:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:35:08 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:35:20 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:35:37 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:35:49 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:36:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:36:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:36:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:36:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:36:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:36:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:37:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:37:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:37:29 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:37:41 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:37:56 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:38:09 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:38:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b28df4c8a155654ad705e08f459bd177acc1005644ce2173ac62e954d6d4d2`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 302.4 KB (302369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c2cc7761fc2675da80a24060fc865587f2c860a62a474056465c2402d691f8`  
		Last Modified: Fri, 25 Sep 2020 22:45:07 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98625f8d1b9c837094e190b29036054a427daabf5d3945434b54c89da129cc43`  
		Last Modified: Fri, 25 Sep 2020 22:45:10 GMT  
		Size: 11.8 MB (11785466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca513b6513d2e7c22c90baf1a8509f6d91cfc20edb99506d72239f7e755d62d`  
		Last Modified: Fri, 25 Sep 2020 22:45:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; s390x

```console
$ docker pull caddy@sha256:20408b3f483d7f32960f3839286b404f633ae99da1e8932dc429bc0c6b3a94b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84cdf8e8f810203a97d0597b2d9f5bab7d5b0eecb14ed3a12237bdea870bf2c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:41:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:41:22 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:41:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:41:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:41:26 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:41:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:41:26 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:41:27 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:41:27 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:41:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:41:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:41:29 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:41:29 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:41:29 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:41:29 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:41:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc47bdcaea173dfb029a09265c41846030477dc696b22fed52acad2b2078bb7`  
		Last Modified: Mon, 15 Jun 2020 20:44:21 GMT  
		Size: 300.5 KB (300524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13489b412dcfe7f996349c0742c4bbefde864c19defb8240fa21a95881ea436`  
		Last Modified: Fri, 25 Sep 2020 22:42:11 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4b720629eafad7b4379d0af34dcfd8d8de2540c694d2e1f420f89b2ee5d68`  
		Last Modified: Fri, 25 Sep 2020 22:42:13 GMT  
		Size: 12.8 MB (12836819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873125611edecc47abc85437ff79cdbf0c56c9d7509ac7e7a3941f87323e9fa4`  
		Last Modified: Fri, 25 Sep 2020 22:42:11 GMT  
		Size: 153.0 B  
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
$ docker pull caddy@sha256:0423525df39f98ebbdaa054439fb4b51a650f0da9af188f681f696bad64c095e
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
$ docker pull caddy@sha256:80d608bfebf1d919d7613d401af6004ba74a3be96867e1a25d9ab35a2da6714f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd8ade3df48988e09df79afd3361daa868169892daa8efc4b9b88028fada48a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:27:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:27:13 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:27:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:27:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:27:16 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:27:16 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:27:16 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:27:17 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:27:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:27:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:27:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:27:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:27:18 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:27:18 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:27:19 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:27:19 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:27:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed237faf7b90187b720d5e863fb021a1ca678304744dad14ff8ad6434e4e1da`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 300.0 KB (299981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff8cd7408716264fcaa599bf31e94490e2cf2281ce3d87c7376ecaabf995f2c`  
		Last Modified: Fri, 25 Sep 2020 22:27:59 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445f33e99ec338357aded23d1cf928a75a2ce5f6c840c49fc4a9469c0de07700`  
		Last Modified: Fri, 25 Sep 2020 22:28:01 GMT  
		Size: 13.1 MB (13057337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2107641907cbbc1ab9d5f92fc706779dfb06fa4f287e29f0e0731d27efab1d`  
		Last Modified: Fri, 25 Sep 2020 22:27:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6a6e8e419c6b07de12627d56e57d7526bbf0b7e0ed6444059310741aa823bf85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15324347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32588090d7bb2509380b4739113c43093f60dba0016465ed03143ef0225790e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:49:30 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:49:30 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:49:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:49:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:49:37 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:49:37 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:49:38 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:49:39 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:49:39 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:49:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:49:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:49:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:49:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:49:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:49:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:49:45 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:49:46 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:49:46 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:49:47 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:49:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a5a47b7ff29cc165cee9824ba874fa6cb56d737ce18f841fc3ed5e937cb75`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 300.1 KB (300144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f230a7df78269514af68ed5207d0d2ade5646619012a49f07564abd097a4f43`  
		Last Modified: Fri, 25 Sep 2020 22:51:00 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9826d83e7a201860c01ef0c6b537b3c7b672a109e04dc5e37b58051a7173ec21`  
		Last Modified: Fri, 25 Sep 2020 22:51:05 GMT  
		Size: 12.4 MB (12414930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20425603e5d968a6603537e218e4cc64a53b97498cbaf265bd952b931f6bbea`  
		Last Modified: Fri, 25 Sep 2020 22:51:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:b1d5c01fc7bfacc51f7d10dcdcb0b6b8de3aac2df9bfd8db586d207d88f2a833
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a694089ff1fc1cffa1e5ea27b0ae3f3cf3c40ee1d21bcf6e9eb7ea94352b4fe`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:57:50 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:57:50 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:57:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:57:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:57:57 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:57:58 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:57:59 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:57:59 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:58:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:58:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:58:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:58:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:58:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:58:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:58:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:58:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:58:06 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:58:07 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:58:07 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:58:08 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:58:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2aa34f01f2f9112772fdaebe7083b7dcdb4313768e0d6533a3e5b99597c98d`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 299.2 KB (299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c815fe644041cd1e2a8be930b155833108c9af6b9214feb5b1c2f3b1710842af`  
		Last Modified: Fri, 25 Sep 2020 22:59:26 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c03433041ed8c869ebfd10d91d6673d1892324cbad0cdf2bdfb7eedc084a9d`  
		Last Modified: Fri, 25 Sep 2020 22:59:30 GMT  
		Size: 12.4 MB (12396043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8766336719d6750ac25a3c3bb665a18388a58138b4cdf8792ffc8aeb49c0099f`  
		Last Modified: Fri, 25 Sep 2020 22:59:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:04c78db76cedc0f3b4c2133fdc640dd69b1d9899b74b006c122f18352ab5fb1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15027441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe2123125accfb26638d3d060043f8032c66ff423f24993e350219facbf429c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:39:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:39:36 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:39:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:39:42 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:39:43 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:39:43 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:39:44 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:39:45 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:39:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:39:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:39:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:39:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:39:48 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:39:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:39:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:39:50 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:39:50 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:39:51 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:39:52 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:39:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f33282aee1a51127f669c7222e26bd0d5107b28d68819a6ead7f68076a73dc`  
		Last Modified: Mon, 15 Jun 2020 20:44:05 GMT  
		Size: 300.4 KB (300393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7ce2e195b05936e35a055c73bad445ca921206fd8c0c018f8a9b882488ec1a`  
		Last Modified: Fri, 25 Sep 2020 22:41:07 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0170c97deb56c282ca48bf564346008e7f0e44767d6e54a3cc25403771f36957`  
		Last Modified: Fri, 25 Sep 2020 22:41:10 GMT  
		Size: 12.0 MB (12013100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8f581aff5bd1747039f52bd705bbe5482b368537c82ea8d9ec22c966a97dbc`  
		Last Modified: Fri, 25 Sep 2020 22:41:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d5fc341e5909164e6d09c5aa91ffea06ecdec40e4ece378e4d20a05ca1ac2d38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14899023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67135043576dd821b2eebd66491f6bdf03d306dd63f80ae70348a3a44d12f63`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:34:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:34:28 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:34:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:35:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:35:08 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:35:20 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:35:37 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:35:49 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:36:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:36:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:36:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:36:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:36:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:36:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:37:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:37:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:37:29 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:37:41 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:37:56 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:38:09 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:38:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b28df4c8a155654ad705e08f459bd177acc1005644ce2173ac62e954d6d4d2`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 302.4 KB (302369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c2cc7761fc2675da80a24060fc865587f2c860a62a474056465c2402d691f8`  
		Last Modified: Fri, 25 Sep 2020 22:45:07 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98625f8d1b9c837094e190b29036054a427daabf5d3945434b54c89da129cc43`  
		Last Modified: Fri, 25 Sep 2020 22:45:10 GMT  
		Size: 11.8 MB (11785466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca513b6513d2e7c22c90baf1a8509f6d91cfc20edb99506d72239f7e755d62d`  
		Last Modified: Fri, 25 Sep 2020 22:45:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:20408b3f483d7f32960f3839286b404f633ae99da1e8932dc429bc0c6b3a94b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84cdf8e8f810203a97d0597b2d9f5bab7d5b0eecb14ed3a12237bdea870bf2c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:41:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/506330b23c5cce43a9352179e7977a684678fbaf/welcome/index.html"
# Fri, 25 Sep 2020 22:41:22 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:41:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 25 Sep 2020 22:41:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 25 Sep 2020 22:41:26 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 25 Sep 2020 22:41:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 25 Sep 2020 22:41:26 GMT
VOLUME [/config]
# Fri, 25 Sep 2020 22:41:27 GMT
VOLUME [/data]
# Fri, 25 Sep 2020 22:41:27 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Fri, 25 Sep 2020 22:41:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 25 Sep 2020 22:41:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 25 Sep 2020 22:41:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 25 Sep 2020 22:41:29 GMT
EXPOSE 80
# Fri, 25 Sep 2020 22:41:29 GMT
EXPOSE 443
# Fri, 25 Sep 2020 22:41:29 GMT
EXPOSE 2019
# Fri, 25 Sep 2020 22:41:29 GMT
WORKDIR /srv
# Fri, 25 Sep 2020 22:41:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc47bdcaea173dfb029a09265c41846030477dc696b22fed52acad2b2078bb7`  
		Last Modified: Mon, 15 Jun 2020 20:44:21 GMT  
		Size: 300.5 KB (300524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13489b412dcfe7f996349c0742c4bbefde864c19defb8240fa21a95881ea436`  
		Last Modified: Fri, 25 Sep 2020 22:42:11 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4b720629eafad7b4379d0af34dcfd8d8de2540c694d2e1f420f89b2ee5d68`  
		Last Modified: Fri, 25 Sep 2020 22:42:13 GMT  
		Size: 12.8 MB (12836819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873125611edecc47abc85437ff79cdbf0c56c9d7509ac7e7a3941f87323e9fa4`  
		Last Modified: Fri, 25 Sep 2020 22:42:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-builder`

```console
$ docker pull caddy@sha256:e6917fe7df3d561e793dd69788b42e2448d884dc4e684ae2dd8706f72ecca845
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
$ docker pull caddy@sha256:d5f7999af933a6d3350e575786a2f16aba5e930513faa770602b0e4bff23f1f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120169717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9523c15dba19a965a9876feb739c5e803195ef8873e9e1717cec30807013bfff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:22:58 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:25:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:25:12 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:25:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:25:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:25:13 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:27:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:27:25 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:27:25 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:27:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:27:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:27:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:27:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0547b08c8963faeee9d579d8351699f769179aa7a58ada0290e6ab8f5a676c`  
		Last Modified: Wed, 09 Sep 2020 22:30:12 GMT  
		Size: 107.4 MB (107371657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6f0657434294654385190364b1a7c9af2a6f7b7ef0e821b8d51e20cdd8da5`  
		Last Modified: Wed, 09 Sep 2020 22:29:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b6567fb8ec7e0ec3b0ae6600ccda0528e94ef892ebb7437d9a3d2618e52d2c`  
		Last Modified: Fri, 25 Sep 2020 22:28:06 GMT  
		Size: 8.3 MB (8310024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea9a80e0e2435373930ec1446faf55a0c9a6c38c6345c8dc311f53980bea9cc`  
		Last Modified: Fri, 25 Sep 2020 22:28:05 GMT  
		Size: 1.4 MB (1407206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ca5e78208a09f95566cee8aaf87377d4a90ee0876ed6cfef4112094985eafc`  
		Last Modified: Fri, 25 Sep 2020 22:28:04 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a8307a5e8bbafa996de097f1ce5cce7356ca69dd876f73b75c81981d070e271f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115855840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ccc058ff7d3bdf7ba573fd105e819d1b549cee1155c15878e62d4ddc3183d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:54:15 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:57:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:57:19 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:57:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:57:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:57:23 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:49:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:49:58 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:49:59 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:49:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:50:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:50:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:50:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6fe6c5f0fa89cff72714190eb250d37035e32c7216624ea20cfcdfc88d8932`  
		Last Modified: Wed, 09 Sep 2020 23:02:32 GMT  
		Size: 103.7 MB (103712873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186bd058112580f710efc27a0aae302bc22b6933011ca92545db5a513ddde4c0`  
		Last Modified: Wed, 09 Sep 2020 23:02:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabce2f857cbac8727f8021a5cf32f58d584d215c2e8335b66f0219a29a3033d`  
		Last Modified: Fri, 25 Sep 2020 22:51:13 GMT  
		Size: 7.9 MB (7928840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e241c148840303273064a679499c21f3aca20b4aaf58c77f28779e279fb48f84`  
		Last Modified: Fri, 25 Sep 2020 22:51:11 GMT  
		Size: 1.3 MB (1327350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27b1b507797e2939000db251e060bed35635884911e1ca2169971fffcc486b2`  
		Last Modified: Fri, 25 Sep 2020 22:51:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f67a650b90e8d2a154c1c2b336cfe21520f944706539151c61f3afaee7793d4b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114622952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3abcefdc9bf61ec46fb1d63b3460e4632f700d7557c697007c9eed2efa0d826`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:46:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:05:40 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:07:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:07:51 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:07:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:07:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:07:54 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:58:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:58:19 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:58:20 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:58:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:58:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:58:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:58:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189358c25ed3947ca4fd93936880bae2e9a32a62f75d865d03db0ce536130f63`  
		Last Modified: Wed, 09 Sep 2020 22:14:22 GMT  
		Size: 103.5 MB (103462777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a5f301bfa0a4263c5e4fd043d781161d2579b6d5ac42d3a18287f1452e4194`  
		Last Modified: Wed, 09 Sep 2020 22:13:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66072234449cb7ebdfa002c42bc8bc4d2bd9b9fc3eb35b2f42f97cda16e9c465`  
		Last Modified: Fri, 25 Sep 2020 22:59:37 GMT  
		Size: 7.1 MB (7144963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057878579f01640f17bd812b5eb955522f4417c13140581f324bd45ec72c8171`  
		Last Modified: Fri, 25 Sep 2020 22:59:36 GMT  
		Size: 1.3 MB (1325844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f2dd8c431593bb818262a0f6cf4e99384b7a3bd428eaf77e41adcdd56d1b61`  
		Last Modified: Fri, 25 Sep 2020 22:59:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ae0a341e115b71cabe57716540ed3f37cc4a8781968014872b092cc4056dcc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115613481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d8bff2d69027fa736b15d37f3bd4a0d25526f3a5ba62d9e5fc9edddee2a7ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:22 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:45:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:45:10 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:45:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:45:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:45:14 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:40:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:40:04 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:40:05 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:40:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:40:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:40:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:40:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aee363a75d12710f67004978ba4509d1ddb769cc47ba518bc277ecd103a6b8d`  
		Last Modified: Wed, 09 Sep 2020 22:51:01 GMT  
		Size: 102.8 MB (102811724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab2d6f42095309ce47a6ec4edd38bd86aabe0fb28a18cb007652d42e0f19e0`  
		Last Modified: Wed, 09 Sep 2020 22:50:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c3daf327048ea4a763cbf539c90940c6b9aa38c855f7ef3ed94cd8ec78b3f0`  
		Last Modified: Fri, 25 Sep 2020 22:41:18 GMT  
		Size: 8.5 MB (8499903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060cae146f34b58e867a469646d5890b88814e89f40e79bf189a0d8328794bf3`  
		Last Modified: Fri, 25 Sep 2020 22:41:16 GMT  
		Size: 1.3 MB (1310178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e04b02068c1b0c55346de19ab65cfaf81f0c7e592e3b9186770805d808cc2f`  
		Last Modified: Fri, 25 Sep 2020 22:41:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:123d4d4d278526a8e701cd04340f1dba7b30e30c5c5670eb1262a135c5b10cd8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114975359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353c0018d03b3c5caaf56597dad9f71994ee3484891dafa93293c87c52e89970`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:26:40 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:29:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:29:52 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:29:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:30:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:30:39 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:38:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:39:05 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:39:17 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:39:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:39:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:40:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba569e5c85b1b70b3985f097dd79fee89c81c111899c623098e368323e560524`  
		Last Modified: Wed, 09 Sep 2020 22:44:05 GMT  
		Size: 101.7 MB (101676592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826cb177af69484b6f3437a2174165ac7a6c677d76f72e742f049397fb1fe2df`  
		Last Modified: Wed, 09 Sep 2020 22:43:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b9f0d89c6dc27e3c5c140b29344ef655160fc9e88f4196c49fe8dc1ed7e920`  
		Last Modified: Fri, 25 Sep 2020 22:45:22 GMT  
		Size: 8.9 MB (8920029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb48f7a86e8728bdc83e425192be427270c4373d75021b798b6d823187d98c0`  
		Last Modified: Fri, 25 Sep 2020 22:45:20 GMT  
		Size: 1.3 MB (1287790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e11ed799593484a68e98ebebc5a412185deced61c2a18bc4c822c534533ae69`  
		Last Modified: Fri, 25 Sep 2020 22:45:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:1285082a295430e40664f8c45d9afaeef9882396aee2a9032e0148419bd1815e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119845154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e8e2ac6196cf2f55081248aa3fa9679367f116d18ae3d94f928bbdd1979a38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:55 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:45:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:45:07 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:45:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:45:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:45:08 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:41:36 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:41:36 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:41:36 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:41:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:41:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:41:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:41:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e7f0b644229c4d22243efaf9cde7728d52c4624e9d48ab2d5174ec187de5f9`  
		Last Modified: Wed, 09 Sep 2020 22:48:16 GMT  
		Size: 107.3 MB (107254107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b1ab98332292b26f0fee8484fc91221c2e937011cbcd0fa39c2b7f8b32252e`  
		Last Modified: Wed, 09 Sep 2020 22:48:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3410d79dc81d3365abcfd9af5b2a59c63ca9271245267f755bd050b16b7e223e`  
		Last Modified: Fri, 25 Sep 2020 22:42:19 GMT  
		Size: 8.4 MB (8352248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b31e4bcee38a9106ed828122ca5dbf26b0eb949b75812a7cef4030e433b28`  
		Last Modified: Fri, 25 Sep 2020 22:42:18 GMT  
		Size: 1.4 MB (1388751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e19ef40a33a5b2d606204c7a107998bb8d08dbf01e36c3a3bfaee4ec4d46b8`  
		Last Modified: Fri, 25 Sep 2020 22:42:18 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:619abb4972366e19a3cecf06ccf5a5500ee382d8e0b725415afc6671057e3176
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548379291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be96536344bd43c4263fc0abab1e4100b0e4239c5c5e1448886d9e0dbc697a57`
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
# Wed, 14 Oct 2020 12:41:27 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 14 Oct 2020 12:43:51 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.14.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16bb44448c4423740c5fd751bad28061d5ec44cd08272d4e1efdd16cdf8221e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:43:53 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:01:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:01:07 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:01:07 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 21:01:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:01:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:01:35 GMT
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
	-	`sha256:5de95bbe4c06b5ec1e11f79b684773d419eb2236e0dafc0dc918903f42e520ff`  
		Last Modified: Wed, 14 Oct 2020 12:52:59 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78df25c12716570f89f8a047ef08e7f1b5e034764a58ffd78238fa484bbe6aaa`  
		Last Modified: Wed, 14 Oct 2020 12:53:26 GMT  
		Size: 137.9 MB (137870578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778947ded1566c0dcebc9b8814983e16ff29f501405fd177b1b7cb4c156800a`  
		Last Modified: Wed, 14 Oct 2020 12:53:00 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f24ac044271e744dce202dc376d9e19b77bbbb181b4f403d718cd7ceb9a9c9c`  
		Last Modified: Wed, 14 Oct 2020 21:12:42 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0d4e0f2bcd042a7dc18ce24a67065d60a577911c683ba33376bcd1843c86d4`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ce4de4c08d7c334a4968d897e61681dc85ffe560b778b9db75426907070d9`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9f6c856fee2d7e9adeefb4c769a76404388d9c76c433405d8657594c87b4a1`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd52ae6f924f58c3a7716cc5e56c928033b522a5b884158f19e3dc0282bbee`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.8 MB (1780479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bbf47d6c923e5294e61089f6facc5bf2fae0ee29ea9f1b9a8de2db82c4d6de`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4ef9d82eeef794e09e249d568dd248482236de4d0f5d8ae1603910f4f644703b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5936144411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d6db2ab19123c5b5ba620a762bcb9f71e23e1906abd2bf4cbf51abefe863f0`
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
# Wed, 14 Oct 2020 12:44:08 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 14 Oct 2020 12:47:29 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.14.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16bb44448c4423740c5fd751bad28061d5ec44cd08272d4e1efdd16cdf8221e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:47:31 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:01:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:01:43 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:01:43 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 21:01:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:03:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:03:01 GMT
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
	-	`sha256:d1c853f53fc418479f31e0f3126ce797d8856ac18457d52a6a8afd2bb82bb901`  
		Last Modified: Wed, 14 Oct 2020 12:53:38 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9252b4af3042a54d971ec0b85e86d2e2630f01f1d86a4bb0ddc033e0784cb329`  
		Last Modified: Wed, 14 Oct 2020 12:56:24 GMT  
		Size: 143.1 MB (143053993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eca72c26de5c2a3894be93ad63055723ded8800314dbfc9a845b927efc0aeda`  
		Last Modified: Wed, 14 Oct 2020 12:53:38 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e704b86c9907a03003c89e4006c7cebd14d9fbaeef88cffac61b74ffc990ec1e`  
		Last Modified: Wed, 14 Oct 2020 21:12:55 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646ed8f4fd451b8bb06909f7beed493e59784b40c8b836a9548f129be1a243a7`  
		Last Modified: Wed, 14 Oct 2020 21:12:52 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2daffddd22c63074b092cff776d945b187cba1cf92e0a614e788134eb3285c`  
		Last Modified: Wed, 14 Oct 2020 21:12:52 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd0551e18d924bf52827df34ede4ff1c46c168f97a2bbd2c8db4f27be986137`  
		Last Modified: Wed, 14 Oct 2020 21:12:53 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6d7cbddd5c4f5a80e822e453f3e6d3f45c753aff73e0a491813661d27075f1`  
		Last Modified: Wed, 14 Oct 2020 21:12:54 GMT  
		Size: 6.8 MB (6836641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ebf859ffb9a352cee6b20f1845441a9e95f6e4e518e492ae9af39c545f992d`  
		Last Modified: Wed, 14 Oct 2020 21:12:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-builder-alpine`

```console
$ docker pull caddy@sha256:589f69d3b427997c0d1091068c65d8e57424cc7e77674c4137c26552d6bd0410
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
$ docker pull caddy@sha256:d5f7999af933a6d3350e575786a2f16aba5e930513faa770602b0e4bff23f1f1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120169717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9523c15dba19a965a9876feb739c5e803195ef8873e9e1717cec30807013bfff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:22:58 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:25:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:25:12 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:25:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:25:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:25:13 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:27:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:27:25 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:27:25 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:27:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:27:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:27:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:27:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0547b08c8963faeee9d579d8351699f769179aa7a58ada0290e6ab8f5a676c`  
		Last Modified: Wed, 09 Sep 2020 22:30:12 GMT  
		Size: 107.4 MB (107371657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b6f0657434294654385190364b1a7c9af2a6f7b7ef0e821b8d51e20cdd8da5`  
		Last Modified: Wed, 09 Sep 2020 22:29:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b6567fb8ec7e0ec3b0ae6600ccda0528e94ef892ebb7437d9a3d2618e52d2c`  
		Last Modified: Fri, 25 Sep 2020 22:28:06 GMT  
		Size: 8.3 MB (8310024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea9a80e0e2435373930ec1446faf55a0c9a6c38c6345c8dc311f53980bea9cc`  
		Last Modified: Fri, 25 Sep 2020 22:28:05 GMT  
		Size: 1.4 MB (1407206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ca5e78208a09f95566cee8aaf87377d4a90ee0876ed6cfef4112094985eafc`  
		Last Modified: Fri, 25 Sep 2020 22:28:04 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a8307a5e8bbafa996de097f1ce5cce7356ca69dd876f73b75c81981d070e271f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115855840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ccc058ff7d3bdf7ba573fd105e819d1b549cee1155c15878e62d4ddc3183d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:54:15 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:57:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:57:19 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:57:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:57:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:57:23 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:49:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:49:58 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:49:59 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:49:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:50:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:50:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:50:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6fe6c5f0fa89cff72714190eb250d37035e32c7216624ea20cfcdfc88d8932`  
		Last Modified: Wed, 09 Sep 2020 23:02:32 GMT  
		Size: 103.7 MB (103712873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186bd058112580f710efc27a0aae302bc22b6933011ca92545db5a513ddde4c0`  
		Last Modified: Wed, 09 Sep 2020 23:02:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabce2f857cbac8727f8021a5cf32f58d584d215c2e8335b66f0219a29a3033d`  
		Last Modified: Fri, 25 Sep 2020 22:51:13 GMT  
		Size: 7.9 MB (7928840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e241c148840303273064a679499c21f3aca20b4aaf58c77f28779e279fb48f84`  
		Last Modified: Fri, 25 Sep 2020 22:51:11 GMT  
		Size: 1.3 MB (1327350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27b1b507797e2939000db251e060bed35635884911e1ca2169971fffcc486b2`  
		Last Modified: Fri, 25 Sep 2020 22:51:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f67a650b90e8d2a154c1c2b336cfe21520f944706539151c61f3afaee7793d4b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114622952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3abcefdc9bf61ec46fb1d63b3460e4632f700d7557c697007c9eed2efa0d826`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:46:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:05:40 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:07:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:07:51 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:07:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:07:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:07:54 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:58:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:58:19 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:58:20 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:58:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:58:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:58:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:58:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189358c25ed3947ca4fd93936880bae2e9a32a62f75d865d03db0ce536130f63`  
		Last Modified: Wed, 09 Sep 2020 22:14:22 GMT  
		Size: 103.5 MB (103462777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a5f301bfa0a4263c5e4fd043d781161d2579b6d5ac42d3a18287f1452e4194`  
		Last Modified: Wed, 09 Sep 2020 22:13:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66072234449cb7ebdfa002c42bc8bc4d2bd9b9fc3eb35b2f42f97cda16e9c465`  
		Last Modified: Fri, 25 Sep 2020 22:59:37 GMT  
		Size: 7.1 MB (7144963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057878579f01640f17bd812b5eb955522f4417c13140581f324bd45ec72c8171`  
		Last Modified: Fri, 25 Sep 2020 22:59:36 GMT  
		Size: 1.3 MB (1325844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f2dd8c431593bb818262a0f6cf4e99384b7a3bd428eaf77e41adcdd56d1b61`  
		Last Modified: Fri, 25 Sep 2020 22:59:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9ae0a341e115b71cabe57716540ed3f37cc4a8781968014872b092cc4056dcc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115613481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d8bff2d69027fa736b15d37f3bd4a0d25526f3a5ba62d9e5fc9edddee2a7ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:22 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:45:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:45:10 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:45:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:45:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:45:14 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:40:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:40:04 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:40:05 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:40:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:40:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:40:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:40:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aee363a75d12710f67004978ba4509d1ddb769cc47ba518bc277ecd103a6b8d`  
		Last Modified: Wed, 09 Sep 2020 22:51:01 GMT  
		Size: 102.8 MB (102811724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab2d6f42095309ce47a6ec4edd38bd86aabe0fb28a18cb007652d42e0f19e0`  
		Last Modified: Wed, 09 Sep 2020 22:50:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c3daf327048ea4a763cbf539c90940c6b9aa38c855f7ef3ed94cd8ec78b3f0`  
		Last Modified: Fri, 25 Sep 2020 22:41:18 GMT  
		Size: 8.5 MB (8499903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060cae146f34b58e867a469646d5890b88814e89f40e79bf189a0d8328794bf3`  
		Last Modified: Fri, 25 Sep 2020 22:41:16 GMT  
		Size: 1.3 MB (1310178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e04b02068c1b0c55346de19ab65cfaf81f0c7e592e3b9186770805d808cc2f`  
		Last Modified: Fri, 25 Sep 2020 22:41:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:123d4d4d278526a8e701cd04340f1dba7b30e30c5c5670eb1262a135c5b10cd8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114975359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353c0018d03b3c5caaf56597dad9f71994ee3484891dafa93293c87c52e89970`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:26:40 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:29:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:29:52 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:29:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:30:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:30:39 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:38:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:39:05 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:39:17 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:39:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:39:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:40:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba569e5c85b1b70b3985f097dd79fee89c81c111899c623098e368323e560524`  
		Last Modified: Wed, 09 Sep 2020 22:44:05 GMT  
		Size: 101.7 MB (101676592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826cb177af69484b6f3437a2174165ac7a6c677d76f72e742f049397fb1fe2df`  
		Last Modified: Wed, 09 Sep 2020 22:43:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b9f0d89c6dc27e3c5c140b29344ef655160fc9e88f4196c49fe8dc1ed7e920`  
		Last Modified: Fri, 25 Sep 2020 22:45:22 GMT  
		Size: 8.9 MB (8920029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb48f7a86e8728bdc83e425192be427270c4373d75021b798b6d823187d98c0`  
		Last Modified: Fri, 25 Sep 2020 22:45:20 GMT  
		Size: 1.3 MB (1287790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e11ed799593484a68e98ebebc5a412185deced61c2a18bc4c822c534533ae69`  
		Last Modified: Fri, 25 Sep 2020 22:45:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:1285082a295430e40664f8c45d9afaeef9882396aee2a9032e0148419bd1815e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119845154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e8e2ac6196cf2f55081248aa3fa9679367f116d18ae3d94f928bbdd1979a38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:55 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 09 Sep 2020 22:45:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.9.src.tar.gz'; 	sha256='c687c848cc09bcabf2b5e534c3fc4259abebbfc9014dd05a1a2dc6106f404554'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:45:07 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:45:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:45:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:45:08 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:41:36 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:41:36 GMT
ENV XCADDY_VERSION=v0.1.5
# Fri, 25 Sep 2020 22:41:36 GMT
ENV CADDY_VERSION=v2.1.1
# Fri, 25 Sep 2020 22:41:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 25 Sep 2020 22:41:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 25 Sep 2020 22:41:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 25 Sep 2020 22:41:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e7f0b644229c4d22243efaf9cde7728d52c4624e9d48ab2d5174ec187de5f9`  
		Last Modified: Wed, 09 Sep 2020 22:48:16 GMT  
		Size: 107.3 MB (107254107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b1ab98332292b26f0fee8484fc91221c2e937011cbcd0fa39c2b7f8b32252e`  
		Last Modified: Wed, 09 Sep 2020 22:48:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3410d79dc81d3365abcfd9af5b2a59c63ca9271245267f755bd050b16b7e223e`  
		Last Modified: Fri, 25 Sep 2020 22:42:19 GMT  
		Size: 8.4 MB (8352248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65b31e4bcee38a9106ed828122ca5dbf26b0eb949b75812a7cef4030e433b28`  
		Last Modified: Fri, 25 Sep 2020 22:42:18 GMT  
		Size: 1.4 MB (1388751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e19ef40a33a5b2d606204c7a107998bb8d08dbf01e36c3a3bfaee4ec4d46b8`  
		Last Modified: Fri, 25 Sep 2020 22:42:18 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:4f2c9a41b48aebdcbdeb63f6395a43fec8b3f95898c579bc1b4ebeb6f5203172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:2.1.1-builder-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:619abb4972366e19a3cecf06ccf5a5500ee382d8e0b725415afc6671057e3176
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2548379291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be96536344bd43c4263fc0abab1e4100b0e4239c5c5e1448886d9e0dbc697a57`
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
# Wed, 14 Oct 2020 12:41:27 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 14 Oct 2020 12:43:51 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.14.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16bb44448c4423740c5fd751bad28061d5ec44cd08272d4e1efdd16cdf8221e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:43:53 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:01:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:01:07 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:01:07 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 21:01:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:01:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:01:35 GMT
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
	-	`sha256:5de95bbe4c06b5ec1e11f79b684773d419eb2236e0dafc0dc918903f42e520ff`  
		Last Modified: Wed, 14 Oct 2020 12:52:59 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78df25c12716570f89f8a047ef08e7f1b5e034764a58ffd78238fa484bbe6aaa`  
		Last Modified: Wed, 14 Oct 2020 12:53:26 GMT  
		Size: 137.9 MB (137870578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778947ded1566c0dcebc9b8814983e16ff29f501405fd177b1b7cb4c156800a`  
		Last Modified: Wed, 14 Oct 2020 12:53:00 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f24ac044271e744dce202dc376d9e19b77bbbb181b4f403d718cd7ceb9a9c9c`  
		Last Modified: Wed, 14 Oct 2020 21:12:42 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0d4e0f2bcd042a7dc18ce24a67065d60a577911c683ba33376bcd1843c86d4`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ce4de4c08d7c334a4968d897e61681dc85ffe560b778b9db75426907070d9`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9f6c856fee2d7e9adeefb4c769a76404388d9c76c433405d8657594c87b4a1`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd52ae6f924f58c3a7716cc5e56c928033b522a5b884158f19e3dc0282bbee`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.8 MB (1780479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bbf47d6c923e5294e61089f6facc5bf2fae0ee29ea9f1b9a8de2db82c4d6de`  
		Last Modified: Wed, 14 Oct 2020 21:12:38 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:c58c873b8a78ee19c881ea2f7fcaa565352973fa10380dfb0368d7b1b48fe74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.1.1-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4ef9d82eeef794e09e249d568dd248482236de4d0f5d8ae1603910f4f644703b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5936144411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d6db2ab19123c5b5ba620a762bcb9f71e23e1906abd2bf4cbf51abefe863f0`
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
# Wed, 14 Oct 2020 12:44:08 GMT
ENV GOLANG_VERSION=1.14.9
# Wed, 14 Oct 2020 12:47:29 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.14.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16bb44448c4423740c5fd751bad28061d5ec44cd08272d4e1efdd16cdf8221e9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:47:31 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:01:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:01:43 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:01:43 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 14 Oct 2020 21:01:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:03:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:03:01 GMT
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
	-	`sha256:d1c853f53fc418479f31e0f3126ce797d8856ac18457d52a6a8afd2bb82bb901`  
		Last Modified: Wed, 14 Oct 2020 12:53:38 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9252b4af3042a54d971ec0b85e86d2e2630f01f1d86a4bb0ddc033e0784cb329`  
		Last Modified: Wed, 14 Oct 2020 12:56:24 GMT  
		Size: 143.1 MB (143053993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eca72c26de5c2a3894be93ad63055723ded8800314dbfc9a845b927efc0aeda`  
		Last Modified: Wed, 14 Oct 2020 12:53:38 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e704b86c9907a03003c89e4006c7cebd14d9fbaeef88cffac61b74ffc990ec1e`  
		Last Modified: Wed, 14 Oct 2020 21:12:55 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646ed8f4fd451b8bb06909f7beed493e59784b40c8b836a9548f129be1a243a7`  
		Last Modified: Wed, 14 Oct 2020 21:12:52 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2daffddd22c63074b092cff776d945b187cba1cf92e0a614e788134eb3285c`  
		Last Modified: Wed, 14 Oct 2020 21:12:52 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd0551e18d924bf52827df34ede4ff1c46c168f97a2bbd2c8db4f27be986137`  
		Last Modified: Wed, 14 Oct 2020 21:12:53 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6d7cbddd5c4f5a80e822e453f3e6d3f45c753aff73e0a491813661d27075f1`  
		Last Modified: Wed, 14 Oct 2020 21:12:54 GMT  
		Size: 6.8 MB (6836641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ebf859ffb9a352cee6b20f1845441a9e95f6e4e518e492ae9af39c545f992d`  
		Last Modified: Wed, 14 Oct 2020 21:12:52 GMT  
		Size: 1.2 KB (1162 bytes)  
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
$ docker pull caddy@sha256:3a74c78d0fee5eb8ce5450520461a48a6f9e901569a2459912318be59da3823e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.2.1` - linux; amd64

```console
$ docker pull caddy@sha256:63fe670997595a40c2f8c81f38cf634a430587648769244325baf4a21be3010c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fd2a84cc279dbdc53de15daeae84bd726376c255582d12f3d2a3fa105150c9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:27:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:19:42 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:19:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:19:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:19:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:19:47 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:19:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed237faf7b90187b720d5e863fb021a1ca678304744dad14ff8ad6434e4e1da`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 300.0 KB (299981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5bea3a62f2eb8bdd91cf1d01de5e62aa88dbcd8e5834f5dd686a4f1a482531`  
		Last Modified: Fri, 25 Sep 2020 22:28:09 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69398e09bae2fd51db197ec44792b08ec525846a197c98f0b59c7b2f0f9d627`  
		Last Modified: Wed, 14 Oct 2020 19:20:12 GMT  
		Size: 11.5 MB (11532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae648b058e6f63bcb417b92a4c41d61b2af30d50a970bd8d4b959e38bc7415`  
		Last Modified: Wed, 14 Oct 2020 19:20:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - linux; arm variant v6

```console
$ docker pull caddy@sha256:7b5920e4a82b1bf465e06b3cf4893ee2e986063812e261bfa462dc7dda7a2d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13785708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d200bf3c822897c2bfe0d920d00e46b8125144c5947c88455acac1900bb34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:50:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:49:50 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:50:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:51:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:51:09 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:51:16 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:51:23 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:51:29 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:51:35 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:51:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:51:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:51:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:52:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:52:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:52:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:52:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:52:35 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:52:42 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:52:50 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:52:56 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:53:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a5a47b7ff29cc165cee9824ba874fa6cb56d737ce18f841fc3ed5e937cb75`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 300.1 KB (300144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdf9fef63ad932b076740c7fd4eac18d505c2e815b2b27093fae4a1037c1f83`  
		Last Modified: Fri, 25 Sep 2020 22:51:18 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481612b82405dab13f0ff7160cd02b31cafd7702962e9574045583eaed3fc7fe`  
		Last Modified: Wed, 14 Oct 2020 19:55:07 GMT  
		Size: 10.9 MB (10876291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c736385a37cc7654340f9f0217853549d57059a6fa720033afa8d97dea203`  
		Last Modified: Wed, 14 Oct 2020 19:54:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8b43c89dba95e29c51ac668ab67a77e739e67a469eef340fc8d3a7061adeb4b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13566363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01501010b8089fb9a9538277b4324106cc9891e2c01901d93699d43f832e96`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:58:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:58:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:59:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:59:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:59:51 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:00:01 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:00:10 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:00:22 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:00:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:00:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:01:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:01:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:01:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:01:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:01:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:02:02 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:02:17 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:02:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:02:41 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:02:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2aa34f01f2f9112772fdaebe7083b7dcdb4313768e0d6533a3e5b99597c98d`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 299.2 KB (299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f21378d6028fa7cda0d5b592cd8b633c405139cc47eee9863c2b21da4378b`  
		Last Modified: Fri, 25 Sep 2020 22:59:48 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c6573f114e083e57fdf28ed5339e567f2b1c3d13fda1b3b7d806e00f661128`  
		Last Modified: Wed, 14 Oct 2020 20:05:08 GMT  
		Size: 10.9 MB (10854375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660847f79f32b467c1ddaddb5a8306182d9f54c5fe1c2ee2aadd747cf78ed875`  
		Last Modified: Wed, 14 Oct 2020 20:05:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - linux; ppc64le

```console
$ docker pull caddy@sha256:a2f3a819439235784bf7fc8e3826e21acd4ed1825eaaf18e8d159e10e78c0f4d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13293783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12253d19d51ce81473f3f6884026957b92da390eaa7ede0fc8cb5d02f9281359`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 20:49:29 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:49:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 20:50:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 20:50:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 20:50:15 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:50:20 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:50:30 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:50:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:50:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:50:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:51:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:51:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:51:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:51:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:51:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:51:55 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:52:05 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:52:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:52:19 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:52:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b28df4c8a155654ad705e08f459bd177acc1005644ce2173ac62e954d6d4d2`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 302.4 KB (302369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899a5c1a337a29052e5f09180d092a86821dcf3d513b96fdf5db876ec3d6368`  
		Last Modified: Fri, 25 Sep 2020 22:45:34 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eb1518aae776833158c987ae4ac7c130ea2bfa680a61f757641ec0c57aab0c`  
		Last Modified: Wed, 14 Oct 2020 20:53:43 GMT  
		Size: 10.2 MB (10180227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18486e268d34e22c2aaac813d9e42b8401140f0fc8fd5a10b91ce37051de9b79`  
		Last Modified: Wed, 14 Oct 2020 20:53:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1` - linux; s390x

```console
$ docker pull caddy@sha256:9cb650ded68dd03f834621e7bea5b3411e6ac5b1162dbb759fef8acbf6404306
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14075256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54b98421e83dd9ca78953845196b424f44e37cdc25856a0fd9e7e0a38db7190`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:41:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:41:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:41:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:41:40 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc47bdcaea173dfb029a09265c41846030477dc696b22fed52acad2b2078bb7`  
		Last Modified: Mon, 15 Jun 2020 20:44:21 GMT  
		Size: 300.5 KB (300524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b62d245db5345045e7a29f409c7a0109545e93366793659a9538d863745398`  
		Last Modified: Fri, 25 Sep 2020 22:42:24 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec4c67136f6b42bf7c9ffc1b3d6ae4f4f6f8ae1c3da947aaac8391f8c0437f`  
		Last Modified: Wed, 14 Oct 2020 19:42:08 GMT  
		Size: 11.2 MB (11202554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15a505e0b8040884a4e54d19382378931d39e70eb5fddc880f5771f796b06b8`  
		Last Modified: Wed, 14 Oct 2020 19:42:07 GMT  
		Size: 153.0 B  
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
$ docker pull caddy@sha256:183b2be4b53344f077f10606b1399d029975dfb98d8d3a7ea57a4c88087552a3
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
$ docker pull caddy@sha256:63fe670997595a40c2f8c81f38cf634a430587648769244325baf4a21be3010c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fd2a84cc279dbdc53de15daeae84bd726376c255582d12f3d2a3fa105150c9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:27:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:19:42 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:19:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:19:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:19:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:19:47 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:19:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed237faf7b90187b720d5e863fb021a1ca678304744dad14ff8ad6434e4e1da`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 300.0 KB (299981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5bea3a62f2eb8bdd91cf1d01de5e62aa88dbcd8e5834f5dd686a4f1a482531`  
		Last Modified: Fri, 25 Sep 2020 22:28:09 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69398e09bae2fd51db197ec44792b08ec525846a197c98f0b59c7b2f0f9d627`  
		Last Modified: Wed, 14 Oct 2020 19:20:12 GMT  
		Size: 11.5 MB (11532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae648b058e6f63bcb417b92a4c41d61b2af30d50a970bd8d4b959e38bc7415`  
		Last Modified: Wed, 14 Oct 2020 19:20:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:7b5920e4a82b1bf465e06b3cf4893ee2e986063812e261bfa462dc7dda7a2d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13785708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d200bf3c822897c2bfe0d920d00e46b8125144c5947c88455acac1900bb34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:50:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:49:50 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:50:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:51:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:51:09 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:51:16 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:51:23 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:51:29 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:51:35 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:51:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:51:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:51:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:52:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:52:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:52:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:52:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:52:35 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:52:42 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:52:50 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:52:56 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:53:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a5a47b7ff29cc165cee9824ba874fa6cb56d737ce18f841fc3ed5e937cb75`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 300.1 KB (300144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdf9fef63ad932b076740c7fd4eac18d505c2e815b2b27093fae4a1037c1f83`  
		Last Modified: Fri, 25 Sep 2020 22:51:18 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481612b82405dab13f0ff7160cd02b31cafd7702962e9574045583eaed3fc7fe`  
		Last Modified: Wed, 14 Oct 2020 19:55:07 GMT  
		Size: 10.9 MB (10876291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c736385a37cc7654340f9f0217853549d57059a6fa720033afa8d97dea203`  
		Last Modified: Wed, 14 Oct 2020 19:54:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8b43c89dba95e29c51ac668ab67a77e739e67a469eef340fc8d3a7061adeb4b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13566363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01501010b8089fb9a9538277b4324106cc9891e2c01901d93699d43f832e96`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:58:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:58:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:59:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:59:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:59:51 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:00:01 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:00:10 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:00:22 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:00:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:00:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:01:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:01:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:01:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:01:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:01:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:02:02 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:02:17 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:02:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:02:41 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:02:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2aa34f01f2f9112772fdaebe7083b7dcdb4313768e0d6533a3e5b99597c98d`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 299.2 KB (299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f21378d6028fa7cda0d5b592cd8b633c405139cc47eee9863c2b21da4378b`  
		Last Modified: Fri, 25 Sep 2020 22:59:48 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c6573f114e083e57fdf28ed5339e567f2b1c3d13fda1b3b7d806e00f661128`  
		Last Modified: Wed, 14 Oct 2020 20:05:08 GMT  
		Size: 10.9 MB (10854375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660847f79f32b467c1ddaddb5a8306182d9f54c5fe1c2ee2aadd747cf78ed875`  
		Last Modified: Wed, 14 Oct 2020 20:05:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:085d496dad79fa71008de50e50f06591ab871b8f4711510a759b48a560bfe3aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13541809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e9fbe7d7a3cb53f7c6ee613e9c0ac1c82dbdfabb2a5e00cc6e577529e55b14`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:40:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:40:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:40:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:40:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:40:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:40:47 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:40:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:40:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:40:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:40:52 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:40:53 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:40:54 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:40:54 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:40:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f33282aee1a51127f669c7222e26bd0d5107b28d68819a6ead7f68076a73dc`  
		Last Modified: Mon, 15 Jun 2020 20:44:05 GMT  
		Size: 300.4 KB (300393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bbc79642b3dde186ddb45804729b84a8d010ca521d5c376311e2f613371675`  
		Last Modified: Fri, 25 Sep 2020 22:41:23 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f032bb954a154a6fcad58e71dc4fb90dabf12cf1ab3662992264236e3c2bd6e4`  
		Last Modified: Wed, 14 Oct 2020 19:41:31 GMT  
		Size: 10.5 MB (10527467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f62f208da9abbd187aaf41377a50af8149a6e8483fc0e04f5f5f507e4be7e`  
		Last Modified: Wed, 14 Oct 2020 19:41:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:a2f3a819439235784bf7fc8e3826e21acd4ed1825eaaf18e8d159e10e78c0f4d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13293783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12253d19d51ce81473f3f6884026957b92da390eaa7ede0fc8cb5d02f9281359`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 20:49:29 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:49:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 20:50:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 20:50:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 20:50:15 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:50:20 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:50:30 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:50:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:50:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:50:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:51:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:51:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:51:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:51:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:51:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:51:55 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:52:05 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:52:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:52:19 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:52:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b28df4c8a155654ad705e08f459bd177acc1005644ce2173ac62e954d6d4d2`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 302.4 KB (302369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899a5c1a337a29052e5f09180d092a86821dcf3d513b96fdf5db876ec3d6368`  
		Last Modified: Fri, 25 Sep 2020 22:45:34 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eb1518aae776833158c987ae4ac7c130ea2bfa680a61f757641ec0c57aab0c`  
		Last Modified: Wed, 14 Oct 2020 20:53:43 GMT  
		Size: 10.2 MB (10180227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18486e268d34e22c2aaac813d9e42b8401140f0fc8fd5a10b91ce37051de9b79`  
		Last Modified: Wed, 14 Oct 2020 20:53:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9cb650ded68dd03f834621e7bea5b3411e6ac5b1162dbb759fef8acbf6404306
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14075256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54b98421e83dd9ca78953845196b424f44e37cdc25856a0fd9e7e0a38db7190`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:41:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:41:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:41:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:41:40 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc47bdcaea173dfb029a09265c41846030477dc696b22fed52acad2b2078bb7`  
		Last Modified: Mon, 15 Jun 2020 20:44:21 GMT  
		Size: 300.5 KB (300524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b62d245db5345045e7a29f409c7a0109545e93366793659a9538d863745398`  
		Last Modified: Fri, 25 Sep 2020 22:42:24 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec4c67136f6b42bf7c9ffc1b3d6ae4f4f6f8ae1c3da947aaac8391f8c0437f`  
		Last Modified: Wed, 14 Oct 2020 19:42:08 GMT  
		Size: 11.2 MB (11202554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15a505e0b8040884a4e54d19382378931d39e70eb5fddc880f5771f796b06b8`  
		Last Modified: Wed, 14 Oct 2020 19:42:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-builder`

```console
$ docker pull caddy@sha256:f0c24a9a90aedf7b7055dc9b611029d4a0a4b358de29f427c2fbe21c3c322b98
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
$ docker pull caddy@sha256:a390b4809acd419cf9c0a7954e324c4ecbf057ca2f84f8dc32a80dc11afd9481
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120085155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140237d3d47f0447dc9886f905524753902ebdd7b6f7b44d741eb7e62ba95a67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:20:06 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:22:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:22:16 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:22:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:22:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:22:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:27:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:27:45 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:19:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:19:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:19:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:19:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871e8e8d7a9e6e0e8b5c74575f14475ace81baa17901d798568eb6fc89c6605`  
		Last Modified: Wed, 09 Sep 2020 22:28:59 GMT  
		Size: 107.3 MB (107287077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73272ec9a57b94a2277ac06d457ca5382aa07be5c17cfddc44e9572e058f01e`  
		Last Modified: Wed, 09 Sep 2020 22:28:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc77d7d3d1a8614ee91da79da91cf0aad076637b63568e8f37506c7753ce627c`  
		Last Modified: Fri, 25 Sep 2020 22:28:18 GMT  
		Size: 8.3 MB (8310024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74225606380107b86f2b8090c232169ee13b9c4d24b2643943f277f2602491b8`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 1.4 MB (1407220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f01b76a627656998340b6f8731b2b02cdc1095b58cf6360229fc1f413941fd4`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a9bf883ad8cba9ea2999d978904c95e6442b5e81a35d7bf0143389e958915b66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115230626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eea91094e5881890305c5794af85fc485156b8ca9c4888c73aadd577a5ae6f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:51:10 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:53:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:53:57 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:53:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:53:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:54:00 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:50:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:50:39 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:53:27 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:53:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:54:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:54:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33289ebfa0798f70595592ba1a31e18c039bf9047bbf13b9daf83c6bdf47fd9a`  
		Last Modified: Wed, 09 Sep 2020 23:01:48 GMT  
		Size: 103.1 MB (103087634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7835f9f7cff0ebd0351d7c28d6324d6466e20a35d1988db525477611b9909550`  
		Last Modified: Wed, 09 Sep 2020 23:01:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a9ed04456aff68ffe1e84bda9b04c2fa1c359fcd7cb23e64fd328a6d4fe6c`  
		Last Modified: Fri, 25 Sep 2020 22:51:32 GMT  
		Size: 7.9 MB (7928846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc97c54912b2e9a4a3b73bc7845661be88ddce3c7163a4106e656250b3d1046`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 1.3 MB (1327364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a643521102a74cdff40698863e8ab102bc00dcb3aaa0c3a7a2366b55e40be28`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:22d7e5651fc23f90659d5bd8e0f6799aa6401e643739aec3cf02c835845989b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114011088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2278dfa7d9aaa63788ee41c26f3382f6476b6c0fce8cf1d241442beda56d59ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:46:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:01:53 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:04:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:04:13 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:04:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:04:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:04:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:59:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:59:04 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:03:23 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:03:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:04:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:04:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:04:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4617330c6e6b78b275a88d667be57a5b0fb668dab185289351c64522b8bbe65a`  
		Last Modified: Wed, 09 Sep 2020 22:12:18 GMT  
		Size: 102.9 MB (102850878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3139b43ff2f6d56f9dfa6751a3ea1972340b9102c86f45efdc310d66cd69d482`  
		Last Modified: Wed, 09 Sep 2020 22:11:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b18e3ae4626b5fa43914df0ea51e4de5da9432c60cc389a99d9d105c1a9747a`  
		Last Modified: Fri, 25 Sep 2020 23:00:00 GMT  
		Size: 7.1 MB (7144989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419d576ba1751faf2b9aa10f0788e64a79b1367282c7d1ead196ec976bba1c5b`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 1.3 MB (1325847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c9517d14e71111d4034c0256fa3dbde0775a541453da3102614df3d285e226`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:1f76657589db6fa2be75268287cbbab811f3b3f6963c093bbd44635c0659de33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115368944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928d720f438087eba2c14fbaa18b341acc6054534ea8681a1c33371e93d03caf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:40:20 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:42:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:42:09 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:42:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:42:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:42:11 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:40:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:40:46 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:02 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8529a6b9a6be640bc502712219f1fb2745504a3f39ec97daaf85d4c8264af755`  
		Last Modified: Wed, 09 Sep 2020 22:49:05 GMT  
		Size: 102.6 MB (102567178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45590311c82a93cced41b144bb10045cbd6cc2e5021a4cea50b1a72aa405fc1b`  
		Last Modified: Wed, 09 Sep 2020 22:48:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c054b5ce906c9bc36844a82271f2781122ef429003d967ab45644a8e017c7ffd`  
		Last Modified: Fri, 25 Sep 2020 22:41:36 GMT  
		Size: 8.5 MB (8499901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad294bd10348dabe38fe80d1b1ef8dada96b8303efa9273278211cb4179b247`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 1.3 MB (1310185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f47c002964b17e21d766eb617744089f4e0fb377160284fa630766110b24cc`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51e97e4c97ff4eeb5e1a677f345bcb87b5a7623b62e3bef3c4f2fad404cacae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114548833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f08dd245e147ed09ad35833ac5fdf7986cd34cb40918188ca26db058666a560`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:21:49 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:23:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:24:14 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:24:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:24:53 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:43:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:43:49 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:52:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:52:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:52:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:52:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:53:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e5c3bda96921f0fcdc52d34b4e8e57c154d9eeef090c6ca17e00ac1ca58d6`  
		Last Modified: Wed, 09 Sep 2020 22:41:21 GMT  
		Size: 101.3 MB (101250060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb6e866365ec04fdd345e22c049091abf460071fa0470866449b5c14cda08e`  
		Last Modified: Wed, 09 Sep 2020 22:39:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a4b970cfa1f0abf17873192eda639c3d1c128a0daef00315ea38bafa52bc6`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 8.9 MB (8920027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab74e879b267d02b2da382e2c5ca2e22fc5250997d748ba8f7451799fc5d20`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 1.3 MB (1287794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f96b78f4085cc0937cecfcd333f6263f52e5122d5c4b5977299137e870bfc91`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:32be187ea5fb2790ad34c7e181c5692239afc3a3ca882dc159cb34d9ef4f93cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118955263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c54429d0f3f6808444bf196fab77e6e595a1964b6218942f7112fe6c539b057`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:41:59 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:43:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:43:25 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:43:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:43:27 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:41:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:41:57 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:46 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:48 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eabcd3f00523ec5c8f8dca341969baa7b2786a73abc348fb5f39edf7a6410c6`  
		Last Modified: Wed, 09 Sep 2020 22:47:34 GMT  
		Size: 106.4 MB (106364195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36edeb811f26567d876bcc25c7d4c1c9ffb755523494a4c1670fb44b04a763aa`  
		Last Modified: Wed, 09 Sep 2020 22:47:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616042cacfc26da785f94395686f009bfa4b74481d41345619cf42a83dd7e2ab`  
		Last Modified: Fri, 25 Sep 2020 22:42:37 GMT  
		Size: 8.4 MB (8352247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e10f447b72ffcc29a59a55433dd9cf3d2776fff6431999836fa58087046837`  
		Last Modified: Wed, 14 Oct 2020 19:42:17 GMT  
		Size: 1.4 MB (1388769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd5ab0971f40a63405919c02456c3531709f1b7bce49c608bbaf95d646fc601`  
		Last Modified: Wed, 14 Oct 2020 19:42:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:3ba6b600176719bd63edb11bf0ae94e50f988e56cc4e85ba9925f32210861705
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2549189991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d7ef6ab31475a71e36630cb427f3f497c87dec6d112efbc196d70bd86f6817`
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
# Wed, 14 Oct 2020 12:29:03 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:31:28 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:31:30 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:02 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:03 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:09:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:09:31 GMT
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
	-	`sha256:e2d12d413526d5d1d8366bb7e48eb818bf637bacc48474c46cbfd3d4a90fe2b8`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e8fd6fb63c72075cd39946e1f58316f170c83d2690974bd5a81e9c0d8964c5`  
		Last Modified: Wed, 14 Oct 2020 12:50:53 GMT  
		Size: 138.7 MB (138681016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7197fbf266c1c46a72d143a070e8c9e78a5a4a3136a6deeafd6dd9bbf2fe22`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6c87eb231da1d3837c6a7f67c221889f56771cabd853b34e1b7f010139ee71`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069e825d6dd505d81c9a0a93bed795aa7b47f699ed863bd7f3125684664e889e`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5993393cf641947f6f9ab36ebaebffdb6c514ee74ff3373c93a32b83b873b0`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad9ee46931788edc71b3dc6bda2e279927b570cee5a8d0d240046ad9c5d916`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f4804228117bb75ce3d766338b80593b035625bce7d1581d1627f0a6ec683`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.8 MB (1780650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddec9e68813a9c5693c7934ee28aba70ecc97fc46e63b54aed1f39a5775cbe7`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:161ca87862741b3768b5ec1270ceae7d810ca89addff7ed55527e9ea648b2483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941391039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422cfe564b9278afa4fef1765baef01ab6cb4dcab62baae97dee103d14105039`
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
# Wed, 14 Oct 2020 12:35:14 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:38:37 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:38:39 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:38 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:39 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:11:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:11:02 GMT
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
	-	`sha256:43b092cb3237abc132910a3f21e44eeca2309630a905017be2f72a8ad938084d`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccea4c7c8503eedcb64c76b2b9e85bb36f157d91b8f5c218b125ab6c3ec8db7`  
		Last Modified: Wed, 14 Oct 2020 12:51:53 GMT  
		Size: 143.8 MB (143814531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e54f426c13bc41d2bd7bbe44e761440984b17ca53fd22a76a2cc981e0af5852`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690e1fece3f015a20ec4c6a92752e662dd8d92a6f0a3baa711bef8c28bd94f`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be175884faa3fdd2f45ce4a4991a52af6bc99fe2a2992175e59ecb3c668e0b9`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb30b173a9a26b142b7a1b43023f2de9aaec743b5aff188ed793c1d8223630ae`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f925f145dd6e8c98dfa60e7d788bcb25c992ac9c87b55fc784e459d655ca2a04`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9643de6696bb6f4080794fa706656eadc8cbb83eb45987150849096ac540fcc`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 11.3 MB (11322784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992e1b94c1e27f89b0accd8838c7033c7513a149dc64695b4f8e9881d417e123`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-builder-alpine`

```console
$ docker pull caddy@sha256:7c9a89170824bdb5c2cb528051c61b69f71b1fc0c2a1e2eea0bf5aaa33156117
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
$ docker pull caddy@sha256:a390b4809acd419cf9c0a7954e324c4ecbf057ca2f84f8dc32a80dc11afd9481
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120085155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140237d3d47f0447dc9886f905524753902ebdd7b6f7b44d741eb7e62ba95a67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:20:06 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:22:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:22:16 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:22:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:22:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:22:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:27:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:27:45 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:19:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:19:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:19:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:19:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871e8e8d7a9e6e0e8b5c74575f14475ace81baa17901d798568eb6fc89c6605`  
		Last Modified: Wed, 09 Sep 2020 22:28:59 GMT  
		Size: 107.3 MB (107287077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73272ec9a57b94a2277ac06d457ca5382aa07be5c17cfddc44e9572e058f01e`  
		Last Modified: Wed, 09 Sep 2020 22:28:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc77d7d3d1a8614ee91da79da91cf0aad076637b63568e8f37506c7753ce627c`  
		Last Modified: Fri, 25 Sep 2020 22:28:18 GMT  
		Size: 8.3 MB (8310024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74225606380107b86f2b8090c232169ee13b9c4d24b2643943f277f2602491b8`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 1.4 MB (1407220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f01b76a627656998340b6f8731b2b02cdc1095b58cf6360229fc1f413941fd4`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a9bf883ad8cba9ea2999d978904c95e6442b5e81a35d7bf0143389e958915b66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115230626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eea91094e5881890305c5794af85fc485156b8ca9c4888c73aadd577a5ae6f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:51:10 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:53:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:53:57 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:53:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:53:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:54:00 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:50:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:50:39 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:53:27 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:53:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:54:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:54:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33289ebfa0798f70595592ba1a31e18c039bf9047bbf13b9daf83c6bdf47fd9a`  
		Last Modified: Wed, 09 Sep 2020 23:01:48 GMT  
		Size: 103.1 MB (103087634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7835f9f7cff0ebd0351d7c28d6324d6466e20a35d1988db525477611b9909550`  
		Last Modified: Wed, 09 Sep 2020 23:01:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a9ed04456aff68ffe1e84bda9b04c2fa1c359fcd7cb23e64fd328a6d4fe6c`  
		Last Modified: Fri, 25 Sep 2020 22:51:32 GMT  
		Size: 7.9 MB (7928846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc97c54912b2e9a4a3b73bc7845661be88ddce3c7163a4106e656250b3d1046`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 1.3 MB (1327364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a643521102a74cdff40698863e8ab102bc00dcb3aaa0c3a7a2366b55e40be28`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:22d7e5651fc23f90659d5bd8e0f6799aa6401e643739aec3cf02c835845989b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114011088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2278dfa7d9aaa63788ee41c26f3382f6476b6c0fce8cf1d241442beda56d59ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:46:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:01:53 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:04:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:04:13 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:04:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:04:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:04:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:59:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:59:04 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:03:23 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:03:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:04:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:04:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:04:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4617330c6e6b78b275a88d667be57a5b0fb668dab185289351c64522b8bbe65a`  
		Last Modified: Wed, 09 Sep 2020 22:12:18 GMT  
		Size: 102.9 MB (102850878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3139b43ff2f6d56f9dfa6751a3ea1972340b9102c86f45efdc310d66cd69d482`  
		Last Modified: Wed, 09 Sep 2020 22:11:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b18e3ae4626b5fa43914df0ea51e4de5da9432c60cc389a99d9d105c1a9747a`  
		Last Modified: Fri, 25 Sep 2020 23:00:00 GMT  
		Size: 7.1 MB (7144989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419d576ba1751faf2b9aa10f0788e64a79b1367282c7d1ead196ec976bba1c5b`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 1.3 MB (1325847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c9517d14e71111d4034c0256fa3dbde0775a541453da3102614df3d285e226`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:1f76657589db6fa2be75268287cbbab811f3b3f6963c093bbd44635c0659de33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115368944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928d720f438087eba2c14fbaa18b341acc6054534ea8681a1c33371e93d03caf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:40:20 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:42:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:42:09 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:42:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:42:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:42:11 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:40:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:40:46 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:02 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8529a6b9a6be640bc502712219f1fb2745504a3f39ec97daaf85d4c8264af755`  
		Last Modified: Wed, 09 Sep 2020 22:49:05 GMT  
		Size: 102.6 MB (102567178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45590311c82a93cced41b144bb10045cbd6cc2e5021a4cea50b1a72aa405fc1b`  
		Last Modified: Wed, 09 Sep 2020 22:48:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c054b5ce906c9bc36844a82271f2781122ef429003d967ab45644a8e017c7ffd`  
		Last Modified: Fri, 25 Sep 2020 22:41:36 GMT  
		Size: 8.5 MB (8499901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad294bd10348dabe38fe80d1b1ef8dada96b8303efa9273278211cb4179b247`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 1.3 MB (1310185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f47c002964b17e21d766eb617744089f4e0fb377160284fa630766110b24cc`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51e97e4c97ff4eeb5e1a677f345bcb87b5a7623b62e3bef3c4f2fad404cacae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114548833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f08dd245e147ed09ad35833ac5fdf7986cd34cb40918188ca26db058666a560`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:21:49 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:23:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:24:14 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:24:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:24:53 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:43:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:43:49 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:52:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:52:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:52:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:52:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:53:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e5c3bda96921f0fcdc52d34b4e8e57c154d9eeef090c6ca17e00ac1ca58d6`  
		Last Modified: Wed, 09 Sep 2020 22:41:21 GMT  
		Size: 101.3 MB (101250060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb6e866365ec04fdd345e22c049091abf460071fa0470866449b5c14cda08e`  
		Last Modified: Wed, 09 Sep 2020 22:39:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a4b970cfa1f0abf17873192eda639c3d1c128a0daef00315ea38bafa52bc6`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 8.9 MB (8920027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab74e879b267d02b2da382e2c5ca2e22fc5250997d748ba8f7451799fc5d20`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 1.3 MB (1287794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f96b78f4085cc0937cecfcd333f6263f52e5122d5c4b5977299137e870bfc91`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.2.1-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:32be187ea5fb2790ad34c7e181c5692239afc3a3ca882dc159cb34d9ef4f93cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118955263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c54429d0f3f6808444bf196fab77e6e595a1964b6218942f7112fe6c539b057`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:41:59 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:43:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:43:25 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:43:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:43:27 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:41:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:41:57 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:46 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:48 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eabcd3f00523ec5c8f8dca341969baa7b2786a73abc348fb5f39edf7a6410c6`  
		Last Modified: Wed, 09 Sep 2020 22:47:34 GMT  
		Size: 106.4 MB (106364195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36edeb811f26567d876bcc25c7d4c1c9ffb755523494a4c1670fb44b04a763aa`  
		Last Modified: Wed, 09 Sep 2020 22:47:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616042cacfc26da785f94395686f009bfa4b74481d41345619cf42a83dd7e2ab`  
		Last Modified: Fri, 25 Sep 2020 22:42:37 GMT  
		Size: 8.4 MB (8352247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e10f447b72ffcc29a59a55433dd9cf3d2776fff6431999836fa58087046837`  
		Last Modified: Wed, 14 Oct 2020 19:42:17 GMT  
		Size: 1.4 MB (1388769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd5ab0971f40a63405919c02456c3531709f1b7bce49c608bbaf95d646fc601`  
		Last Modified: Wed, 14 Oct 2020 19:42:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:059405ea3383d42da538726c20d809f0f5f585e5bd4bf91da9670787bb2ba357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:2.2.1-builder-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:3ba6b600176719bd63edb11bf0ae94e50f988e56cc4e85ba9925f32210861705
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2549189991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d7ef6ab31475a71e36630cb427f3f497c87dec6d112efbc196d70bd86f6817`
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
# Wed, 14 Oct 2020 12:29:03 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:31:28 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:31:30 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:02 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:03 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:09:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:09:31 GMT
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
	-	`sha256:e2d12d413526d5d1d8366bb7e48eb818bf637bacc48474c46cbfd3d4a90fe2b8`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e8fd6fb63c72075cd39946e1f58316f170c83d2690974bd5a81e9c0d8964c5`  
		Last Modified: Wed, 14 Oct 2020 12:50:53 GMT  
		Size: 138.7 MB (138681016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7197fbf266c1c46a72d143a070e8c9e78a5a4a3136a6deeafd6dd9bbf2fe22`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6c87eb231da1d3837c6a7f67c221889f56771cabd853b34e1b7f010139ee71`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069e825d6dd505d81c9a0a93bed795aa7b47f699ed863bd7f3125684664e889e`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5993393cf641947f6f9ab36ebaebffdb6c514ee74ff3373c93a32b83b873b0`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad9ee46931788edc71b3dc6bda2e279927b570cee5a8d0d240046ad9c5d916`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f4804228117bb75ce3d766338b80593b035625bce7d1581d1627f0a6ec683`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.8 MB (1780650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddec9e68813a9c5693c7934ee28aba70ecc97fc46e63b54aed1f39a5775cbe7`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.2.1-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:bcd37c91cc335877d442d174bc2bd1734af769f863e100be9ae72aea4c9dd730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:2.2.1-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:161ca87862741b3768b5ec1270ceae7d810ca89addff7ed55527e9ea648b2483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941391039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422cfe564b9278afa4fef1765baef01ab6cb4dcab62baae97dee103d14105039`
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
# Wed, 14 Oct 2020 12:35:14 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:38:37 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:38:39 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:38 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:39 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:11:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:11:02 GMT
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
	-	`sha256:43b092cb3237abc132910a3f21e44eeca2309630a905017be2f72a8ad938084d`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccea4c7c8503eedcb64c76b2b9e85bb36f157d91b8f5c218b125ab6c3ec8db7`  
		Last Modified: Wed, 14 Oct 2020 12:51:53 GMT  
		Size: 143.8 MB (143814531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e54f426c13bc41d2bd7bbe44e761440984b17ca53fd22a76a2cc981e0af5852`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690e1fece3f015a20ec4c6a92752e662dd8d92a6f0a3baa711bef8c28bd94f`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be175884faa3fdd2f45ce4a4991a52af6bc99fe2a2992175e59ecb3c668e0b9`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb30b173a9a26b142b7a1b43023f2de9aaec743b5aff188ed793c1d8223630ae`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f925f145dd6e8c98dfa60e7d788bcb25c992ac9c87b55fc784e459d655ca2a04`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9643de6696bb6f4080794fa706656eadc8cbb83eb45987150849096ac540fcc`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 11.3 MB (11322784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992e1b94c1e27f89b0accd8838c7033c7513a149dc64695b4f8e9881d417e123`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1120 bytes)  
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
$ docker pull caddy@sha256:183b2be4b53344f077f10606b1399d029975dfb98d8d3a7ea57a4c88087552a3
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
$ docker pull caddy@sha256:63fe670997595a40c2f8c81f38cf634a430587648769244325baf4a21be3010c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fd2a84cc279dbdc53de15daeae84bd726376c255582d12f3d2a3fa105150c9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:27:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:19:42 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:19:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:19:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:19:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:19:47 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:19:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed237faf7b90187b720d5e863fb021a1ca678304744dad14ff8ad6434e4e1da`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 300.0 KB (299981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5bea3a62f2eb8bdd91cf1d01de5e62aa88dbcd8e5834f5dd686a4f1a482531`  
		Last Modified: Fri, 25 Sep 2020 22:28:09 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69398e09bae2fd51db197ec44792b08ec525846a197c98f0b59c7b2f0f9d627`  
		Last Modified: Wed, 14 Oct 2020 19:20:12 GMT  
		Size: 11.5 MB (11532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae648b058e6f63bcb417b92a4c41d61b2af30d50a970bd8d4b959e38bc7415`  
		Last Modified: Wed, 14 Oct 2020 19:20:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:7b5920e4a82b1bf465e06b3cf4893ee2e986063812e261bfa462dc7dda7a2d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13785708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d200bf3c822897c2bfe0d920d00e46b8125144c5947c88455acac1900bb34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:50:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:49:50 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:50:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:51:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:51:09 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:51:16 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:51:23 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:51:29 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:51:35 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:51:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:51:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:51:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:52:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:52:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:52:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:52:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:52:35 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:52:42 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:52:50 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:52:56 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:53:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a5a47b7ff29cc165cee9824ba874fa6cb56d737ce18f841fc3ed5e937cb75`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 300.1 KB (300144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdf9fef63ad932b076740c7fd4eac18d505c2e815b2b27093fae4a1037c1f83`  
		Last Modified: Fri, 25 Sep 2020 22:51:18 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481612b82405dab13f0ff7160cd02b31cafd7702962e9574045583eaed3fc7fe`  
		Last Modified: Wed, 14 Oct 2020 19:55:07 GMT  
		Size: 10.9 MB (10876291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c736385a37cc7654340f9f0217853549d57059a6fa720033afa8d97dea203`  
		Last Modified: Wed, 14 Oct 2020 19:54:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8b43c89dba95e29c51ac668ab67a77e739e67a469eef340fc8d3a7061adeb4b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13566363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01501010b8089fb9a9538277b4324106cc9891e2c01901d93699d43f832e96`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:58:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:58:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:59:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:59:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:59:51 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:00:01 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:00:10 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:00:22 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:00:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:00:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:01:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:01:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:01:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:01:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:01:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:02:02 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:02:17 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:02:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:02:41 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:02:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2aa34f01f2f9112772fdaebe7083b7dcdb4313768e0d6533a3e5b99597c98d`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 299.2 KB (299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f21378d6028fa7cda0d5b592cd8b633c405139cc47eee9863c2b21da4378b`  
		Last Modified: Fri, 25 Sep 2020 22:59:48 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c6573f114e083e57fdf28ed5339e567f2b1c3d13fda1b3b7d806e00f661128`  
		Last Modified: Wed, 14 Oct 2020 20:05:08 GMT  
		Size: 10.9 MB (10854375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660847f79f32b467c1ddaddb5a8306182d9f54c5fe1c2ee2aadd747cf78ed875`  
		Last Modified: Wed, 14 Oct 2020 20:05:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:085d496dad79fa71008de50e50f06591ab871b8f4711510a759b48a560bfe3aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13541809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e9fbe7d7a3cb53f7c6ee613e9c0ac1c82dbdfabb2a5e00cc6e577529e55b14`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:40:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:40:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:40:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:40:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:40:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:40:47 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:40:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:40:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:40:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:40:52 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:40:53 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:40:54 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:40:54 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:40:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f33282aee1a51127f669c7222e26bd0d5107b28d68819a6ead7f68076a73dc`  
		Last Modified: Mon, 15 Jun 2020 20:44:05 GMT  
		Size: 300.4 KB (300393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bbc79642b3dde186ddb45804729b84a8d010ca521d5c376311e2f613371675`  
		Last Modified: Fri, 25 Sep 2020 22:41:23 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f032bb954a154a6fcad58e71dc4fb90dabf12cf1ab3662992264236e3c2bd6e4`  
		Last Modified: Wed, 14 Oct 2020 19:41:31 GMT  
		Size: 10.5 MB (10527467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f62f208da9abbd187aaf41377a50af8149a6e8483fc0e04f5f5f507e4be7e`  
		Last Modified: Wed, 14 Oct 2020 19:41:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:a2f3a819439235784bf7fc8e3826e21acd4ed1825eaaf18e8d159e10e78c0f4d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13293783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12253d19d51ce81473f3f6884026957b92da390eaa7ede0fc8cb5d02f9281359`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 20:49:29 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:49:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 20:50:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 20:50:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 20:50:15 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:50:20 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:50:30 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:50:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:50:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:50:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:51:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:51:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:51:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:51:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:51:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:51:55 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:52:05 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:52:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:52:19 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:52:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b28df4c8a155654ad705e08f459bd177acc1005644ce2173ac62e954d6d4d2`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 302.4 KB (302369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899a5c1a337a29052e5f09180d092a86821dcf3d513b96fdf5db876ec3d6368`  
		Last Modified: Fri, 25 Sep 2020 22:45:34 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eb1518aae776833158c987ae4ac7c130ea2bfa680a61f757641ec0c57aab0c`  
		Last Modified: Wed, 14 Oct 2020 20:53:43 GMT  
		Size: 10.2 MB (10180227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18486e268d34e22c2aaac813d9e42b8401140f0fc8fd5a10b91ce37051de9b79`  
		Last Modified: Wed, 14 Oct 2020 20:53:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9cb650ded68dd03f834621e7bea5b3411e6ac5b1162dbb759fef8acbf6404306
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14075256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54b98421e83dd9ca78953845196b424f44e37cdc25856a0fd9e7e0a38db7190`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:41:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:41:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:41:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:41:40 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc47bdcaea173dfb029a09265c41846030477dc696b22fed52acad2b2078bb7`  
		Last Modified: Mon, 15 Jun 2020 20:44:21 GMT  
		Size: 300.5 KB (300524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b62d245db5345045e7a29f409c7a0109545e93366793659a9538d863745398`  
		Last Modified: Fri, 25 Sep 2020 22:42:24 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec4c67136f6b42bf7c9ffc1b3d6ae4f4f6f8ae1c3da947aaac8391f8c0437f`  
		Last Modified: Wed, 14 Oct 2020 19:42:08 GMT  
		Size: 11.2 MB (11202554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15a505e0b8040884a4e54d19382378931d39e70eb5fddc880f5771f796b06b8`  
		Last Modified: Wed, 14 Oct 2020 19:42:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:f0c24a9a90aedf7b7055dc9b611029d4a0a4b358de29f427c2fbe21c3c322b98
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
$ docker pull caddy@sha256:a390b4809acd419cf9c0a7954e324c4ecbf057ca2f84f8dc32a80dc11afd9481
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120085155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140237d3d47f0447dc9886f905524753902ebdd7b6f7b44d741eb7e62ba95a67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:20:06 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:22:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:22:16 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:22:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:22:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:22:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:27:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:27:45 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:19:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:19:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:19:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:19:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871e8e8d7a9e6e0e8b5c74575f14475ace81baa17901d798568eb6fc89c6605`  
		Last Modified: Wed, 09 Sep 2020 22:28:59 GMT  
		Size: 107.3 MB (107287077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73272ec9a57b94a2277ac06d457ca5382aa07be5c17cfddc44e9572e058f01e`  
		Last Modified: Wed, 09 Sep 2020 22:28:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc77d7d3d1a8614ee91da79da91cf0aad076637b63568e8f37506c7753ce627c`  
		Last Modified: Fri, 25 Sep 2020 22:28:18 GMT  
		Size: 8.3 MB (8310024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74225606380107b86f2b8090c232169ee13b9c4d24b2643943f277f2602491b8`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 1.4 MB (1407220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f01b76a627656998340b6f8731b2b02cdc1095b58cf6360229fc1f413941fd4`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a9bf883ad8cba9ea2999d978904c95e6442b5e81a35d7bf0143389e958915b66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115230626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eea91094e5881890305c5794af85fc485156b8ca9c4888c73aadd577a5ae6f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:51:10 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:53:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:53:57 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:53:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:53:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:54:00 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:50:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:50:39 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:53:27 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:53:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:54:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:54:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33289ebfa0798f70595592ba1a31e18c039bf9047bbf13b9daf83c6bdf47fd9a`  
		Last Modified: Wed, 09 Sep 2020 23:01:48 GMT  
		Size: 103.1 MB (103087634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7835f9f7cff0ebd0351d7c28d6324d6466e20a35d1988db525477611b9909550`  
		Last Modified: Wed, 09 Sep 2020 23:01:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a9ed04456aff68ffe1e84bda9b04c2fa1c359fcd7cb23e64fd328a6d4fe6c`  
		Last Modified: Fri, 25 Sep 2020 22:51:32 GMT  
		Size: 7.9 MB (7928846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc97c54912b2e9a4a3b73bc7845661be88ddce3c7163a4106e656250b3d1046`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 1.3 MB (1327364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a643521102a74cdff40698863e8ab102bc00dcb3aaa0c3a7a2366b55e40be28`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:22d7e5651fc23f90659d5bd8e0f6799aa6401e643739aec3cf02c835845989b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114011088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2278dfa7d9aaa63788ee41c26f3382f6476b6c0fce8cf1d241442beda56d59ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:46:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:01:53 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:04:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:04:13 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:04:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:04:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:04:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:59:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:59:04 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:03:23 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:03:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:04:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:04:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:04:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4617330c6e6b78b275a88d667be57a5b0fb668dab185289351c64522b8bbe65a`  
		Last Modified: Wed, 09 Sep 2020 22:12:18 GMT  
		Size: 102.9 MB (102850878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3139b43ff2f6d56f9dfa6751a3ea1972340b9102c86f45efdc310d66cd69d482`  
		Last Modified: Wed, 09 Sep 2020 22:11:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b18e3ae4626b5fa43914df0ea51e4de5da9432c60cc389a99d9d105c1a9747a`  
		Last Modified: Fri, 25 Sep 2020 23:00:00 GMT  
		Size: 7.1 MB (7144989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419d576ba1751faf2b9aa10f0788e64a79b1367282c7d1ead196ec976bba1c5b`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 1.3 MB (1325847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c9517d14e71111d4034c0256fa3dbde0775a541453da3102614df3d285e226`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:1f76657589db6fa2be75268287cbbab811f3b3f6963c093bbd44635c0659de33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115368944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928d720f438087eba2c14fbaa18b341acc6054534ea8681a1c33371e93d03caf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:40:20 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:42:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:42:09 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:42:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:42:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:42:11 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:40:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:40:46 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:02 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8529a6b9a6be640bc502712219f1fb2745504a3f39ec97daaf85d4c8264af755`  
		Last Modified: Wed, 09 Sep 2020 22:49:05 GMT  
		Size: 102.6 MB (102567178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45590311c82a93cced41b144bb10045cbd6cc2e5021a4cea50b1a72aa405fc1b`  
		Last Modified: Wed, 09 Sep 2020 22:48:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c054b5ce906c9bc36844a82271f2781122ef429003d967ab45644a8e017c7ffd`  
		Last Modified: Fri, 25 Sep 2020 22:41:36 GMT  
		Size: 8.5 MB (8499901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad294bd10348dabe38fe80d1b1ef8dada96b8303efa9273278211cb4179b247`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 1.3 MB (1310185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f47c002964b17e21d766eb617744089f4e0fb377160284fa630766110b24cc`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51e97e4c97ff4eeb5e1a677f345bcb87b5a7623b62e3bef3c4f2fad404cacae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114548833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f08dd245e147ed09ad35833ac5fdf7986cd34cb40918188ca26db058666a560`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:21:49 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:23:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:24:14 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:24:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:24:53 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:43:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:43:49 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:52:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:52:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:52:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:52:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:53:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e5c3bda96921f0fcdc52d34b4e8e57c154d9eeef090c6ca17e00ac1ca58d6`  
		Last Modified: Wed, 09 Sep 2020 22:41:21 GMT  
		Size: 101.3 MB (101250060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb6e866365ec04fdd345e22c049091abf460071fa0470866449b5c14cda08e`  
		Last Modified: Wed, 09 Sep 2020 22:39:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a4b970cfa1f0abf17873192eda639c3d1c128a0daef00315ea38bafa52bc6`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 8.9 MB (8920027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab74e879b267d02b2da382e2c5ca2e22fc5250997d748ba8f7451799fc5d20`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 1.3 MB (1287794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f96b78f4085cc0937cecfcd333f6263f52e5122d5c4b5977299137e870bfc91`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:32be187ea5fb2790ad34c7e181c5692239afc3a3ca882dc159cb34d9ef4f93cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118955263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c54429d0f3f6808444bf196fab77e6e595a1964b6218942f7112fe6c539b057`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:41:59 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:43:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:43:25 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:43:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:43:27 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:41:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:41:57 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:46 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:48 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eabcd3f00523ec5c8f8dca341969baa7b2786a73abc348fb5f39edf7a6410c6`  
		Last Modified: Wed, 09 Sep 2020 22:47:34 GMT  
		Size: 106.4 MB (106364195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36edeb811f26567d876bcc25c7d4c1c9ffb755523494a4c1670fb44b04a763aa`  
		Last Modified: Wed, 09 Sep 2020 22:47:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616042cacfc26da785f94395686f009bfa4b74481d41345619cf42a83dd7e2ab`  
		Last Modified: Fri, 25 Sep 2020 22:42:37 GMT  
		Size: 8.4 MB (8352247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e10f447b72ffcc29a59a55433dd9cf3d2776fff6431999836fa58087046837`  
		Last Modified: Wed, 14 Oct 2020 19:42:17 GMT  
		Size: 1.4 MB (1388769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd5ab0971f40a63405919c02456c3531709f1b7bce49c608bbaf95d646fc601`  
		Last Modified: Wed, 14 Oct 2020 19:42:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:3ba6b600176719bd63edb11bf0ae94e50f988e56cc4e85ba9925f32210861705
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2549189991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d7ef6ab31475a71e36630cb427f3f497c87dec6d112efbc196d70bd86f6817`
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
# Wed, 14 Oct 2020 12:29:03 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:31:28 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:31:30 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:02 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:03 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:09:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:09:31 GMT
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
	-	`sha256:e2d12d413526d5d1d8366bb7e48eb818bf637bacc48474c46cbfd3d4a90fe2b8`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e8fd6fb63c72075cd39946e1f58316f170c83d2690974bd5a81e9c0d8964c5`  
		Last Modified: Wed, 14 Oct 2020 12:50:53 GMT  
		Size: 138.7 MB (138681016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7197fbf266c1c46a72d143a070e8c9e78a5a4a3136a6deeafd6dd9bbf2fe22`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6c87eb231da1d3837c6a7f67c221889f56771cabd853b34e1b7f010139ee71`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069e825d6dd505d81c9a0a93bed795aa7b47f699ed863bd7f3125684664e889e`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5993393cf641947f6f9ab36ebaebffdb6c514ee74ff3373c93a32b83b873b0`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad9ee46931788edc71b3dc6bda2e279927b570cee5a8d0d240046ad9c5d916`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f4804228117bb75ce3d766338b80593b035625bce7d1581d1627f0a6ec683`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.8 MB (1780650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddec9e68813a9c5693c7934ee28aba70ecc97fc46e63b54aed1f39a5775cbe7`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:161ca87862741b3768b5ec1270ceae7d810ca89addff7ed55527e9ea648b2483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941391039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422cfe564b9278afa4fef1765baef01ab6cb4dcab62baae97dee103d14105039`
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
# Wed, 14 Oct 2020 12:35:14 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:38:37 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:38:39 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:38 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:39 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:11:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:11:02 GMT
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
	-	`sha256:43b092cb3237abc132910a3f21e44eeca2309630a905017be2f72a8ad938084d`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccea4c7c8503eedcb64c76b2b9e85bb36f157d91b8f5c218b125ab6c3ec8db7`  
		Last Modified: Wed, 14 Oct 2020 12:51:53 GMT  
		Size: 143.8 MB (143814531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e54f426c13bc41d2bd7bbe44e761440984b17ca53fd22a76a2cc981e0af5852`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690e1fece3f015a20ec4c6a92752e662dd8d92a6f0a3baa711bef8c28bd94f`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be175884faa3fdd2f45ce4a4991a52af6bc99fe2a2992175e59ecb3c668e0b9`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb30b173a9a26b142b7a1b43023f2de9aaec743b5aff188ed793c1d8223630ae`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f925f145dd6e8c98dfa60e7d788bcb25c992ac9c87b55fc784e459d655ca2a04`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9643de6696bb6f4080794fa706656eadc8cbb83eb45987150849096ac540fcc`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 11.3 MB (11322784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992e1b94c1e27f89b0accd8838c7033c7513a149dc64695b4f8e9881d417e123`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:7c9a89170824bdb5c2cb528051c61b69f71b1fc0c2a1e2eea0bf5aaa33156117
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
$ docker pull caddy@sha256:a390b4809acd419cf9c0a7954e324c4ecbf057ca2f84f8dc32a80dc11afd9481
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120085155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140237d3d47f0447dc9886f905524753902ebdd7b6f7b44d741eb7e62ba95a67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:20:06 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:22:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:22:16 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:22:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:22:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:22:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:27:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:27:45 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:19:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:19:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:19:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:19:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871e8e8d7a9e6e0e8b5c74575f14475ace81baa17901d798568eb6fc89c6605`  
		Last Modified: Wed, 09 Sep 2020 22:28:59 GMT  
		Size: 107.3 MB (107287077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73272ec9a57b94a2277ac06d457ca5382aa07be5c17cfddc44e9572e058f01e`  
		Last Modified: Wed, 09 Sep 2020 22:28:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc77d7d3d1a8614ee91da79da91cf0aad076637b63568e8f37506c7753ce627c`  
		Last Modified: Fri, 25 Sep 2020 22:28:18 GMT  
		Size: 8.3 MB (8310024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74225606380107b86f2b8090c232169ee13b9c4d24b2643943f277f2602491b8`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 1.4 MB (1407220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f01b76a627656998340b6f8731b2b02cdc1095b58cf6360229fc1f413941fd4`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a9bf883ad8cba9ea2999d978904c95e6442b5e81a35d7bf0143389e958915b66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115230626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eea91094e5881890305c5794af85fc485156b8ca9c4888c73aadd577a5ae6f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:51:10 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:53:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:53:57 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:53:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:53:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:54:00 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:50:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:50:39 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:53:27 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:53:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:54:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:54:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33289ebfa0798f70595592ba1a31e18c039bf9047bbf13b9daf83c6bdf47fd9a`  
		Last Modified: Wed, 09 Sep 2020 23:01:48 GMT  
		Size: 103.1 MB (103087634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7835f9f7cff0ebd0351d7c28d6324d6466e20a35d1988db525477611b9909550`  
		Last Modified: Wed, 09 Sep 2020 23:01:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a9ed04456aff68ffe1e84bda9b04c2fa1c359fcd7cb23e64fd328a6d4fe6c`  
		Last Modified: Fri, 25 Sep 2020 22:51:32 GMT  
		Size: 7.9 MB (7928846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc97c54912b2e9a4a3b73bc7845661be88ddce3c7163a4106e656250b3d1046`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 1.3 MB (1327364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a643521102a74cdff40698863e8ab102bc00dcb3aaa0c3a7a2366b55e40be28`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:22d7e5651fc23f90659d5bd8e0f6799aa6401e643739aec3cf02c835845989b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114011088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2278dfa7d9aaa63788ee41c26f3382f6476b6c0fce8cf1d241442beda56d59ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:46:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:01:53 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:04:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:04:13 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:04:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:04:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:04:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:59:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:59:04 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:03:23 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:03:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:04:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:04:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:04:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4617330c6e6b78b275a88d667be57a5b0fb668dab185289351c64522b8bbe65a`  
		Last Modified: Wed, 09 Sep 2020 22:12:18 GMT  
		Size: 102.9 MB (102850878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3139b43ff2f6d56f9dfa6751a3ea1972340b9102c86f45efdc310d66cd69d482`  
		Last Modified: Wed, 09 Sep 2020 22:11:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b18e3ae4626b5fa43914df0ea51e4de5da9432c60cc389a99d9d105c1a9747a`  
		Last Modified: Fri, 25 Sep 2020 23:00:00 GMT  
		Size: 7.1 MB (7144989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419d576ba1751faf2b9aa10f0788e64a79b1367282c7d1ead196ec976bba1c5b`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 1.3 MB (1325847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c9517d14e71111d4034c0256fa3dbde0775a541453da3102614df3d285e226`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:1f76657589db6fa2be75268287cbbab811f3b3f6963c093bbd44635c0659de33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115368944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928d720f438087eba2c14fbaa18b341acc6054534ea8681a1c33371e93d03caf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:40:20 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:42:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:42:09 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:42:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:42:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:42:11 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:40:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:40:46 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:02 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8529a6b9a6be640bc502712219f1fb2745504a3f39ec97daaf85d4c8264af755`  
		Last Modified: Wed, 09 Sep 2020 22:49:05 GMT  
		Size: 102.6 MB (102567178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45590311c82a93cced41b144bb10045cbd6cc2e5021a4cea50b1a72aa405fc1b`  
		Last Modified: Wed, 09 Sep 2020 22:48:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c054b5ce906c9bc36844a82271f2781122ef429003d967ab45644a8e017c7ffd`  
		Last Modified: Fri, 25 Sep 2020 22:41:36 GMT  
		Size: 8.5 MB (8499901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad294bd10348dabe38fe80d1b1ef8dada96b8303efa9273278211cb4179b247`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 1.3 MB (1310185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f47c002964b17e21d766eb617744089f4e0fb377160284fa630766110b24cc`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51e97e4c97ff4eeb5e1a677f345bcb87b5a7623b62e3bef3c4f2fad404cacae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114548833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f08dd245e147ed09ad35833ac5fdf7986cd34cb40918188ca26db058666a560`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:21:49 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:23:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:24:14 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:24:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:24:53 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:43:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:43:49 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:52:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:52:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:52:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:52:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:53:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e5c3bda96921f0fcdc52d34b4e8e57c154d9eeef090c6ca17e00ac1ca58d6`  
		Last Modified: Wed, 09 Sep 2020 22:41:21 GMT  
		Size: 101.3 MB (101250060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb6e866365ec04fdd345e22c049091abf460071fa0470866449b5c14cda08e`  
		Last Modified: Wed, 09 Sep 2020 22:39:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a4b970cfa1f0abf17873192eda639c3d1c128a0daef00315ea38bafa52bc6`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 8.9 MB (8920027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab74e879b267d02b2da382e2c5ca2e22fc5250997d748ba8f7451799fc5d20`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 1.3 MB (1287794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f96b78f4085cc0937cecfcd333f6263f52e5122d5c4b5977299137e870bfc91`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:32be187ea5fb2790ad34c7e181c5692239afc3a3ca882dc159cb34d9ef4f93cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118955263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c54429d0f3f6808444bf196fab77e6e595a1964b6218942f7112fe6c539b057`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:41:59 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:43:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:43:25 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:43:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:43:27 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:41:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:41:57 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:46 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:48 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eabcd3f00523ec5c8f8dca341969baa7b2786a73abc348fb5f39edf7a6410c6`  
		Last Modified: Wed, 09 Sep 2020 22:47:34 GMT  
		Size: 106.4 MB (106364195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36edeb811f26567d876bcc25c7d4c1c9ffb755523494a4c1670fb44b04a763aa`  
		Last Modified: Wed, 09 Sep 2020 22:47:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616042cacfc26da785f94395686f009bfa4b74481d41345619cf42a83dd7e2ab`  
		Last Modified: Fri, 25 Sep 2020 22:42:37 GMT  
		Size: 8.4 MB (8352247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e10f447b72ffcc29a59a55433dd9cf3d2776fff6431999836fa58087046837`  
		Last Modified: Wed, 14 Oct 2020 19:42:17 GMT  
		Size: 1.4 MB (1388769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd5ab0971f40a63405919c02456c3531709f1b7bce49c608bbaf95d646fc601`  
		Last Modified: Wed, 14 Oct 2020 19:42:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:059405ea3383d42da538726c20d809f0f5f585e5bd4bf91da9670787bb2ba357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:3ba6b600176719bd63edb11bf0ae94e50f988e56cc4e85ba9925f32210861705
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2549189991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d7ef6ab31475a71e36630cb427f3f497c87dec6d112efbc196d70bd86f6817`
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
# Wed, 14 Oct 2020 12:29:03 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:31:28 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:31:30 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:02 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:03 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:09:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:09:31 GMT
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
	-	`sha256:e2d12d413526d5d1d8366bb7e48eb818bf637bacc48474c46cbfd3d4a90fe2b8`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e8fd6fb63c72075cd39946e1f58316f170c83d2690974bd5a81e9c0d8964c5`  
		Last Modified: Wed, 14 Oct 2020 12:50:53 GMT  
		Size: 138.7 MB (138681016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7197fbf266c1c46a72d143a070e8c9e78a5a4a3136a6deeafd6dd9bbf2fe22`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6c87eb231da1d3837c6a7f67c221889f56771cabd853b34e1b7f010139ee71`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069e825d6dd505d81c9a0a93bed795aa7b47f699ed863bd7f3125684664e889e`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5993393cf641947f6f9ab36ebaebffdb6c514ee74ff3373c93a32b83b873b0`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad9ee46931788edc71b3dc6bda2e279927b570cee5a8d0d240046ad9c5d916`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f4804228117bb75ce3d766338b80593b035625bce7d1581d1627f0a6ec683`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.8 MB (1780650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddec9e68813a9c5693c7934ee28aba70ecc97fc46e63b54aed1f39a5775cbe7`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:bcd37c91cc335877d442d174bc2bd1734af769f863e100be9ae72aea4c9dd730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:161ca87862741b3768b5ec1270ceae7d810ca89addff7ed55527e9ea648b2483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941391039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422cfe564b9278afa4fef1765baef01ab6cb4dcab62baae97dee103d14105039`
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
# Wed, 14 Oct 2020 12:35:14 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:38:37 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:38:39 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:38 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:39 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:11:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:11:02 GMT
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
	-	`sha256:43b092cb3237abc132910a3f21e44eeca2309630a905017be2f72a8ad938084d`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccea4c7c8503eedcb64c76b2b9e85bb36f157d91b8f5c218b125ab6c3ec8db7`  
		Last Modified: Wed, 14 Oct 2020 12:51:53 GMT  
		Size: 143.8 MB (143814531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e54f426c13bc41d2bd7bbe44e761440984b17ca53fd22a76a2cc981e0af5852`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690e1fece3f015a20ec4c6a92752e662dd8d92a6f0a3baa711bef8c28bd94f`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be175884faa3fdd2f45ce4a4991a52af6bc99fe2a2992175e59ecb3c668e0b9`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb30b173a9a26b142b7a1b43023f2de9aaec743b5aff188ed793c1d8223630ae`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f925f145dd6e8c98dfa60e7d788bcb25c992ac9c87b55fc784e459d655ca2a04`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9643de6696bb6f4080794fa706656eadc8cbb83eb45987150849096ac540fcc`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 11.3 MB (11322784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992e1b94c1e27f89b0accd8838c7033c7513a149dc64695b4f8e9881d417e123`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1120 bytes)  
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
$ docker pull caddy@sha256:183b2be4b53344f077f10606b1399d029975dfb98d8d3a7ea57a4c88087552a3
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
$ docker pull caddy@sha256:63fe670997595a40c2f8c81f38cf634a430587648769244325baf4a21be3010c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fd2a84cc279dbdc53de15daeae84bd726376c255582d12f3d2a3fa105150c9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:27:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:19:42 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:19:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:19:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:19:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:19:47 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:19:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed237faf7b90187b720d5e863fb021a1ca678304744dad14ff8ad6434e4e1da`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 300.0 KB (299981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5bea3a62f2eb8bdd91cf1d01de5e62aa88dbcd8e5834f5dd686a4f1a482531`  
		Last Modified: Fri, 25 Sep 2020 22:28:09 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69398e09bae2fd51db197ec44792b08ec525846a197c98f0b59c7b2f0f9d627`  
		Last Modified: Wed, 14 Oct 2020 19:20:12 GMT  
		Size: 11.5 MB (11532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae648b058e6f63bcb417b92a4c41d61b2af30d50a970bd8d4b959e38bc7415`  
		Last Modified: Wed, 14 Oct 2020 19:20:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:7b5920e4a82b1bf465e06b3cf4893ee2e986063812e261bfa462dc7dda7a2d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13785708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d200bf3c822897c2bfe0d920d00e46b8125144c5947c88455acac1900bb34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:50:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:49:50 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:50:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:51:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:51:09 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:51:16 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:51:23 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:51:29 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:51:35 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:51:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:51:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:51:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:52:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:52:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:52:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:52:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:52:35 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:52:42 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:52:50 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:52:56 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:53:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a5a47b7ff29cc165cee9824ba874fa6cb56d737ce18f841fc3ed5e937cb75`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 300.1 KB (300144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdf9fef63ad932b076740c7fd4eac18d505c2e815b2b27093fae4a1037c1f83`  
		Last Modified: Fri, 25 Sep 2020 22:51:18 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481612b82405dab13f0ff7160cd02b31cafd7702962e9574045583eaed3fc7fe`  
		Last Modified: Wed, 14 Oct 2020 19:55:07 GMT  
		Size: 10.9 MB (10876291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c736385a37cc7654340f9f0217853549d57059a6fa720033afa8d97dea203`  
		Last Modified: Wed, 14 Oct 2020 19:54:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8b43c89dba95e29c51ac668ab67a77e739e67a469eef340fc8d3a7061adeb4b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13566363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01501010b8089fb9a9538277b4324106cc9891e2c01901d93699d43f832e96`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:58:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:58:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:59:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:59:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:59:51 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:00:01 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:00:10 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:00:22 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:00:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:00:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:01:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:01:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:01:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:01:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:01:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:02:02 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:02:17 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:02:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:02:41 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:02:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2aa34f01f2f9112772fdaebe7083b7dcdb4313768e0d6533a3e5b99597c98d`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 299.2 KB (299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f21378d6028fa7cda0d5b592cd8b633c405139cc47eee9863c2b21da4378b`  
		Last Modified: Fri, 25 Sep 2020 22:59:48 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c6573f114e083e57fdf28ed5339e567f2b1c3d13fda1b3b7d806e00f661128`  
		Last Modified: Wed, 14 Oct 2020 20:05:08 GMT  
		Size: 10.9 MB (10854375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660847f79f32b467c1ddaddb5a8306182d9f54c5fe1c2ee2aadd747cf78ed875`  
		Last Modified: Wed, 14 Oct 2020 20:05:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:085d496dad79fa71008de50e50f06591ab871b8f4711510a759b48a560bfe3aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13541809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e9fbe7d7a3cb53f7c6ee613e9c0ac1c82dbdfabb2a5e00cc6e577529e55b14`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:40:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:40:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:40:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:40:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:40:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:40:47 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:40:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:40:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:40:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:40:52 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:40:53 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:40:54 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:40:54 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:40:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f33282aee1a51127f669c7222e26bd0d5107b28d68819a6ead7f68076a73dc`  
		Last Modified: Mon, 15 Jun 2020 20:44:05 GMT  
		Size: 300.4 KB (300393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bbc79642b3dde186ddb45804729b84a8d010ca521d5c376311e2f613371675`  
		Last Modified: Fri, 25 Sep 2020 22:41:23 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f032bb954a154a6fcad58e71dc4fb90dabf12cf1ab3662992264236e3c2bd6e4`  
		Last Modified: Wed, 14 Oct 2020 19:41:31 GMT  
		Size: 10.5 MB (10527467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f62f208da9abbd187aaf41377a50af8149a6e8483fc0e04f5f5f507e4be7e`  
		Last Modified: Wed, 14 Oct 2020 19:41:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:a2f3a819439235784bf7fc8e3826e21acd4ed1825eaaf18e8d159e10e78c0f4d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13293783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12253d19d51ce81473f3f6884026957b92da390eaa7ede0fc8cb5d02f9281359`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 20:49:29 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:49:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 20:50:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 20:50:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 20:50:15 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:50:20 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:50:30 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:50:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:50:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:50:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:51:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:51:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:51:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:51:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:51:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:51:55 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:52:05 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:52:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:52:19 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:52:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b28df4c8a155654ad705e08f459bd177acc1005644ce2173ac62e954d6d4d2`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 302.4 KB (302369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899a5c1a337a29052e5f09180d092a86821dcf3d513b96fdf5db876ec3d6368`  
		Last Modified: Fri, 25 Sep 2020 22:45:34 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eb1518aae776833158c987ae4ac7c130ea2bfa680a61f757641ec0c57aab0c`  
		Last Modified: Wed, 14 Oct 2020 20:53:43 GMT  
		Size: 10.2 MB (10180227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18486e268d34e22c2aaac813d9e42b8401140f0fc8fd5a10b91ce37051de9b79`  
		Last Modified: Wed, 14 Oct 2020 20:53:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9cb650ded68dd03f834621e7bea5b3411e6ac5b1162dbb759fef8acbf6404306
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14075256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54b98421e83dd9ca78953845196b424f44e37cdc25856a0fd9e7e0a38db7190`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:41:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:41:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:41:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:41:40 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc47bdcaea173dfb029a09265c41846030477dc696b22fed52acad2b2078bb7`  
		Last Modified: Mon, 15 Jun 2020 20:44:21 GMT  
		Size: 300.5 KB (300524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b62d245db5345045e7a29f409c7a0109545e93366793659a9538d863745398`  
		Last Modified: Fri, 25 Sep 2020 22:42:24 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec4c67136f6b42bf7c9ffc1b3d6ae4f4f6f8ae1c3da947aaac8391f8c0437f`  
		Last Modified: Wed, 14 Oct 2020 19:42:08 GMT  
		Size: 11.2 MB (11202554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15a505e0b8040884a4e54d19382378931d39e70eb5fddc880f5771f796b06b8`  
		Last Modified: Wed, 14 Oct 2020 19:42:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:f0c24a9a90aedf7b7055dc9b611029d4a0a4b358de29f427c2fbe21c3c322b98
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
$ docker pull caddy@sha256:a390b4809acd419cf9c0a7954e324c4ecbf057ca2f84f8dc32a80dc11afd9481
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120085155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140237d3d47f0447dc9886f905524753902ebdd7b6f7b44d741eb7e62ba95a67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:20:06 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:22:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:22:16 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:22:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:22:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:22:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:27:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:27:45 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:19:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:19:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:19:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:19:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871e8e8d7a9e6e0e8b5c74575f14475ace81baa17901d798568eb6fc89c6605`  
		Last Modified: Wed, 09 Sep 2020 22:28:59 GMT  
		Size: 107.3 MB (107287077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73272ec9a57b94a2277ac06d457ca5382aa07be5c17cfddc44e9572e058f01e`  
		Last Modified: Wed, 09 Sep 2020 22:28:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc77d7d3d1a8614ee91da79da91cf0aad076637b63568e8f37506c7753ce627c`  
		Last Modified: Fri, 25 Sep 2020 22:28:18 GMT  
		Size: 8.3 MB (8310024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74225606380107b86f2b8090c232169ee13b9c4d24b2643943f277f2602491b8`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 1.4 MB (1407220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f01b76a627656998340b6f8731b2b02cdc1095b58cf6360229fc1f413941fd4`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a9bf883ad8cba9ea2999d978904c95e6442b5e81a35d7bf0143389e958915b66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115230626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eea91094e5881890305c5794af85fc485156b8ca9c4888c73aadd577a5ae6f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:51:10 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:53:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:53:57 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:53:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:53:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:54:00 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:50:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:50:39 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:53:27 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:53:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:54:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:54:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33289ebfa0798f70595592ba1a31e18c039bf9047bbf13b9daf83c6bdf47fd9a`  
		Last Modified: Wed, 09 Sep 2020 23:01:48 GMT  
		Size: 103.1 MB (103087634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7835f9f7cff0ebd0351d7c28d6324d6466e20a35d1988db525477611b9909550`  
		Last Modified: Wed, 09 Sep 2020 23:01:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a9ed04456aff68ffe1e84bda9b04c2fa1c359fcd7cb23e64fd328a6d4fe6c`  
		Last Modified: Fri, 25 Sep 2020 22:51:32 GMT  
		Size: 7.9 MB (7928846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc97c54912b2e9a4a3b73bc7845661be88ddce3c7163a4106e656250b3d1046`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 1.3 MB (1327364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a643521102a74cdff40698863e8ab102bc00dcb3aaa0c3a7a2366b55e40be28`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:22d7e5651fc23f90659d5bd8e0f6799aa6401e643739aec3cf02c835845989b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114011088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2278dfa7d9aaa63788ee41c26f3382f6476b6c0fce8cf1d241442beda56d59ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:46:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:01:53 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:04:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:04:13 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:04:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:04:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:04:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:59:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:59:04 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:03:23 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:03:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:04:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:04:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:04:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4617330c6e6b78b275a88d667be57a5b0fb668dab185289351c64522b8bbe65a`  
		Last Modified: Wed, 09 Sep 2020 22:12:18 GMT  
		Size: 102.9 MB (102850878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3139b43ff2f6d56f9dfa6751a3ea1972340b9102c86f45efdc310d66cd69d482`  
		Last Modified: Wed, 09 Sep 2020 22:11:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b18e3ae4626b5fa43914df0ea51e4de5da9432c60cc389a99d9d105c1a9747a`  
		Last Modified: Fri, 25 Sep 2020 23:00:00 GMT  
		Size: 7.1 MB (7144989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419d576ba1751faf2b9aa10f0788e64a79b1367282c7d1ead196ec976bba1c5b`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 1.3 MB (1325847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c9517d14e71111d4034c0256fa3dbde0775a541453da3102614df3d285e226`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:1f76657589db6fa2be75268287cbbab811f3b3f6963c093bbd44635c0659de33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115368944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928d720f438087eba2c14fbaa18b341acc6054534ea8681a1c33371e93d03caf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:40:20 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:42:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:42:09 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:42:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:42:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:42:11 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:40:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:40:46 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:02 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8529a6b9a6be640bc502712219f1fb2745504a3f39ec97daaf85d4c8264af755`  
		Last Modified: Wed, 09 Sep 2020 22:49:05 GMT  
		Size: 102.6 MB (102567178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45590311c82a93cced41b144bb10045cbd6cc2e5021a4cea50b1a72aa405fc1b`  
		Last Modified: Wed, 09 Sep 2020 22:48:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c054b5ce906c9bc36844a82271f2781122ef429003d967ab45644a8e017c7ffd`  
		Last Modified: Fri, 25 Sep 2020 22:41:36 GMT  
		Size: 8.5 MB (8499901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad294bd10348dabe38fe80d1b1ef8dada96b8303efa9273278211cb4179b247`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 1.3 MB (1310185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f47c002964b17e21d766eb617744089f4e0fb377160284fa630766110b24cc`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51e97e4c97ff4eeb5e1a677f345bcb87b5a7623b62e3bef3c4f2fad404cacae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114548833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f08dd245e147ed09ad35833ac5fdf7986cd34cb40918188ca26db058666a560`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:21:49 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:23:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:24:14 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:24:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:24:53 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:43:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:43:49 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:52:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:52:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:52:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:52:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:53:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e5c3bda96921f0fcdc52d34b4e8e57c154d9eeef090c6ca17e00ac1ca58d6`  
		Last Modified: Wed, 09 Sep 2020 22:41:21 GMT  
		Size: 101.3 MB (101250060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb6e866365ec04fdd345e22c049091abf460071fa0470866449b5c14cda08e`  
		Last Modified: Wed, 09 Sep 2020 22:39:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a4b970cfa1f0abf17873192eda639c3d1c128a0daef00315ea38bafa52bc6`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 8.9 MB (8920027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab74e879b267d02b2da382e2c5ca2e22fc5250997d748ba8f7451799fc5d20`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 1.3 MB (1287794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f96b78f4085cc0937cecfcd333f6263f52e5122d5c4b5977299137e870bfc91`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:32be187ea5fb2790ad34c7e181c5692239afc3a3ca882dc159cb34d9ef4f93cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118955263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c54429d0f3f6808444bf196fab77e6e595a1964b6218942f7112fe6c539b057`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:41:59 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:43:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:43:25 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:43:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:43:27 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:41:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:41:57 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:46 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:48 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eabcd3f00523ec5c8f8dca341969baa7b2786a73abc348fb5f39edf7a6410c6`  
		Last Modified: Wed, 09 Sep 2020 22:47:34 GMT  
		Size: 106.4 MB (106364195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36edeb811f26567d876bcc25c7d4c1c9ffb755523494a4c1670fb44b04a763aa`  
		Last Modified: Wed, 09 Sep 2020 22:47:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616042cacfc26da785f94395686f009bfa4b74481d41345619cf42a83dd7e2ab`  
		Last Modified: Fri, 25 Sep 2020 22:42:37 GMT  
		Size: 8.4 MB (8352247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e10f447b72ffcc29a59a55433dd9cf3d2776fff6431999836fa58087046837`  
		Last Modified: Wed, 14 Oct 2020 19:42:17 GMT  
		Size: 1.4 MB (1388769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd5ab0971f40a63405919c02456c3531709f1b7bce49c608bbaf95d646fc601`  
		Last Modified: Wed, 14 Oct 2020 19:42:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:3ba6b600176719bd63edb11bf0ae94e50f988e56cc4e85ba9925f32210861705
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2549189991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d7ef6ab31475a71e36630cb427f3f497c87dec6d112efbc196d70bd86f6817`
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
# Wed, 14 Oct 2020 12:29:03 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:31:28 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:31:30 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:02 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:03 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:09:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:09:31 GMT
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
	-	`sha256:e2d12d413526d5d1d8366bb7e48eb818bf637bacc48474c46cbfd3d4a90fe2b8`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e8fd6fb63c72075cd39946e1f58316f170c83d2690974bd5a81e9c0d8964c5`  
		Last Modified: Wed, 14 Oct 2020 12:50:53 GMT  
		Size: 138.7 MB (138681016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7197fbf266c1c46a72d143a070e8c9e78a5a4a3136a6deeafd6dd9bbf2fe22`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6c87eb231da1d3837c6a7f67c221889f56771cabd853b34e1b7f010139ee71`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069e825d6dd505d81c9a0a93bed795aa7b47f699ed863bd7f3125684664e889e`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5993393cf641947f6f9ab36ebaebffdb6c514ee74ff3373c93a32b83b873b0`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad9ee46931788edc71b3dc6bda2e279927b570cee5a8d0d240046ad9c5d916`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f4804228117bb75ce3d766338b80593b035625bce7d1581d1627f0a6ec683`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.8 MB (1780650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddec9e68813a9c5693c7934ee28aba70ecc97fc46e63b54aed1f39a5775cbe7`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:161ca87862741b3768b5ec1270ceae7d810ca89addff7ed55527e9ea648b2483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941391039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422cfe564b9278afa4fef1765baef01ab6cb4dcab62baae97dee103d14105039`
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
# Wed, 14 Oct 2020 12:35:14 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:38:37 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:38:39 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:38 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:39 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:11:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:11:02 GMT
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
	-	`sha256:43b092cb3237abc132910a3f21e44eeca2309630a905017be2f72a8ad938084d`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccea4c7c8503eedcb64c76b2b9e85bb36f157d91b8f5c218b125ab6c3ec8db7`  
		Last Modified: Wed, 14 Oct 2020 12:51:53 GMT  
		Size: 143.8 MB (143814531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e54f426c13bc41d2bd7bbe44e761440984b17ca53fd22a76a2cc981e0af5852`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690e1fece3f015a20ec4c6a92752e662dd8d92a6f0a3baa711bef8c28bd94f`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be175884faa3fdd2f45ce4a4991a52af6bc99fe2a2992175e59ecb3c668e0b9`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb30b173a9a26b142b7a1b43023f2de9aaec743b5aff188ed793c1d8223630ae`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f925f145dd6e8c98dfa60e7d788bcb25c992ac9c87b55fc784e459d655ca2a04`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9643de6696bb6f4080794fa706656eadc8cbb83eb45987150849096ac540fcc`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 11.3 MB (11322784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992e1b94c1e27f89b0accd8838c7033c7513a149dc64695b4f8e9881d417e123`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:7c9a89170824bdb5c2cb528051c61b69f71b1fc0c2a1e2eea0bf5aaa33156117
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
$ docker pull caddy@sha256:a390b4809acd419cf9c0a7954e324c4ecbf057ca2f84f8dc32a80dc11afd9481
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120085155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140237d3d47f0447dc9886f905524753902ebdd7b6f7b44d741eb7e62ba95a67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:40:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:20:06 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:22:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:22:16 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:22:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:22:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:22:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:27:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:27:45 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:19:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:19:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:19:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:19:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871e8e8d7a9e6e0e8b5c74575f14475ace81baa17901d798568eb6fc89c6605`  
		Last Modified: Wed, 09 Sep 2020 22:28:59 GMT  
		Size: 107.3 MB (107287077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73272ec9a57b94a2277ac06d457ca5382aa07be5c17cfddc44e9572e058f01e`  
		Last Modified: Wed, 09 Sep 2020 22:28:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc77d7d3d1a8614ee91da79da91cf0aad076637b63568e8f37506c7753ce627c`  
		Last Modified: Fri, 25 Sep 2020 22:28:18 GMT  
		Size: 8.3 MB (8310024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74225606380107b86f2b8090c232169ee13b9c4d24b2643943f277f2602491b8`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 1.4 MB (1407220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f01b76a627656998340b6f8731b2b02cdc1095b58cf6360229fc1f413941fd4`  
		Last Modified: Wed, 14 Oct 2020 19:20:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a9bf883ad8cba9ea2999d978904c95e6442b5e81a35d7bf0143389e958915b66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115230626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eea91094e5881890305c5794af85fc485156b8ca9c4888c73aadd577a5ae6f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:51:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:51:10 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:53:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:53:57 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:53:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:53:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:54:00 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:50:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:50:39 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:53:27 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:53:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:54:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:54:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:54:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33289ebfa0798f70595592ba1a31e18c039bf9047bbf13b9daf83c6bdf47fd9a`  
		Last Modified: Wed, 09 Sep 2020 23:01:48 GMT  
		Size: 103.1 MB (103087634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7835f9f7cff0ebd0351d7c28d6324d6466e20a35d1988db525477611b9909550`  
		Last Modified: Wed, 09 Sep 2020 23:01:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a9ed04456aff68ffe1e84bda9b04c2fa1c359fcd7cb23e64fd328a6d4fe6c`  
		Last Modified: Fri, 25 Sep 2020 22:51:32 GMT  
		Size: 7.9 MB (7928846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc97c54912b2e9a4a3b73bc7845661be88ddce3c7163a4106e656250b3d1046`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 1.3 MB (1327364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a643521102a74cdff40698863e8ab102bc00dcb3aaa0c3a7a2366b55e40be28`  
		Last Modified: Wed, 14 Oct 2020 19:55:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:22d7e5651fc23f90659d5bd8e0f6799aa6401e643739aec3cf02c835845989b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114011088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2278dfa7d9aaa63788ee41c26f3382f6476b6c0fce8cf1d241442beda56d59ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:46:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:01:53 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:04:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:04:13 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:04:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:04:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:04:17 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:59:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:59:04 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:03:23 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:03:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:04:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:04:23 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:04:30 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4617330c6e6b78b275a88d667be57a5b0fb668dab185289351c64522b8bbe65a`  
		Last Modified: Wed, 09 Sep 2020 22:12:18 GMT  
		Size: 102.9 MB (102850878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3139b43ff2f6d56f9dfa6751a3ea1972340b9102c86f45efdc310d66cd69d482`  
		Last Modified: Wed, 09 Sep 2020 22:11:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b18e3ae4626b5fa43914df0ea51e4de5da9432c60cc389a99d9d105c1a9747a`  
		Last Modified: Fri, 25 Sep 2020 23:00:00 GMT  
		Size: 7.1 MB (7144989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419d576ba1751faf2b9aa10f0788e64a79b1367282c7d1ead196ec976bba1c5b`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 1.3 MB (1325847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c9517d14e71111d4034c0256fa3dbde0775a541453da3102614df3d285e226`  
		Last Modified: Wed, 14 Oct 2020 20:05:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:1f76657589db6fa2be75268287cbbab811f3b3f6963c093bbd44635c0659de33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115368944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928d720f438087eba2c14fbaa18b341acc6054534ea8681a1c33371e93d03caf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:59:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:40:20 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:42:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:42:09 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:42:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:42:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:42:11 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:40:45 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:40:46 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:02 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8529a6b9a6be640bc502712219f1fb2745504a3f39ec97daaf85d4c8264af755`  
		Last Modified: Wed, 09 Sep 2020 22:49:05 GMT  
		Size: 102.6 MB (102567178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45590311c82a93cced41b144bb10045cbd6cc2e5021a4cea50b1a72aa405fc1b`  
		Last Modified: Wed, 09 Sep 2020 22:48:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c054b5ce906c9bc36844a82271f2781122ef429003d967ab45644a8e017c7ffd`  
		Last Modified: Fri, 25 Sep 2020 22:41:36 GMT  
		Size: 8.5 MB (8499901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad294bd10348dabe38fe80d1b1ef8dada96b8303efa9273278211cb4179b247`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 1.3 MB (1310185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f47c002964b17e21d766eb617744089f4e0fb377160284fa630766110b24cc`  
		Last Modified: Wed, 14 Oct 2020 19:41:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d51e97e4c97ff4eeb5e1a677f345bcb87b5a7623b62e3bef3c4f2fad404cacae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114548833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f08dd245e147ed09ad35833ac5fdf7986cd34cb40918188ca26db058666a560`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Sep 2020 01:38:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:21:49 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:23:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:24:14 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:24:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:24:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:24:53 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:43:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:43:49 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 20:52:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:52:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 20:52:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 20:52:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 20:53:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e5c3bda96921f0fcdc52d34b4e8e57c154d9eeef090c6ca17e00ac1ca58d6`  
		Last Modified: Wed, 09 Sep 2020 22:41:21 GMT  
		Size: 101.3 MB (101250060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb6e866365ec04fdd345e22c049091abf460071fa0470866449b5c14cda08e`  
		Last Modified: Wed, 09 Sep 2020 22:39:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a4b970cfa1f0abf17873192eda639c3d1c128a0daef00315ea38bafa52bc6`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 8.9 MB (8920027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab74e879b267d02b2da382e2c5ca2e22fc5250997d748ba8f7451799fc5d20`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 1.3 MB (1287794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f96b78f4085cc0937cecfcd333f6263f52e5122d5c4b5977299137e870bfc91`  
		Last Modified: Wed, 14 Oct 2020 20:53:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:32be187ea5fb2790ad34c7e181c5692239afc3a3ca882dc159cb34d9ef4f93cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118955263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c54429d0f3f6808444bf196fab77e6e595a1964b6218942f7112fe6c539b057`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 31 Aug 2020 23:53:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:41:59 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 09 Sep 2020 22:43:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.15.2.src.tar.gz'; 	sha256='28bf9d0bcde251011caae230a4a05d917b172ea203f2a62f2c2f9533589d4b4d'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 09 Sep 2020 22:43:25 GMT
ENV GOPATH=/go
# Wed, 09 Sep 2020 22:43:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Sep 2020 22:43:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 09 Sep 2020 22:43:27 GMT
WORKDIR /go
# Fri, 25 Sep 2020 22:41:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 25 Sep 2020 22:41:57 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 19:41:46 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 19:41:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3d71e90a4b4f3ebc55d79086d5fb4e36d675fd067435b0a2e37f50361e89ceb58a4b8eae43ea502d1b6d1522c3020f1791ffad9a9fbd374883c6202cf9ed67f7' ;; 		armhf)   binArch='armv6'; checksum='243f58f32bba0b6295267ba78ed18c1b36dfd3c8af4ddbe1f8e1fe096a58cb3326d795b19ce06d87b8641fc17d6e8f1fd2ee372af7dca8c844544768cd05c418' ;; 		armv7)   binArch='armv7'; checksum='51c212b44bf21e3d9feb841cb91c93289f5244d7276a7ce4b1eea73121855345190de77f4a87a3e4e1a93cccf6085133b8552de48687c2164277c0766d3404f0' ;; 		aarch64) binArch='arm64'; checksum='13c3184699c20734a5718cad3e4ee8fed52df1eca21d0d3fa5d34a671990bfd1fae23824c7618c0cba1ceac6262b3225f85cbb37cd9c162935c2c367c623e1ea' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='faf068bb6b6086881504699fb92f77f628e36297eda3651021fea40a06a2fa043453a729000d460e530b2772420071b65fdd3915abfdd4d47dbf820e3590393d' ;; 		s390x)   binArch='s390x'; checksum='79527340291d9e2196079c87daabe6fed5f5e354dc3a4a37e59c684aeed910376b472e4d8969c3ae957f1af35272d46e669fa111fcb47bb90a0822aa039970ea' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 14 Oct 2020 19:41:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 14 Oct 2020 19:41:48 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eabcd3f00523ec5c8f8dca341969baa7b2786a73abc348fb5f39edf7a6410c6`  
		Last Modified: Wed, 09 Sep 2020 22:47:34 GMT  
		Size: 106.4 MB (106364195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36edeb811f26567d876bcc25c7d4c1c9ffb755523494a4c1670fb44b04a763aa`  
		Last Modified: Wed, 09 Sep 2020 22:47:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616042cacfc26da785f94395686f009bfa4b74481d41345619cf42a83dd7e2ab`  
		Last Modified: Fri, 25 Sep 2020 22:42:37 GMT  
		Size: 8.4 MB (8352247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e10f447b72ffcc29a59a55433dd9cf3d2776fff6431999836fa58087046837`  
		Last Modified: Wed, 14 Oct 2020 19:42:17 GMT  
		Size: 1.4 MB (1388769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd5ab0971f40a63405919c02456c3531709f1b7bce49c608bbaf95d646fc601`  
		Last Modified: Wed, 14 Oct 2020 19:42:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:059405ea3383d42da538726c20d809f0f5f585e5bd4bf91da9670787bb2ba357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:3ba6b600176719bd63edb11bf0ae94e50f988e56cc4e85ba9925f32210861705
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2549189991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d7ef6ab31475a71e36630cb427f3f497c87dec6d112efbc196d70bd86f6817`
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
# Wed, 14 Oct 2020 12:29:03 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:31:28 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:31:30 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:02 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:03 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:09:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:09:31 GMT
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
	-	`sha256:e2d12d413526d5d1d8366bb7e48eb818bf637bacc48474c46cbfd3d4a90fe2b8`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e8fd6fb63c72075cd39946e1f58316f170c83d2690974bd5a81e9c0d8964c5`  
		Last Modified: Wed, 14 Oct 2020 12:50:53 GMT  
		Size: 138.7 MB (138681016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7197fbf266c1c46a72d143a070e8c9e78a5a4a3136a6deeafd6dd9bbf2fe22`  
		Last Modified: Wed, 14 Oct 2020 12:50:19 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6c87eb231da1d3837c6a7f67c221889f56771cabd853b34e1b7f010139ee71`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069e825d6dd505d81c9a0a93bed795aa7b47f699ed863bd7f3125684664e889e`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5993393cf641947f6f9ab36ebaebffdb6c514ee74ff3373c93a32b83b873b0`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad9ee46931788edc71b3dc6bda2e279927b570cee5a8d0d240046ad9c5d916`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5f4804228117bb75ce3d766338b80593b035625bce7d1581d1627f0a6ec683`  
		Last Modified: Wed, 14 Oct 2020 21:14:20 GMT  
		Size: 1.8 MB (1780650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddec9e68813a9c5693c7934ee28aba70ecc97fc46e63b54aed1f39a5775cbe7`  
		Last Modified: Wed, 14 Oct 2020 21:14:17 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:bcd37c91cc335877d442d174bc2bd1734af769f863e100be9ae72aea4c9dd730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `caddy:builder-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:161ca87862741b3768b5ec1270ceae7d810ca89addff7ed55527e9ea648b2483
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941391039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422cfe564b9278afa4fef1765baef01ab6cb4dcab62baae97dee103d14105039`
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
# Wed, 14 Oct 2020 12:35:14 GMT
ENV GOLANG_VERSION=1.15.2
# Wed, 14 Oct 2020 12:38:37 GMT
RUN $url = 'https://storage.googleapis.com/golang/go1.15.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e72782cc6de233188c75b06849368826eaa1b8bd9e1cd766db9466a12b7138ca'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 12:38:39 GMT
WORKDIR C:\gopath
# Wed, 14 Oct 2020 21:09:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:09:38 GMT
ENV XCADDY_VERSION=v0.1.5
# Wed, 14 Oct 2020 21:09:39 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:09:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Oct 2020 21:11:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.5/xcaddy_0.1.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('9372295e75cb10cff85c609a195b9ac12cea3e9fc3490234d4271d415cd210cfa78116b03d82f008b9519e4d1f6e03fc59c27db80e098798a3065e4e89edd653')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Oct 2020 21:11:02 GMT
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
	-	`sha256:43b092cb3237abc132910a3f21e44eeca2309630a905017be2f72a8ad938084d`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccea4c7c8503eedcb64c76b2b9e85bb36f157d91b8f5c218b125ab6c3ec8db7`  
		Last Modified: Wed, 14 Oct 2020 12:51:53 GMT  
		Size: 143.8 MB (143814531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e54f426c13bc41d2bd7bbe44e761440984b17ca53fd22a76a2cc981e0af5852`  
		Last Modified: Wed, 14 Oct 2020 12:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690e1fece3f015a20ec4c6a92752e662dd8d92a6f0a3baa711bef8c28bd94f`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be175884faa3fdd2f45ce4a4991a52af6bc99fe2a2992175e59ecb3c668e0b9`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb30b173a9a26b142b7a1b43023f2de9aaec743b5aff188ed793c1d8223630ae`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f925f145dd6e8c98dfa60e7d788bcb25c992ac9c87b55fc784e459d655ca2a04`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9643de6696bb6f4080794fa706656eadc8cbb83eb45987150849096ac540fcc`  
		Last Modified: Wed, 14 Oct 2020 21:14:38 GMT  
		Size: 11.3 MB (11322784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992e1b94c1e27f89b0accd8838c7033c7513a149dc64695b4f8e9881d417e123`  
		Last Modified: Wed, 14 Oct 2020 21:14:35 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:6d45511406faf9fe59e433a6b907a6cf136e7200435545dc0c47e04e6e4e27df
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
$ docker pull caddy@sha256:63fe670997595a40c2f8c81f38cf634a430587648769244325baf4a21be3010c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14635950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fd2a84cc279dbdc53de15daeae84bd726376c255582d12f3d2a3fa105150c9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:27:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:19:42 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:19:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:19:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:19:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:19:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:19:45 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:19:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:19:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:19:47 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:19:47 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:19:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed237faf7b90187b720d5e863fb021a1ca678304744dad14ff8ad6434e4e1da`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 300.0 KB (299981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5bea3a62f2eb8bdd91cf1d01de5e62aa88dbcd8e5834f5dd686a4f1a482531`  
		Last Modified: Fri, 25 Sep 2020 22:28:09 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69398e09bae2fd51db197ec44792b08ec525846a197c98f0b59c7b2f0f9d627`  
		Last Modified: Wed, 14 Oct 2020 19:20:12 GMT  
		Size: 11.5 MB (11532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ae648b058e6f63bcb417b92a4c41d61b2af30d50a970bd8d4b959e38bc7415`  
		Last Modified: Wed, 14 Oct 2020 19:20:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:7b5920e4a82b1bf465e06b3cf4893ee2e986063812e261bfa462dc7dda7a2d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13785708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d200bf3c822897c2bfe0d920d00e46b8125144c5947c88455acac1900bb34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:50:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:49:50 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:50:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:51:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:51:09 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:51:16 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:51:23 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:51:29 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:51:35 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:51:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:51:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:51:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:52:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:52:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:52:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:52:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:52:35 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:52:42 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:52:50 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:52:56 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:53:04 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a5a47b7ff29cc165cee9824ba874fa6cb56d737ce18f841fc3ed5e937cb75`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 300.1 KB (300144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdf9fef63ad932b076740c7fd4eac18d505c2e815b2b27093fae4a1037c1f83`  
		Last Modified: Fri, 25 Sep 2020 22:51:18 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481612b82405dab13f0ff7160cd02b31cafd7702962e9574045583eaed3fc7fe`  
		Last Modified: Wed, 14 Oct 2020 19:55:07 GMT  
		Size: 10.9 MB (10876291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c736385a37cc7654340f9f0217853549d57059a6fa720033afa8d97dea203`  
		Last Modified: Wed, 14 Oct 2020 19:54:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:8b43c89dba95e29c51ac668ab67a77e739e67a469eef340fc8d3a7061adeb4b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13566363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b01501010b8089fb9a9538277b4324106cc9891e2c01901d93699d43f832e96`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:58:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:57:52 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:58:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:59:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:59:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:59:51 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:00:01 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:00:10 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:00:22 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:00:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:00:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:01:06 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:01:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:01:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:01:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:01:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:02:02 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:02:17 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:02:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:02:41 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:02:52 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2aa34f01f2f9112772fdaebe7083b7dcdb4313768e0d6533a3e5b99597c98d`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 299.2 KB (299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f21378d6028fa7cda0d5b592cd8b633c405139cc47eee9863c2b21da4378b`  
		Last Modified: Fri, 25 Sep 2020 22:59:48 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c6573f114e083e57fdf28ed5339e567f2b1c3d13fda1b3b7d806e00f661128`  
		Last Modified: Wed, 14 Oct 2020 20:05:08 GMT  
		Size: 10.9 MB (10854375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660847f79f32b467c1ddaddb5a8306182d9f54c5fe1c2ee2aadd747cf78ed875`  
		Last Modified: Wed, 14 Oct 2020 20:05:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:085d496dad79fa71008de50e50f06591ab871b8f4711510a759b48a560bfe3aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13541809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e9fbe7d7a3cb53f7c6ee613e9c0ac1c82dbdfabb2a5e00cc6e577529e55b14`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:40:38 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:40:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:40:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:40:44 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:40:45 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:40:46 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:40:47 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:40:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:40:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:40:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:40:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:40:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:40:52 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:40:53 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:40:54 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:40:54 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:40:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f33282aee1a51127f669c7222e26bd0d5107b28d68819a6ead7f68076a73dc`  
		Last Modified: Mon, 15 Jun 2020 20:44:05 GMT  
		Size: 300.4 KB (300393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bbc79642b3dde186ddb45804729b84a8d010ca521d5c376311e2f613371675`  
		Last Modified: Fri, 25 Sep 2020 22:41:23 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f032bb954a154a6fcad58e71dc4fb90dabf12cf1ab3662992264236e3c2bd6e4`  
		Last Modified: Wed, 14 Oct 2020 19:41:31 GMT  
		Size: 10.5 MB (10527467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f62f208da9abbd187aaf41377a50af8149a6e8483fc0e04f5f5f507e4be7e`  
		Last Modified: Wed, 14 Oct 2020 19:41:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:a2f3a819439235784bf7fc8e3826e21acd4ed1825eaaf18e8d159e10e78c0f4d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13293783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12253d19d51ce81473f3f6884026957b92da390eaa7ede0fc8cb5d02f9281359`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:40:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 20:49:29 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 20:49:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 20:50:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 20:50:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 20:50:15 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 20:50:20 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 20:50:30 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 20:50:37 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 20:50:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 20:50:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 20:51:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 20:51:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 20:51:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 20:51:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 20:51:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 20:51:55 GMT
EXPOSE 80
# Wed, 14 Oct 2020 20:52:05 GMT
EXPOSE 443
# Wed, 14 Oct 2020 20:52:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 20:52:19 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 20:52:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b28df4c8a155654ad705e08f459bd177acc1005644ce2173ac62e954d6d4d2`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 302.4 KB (302369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899a5c1a337a29052e5f09180d092a86821dcf3d513b96fdf5db876ec3d6368`  
		Last Modified: Fri, 25 Sep 2020 22:45:34 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eb1518aae776833158c987ae4ac7c130ea2bfa680a61f757641ec0c57aab0c`  
		Last Modified: Wed, 14 Oct 2020 20:53:43 GMT  
		Size: 10.2 MB (10180227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18486e268d34e22c2aaac813d9e42b8401140f0fc8fd5a10b91ce37051de9b79`  
		Last Modified: Wed, 14 Oct 2020 20:53:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:9cb650ded68dd03f834621e7bea5b3411e6ac5b1162dbb759fef8acbf6404306
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14075256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54b98421e83dd9ca78953845196b424f44e37cdc25856a0fd9e7e0a38db7190`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 25 Sep 2020 22:41:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Oct 2020 19:41:31 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 19:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='66a21e0643fd2538ffe88ab93cb4a158b94873c1ce7494543a8355c8a3492d5fa43f4fa030dfc9e9833d15fe04f010063c61cb3f04ad5ac6bcff80396f928a08' ;; 		armhf)   binArch='armv6'; checksum='7e358d452fe7bbc0cdcba8a800339e34bd6277f698909d1d7a3b2ebd722653899b9bff6b7e8b996e9f054356374537f9971c1d5aed95f117dcce6be08e80446e' ;; 		armv7)   binArch='armv7'; checksum='ed847f91c9726ba4f25dbf9954ebe072c893f3eecfac3b83ee5c541fc762f88f59b4bd8aa35d54dd1ac043ca6e54235a197137529fe003792fdc3801a5100cd0' ;; 		aarch64) binArch='arm64'; checksum='dfc7ef12feea26b13b818cac8492664662c24835db1f8b862500debfddd30b7399d3ccc18a52fc8cc62b82ddb4cc41f2810580c1727b6c22e27dd74724bfae96' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3b38fcb4752be955e05156d2510825e93c7f83592a405d22f9ecd63cecd1d102b2aae4b50ce8586c035edd5d53075d4daeac986bc2cc1e2e1f41c6d9723066c5' ;; 		s390x)   binArch='s390x'; checksum='ebd76de742d38556aa6a7c68c000d530f46989f3db712b486d4dbe653ca69c3ba2333d19337e85d63c619f5c410f1d22dc982d9cdb6ce5e1ed94dbf29ec15190' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Oct 2020 19:41:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Oct 2020 19:41:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/config]
# Wed, 14 Oct 2020 19:41:38 GMT
VOLUME [/data]
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 19:41:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 19:41:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 19:41:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 80
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 443
# Wed, 14 Oct 2020 19:41:40 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 19:41:40 GMT
WORKDIR /srv
# Wed, 14 Oct 2020 19:41:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc47bdcaea173dfb029a09265c41846030477dc696b22fed52acad2b2078bb7`  
		Last Modified: Mon, 15 Jun 2020 20:44:21 GMT  
		Size: 300.5 KB (300524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b62d245db5345045e7a29f409c7a0109545e93366793659a9538d863745398`  
		Last Modified: Fri, 25 Sep 2020 22:42:24 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec4c67136f6b42bf7c9ffc1b3d6ae4f4f6f8ae1c3da947aaac8391f8c0437f`  
		Last Modified: Wed, 14 Oct 2020 19:42:08 GMT  
		Size: 11.2 MB (11202554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15a505e0b8040884a4e54d19382378931d39e70eb5fddc880f5771f796b06b8`  
		Last Modified: Wed, 14 Oct 2020 19:42:07 GMT  
		Size: 153.0 B  
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
