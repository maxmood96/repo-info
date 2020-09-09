<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2.1.1`](#caddy211)
-	[`caddy:2.1.1-alpine`](#caddy211-alpine)
-	[`caddy:2.1.1-builder`](#caddy211-builder)
-	[`caddy:2.1.1-windowsservercore`](#caddy211-windowsservercore)
-	[`caddy:2.1.1-windowsservercore-1809`](#caddy211-windowsservercore-1809)
-	[`caddy:2.1.1-windowsservercore-ltsc2016`](#caddy211-windowsservercore-ltsc2016)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2-windowsservercore-ltsc2016`](#caddy2-windowsservercore-ltsc2016)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)
-	[`caddy:windowsservercore-ltsc2016`](#caddywindowsservercore-ltsc2016)

## `caddy:2`

```console
$ docker pull caddy@sha256:d9e3041657102dfd878f2c70893cb324cca11f9e1d22ad82692d2c4bb83f41c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1457; amd64
	-	windows version 10.0.14393.3930; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:9ce811ab3540971fab00748e5d9a6bc7a91518fc9848367c907e32fda8d01411
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a12b5c957bab94f57aadfd9e655d414ab69443495f22ef430152181ab0aede`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:21:16 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:21:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:19:34 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:19:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:19:40 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:19:40 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:19:40 GMT
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
	-	`sha256:b1e49a2f7ba4b80caa31bb2874b39f9c4bbb447708f3a0e07ff43892744e63a4`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6f0d7c084024816c9d62c8cf79558a18c5df4cdcc951484a9e0ca63dd0b72`  
		Last Modified: Wed, 01 Jul 2020 00:20:17 GMT  
		Size: 13.1 MB (13057334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639b35073727cad03304869adcd7b9118cd8039707d055f5b37992f7188076d3`  
		Last Modified: Wed, 01 Jul 2020 00:20:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c8dd4b191727d7eccb50cdf3f3d26fe19abbd23be153dfd53a11f01059002928
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15324343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352f7aeefb2f9e7015bf833505ff90d75dc751bfa7d202255900787d9c1a6e1a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:52:07 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:52:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:49:25 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:49:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:49:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:49:33 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:49:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:49:34 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:49:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:49:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:49:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:49:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:49:42 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:49:43 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:49:43 GMT
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
	-	`sha256:3243ce9c25dc28a597c553cc7f0d4816c4b75789e4ebc37225ac58d5bd078995`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed8e0a01609838fd9b844360403b0c62d26ca345d311c0e12ce9b3b7598f38`  
		Last Modified: Tue, 30 Jun 2020 23:51:10 GMT  
		Size: 12.4 MB (12414918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697e38da42d8f15b4dd54f63870d7e806d1eb7fc0fa15968afda08c82ebb567d`  
		Last Modified: Tue, 30 Jun 2020 23:51:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:251cd735b768dece1a258fe61d2f5f17489920c820d5ed42c431bf03df06c62b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b113527fd3cc583349e001c913567cb5ae6f17df91d84b587c597a69e63574`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:00:00 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:00:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:57:45 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:57:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:57:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:57:57 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:57:58 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:57:58 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:57:59 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:58:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:58:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:58:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:58:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:58:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:58:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:58:09 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:58:10 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:58:11 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:58:12 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:58:13 GMT
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
	-	`sha256:78b107a7bf1560d80dcded532795715f77765cf1a3d9464665d42acab82d366e`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650c88e8e905db99ee64cc19f474dc3c7a32c737e05c403dcda6d96cbee69c4`  
		Last Modified: Tue, 30 Jun 2020 23:59:49 GMT  
		Size: 12.4 MB (12396011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8987db1ddf93e7c11e4c142ecfc8724b54131c3a5bf498a315d3c3dc6846990`  
		Last Modified: Tue, 30 Jun 2020 23:59:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:788931ce2b8e71b550976686f4085c0d4916bdbcc762f9db67d6f0036a109897
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15027460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b8f97e703682d7f83ea2a0146297c030599f59b72b006da9f851c8594777f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:42:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:42:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:39:44 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:39:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:39:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:39:50 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:39:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:39:51 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:39:52 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:39:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:39:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:39:59 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:40:00 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:40:00 GMT
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
	-	`sha256:2b85f4621f67650b74dc2db70b30f9593bc6695d3e91ff3899b3ee7c34cffc04`  
		Last Modified: Mon, 15 Jun 2020 20:44:04 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb12521bcb6d56dcfc220f0b20353a7aa329d702f5feb52f41bcf589de54695`  
		Last Modified: Tue, 30 Jun 2020 23:41:07 GMT  
		Size: 12.0 MB (12013102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599000c030713113e35f054497b6ea20d7cfe46540c547c904d1cb29e5ab5e09`  
		Last Modified: Tue, 30 Jun 2020 23:41:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:eda12afcf0918e61a08bdd958c9c41e599ef640367a8a50b21c7208d3864b9ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14899035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fd2d02dd7c74b824afe02694093d9ad27a7fe4da1f70dc8f499d714c0de004`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:19:13 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:19:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:52:33 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:52:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:53:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:53:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:53:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:53:18 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:53:24 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:53:30 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:53:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:53:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:53:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:54:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:54:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:54:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:54:20 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:54:29 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:54:38 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:54:41 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:54:46 GMT
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
	-	`sha256:3b2288431c86a795754eb4d3a678e778c534a14e9243aea01a7cf9feff8d8e4e`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370c1e51003a37803d04248bb3fbf1f56ca3809ab021a4e661b6d39fb8ef21f`  
		Last Modified: Wed, 01 Jul 2020 01:01:31 GMT  
		Size: 11.8 MB (11785466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acf474ff4d447e0ee036263e810f271f045341957b949e742c4299ff7e8199a`  
		Last Modified: Wed, 01 Jul 2020 01:01:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:c15a47ccc69b6ea56daff5a268d5e93e40faf8ca0124f19c065e301e8ad4bedd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e80a8389cb6f5ffcd0f2092c3c3898d44aa2d3035a3c7482e315a32626622d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:43:15 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:43:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:41:28 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:41:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:41:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:41:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:41:34 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:41:38 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:41:39 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:41:39 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:41:40 GMT
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
	-	`sha256:bf084f3ceb3b3b1196400fa251cc45e01de7ece41b7605bb40ae5178d849b47d`  
		Last Modified: Mon, 15 Jun 2020 20:44:26 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a74ac154ef35abae9974398394ecc94fe54ad18af49231bc6a337fc43346c5`  
		Last Modified: Tue, 30 Jun 2020 23:42:46 GMT  
		Size: 12.8 MB (12836780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5673e745c5f3d1ac989f1a9cc90e301eb65e6dec0d3875d0480300738a959f32`  
		Last Modified: Tue, 30 Jun 2020 23:42:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1`

```console
$ docker pull caddy@sha256:d9e3041657102dfd878f2c70893cb324cca11f9e1d22ad82692d2c4bb83f41c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1457; amd64
	-	windows version 10.0.14393.3930; amd64

### `caddy:2.1.1` - linux; amd64

```console
$ docker pull caddy@sha256:9ce811ab3540971fab00748e5d9a6bc7a91518fc9848367c907e32fda8d01411
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a12b5c957bab94f57aadfd9e655d414ab69443495f22ef430152181ab0aede`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:21:16 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:21:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:19:34 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:19:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:19:40 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:19:40 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:19:40 GMT
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
	-	`sha256:b1e49a2f7ba4b80caa31bb2874b39f9c4bbb447708f3a0e07ff43892744e63a4`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6f0d7c084024816c9d62c8cf79558a18c5df4cdcc951484a9e0ca63dd0b72`  
		Last Modified: Wed, 01 Jul 2020 00:20:17 GMT  
		Size: 13.1 MB (13057334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639b35073727cad03304869adcd7b9118cd8039707d055f5b37992f7188076d3`  
		Last Modified: Wed, 01 Jul 2020 00:20:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c8dd4b191727d7eccb50cdf3f3d26fe19abbd23be153dfd53a11f01059002928
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15324343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352f7aeefb2f9e7015bf833505ff90d75dc751bfa7d202255900787d9c1a6e1a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:52:07 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:52:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:49:25 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:49:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:49:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:49:33 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:49:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:49:34 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:49:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:49:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:49:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:49:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:49:42 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:49:43 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:49:43 GMT
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
	-	`sha256:3243ce9c25dc28a597c553cc7f0d4816c4b75789e4ebc37225ac58d5bd078995`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed8e0a01609838fd9b844360403b0c62d26ca345d311c0e12ce9b3b7598f38`  
		Last Modified: Tue, 30 Jun 2020 23:51:10 GMT  
		Size: 12.4 MB (12414918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697e38da42d8f15b4dd54f63870d7e806d1eb7fc0fa15968afda08c82ebb567d`  
		Last Modified: Tue, 30 Jun 2020 23:51:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; arm variant v7

```console
$ docker pull caddy@sha256:251cd735b768dece1a258fe61d2f5f17489920c820d5ed42c431bf03df06c62b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b113527fd3cc583349e001c913567cb5ae6f17df91d84b587c597a69e63574`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:00:00 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:00:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:57:45 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:57:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:57:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:57:57 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:57:58 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:57:58 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:57:59 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:58:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:58:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:58:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:58:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:58:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:58:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:58:09 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:58:10 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:58:11 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:58:12 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:58:13 GMT
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
	-	`sha256:78b107a7bf1560d80dcded532795715f77765cf1a3d9464665d42acab82d366e`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650c88e8e905db99ee64cc19f474dc3c7a32c737e05c403dcda6d96cbee69c4`  
		Last Modified: Tue, 30 Jun 2020 23:59:49 GMT  
		Size: 12.4 MB (12396011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8987db1ddf93e7c11e4c142ecfc8724b54131c3a5bf498a315d3c3dc6846990`  
		Last Modified: Tue, 30 Jun 2020 23:59:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:788931ce2b8e71b550976686f4085c0d4916bdbcc762f9db67d6f0036a109897
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15027460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b8f97e703682d7f83ea2a0146297c030599f59b72b006da9f851c8594777f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:42:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:42:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:39:44 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:39:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:39:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:39:50 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:39:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:39:51 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:39:52 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:39:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:39:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:39:59 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:40:00 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:40:00 GMT
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
	-	`sha256:2b85f4621f67650b74dc2db70b30f9593bc6695d3e91ff3899b3ee7c34cffc04`  
		Last Modified: Mon, 15 Jun 2020 20:44:04 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb12521bcb6d56dcfc220f0b20353a7aa329d702f5feb52f41bcf589de54695`  
		Last Modified: Tue, 30 Jun 2020 23:41:07 GMT  
		Size: 12.0 MB (12013102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599000c030713113e35f054497b6ea20d7cfe46540c547c904d1cb29e5ab5e09`  
		Last Modified: Tue, 30 Jun 2020 23:41:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; ppc64le

```console
$ docker pull caddy@sha256:eda12afcf0918e61a08bdd958c9c41e599ef640367a8a50b21c7208d3864b9ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14899035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fd2d02dd7c74b824afe02694093d9ad27a7fe4da1f70dc8f499d714c0de004`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:19:13 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:19:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:52:33 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:52:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:53:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:53:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:53:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:53:18 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:53:24 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:53:30 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:53:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:53:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:53:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:54:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:54:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:54:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:54:20 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:54:29 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:54:38 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:54:41 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:54:46 GMT
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
	-	`sha256:3b2288431c86a795754eb4d3a678e778c534a14e9243aea01a7cf9feff8d8e4e`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370c1e51003a37803d04248bb3fbf1f56ca3809ab021a4e661b6d39fb8ef21f`  
		Last Modified: Wed, 01 Jul 2020 01:01:31 GMT  
		Size: 11.8 MB (11785466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acf474ff4d447e0ee036263e810f271f045341957b949e742c4299ff7e8199a`  
		Last Modified: Wed, 01 Jul 2020 01:01:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - linux; s390x

```console
$ docker pull caddy@sha256:c15a47ccc69b6ea56daff5a268d5e93e40faf8ca0124f19c065e301e8ad4bedd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e80a8389cb6f5ffcd0f2092c3c3898d44aa2d3035a3c7482e315a32626622d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:43:15 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:43:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:41:28 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:41:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:41:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:41:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:41:34 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:41:38 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:41:39 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:41:39 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:41:40 GMT
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
	-	`sha256:bf084f3ceb3b3b1196400fa251cc45e01de7ece41b7605bb40ae5178d849b47d`  
		Last Modified: Mon, 15 Jun 2020 20:44:26 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a74ac154ef35abae9974398394ecc94fe54ad18af49231bc6a337fc43346c5`  
		Last Modified: Tue, 30 Jun 2020 23:42:46 GMT  
		Size: 12.8 MB (12836780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5673e745c5f3d1ac989f1a9cc90e301eb65e6dec0d3875d0480300738a959f32`  
		Last Modified: Tue, 30 Jun 2020 23:42:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-alpine`

```console
$ docker pull caddy@sha256:707e960e783141b786754199242c2aa10046712e7b2697aa3bc030492c50de2a
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
$ docker pull caddy@sha256:9ce811ab3540971fab00748e5d9a6bc7a91518fc9848367c907e32fda8d01411
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a12b5c957bab94f57aadfd9e655d414ab69443495f22ef430152181ab0aede`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:21:16 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:21:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:19:34 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:19:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:19:40 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:19:40 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:19:40 GMT
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
	-	`sha256:b1e49a2f7ba4b80caa31bb2874b39f9c4bbb447708f3a0e07ff43892744e63a4`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6f0d7c084024816c9d62c8cf79558a18c5df4cdcc951484a9e0ca63dd0b72`  
		Last Modified: Wed, 01 Jul 2020 00:20:17 GMT  
		Size: 13.1 MB (13057334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639b35073727cad03304869adcd7b9118cd8039707d055f5b37992f7188076d3`  
		Last Modified: Wed, 01 Jul 2020 00:20:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c8dd4b191727d7eccb50cdf3f3d26fe19abbd23be153dfd53a11f01059002928
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15324343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352f7aeefb2f9e7015bf833505ff90d75dc751bfa7d202255900787d9c1a6e1a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:52:07 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:52:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:49:25 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:49:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:49:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:49:33 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:49:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:49:34 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:49:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:49:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:49:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:49:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:49:42 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:49:43 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:49:43 GMT
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
	-	`sha256:3243ce9c25dc28a597c553cc7f0d4816c4b75789e4ebc37225ac58d5bd078995`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed8e0a01609838fd9b844360403b0c62d26ca345d311c0e12ce9b3b7598f38`  
		Last Modified: Tue, 30 Jun 2020 23:51:10 GMT  
		Size: 12.4 MB (12414918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697e38da42d8f15b4dd54f63870d7e806d1eb7fc0fa15968afda08c82ebb567d`  
		Last Modified: Tue, 30 Jun 2020 23:51:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:251cd735b768dece1a258fe61d2f5f17489920c820d5ed42c431bf03df06c62b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b113527fd3cc583349e001c913567cb5ae6f17df91d84b587c597a69e63574`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:00:00 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:00:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:57:45 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:57:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:57:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:57:57 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:57:58 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:57:58 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:57:59 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:58:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:58:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:58:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:58:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:58:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:58:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:58:09 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:58:10 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:58:11 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:58:12 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:58:13 GMT
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
	-	`sha256:78b107a7bf1560d80dcded532795715f77765cf1a3d9464665d42acab82d366e`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650c88e8e905db99ee64cc19f474dc3c7a32c737e05c403dcda6d96cbee69c4`  
		Last Modified: Tue, 30 Jun 2020 23:59:49 GMT  
		Size: 12.4 MB (12396011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8987db1ddf93e7c11e4c142ecfc8724b54131c3a5bf498a315d3c3dc6846990`  
		Last Modified: Tue, 30 Jun 2020 23:59:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:788931ce2b8e71b550976686f4085c0d4916bdbcc762f9db67d6f0036a109897
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15027460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b8f97e703682d7f83ea2a0146297c030599f59b72b006da9f851c8594777f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:42:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:42:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:39:44 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:39:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:39:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:39:50 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:39:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:39:51 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:39:52 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:39:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:39:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:39:59 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:40:00 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:40:00 GMT
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
	-	`sha256:2b85f4621f67650b74dc2db70b30f9593bc6695d3e91ff3899b3ee7c34cffc04`  
		Last Modified: Mon, 15 Jun 2020 20:44:04 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb12521bcb6d56dcfc220f0b20353a7aa329d702f5feb52f41bcf589de54695`  
		Last Modified: Tue, 30 Jun 2020 23:41:07 GMT  
		Size: 12.0 MB (12013102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599000c030713113e35f054497b6ea20d7cfe46540c547c904d1cb29e5ab5e09`  
		Last Modified: Tue, 30 Jun 2020 23:41:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:eda12afcf0918e61a08bdd958c9c41e599ef640367a8a50b21c7208d3864b9ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14899035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fd2d02dd7c74b824afe02694093d9ad27a7fe4da1f70dc8f499d714c0de004`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:19:13 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:19:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:52:33 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:52:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:53:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:53:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:53:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:53:18 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:53:24 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:53:30 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:53:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:53:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:53:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:54:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:54:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:54:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:54:20 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:54:29 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:54:38 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:54:41 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:54:46 GMT
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
	-	`sha256:3b2288431c86a795754eb4d3a678e778c534a14e9243aea01a7cf9feff8d8e4e`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370c1e51003a37803d04248bb3fbf1f56ca3809ab021a4e661b6d39fb8ef21f`  
		Last Modified: Wed, 01 Jul 2020 01:01:31 GMT  
		Size: 11.8 MB (11785466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acf474ff4d447e0ee036263e810f271f045341957b949e742c4299ff7e8199a`  
		Last Modified: Wed, 01 Jul 2020 01:01:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:c15a47ccc69b6ea56daff5a268d5e93e40faf8ca0124f19c065e301e8ad4bedd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e80a8389cb6f5ffcd0f2092c3c3898d44aa2d3035a3c7482e315a32626622d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:43:15 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:43:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:41:28 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:41:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:41:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:41:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:41:34 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:41:38 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:41:39 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:41:39 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:41:40 GMT
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
	-	`sha256:bf084f3ceb3b3b1196400fa251cc45e01de7ece41b7605bb40ae5178d849b47d`  
		Last Modified: Mon, 15 Jun 2020 20:44:26 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a74ac154ef35abae9974398394ecc94fe54ad18af49231bc6a337fc43346c5`  
		Last Modified: Tue, 30 Jun 2020 23:42:46 GMT  
		Size: 12.8 MB (12836780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5673e745c5f3d1ac989f1a9cc90e301eb65e6dec0d3875d0480300738a959f32`  
		Last Modified: Tue, 30 Jun 2020 23:42:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-builder`

```console
$ docker pull caddy@sha256:643c97d5875621ee1a224c300d130344b4518bb33c1f13ecd48fcce97f2c7bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.1.1-builder` - linux; amd64

```console
$ docker pull caddy@sha256:530d664fc93dca48b1c5aac4041ab8f94db2300c7e301b721578d3aadc9f60d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305982305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f89e49117b8f842b47277b8ce37f02851dfeb18da89c241f25afe1322ccc517`
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
# Tue, 01 Sep 2020 19:34:35 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 19:36:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 19:36:50 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 19:36:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:36:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 19:36:51 GMT
WORKDIR /go
# Tue, 01 Sep 2020 19:46:18 GMT
WORKDIR /src
# Tue, 01 Sep 2020 19:46:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 19:46:19 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 19:46:21 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 19:46:21 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 19:46:40 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 19:46:43 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 19:46:43 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:cd28c722f6f6bff33648d1a69362ea09192e6c5b41c0604848f7ea8490ff4db9`  
		Last Modified: Tue, 01 Sep 2020 19:43:02 GMT  
		Size: 107.3 MB (107338308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f4f084ab04cf5f263eaadf7ae8add978a542c095db636287348ff0011b060a`  
		Last Modified: Tue, 01 Sep 2020 19:42:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ebda6c2bf751925c9d28dd3ddf434711b59757ff414e94bc7e95b084490fb3`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22004df01bcc06db36622c0faa009585dbdf7419984692ef289bfb30e2df7001`  
		Last Modified: Tue, 01 Sep 2020 19:46:55 GMT  
		Size: 8.3 MB (8310031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95063ecc956a4900df7dbd46015c622c95845c3c82efc7994e13fc83ba0d4d8`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 3.0 MB (3021529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a5064d0396a56f11b584ef9473239e91b053dc33705d4cb75dc90a4e5db2a7`  
		Last Modified: Tue, 01 Sep 2020 19:47:22 GMT  
		Size: 184.2 MB (184231261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac18da66ebccce66529a8a5c82b6f2f5d98e0284937b2c8b43c204fdd1f09fa5`  
		Last Modified: Tue, 01 Sep 2020 19:46:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a6bc59dd3c10a42c3519d7aa483f03e42c0db5ac5e8ccf1c0862cc6e365be1`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bca9f97ade95febc09408fa2d10d24ed25d27a294539631f0fd202b3c6312fa5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301744909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d3e3528b20c6a94ded6b5d109520ae79c86955a4e4fdbcdf4f14150846aaab`
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
# Tue, 01 Sep 2020 21:02:35 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 22:13:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 22:13:41 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 22:14:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 22:15:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 22:15:43 GMT
WORKDIR /go
# Tue, 01 Sep 2020 23:54:52 GMT
WORKDIR /src
# Tue, 01 Sep 2020 23:55:50 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 23:56:08 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 23:57:23 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 23:57:36 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 00:01:34 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 00:02:17 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 00:02:51 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:0c1a3d691278cfe4625eb35113eb4e76dba7b7b922cd23213e3615a7449b7f72`  
		Last Modified: Tue, 01 Sep 2020 23:26:58 GMT  
		Size: 103.7 MB (103667911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755f9ee371ff232fae8ecd0068039d8720f3f3f95fb9d102e7e6a58cb58f9e6e`  
		Last Modified: Tue, 01 Sep 2020 23:26:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e887d24fbc2350fecff867f6127f917fc6eb4b7df003b1774e91e9a1f2f27`  
		Last Modified: Wed, 02 Sep 2020 00:03:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807a9c07aa5d372f3fe371b3a8f5c0bc7faa3349934a30ef9346a6366dba2703`  
		Last Modified: Wed, 02 Sep 2020 00:03:22 GMT  
		Size: 7.9 MB (7928883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61096b4836c4bc4dd217b18de0eb5d8ac019a7f8429b138e3cc4edf31b2dbe82`  
		Last Modified: Wed, 02 Sep 2020 00:03:20 GMT  
		Size: 3.0 MB (3019410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6b78006ffc6587da18d44f165ef51866b235717d237176121b70a1a403d6d`  
		Last Modified: Wed, 02 Sep 2020 00:05:09 GMT  
		Size: 184.2 MB (184241509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9077b5629d7e79f07d846547d35e15467f6dad0686e7777cf8132e9a74f5de`  
		Last Modified: Wed, 02 Sep 2020 00:03:20 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5099129bea582dbd70a6c6f2fd933a6ef6dbeec6b23726ed103095e5a2084b7a`  
		Last Modified: Wed, 02 Sep 2020 00:03:20 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fcb33ea694c7bdb3bc88c21632942684155bc3ff746b11b20fe9440863bd7e59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300522401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36afb392704f9e4127f3f545047cd24888d97078d4728f12ac0de131bb49a9dd`
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
# Tue, 01 Sep 2020 23:03:51 GMT
ENV GOLANG_VERSION=1.14.8
# Wed, 02 Sep 2020 00:10:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 02 Sep 2020 00:11:00 GMT
ENV GOPATH=/go
# Wed, 02 Sep 2020 00:11:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Sep 2020 00:11:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Sep 2020 00:11:35 GMT
WORKDIR /go
# Wed, 02 Sep 2020 01:30:15 GMT
WORKDIR /src
# Wed, 02 Sep 2020 01:30:41 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 02 Sep 2020 01:30:46 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 02 Sep 2020 01:31:15 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 02 Sep 2020 01:31:19 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 01:32:56 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 01:33:10 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 01:33:15 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:ccafdd70e65ad98952807d42e06e048856f0c083e2978115ab4a4dde9205d7e2`  
		Last Modified: Wed, 02 Sep 2020 01:19:29 GMT  
		Size: 103.4 MB (103425137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd1514ccf0f746c697082d73324febe490c127c7642ef083de4a32136a3939c`  
		Last Modified: Wed, 02 Sep 2020 01:18:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b850ac09b7e0dbccd54397052f9635f84d8dbc906924ff659eb36d9da92c64`  
		Last Modified: Wed, 02 Sep 2020 01:33:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c305eb69f70ad04ca7bebd869369774a052be87a39f2adbb35ff36410f961c`  
		Last Modified: Wed, 02 Sep 2020 01:33:37 GMT  
		Size: 7.1 MB (7144945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6498251e87f04f5193188d7d81f39ebaabc92a062e12672df80a944f982ec01`  
		Last Modified: Wed, 02 Sep 2020 01:33:36 GMT  
		Size: 3.0 MB (3023124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c1863b298bdd871d6d5b3054be0513d1b919f4a2b8d9594269e69955187bf6`  
		Last Modified: Wed, 02 Sep 2020 01:34:20 GMT  
		Size: 184.2 MB (184239410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7820692de33884f3f143ce04108330d918263155dcb094f632d49353cc6fc`  
		Last Modified: Wed, 02 Sep 2020 01:33:36 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac75b79cbff116bca566952a6915a413878540ac764f28cb5618e7f6c5b26ec`  
		Last Modified: Wed, 02 Sep 2020 01:33:36 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:0f38e26a40310a168078cb7b86a52c600d873c7e9838fa8c3f957a460ff3896f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301521324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fc152bf238535be273ff83aa09cd84c9167f3a401056db6c22b07d01a5b639`
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
# Tue, 01 Sep 2020 22:21:53 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 22:28:02 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 22:28:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 22:29:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 22:29:59 GMT
WORKDIR /go
# Tue, 01 Sep 2020 23:59:26 GMT
WORKDIR /src
# Wed, 02 Sep 2020 00:00:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 02 Sep 2020 00:00:11 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 02 Sep 2020 00:03:01 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 02 Sep 2020 00:03:20 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 00:04:32 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 00:04:43 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 00:04:51 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:1b753c98a16c78448f78b84920abfa41d762cccff115f2470d293b55284eb67c`  
		Last Modified: Tue, 01 Sep 2020 22:44:39 GMT  
		Size: 102.8 MB (102770337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb840484a8cf8606be10acc343938d8a0873d5fe46ba82c9c597a739dd217d5`  
		Last Modified: Tue, 01 Sep 2020 22:44:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76417713493a8725e79524a31ac62fc8eaffbd316ea9d552681fca013fbd3099`  
		Last Modified: Wed, 02 Sep 2020 00:05:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4c31c540f49a3194ad36892aa103ddb83fe9e790797f2340655c6c7ac9817e`  
		Last Modified: Wed, 02 Sep 2020 00:05:17 GMT  
		Size: 8.5 MB (8499919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416a2e78480040fa946d4af0e14276575ef691ecbca5f87da67f93ed765b4d05`  
		Last Modified: Wed, 02 Sep 2020 00:05:17 GMT  
		Size: 3.0 MB (3019449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cff76c2ff5d488b52a3d38fbab7ef2c7371716875f832cf38c35de021880f7`  
		Last Modified: Wed, 02 Sep 2020 00:06:00 GMT  
		Size: 184.2 MB (184239526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51743cf71732c8b66796ae05cdaf4975f42f862c185978ca78b094296fe2a174`  
		Last Modified: Wed, 02 Sep 2020 00:05:16 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb9a8de871f4c123dc35f3d167810586180f0c9d13cad2bb6e1ad7dc7c70150`  
		Last Modified: Wed, 02 Sep 2020 00:05:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:a4c9e614785e73f9980f8b2f1280e60cb78c8bc69fb96fbfcd4738b286a1961f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300863289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f5c3531bfaff72603882514e919fdc422f04d5961b2e740266d170cdd783e`
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
# Wed, 02 Sep 2020 02:56:21 GMT
ENV GOLANG_VERSION=1.14.8
# Wed, 02 Sep 2020 02:58:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 02 Sep 2020 02:58:41 GMT
ENV GOPATH=/go
# Wed, 02 Sep 2020 02:58:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Sep 2020 02:59:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Sep 2020 02:59:04 GMT
WORKDIR /go
# Wed, 02 Sep 2020 03:30:04 GMT
WORKDIR /src
# Wed, 02 Sep 2020 03:30:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 02 Sep 2020 03:30:19 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 02 Sep 2020 03:30:30 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 02 Sep 2020 03:30:34 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 03:34:51 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 03:34:58 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 03:35:05 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:a7be439f828eeb9dade6b3c4d250fea147c4bf9ea749ad1171b1e0f15cb0e7a0`  
		Last Modified: Wed, 02 Sep 2020 03:05:12 GMT  
		Size: 101.6 MB (101587261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858283ff3c5a8a5672a547616e2bccfb9e9d3c47a62794acce6eb9ff926473f8`  
		Last Modified: Wed, 02 Sep 2020 03:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448945833acd7eec62ff140509665b36ac2a3e4d255d90ac6de59f53a8eded9a`  
		Last Modified: Wed, 02 Sep 2020 03:35:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445cb5b17ad69c6db778ba638564478d36f35150d080ce2b32ab27d4eac1039`  
		Last Modified: Wed, 02 Sep 2020 03:35:43 GMT  
		Size: 8.9 MB (8920026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c779dfbf194735d2c7c60a94b07405e8ef77e68f99deb7dbf2ff1f069c8e27ca`  
		Last Modified: Wed, 02 Sep 2020 03:35:42 GMT  
		Size: 3.0 MB (3019813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b327557c04a11b827536c6b5b4e8345e8887e26d43d1096bcb885085bc65157`  
		Last Modified: Wed, 02 Sep 2020 03:36:12 GMT  
		Size: 184.2 MB (184244825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2cc122dd885bcc30ad0d0637a1d28208beec16664ebc9a17775e61a29ee2`  
		Last Modified: Wed, 02 Sep 2020 03:35:40 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21bd9e29bbf2dc2b7e9708b23cf901f3bf4c2ce214fd048f0264959e759397e`  
		Last Modified: Wed, 02 Sep 2020 03:35:41 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:7e4c3f3223de987021dc6c2e2dd0171c828b7aa9bb6293181b8cb697e6dab9fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305648613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dac070d5c68f4c2e6cfcc91d843df4050389c9cebe743104c796ea839cdda3`
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
# Tue, 01 Sep 2020 19:44:01 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 19:45:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 19:45:35 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 19:45:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:45:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 19:45:37 GMT
WORKDIR /go
# Tue, 01 Sep 2020 20:04:54 GMT
WORKDIR /src
# Tue, 01 Sep 2020 20:04:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 20:04:56 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 20:04:57 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 20:04:58 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 20:05:14 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 20:05:22 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 20:05:23 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:30e232aad579fb98c2f2045f3f7b7ba0fbffcfc8e29b42d0ba5a359837b0c4e1`  
		Last Modified: Tue, 01 Sep 2020 19:49:06 GMT  
		Size: 107.2 MB (107195429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2165b261634b409611a87b9a553177bf635c26b3a0516de364edac85a8d27b27`  
		Last Modified: Tue, 01 Sep 2020 19:48:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1062f7882f263f26082444069fc6189191916dc260cbfc4dbe282b15d49a3fbd`  
		Last Modified: Tue, 01 Sep 2020 20:05:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c18eaf417133e1baa67c0e5e908a0d1cc12dbac23d7d930307c5b9973f3b91`  
		Last Modified: Tue, 01 Sep 2020 20:05:38 GMT  
		Size: 8.4 MB (8352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e16c5f4c29abf40f9273613ac29277c5ee3401f1e69d6e11393d1c5cde4440e`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 3.0 MB (3019353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae13017144598018fbf639fd94a2cff812baec7a4a31e5eec23d4b12738fa3cd`  
		Last Modified: Tue, 01 Sep 2020 20:05:53 GMT  
		Size: 184.2 MB (184231123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e262f312527240c7ac156ee2650905668e128bd06e381594ab2f18f66d6000e2`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb074fabd331ca17a2cb9e7f77792f2e79671375f012ecee518944363de5157`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-windowsservercore`

```console
$ docker pull caddy@sha256:40c4f77513048ee7e05ee01fb89d360e22b13325c3daaffca57dee62c72b575d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64
	-	windows version 10.0.14393.3930; amd64

### `caddy:2.1.1-windowsservercore` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-windowsservercore` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-windowsservercore-1809`

```console
$ docker pull caddy@sha256:54fc1c11a9a4de45c0e3b30aa2702ac0e55d355cd47e3f7f4fbfdc475bc6c132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `caddy:2.1.1-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:deb60a2701067b98424a7cc203f79a61a9f41d6b772df3b6c0ba34236cce1c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3930; amd64

### `caddy:2.1.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:707e960e783141b786754199242c2aa10046712e7b2697aa3bc030492c50de2a
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
$ docker pull caddy@sha256:9ce811ab3540971fab00748e5d9a6bc7a91518fc9848367c907e32fda8d01411
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a12b5c957bab94f57aadfd9e655d414ab69443495f22ef430152181ab0aede`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:21:16 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:21:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:19:34 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:19:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:19:40 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:19:40 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:19:40 GMT
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
	-	`sha256:b1e49a2f7ba4b80caa31bb2874b39f9c4bbb447708f3a0e07ff43892744e63a4`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6f0d7c084024816c9d62c8cf79558a18c5df4cdcc951484a9e0ca63dd0b72`  
		Last Modified: Wed, 01 Jul 2020 00:20:17 GMT  
		Size: 13.1 MB (13057334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639b35073727cad03304869adcd7b9118cd8039707d055f5b37992f7188076d3`  
		Last Modified: Wed, 01 Jul 2020 00:20:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c8dd4b191727d7eccb50cdf3f3d26fe19abbd23be153dfd53a11f01059002928
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15324343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352f7aeefb2f9e7015bf833505ff90d75dc751bfa7d202255900787d9c1a6e1a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:52:07 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:52:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:49:25 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:49:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:49:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:49:33 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:49:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:49:34 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:49:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:49:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:49:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:49:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:49:42 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:49:43 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:49:43 GMT
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
	-	`sha256:3243ce9c25dc28a597c553cc7f0d4816c4b75789e4ebc37225ac58d5bd078995`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed8e0a01609838fd9b844360403b0c62d26ca345d311c0e12ce9b3b7598f38`  
		Last Modified: Tue, 30 Jun 2020 23:51:10 GMT  
		Size: 12.4 MB (12414918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697e38da42d8f15b4dd54f63870d7e806d1eb7fc0fa15968afda08c82ebb567d`  
		Last Modified: Tue, 30 Jun 2020 23:51:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:251cd735b768dece1a258fe61d2f5f17489920c820d5ed42c431bf03df06c62b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b113527fd3cc583349e001c913567cb5ae6f17df91d84b587c597a69e63574`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:00:00 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:00:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:57:45 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:57:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:57:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:57:57 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:57:58 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:57:58 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:57:59 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:58:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:58:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:58:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:58:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:58:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:58:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:58:09 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:58:10 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:58:11 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:58:12 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:58:13 GMT
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
	-	`sha256:78b107a7bf1560d80dcded532795715f77765cf1a3d9464665d42acab82d366e`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650c88e8e905db99ee64cc19f474dc3c7a32c737e05c403dcda6d96cbee69c4`  
		Last Modified: Tue, 30 Jun 2020 23:59:49 GMT  
		Size: 12.4 MB (12396011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8987db1ddf93e7c11e4c142ecfc8724b54131c3a5bf498a315d3c3dc6846990`  
		Last Modified: Tue, 30 Jun 2020 23:59:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:788931ce2b8e71b550976686f4085c0d4916bdbcc762f9db67d6f0036a109897
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15027460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b8f97e703682d7f83ea2a0146297c030599f59b72b006da9f851c8594777f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:42:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:42:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:39:44 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:39:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:39:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:39:50 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:39:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:39:51 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:39:52 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:39:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:39:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:39:59 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:40:00 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:40:00 GMT
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
	-	`sha256:2b85f4621f67650b74dc2db70b30f9593bc6695d3e91ff3899b3ee7c34cffc04`  
		Last Modified: Mon, 15 Jun 2020 20:44:04 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb12521bcb6d56dcfc220f0b20353a7aa329d702f5feb52f41bcf589de54695`  
		Last Modified: Tue, 30 Jun 2020 23:41:07 GMT  
		Size: 12.0 MB (12013102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599000c030713113e35f054497b6ea20d7cfe46540c547c904d1cb29e5ab5e09`  
		Last Modified: Tue, 30 Jun 2020 23:41:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:eda12afcf0918e61a08bdd958c9c41e599ef640367a8a50b21c7208d3864b9ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14899035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fd2d02dd7c74b824afe02694093d9ad27a7fe4da1f70dc8f499d714c0de004`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:19:13 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:19:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:52:33 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:52:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:53:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:53:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:53:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:53:18 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:53:24 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:53:30 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:53:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:53:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:53:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:54:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:54:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:54:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:54:20 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:54:29 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:54:38 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:54:41 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:54:46 GMT
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
	-	`sha256:3b2288431c86a795754eb4d3a678e778c534a14e9243aea01a7cf9feff8d8e4e`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370c1e51003a37803d04248bb3fbf1f56ca3809ab021a4e661b6d39fb8ef21f`  
		Last Modified: Wed, 01 Jul 2020 01:01:31 GMT  
		Size: 11.8 MB (11785466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acf474ff4d447e0ee036263e810f271f045341957b949e742c4299ff7e8199a`  
		Last Modified: Wed, 01 Jul 2020 01:01:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:c15a47ccc69b6ea56daff5a268d5e93e40faf8ca0124f19c065e301e8ad4bedd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e80a8389cb6f5ffcd0f2092c3c3898d44aa2d3035a3c7482e315a32626622d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:43:15 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:43:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:41:28 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:41:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:41:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:41:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:41:34 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:41:38 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:41:39 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:41:39 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:41:40 GMT
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
	-	`sha256:bf084f3ceb3b3b1196400fa251cc45e01de7ece41b7605bb40ae5178d849b47d`  
		Last Modified: Mon, 15 Jun 2020 20:44:26 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a74ac154ef35abae9974398394ecc94fe54ad18af49231bc6a337fc43346c5`  
		Last Modified: Tue, 30 Jun 2020 23:42:46 GMT  
		Size: 12.8 MB (12836780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5673e745c5f3d1ac989f1a9cc90e301eb65e6dec0d3875d0480300738a959f32`  
		Last Modified: Tue, 30 Jun 2020 23:42:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:643c97d5875621ee1a224c300d130344b4518bb33c1f13ecd48fcce97f2c7bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:530d664fc93dca48b1c5aac4041ab8f94db2300c7e301b721578d3aadc9f60d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305982305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f89e49117b8f842b47277b8ce37f02851dfeb18da89c241f25afe1322ccc517`
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
# Tue, 01 Sep 2020 19:34:35 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 19:36:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 19:36:50 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 19:36:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:36:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 19:36:51 GMT
WORKDIR /go
# Tue, 01 Sep 2020 19:46:18 GMT
WORKDIR /src
# Tue, 01 Sep 2020 19:46:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 19:46:19 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 19:46:21 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 19:46:21 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 19:46:40 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 19:46:43 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 19:46:43 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:cd28c722f6f6bff33648d1a69362ea09192e6c5b41c0604848f7ea8490ff4db9`  
		Last Modified: Tue, 01 Sep 2020 19:43:02 GMT  
		Size: 107.3 MB (107338308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f4f084ab04cf5f263eaadf7ae8add978a542c095db636287348ff0011b060a`  
		Last Modified: Tue, 01 Sep 2020 19:42:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ebda6c2bf751925c9d28dd3ddf434711b59757ff414e94bc7e95b084490fb3`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22004df01bcc06db36622c0faa009585dbdf7419984692ef289bfb30e2df7001`  
		Last Modified: Tue, 01 Sep 2020 19:46:55 GMT  
		Size: 8.3 MB (8310031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95063ecc956a4900df7dbd46015c622c95845c3c82efc7994e13fc83ba0d4d8`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 3.0 MB (3021529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a5064d0396a56f11b584ef9473239e91b053dc33705d4cb75dc90a4e5db2a7`  
		Last Modified: Tue, 01 Sep 2020 19:47:22 GMT  
		Size: 184.2 MB (184231261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac18da66ebccce66529a8a5c82b6f2f5d98e0284937b2c8b43c204fdd1f09fa5`  
		Last Modified: Tue, 01 Sep 2020 19:46:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a6bc59dd3c10a42c3519d7aa483f03e42c0db5ac5e8ccf1c0862cc6e365be1`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bca9f97ade95febc09408fa2d10d24ed25d27a294539631f0fd202b3c6312fa5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301744909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d3e3528b20c6a94ded6b5d109520ae79c86955a4e4fdbcdf4f14150846aaab`
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
# Tue, 01 Sep 2020 21:02:35 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 22:13:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 22:13:41 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 22:14:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 22:15:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 22:15:43 GMT
WORKDIR /go
# Tue, 01 Sep 2020 23:54:52 GMT
WORKDIR /src
# Tue, 01 Sep 2020 23:55:50 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 23:56:08 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 23:57:23 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 23:57:36 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 00:01:34 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 00:02:17 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 00:02:51 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:0c1a3d691278cfe4625eb35113eb4e76dba7b7b922cd23213e3615a7449b7f72`  
		Last Modified: Tue, 01 Sep 2020 23:26:58 GMT  
		Size: 103.7 MB (103667911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755f9ee371ff232fae8ecd0068039d8720f3f3f95fb9d102e7e6a58cb58f9e6e`  
		Last Modified: Tue, 01 Sep 2020 23:26:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e887d24fbc2350fecff867f6127f917fc6eb4b7df003b1774e91e9a1f2f27`  
		Last Modified: Wed, 02 Sep 2020 00:03:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807a9c07aa5d372f3fe371b3a8f5c0bc7faa3349934a30ef9346a6366dba2703`  
		Last Modified: Wed, 02 Sep 2020 00:03:22 GMT  
		Size: 7.9 MB (7928883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61096b4836c4bc4dd217b18de0eb5d8ac019a7f8429b138e3cc4edf31b2dbe82`  
		Last Modified: Wed, 02 Sep 2020 00:03:20 GMT  
		Size: 3.0 MB (3019410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6b78006ffc6587da18d44f165ef51866b235717d237176121b70a1a403d6d`  
		Last Modified: Wed, 02 Sep 2020 00:05:09 GMT  
		Size: 184.2 MB (184241509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9077b5629d7e79f07d846547d35e15467f6dad0686e7777cf8132e9a74f5de`  
		Last Modified: Wed, 02 Sep 2020 00:03:20 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5099129bea582dbd70a6c6f2fd933a6ef6dbeec6b23726ed103095e5a2084b7a`  
		Last Modified: Wed, 02 Sep 2020 00:03:20 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fcb33ea694c7bdb3bc88c21632942684155bc3ff746b11b20fe9440863bd7e59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300522401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36afb392704f9e4127f3f545047cd24888d97078d4728f12ac0de131bb49a9dd`
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
# Tue, 01 Sep 2020 23:03:51 GMT
ENV GOLANG_VERSION=1.14.8
# Wed, 02 Sep 2020 00:10:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 02 Sep 2020 00:11:00 GMT
ENV GOPATH=/go
# Wed, 02 Sep 2020 00:11:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Sep 2020 00:11:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Sep 2020 00:11:35 GMT
WORKDIR /go
# Wed, 02 Sep 2020 01:30:15 GMT
WORKDIR /src
# Wed, 02 Sep 2020 01:30:41 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 02 Sep 2020 01:30:46 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 02 Sep 2020 01:31:15 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 02 Sep 2020 01:31:19 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 01:32:56 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 01:33:10 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 01:33:15 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:ccafdd70e65ad98952807d42e06e048856f0c083e2978115ab4a4dde9205d7e2`  
		Last Modified: Wed, 02 Sep 2020 01:19:29 GMT  
		Size: 103.4 MB (103425137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd1514ccf0f746c697082d73324febe490c127c7642ef083de4a32136a3939c`  
		Last Modified: Wed, 02 Sep 2020 01:18:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b850ac09b7e0dbccd54397052f9635f84d8dbc906924ff659eb36d9da92c64`  
		Last Modified: Wed, 02 Sep 2020 01:33:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c305eb69f70ad04ca7bebd869369774a052be87a39f2adbb35ff36410f961c`  
		Last Modified: Wed, 02 Sep 2020 01:33:37 GMT  
		Size: 7.1 MB (7144945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6498251e87f04f5193188d7d81f39ebaabc92a062e12672df80a944f982ec01`  
		Last Modified: Wed, 02 Sep 2020 01:33:36 GMT  
		Size: 3.0 MB (3023124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c1863b298bdd871d6d5b3054be0513d1b919f4a2b8d9594269e69955187bf6`  
		Last Modified: Wed, 02 Sep 2020 01:34:20 GMT  
		Size: 184.2 MB (184239410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7820692de33884f3f143ce04108330d918263155dcb094f632d49353cc6fc`  
		Last Modified: Wed, 02 Sep 2020 01:33:36 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac75b79cbff116bca566952a6915a413878540ac764f28cb5618e7f6c5b26ec`  
		Last Modified: Wed, 02 Sep 2020 01:33:36 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:0f38e26a40310a168078cb7b86a52c600d873c7e9838fa8c3f957a460ff3896f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301521324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fc152bf238535be273ff83aa09cd84c9167f3a401056db6c22b07d01a5b639`
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
# Tue, 01 Sep 2020 22:21:53 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 22:28:02 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 22:28:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 22:29:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 22:29:59 GMT
WORKDIR /go
# Tue, 01 Sep 2020 23:59:26 GMT
WORKDIR /src
# Wed, 02 Sep 2020 00:00:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 02 Sep 2020 00:00:11 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 02 Sep 2020 00:03:01 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 02 Sep 2020 00:03:20 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 00:04:32 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 00:04:43 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 00:04:51 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:1b753c98a16c78448f78b84920abfa41d762cccff115f2470d293b55284eb67c`  
		Last Modified: Tue, 01 Sep 2020 22:44:39 GMT  
		Size: 102.8 MB (102770337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb840484a8cf8606be10acc343938d8a0873d5fe46ba82c9c597a739dd217d5`  
		Last Modified: Tue, 01 Sep 2020 22:44:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76417713493a8725e79524a31ac62fc8eaffbd316ea9d552681fca013fbd3099`  
		Last Modified: Wed, 02 Sep 2020 00:05:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4c31c540f49a3194ad36892aa103ddb83fe9e790797f2340655c6c7ac9817e`  
		Last Modified: Wed, 02 Sep 2020 00:05:17 GMT  
		Size: 8.5 MB (8499919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416a2e78480040fa946d4af0e14276575ef691ecbca5f87da67f93ed765b4d05`  
		Last Modified: Wed, 02 Sep 2020 00:05:17 GMT  
		Size: 3.0 MB (3019449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cff76c2ff5d488b52a3d38fbab7ef2c7371716875f832cf38c35de021880f7`  
		Last Modified: Wed, 02 Sep 2020 00:06:00 GMT  
		Size: 184.2 MB (184239526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51743cf71732c8b66796ae05cdaf4975f42f862c185978ca78b094296fe2a174`  
		Last Modified: Wed, 02 Sep 2020 00:05:16 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb9a8de871f4c123dc35f3d167810586180f0c9d13cad2bb6e1ad7dc7c70150`  
		Last Modified: Wed, 02 Sep 2020 00:05:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:a4c9e614785e73f9980f8b2f1280e60cb78c8bc69fb96fbfcd4738b286a1961f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300863289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f5c3531bfaff72603882514e919fdc422f04d5961b2e740266d170cdd783e`
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
# Wed, 02 Sep 2020 02:56:21 GMT
ENV GOLANG_VERSION=1.14.8
# Wed, 02 Sep 2020 02:58:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 02 Sep 2020 02:58:41 GMT
ENV GOPATH=/go
# Wed, 02 Sep 2020 02:58:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Sep 2020 02:59:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Sep 2020 02:59:04 GMT
WORKDIR /go
# Wed, 02 Sep 2020 03:30:04 GMT
WORKDIR /src
# Wed, 02 Sep 2020 03:30:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 02 Sep 2020 03:30:19 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 02 Sep 2020 03:30:30 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 02 Sep 2020 03:30:34 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 03:34:51 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 03:34:58 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 03:35:05 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:a7be439f828eeb9dade6b3c4d250fea147c4bf9ea749ad1171b1e0f15cb0e7a0`  
		Last Modified: Wed, 02 Sep 2020 03:05:12 GMT  
		Size: 101.6 MB (101587261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858283ff3c5a8a5672a547616e2bccfb9e9d3c47a62794acce6eb9ff926473f8`  
		Last Modified: Wed, 02 Sep 2020 03:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448945833acd7eec62ff140509665b36ac2a3e4d255d90ac6de59f53a8eded9a`  
		Last Modified: Wed, 02 Sep 2020 03:35:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445cb5b17ad69c6db778ba638564478d36f35150d080ce2b32ab27d4eac1039`  
		Last Modified: Wed, 02 Sep 2020 03:35:43 GMT  
		Size: 8.9 MB (8920026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c779dfbf194735d2c7c60a94b07405e8ef77e68f99deb7dbf2ff1f069c8e27ca`  
		Last Modified: Wed, 02 Sep 2020 03:35:42 GMT  
		Size: 3.0 MB (3019813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b327557c04a11b827536c6b5b4e8345e8887e26d43d1096bcb885085bc65157`  
		Last Modified: Wed, 02 Sep 2020 03:36:12 GMT  
		Size: 184.2 MB (184244825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2cc122dd885bcc30ad0d0637a1d28208beec16664ebc9a17775e61a29ee2`  
		Last Modified: Wed, 02 Sep 2020 03:35:40 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21bd9e29bbf2dc2b7e9708b23cf901f3bf4c2ce214fd048f0264959e759397e`  
		Last Modified: Wed, 02 Sep 2020 03:35:41 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:7e4c3f3223de987021dc6c2e2dd0171c828b7aa9bb6293181b8cb697e6dab9fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305648613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dac070d5c68f4c2e6cfcc91d843df4050389c9cebe743104c796ea839cdda3`
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
# Tue, 01 Sep 2020 19:44:01 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 19:45:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 19:45:35 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 19:45:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:45:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 19:45:37 GMT
WORKDIR /go
# Tue, 01 Sep 2020 20:04:54 GMT
WORKDIR /src
# Tue, 01 Sep 2020 20:04:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 20:04:56 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 20:04:57 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 20:04:58 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 20:05:14 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 20:05:22 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 20:05:23 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:30e232aad579fb98c2f2045f3f7b7ba0fbffcfc8e29b42d0ba5a359837b0c4e1`  
		Last Modified: Tue, 01 Sep 2020 19:49:06 GMT  
		Size: 107.2 MB (107195429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2165b261634b409611a87b9a553177bf635c26b3a0516de364edac85a8d27b27`  
		Last Modified: Tue, 01 Sep 2020 19:48:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1062f7882f263f26082444069fc6189191916dc260cbfc4dbe282b15d49a3fbd`  
		Last Modified: Tue, 01 Sep 2020 20:05:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c18eaf417133e1baa67c0e5e908a0d1cc12dbac23d7d930307c5b9973f3b91`  
		Last Modified: Tue, 01 Sep 2020 20:05:38 GMT  
		Size: 8.4 MB (8352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e16c5f4c29abf40f9273613ac29277c5ee3401f1e69d6e11393d1c5cde4440e`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 3.0 MB (3019353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae13017144598018fbf639fd94a2cff812baec7a4a31e5eec23d4b12738fa3cd`  
		Last Modified: Tue, 01 Sep 2020 20:05:53 GMT  
		Size: 184.2 MB (184231123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e262f312527240c7ac156ee2650905668e128bd06e381594ab2f18f66d6000e2`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb074fabd331ca17a2cb9e7f77792f2e79671375f012ecee518944363de5157`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:40c4f77513048ee7e05ee01fb89d360e22b13325c3daaffca57dee62c72b575d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64
	-	windows version 10.0.14393.3930; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:54fc1c11a9a4de45c0e3b30aa2702ac0e55d355cd47e3f7f4fbfdc475bc6c132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:deb60a2701067b98424a7cc203f79a61a9f41d6b772df3b6c0ba34236cce1c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3930; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:707e960e783141b786754199242c2aa10046712e7b2697aa3bc030492c50de2a
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
$ docker pull caddy@sha256:9ce811ab3540971fab00748e5d9a6bc7a91518fc9848367c907e32fda8d01411
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a12b5c957bab94f57aadfd9e655d414ab69443495f22ef430152181ab0aede`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:21:16 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:21:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:19:34 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:19:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:19:40 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:19:40 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:19:40 GMT
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
	-	`sha256:b1e49a2f7ba4b80caa31bb2874b39f9c4bbb447708f3a0e07ff43892744e63a4`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6f0d7c084024816c9d62c8cf79558a18c5df4cdcc951484a9e0ca63dd0b72`  
		Last Modified: Wed, 01 Jul 2020 00:20:17 GMT  
		Size: 13.1 MB (13057334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639b35073727cad03304869adcd7b9118cd8039707d055f5b37992f7188076d3`  
		Last Modified: Wed, 01 Jul 2020 00:20:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c8dd4b191727d7eccb50cdf3f3d26fe19abbd23be153dfd53a11f01059002928
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15324343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352f7aeefb2f9e7015bf833505ff90d75dc751bfa7d202255900787d9c1a6e1a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:52:07 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:52:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:49:25 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:49:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:49:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:49:33 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:49:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:49:34 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:49:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:49:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:49:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:49:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:49:42 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:49:43 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:49:43 GMT
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
	-	`sha256:3243ce9c25dc28a597c553cc7f0d4816c4b75789e4ebc37225ac58d5bd078995`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed8e0a01609838fd9b844360403b0c62d26ca345d311c0e12ce9b3b7598f38`  
		Last Modified: Tue, 30 Jun 2020 23:51:10 GMT  
		Size: 12.4 MB (12414918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697e38da42d8f15b4dd54f63870d7e806d1eb7fc0fa15968afda08c82ebb567d`  
		Last Modified: Tue, 30 Jun 2020 23:51:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:251cd735b768dece1a258fe61d2f5f17489920c820d5ed42c431bf03df06c62b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b113527fd3cc583349e001c913567cb5ae6f17df91d84b587c597a69e63574`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:00:00 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:00:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:57:45 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:57:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:57:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:57:57 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:57:58 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:57:58 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:57:59 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:58:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:58:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:58:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:58:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:58:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:58:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:58:09 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:58:10 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:58:11 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:58:12 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:58:13 GMT
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
	-	`sha256:78b107a7bf1560d80dcded532795715f77765cf1a3d9464665d42acab82d366e`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650c88e8e905db99ee64cc19f474dc3c7a32c737e05c403dcda6d96cbee69c4`  
		Last Modified: Tue, 30 Jun 2020 23:59:49 GMT  
		Size: 12.4 MB (12396011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8987db1ddf93e7c11e4c142ecfc8724b54131c3a5bf498a315d3c3dc6846990`  
		Last Modified: Tue, 30 Jun 2020 23:59:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:788931ce2b8e71b550976686f4085c0d4916bdbcc762f9db67d6f0036a109897
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15027460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b8f97e703682d7f83ea2a0146297c030599f59b72b006da9f851c8594777f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:42:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:42:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:39:44 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:39:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:39:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:39:50 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:39:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:39:51 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:39:52 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:39:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:39:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:39:59 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:40:00 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:40:00 GMT
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
	-	`sha256:2b85f4621f67650b74dc2db70b30f9593bc6695d3e91ff3899b3ee7c34cffc04`  
		Last Modified: Mon, 15 Jun 2020 20:44:04 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb12521bcb6d56dcfc220f0b20353a7aa329d702f5feb52f41bcf589de54695`  
		Last Modified: Tue, 30 Jun 2020 23:41:07 GMT  
		Size: 12.0 MB (12013102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599000c030713113e35f054497b6ea20d7cfe46540c547c904d1cb29e5ab5e09`  
		Last Modified: Tue, 30 Jun 2020 23:41:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:eda12afcf0918e61a08bdd958c9c41e599ef640367a8a50b21c7208d3864b9ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14899035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fd2d02dd7c74b824afe02694093d9ad27a7fe4da1f70dc8f499d714c0de004`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:19:13 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:19:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:52:33 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:52:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:53:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:53:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:53:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:53:18 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:53:24 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:53:30 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:53:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:53:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:53:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:54:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:54:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:54:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:54:20 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:54:29 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:54:38 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:54:41 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:54:46 GMT
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
	-	`sha256:3b2288431c86a795754eb4d3a678e778c534a14e9243aea01a7cf9feff8d8e4e`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370c1e51003a37803d04248bb3fbf1f56ca3809ab021a4e661b6d39fb8ef21f`  
		Last Modified: Wed, 01 Jul 2020 01:01:31 GMT  
		Size: 11.8 MB (11785466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acf474ff4d447e0ee036263e810f271f045341957b949e742c4299ff7e8199a`  
		Last Modified: Wed, 01 Jul 2020 01:01:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:c15a47ccc69b6ea56daff5a268d5e93e40faf8ca0124f19c065e301e8ad4bedd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e80a8389cb6f5ffcd0f2092c3c3898d44aa2d3035a3c7482e315a32626622d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:43:15 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:43:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:41:28 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:41:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:41:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:41:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:41:34 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:41:38 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:41:39 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:41:39 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:41:40 GMT
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
	-	`sha256:bf084f3ceb3b3b1196400fa251cc45e01de7ece41b7605bb40ae5178d849b47d`  
		Last Modified: Mon, 15 Jun 2020 20:44:26 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a74ac154ef35abae9974398394ecc94fe54ad18af49231bc6a337fc43346c5`  
		Last Modified: Tue, 30 Jun 2020 23:42:46 GMT  
		Size: 12.8 MB (12836780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5673e745c5f3d1ac989f1a9cc90e301eb65e6dec0d3875d0480300738a959f32`  
		Last Modified: Tue, 30 Jun 2020 23:42:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:643c97d5875621ee1a224c300d130344b4518bb33c1f13ecd48fcce97f2c7bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:530d664fc93dca48b1c5aac4041ab8f94db2300c7e301b721578d3aadc9f60d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305982305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f89e49117b8f842b47277b8ce37f02851dfeb18da89c241f25afe1322ccc517`
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
# Tue, 01 Sep 2020 19:34:35 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 19:36:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 19:36:50 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 19:36:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:36:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 19:36:51 GMT
WORKDIR /go
# Tue, 01 Sep 2020 19:46:18 GMT
WORKDIR /src
# Tue, 01 Sep 2020 19:46:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 19:46:19 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 19:46:21 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 19:46:21 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 19:46:40 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 19:46:43 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 19:46:43 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:cd28c722f6f6bff33648d1a69362ea09192e6c5b41c0604848f7ea8490ff4db9`  
		Last Modified: Tue, 01 Sep 2020 19:43:02 GMT  
		Size: 107.3 MB (107338308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f4f084ab04cf5f263eaadf7ae8add978a542c095db636287348ff0011b060a`  
		Last Modified: Tue, 01 Sep 2020 19:42:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ebda6c2bf751925c9d28dd3ddf434711b59757ff414e94bc7e95b084490fb3`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22004df01bcc06db36622c0faa009585dbdf7419984692ef289bfb30e2df7001`  
		Last Modified: Tue, 01 Sep 2020 19:46:55 GMT  
		Size: 8.3 MB (8310031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95063ecc956a4900df7dbd46015c622c95845c3c82efc7994e13fc83ba0d4d8`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 3.0 MB (3021529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a5064d0396a56f11b584ef9473239e91b053dc33705d4cb75dc90a4e5db2a7`  
		Last Modified: Tue, 01 Sep 2020 19:47:22 GMT  
		Size: 184.2 MB (184231261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac18da66ebccce66529a8a5c82b6f2f5d98e0284937b2c8b43c204fdd1f09fa5`  
		Last Modified: Tue, 01 Sep 2020 19:46:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a6bc59dd3c10a42c3519d7aa483f03e42c0db5ac5e8ccf1c0862cc6e365be1`  
		Last Modified: Tue, 01 Sep 2020 19:46:54 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bca9f97ade95febc09408fa2d10d24ed25d27a294539631f0fd202b3c6312fa5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301744909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d3e3528b20c6a94ded6b5d109520ae79c86955a4e4fdbcdf4f14150846aaab`
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
# Tue, 01 Sep 2020 21:02:35 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 22:13:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 22:13:41 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 22:14:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 22:15:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 22:15:43 GMT
WORKDIR /go
# Tue, 01 Sep 2020 23:54:52 GMT
WORKDIR /src
# Tue, 01 Sep 2020 23:55:50 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 23:56:08 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 23:57:23 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 23:57:36 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 00:01:34 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 00:02:17 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 00:02:51 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:0c1a3d691278cfe4625eb35113eb4e76dba7b7b922cd23213e3615a7449b7f72`  
		Last Modified: Tue, 01 Sep 2020 23:26:58 GMT  
		Size: 103.7 MB (103667911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755f9ee371ff232fae8ecd0068039d8720f3f3f95fb9d102e7e6a58cb58f9e6e`  
		Last Modified: Tue, 01 Sep 2020 23:26:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7e887d24fbc2350fecff867f6127f917fc6eb4b7df003b1774e91e9a1f2f27`  
		Last Modified: Wed, 02 Sep 2020 00:03:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807a9c07aa5d372f3fe371b3a8f5c0bc7faa3349934a30ef9346a6366dba2703`  
		Last Modified: Wed, 02 Sep 2020 00:03:22 GMT  
		Size: 7.9 MB (7928883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61096b4836c4bc4dd217b18de0eb5d8ac019a7f8429b138e3cc4edf31b2dbe82`  
		Last Modified: Wed, 02 Sep 2020 00:03:20 GMT  
		Size: 3.0 MB (3019410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6b78006ffc6587da18d44f165ef51866b235717d237176121b70a1a403d6d`  
		Last Modified: Wed, 02 Sep 2020 00:05:09 GMT  
		Size: 184.2 MB (184241509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9077b5629d7e79f07d846547d35e15467f6dad0686e7777cf8132e9a74f5de`  
		Last Modified: Wed, 02 Sep 2020 00:03:20 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5099129bea582dbd70a6c6f2fd933a6ef6dbeec6b23726ed103095e5a2084b7a`  
		Last Modified: Wed, 02 Sep 2020 00:03:20 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fcb33ea694c7bdb3bc88c21632942684155bc3ff746b11b20fe9440863bd7e59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300522401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36afb392704f9e4127f3f545047cd24888d97078d4728f12ac0de131bb49a9dd`
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
# Tue, 01 Sep 2020 23:03:51 GMT
ENV GOLANG_VERSION=1.14.8
# Wed, 02 Sep 2020 00:10:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 02 Sep 2020 00:11:00 GMT
ENV GOPATH=/go
# Wed, 02 Sep 2020 00:11:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Sep 2020 00:11:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Sep 2020 00:11:35 GMT
WORKDIR /go
# Wed, 02 Sep 2020 01:30:15 GMT
WORKDIR /src
# Wed, 02 Sep 2020 01:30:41 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 02 Sep 2020 01:30:46 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 02 Sep 2020 01:31:15 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 02 Sep 2020 01:31:19 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 01:32:56 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 01:33:10 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 01:33:15 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:ccafdd70e65ad98952807d42e06e048856f0c083e2978115ab4a4dde9205d7e2`  
		Last Modified: Wed, 02 Sep 2020 01:19:29 GMT  
		Size: 103.4 MB (103425137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd1514ccf0f746c697082d73324febe490c127c7642ef083de4a32136a3939c`  
		Last Modified: Wed, 02 Sep 2020 01:18:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b850ac09b7e0dbccd54397052f9635f84d8dbc906924ff659eb36d9da92c64`  
		Last Modified: Wed, 02 Sep 2020 01:33:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c305eb69f70ad04ca7bebd869369774a052be87a39f2adbb35ff36410f961c`  
		Last Modified: Wed, 02 Sep 2020 01:33:37 GMT  
		Size: 7.1 MB (7144945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6498251e87f04f5193188d7d81f39ebaabc92a062e12672df80a944f982ec01`  
		Last Modified: Wed, 02 Sep 2020 01:33:36 GMT  
		Size: 3.0 MB (3023124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c1863b298bdd871d6d5b3054be0513d1b919f4a2b8d9594269e69955187bf6`  
		Last Modified: Wed, 02 Sep 2020 01:34:20 GMT  
		Size: 184.2 MB (184239410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7820692de33884f3f143ce04108330d918263155dcb094f632d49353cc6fc`  
		Last Modified: Wed, 02 Sep 2020 01:33:36 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac75b79cbff116bca566952a6915a413878540ac764f28cb5618e7f6c5b26ec`  
		Last Modified: Wed, 02 Sep 2020 01:33:36 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:0f38e26a40310a168078cb7b86a52c600d873c7e9838fa8c3f957a460ff3896f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301521324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fc152bf238535be273ff83aa09cd84c9167f3a401056db6c22b07d01a5b639`
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
# Tue, 01 Sep 2020 22:21:53 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 22:28:02 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 22:28:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 22:29:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 22:29:59 GMT
WORKDIR /go
# Tue, 01 Sep 2020 23:59:26 GMT
WORKDIR /src
# Wed, 02 Sep 2020 00:00:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 02 Sep 2020 00:00:11 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 02 Sep 2020 00:03:01 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 02 Sep 2020 00:03:20 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 00:04:32 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 00:04:43 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 00:04:51 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:1b753c98a16c78448f78b84920abfa41d762cccff115f2470d293b55284eb67c`  
		Last Modified: Tue, 01 Sep 2020 22:44:39 GMT  
		Size: 102.8 MB (102770337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb840484a8cf8606be10acc343938d8a0873d5fe46ba82c9c597a739dd217d5`  
		Last Modified: Tue, 01 Sep 2020 22:44:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76417713493a8725e79524a31ac62fc8eaffbd316ea9d552681fca013fbd3099`  
		Last Modified: Wed, 02 Sep 2020 00:05:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4c31c540f49a3194ad36892aa103ddb83fe9e790797f2340655c6c7ac9817e`  
		Last Modified: Wed, 02 Sep 2020 00:05:17 GMT  
		Size: 8.5 MB (8499919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416a2e78480040fa946d4af0e14276575ef691ecbca5f87da67f93ed765b4d05`  
		Last Modified: Wed, 02 Sep 2020 00:05:17 GMT  
		Size: 3.0 MB (3019449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cff76c2ff5d488b52a3d38fbab7ef2c7371716875f832cf38c35de021880f7`  
		Last Modified: Wed, 02 Sep 2020 00:06:00 GMT  
		Size: 184.2 MB (184239526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51743cf71732c8b66796ae05cdaf4975f42f862c185978ca78b094296fe2a174`  
		Last Modified: Wed, 02 Sep 2020 00:05:16 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb9a8de871f4c123dc35f3d167810586180f0c9d13cad2bb6e1ad7dc7c70150`  
		Last Modified: Wed, 02 Sep 2020 00:05:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:a4c9e614785e73f9980f8b2f1280e60cb78c8bc69fb96fbfcd4738b286a1961f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300863289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9f5c3531bfaff72603882514e919fdc422f04d5961b2e740266d170cdd783e`
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
# Wed, 02 Sep 2020 02:56:21 GMT
ENV GOLANG_VERSION=1.14.8
# Wed, 02 Sep 2020 02:58:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Wed, 02 Sep 2020 02:58:41 GMT
ENV GOPATH=/go
# Wed, 02 Sep 2020 02:58:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Sep 2020 02:59:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Sep 2020 02:59:04 GMT
WORKDIR /go
# Wed, 02 Sep 2020 03:30:04 GMT
WORKDIR /src
# Wed, 02 Sep 2020 03:30:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 02 Sep 2020 03:30:19 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Wed, 02 Sep 2020 03:30:30 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Wed, 02 Sep 2020 03:30:34 GMT
WORKDIR /src/caddy/cmd/caddy
# Wed, 02 Sep 2020 03:34:51 GMT
RUN go get -d ./...
# Wed, 02 Sep 2020 03:34:58 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Wed, 02 Sep 2020 03:35:05 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:a7be439f828eeb9dade6b3c4d250fea147c4bf9ea749ad1171b1e0f15cb0e7a0`  
		Last Modified: Wed, 02 Sep 2020 03:05:12 GMT  
		Size: 101.6 MB (101587261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858283ff3c5a8a5672a547616e2bccfb9e9d3c47a62794acce6eb9ff926473f8`  
		Last Modified: Wed, 02 Sep 2020 03:04:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448945833acd7eec62ff140509665b36ac2a3e4d255d90ac6de59f53a8eded9a`  
		Last Modified: Wed, 02 Sep 2020 03:35:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445cb5b17ad69c6db778ba638564478d36f35150d080ce2b32ab27d4eac1039`  
		Last Modified: Wed, 02 Sep 2020 03:35:43 GMT  
		Size: 8.9 MB (8920026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c779dfbf194735d2c7c60a94b07405e8ef77e68f99deb7dbf2ff1f069c8e27ca`  
		Last Modified: Wed, 02 Sep 2020 03:35:42 GMT  
		Size: 3.0 MB (3019813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b327557c04a11b827536c6b5b4e8345e8887e26d43d1096bcb885085bc65157`  
		Last Modified: Wed, 02 Sep 2020 03:36:12 GMT  
		Size: 184.2 MB (184244825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2cc122dd885bcc30ad0d0637a1d28208beec16664ebc9a17775e61a29ee2`  
		Last Modified: Wed, 02 Sep 2020 03:35:40 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21bd9e29bbf2dc2b7e9708b23cf901f3bf4c2ce214fd048f0264959e759397e`  
		Last Modified: Wed, 02 Sep 2020 03:35:41 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:7e4c3f3223de987021dc6c2e2dd0171c828b7aa9bb6293181b8cb697e6dab9fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305648613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dac070d5c68f4c2e6cfcc91d843df4050389c9cebe743104c796ea839cdda3`
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
# Tue, 01 Sep 2020 19:44:01 GMT
ENV GOLANG_VERSION=1.14.8
# Tue, 01 Sep 2020 19:45:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		url='https://storage.googleapis.com/golang/go1.14.8.src.tar.gz'; 	sha256='d9a613fb55f508cf84e753456a7c6a113c8265839d5b7fe060da335c93d6e36a'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 	eval "$goEnv"; 	[ -n "$GOOS" ]; 	[ -n "$GOARCH" ]; 	( 		cd /usr/local/go/src; 		./make.bash; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Tue, 01 Sep 2020 19:45:35 GMT
ENV GOPATH=/go
# Tue, 01 Sep 2020 19:45:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 19:45:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Sep 2020 19:45:37 GMT
WORKDIR /go
# Tue, 01 Sep 2020 20:04:54 GMT
WORKDIR /src
# Tue, 01 Sep 2020 20:04:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 01 Sep 2020 20:04:56 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 01 Sep 2020 20:04:57 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 01 Sep 2020 20:04:58 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 01 Sep 2020 20:05:14 GMT
RUN go get -d ./...
# Tue, 01 Sep 2020 20:05:22 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 01 Sep 2020 20:05:23 GMT
WORKDIR /src/custom-caddy/cmd/caddy
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
	-	`sha256:30e232aad579fb98c2f2045f3f7b7ba0fbffcfc8e29b42d0ba5a359837b0c4e1`  
		Last Modified: Tue, 01 Sep 2020 19:49:06 GMT  
		Size: 107.2 MB (107195429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2165b261634b409611a87b9a553177bf635c26b3a0516de364edac85a8d27b27`  
		Last Modified: Tue, 01 Sep 2020 19:48:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1062f7882f263f26082444069fc6189191916dc260cbfc4dbe282b15d49a3fbd`  
		Last Modified: Tue, 01 Sep 2020 20:05:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c18eaf417133e1baa67c0e5e908a0d1cc12dbac23d7d930307c5b9973f3b91`  
		Last Modified: Tue, 01 Sep 2020 20:05:38 GMT  
		Size: 8.4 MB (8352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e16c5f4c29abf40f9273613ac29277c5ee3401f1e69d6e11393d1c5cde4440e`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 3.0 MB (3019353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae13017144598018fbf639fd94a2cff812baec7a4a31e5eec23d4b12738fa3cd`  
		Last Modified: Tue, 01 Sep 2020 20:05:53 GMT  
		Size: 184.2 MB (184231123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e262f312527240c7ac156ee2650905668e128bd06e381594ab2f18f66d6000e2`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb074fabd331ca17a2cb9e7f77792f2e79671375f012ecee518944363de5157`  
		Last Modified: Tue, 01 Sep 2020 20:05:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:d9e3041657102dfd878f2c70893cb324cca11f9e1d22ad82692d2c4bb83f41c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1457; amd64
	-	windows version 10.0.14393.3930; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:9ce811ab3540971fab00748e5d9a6bc7a91518fc9848367c907e32fda8d01411
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16160777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a12b5c957bab94f57aadfd9e655d414ab69443495f22ef430152181ab0aede`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:21:16 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:21:16 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:21:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:19:34 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:19:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:19:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:19:37 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:19:37 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:19:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:19:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:19:39 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:19:40 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:19:40 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:19:40 GMT
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
	-	`sha256:b1e49a2f7ba4b80caa31bb2874b39f9c4bbb447708f3a0e07ff43892744e63a4`  
		Last Modified: Mon, 15 Jun 2020 21:22:02 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d6f0d7c084024816c9d62c8cf79558a18c5df4cdcc951484a9e0ca63dd0b72`  
		Last Modified: Wed, 01 Jul 2020 00:20:17 GMT  
		Size: 13.1 MB (13057334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639b35073727cad03304869adcd7b9118cd8039707d055f5b37992f7188076d3`  
		Last Modified: Wed, 01 Jul 2020 00:20:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c8dd4b191727d7eccb50cdf3f3d26fe19abbd23be153dfd53a11f01059002928
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15324343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352f7aeefb2f9e7015bf833505ff90d75dc751bfa7d202255900787d9c1a6e1a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:52:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:52:07 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:52:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:49:25 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:49:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:49:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:49:32 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:49:33 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:49:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:49:34 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:49:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:49:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:49:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:49:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:49:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:49:41 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:49:42 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:49:43 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:49:43 GMT
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
	-	`sha256:3243ce9c25dc28a597c553cc7f0d4816c4b75789e4ebc37225ac58d5bd078995`  
		Last Modified: Mon, 15 Jun 2020 20:54:38 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ed8e0a01609838fd9b844360403b0c62d26ca345d311c0e12ce9b3b7598f38`  
		Last Modified: Tue, 30 Jun 2020 23:51:10 GMT  
		Size: 12.4 MB (12414918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697e38da42d8f15b4dd54f63870d7e806d1eb7fc0fa15968afda08c82ebb567d`  
		Last Modified: Tue, 30 Jun 2020 23:51:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:251cd735b768dece1a258fe61d2f5f17489920c820d5ed42c431bf03df06c62b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b113527fd3cc583349e001c913567cb5ae6f17df91d84b587c597a69e63574`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:59:59 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:00:00 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:00:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:57:45 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:57:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:57:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:57:57 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:57:58 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:57:58 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:57:59 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:58:00 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:58:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:58:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:58:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:58:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:58:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:58:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:58:09 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:58:10 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:58:11 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:58:12 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:58:13 GMT
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
	-	`sha256:78b107a7bf1560d80dcded532795715f77765cf1a3d9464665d42acab82d366e`  
		Last Modified: Mon, 15 Jun 2020 21:02:12 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650c88e8e905db99ee64cc19f474dc3c7a32c737e05c403dcda6d96cbee69c4`  
		Last Modified: Tue, 30 Jun 2020 23:59:49 GMT  
		Size: 12.4 MB (12396011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8987db1ddf93e7c11e4c142ecfc8724b54131c3a5bf498a315d3c3dc6846990`  
		Last Modified: Tue, 30 Jun 2020 23:59:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:788931ce2b8e71b550976686f4085c0d4916bdbcc762f9db67d6f0036a109897
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15027460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b8f97e703682d7f83ea2a0146297c030599f59b72b006da9f851c8594777f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:42:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:42:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:42:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:39:44 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:39:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:39:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:39:50 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:39:51 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:39:51 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:39:52 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:39:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:39:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:39:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:39:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:39:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:39:58 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:39:59 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:40:00 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:40:00 GMT
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
	-	`sha256:2b85f4621f67650b74dc2db70b30f9593bc6695d3e91ff3899b3ee7c34cffc04`  
		Last Modified: Mon, 15 Jun 2020 20:44:04 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb12521bcb6d56dcfc220f0b20353a7aa329d702f5feb52f41bcf589de54695`  
		Last Modified: Tue, 30 Jun 2020 23:41:07 GMT  
		Size: 12.0 MB (12013102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599000c030713113e35f054497b6ea20d7cfe46540c547c904d1cb29e5ab5e09`  
		Last Modified: Tue, 30 Jun 2020 23:41:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:eda12afcf0918e61a08bdd958c9c41e599ef640367a8a50b21c7208d3864b9ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14899035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fd2d02dd7c74b824afe02694093d9ad27a7fe4da1f70dc8f499d714c0de004`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 21:19:09 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 21:19:13 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 21:19:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 01 Jul 2020 00:52:33 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 01 Jul 2020 00:52:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 01 Jul 2020 00:53:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 01 Jul 2020 00:53:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 01 Jul 2020 00:53:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 01 Jul 2020 00:53:18 GMT
VOLUME [/config]
# Wed, 01 Jul 2020 00:53:24 GMT
VOLUME [/data]
# Wed, 01 Jul 2020 00:53:30 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 01 Jul 2020 00:53:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 Jul 2020 00:53:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 Jul 2020 00:53:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 Jul 2020 00:53:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 Jul 2020 00:54:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 Jul 2020 00:54:11 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 Jul 2020 00:54:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 Jul 2020 00:54:20 GMT
EXPOSE 80
# Wed, 01 Jul 2020 00:54:29 GMT
EXPOSE 443
# Wed, 01 Jul 2020 00:54:38 GMT
EXPOSE 2019
# Wed, 01 Jul 2020 00:54:41 GMT
WORKDIR /srv
# Wed, 01 Jul 2020 00:54:46 GMT
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
	-	`sha256:3b2288431c86a795754eb4d3a678e778c534a14e9243aea01a7cf9feff8d8e4e`  
		Last Modified: Mon, 15 Jun 2020 21:24:35 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370c1e51003a37803d04248bb3fbf1f56ca3809ab021a4e661b6d39fb8ef21f`  
		Last Modified: Wed, 01 Jul 2020 01:01:31 GMT  
		Size: 11.8 MB (11785466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acf474ff4d447e0ee036263e810f271f045341957b949e742c4299ff7e8199a`  
		Last Modified: Wed, 01 Jul 2020 01:01:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:c15a47ccc69b6ea56daff5a268d5e93e40faf8ca0124f19c065e301e8ad4bedd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15709487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e80a8389cb6f5ffcd0f2092c3c3898d44aa2d3035a3c7482e315a32626622d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Mon, 15 Jun 2020 20:43:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 15 Jun 2020 20:43:15 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Mon, 15 Jun 2020 20:43:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Tue, 30 Jun 2020 23:41:28 GMT
ENV CADDY_VERSION=v2.1.1
# Tue, 30 Jun 2020 23:41:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='41f2442c52daf5a36d07af5024711072925997d8b5a7bd459994b000cfee1cb63d0c97d1b54b172c59b6b02a0f0eab285141a8cd3fc23cbca684f824c7b21b75' ;; 		armhf)   binArch='armv6'; checksum='91b69356155b4909feec8c4e5674a52d13c75b5c4bedfa3c7be2615a18cecbb58212de753d288ecd355502412d33bde9beed713055263636039ee4c47466ca90' ;; 		armv7)   binArch='armv7'; checksum='e45d8c8ac9fab83a26660531ef117dd0fbcaf81e442bb01f0d068afda6c507e692105e0c7f5fb86f227cf7693bff12b63647377e72571dc98c2dd0b6a7d76d81' ;; 		aarch64) binArch='arm64'; checksum='8d9d873e701ab2dfe6046c5f6a9bbd19dd2aef7e4c57640c897e70cc5d2775353f0c467779e2fba4c024c9de89d2b1d64c1b46568dda65e6f5a114f13b239c6d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='30248cca16ec07e1e9aee0dabaaf0959f2f3622aafbdd9dac9135a4f2117ca3cc5b5bbfb8c94d45ea2c1abf61840587885f2db7fec420cd00918819cd39bfc92' ;; 		s390x)   binArch='s390x'; checksum='f4e16ad4f03f13cbe463efb8577d99f22a30161916cde10f5a0c838f7c57022b572b9a18d25fb20925aef4a5366537948ffdd4a191b3d5205ab9ab980406ca4b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 30 Jun 2020 23:41:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Jun 2020 23:41:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 30 Jun 2020 23:41:34 GMT
ENV XDG_DATA_HOME=/data
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/config]
# Tue, 30 Jun 2020 23:41:34 GMT
VOLUME [/data]
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Tue, 30 Jun 2020 23:41:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 30 Jun 2020 23:41:36 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 30 Jun 2020 23:41:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 30 Jun 2020 23:41:38 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 80
# Tue, 30 Jun 2020 23:41:38 GMT
EXPOSE 443
# Tue, 30 Jun 2020 23:41:39 GMT
EXPOSE 2019
# Tue, 30 Jun 2020 23:41:39 GMT
WORKDIR /srv
# Tue, 30 Jun 2020 23:41:40 GMT
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
	-	`sha256:bf084f3ceb3b3b1196400fa251cc45e01de7ece41b7605bb40ae5178d849b47d`  
		Last Modified: Mon, 15 Jun 2020 20:44:26 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a74ac154ef35abae9974398394ecc94fe54ad18af49231bc6a337fc43346c5`  
		Last Modified: Tue, 30 Jun 2020 23:42:46 GMT  
		Size: 12.8 MB (12836780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5673e745c5f3d1ac989f1a9cc90e301eb65e6dec0d3875d0480300738a959f32`  
		Last Modified: Tue, 30 Jun 2020 23:42:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:40c4f77513048ee7e05ee01fb89d360e22b13325c3daaffca57dee62c72b575d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64
	-	windows version 10.0.14393.3930; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:54fc1c11a9a4de45c0e3b30aa2702ac0e55d355cd47e3f7f4fbfdc475bc6c132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull caddy@sha256:6fdda8066ebb2cfcbb65432af3efad7ecef7f89d4b5a2e0b325692d95ea4e3b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2378390339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a3b078a6f6a6627a26f04efe9831b83aa9ce0bbb6249c8b0f92d7a50881c02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 19:53:27 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 19:54:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 19:54:05 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 19:54:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 19:54:36 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 19:54:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 19:54:38 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 19:54:39 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 19:54:40 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 19:54:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 19:54:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 19:54:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 19:54:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 19:54:45 GMT
EXPOSE 80
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 443
# Wed, 09 Sep 2020 19:54:46 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:25:17 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:25:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c325b871c49357c593876a98f079c074af004dee2cb9cf372880b2cd25fd6a0c`  
		Last Modified: Wed, 09 Sep 2020 20:29:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5eb7f2e0263c6213fc9423cf6eb719de3f7c849643ccdabec913b618f41ad`  
		Last Modified: Wed, 09 Sep 2020 20:29:39 GMT  
		Size: 9.1 MB (9137985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a77a42e4acde519b57884bb795f3dc263fa0169242832aa756ec95c04dddd`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ef31d9b01fa7c0d2d8b5dc3eb4d389001034b74d7d472cc951df62d115118`  
		Last Modified: Wed, 09 Sep 2020 20:29:48 GMT  
		Size: 17.7 MB (17672633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a7d301d80ee07b021c74d836eb43352e05ce53a3480b8d9e24d99186bbfbf`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0770a21ef08a40302425e6476fe8c78962bc91e1f2e01ce71d58b44d1eec27ff`  
		Last Modified: Wed, 09 Sep 2020 20:29:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74371eb56f1a9b6b6e10b2915999a33587eecd4cf57dc6442471c378718c1062`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3517d1abc56a70595cf5ae149a9f2843e8fa9eaa2c2f3c9e793cacc8e117dc3`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bf115547c84fde7026e799220c3a33867058af6f6b469f7f6cad4fb501342`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ba56b6ad310ca4acd04b36bab15c11509edd717eacc8a7a31c575becf2e58c`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e5887ab35d7d9526248c8ba42cd34560054c2eda04112f03bbb2c7051df82`  
		Last Modified: Wed, 09 Sep 2020 20:29:26 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced70216aec7f6562500c53e1cb318c4f5fbd754b45dfd4778796eddcc3f44bf`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d064b47540d3a0413e187206009b7420d041bc2abe86a2bdb159421da8a76e63`  
		Last Modified: Wed, 09 Sep 2020 20:29:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370539f66a716c49521cd612333716543831af692859d7406721cef7ac87476d`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c29ac445b054afa01e8bd41bdb11ba36d5af91e515aaf7abe5a6a156d838b4`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173743838549e9d6d35bf843fd1d0d578b7ff6f4353e4e14c9b62ac16d750efb`  
		Last Modified: Wed, 09 Sep 2020 20:29:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2116539be5612b7b677cc16f59fd8f7268ad3b1bea415498c4b31c99e1ca4565`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaed27ebe4f3042ae55963898c25ebf1f39d9e362ba02b80ddcefd0f40f3146`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc079d30d61f51e726e25d5f65fad824d0749aefa98e25d25b1562b8785c753`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f7fdcbced701ca09049814e389bdab25b50586d869b3191093f5e9066efcd0`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 285.9 KB (285915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2630294809bc2c1fcd1b1976547723b64c5e7ed91f008f6f7ef23c871474a7fa`  
		Last Modified: Wed, 09 Sep 2020 20:29:21 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:deb60a2701067b98424a7cc203f79a61a9f41d6b772df3b6c0ba34236cce1c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3930; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.3930; amd64

```console
$ docker pull caddy@sha256:c399072135a67ae1bf41ddf60b732de7e9d1513000021162c25f1a1471c07f95
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5772293185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb680f013a85014fccf399ba08c16d449ca381f1a5154276bc2b49470ac8f942`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Sep 2020 20:25:23 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 09 Sep 2020 20:26:37 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Sep 2020 20:26:38 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 09 Sep 2020 20:28:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Sep 2020 20:28:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Sep 2020 20:28:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Sep 2020 20:28:03 GMT
VOLUME [c:/config]
# Wed, 09 Sep 2020 20:28:04 GMT
VOLUME [c:/data]
# Wed, 09 Sep 2020 20:28:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 09 Sep 2020 20:28:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Sep 2020 20:28:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Sep 2020 20:28:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Sep 2020 20:28:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Sep 2020 20:28:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Sep 2020 20:28:11 GMT
EXPOSE 80
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 443
# Wed, 09 Sep 2020 20:28:12 GMT
EXPOSE 2019
# Wed, 09 Sep 2020 20:28:52 GMT
RUN caddy version
# Wed, 09 Sep 2020 20:28:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a449faf0a811f283e675b95675b755ed5caeaf09c377b034b4730f6451aa51`  
		Last Modified: Wed, 09 Sep 2020 20:30:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3226e2cab68073e9c97dacb0b90ecf5fec0142f1690d3ce6268fbe7236afc5`  
		Last Modified: Wed, 09 Sep 2020 20:30:24 GMT  
		Size: 9.9 MB (9897398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761d232ac4fd149d90e5347a5bd38a319bfb55a301c1a111b6503356911322b8`  
		Last Modified: Wed, 09 Sep 2020 20:30:13 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c767daadf962c116a6b9c0a3515446a8b285066125527c4222daf121a40a2ad7`  
		Last Modified: Wed, 09 Sep 2020 20:30:18 GMT  
		Size: 22.9 MB (22872196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b987d95380ab88f45603aaaed62a622130e9e3fdfaf920f4f75bce40bae1a635`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d802d13151eefdd188af28474ad33dc2a1c63c9403c1ed769da6d40b0e54a806`  
		Last Modified: Wed, 09 Sep 2020 20:30:12 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26007a9ef743163079afd033ec88dc054a50a1691ceb86abf06c3027fb4e5960`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42df9545735b7e2fd0e54384a7d867cb94d15f421965a72064960cd7b8884700`  
		Last Modified: Wed, 09 Sep 2020 20:30:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91bd9d5351e7b6f497b9506e976a1e9a722f4c1e3a99e8a476e1a7bda5fd3f4`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fdc70bbab6bb9610494fc861f433042c460157a65717802379ddf4da12e81e`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b663a9f158ac2229e071d383cec9f621fd28f6b0652215f5b4b4450b58dc68a1`  
		Last Modified: Wed, 09 Sep 2020 20:30:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a243df49719e70d6a15b261449414bc069ffdd04a552563e129e402e3cc129`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8f5da7ba33566df13bc15bfa47c970f50f27d4a373e0ad2085ff6435ffb4`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05d556209c77456fc89bd1484059081409259c5946aa6fc367179ceaca4674d`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1f5c7e3672363102592a251895dd3aebe3b1ffb623b0b03712525571abf474`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deca8290b7668c1e16e216ed2040490186e8013ee60f992ab46347e92ccfde5`  
		Last Modified: Wed, 09 Sep 2020 20:30:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713887e22bbfa9481da702fba31404d11d79a9952c0ba63e8db952c7ab063b6d`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087dd32d3c1a6a7665699ccc8a08848a94b90c86b352804c29de30be754c7508`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202c220609d5cf8ed133c56b31a32168cf749346cdd1453edc215f62cd09a8f`  
		Last Modified: Wed, 09 Sep 2020 20:30:05 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0823fb990936970db69fcf021f5cf762bcf64bf24669f09449c6f578ddd6f2`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 247.5 KB (247496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51024f33e212313a4c9be7fb692bf2a599f8b8095c80c62127268d4ce704d3`  
		Last Modified: Wed, 09 Sep 2020 20:30:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
