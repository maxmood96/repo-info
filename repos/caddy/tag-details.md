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
$ docker pull caddy@sha256:b1d5080ca3217345d121fc8b87d3a0253dfacfad698a7495b6814531849f1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

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

### `caddy:2` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1`

```console
$ docker pull caddy@sha256:b1d5080ca3217345d121fc8b87d3a0253dfacfad698a7495b6814531849f1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

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

### `caddy:2.1.1` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
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
$ docker pull caddy@sha256:35a8ba2cfa316ae8b172928803e59b7b08409e76c661060e150e833d70d45d4a
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
$ docker pull caddy@sha256:e36b8ed5c449779e0a1fa9ece869a502a844a21d3c246bec3c64f54e494ea80b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331168382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4952a0e367e3902096934f29eabb3b40146d64aaabfc533b08ec7df4295b681d`
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
# Fri, 17 Jul 2020 02:20:31 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:22:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:22:45 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:22:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:22:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:22:46 GMT
WORKDIR /go
# Fri, 17 Jul 2020 02:50:22 GMT
WORKDIR /src
# Fri, 17 Jul 2020 02:50:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 02:50:24 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 02:50:26 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 02:50:26 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 02:50:49 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 02:50:51 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 02:50:51 GMT
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
	-	`sha256:00abe362642d012af91b6be6c49d92940b67166682973d33b494ba7ded5a635a`  
		Last Modified: Fri, 17 Jul 2020 02:32:28 GMT  
		Size: 132.5 MB (132524788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0491c15e88ffef3bb5af8af7ac5aea412adb85ab1632b2bb89179132304df81`  
		Last Modified: Fri, 17 Jul 2020 02:32:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ab277974210fa40d65f8a717b614476cf2a00b95f1615f95af605e6dc8752a`  
		Last Modified: Fri, 17 Jul 2020 02:51:07 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ea3544be42ca4bacfead93d01b33949cc5729af5b7b16e5a2304561f2c4c6e`  
		Last Modified: Fri, 17 Jul 2020 02:51:08 GMT  
		Size: 8.3 MB (8310030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb55020dfbb96ed86536d3f3ee4cfe5d65c31fd943b084fb98411b1441c0a60`  
		Last Modified: Fri, 17 Jul 2020 02:51:06 GMT  
		Size: 3.0 MB (3020915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cb4727040aafcb55500dc13aab52d4a34221462584428f46c21e41bc086495`  
		Last Modified: Fri, 17 Jul 2020 02:51:37 GMT  
		Size: 184.2 MB (184231468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd2f1035f3378ab0ca666ecef614fb9ce84c8374e6c48849db241bf74d92f7`  
		Last Modified: Fri, 17 Jul 2020 02:51:05 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74308353d5e0db8661ab6a54f64c651aaa60c78e229fdd8855c7514dccf02eed`  
		Last Modified: Fri, 17 Jul 2020 02:51:06 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e0108d6b5812a3ead483a1dffc0ec600842f814ac81c8a1fc83bb89d99cbf7b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326674956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77cd9702b19785ac8f4126e9952c281df59e96592d11b58d412b91569024ab8`
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
# Tue, 14 Jul 2020 18:49:40 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 19:53:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 19:53:10 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 19:53:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 19:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 19:53:13 GMT
WORKDIR /go
# Tue, 14 Jul 2020 23:03:34 GMT
WORKDIR /src
# Tue, 14 Jul 2020 23:03:37 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 23:03:37 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 23:03:40 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 23:03:41 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 23:04:59 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 23:05:08 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 23:05:09 GMT
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
	-	`sha256:d6734511f5453510f789a8f7ea169069aeecf283185971411bd89d51922e664d`  
		Last Modified: Tue, 14 Jul 2020 22:45:39 GMT  
		Size: 128.6 MB (128598150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ee9318de4a795497843fc620410e8d6a98a1d19fbab73e68dcf95383d4a1f6`  
		Last Modified: Tue, 14 Jul 2020 22:45:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947232530c9fc7196e07fd4bb0cba9181daba56e2b40f99efa5c2c2d4a9efeca`  
		Last Modified: Tue, 14 Jul 2020 23:05:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13f7e40a2b5637113854a0f561473128d51495cc514ec4bacd36135a4566d3`  
		Last Modified: Tue, 14 Jul 2020 23:05:33 GMT  
		Size: 7.9 MB (7928849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5a9cfd6c38fce2c59e1623fe46b06d86440ed1668550c0db2ed0538449c316`  
		Last Modified: Tue, 14 Jul 2020 23:05:31 GMT  
		Size: 3.0 MB (3021030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61dc12432928c24532ce9ab7ee77d48fe2d76b9c57465491e73a3400d90b869`  
		Last Modified: Tue, 14 Jul 2020 23:06:15 GMT  
		Size: 184.2 MB (184239735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1390e4f7366d2946949fbc5da93c1e1e7b23ebfb33f9e3cb73a4371fb7027a`  
		Last Modified: Tue, 14 Jul 2020 23:05:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f2efe06b095053a12efa6f412a9b7a24da04c03bc58de9b14cc812f21fd2c5`  
		Last Modified: Tue, 14 Jul 2020 23:05:30 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6160b3382be3fa17b2bd5fc460b54a0679f0d0da6329b3849b3830130d396808
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325279166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa11268e132afb3f8db4e8968f0f61eda85f31035ddbc4445d2df757b056ac49`
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
# Tue, 14 Jul 2020 17:59:05 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 18:02:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 18:02:50 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 18:02:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 18:02:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 18:02:54 GMT
WORKDIR /go
# Tue, 14 Jul 2020 18:56:35 GMT
WORKDIR /src
# Tue, 14 Jul 2020 18:58:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 18:58:16 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 18:59:12 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 18:59:25 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 19:01:30 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 19:01:41 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 19:01:54 GMT
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
	-	`sha256:d6f82be5bf601cf8b3ce3831f415f8e4057942f012533eaff2a58504716e691a`  
		Last Modified: Tue, 14 Jul 2020 18:36:34 GMT  
		Size: 128.2 MB (128182109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba0c03e33b6ad6744dd6d0d95b528b643575969ef43d8ee7ed376c414852d6e`  
		Last Modified: Tue, 14 Jul 2020 18:35:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fc53d02f1b9139c39820bc6e987afeeb05c8771bbd857f29250bb964c27e9f`  
		Last Modified: Tue, 14 Jul 2020 19:02:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b25dac59cc9b0ea27059634cec097482636f01af1d7a844bf8a539f7fb2cf6`  
		Last Modified: Tue, 14 Jul 2020 19:02:22 GMT  
		Size: 7.1 MB (7144964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9886a84420be869be028a4ad927a6feceed4326d5a2185305023462496e44a22`  
		Last Modified: Tue, 14 Jul 2020 19:02:21 GMT  
		Size: 3.0 MB (3022770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee58a591970022dc8e292299bb78a6adca590e98417d91b36dabd8da154082c7`  
		Last Modified: Tue, 14 Jul 2020 19:03:15 GMT  
		Size: 184.2 MB (184239539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deee7fad20b8615c78c92a371c22e5ceb4a2e13e0aa7bd54aab2d9b49a8d478a`  
		Last Modified: Tue, 14 Jul 2020 19:02:21 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb0d7cb5d89f97627a2ae70d17e08b04d7e3ee1796e28e72894663184d3407`  
		Last Modified: Tue, 14 Jul 2020 19:02:21 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ae8b3b35d51c1eb448fccb525964b83f45401f9742b328eeb66eb511abb1bb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325648497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c92347766e3850b34fbdea8a715e307dc87c8ac2a2eacbcdf1d4c921b24418`
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
# Tue, 14 Jul 2020 18:41:29 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 18:43:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 18:43:50 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 18:43:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 18:43:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 18:43:53 GMT
WORKDIR /go
# Tue, 14 Jul 2020 19:20:52 GMT
WORKDIR /src
# Tue, 14 Jul 2020 19:21:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 19:21:13 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 19:21:49 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 19:21:58 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 19:23:26 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 19:23:37 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 19:23:50 GMT
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
	-	`sha256:92485ad5f2d3ea346a9b9c8bc5ecad8f5a7bd7307627c7eb9c028542d031c3c4`  
		Last Modified: Tue, 14 Jul 2020 19:01:08 GMT  
		Size: 126.9 MB (126893488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2de403c7edbdeb533ddf9de0f77d34967e0732a96718383ce14a94fda9a90c`  
		Last Modified: Tue, 14 Jul 2020 19:00:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798190983ee3217a79f307281f44856700c35522303a90a8919381bf7966ad09`  
		Last Modified: Tue, 14 Jul 2020 19:24:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33545d8fa9bbce0d09f720f2782c78861559dfacabbee8fb8d0dc0ba51cc401`  
		Last Modified: Tue, 14 Jul 2020 19:24:20 GMT  
		Size: 8.5 MB (8499921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22da6d889ac1af3ab3c92fc98fa5734b13a7ee8cae9c8fc0b5c6fcca0a9d4d96`  
		Last Modified: Tue, 14 Jul 2020 19:24:20 GMT  
		Size: 3.0 MB (3024185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4881453df79bdef3e280c2107fbd7adf7c0afe2613b4d4b7aba2556f9dbdc569`  
		Last Modified: Tue, 14 Jul 2020 19:25:02 GMT  
		Size: 184.2 MB (184238813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ba8dca3508d488fac5d42462196c64c861bf4a3ca5759237a44d7cd25f5c55`  
		Last Modified: Tue, 14 Jul 2020 19:24:19 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c649979b913b0bbcf906f4cad6d628821c19a7980077599e9fb513ed67aaae`  
		Last Modified: Tue, 14 Jul 2020 19:24:19 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:6f0d7c9bb84c51ed939efb13e3bf6ca9446d49b9d6f85958f0fb138de6a5c564
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324933638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833092067ee129e61a268dd93d22ceb73687f1de1cecd5e0df72bcda02dc5426`
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
# Fri, 17 Jul 2020 02:21:44 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:24:14 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:24:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:24:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:24:36 GMT
WORKDIR /go
# Fri, 17 Jul 2020 03:12:38 GMT
WORKDIR /src
# Fri, 17 Jul 2020 03:12:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 03:13:07 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 03:13:21 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 03:13:28 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 03:18:29 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 03:18:37 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 03:18:43 GMT
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
	-	`sha256:869ed739838c69d7e160dc1ff1fdd2300d17b52ee5d67aee493ca90d9b4fbd68`  
		Last Modified: Fri, 17 Jul 2020 02:45:38 GMT  
		Size: 125.7 MB (125656430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a61d3270248636b8a3f7205c3beff887ef7d4e2d403236b40d966e78b436f3`  
		Last Modified: Fri, 17 Jul 2020 02:43:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b42d4c77523f2d142783f55bea8336f93ff2cffd130887ca26938de15e3f7f`  
		Last Modified: Fri, 17 Jul 2020 03:19:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d23037bff9becbc5cea0824bae9147c00c87e29b5e83f2d3d3731d4542a3822`  
		Last Modified: Fri, 17 Jul 2020 03:19:09 GMT  
		Size: 8.9 MB (8920009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5927740889cdf47f4a17ea13d4bb5a9f5afca616c3c80b149e904f384b88bc64`  
		Last Modified: Fri, 17 Jul 2020 03:19:07 GMT  
		Size: 3.0 MB (3021040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa038742c660b74c276241553dd0dad4ad3ac9e8ad93d193a4c69258f93dff42`  
		Last Modified: Fri, 17 Jul 2020 03:19:34 GMT  
		Size: 184.2 MB (184244796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8514849ad61d3a9e0d21db033cc533db85e018c56ff97450ab8c55cfb2edca7e`  
		Last Modified: Fri, 17 Jul 2020 03:19:06 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75180876e9c63f9f97d6b4c520adaf9fe6fbfb5b935515aec347dbba6d8aa0c0`  
		Last Modified: Fri, 17 Jul 2020 03:19:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:6330b0180c606a640045d73f471239638e0082e1ac3de2ce2e799608b1403cff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330732719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2744f7b60057c0c75e28371bfa6b50008bd9abfe4ce40e894258ec0fe5dfa00`
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
# Fri, 17 Jul 2020 02:42:46 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:44:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:44:13 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:44:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:44:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:44:14 GMT
WORKDIR /go
# Fri, 17 Jul 2020 03:09:23 GMT
WORKDIR /src
# Fri, 17 Jul 2020 03:09:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 03:09:27 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 03:09:29 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 03:09:30 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 03:10:20 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 03:10:41 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 03:10:42 GMT
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
	-	`sha256:561add13be46fdce5a695d1ca8906ad50a90e3d3d25d47e1ad2c8478537bc445`  
		Last Modified: Fri, 17 Jul 2020 02:51:38 GMT  
		Size: 132.3 MB (132268907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f72d70911ac3c6bbdf16aa3d58a6bbe08cf171406e75d7dbf84c7ffd219073`  
		Last Modified: Fri, 17 Jul 2020 02:51:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38e21bb7fac2484df2339b1be77584264518b7a0dcb878869e6fade02cd7a2e`  
		Last Modified: Fri, 17 Jul 2020 03:11:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a5388655ece15f0d53ad7c41a2cdde6c25eab31b939efbe1eb3aa76c0279b3`  
		Last Modified: Fri, 17 Jul 2020 03:11:07 GMT  
		Size: 8.4 MB (8352234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4c55d0a142dc8b432c7f402cedd62737abb5d83f72caf89a1b0bed0066c6be`  
		Last Modified: Fri, 17 Jul 2020 03:11:11 GMT  
		Size: 3.0 MB (3024180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a5905cbf69b78060dd069e31cdabd5ee3a08eefaa57bc455415b85929755ac`  
		Last Modified: Fri, 17 Jul 2020 03:11:23 GMT  
		Size: 184.2 MB (184236938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af024d101834697f989a8213e8472351a541b76397f2be2fd6cdf79bef5292a8`  
		Last Modified: Fri, 17 Jul 2020 03:11:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7dbf6babd157dfc3f807bef9a82ac255c5c1c471919c8578aa0a4626d5f834`  
		Last Modified: Fri, 17 Jul 2020 03:11:36 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-windowsservercore`

```console
$ docker pull caddy@sha256:c69acf82737ac04895de0fe82b6460bf07cbb49ba46a3b50df15e1210d7630bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

### `caddy:2.1.1-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.1.1-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-windowsservercore-1809`

```console
$ docker pull caddy@sha256:eac1adaea9ec4c19a0a1b6fae6187b72828c250ddb7945b39bd1e9d33fb71344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `caddy:2.1.1-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.1.1-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:3f88aabc0b2d55a45411b9751f8115fabcb2f3287a98bbaee17a9ff00a314b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `caddy:2.1.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
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
$ docker pull caddy@sha256:35a8ba2cfa316ae8b172928803e59b7b08409e76c661060e150e833d70d45d4a
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
$ docker pull caddy@sha256:e36b8ed5c449779e0a1fa9ece869a502a844a21d3c246bec3c64f54e494ea80b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331168382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4952a0e367e3902096934f29eabb3b40146d64aaabfc533b08ec7df4295b681d`
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
# Fri, 17 Jul 2020 02:20:31 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:22:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:22:45 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:22:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:22:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:22:46 GMT
WORKDIR /go
# Fri, 17 Jul 2020 02:50:22 GMT
WORKDIR /src
# Fri, 17 Jul 2020 02:50:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 02:50:24 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 02:50:26 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 02:50:26 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 02:50:49 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 02:50:51 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 02:50:51 GMT
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
	-	`sha256:00abe362642d012af91b6be6c49d92940b67166682973d33b494ba7ded5a635a`  
		Last Modified: Fri, 17 Jul 2020 02:32:28 GMT  
		Size: 132.5 MB (132524788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0491c15e88ffef3bb5af8af7ac5aea412adb85ab1632b2bb89179132304df81`  
		Last Modified: Fri, 17 Jul 2020 02:32:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ab277974210fa40d65f8a717b614476cf2a00b95f1615f95af605e6dc8752a`  
		Last Modified: Fri, 17 Jul 2020 02:51:07 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ea3544be42ca4bacfead93d01b33949cc5729af5b7b16e5a2304561f2c4c6e`  
		Last Modified: Fri, 17 Jul 2020 02:51:08 GMT  
		Size: 8.3 MB (8310030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb55020dfbb96ed86536d3f3ee4cfe5d65c31fd943b084fb98411b1441c0a60`  
		Last Modified: Fri, 17 Jul 2020 02:51:06 GMT  
		Size: 3.0 MB (3020915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cb4727040aafcb55500dc13aab52d4a34221462584428f46c21e41bc086495`  
		Last Modified: Fri, 17 Jul 2020 02:51:37 GMT  
		Size: 184.2 MB (184231468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd2f1035f3378ab0ca666ecef614fb9ce84c8374e6c48849db241bf74d92f7`  
		Last Modified: Fri, 17 Jul 2020 02:51:05 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74308353d5e0db8661ab6a54f64c651aaa60c78e229fdd8855c7514dccf02eed`  
		Last Modified: Fri, 17 Jul 2020 02:51:06 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e0108d6b5812a3ead483a1dffc0ec600842f814ac81c8a1fc83bb89d99cbf7b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326674956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77cd9702b19785ac8f4126e9952c281df59e96592d11b58d412b91569024ab8`
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
# Tue, 14 Jul 2020 18:49:40 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 19:53:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 19:53:10 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 19:53:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 19:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 19:53:13 GMT
WORKDIR /go
# Tue, 14 Jul 2020 23:03:34 GMT
WORKDIR /src
# Tue, 14 Jul 2020 23:03:37 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 23:03:37 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 23:03:40 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 23:03:41 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 23:04:59 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 23:05:08 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 23:05:09 GMT
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
	-	`sha256:d6734511f5453510f789a8f7ea169069aeecf283185971411bd89d51922e664d`  
		Last Modified: Tue, 14 Jul 2020 22:45:39 GMT  
		Size: 128.6 MB (128598150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ee9318de4a795497843fc620410e8d6a98a1d19fbab73e68dcf95383d4a1f6`  
		Last Modified: Tue, 14 Jul 2020 22:45:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947232530c9fc7196e07fd4bb0cba9181daba56e2b40f99efa5c2c2d4a9efeca`  
		Last Modified: Tue, 14 Jul 2020 23:05:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13f7e40a2b5637113854a0f561473128d51495cc514ec4bacd36135a4566d3`  
		Last Modified: Tue, 14 Jul 2020 23:05:33 GMT  
		Size: 7.9 MB (7928849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5a9cfd6c38fce2c59e1623fe46b06d86440ed1668550c0db2ed0538449c316`  
		Last Modified: Tue, 14 Jul 2020 23:05:31 GMT  
		Size: 3.0 MB (3021030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61dc12432928c24532ce9ab7ee77d48fe2d76b9c57465491e73a3400d90b869`  
		Last Modified: Tue, 14 Jul 2020 23:06:15 GMT  
		Size: 184.2 MB (184239735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1390e4f7366d2946949fbc5da93c1e1e7b23ebfb33f9e3cb73a4371fb7027a`  
		Last Modified: Tue, 14 Jul 2020 23:05:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f2efe06b095053a12efa6f412a9b7a24da04c03bc58de9b14cc812f21fd2c5`  
		Last Modified: Tue, 14 Jul 2020 23:05:30 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6160b3382be3fa17b2bd5fc460b54a0679f0d0da6329b3849b3830130d396808
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325279166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa11268e132afb3f8db4e8968f0f61eda85f31035ddbc4445d2df757b056ac49`
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
# Tue, 14 Jul 2020 17:59:05 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 18:02:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 18:02:50 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 18:02:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 18:02:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 18:02:54 GMT
WORKDIR /go
# Tue, 14 Jul 2020 18:56:35 GMT
WORKDIR /src
# Tue, 14 Jul 2020 18:58:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 18:58:16 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 18:59:12 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 18:59:25 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 19:01:30 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 19:01:41 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 19:01:54 GMT
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
	-	`sha256:d6f82be5bf601cf8b3ce3831f415f8e4057942f012533eaff2a58504716e691a`  
		Last Modified: Tue, 14 Jul 2020 18:36:34 GMT  
		Size: 128.2 MB (128182109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba0c03e33b6ad6744dd6d0d95b528b643575969ef43d8ee7ed376c414852d6e`  
		Last Modified: Tue, 14 Jul 2020 18:35:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fc53d02f1b9139c39820bc6e987afeeb05c8771bbd857f29250bb964c27e9f`  
		Last Modified: Tue, 14 Jul 2020 19:02:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b25dac59cc9b0ea27059634cec097482636f01af1d7a844bf8a539f7fb2cf6`  
		Last Modified: Tue, 14 Jul 2020 19:02:22 GMT  
		Size: 7.1 MB (7144964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9886a84420be869be028a4ad927a6feceed4326d5a2185305023462496e44a22`  
		Last Modified: Tue, 14 Jul 2020 19:02:21 GMT  
		Size: 3.0 MB (3022770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee58a591970022dc8e292299bb78a6adca590e98417d91b36dabd8da154082c7`  
		Last Modified: Tue, 14 Jul 2020 19:03:15 GMT  
		Size: 184.2 MB (184239539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deee7fad20b8615c78c92a371c22e5ceb4a2e13e0aa7bd54aab2d9b49a8d478a`  
		Last Modified: Tue, 14 Jul 2020 19:02:21 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb0d7cb5d89f97627a2ae70d17e08b04d7e3ee1796e28e72894663184d3407`  
		Last Modified: Tue, 14 Jul 2020 19:02:21 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ae8b3b35d51c1eb448fccb525964b83f45401f9742b328eeb66eb511abb1bb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325648497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c92347766e3850b34fbdea8a715e307dc87c8ac2a2eacbcdf1d4c921b24418`
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
# Tue, 14 Jul 2020 18:41:29 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 18:43:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 18:43:50 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 18:43:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 18:43:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 18:43:53 GMT
WORKDIR /go
# Tue, 14 Jul 2020 19:20:52 GMT
WORKDIR /src
# Tue, 14 Jul 2020 19:21:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 19:21:13 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 19:21:49 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 19:21:58 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 19:23:26 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 19:23:37 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 19:23:50 GMT
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
	-	`sha256:92485ad5f2d3ea346a9b9c8bc5ecad8f5a7bd7307627c7eb9c028542d031c3c4`  
		Last Modified: Tue, 14 Jul 2020 19:01:08 GMT  
		Size: 126.9 MB (126893488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2de403c7edbdeb533ddf9de0f77d34967e0732a96718383ce14a94fda9a90c`  
		Last Modified: Tue, 14 Jul 2020 19:00:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798190983ee3217a79f307281f44856700c35522303a90a8919381bf7966ad09`  
		Last Modified: Tue, 14 Jul 2020 19:24:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33545d8fa9bbce0d09f720f2782c78861559dfacabbee8fb8d0dc0ba51cc401`  
		Last Modified: Tue, 14 Jul 2020 19:24:20 GMT  
		Size: 8.5 MB (8499921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22da6d889ac1af3ab3c92fc98fa5734b13a7ee8cae9c8fc0b5c6fcca0a9d4d96`  
		Last Modified: Tue, 14 Jul 2020 19:24:20 GMT  
		Size: 3.0 MB (3024185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4881453df79bdef3e280c2107fbd7adf7c0afe2613b4d4b7aba2556f9dbdc569`  
		Last Modified: Tue, 14 Jul 2020 19:25:02 GMT  
		Size: 184.2 MB (184238813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ba8dca3508d488fac5d42462196c64c861bf4a3ca5759237a44d7cd25f5c55`  
		Last Modified: Tue, 14 Jul 2020 19:24:19 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c649979b913b0bbcf906f4cad6d628821c19a7980077599e9fb513ed67aaae`  
		Last Modified: Tue, 14 Jul 2020 19:24:19 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:6f0d7c9bb84c51ed939efb13e3bf6ca9446d49b9d6f85958f0fb138de6a5c564
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324933638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833092067ee129e61a268dd93d22ceb73687f1de1cecd5e0df72bcda02dc5426`
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
# Fri, 17 Jul 2020 02:21:44 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:24:14 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:24:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:24:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:24:36 GMT
WORKDIR /go
# Fri, 17 Jul 2020 03:12:38 GMT
WORKDIR /src
# Fri, 17 Jul 2020 03:12:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 03:13:07 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 03:13:21 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 03:13:28 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 03:18:29 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 03:18:37 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 03:18:43 GMT
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
	-	`sha256:869ed739838c69d7e160dc1ff1fdd2300d17b52ee5d67aee493ca90d9b4fbd68`  
		Last Modified: Fri, 17 Jul 2020 02:45:38 GMT  
		Size: 125.7 MB (125656430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a61d3270248636b8a3f7205c3beff887ef7d4e2d403236b40d966e78b436f3`  
		Last Modified: Fri, 17 Jul 2020 02:43:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b42d4c77523f2d142783f55bea8336f93ff2cffd130887ca26938de15e3f7f`  
		Last Modified: Fri, 17 Jul 2020 03:19:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d23037bff9becbc5cea0824bae9147c00c87e29b5e83f2d3d3731d4542a3822`  
		Last Modified: Fri, 17 Jul 2020 03:19:09 GMT  
		Size: 8.9 MB (8920009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5927740889cdf47f4a17ea13d4bb5a9f5afca616c3c80b149e904f384b88bc64`  
		Last Modified: Fri, 17 Jul 2020 03:19:07 GMT  
		Size: 3.0 MB (3021040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa038742c660b74c276241553dd0dad4ad3ac9e8ad93d193a4c69258f93dff42`  
		Last Modified: Fri, 17 Jul 2020 03:19:34 GMT  
		Size: 184.2 MB (184244796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8514849ad61d3a9e0d21db033cc533db85e018c56ff97450ab8c55cfb2edca7e`  
		Last Modified: Fri, 17 Jul 2020 03:19:06 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75180876e9c63f9f97d6b4c520adaf9fe6fbfb5b935515aec347dbba6d8aa0c0`  
		Last Modified: Fri, 17 Jul 2020 03:19:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:6330b0180c606a640045d73f471239638e0082e1ac3de2ce2e799608b1403cff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330732719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2744f7b60057c0c75e28371bfa6b50008bd9abfe4ce40e894258ec0fe5dfa00`
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
# Fri, 17 Jul 2020 02:42:46 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:44:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:44:13 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:44:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:44:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:44:14 GMT
WORKDIR /go
# Fri, 17 Jul 2020 03:09:23 GMT
WORKDIR /src
# Fri, 17 Jul 2020 03:09:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 03:09:27 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 03:09:29 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 03:09:30 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 03:10:20 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 03:10:41 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 03:10:42 GMT
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
	-	`sha256:561add13be46fdce5a695d1ca8906ad50a90e3d3d25d47e1ad2c8478537bc445`  
		Last Modified: Fri, 17 Jul 2020 02:51:38 GMT  
		Size: 132.3 MB (132268907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f72d70911ac3c6bbdf16aa3d58a6bbe08cf171406e75d7dbf84c7ffd219073`  
		Last Modified: Fri, 17 Jul 2020 02:51:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38e21bb7fac2484df2339b1be77584264518b7a0dcb878869e6fade02cd7a2e`  
		Last Modified: Fri, 17 Jul 2020 03:11:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a5388655ece15f0d53ad7c41a2cdde6c25eab31b939efbe1eb3aa76c0279b3`  
		Last Modified: Fri, 17 Jul 2020 03:11:07 GMT  
		Size: 8.4 MB (8352234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4c55d0a142dc8b432c7f402cedd62737abb5d83f72caf89a1b0bed0066c6be`  
		Last Modified: Fri, 17 Jul 2020 03:11:11 GMT  
		Size: 3.0 MB (3024180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a5905cbf69b78060dd069e31cdabd5ee3a08eefaa57bc455415b85929755ac`  
		Last Modified: Fri, 17 Jul 2020 03:11:23 GMT  
		Size: 184.2 MB (184236938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af024d101834697f989a8213e8472351a541b76397f2be2fd6cdf79bef5292a8`  
		Last Modified: Fri, 17 Jul 2020 03:11:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7dbf6babd157dfc3f807bef9a82ac255c5c1c471919c8578aa0a4626d5f834`  
		Last Modified: Fri, 17 Jul 2020 03:11:36 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:c69acf82737ac04895de0fe82b6460bf07cbb49ba46a3b50df15e1210d7630bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:eac1adaea9ec4c19a0a1b6fae6187b72828c250ddb7945b39bd1e9d33fb71344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:3f88aabc0b2d55a45411b9751f8115fabcb2f3287a98bbaee17a9ff00a314b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
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
$ docker pull caddy@sha256:35a8ba2cfa316ae8b172928803e59b7b08409e76c661060e150e833d70d45d4a
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
$ docker pull caddy@sha256:e36b8ed5c449779e0a1fa9ece869a502a844a21d3c246bec3c64f54e494ea80b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331168382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4952a0e367e3902096934f29eabb3b40146d64aaabfc533b08ec7df4295b681d`
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
# Fri, 17 Jul 2020 02:20:31 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:22:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:22:45 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:22:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:22:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:22:46 GMT
WORKDIR /go
# Fri, 17 Jul 2020 02:50:22 GMT
WORKDIR /src
# Fri, 17 Jul 2020 02:50:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 02:50:24 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 02:50:26 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 02:50:26 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 02:50:49 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 02:50:51 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 02:50:51 GMT
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
	-	`sha256:00abe362642d012af91b6be6c49d92940b67166682973d33b494ba7ded5a635a`  
		Last Modified: Fri, 17 Jul 2020 02:32:28 GMT  
		Size: 132.5 MB (132524788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0491c15e88ffef3bb5af8af7ac5aea412adb85ab1632b2bb89179132304df81`  
		Last Modified: Fri, 17 Jul 2020 02:32:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ab277974210fa40d65f8a717b614476cf2a00b95f1615f95af605e6dc8752a`  
		Last Modified: Fri, 17 Jul 2020 02:51:07 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ea3544be42ca4bacfead93d01b33949cc5729af5b7b16e5a2304561f2c4c6e`  
		Last Modified: Fri, 17 Jul 2020 02:51:08 GMT  
		Size: 8.3 MB (8310030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb55020dfbb96ed86536d3f3ee4cfe5d65c31fd943b084fb98411b1441c0a60`  
		Last Modified: Fri, 17 Jul 2020 02:51:06 GMT  
		Size: 3.0 MB (3020915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cb4727040aafcb55500dc13aab52d4a34221462584428f46c21e41bc086495`  
		Last Modified: Fri, 17 Jul 2020 02:51:37 GMT  
		Size: 184.2 MB (184231468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd2f1035f3378ab0ca666ecef614fb9ce84c8374e6c48849db241bf74d92f7`  
		Last Modified: Fri, 17 Jul 2020 02:51:05 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74308353d5e0db8661ab6a54f64c651aaa60c78e229fdd8855c7514dccf02eed`  
		Last Modified: Fri, 17 Jul 2020 02:51:06 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e0108d6b5812a3ead483a1dffc0ec600842f814ac81c8a1fc83bb89d99cbf7b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326674956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77cd9702b19785ac8f4126e9952c281df59e96592d11b58d412b91569024ab8`
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
# Tue, 14 Jul 2020 18:49:40 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 19:53:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 19:53:10 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 19:53:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 19:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 19:53:13 GMT
WORKDIR /go
# Tue, 14 Jul 2020 23:03:34 GMT
WORKDIR /src
# Tue, 14 Jul 2020 23:03:37 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 23:03:37 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 23:03:40 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 23:03:41 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 23:04:59 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 23:05:08 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 23:05:09 GMT
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
	-	`sha256:d6734511f5453510f789a8f7ea169069aeecf283185971411bd89d51922e664d`  
		Last Modified: Tue, 14 Jul 2020 22:45:39 GMT  
		Size: 128.6 MB (128598150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ee9318de4a795497843fc620410e8d6a98a1d19fbab73e68dcf95383d4a1f6`  
		Last Modified: Tue, 14 Jul 2020 22:45:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947232530c9fc7196e07fd4bb0cba9181daba56e2b40f99efa5c2c2d4a9efeca`  
		Last Modified: Tue, 14 Jul 2020 23:05:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13f7e40a2b5637113854a0f561473128d51495cc514ec4bacd36135a4566d3`  
		Last Modified: Tue, 14 Jul 2020 23:05:33 GMT  
		Size: 7.9 MB (7928849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5a9cfd6c38fce2c59e1623fe46b06d86440ed1668550c0db2ed0538449c316`  
		Last Modified: Tue, 14 Jul 2020 23:05:31 GMT  
		Size: 3.0 MB (3021030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61dc12432928c24532ce9ab7ee77d48fe2d76b9c57465491e73a3400d90b869`  
		Last Modified: Tue, 14 Jul 2020 23:06:15 GMT  
		Size: 184.2 MB (184239735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1390e4f7366d2946949fbc5da93c1e1e7b23ebfb33f9e3cb73a4371fb7027a`  
		Last Modified: Tue, 14 Jul 2020 23:05:31 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f2efe06b095053a12efa6f412a9b7a24da04c03bc58de9b14cc812f21fd2c5`  
		Last Modified: Tue, 14 Jul 2020 23:05:30 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6160b3382be3fa17b2bd5fc460b54a0679f0d0da6329b3849b3830130d396808
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325279166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa11268e132afb3f8db4e8968f0f61eda85f31035ddbc4445d2df757b056ac49`
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
# Tue, 14 Jul 2020 17:59:05 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 18:02:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 18:02:50 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 18:02:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 18:02:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 18:02:54 GMT
WORKDIR /go
# Tue, 14 Jul 2020 18:56:35 GMT
WORKDIR /src
# Tue, 14 Jul 2020 18:58:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 18:58:16 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 18:59:12 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 18:59:25 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 19:01:30 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 19:01:41 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 19:01:54 GMT
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
	-	`sha256:d6f82be5bf601cf8b3ce3831f415f8e4057942f012533eaff2a58504716e691a`  
		Last Modified: Tue, 14 Jul 2020 18:36:34 GMT  
		Size: 128.2 MB (128182109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba0c03e33b6ad6744dd6d0d95b528b643575969ef43d8ee7ed376c414852d6e`  
		Last Modified: Tue, 14 Jul 2020 18:35:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fc53d02f1b9139c39820bc6e987afeeb05c8771bbd857f29250bb964c27e9f`  
		Last Modified: Tue, 14 Jul 2020 19:02:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b25dac59cc9b0ea27059634cec097482636f01af1d7a844bf8a539f7fb2cf6`  
		Last Modified: Tue, 14 Jul 2020 19:02:22 GMT  
		Size: 7.1 MB (7144964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9886a84420be869be028a4ad927a6feceed4326d5a2185305023462496e44a22`  
		Last Modified: Tue, 14 Jul 2020 19:02:21 GMT  
		Size: 3.0 MB (3022770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee58a591970022dc8e292299bb78a6adca590e98417d91b36dabd8da154082c7`  
		Last Modified: Tue, 14 Jul 2020 19:03:15 GMT  
		Size: 184.2 MB (184239539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deee7fad20b8615c78c92a371c22e5ceb4a2e13e0aa7bd54aab2d9b49a8d478a`  
		Last Modified: Tue, 14 Jul 2020 19:02:21 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb0d7cb5d89f97627a2ae70d17e08b04d7e3ee1796e28e72894663184d3407`  
		Last Modified: Tue, 14 Jul 2020 19:02:21 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ae8b3b35d51c1eb448fccb525964b83f45401f9742b328eeb66eb511abb1bb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325648497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c92347766e3850b34fbdea8a715e307dc87c8ac2a2eacbcdf1d4c921b24418`
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
# Tue, 14 Jul 2020 18:41:29 GMT
ENV GOLANG_VERSION=1.14.5
# Tue, 14 Jul 2020 18:43:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'ca4c080c90735e56152ac52cd77ae57fe573d1debb1a58e03da9cc362440315c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 14 Jul 2020 18:43:50 GMT
ENV GOPATH=/go
# Tue, 14 Jul 2020 18:43:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jul 2020 18:43:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Jul 2020 18:43:53 GMT
WORKDIR /go
# Tue, 14 Jul 2020 19:20:52 GMT
WORKDIR /src
# Tue, 14 Jul 2020 19:21:08 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Jul 2020 19:21:13 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Tue, 14 Jul 2020 19:21:49 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Jul 2020 19:21:58 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Jul 2020 19:23:26 GMT
RUN go get -d ./...
# Tue, 14 Jul 2020 19:23:37 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Tue, 14 Jul 2020 19:23:50 GMT
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
	-	`sha256:92485ad5f2d3ea346a9b9c8bc5ecad8f5a7bd7307627c7eb9c028542d031c3c4`  
		Last Modified: Tue, 14 Jul 2020 19:01:08 GMT  
		Size: 126.9 MB (126893488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2de403c7edbdeb533ddf9de0f77d34967e0732a96718383ce14a94fda9a90c`  
		Last Modified: Tue, 14 Jul 2020 19:00:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798190983ee3217a79f307281f44856700c35522303a90a8919381bf7966ad09`  
		Last Modified: Tue, 14 Jul 2020 19:24:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33545d8fa9bbce0d09f720f2782c78861559dfacabbee8fb8d0dc0ba51cc401`  
		Last Modified: Tue, 14 Jul 2020 19:24:20 GMT  
		Size: 8.5 MB (8499921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22da6d889ac1af3ab3c92fc98fa5734b13a7ee8cae9c8fc0b5c6fcca0a9d4d96`  
		Last Modified: Tue, 14 Jul 2020 19:24:20 GMT  
		Size: 3.0 MB (3024185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4881453df79bdef3e280c2107fbd7adf7c0afe2613b4d4b7aba2556f9dbdc569`  
		Last Modified: Tue, 14 Jul 2020 19:25:02 GMT  
		Size: 184.2 MB (184238813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ba8dca3508d488fac5d42462196c64c861bf4a3ca5759237a44d7cd25f5c55`  
		Last Modified: Tue, 14 Jul 2020 19:24:19 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c649979b913b0bbcf906f4cad6d628821c19a7980077599e9fb513ed67aaae`  
		Last Modified: Tue, 14 Jul 2020 19:24:19 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:6f0d7c9bb84c51ed939efb13e3bf6ca9446d49b9d6f85958f0fb138de6a5c564
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324933638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833092067ee129e61a268dd93d22ceb73687f1de1cecd5e0df72bcda02dc5426`
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
# Fri, 17 Jul 2020 02:21:44 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:24:14 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:24:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:24:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:24:36 GMT
WORKDIR /go
# Fri, 17 Jul 2020 03:12:38 GMT
WORKDIR /src
# Fri, 17 Jul 2020 03:12:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 03:13:07 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 03:13:21 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 03:13:28 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 03:18:29 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 03:18:37 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 03:18:43 GMT
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
	-	`sha256:869ed739838c69d7e160dc1ff1fdd2300d17b52ee5d67aee493ca90d9b4fbd68`  
		Last Modified: Fri, 17 Jul 2020 02:45:38 GMT  
		Size: 125.7 MB (125656430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a61d3270248636b8a3f7205c3beff887ef7d4e2d403236b40d966e78b436f3`  
		Last Modified: Fri, 17 Jul 2020 02:43:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b42d4c77523f2d142783f55bea8336f93ff2cffd130887ca26938de15e3f7f`  
		Last Modified: Fri, 17 Jul 2020 03:19:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d23037bff9becbc5cea0824bae9147c00c87e29b5e83f2d3d3731d4542a3822`  
		Last Modified: Fri, 17 Jul 2020 03:19:09 GMT  
		Size: 8.9 MB (8920009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5927740889cdf47f4a17ea13d4bb5a9f5afca616c3c80b149e904f384b88bc64`  
		Last Modified: Fri, 17 Jul 2020 03:19:07 GMT  
		Size: 3.0 MB (3021040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa038742c660b74c276241553dd0dad4ad3ac9e8ad93d193a4c69258f93dff42`  
		Last Modified: Fri, 17 Jul 2020 03:19:34 GMT  
		Size: 184.2 MB (184244796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8514849ad61d3a9e0d21db033cc533db85e018c56ff97450ab8c55cfb2edca7e`  
		Last Modified: Fri, 17 Jul 2020 03:19:06 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75180876e9c63f9f97d6b4c520adaf9fe6fbfb5b935515aec347dbba6d8aa0c0`  
		Last Modified: Fri, 17 Jul 2020 03:19:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:6330b0180c606a640045d73f471239638e0082e1ac3de2ce2e799608b1403cff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330732719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2744f7b60057c0c75e28371bfa6b50008bd9abfe4ce40e894258ec0fe5dfa00`
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
# Fri, 17 Jul 2020 02:42:46 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:44:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:44:13 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:44:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:44:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:44:14 GMT
WORKDIR /go
# Fri, 17 Jul 2020 03:09:23 GMT
WORKDIR /src
# Fri, 17 Jul 2020 03:09:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 03:09:27 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 03:09:29 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 03:09:30 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 03:10:20 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 03:10:41 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 03:10:42 GMT
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
	-	`sha256:561add13be46fdce5a695d1ca8906ad50a90e3d3d25d47e1ad2c8478537bc445`  
		Last Modified: Fri, 17 Jul 2020 02:51:38 GMT  
		Size: 132.3 MB (132268907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f72d70911ac3c6bbdf16aa3d58a6bbe08cf171406e75d7dbf84c7ffd219073`  
		Last Modified: Fri, 17 Jul 2020 02:51:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38e21bb7fac2484df2339b1be77584264518b7a0dcb878869e6fade02cd7a2e`  
		Last Modified: Fri, 17 Jul 2020 03:11:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a5388655ece15f0d53ad7c41a2cdde6c25eab31b939efbe1eb3aa76c0279b3`  
		Last Modified: Fri, 17 Jul 2020 03:11:07 GMT  
		Size: 8.4 MB (8352234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4c55d0a142dc8b432c7f402cedd62737abb5d83f72caf89a1b0bed0066c6be`  
		Last Modified: Fri, 17 Jul 2020 03:11:11 GMT  
		Size: 3.0 MB (3024180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a5905cbf69b78060dd069e31cdabd5ee3a08eefaa57bc455415b85929755ac`  
		Last Modified: Fri, 17 Jul 2020 03:11:23 GMT  
		Size: 184.2 MB (184236938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af024d101834697f989a8213e8472351a541b76397f2be2fd6cdf79bef5292a8`  
		Last Modified: Fri, 17 Jul 2020 03:11:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7dbf6babd157dfc3f807bef9a82ac255c5c1c471919c8578aa0a4626d5f834`  
		Last Modified: Fri, 17 Jul 2020 03:11:36 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:b1d5080ca3217345d121fc8b87d3a0253dfacfad698a7495b6814531849f1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

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

### `caddy:latest` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:c69acf82737ac04895de0fe82b6460bf07cbb49ba46a3b50df15e1210d7630bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:eac1adaea9ec4c19a0a1b6fae6187b72828c250ddb7945b39bd1e9d33fb71344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull caddy@sha256:99a0cb78f621c8ece884f98efa577a294468e5698e107743deba0b7ac0e3764a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2337383535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d47d90e40341b6b8fa66121e42b7dfc6b0d5555db02c90160db6b48fe155914`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 20:28:08 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 20:28:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 20:28:57 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 20:29:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 20:29:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 20:29:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 20:29:46 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 20:29:47 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 20:29:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 20:29:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 20:29:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 20:29:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 20:29:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 20:29:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 20:29:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 20:29:55 GMT
EXPOSE 80
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 443
# Wed, 15 Jul 2020 20:29:56 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:00:34 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:00:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc64d1c029a50ee3e856575ec256b57b393113571c86b1a5919c0c0514d157`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be8eb775646bb233b242e9d3ca7163ec243fbcd8e07a15848432d031f84eb43`  
		Last Modified: Wed, 15 Jul 2020 21:05:51 GMT  
		Size: 9.2 MB (9167169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862322254c73df806b8c71877b281e8d4a8a280e41d4387ea3c5389a04252624`  
		Last Modified: Wed, 15 Jul 2020 21:05:47 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a051d5264ef87f76d069292da2721f249518b569a8a0eb2e11d70eea9eb6395`  
		Last Modified: Wed, 15 Jul 2020 21:05:53 GMT  
		Size: 17.7 MB (17696048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbffcf9bd80c8e6eb8c25f9d5699e5b0c0be9c2980b6627216c3ea6273c01a56`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007876629223e4b02ed8558f717c3ec6834d824143e14da08e087102730a50ce`  
		Last Modified: Wed, 15 Jul 2020 21:05:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fccb3b9bcd1c77bd6e3e9988348dd097f9414eb265e85b185e7f7d79dba5f`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839ddf96a6d0b134653c332d17fedc7c93d2375e5f0335cb29c5b860c9252c6`  
		Last Modified: Wed, 15 Jul 2020 21:05:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9111a30dd3a9c44e24fc646e3106ff9481e8c2bed203d993890616303f2d97`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4054cf722fa3e1e89252c0586ec631e5d9dd2c163ff53392fd08ff0026d7c21d`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020b5942f006103c75544d19b05e005d7588d92dd74eff78f505715873bcefa`  
		Last Modified: Wed, 15 Jul 2020 21:05:44 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b9901bf6a273ed5b94ccce40bbdac3a670de6a6c09c6ab19bd971c65dd93e`  
		Last Modified: Wed, 15 Jul 2020 21:05:43 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6cab8d2ea2f7f2f02db09187c7f0b191e66f2e3d4198c4f90d2ccd2c37904`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddd9cea5d6f968998061e3457c74e9f56662d631fb741c63d6d162f9870199c`  
		Last Modified: Wed, 15 Jul 2020 21:05:42 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95566356968511d7d531233211da3aeb409480742ed5e8257bb434b766edbb47`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c0df1f60886f0ffcfbe19763e6e308c6f00b08e063663afe3362882ecd0452`  
		Last Modified: Wed, 15 Jul 2020 21:05:41 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474cdd3e71b87521fe61ce50fd15427e4bd34b8d6de250000d6df9f05711ca9`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9790b984113584011ea4b82790a02d435fe886e882d45892c6a90e05236cdb`  
		Last Modified: Wed, 15 Jul 2020 21:05:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a61f9bf4bbce65cde60054ed9b62fca33f7393c5f167b20dc15db287c1a4`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b833422b391d03dfcdc1949a2b4d454b14f08d76d7c6333b00d705a889a3d2`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 306.2 KB (306237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e42c711d532ef5229587942a616d8c142609d4d27bf29503082f5154fa52ea`  
		Last Modified: Wed, 15 Jul 2020 21:05:39 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:3f88aabc0b2d55a45411b9751f8115fabcb2f3287a98bbaee17a9ff00a314b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull caddy@sha256:9309bb10d0c669007e988170de8a41389199e441213ccb1008719045ebd871ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5770427260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec3aa4c7384a5a7cba1c487c1d02e49f9614a0b77af72f9b61c3552842418ad`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jul 2020 18:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 21:00:41 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 15 Jul 2020 21:02:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Jul 2020 21:02:17 GMT
ENV CADDY_VERSION=v2.1.1
# Wed, 15 Jul 2020 21:03:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.1/caddy_2.1.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('435c881bf3d149da2339fdca28cf4bedcba79a3ed6bbd79365113e7e78bd110f544a13ab4976529cf73d4760c64991abed7b6f952ace4396ff5a78d98fcf3e19')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Jul 2020 21:04:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Jul 2020 21:04:02 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Jul 2020 21:04:03 GMT
VOLUME [c:/config]
# Wed, 15 Jul 2020 21:04:04 GMT
VOLUME [c:/data]
# Wed, 15 Jul 2020 21:04:05 GMT
LABEL org.opencontainers.image.version=v2.1.1
# Wed, 15 Jul 2020 21:04:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Jul 2020 21:04:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Jul 2020 21:04:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Jul 2020 21:04:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Jul 2020 21:04:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Jul 2020 21:04:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Jul 2020 21:04:12 GMT
EXPOSE 80
# Wed, 15 Jul 2020 21:04:13 GMT
EXPOSE 443
# Wed, 15 Jul 2020 21:04:14 GMT
EXPOSE 2019
# Wed, 15 Jul 2020 21:05:07 GMT
RUN caddy version
# Wed, 15 Jul 2020 21:05:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9a64f8d0454dba1fb133615caae6ab4d76b85b8be54102ee2ce5f7fd034edbff`  
		Last Modified: Tue, 14 Jul 2020 19:42:07 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973eea74d5e1ffbee09352aaa6979a2d5e7f3c706dadaf44f4735b71528e922`  
		Last Modified: Wed, 15 Jul 2020 21:06:19 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f61001103e65bd146a657498ccfcfef4b3e655e152634f152f700fdabc17`  
		Last Modified: Wed, 15 Jul 2020 21:06:20 GMT  
		Size: 9.9 MB (9860229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed887351cc64ca113fa7bf7f7a2aebb4211ddce4e231d0788faf2901d728f73`  
		Last Modified: Wed, 15 Jul 2020 21:06:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c505dc3cb2fb08c1762e86cec96351555b1abe4c696257d5bd6bf8ad8d63fa`  
		Last Modified: Wed, 15 Jul 2020 21:06:22 GMT  
		Size: 22.8 MB (22833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495a4007452fe320b5bcd5eaff6043e3e7109e555aaef70fe48415a0f0421da3`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ef463accb9b7440da0074a6a76406c2609cae40dfb7e2c5a86f2b6f2c710a`  
		Last Modified: Wed, 15 Jul 2020 21:06:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba58a4c1dc0267ebcdd7a394efe0579230d6e1978d432f0a26655f9cd08f55c`  
		Last Modified: Wed, 15 Jul 2020 21:06:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6251cd849c18772101da9a5f71426f8339bef0c24e203b9bd825db4cae16d12`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002e23d61ce3428e1fa084e6ffd1b9be668908d71de91e1faaa786c8e6fba78`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb19c35b49270f4d2aeaaf824025a60155e944919f9f004388a17cfff48484`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ddc2a191bf998f6e818f0d60659d7d3c484ad20278f9833a5907dffde86892`  
		Last Modified: Wed, 15 Jul 2020 21:06:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9d6373b17b66ef4c716a0c96d055a68fc978ff714db11cb09c3308884a4a1`  
		Last Modified: Wed, 15 Jul 2020 21:06:11 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5095f9f74e5647a4a6b1b98cc35e2c569db0850b6aec715fb3baab1623ee5a8`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897ee4b18292062520147945a013cfa6c8a0d3797a4d2524e3534beaefd575c`  
		Last Modified: Wed, 15 Jul 2020 21:06:10 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8794fd0e5e655ec2d89a9d9d1f47d5f2caef36c2ec2a6cc991b8f7c67cec6a41`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2493d876886903285caa29fb7b4832d31e2151d3a67bcda7826d46481df75760`  
		Last Modified: Wed, 15 Jul 2020 21:06:09 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf378561c7f8518ef0225407bd8313de0cca4163ac035bff87df4c4be9b03b6`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aacd0d404da37e5ea550034d905b05d5213a8d9031693c6872af21dbcd22e5`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba977b186a4be8e23c17faa98503f4515730562bfcb2743db73e049f1bf88f19`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd44d05094d09ad50f236a4bcf6fed122d75c70ee60acdaea9d1e3047b26e09`  
		Last Modified: Wed, 15 Jul 2020 21:06:08 GMT  
		Size: 250.2 KB (250201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67070899e7f7404e80024c2189b2ccde88bd8732fe4d93ee92b3eebeb90c63e`  
		Last Modified: Wed, 15 Jul 2020 21:06:07 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
