<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2.0.0`](#caddy200)
-	[`caddy:2.0.0-alpine`](#caddy200-alpine)
-	[`caddy:2.0.0-builder`](#caddy200-builder)
-	[`caddy:2.0.0-windowsservercore`](#caddy200-windowsservercore)
-	[`caddy:2.0.0-windowsservercore-1809`](#caddy200-windowsservercore-1809)
-	[`caddy:2.0.0-windowsservercore-ltsc2016`](#caddy200-windowsservercore-ltsc2016)
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
$ docker pull caddy@sha256:a318e53203be65b120d2bfc2a887838fe32bcc839c02df83571d101429bc4f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:5dcf7aba2d86d1bd9d019b4431b683f78e674b0463ca17b2a7f46464bbc62332
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15145219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2721e97adcec739105d14978b5eafb916a9174c643402360ce0397d490c25f49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:39:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 13:39:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 13:39:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 19:20:49 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:21:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 80
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 443
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:21:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c92d2df695a8e1549e487fe6691311b8c3ccfdd90383c6ae37c578c4465c76`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 318.6 KB (318554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d779d752c63b3ccba5c5fbec57ae2361cef2059d83ea0770f389f1d9849ccde`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 5.8 KB (5765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e321d52b548add190f8f5974453da203fc605ed33865ced7b83cc1e8fddc904e`  
		Last Modified: Wed, 06 May 2020 16:21:33 GMT  
		Size: 12.0 MB (12007584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a81d694d3aa6fb71250200e1bd70d07066f22e9ac6a1951b3d6df18d03e12b20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14390606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19bc691ae372dac3178e3250246952c0abba5a58c5f48ae92782d9c02660ef6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:42:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 17:42:31 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 17:42:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:49:25 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:49:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:49:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:49:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:49:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:49:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:49:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4aecf4b3c455b15219e7ae2914078c1796d34e6b1c2916aab2fa79d0aecc97`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 318.9 KB (318932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f3e6c459120cfcfb844a46e1d5fa39f425743ad39e3265fdb6b4c4ea312b6`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6977aa451d29e02cfa0a60ee52aadf3bfa7fad7712ac1687007cbb0bd812f996`  
		Last Modified: Wed, 06 May 2020 15:50:14 GMT  
		Size: 11.4 MB (11445896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fc3097b3cd99187dca11658bd33e93e002c8c5cc7de8bc6a29e9ba97d9d405ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14164557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a168a021dfdb6e7170f3f10bb242384bb0946809b89047cc76cd4f0127f74bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 23:22:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 23:22:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 23:23:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:57:29 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:57:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:57:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:57:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:57:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:57:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:57:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:57:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:57:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:57:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:57:43 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:57:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf760b044fed05d609c6cc0dbc0163d673af839c2bd8b93be46a9dd9b3235d8d`  
		Last Modified: Thu, 23 Apr 2020 23:23:51 GMT  
		Size: 317.9 KB (317871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702db93291bb8c691008d86b00d866d87fd9904461e56e447408436f67069d12`  
		Last Modified: Thu, 23 Apr 2020 23:23:50 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a240b5e189e2da028c9e14c55e560dda7eebabe89a0fdc68bd063df8ac5403`  
		Last Modified: Wed, 06 May 2020 15:58:14 GMT  
		Size: 11.4 MB (11418780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:fda3e6c211e921c164d446eb0db4516b3100092ac6906e34142f02d2a1467ed8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14099349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6718b41c65682371b1c36f12939c112979db7a4cabdd180ceb046dc80a3653`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 03:41:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 03:41:27 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 03:41:30 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:39:39 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:39:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:39:44 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:39:45 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:39:47 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:39:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:39:57 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:39:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:40:01 GMT
EXPOSE 80
# Wed, 06 May 2020 16:40:02 GMT
EXPOSE 443
# Wed, 06 May 2020 16:40:04 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:40:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1dd90474a5634d83eea66237a34342ba1aa7b9660127d7a6168f9dd16a6800`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 319.1 KB (319109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523ce157ee2040adfd1d897f97c884c8df6de54df4581f3982d4114fea063843`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45586f3cd2c78aa4e4ec308b720449bd298ff8184489fc23ed1b63329d5bfba`  
		Last Modified: Wed, 06 May 2020 16:40:28 GMT  
		Size: 11.0 MB (11049973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:d41420be541ff741166121a337ab2380a37986b80e2c198d33cfa2716b89eebc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14000265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620e8e504bd843011d47928ba3108b784ab917c2b4e49c91f9b5e7a1ed0488e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:29:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:01 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:10 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:25 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:29 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:34 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:31:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:31:03 GMT
EXPOSE 80
# Wed, 06 May 2020 15:31:09 GMT
EXPOSE 443
# Wed, 06 May 2020 15:31:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:31:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5a8966b60d898cbfd9fb53281860fcb82df54d8f66c9142f4038d0e3d8afb8`  
		Last Modified: Wed, 06 May 2020 15:36:35 GMT  
		Size: 321.6 KB (321641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdcee6bf7f07bf2e87c36762756faa63a587b445b5112371d799d9983a38d7f`  
		Last Modified: Wed, 06 May 2020 15:36:34 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912d87d0a8415f3b9ba60c72fc6309c0c67fb08b2834913add34eb8344ce0826`  
		Last Modified: Wed, 06 May 2020 15:36:42 GMT  
		Size: 10.9 MB (10850936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:befbf95ceefa9c63c3cb86d06d19549d32b0e79546b943634e906584a01fec1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14740576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b4e73e6c6c10833f75c31436b5903780a5cf76d6d767633538129d7d9cef2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:30:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:05 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:30:19 GMT
EXPOSE 80
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 443
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:30:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1098bec6a96fa022c5d1e1043cbd10f41d1b5e0788cdeb71e1cbdf3ba0f6b6`  
		Last Modified: Wed, 06 May 2020 15:32:28 GMT  
		Size: 319.2 KB (319200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b06bf33ed224c71042842eaa50af6440423bb48f5cf032ce51277c7d08cb79f`  
		Last Modified: Wed, 06 May 2020 15:32:27 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b3c02c4f07ca031406ddeefa20f1428b199d11370f5548cffe6bf3c294088c`  
		Last Modified: Wed, 06 May 2020 15:32:29 GMT  
		Size: 11.8 MB (11832677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.1217; amd64

```console
$ docker pull caddy@sha256:72fb2769c5bca3a826c2d20272955543ae0505293b8a21f9d7be902c4024462d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1731274652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de5663795f5d4dcdda76bf3051f819c10c1b278328fcf09e429e336ca484f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:46:58 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:47:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:47:22 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:47:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:47:52 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:47:53 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:47:54 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:47:55 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:47:56 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:47:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:47:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:48:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:48:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:48:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:48:03 GMT
EXPOSE 80
# Wed, 13 May 2020 18:48:04 GMT
EXPOSE 443
# Wed, 13 May 2020 18:48:05 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:48:22 GMT
RUN caddy version
# Wed, 13 May 2020 18:48:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cc8f1346629803094aa24186a3ffc8662b4a2ee69dc801d795f005d4a0d95`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18106f83313e5d34a070612d3f1c39e8cf8d9848e2b227296adfffd3965ba25d`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 355.3 KB (355269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f287fd10774920755d67b6de43826c118ec5fc4e8f9702a55be22da2df6358`  
		Last Modified: Wed, 13 May 2020 18:53:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffcf71efbb212a67332d8465f099b447811876b9e83c74eec3c01de1fcb9d0`  
		Last Modified: Wed, 13 May 2020 18:53:10 GMT  
		Size: 12.3 MB (12275873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0eb7cc61a3acb2499d87ea010471ade578b24271a239602554546a519ffbf9`  
		Last Modified: Wed, 13 May 2020 18:53:04 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafa5496993eb381a49e7fbbadd58834e3ddc0c0e33a83a2b81965beaa664e0`  
		Last Modified: Wed, 13 May 2020 18:53:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8269f4f8903d1aef05afd562fda930223dee66a331d0047620fd05dfc076caa`  
		Last Modified: Wed, 13 May 2020 18:53:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0ba135849e8ad69d2e177204089724847fea899770d08be4f326960779471`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775de502a9e90f88c9d9c68063a1aed6775b8a8eaa4f680ea12b84c7a86997aa`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8993d7ccb4765510c6cd037e5115c7af0ce11df1c85256085067fdc1fc433`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3755d5c96e8367ee1c769a90f6e6cfc081fdaf18343af918f815188b334e9`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601866b20fd891e3cb277f3f8f172047a2f71d4ff1d97f310c3b94093dc46a50`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01551299aef213dc22bc7224e912b43e5787201c29b0c31153423f15c5db0a94`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a51580e4218eb251ae8f64eadc2ec6762034308a4057de80eb7472494393b`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be3a4f0438b1d7c8f2a308cb89fea8bbe8fb3b40f143a62069975f86ba1b059`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118019e0b8aa2d8afae2f438d7ff8005a9e4099624fab2c12ea86fec750c64f2`  
		Last Modified: Wed, 13 May 2020 18:52:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ef0c9522d683451d62dee32a69cde84172241d69c164110f784f78162e2a0`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b1c41daa7f57c8fe29b16a91ac4e60b636df159ed486ca9f9dc35bab92154`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96904d7376e44abc396e46bb450c2da8dcfba33355155f6240e07a878423a5`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27936f5bc0bfbebee69fb6ffdd7bb368b4894c8388b64ee02ad1c7c467677`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 288.9 KB (288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2f832bbb7958dfa84ad0d27ee64e1f200e10eb27024304f6f7cac63a1be89`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.14393.3686; amd64

```console
$ docker pull caddy@sha256:934fdbcbab89ce90c31479b6686014c304c2e4025f40ab12a0184d7d7031e77c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5754870634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3efc2e9d649455a51c1e525b202723307ac0807d3a66606f8b89e8e1722425`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:48:38 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:49:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:49:58 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:51:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:51:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:51:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:51:25 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:51:26 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:51:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:51:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:51:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:51:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:51:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:51:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:51:35 GMT
EXPOSE 80
# Wed, 13 May 2020 18:51:36 GMT
EXPOSE 443
# Wed, 13 May 2020 18:51:37 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:52:21 GMT
RUN caddy version
# Wed, 13 May 2020 18:52:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8d9441a5da81d2777cfc76980d60cc19b098fe856021de5a9895613a07a917`  
		Last Modified: Wed, 13 May 2020 18:54:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c45322765cd792196713eabac6cc04ae89c4fa85c29b1ca626b72c62996f6`  
		Last Modified: Wed, 13 May 2020 18:54:27 GMT  
		Size: 5.4 MB (5392506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b93c4954c5f72c6e382ba1480c3d976f845f42c19bb5e0a085798079bb636`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4516cd556129c57a85ef8c01db6dd2122853c304e58bf1d1594fdd77424509`  
		Last Modified: Wed, 13 May 2020 18:54:26 GMT  
		Size: 17.3 MB (17316249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b2c917ea7e1658aee4b4fa5144174055d3138552746c780d9540a188c3d7`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159ba07aef82e0d25aaef42f0ea5a8f3e9ac5979006bb5cfd717fa2b5979c19`  
		Last Modified: Wed, 13 May 2020 18:54:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed119e58b16c0727c096be5f489492947e6c14fa38726d290d671d3eb0b7ddc`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36668ca695daf89b18a9a9f22a1ab73b9caff740b5fe364c83b8752053bd520a`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda31fec458b3a7161e6b3a2ab63d82bb1ab9291b37081e70941e73a13d4cad6`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31dc3ae4fe27e8327f459ea65e33ab8c62ffdea360d1b9553ed5cae8d21e7b`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0ac6915dd1ededf8d058abfbf5bf18ae61704814448b2017af1b56ac222f`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3813123a037b3f32302ec2832c105f64f7e4a171a7c551709919d2a2fe50`  
		Last Modified: Wed, 13 May 2020 18:54:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5c9c51be87e873c5fd688f518a5287153de163472db0a1b8ef5219ebc4667`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b34839eed5be808ac4292dce3424594ea3cff620ab4c5abbb21d7175165bf`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e296d31b4d6061f26450d68b391b5d96928617c8bc8cbf385721f19db40f13`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a176c2fcfe281888b44bd6b42edc40ecb1f15fa70e3b46a4057a06a461d97`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80eb7786a112e5e30e573401f1db37e107bf00f6dd3cb2d5e4a5bfcff5864e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fc20b2cbd0d3d3009ab3518b6b3df01534f7bf771ac110e8d1d399a1d4c8e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2955b5f7006f6354828c6ed4286cecaf180196b00f8c315c9f6cf796a9cde`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc73cc73e699dfa7d295778821ae30a39417fe6ae6d52ad4d0ab252cf71976`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 250.3 KB (250292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebb1402ecee93e19be9f62d2148b518e2d255f5592ab44f8090e373ccd7eeb`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.0.0`

```console
$ docker pull caddy@sha256:a318e53203be65b120d2bfc2a887838fe32bcc839c02df83571d101429bc4f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `caddy:2.0.0` - linux; amd64

```console
$ docker pull caddy@sha256:5dcf7aba2d86d1bd9d019b4431b683f78e674b0463ca17b2a7f46464bbc62332
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15145219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2721e97adcec739105d14978b5eafb916a9174c643402360ce0397d490c25f49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:39:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 13:39:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 13:39:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 19:20:49 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:21:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 80
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 443
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:21:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c92d2df695a8e1549e487fe6691311b8c3ccfdd90383c6ae37c578c4465c76`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 318.6 KB (318554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d779d752c63b3ccba5c5fbec57ae2361cef2059d83ea0770f389f1d9849ccde`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 5.8 KB (5765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e321d52b548add190f8f5974453da203fc605ed33865ced7b83cc1e8fddc904e`  
		Last Modified: Wed, 06 May 2020 16:21:33 GMT  
		Size: 12.0 MB (12007584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a81d694d3aa6fb71250200e1bd70d07066f22e9ac6a1951b3d6df18d03e12b20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14390606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19bc691ae372dac3178e3250246952c0abba5a58c5f48ae92782d9c02660ef6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:42:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 17:42:31 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 17:42:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:49:25 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:49:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:49:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:49:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:49:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:49:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:49:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4aecf4b3c455b15219e7ae2914078c1796d34e6b1c2916aab2fa79d0aecc97`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 318.9 KB (318932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f3e6c459120cfcfb844a46e1d5fa39f425743ad39e3265fdb6b4c4ea312b6`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6977aa451d29e02cfa0a60ee52aadf3bfa7fad7712ac1687007cbb0bd812f996`  
		Last Modified: Wed, 06 May 2020 15:50:14 GMT  
		Size: 11.4 MB (11445896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fc3097b3cd99187dca11658bd33e93e002c8c5cc7de8bc6a29e9ba97d9d405ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14164557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a168a021dfdb6e7170f3f10bb242384bb0946809b89047cc76cd4f0127f74bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 23:22:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 23:22:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 23:23:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:57:29 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:57:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:57:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:57:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:57:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:57:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:57:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:57:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:57:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:57:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:57:43 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:57:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf760b044fed05d609c6cc0dbc0163d673af839c2bd8b93be46a9dd9b3235d8d`  
		Last Modified: Thu, 23 Apr 2020 23:23:51 GMT  
		Size: 317.9 KB (317871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702db93291bb8c691008d86b00d866d87fd9904461e56e447408436f67069d12`  
		Last Modified: Thu, 23 Apr 2020 23:23:50 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a240b5e189e2da028c9e14c55e560dda7eebabe89a0fdc68bd063df8ac5403`  
		Last Modified: Wed, 06 May 2020 15:58:14 GMT  
		Size: 11.4 MB (11418780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:fda3e6c211e921c164d446eb0db4516b3100092ac6906e34142f02d2a1467ed8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14099349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6718b41c65682371b1c36f12939c112979db7a4cabdd180ceb046dc80a3653`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 03:41:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 03:41:27 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 03:41:30 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:39:39 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:39:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:39:44 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:39:45 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:39:47 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:39:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:39:57 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:39:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:40:01 GMT
EXPOSE 80
# Wed, 06 May 2020 16:40:02 GMT
EXPOSE 443
# Wed, 06 May 2020 16:40:04 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:40:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1dd90474a5634d83eea66237a34342ba1aa7b9660127d7a6168f9dd16a6800`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 319.1 KB (319109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523ce157ee2040adfd1d897f97c884c8df6de54df4581f3982d4114fea063843`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45586f3cd2c78aa4e4ec308b720449bd298ff8184489fc23ed1b63329d5bfba`  
		Last Modified: Wed, 06 May 2020 16:40:28 GMT  
		Size: 11.0 MB (11049973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0` - linux; ppc64le

```console
$ docker pull caddy@sha256:d41420be541ff741166121a337ab2380a37986b80e2c198d33cfa2716b89eebc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14000265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620e8e504bd843011d47928ba3108b784ab917c2b4e49c91f9b5e7a1ed0488e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:29:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:01 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:10 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:25 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:29 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:34 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:31:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:31:03 GMT
EXPOSE 80
# Wed, 06 May 2020 15:31:09 GMT
EXPOSE 443
# Wed, 06 May 2020 15:31:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:31:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5a8966b60d898cbfd9fb53281860fcb82df54d8f66c9142f4038d0e3d8afb8`  
		Last Modified: Wed, 06 May 2020 15:36:35 GMT  
		Size: 321.6 KB (321641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdcee6bf7f07bf2e87c36762756faa63a587b445b5112371d799d9983a38d7f`  
		Last Modified: Wed, 06 May 2020 15:36:34 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912d87d0a8415f3b9ba60c72fc6309c0c67fb08b2834913add34eb8344ce0826`  
		Last Modified: Wed, 06 May 2020 15:36:42 GMT  
		Size: 10.9 MB (10850936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0` - linux; s390x

```console
$ docker pull caddy@sha256:befbf95ceefa9c63c3cb86d06d19549d32b0e79546b943634e906584a01fec1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14740576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b4e73e6c6c10833f75c31436b5903780a5cf76d6d767633538129d7d9cef2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:30:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:05 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:30:19 GMT
EXPOSE 80
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 443
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:30:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1098bec6a96fa022c5d1e1043cbd10f41d1b5e0788cdeb71e1cbdf3ba0f6b6`  
		Last Modified: Wed, 06 May 2020 15:32:28 GMT  
		Size: 319.2 KB (319200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b06bf33ed224c71042842eaa50af6440423bb48f5cf032ce51277c7d08cb79f`  
		Last Modified: Wed, 06 May 2020 15:32:27 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b3c02c4f07ca031406ddeefa20f1428b199d11370f5548cffe6bf3c294088c`  
		Last Modified: Wed, 06 May 2020 15:32:29 GMT  
		Size: 11.8 MB (11832677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0` - windows version 10.0.17763.1217; amd64

```console
$ docker pull caddy@sha256:72fb2769c5bca3a826c2d20272955543ae0505293b8a21f9d7be902c4024462d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1731274652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de5663795f5d4dcdda76bf3051f819c10c1b278328fcf09e429e336ca484f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:46:58 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:47:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:47:22 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:47:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:47:52 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:47:53 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:47:54 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:47:55 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:47:56 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:47:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:47:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:48:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:48:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:48:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:48:03 GMT
EXPOSE 80
# Wed, 13 May 2020 18:48:04 GMT
EXPOSE 443
# Wed, 13 May 2020 18:48:05 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:48:22 GMT
RUN caddy version
# Wed, 13 May 2020 18:48:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cc8f1346629803094aa24186a3ffc8662b4a2ee69dc801d795f005d4a0d95`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18106f83313e5d34a070612d3f1c39e8cf8d9848e2b227296adfffd3965ba25d`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 355.3 KB (355269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f287fd10774920755d67b6de43826c118ec5fc4e8f9702a55be22da2df6358`  
		Last Modified: Wed, 13 May 2020 18:53:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffcf71efbb212a67332d8465f099b447811876b9e83c74eec3c01de1fcb9d0`  
		Last Modified: Wed, 13 May 2020 18:53:10 GMT  
		Size: 12.3 MB (12275873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0eb7cc61a3acb2499d87ea010471ade578b24271a239602554546a519ffbf9`  
		Last Modified: Wed, 13 May 2020 18:53:04 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafa5496993eb381a49e7fbbadd58834e3ddc0c0e33a83a2b81965beaa664e0`  
		Last Modified: Wed, 13 May 2020 18:53:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8269f4f8903d1aef05afd562fda930223dee66a331d0047620fd05dfc076caa`  
		Last Modified: Wed, 13 May 2020 18:53:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0ba135849e8ad69d2e177204089724847fea899770d08be4f326960779471`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775de502a9e90f88c9d9c68063a1aed6775b8a8eaa4f680ea12b84c7a86997aa`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8993d7ccb4765510c6cd037e5115c7af0ce11df1c85256085067fdc1fc433`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3755d5c96e8367ee1c769a90f6e6cfc081fdaf18343af918f815188b334e9`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601866b20fd891e3cb277f3f8f172047a2f71d4ff1d97f310c3b94093dc46a50`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01551299aef213dc22bc7224e912b43e5787201c29b0c31153423f15c5db0a94`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a51580e4218eb251ae8f64eadc2ec6762034308a4057de80eb7472494393b`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be3a4f0438b1d7c8f2a308cb89fea8bbe8fb3b40f143a62069975f86ba1b059`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118019e0b8aa2d8afae2f438d7ff8005a9e4099624fab2c12ea86fec750c64f2`  
		Last Modified: Wed, 13 May 2020 18:52:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ef0c9522d683451d62dee32a69cde84172241d69c164110f784f78162e2a0`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b1c41daa7f57c8fe29b16a91ac4e60b636df159ed486ca9f9dc35bab92154`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96904d7376e44abc396e46bb450c2da8dcfba33355155f6240e07a878423a5`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27936f5bc0bfbebee69fb6ffdd7bb368b4894c8388b64ee02ad1c7c467677`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 288.9 KB (288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2f832bbb7958dfa84ad0d27ee64e1f200e10eb27024304f6f7cac63a1be89`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0` - windows version 10.0.14393.3686; amd64

```console
$ docker pull caddy@sha256:934fdbcbab89ce90c31479b6686014c304c2e4025f40ab12a0184d7d7031e77c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5754870634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3efc2e9d649455a51c1e525b202723307ac0807d3a66606f8b89e8e1722425`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:48:38 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:49:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:49:58 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:51:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:51:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:51:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:51:25 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:51:26 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:51:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:51:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:51:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:51:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:51:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:51:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:51:35 GMT
EXPOSE 80
# Wed, 13 May 2020 18:51:36 GMT
EXPOSE 443
# Wed, 13 May 2020 18:51:37 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:52:21 GMT
RUN caddy version
# Wed, 13 May 2020 18:52:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8d9441a5da81d2777cfc76980d60cc19b098fe856021de5a9895613a07a917`  
		Last Modified: Wed, 13 May 2020 18:54:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c45322765cd792196713eabac6cc04ae89c4fa85c29b1ca626b72c62996f6`  
		Last Modified: Wed, 13 May 2020 18:54:27 GMT  
		Size: 5.4 MB (5392506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b93c4954c5f72c6e382ba1480c3d976f845f42c19bb5e0a085798079bb636`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4516cd556129c57a85ef8c01db6dd2122853c304e58bf1d1594fdd77424509`  
		Last Modified: Wed, 13 May 2020 18:54:26 GMT  
		Size: 17.3 MB (17316249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b2c917ea7e1658aee4b4fa5144174055d3138552746c780d9540a188c3d7`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159ba07aef82e0d25aaef42f0ea5a8f3e9ac5979006bb5cfd717fa2b5979c19`  
		Last Modified: Wed, 13 May 2020 18:54:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed119e58b16c0727c096be5f489492947e6c14fa38726d290d671d3eb0b7ddc`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36668ca695daf89b18a9a9f22a1ab73b9caff740b5fe364c83b8752053bd520a`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda31fec458b3a7161e6b3a2ab63d82bb1ab9291b37081e70941e73a13d4cad6`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31dc3ae4fe27e8327f459ea65e33ab8c62ffdea360d1b9553ed5cae8d21e7b`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0ac6915dd1ededf8d058abfbf5bf18ae61704814448b2017af1b56ac222f`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3813123a037b3f32302ec2832c105f64f7e4a171a7c551709919d2a2fe50`  
		Last Modified: Wed, 13 May 2020 18:54:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5c9c51be87e873c5fd688f518a5287153de163472db0a1b8ef5219ebc4667`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b34839eed5be808ac4292dce3424594ea3cff620ab4c5abbb21d7175165bf`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e296d31b4d6061f26450d68b391b5d96928617c8bc8cbf385721f19db40f13`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a176c2fcfe281888b44bd6b42edc40ecb1f15fa70e3b46a4057a06a461d97`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80eb7786a112e5e30e573401f1db37e107bf00f6dd3cb2d5e4a5bfcff5864e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fc20b2cbd0d3d3009ab3518b6b3df01534f7bf771ac110e8d1d399a1d4c8e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2955b5f7006f6354828c6ed4286cecaf180196b00f8c315c9f6cf796a9cde`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc73cc73e699dfa7d295778821ae30a39417fe6ae6d52ad4d0ab252cf71976`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 250.3 KB (250292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebb1402ecee93e19be9f62d2148b518e2d255f5592ab44f8090e373ccd7eeb`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.0.0-alpine`

```console
$ docker pull caddy@sha256:23d7342a40c9a3961d73d2e2d31a7d18ea84b8bbfb2f189460661614613ffb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.0.0-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:5dcf7aba2d86d1bd9d019b4431b683f78e674b0463ca17b2a7f46464bbc62332
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15145219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2721e97adcec739105d14978b5eafb916a9174c643402360ce0397d490c25f49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:39:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 13:39:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 13:39:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 19:20:49 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:21:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 80
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 443
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:21:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c92d2df695a8e1549e487fe6691311b8c3ccfdd90383c6ae37c578c4465c76`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 318.6 KB (318554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d779d752c63b3ccba5c5fbec57ae2361cef2059d83ea0770f389f1d9849ccde`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 5.8 KB (5765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e321d52b548add190f8f5974453da203fc605ed33865ced7b83cc1e8fddc904e`  
		Last Modified: Wed, 06 May 2020 16:21:33 GMT  
		Size: 12.0 MB (12007584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a81d694d3aa6fb71250200e1bd70d07066f22e9ac6a1951b3d6df18d03e12b20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14390606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19bc691ae372dac3178e3250246952c0abba5a58c5f48ae92782d9c02660ef6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:42:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 17:42:31 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 17:42:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:49:25 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:49:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:49:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:49:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:49:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:49:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:49:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4aecf4b3c455b15219e7ae2914078c1796d34e6b1c2916aab2fa79d0aecc97`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 318.9 KB (318932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f3e6c459120cfcfb844a46e1d5fa39f425743ad39e3265fdb6b4c4ea312b6`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6977aa451d29e02cfa0a60ee52aadf3bfa7fad7712ac1687007cbb0bd812f996`  
		Last Modified: Wed, 06 May 2020 15:50:14 GMT  
		Size: 11.4 MB (11445896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fc3097b3cd99187dca11658bd33e93e002c8c5cc7de8bc6a29e9ba97d9d405ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14164557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a168a021dfdb6e7170f3f10bb242384bb0946809b89047cc76cd4f0127f74bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 23:22:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 23:22:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 23:23:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:57:29 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:57:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:57:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:57:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:57:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:57:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:57:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:57:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:57:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:57:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:57:43 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:57:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf760b044fed05d609c6cc0dbc0163d673af839c2bd8b93be46a9dd9b3235d8d`  
		Last Modified: Thu, 23 Apr 2020 23:23:51 GMT  
		Size: 317.9 KB (317871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702db93291bb8c691008d86b00d866d87fd9904461e56e447408436f67069d12`  
		Last Modified: Thu, 23 Apr 2020 23:23:50 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a240b5e189e2da028c9e14c55e560dda7eebabe89a0fdc68bd063df8ac5403`  
		Last Modified: Wed, 06 May 2020 15:58:14 GMT  
		Size: 11.4 MB (11418780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:fda3e6c211e921c164d446eb0db4516b3100092ac6906e34142f02d2a1467ed8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14099349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6718b41c65682371b1c36f12939c112979db7a4cabdd180ceb046dc80a3653`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 03:41:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 03:41:27 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 03:41:30 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:39:39 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:39:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:39:44 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:39:45 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:39:47 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:39:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:39:57 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:39:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:40:01 GMT
EXPOSE 80
# Wed, 06 May 2020 16:40:02 GMT
EXPOSE 443
# Wed, 06 May 2020 16:40:04 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:40:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1dd90474a5634d83eea66237a34342ba1aa7b9660127d7a6168f9dd16a6800`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 319.1 KB (319109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523ce157ee2040adfd1d897f97c884c8df6de54df4581f3982d4114fea063843`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45586f3cd2c78aa4e4ec308b720449bd298ff8184489fc23ed1b63329d5bfba`  
		Last Modified: Wed, 06 May 2020 16:40:28 GMT  
		Size: 11.0 MB (11049973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d41420be541ff741166121a337ab2380a37986b80e2c198d33cfa2716b89eebc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14000265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620e8e504bd843011d47928ba3108b784ab917c2b4e49c91f9b5e7a1ed0488e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:29:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:01 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:10 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:25 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:29 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:34 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:31:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:31:03 GMT
EXPOSE 80
# Wed, 06 May 2020 15:31:09 GMT
EXPOSE 443
# Wed, 06 May 2020 15:31:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:31:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5a8966b60d898cbfd9fb53281860fcb82df54d8f66c9142f4038d0e3d8afb8`  
		Last Modified: Wed, 06 May 2020 15:36:35 GMT  
		Size: 321.6 KB (321641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdcee6bf7f07bf2e87c36762756faa63a587b445b5112371d799d9983a38d7f`  
		Last Modified: Wed, 06 May 2020 15:36:34 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912d87d0a8415f3b9ba60c72fc6309c0c67fb08b2834913add34eb8344ce0826`  
		Last Modified: Wed, 06 May 2020 15:36:42 GMT  
		Size: 10.9 MB (10850936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:befbf95ceefa9c63c3cb86d06d19549d32b0e79546b943634e906584a01fec1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14740576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b4e73e6c6c10833f75c31436b5903780a5cf76d6d767633538129d7d9cef2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:30:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:05 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:30:19 GMT
EXPOSE 80
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 443
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:30:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1098bec6a96fa022c5d1e1043cbd10f41d1b5e0788cdeb71e1cbdf3ba0f6b6`  
		Last Modified: Wed, 06 May 2020 15:32:28 GMT  
		Size: 319.2 KB (319200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b06bf33ed224c71042842eaa50af6440423bb48f5cf032ce51277c7d08cb79f`  
		Last Modified: Wed, 06 May 2020 15:32:27 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b3c02c4f07ca031406ddeefa20f1428b199d11370f5548cffe6bf3c294088c`  
		Last Modified: Wed, 06 May 2020 15:32:29 GMT  
		Size: 11.8 MB (11832677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.0.0-builder`

```console
$ docker pull caddy@sha256:28f0cf06fba1b6793c9361e07152168aef953c25bb7926e57a25b376a2e90ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.0.0-builder` - linux; amd64

```console
$ docker pull caddy@sha256:314112e7e538aad27ede8a097431e901de18f3a9f4fed0512816b32116025369
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322819655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588eb5c82cbfc00ca6e34669701cfbd7d65215fd3826e5ae3e7307375001838d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:29:00 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 14:29:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 08:15:50 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 08:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 08:18:10 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 08:18:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 08:18:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 08:18:11 GMT
WORKDIR /go
# Sat, 16 May 2020 17:18:39 GMT
WORKDIR /src
# Sat, 16 May 2020 17:18:40 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 17:18:40 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 17:18:41 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 17:18:42 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 17:18:55 GMT
RUN go get -d ./...
# Sat, 16 May 2020 17:18:56 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 17:18:56 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408f875501273f3af2a9cbff2a23e736585641e73da80dd81712518b28e7843c`  
		Last Modified: Fri, 24 Apr 2020 14:36:50 GMT  
		Size: 301.3 KB (301282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe522b08c9798748151fec9b7a908aca712cd102cfcbb8ed79d57d05b71e6cc4`  
		Last Modified: Fri, 24 Apr 2020 14:36:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246889057fdc27b4bfdcba5f23c6ecb8dbd3fd185b68b5e7360a1c77e1aefda3`  
		Last Modified: Sat, 16 May 2020 08:25:28 GMT  
		Size: 132.1 MB (132107153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526388c839c017e34cf6c6009299d7920b5ac497bf82e303d285e02e7357c624`  
		Last Modified: Sat, 16 May 2020 08:25:07 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e4344283bec8c883625b45b98960f3179decaca01774d777d5f5939325c64e`  
		Last Modified: Sat, 16 May 2020 17:19:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788a8e724dbfdc591bbd3ea4ea12a305c2df8fe785e57f1698f1a8356c72fc09`  
		Last Modified: Sat, 16 May 2020 17:19:06 GMT  
		Size: 8.2 MB (8177808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd575b65357c1c07d5c69f38b32da4715855921770530e306477113b0b70ba0b`  
		Last Modified: Sat, 16 May 2020 17:19:05 GMT  
		Size: 2.7 MB (2706660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6f4a684203b8ecf5843083b75559e27e25f5d19a1169656d2c788b112316e2`  
		Last Modified: Sat, 16 May 2020 17:19:26 GMT  
		Size: 176.7 MB (176712412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d71a8ff7e62ba3ea3e2ea4f399f4192bf32bbc5a3ff2e021afe24ce4387824`  
		Last Modified: Sat, 16 May 2020 17:19:05 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ec187a487fdd916686a8c1b48c3510a916851a10c59e28436d0115a24388a`  
		Last Modified: Sat, 16 May 2020 17:19:05 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67ffeabbdb3a9f1cb9e2ad6cd54232dcdd34982c8385c5dd02c9ff8832abafc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318365877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63190c4a0b594a90ad4c3da68dd98c39a7019a6864b6fa15b72ddc347514306`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:43:41 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 23 Apr 2020 17:43:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 May 2020 20:53:00 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 21:42:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 15 May 2020 21:42:49 GMT
ENV GOPATH=/go
# Fri, 15 May 2020 21:42:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 21:42:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 15 May 2020 21:42:53 GMT
WORKDIR /go
# Fri, 15 May 2020 23:28:04 GMT
WORKDIR /src
# Fri, 15 May 2020 23:28:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 15 May 2020 23:28:07 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Fri, 15 May 2020 23:28:14 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 15 May 2020 23:28:15 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 15 May 2020 23:29:26 GMT
RUN go get -d ./...
# Fri, 15 May 2020 23:29:30 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 15 May 2020 23:29:31 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ace047eafbdd1d41e753db1fd1004be452f749a7de56a3d24b2614a64577f5`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 301.6 KB (301629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d0031acb1953f56f2c2592c1c5882b29aa828d45deccabbb9a1b5483090a43`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22048f6afd75ef565a9cc612911b01c67d897625b9ca36c60b894d6084696f92`  
		Last Modified: Fri, 15 May 2020 22:59:43 GMT  
		Size: 128.2 MB (128224697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b650a1fbc6e89ab4e30a8124c1986a5b57af9f767ce14247c12ab4626406211d`  
		Last Modified: Fri, 15 May 2020 22:58:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2953b4a08d70d0c5e852f46f654fb76fc4a3f4d84c10378f27537298ac4b0bc9`  
		Last Modified: Fri, 15 May 2020 23:29:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca20c0d8a5fd7c97070d7b2afbfbdf070ef8516d1444d97a7aef420012244f8`  
		Last Modified: Fri, 15 May 2020 23:29:47 GMT  
		Size: 7.8 MB (7794700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ae08a0ea808be3631e7222fe61adb555d0e0b72701058ae4c7f7e24990d8f0`  
		Last Modified: Fri, 15 May 2020 23:29:46 GMT  
		Size: 2.7 MB (2706779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4819b2bd69dec9549694cb4f3c2366750c619b6a5750ea944b035e0aa7b1e8c`  
		Last Modified: Fri, 15 May 2020 23:30:32 GMT  
		Size: 176.7 MB (176717010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b429e222d20612559d02209fa2408af52a51ad89b46a1077ca5391f01fb6f05`  
		Last Modified: Fri, 15 May 2020 23:29:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6052a006c556287b947a63516cf4be70b400cb52a23a9a7c55200d505394c706`  
		Last Modified: Fri, 15 May 2020 23:29:45 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9d6434e970f35955684d4641cac3aa549b0c08f4bb862d040261536b655d456f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (317024290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51393629ba564a6804df4ec7bca16f3196ba14ac48f47a9e12a801296e0a471`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:27:40 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 02:27:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 00:47:38 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 01:12:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 01:12:52 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 01:12:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 01:12:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 01:12:55 GMT
WORKDIR /go
# Sat, 16 May 2020 06:38:01 GMT
WORKDIR /src
# Sat, 16 May 2020 06:38:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 06:38:05 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 06:38:13 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 06:38:14 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 06:39:12 GMT
RUN go get -d ./...
# Sat, 16 May 2020 06:39:20 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 06:39:21 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a35d9f7887ef683587262c6f5ed88364f59775ff882c71bde03cc59f382ffd`  
		Last Modified: Fri, 24 Apr 2020 03:39:46 GMT  
		Size: 300.6 KB (300593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce21b09ea3d1107df35d9f41a664183faabfc461b8f093ab8e9a34d91e8e71b`  
		Last Modified: Fri, 24 Apr 2020 03:39:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888e8edf526a315ecceea6785f665113ffce2e1e0c8617daaf91786d53f6fb27`  
		Last Modified: Sat, 16 May 2020 01:57:54 GMT  
		Size: 127.8 MB (127843769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf78654cd341d4acd2a92217585b18547f1b6afc166ac4334420966a2065e4`  
		Last Modified: Sat, 16 May 2020 01:57:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576e21e89111ed713cfd2dc75fe1261b364c56592b204bf170ab6a15dae771a6`  
		Last Modified: Sat, 16 May 2020 06:39:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d9c785f332b55c2da9f65c5c333bdb5d5b344fb2fae6ad8ccbcc14c49eaa9c`  
		Last Modified: Sat, 16 May 2020 06:39:44 GMT  
		Size: 7.0 MB (7026776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a632ccf2a4dfc372007b6d317687a7cd3ae291df232549a54931d4d1dc5615d2`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 2.7 MB (2712787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beceec94d37853479988bfc576c12e97abc44224d1dbcf2658758ebd3c70a54f`  
		Last Modified: Sat, 16 May 2020 06:40:30 GMT  
		Size: 176.7 MB (176717178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcfee5b8c65815cd602ead3301a71126aff85ea944cb5c52ffad126a99dc74d`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845f02b705caa5b416e93e2f497db8bb6c8f8c370b210e564b478adf0047774f`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:85598ec4328ea8e4338167229b822aa78ffccf80b6f7dbaca35db1c6fcf7e245
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317317127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138fc47d6bf2f7d51df909cdd50e870cb5b8a932cdf173c99a7208c096a20995`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 09:30:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 11:38:29 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 11:41:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 11:41:57 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 11:41:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 11:42:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 11:42:00 GMT
WORKDIR /go
# Sat, 16 May 2020 21:07:53 GMT
WORKDIR /src
# Sat, 16 May 2020 21:07:55 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 21:07:56 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 21:08:03 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 21:08:04 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 21:08:32 GMT
RUN go get -d ./...
# Sat, 16 May 2020 21:08:40 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 21:08:41 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fc45ca0357821724e2824e141e2062d236dedad3d8654e0a390419ec9fe393`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 301.8 KB (301770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332e392c90a454bd9f70a303cda942eb0e131e321e82cb70b9346ece4a52a64`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e5db1d0ef9915cb0b4afdfd9e60bb8b3a9b7a84ab2337f7530913f5f409ab0`  
		Last Modified: Sat, 16 May 2020 11:51:50 GMT  
		Size: 126.5 MB (126495381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0906e356942b8e087e8982ed4f04ebdbbb1825a6a7aa3c4524922dc719d32aab`  
		Last Modified: Sat, 16 May 2020 11:51:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65ed62e222b8c20ce0eb3fa80d0ccd2bf5ed567449bb793b530e8673d63b146`  
		Last Modified: Sat, 16 May 2020 21:09:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c2d440dab2e7731db565370b6fc8bd57331ec4b1878bdfd04710c395c20755`  
		Last Modified: Sat, 16 May 2020 21:09:00 GMT  
		Size: 8.4 MB (8365416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c662237ed4d96c57331738fd0a718901532068bdf824ac16ee260c62e8cac115`  
		Last Modified: Sat, 16 May 2020 21:08:59 GMT  
		Size: 2.7 MB (2712771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dee8bbd90b3f06e9a7785463798ffe66608e0c7f8cbf8dba427cad51a7d218`  
		Last Modified: Sat, 16 May 2020 21:09:34 GMT  
		Size: 176.7 MB (176716241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75212b58ca1bfee309442a84fff53deaf5f449a432df0a5ca8040b3c5879e25`  
		Last Modified: Sat, 16 May 2020 21:08:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7d87b1e2fd291b5edc9551976bfbf1b74e2f42ea52a0746422532e8995539d`  
		Last Modified: Sat, 16 May 2020 21:08:59 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:6a3387dae653c19a3d97054a8c741e92b5c58b5ce10073d2739db46953edcb94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316592169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c7582a4a1356df3e5f5a6f0d2b4c5d28518b2c64502f86c9790bc08e912ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:54:40 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 02:54:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 May 2020 14:03:06 GMT
ENV GOLANG_VERSION=1.14.3
# Mon, 18 May 2020 14:05:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Mon, 18 May 2020 14:06:02 GMT
ENV GOPATH=/go
# Mon, 18 May 2020 14:06:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2020 14:06:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Mon, 18 May 2020 14:06:26 GMT
WORKDIR /go
# Tue, 19 May 2020 00:28:09 GMT
WORKDIR /src
# Tue, 19 May 2020 00:28:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 19 May 2020 00:28:20 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Tue, 19 May 2020 00:28:29 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 19 May 2020 00:28:32 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 19 May 2020 00:30:45 GMT
RUN go get -d ./...
# Tue, 19 May 2020 00:30:52 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 19 May 2020 00:30:55 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20efe26326b88a40e960e9cd11fce1b701b2cf370e8328f66fc846d23b5408`  
		Last Modified: Fri, 24 Apr 2020 03:02:11 GMT  
		Size: 304.0 KB (303974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7438e1bdec433812841560459973aca70d85a3b7661615d9c632998dd366f248`  
		Last Modified: Fri, 24 Apr 2020 03:02:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a70b696c0f75daf440b2cb86e131e2aebd5f745ff174e2298f19542b196469`  
		Last Modified: Mon, 18 May 2020 14:24:03 GMT  
		Size: 125.3 MB (125260524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f81ae7b8c66e0e3a08346392ac117ed85d99a7606f57b5a8af24e902e8267c`  
		Last Modified: Mon, 18 May 2020 14:22:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da03111595c5fac6cd7dbb294a0a5856b84ae07b77ac518de6d61bd000010ba`  
		Last Modified: Tue, 19 May 2020 00:31:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be2b93661cbfc2dcbe9e33756005b45eea44bf7d032ff03cd1e4da55cc82987`  
		Last Modified: Tue, 19 May 2020 00:31:16 GMT  
		Size: 8.8 MB (8784618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd33c49ce02b993eb68ea16faf12fb3938bdd2b96e913a10fe1fa01093369a`  
		Last Modified: Tue, 19 May 2020 00:31:15 GMT  
		Size: 2.7 MB (2706163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9009795505c8692ea4c45ff3fea72dc42bacb795b6928b6d8d93bb4e7540d6f3`  
		Last Modified: Tue, 19 May 2020 00:31:41 GMT  
		Size: 176.7 MB (176713920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbc967ec797454f12dac39372f4e53767ed0ecc897d8c896f6ac1bd7cb85a98`  
		Last Modified: Tue, 19 May 2020 00:31:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc607b9110a234b71888aa2de42ac5a665bd241419680e19081e1462f389588`  
		Last Modified: Tue, 19 May 2020 00:31:15 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-builder` - linux; s390x

```console
$ docker pull caddy@sha256:577597322d9dfafa1285515c8fad56c80e2e6666687c460c504ff9057ec8051e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322380651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67498fdb89e44ca98ffe0ed90f15059e1c785c58d997469a86c95815bca8e153`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 20:01:10 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 23 Apr 2020 20:01:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 May 2020 20:44:43 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 20:45:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 15 May 2020 20:45:56 GMT
ENV GOPATH=/go
# Fri, 15 May 2020 20:45:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 20:45:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 15 May 2020 20:45:57 GMT
WORKDIR /go
# Fri, 15 May 2020 21:45:40 GMT
WORKDIR /src
# Fri, 15 May 2020 21:45:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 15 May 2020 21:45:42 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Fri, 15 May 2020 21:45:47 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 15 May 2020 21:45:47 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 15 May 2020 21:46:02 GMT
RUN go get -d ./...
# Fri, 15 May 2020 21:46:09 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 15 May 2020 21:46:09 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bb5699ff3d626466b57d4c92bbf8a5410490fcece2b350c368cad50778b96d`  
		Last Modified: Thu, 23 Apr 2020 20:06:33 GMT  
		Size: 301.9 KB (301908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf86b8de56aab63659ca622083cd8174db3525f6baa42836863267efa18de0e2`  
		Last Modified: Thu, 23 Apr 2020 20:06:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953996d17e01ab26a510ab21d1b8e140a2a82a3a6d470890ee321abc0bd59fd3`  
		Last Modified: Fri, 15 May 2020 20:50:46 GMT  
		Size: 131.9 MB (131858758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8c1c28767148ade729d11932d2312b1410b36186d0a9cde1e36c9ba3d301e`  
		Last Modified: Fri, 15 May 2020 20:50:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ed906c938756832f1f51a17e0d0646a48609eb7bb7748b193efcee9dab0764`  
		Last Modified: Fri, 15 May 2020 21:46:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53c7446c5e8e872a9d2bdfc7cc7f72ca494f91a3e1f8cb14508032e27f6abc2`  
		Last Modified: Fri, 15 May 2020 21:46:22 GMT  
		Size: 8.2 MB (8212441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d78bef69b13c0f6ef34dee6b17c2db47e19e4c33287e433e415481d9b3a3ce9`  
		Last Modified: Fri, 15 May 2020 21:46:21 GMT  
		Size: 2.7 MB (2708215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5eb0f1d42c2b99f724659a6fdfe4ed355920ecd7849c101c2f4fd300bf6f01`  
		Last Modified: Fri, 15 May 2020 21:46:42 GMT  
		Size: 176.7 MB (176715349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473a5b493d958f1054c96c252c5d6147a49bcc11a5262b58b54319e9b9fe558c`  
		Last Modified: Fri, 15 May 2020 21:46:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47634dd72ea6c819d83f449fe1b61d55c6a3866fcf9c2f0cb9fb92e1cf93d341`  
		Last Modified: Fri, 15 May 2020 21:46:52 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.0.0-windowsservercore`

```console
$ docker pull caddy@sha256:eb74da93a470a6eca2a9da48f7cf6a3f3d87d333c4516745c41fef8363cca1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `caddy:2.0.0-windowsservercore` - windows version 10.0.17763.1217; amd64

```console
$ docker pull caddy@sha256:72fb2769c5bca3a826c2d20272955543ae0505293b8a21f9d7be902c4024462d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1731274652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de5663795f5d4dcdda76bf3051f819c10c1b278328fcf09e429e336ca484f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:46:58 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:47:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:47:22 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:47:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:47:52 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:47:53 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:47:54 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:47:55 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:47:56 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:47:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:47:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:48:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:48:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:48:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:48:03 GMT
EXPOSE 80
# Wed, 13 May 2020 18:48:04 GMT
EXPOSE 443
# Wed, 13 May 2020 18:48:05 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:48:22 GMT
RUN caddy version
# Wed, 13 May 2020 18:48:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cc8f1346629803094aa24186a3ffc8662b4a2ee69dc801d795f005d4a0d95`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18106f83313e5d34a070612d3f1c39e8cf8d9848e2b227296adfffd3965ba25d`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 355.3 KB (355269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f287fd10774920755d67b6de43826c118ec5fc4e8f9702a55be22da2df6358`  
		Last Modified: Wed, 13 May 2020 18:53:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffcf71efbb212a67332d8465f099b447811876b9e83c74eec3c01de1fcb9d0`  
		Last Modified: Wed, 13 May 2020 18:53:10 GMT  
		Size: 12.3 MB (12275873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0eb7cc61a3acb2499d87ea010471ade578b24271a239602554546a519ffbf9`  
		Last Modified: Wed, 13 May 2020 18:53:04 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafa5496993eb381a49e7fbbadd58834e3ddc0c0e33a83a2b81965beaa664e0`  
		Last Modified: Wed, 13 May 2020 18:53:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8269f4f8903d1aef05afd562fda930223dee66a331d0047620fd05dfc076caa`  
		Last Modified: Wed, 13 May 2020 18:53:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0ba135849e8ad69d2e177204089724847fea899770d08be4f326960779471`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775de502a9e90f88c9d9c68063a1aed6775b8a8eaa4f680ea12b84c7a86997aa`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8993d7ccb4765510c6cd037e5115c7af0ce11df1c85256085067fdc1fc433`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3755d5c96e8367ee1c769a90f6e6cfc081fdaf18343af918f815188b334e9`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601866b20fd891e3cb277f3f8f172047a2f71d4ff1d97f310c3b94093dc46a50`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01551299aef213dc22bc7224e912b43e5787201c29b0c31153423f15c5db0a94`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a51580e4218eb251ae8f64eadc2ec6762034308a4057de80eb7472494393b`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be3a4f0438b1d7c8f2a308cb89fea8bbe8fb3b40f143a62069975f86ba1b059`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118019e0b8aa2d8afae2f438d7ff8005a9e4099624fab2c12ea86fec750c64f2`  
		Last Modified: Wed, 13 May 2020 18:52:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ef0c9522d683451d62dee32a69cde84172241d69c164110f784f78162e2a0`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b1c41daa7f57c8fe29b16a91ac4e60b636df159ed486ca9f9dc35bab92154`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96904d7376e44abc396e46bb450c2da8dcfba33355155f6240e07a878423a5`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27936f5bc0bfbebee69fb6ffdd7bb368b4894c8388b64ee02ad1c7c467677`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 288.9 KB (288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2f832bbb7958dfa84ad0d27ee64e1f200e10eb27024304f6f7cac63a1be89`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull caddy@sha256:934fdbcbab89ce90c31479b6686014c304c2e4025f40ab12a0184d7d7031e77c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5754870634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3efc2e9d649455a51c1e525b202723307ac0807d3a66606f8b89e8e1722425`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:48:38 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:49:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:49:58 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:51:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:51:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:51:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:51:25 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:51:26 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:51:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:51:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:51:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:51:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:51:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:51:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:51:35 GMT
EXPOSE 80
# Wed, 13 May 2020 18:51:36 GMT
EXPOSE 443
# Wed, 13 May 2020 18:51:37 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:52:21 GMT
RUN caddy version
# Wed, 13 May 2020 18:52:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8d9441a5da81d2777cfc76980d60cc19b098fe856021de5a9895613a07a917`  
		Last Modified: Wed, 13 May 2020 18:54:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c45322765cd792196713eabac6cc04ae89c4fa85c29b1ca626b72c62996f6`  
		Last Modified: Wed, 13 May 2020 18:54:27 GMT  
		Size: 5.4 MB (5392506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b93c4954c5f72c6e382ba1480c3d976f845f42c19bb5e0a085798079bb636`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4516cd556129c57a85ef8c01db6dd2122853c304e58bf1d1594fdd77424509`  
		Last Modified: Wed, 13 May 2020 18:54:26 GMT  
		Size: 17.3 MB (17316249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b2c917ea7e1658aee4b4fa5144174055d3138552746c780d9540a188c3d7`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159ba07aef82e0d25aaef42f0ea5a8f3e9ac5979006bb5cfd717fa2b5979c19`  
		Last Modified: Wed, 13 May 2020 18:54:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed119e58b16c0727c096be5f489492947e6c14fa38726d290d671d3eb0b7ddc`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36668ca695daf89b18a9a9f22a1ab73b9caff740b5fe364c83b8752053bd520a`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda31fec458b3a7161e6b3a2ab63d82bb1ab9291b37081e70941e73a13d4cad6`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31dc3ae4fe27e8327f459ea65e33ab8c62ffdea360d1b9553ed5cae8d21e7b`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0ac6915dd1ededf8d058abfbf5bf18ae61704814448b2017af1b56ac222f`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3813123a037b3f32302ec2832c105f64f7e4a171a7c551709919d2a2fe50`  
		Last Modified: Wed, 13 May 2020 18:54:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5c9c51be87e873c5fd688f518a5287153de163472db0a1b8ef5219ebc4667`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b34839eed5be808ac4292dce3424594ea3cff620ab4c5abbb21d7175165bf`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e296d31b4d6061f26450d68b391b5d96928617c8bc8cbf385721f19db40f13`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a176c2fcfe281888b44bd6b42edc40ecb1f15fa70e3b46a4057a06a461d97`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80eb7786a112e5e30e573401f1db37e107bf00f6dd3cb2d5e4a5bfcff5864e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fc20b2cbd0d3d3009ab3518b6b3df01534f7bf771ac110e8d1d399a1d4c8e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2955b5f7006f6354828c6ed4286cecaf180196b00f8c315c9f6cf796a9cde`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc73cc73e699dfa7d295778821ae30a39417fe6ae6d52ad4d0ab252cf71976`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 250.3 KB (250292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebb1402ecee93e19be9f62d2148b518e2d255f5592ab44f8090e373ccd7eeb`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.0.0-windowsservercore-1809`

```console
$ docker pull caddy@sha256:bede09a6d63958ebd133c5da1d5e2eca5ed0147061b4835cf2d31373c05e815f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `caddy:2.0.0-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull caddy@sha256:72fb2769c5bca3a826c2d20272955543ae0505293b8a21f9d7be902c4024462d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1731274652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de5663795f5d4dcdda76bf3051f819c10c1b278328fcf09e429e336ca484f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:46:58 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:47:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:47:22 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:47:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:47:52 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:47:53 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:47:54 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:47:55 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:47:56 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:47:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:47:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:48:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:48:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:48:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:48:03 GMT
EXPOSE 80
# Wed, 13 May 2020 18:48:04 GMT
EXPOSE 443
# Wed, 13 May 2020 18:48:05 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:48:22 GMT
RUN caddy version
# Wed, 13 May 2020 18:48:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cc8f1346629803094aa24186a3ffc8662b4a2ee69dc801d795f005d4a0d95`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18106f83313e5d34a070612d3f1c39e8cf8d9848e2b227296adfffd3965ba25d`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 355.3 KB (355269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f287fd10774920755d67b6de43826c118ec5fc4e8f9702a55be22da2df6358`  
		Last Modified: Wed, 13 May 2020 18:53:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffcf71efbb212a67332d8465f099b447811876b9e83c74eec3c01de1fcb9d0`  
		Last Modified: Wed, 13 May 2020 18:53:10 GMT  
		Size: 12.3 MB (12275873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0eb7cc61a3acb2499d87ea010471ade578b24271a239602554546a519ffbf9`  
		Last Modified: Wed, 13 May 2020 18:53:04 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafa5496993eb381a49e7fbbadd58834e3ddc0c0e33a83a2b81965beaa664e0`  
		Last Modified: Wed, 13 May 2020 18:53:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8269f4f8903d1aef05afd562fda930223dee66a331d0047620fd05dfc076caa`  
		Last Modified: Wed, 13 May 2020 18:53:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0ba135849e8ad69d2e177204089724847fea899770d08be4f326960779471`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775de502a9e90f88c9d9c68063a1aed6775b8a8eaa4f680ea12b84c7a86997aa`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8993d7ccb4765510c6cd037e5115c7af0ce11df1c85256085067fdc1fc433`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3755d5c96e8367ee1c769a90f6e6cfc081fdaf18343af918f815188b334e9`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601866b20fd891e3cb277f3f8f172047a2f71d4ff1d97f310c3b94093dc46a50`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01551299aef213dc22bc7224e912b43e5787201c29b0c31153423f15c5db0a94`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a51580e4218eb251ae8f64eadc2ec6762034308a4057de80eb7472494393b`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be3a4f0438b1d7c8f2a308cb89fea8bbe8fb3b40f143a62069975f86ba1b059`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118019e0b8aa2d8afae2f438d7ff8005a9e4099624fab2c12ea86fec750c64f2`  
		Last Modified: Wed, 13 May 2020 18:52:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ef0c9522d683451d62dee32a69cde84172241d69c164110f784f78162e2a0`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b1c41daa7f57c8fe29b16a91ac4e60b636df159ed486ca9f9dc35bab92154`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96904d7376e44abc396e46bb450c2da8dcfba33355155f6240e07a878423a5`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27936f5bc0bfbebee69fb6ffdd7bb368b4894c8388b64ee02ad1c7c467677`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 288.9 KB (288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2f832bbb7958dfa84ad0d27ee64e1f200e10eb27024304f6f7cac63a1be89`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.0.0-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:30a4b139e0d207bbd7ffcd349fea87d2de3512fdaccb941fd4da396d9931f484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `caddy:2.0.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull caddy@sha256:934fdbcbab89ce90c31479b6686014c304c2e4025f40ab12a0184d7d7031e77c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5754870634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3efc2e9d649455a51c1e525b202723307ac0807d3a66606f8b89e8e1722425`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:48:38 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:49:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:49:58 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:51:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:51:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:51:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:51:25 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:51:26 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:51:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:51:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:51:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:51:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:51:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:51:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:51:35 GMT
EXPOSE 80
# Wed, 13 May 2020 18:51:36 GMT
EXPOSE 443
# Wed, 13 May 2020 18:51:37 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:52:21 GMT
RUN caddy version
# Wed, 13 May 2020 18:52:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8d9441a5da81d2777cfc76980d60cc19b098fe856021de5a9895613a07a917`  
		Last Modified: Wed, 13 May 2020 18:54:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c45322765cd792196713eabac6cc04ae89c4fa85c29b1ca626b72c62996f6`  
		Last Modified: Wed, 13 May 2020 18:54:27 GMT  
		Size: 5.4 MB (5392506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b93c4954c5f72c6e382ba1480c3d976f845f42c19bb5e0a085798079bb636`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4516cd556129c57a85ef8c01db6dd2122853c304e58bf1d1594fdd77424509`  
		Last Modified: Wed, 13 May 2020 18:54:26 GMT  
		Size: 17.3 MB (17316249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b2c917ea7e1658aee4b4fa5144174055d3138552746c780d9540a188c3d7`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159ba07aef82e0d25aaef42f0ea5a8f3e9ac5979006bb5cfd717fa2b5979c19`  
		Last Modified: Wed, 13 May 2020 18:54:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed119e58b16c0727c096be5f489492947e6c14fa38726d290d671d3eb0b7ddc`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36668ca695daf89b18a9a9f22a1ab73b9caff740b5fe364c83b8752053bd520a`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda31fec458b3a7161e6b3a2ab63d82bb1ab9291b37081e70941e73a13d4cad6`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31dc3ae4fe27e8327f459ea65e33ab8c62ffdea360d1b9553ed5cae8d21e7b`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0ac6915dd1ededf8d058abfbf5bf18ae61704814448b2017af1b56ac222f`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3813123a037b3f32302ec2832c105f64f7e4a171a7c551709919d2a2fe50`  
		Last Modified: Wed, 13 May 2020 18:54:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5c9c51be87e873c5fd688f518a5287153de163472db0a1b8ef5219ebc4667`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b34839eed5be808ac4292dce3424594ea3cff620ab4c5abbb21d7175165bf`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e296d31b4d6061f26450d68b391b5d96928617c8bc8cbf385721f19db40f13`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a176c2fcfe281888b44bd6b42edc40ecb1f15fa70e3b46a4057a06a461d97`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80eb7786a112e5e30e573401f1db37e107bf00f6dd3cb2d5e4a5bfcff5864e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fc20b2cbd0d3d3009ab3518b6b3df01534f7bf771ac110e8d1d399a1d4c8e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2955b5f7006f6354828c6ed4286cecaf180196b00f8c315c9f6cf796a9cde`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc73cc73e699dfa7d295778821ae30a39417fe6ae6d52ad4d0ab252cf71976`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 250.3 KB (250292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebb1402ecee93e19be9f62d2148b518e2d255f5592ab44f8090e373ccd7eeb`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:23d7342a40c9a3961d73d2e2d31a7d18ea84b8bbfb2f189460661614613ffb5d
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
$ docker pull caddy@sha256:5dcf7aba2d86d1bd9d019b4431b683f78e674b0463ca17b2a7f46464bbc62332
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15145219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2721e97adcec739105d14978b5eafb916a9174c643402360ce0397d490c25f49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:39:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 13:39:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 13:39:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 19:20:49 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:21:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 80
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 443
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:21:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c92d2df695a8e1549e487fe6691311b8c3ccfdd90383c6ae37c578c4465c76`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 318.6 KB (318554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d779d752c63b3ccba5c5fbec57ae2361cef2059d83ea0770f389f1d9849ccde`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 5.8 KB (5765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e321d52b548add190f8f5974453da203fc605ed33865ced7b83cc1e8fddc904e`  
		Last Modified: Wed, 06 May 2020 16:21:33 GMT  
		Size: 12.0 MB (12007584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a81d694d3aa6fb71250200e1bd70d07066f22e9ac6a1951b3d6df18d03e12b20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14390606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19bc691ae372dac3178e3250246952c0abba5a58c5f48ae92782d9c02660ef6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:42:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 17:42:31 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 17:42:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:49:25 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:49:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:49:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:49:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:49:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:49:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:49:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4aecf4b3c455b15219e7ae2914078c1796d34e6b1c2916aab2fa79d0aecc97`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 318.9 KB (318932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f3e6c459120cfcfb844a46e1d5fa39f425743ad39e3265fdb6b4c4ea312b6`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6977aa451d29e02cfa0a60ee52aadf3bfa7fad7712ac1687007cbb0bd812f996`  
		Last Modified: Wed, 06 May 2020 15:50:14 GMT  
		Size: 11.4 MB (11445896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fc3097b3cd99187dca11658bd33e93e002c8c5cc7de8bc6a29e9ba97d9d405ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14164557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a168a021dfdb6e7170f3f10bb242384bb0946809b89047cc76cd4f0127f74bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 23:22:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 23:22:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 23:23:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:57:29 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:57:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:57:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:57:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:57:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:57:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:57:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:57:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:57:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:57:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:57:43 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:57:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf760b044fed05d609c6cc0dbc0163d673af839c2bd8b93be46a9dd9b3235d8d`  
		Last Modified: Thu, 23 Apr 2020 23:23:51 GMT  
		Size: 317.9 KB (317871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702db93291bb8c691008d86b00d866d87fd9904461e56e447408436f67069d12`  
		Last Modified: Thu, 23 Apr 2020 23:23:50 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a240b5e189e2da028c9e14c55e560dda7eebabe89a0fdc68bd063df8ac5403`  
		Last Modified: Wed, 06 May 2020 15:58:14 GMT  
		Size: 11.4 MB (11418780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:fda3e6c211e921c164d446eb0db4516b3100092ac6906e34142f02d2a1467ed8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14099349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6718b41c65682371b1c36f12939c112979db7a4cabdd180ceb046dc80a3653`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 03:41:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 03:41:27 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 03:41:30 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:39:39 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:39:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:39:44 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:39:45 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:39:47 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:39:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:39:57 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:39:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:40:01 GMT
EXPOSE 80
# Wed, 06 May 2020 16:40:02 GMT
EXPOSE 443
# Wed, 06 May 2020 16:40:04 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:40:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1dd90474a5634d83eea66237a34342ba1aa7b9660127d7a6168f9dd16a6800`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 319.1 KB (319109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523ce157ee2040adfd1d897f97c884c8df6de54df4581f3982d4114fea063843`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45586f3cd2c78aa4e4ec308b720449bd298ff8184489fc23ed1b63329d5bfba`  
		Last Modified: Wed, 06 May 2020 16:40:28 GMT  
		Size: 11.0 MB (11049973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d41420be541ff741166121a337ab2380a37986b80e2c198d33cfa2716b89eebc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14000265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620e8e504bd843011d47928ba3108b784ab917c2b4e49c91f9b5e7a1ed0488e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:29:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:01 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:10 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:25 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:29 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:34 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:31:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:31:03 GMT
EXPOSE 80
# Wed, 06 May 2020 15:31:09 GMT
EXPOSE 443
# Wed, 06 May 2020 15:31:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:31:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5a8966b60d898cbfd9fb53281860fcb82df54d8f66c9142f4038d0e3d8afb8`  
		Last Modified: Wed, 06 May 2020 15:36:35 GMT  
		Size: 321.6 KB (321641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdcee6bf7f07bf2e87c36762756faa63a587b445b5112371d799d9983a38d7f`  
		Last Modified: Wed, 06 May 2020 15:36:34 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912d87d0a8415f3b9ba60c72fc6309c0c67fb08b2834913add34eb8344ce0826`  
		Last Modified: Wed, 06 May 2020 15:36:42 GMT  
		Size: 10.9 MB (10850936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:befbf95ceefa9c63c3cb86d06d19549d32b0e79546b943634e906584a01fec1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14740576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b4e73e6c6c10833f75c31436b5903780a5cf76d6d767633538129d7d9cef2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:30:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:05 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:30:19 GMT
EXPOSE 80
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 443
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:30:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1098bec6a96fa022c5d1e1043cbd10f41d1b5e0788cdeb71e1cbdf3ba0f6b6`  
		Last Modified: Wed, 06 May 2020 15:32:28 GMT  
		Size: 319.2 KB (319200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b06bf33ed224c71042842eaa50af6440423bb48f5cf032ce51277c7d08cb79f`  
		Last Modified: Wed, 06 May 2020 15:32:27 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b3c02c4f07ca031406ddeefa20f1428b199d11370f5548cffe6bf3c294088c`  
		Last Modified: Wed, 06 May 2020 15:32:29 GMT  
		Size: 11.8 MB (11832677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:28f0cf06fba1b6793c9361e07152168aef953c25bb7926e57a25b376a2e90ebc
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
$ docker pull caddy@sha256:314112e7e538aad27ede8a097431e901de18f3a9f4fed0512816b32116025369
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322819655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588eb5c82cbfc00ca6e34669701cfbd7d65215fd3826e5ae3e7307375001838d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:29:00 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 14:29:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 08:15:50 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 08:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 08:18:10 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 08:18:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 08:18:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 08:18:11 GMT
WORKDIR /go
# Sat, 16 May 2020 17:18:39 GMT
WORKDIR /src
# Sat, 16 May 2020 17:18:40 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 17:18:40 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 17:18:41 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 17:18:42 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 17:18:55 GMT
RUN go get -d ./...
# Sat, 16 May 2020 17:18:56 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 17:18:56 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408f875501273f3af2a9cbff2a23e736585641e73da80dd81712518b28e7843c`  
		Last Modified: Fri, 24 Apr 2020 14:36:50 GMT  
		Size: 301.3 KB (301282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe522b08c9798748151fec9b7a908aca712cd102cfcbb8ed79d57d05b71e6cc4`  
		Last Modified: Fri, 24 Apr 2020 14:36:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246889057fdc27b4bfdcba5f23c6ecb8dbd3fd185b68b5e7360a1c77e1aefda3`  
		Last Modified: Sat, 16 May 2020 08:25:28 GMT  
		Size: 132.1 MB (132107153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526388c839c017e34cf6c6009299d7920b5ac497bf82e303d285e02e7357c624`  
		Last Modified: Sat, 16 May 2020 08:25:07 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e4344283bec8c883625b45b98960f3179decaca01774d777d5f5939325c64e`  
		Last Modified: Sat, 16 May 2020 17:19:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788a8e724dbfdc591bbd3ea4ea12a305c2df8fe785e57f1698f1a8356c72fc09`  
		Last Modified: Sat, 16 May 2020 17:19:06 GMT  
		Size: 8.2 MB (8177808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd575b65357c1c07d5c69f38b32da4715855921770530e306477113b0b70ba0b`  
		Last Modified: Sat, 16 May 2020 17:19:05 GMT  
		Size: 2.7 MB (2706660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6f4a684203b8ecf5843083b75559e27e25f5d19a1169656d2c788b112316e2`  
		Last Modified: Sat, 16 May 2020 17:19:26 GMT  
		Size: 176.7 MB (176712412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d71a8ff7e62ba3ea3e2ea4f399f4192bf32bbc5a3ff2e021afe24ce4387824`  
		Last Modified: Sat, 16 May 2020 17:19:05 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ec187a487fdd916686a8c1b48c3510a916851a10c59e28436d0115a24388a`  
		Last Modified: Sat, 16 May 2020 17:19:05 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67ffeabbdb3a9f1cb9e2ad6cd54232dcdd34982c8385c5dd02c9ff8832abafc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318365877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63190c4a0b594a90ad4c3da68dd98c39a7019a6864b6fa15b72ddc347514306`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:43:41 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 23 Apr 2020 17:43:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 May 2020 20:53:00 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 21:42:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 15 May 2020 21:42:49 GMT
ENV GOPATH=/go
# Fri, 15 May 2020 21:42:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 21:42:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 15 May 2020 21:42:53 GMT
WORKDIR /go
# Fri, 15 May 2020 23:28:04 GMT
WORKDIR /src
# Fri, 15 May 2020 23:28:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 15 May 2020 23:28:07 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Fri, 15 May 2020 23:28:14 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 15 May 2020 23:28:15 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 15 May 2020 23:29:26 GMT
RUN go get -d ./...
# Fri, 15 May 2020 23:29:30 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 15 May 2020 23:29:31 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ace047eafbdd1d41e753db1fd1004be452f749a7de56a3d24b2614a64577f5`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 301.6 KB (301629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d0031acb1953f56f2c2592c1c5882b29aa828d45deccabbb9a1b5483090a43`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22048f6afd75ef565a9cc612911b01c67d897625b9ca36c60b894d6084696f92`  
		Last Modified: Fri, 15 May 2020 22:59:43 GMT  
		Size: 128.2 MB (128224697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b650a1fbc6e89ab4e30a8124c1986a5b57af9f767ce14247c12ab4626406211d`  
		Last Modified: Fri, 15 May 2020 22:58:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2953b4a08d70d0c5e852f46f654fb76fc4a3f4d84c10378f27537298ac4b0bc9`  
		Last Modified: Fri, 15 May 2020 23:29:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca20c0d8a5fd7c97070d7b2afbfbdf070ef8516d1444d97a7aef420012244f8`  
		Last Modified: Fri, 15 May 2020 23:29:47 GMT  
		Size: 7.8 MB (7794700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ae08a0ea808be3631e7222fe61adb555d0e0b72701058ae4c7f7e24990d8f0`  
		Last Modified: Fri, 15 May 2020 23:29:46 GMT  
		Size: 2.7 MB (2706779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4819b2bd69dec9549694cb4f3c2366750c619b6a5750ea944b035e0aa7b1e8c`  
		Last Modified: Fri, 15 May 2020 23:30:32 GMT  
		Size: 176.7 MB (176717010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b429e222d20612559d02209fa2408af52a51ad89b46a1077ca5391f01fb6f05`  
		Last Modified: Fri, 15 May 2020 23:29:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6052a006c556287b947a63516cf4be70b400cb52a23a9a7c55200d505394c706`  
		Last Modified: Fri, 15 May 2020 23:29:45 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9d6434e970f35955684d4641cac3aa549b0c08f4bb862d040261536b655d456f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (317024290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51393629ba564a6804df4ec7bca16f3196ba14ac48f47a9e12a801296e0a471`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:27:40 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 02:27:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 00:47:38 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 01:12:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 01:12:52 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 01:12:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 01:12:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 01:12:55 GMT
WORKDIR /go
# Sat, 16 May 2020 06:38:01 GMT
WORKDIR /src
# Sat, 16 May 2020 06:38:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 06:38:05 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 06:38:13 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 06:38:14 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 06:39:12 GMT
RUN go get -d ./...
# Sat, 16 May 2020 06:39:20 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 06:39:21 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a35d9f7887ef683587262c6f5ed88364f59775ff882c71bde03cc59f382ffd`  
		Last Modified: Fri, 24 Apr 2020 03:39:46 GMT  
		Size: 300.6 KB (300593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce21b09ea3d1107df35d9f41a664183faabfc461b8f093ab8e9a34d91e8e71b`  
		Last Modified: Fri, 24 Apr 2020 03:39:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888e8edf526a315ecceea6785f665113ffce2e1e0c8617daaf91786d53f6fb27`  
		Last Modified: Sat, 16 May 2020 01:57:54 GMT  
		Size: 127.8 MB (127843769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf78654cd341d4acd2a92217585b18547f1b6afc166ac4334420966a2065e4`  
		Last Modified: Sat, 16 May 2020 01:57:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576e21e89111ed713cfd2dc75fe1261b364c56592b204bf170ab6a15dae771a6`  
		Last Modified: Sat, 16 May 2020 06:39:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d9c785f332b55c2da9f65c5c333bdb5d5b344fb2fae6ad8ccbcc14c49eaa9c`  
		Last Modified: Sat, 16 May 2020 06:39:44 GMT  
		Size: 7.0 MB (7026776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a632ccf2a4dfc372007b6d317687a7cd3ae291df232549a54931d4d1dc5615d2`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 2.7 MB (2712787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beceec94d37853479988bfc576c12e97abc44224d1dbcf2658758ebd3c70a54f`  
		Last Modified: Sat, 16 May 2020 06:40:30 GMT  
		Size: 176.7 MB (176717178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcfee5b8c65815cd602ead3301a71126aff85ea944cb5c52ffad126a99dc74d`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845f02b705caa5b416e93e2f497db8bb6c8f8c370b210e564b478adf0047774f`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:85598ec4328ea8e4338167229b822aa78ffccf80b6f7dbaca35db1c6fcf7e245
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317317127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138fc47d6bf2f7d51df909cdd50e870cb5b8a932cdf173c99a7208c096a20995`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 09:30:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 11:38:29 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 11:41:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 11:41:57 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 11:41:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 11:42:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 11:42:00 GMT
WORKDIR /go
# Sat, 16 May 2020 21:07:53 GMT
WORKDIR /src
# Sat, 16 May 2020 21:07:55 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 21:07:56 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 21:08:03 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 21:08:04 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 21:08:32 GMT
RUN go get -d ./...
# Sat, 16 May 2020 21:08:40 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 21:08:41 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fc45ca0357821724e2824e141e2062d236dedad3d8654e0a390419ec9fe393`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 301.8 KB (301770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332e392c90a454bd9f70a303cda942eb0e131e321e82cb70b9346ece4a52a64`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e5db1d0ef9915cb0b4afdfd9e60bb8b3a9b7a84ab2337f7530913f5f409ab0`  
		Last Modified: Sat, 16 May 2020 11:51:50 GMT  
		Size: 126.5 MB (126495381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0906e356942b8e087e8982ed4f04ebdbbb1825a6a7aa3c4524922dc719d32aab`  
		Last Modified: Sat, 16 May 2020 11:51:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65ed62e222b8c20ce0eb3fa80d0ccd2bf5ed567449bb793b530e8673d63b146`  
		Last Modified: Sat, 16 May 2020 21:09:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c2d440dab2e7731db565370b6fc8bd57331ec4b1878bdfd04710c395c20755`  
		Last Modified: Sat, 16 May 2020 21:09:00 GMT  
		Size: 8.4 MB (8365416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c662237ed4d96c57331738fd0a718901532068bdf824ac16ee260c62e8cac115`  
		Last Modified: Sat, 16 May 2020 21:08:59 GMT  
		Size: 2.7 MB (2712771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dee8bbd90b3f06e9a7785463798ffe66608e0c7f8cbf8dba427cad51a7d218`  
		Last Modified: Sat, 16 May 2020 21:09:34 GMT  
		Size: 176.7 MB (176716241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75212b58ca1bfee309442a84fff53deaf5f449a432df0a5ca8040b3c5879e25`  
		Last Modified: Sat, 16 May 2020 21:08:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7d87b1e2fd291b5edc9551976bfbf1b74e2f42ea52a0746422532e8995539d`  
		Last Modified: Sat, 16 May 2020 21:08:59 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:6a3387dae653c19a3d97054a8c741e92b5c58b5ce10073d2739db46953edcb94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316592169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c7582a4a1356df3e5f5a6f0d2b4c5d28518b2c64502f86c9790bc08e912ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:54:40 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 02:54:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 May 2020 14:03:06 GMT
ENV GOLANG_VERSION=1.14.3
# Mon, 18 May 2020 14:05:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Mon, 18 May 2020 14:06:02 GMT
ENV GOPATH=/go
# Mon, 18 May 2020 14:06:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2020 14:06:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Mon, 18 May 2020 14:06:26 GMT
WORKDIR /go
# Tue, 19 May 2020 00:28:09 GMT
WORKDIR /src
# Tue, 19 May 2020 00:28:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 19 May 2020 00:28:20 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Tue, 19 May 2020 00:28:29 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 19 May 2020 00:28:32 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 19 May 2020 00:30:45 GMT
RUN go get -d ./...
# Tue, 19 May 2020 00:30:52 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 19 May 2020 00:30:55 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20efe26326b88a40e960e9cd11fce1b701b2cf370e8328f66fc846d23b5408`  
		Last Modified: Fri, 24 Apr 2020 03:02:11 GMT  
		Size: 304.0 KB (303974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7438e1bdec433812841560459973aca70d85a3b7661615d9c632998dd366f248`  
		Last Modified: Fri, 24 Apr 2020 03:02:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a70b696c0f75daf440b2cb86e131e2aebd5f745ff174e2298f19542b196469`  
		Last Modified: Mon, 18 May 2020 14:24:03 GMT  
		Size: 125.3 MB (125260524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f81ae7b8c66e0e3a08346392ac117ed85d99a7606f57b5a8af24e902e8267c`  
		Last Modified: Mon, 18 May 2020 14:22:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da03111595c5fac6cd7dbb294a0a5856b84ae07b77ac518de6d61bd000010ba`  
		Last Modified: Tue, 19 May 2020 00:31:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be2b93661cbfc2dcbe9e33756005b45eea44bf7d032ff03cd1e4da55cc82987`  
		Last Modified: Tue, 19 May 2020 00:31:16 GMT  
		Size: 8.8 MB (8784618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd33c49ce02b993eb68ea16faf12fb3938bdd2b96e913a10fe1fa01093369a`  
		Last Modified: Tue, 19 May 2020 00:31:15 GMT  
		Size: 2.7 MB (2706163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9009795505c8692ea4c45ff3fea72dc42bacb795b6928b6d8d93bb4e7540d6f3`  
		Last Modified: Tue, 19 May 2020 00:31:41 GMT  
		Size: 176.7 MB (176713920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbc967ec797454f12dac39372f4e53767ed0ecc897d8c896f6ac1bd7cb85a98`  
		Last Modified: Tue, 19 May 2020 00:31:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc607b9110a234b71888aa2de42ac5a665bd241419680e19081e1462f389588`  
		Last Modified: Tue, 19 May 2020 00:31:15 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:577597322d9dfafa1285515c8fad56c80e2e6666687c460c504ff9057ec8051e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322380651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67498fdb89e44ca98ffe0ed90f15059e1c785c58d997469a86c95815bca8e153`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 20:01:10 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 23 Apr 2020 20:01:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 May 2020 20:44:43 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 20:45:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 15 May 2020 20:45:56 GMT
ENV GOPATH=/go
# Fri, 15 May 2020 20:45:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 20:45:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 15 May 2020 20:45:57 GMT
WORKDIR /go
# Fri, 15 May 2020 21:45:40 GMT
WORKDIR /src
# Fri, 15 May 2020 21:45:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 15 May 2020 21:45:42 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Fri, 15 May 2020 21:45:47 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 15 May 2020 21:45:47 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 15 May 2020 21:46:02 GMT
RUN go get -d ./...
# Fri, 15 May 2020 21:46:09 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 15 May 2020 21:46:09 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bb5699ff3d626466b57d4c92bbf8a5410490fcece2b350c368cad50778b96d`  
		Last Modified: Thu, 23 Apr 2020 20:06:33 GMT  
		Size: 301.9 KB (301908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf86b8de56aab63659ca622083cd8174db3525f6baa42836863267efa18de0e2`  
		Last Modified: Thu, 23 Apr 2020 20:06:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953996d17e01ab26a510ab21d1b8e140a2a82a3a6d470890ee321abc0bd59fd3`  
		Last Modified: Fri, 15 May 2020 20:50:46 GMT  
		Size: 131.9 MB (131858758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8c1c28767148ade729d11932d2312b1410b36186d0a9cde1e36c9ba3d301e`  
		Last Modified: Fri, 15 May 2020 20:50:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ed906c938756832f1f51a17e0d0646a48609eb7bb7748b193efcee9dab0764`  
		Last Modified: Fri, 15 May 2020 21:46:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53c7446c5e8e872a9d2bdfc7cc7f72ca494f91a3e1f8cb14508032e27f6abc2`  
		Last Modified: Fri, 15 May 2020 21:46:22 GMT  
		Size: 8.2 MB (8212441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d78bef69b13c0f6ef34dee6b17c2db47e19e4c33287e433e415481d9b3a3ce9`  
		Last Modified: Fri, 15 May 2020 21:46:21 GMT  
		Size: 2.7 MB (2708215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5eb0f1d42c2b99f724659a6fdfe4ed355920ecd7849c101c2f4fd300bf6f01`  
		Last Modified: Fri, 15 May 2020 21:46:42 GMT  
		Size: 176.7 MB (176715349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473a5b493d958f1054c96c252c5d6147a49bcc11a5262b58b54319e9b9fe558c`  
		Last Modified: Fri, 15 May 2020 21:46:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47634dd72ea6c819d83f449fe1b61d55c6a3866fcf9c2f0cb9fb92e1cf93d341`  
		Last Modified: Fri, 15 May 2020 21:46:52 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:eb74da93a470a6eca2a9da48f7cf6a3f3d87d333c4516745c41fef8363cca1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1217; amd64

```console
$ docker pull caddy@sha256:72fb2769c5bca3a826c2d20272955543ae0505293b8a21f9d7be902c4024462d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1731274652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de5663795f5d4dcdda76bf3051f819c10c1b278328fcf09e429e336ca484f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:46:58 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:47:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:47:22 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:47:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:47:52 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:47:53 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:47:54 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:47:55 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:47:56 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:47:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:47:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:48:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:48:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:48:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:48:03 GMT
EXPOSE 80
# Wed, 13 May 2020 18:48:04 GMT
EXPOSE 443
# Wed, 13 May 2020 18:48:05 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:48:22 GMT
RUN caddy version
# Wed, 13 May 2020 18:48:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cc8f1346629803094aa24186a3ffc8662b4a2ee69dc801d795f005d4a0d95`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18106f83313e5d34a070612d3f1c39e8cf8d9848e2b227296adfffd3965ba25d`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 355.3 KB (355269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f287fd10774920755d67b6de43826c118ec5fc4e8f9702a55be22da2df6358`  
		Last Modified: Wed, 13 May 2020 18:53:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffcf71efbb212a67332d8465f099b447811876b9e83c74eec3c01de1fcb9d0`  
		Last Modified: Wed, 13 May 2020 18:53:10 GMT  
		Size: 12.3 MB (12275873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0eb7cc61a3acb2499d87ea010471ade578b24271a239602554546a519ffbf9`  
		Last Modified: Wed, 13 May 2020 18:53:04 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafa5496993eb381a49e7fbbadd58834e3ddc0c0e33a83a2b81965beaa664e0`  
		Last Modified: Wed, 13 May 2020 18:53:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8269f4f8903d1aef05afd562fda930223dee66a331d0047620fd05dfc076caa`  
		Last Modified: Wed, 13 May 2020 18:53:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0ba135849e8ad69d2e177204089724847fea899770d08be4f326960779471`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775de502a9e90f88c9d9c68063a1aed6775b8a8eaa4f680ea12b84c7a86997aa`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8993d7ccb4765510c6cd037e5115c7af0ce11df1c85256085067fdc1fc433`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3755d5c96e8367ee1c769a90f6e6cfc081fdaf18343af918f815188b334e9`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601866b20fd891e3cb277f3f8f172047a2f71d4ff1d97f310c3b94093dc46a50`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01551299aef213dc22bc7224e912b43e5787201c29b0c31153423f15c5db0a94`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a51580e4218eb251ae8f64eadc2ec6762034308a4057de80eb7472494393b`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be3a4f0438b1d7c8f2a308cb89fea8bbe8fb3b40f143a62069975f86ba1b059`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118019e0b8aa2d8afae2f438d7ff8005a9e4099624fab2c12ea86fec750c64f2`  
		Last Modified: Wed, 13 May 2020 18:52:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ef0c9522d683451d62dee32a69cde84172241d69c164110f784f78162e2a0`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b1c41daa7f57c8fe29b16a91ac4e60b636df159ed486ca9f9dc35bab92154`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96904d7376e44abc396e46bb450c2da8dcfba33355155f6240e07a878423a5`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27936f5bc0bfbebee69fb6ffdd7bb368b4894c8388b64ee02ad1c7c467677`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 288.9 KB (288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2f832bbb7958dfa84ad0d27ee64e1f200e10eb27024304f6f7cac63a1be89`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull caddy@sha256:934fdbcbab89ce90c31479b6686014c304c2e4025f40ab12a0184d7d7031e77c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5754870634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3efc2e9d649455a51c1e525b202723307ac0807d3a66606f8b89e8e1722425`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:48:38 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:49:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:49:58 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:51:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:51:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:51:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:51:25 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:51:26 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:51:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:51:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:51:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:51:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:51:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:51:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:51:35 GMT
EXPOSE 80
# Wed, 13 May 2020 18:51:36 GMT
EXPOSE 443
# Wed, 13 May 2020 18:51:37 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:52:21 GMT
RUN caddy version
# Wed, 13 May 2020 18:52:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8d9441a5da81d2777cfc76980d60cc19b098fe856021de5a9895613a07a917`  
		Last Modified: Wed, 13 May 2020 18:54:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c45322765cd792196713eabac6cc04ae89c4fa85c29b1ca626b72c62996f6`  
		Last Modified: Wed, 13 May 2020 18:54:27 GMT  
		Size: 5.4 MB (5392506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b93c4954c5f72c6e382ba1480c3d976f845f42c19bb5e0a085798079bb636`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4516cd556129c57a85ef8c01db6dd2122853c304e58bf1d1594fdd77424509`  
		Last Modified: Wed, 13 May 2020 18:54:26 GMT  
		Size: 17.3 MB (17316249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b2c917ea7e1658aee4b4fa5144174055d3138552746c780d9540a188c3d7`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159ba07aef82e0d25aaef42f0ea5a8f3e9ac5979006bb5cfd717fa2b5979c19`  
		Last Modified: Wed, 13 May 2020 18:54:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed119e58b16c0727c096be5f489492947e6c14fa38726d290d671d3eb0b7ddc`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36668ca695daf89b18a9a9f22a1ab73b9caff740b5fe364c83b8752053bd520a`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda31fec458b3a7161e6b3a2ab63d82bb1ab9291b37081e70941e73a13d4cad6`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31dc3ae4fe27e8327f459ea65e33ab8c62ffdea360d1b9553ed5cae8d21e7b`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0ac6915dd1ededf8d058abfbf5bf18ae61704814448b2017af1b56ac222f`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3813123a037b3f32302ec2832c105f64f7e4a171a7c551709919d2a2fe50`  
		Last Modified: Wed, 13 May 2020 18:54:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5c9c51be87e873c5fd688f518a5287153de163472db0a1b8ef5219ebc4667`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b34839eed5be808ac4292dce3424594ea3cff620ab4c5abbb21d7175165bf`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e296d31b4d6061f26450d68b391b5d96928617c8bc8cbf385721f19db40f13`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a176c2fcfe281888b44bd6b42edc40ecb1f15fa70e3b46a4057a06a461d97`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80eb7786a112e5e30e573401f1db37e107bf00f6dd3cb2d5e4a5bfcff5864e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fc20b2cbd0d3d3009ab3518b6b3df01534f7bf771ac110e8d1d399a1d4c8e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2955b5f7006f6354828c6ed4286cecaf180196b00f8c315c9f6cf796a9cde`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc73cc73e699dfa7d295778821ae30a39417fe6ae6d52ad4d0ab252cf71976`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 250.3 KB (250292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebb1402ecee93e19be9f62d2148b518e2d255f5592ab44f8090e373ccd7eeb`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:bede09a6d63958ebd133c5da1d5e2eca5ed0147061b4835cf2d31373c05e815f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull caddy@sha256:72fb2769c5bca3a826c2d20272955543ae0505293b8a21f9d7be902c4024462d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1731274652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de5663795f5d4dcdda76bf3051f819c10c1b278328fcf09e429e336ca484f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:46:58 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:47:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:47:22 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:47:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:47:52 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:47:53 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:47:54 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:47:55 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:47:56 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:47:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:47:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:48:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:48:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:48:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:48:03 GMT
EXPOSE 80
# Wed, 13 May 2020 18:48:04 GMT
EXPOSE 443
# Wed, 13 May 2020 18:48:05 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:48:22 GMT
RUN caddy version
# Wed, 13 May 2020 18:48:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cc8f1346629803094aa24186a3ffc8662b4a2ee69dc801d795f005d4a0d95`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18106f83313e5d34a070612d3f1c39e8cf8d9848e2b227296adfffd3965ba25d`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 355.3 KB (355269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f287fd10774920755d67b6de43826c118ec5fc4e8f9702a55be22da2df6358`  
		Last Modified: Wed, 13 May 2020 18:53:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffcf71efbb212a67332d8465f099b447811876b9e83c74eec3c01de1fcb9d0`  
		Last Modified: Wed, 13 May 2020 18:53:10 GMT  
		Size: 12.3 MB (12275873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0eb7cc61a3acb2499d87ea010471ade578b24271a239602554546a519ffbf9`  
		Last Modified: Wed, 13 May 2020 18:53:04 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafa5496993eb381a49e7fbbadd58834e3ddc0c0e33a83a2b81965beaa664e0`  
		Last Modified: Wed, 13 May 2020 18:53:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8269f4f8903d1aef05afd562fda930223dee66a331d0047620fd05dfc076caa`  
		Last Modified: Wed, 13 May 2020 18:53:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0ba135849e8ad69d2e177204089724847fea899770d08be4f326960779471`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775de502a9e90f88c9d9c68063a1aed6775b8a8eaa4f680ea12b84c7a86997aa`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8993d7ccb4765510c6cd037e5115c7af0ce11df1c85256085067fdc1fc433`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3755d5c96e8367ee1c769a90f6e6cfc081fdaf18343af918f815188b334e9`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601866b20fd891e3cb277f3f8f172047a2f71d4ff1d97f310c3b94093dc46a50`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01551299aef213dc22bc7224e912b43e5787201c29b0c31153423f15c5db0a94`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a51580e4218eb251ae8f64eadc2ec6762034308a4057de80eb7472494393b`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be3a4f0438b1d7c8f2a308cb89fea8bbe8fb3b40f143a62069975f86ba1b059`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118019e0b8aa2d8afae2f438d7ff8005a9e4099624fab2c12ea86fec750c64f2`  
		Last Modified: Wed, 13 May 2020 18:52:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ef0c9522d683451d62dee32a69cde84172241d69c164110f784f78162e2a0`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b1c41daa7f57c8fe29b16a91ac4e60b636df159ed486ca9f9dc35bab92154`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96904d7376e44abc396e46bb450c2da8dcfba33355155f6240e07a878423a5`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27936f5bc0bfbebee69fb6ffdd7bb368b4894c8388b64ee02ad1c7c467677`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 288.9 KB (288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2f832bbb7958dfa84ad0d27ee64e1f200e10eb27024304f6f7cac63a1be89`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:30a4b139e0d207bbd7ffcd349fea87d2de3512fdaccb941fd4da396d9931f484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull caddy@sha256:934fdbcbab89ce90c31479b6686014c304c2e4025f40ab12a0184d7d7031e77c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5754870634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3efc2e9d649455a51c1e525b202723307ac0807d3a66606f8b89e8e1722425`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:48:38 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:49:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:49:58 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:51:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:51:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:51:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:51:25 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:51:26 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:51:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:51:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:51:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:51:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:51:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:51:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:51:35 GMT
EXPOSE 80
# Wed, 13 May 2020 18:51:36 GMT
EXPOSE 443
# Wed, 13 May 2020 18:51:37 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:52:21 GMT
RUN caddy version
# Wed, 13 May 2020 18:52:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8d9441a5da81d2777cfc76980d60cc19b098fe856021de5a9895613a07a917`  
		Last Modified: Wed, 13 May 2020 18:54:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c45322765cd792196713eabac6cc04ae89c4fa85c29b1ca626b72c62996f6`  
		Last Modified: Wed, 13 May 2020 18:54:27 GMT  
		Size: 5.4 MB (5392506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b93c4954c5f72c6e382ba1480c3d976f845f42c19bb5e0a085798079bb636`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4516cd556129c57a85ef8c01db6dd2122853c304e58bf1d1594fdd77424509`  
		Last Modified: Wed, 13 May 2020 18:54:26 GMT  
		Size: 17.3 MB (17316249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b2c917ea7e1658aee4b4fa5144174055d3138552746c780d9540a188c3d7`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159ba07aef82e0d25aaef42f0ea5a8f3e9ac5979006bb5cfd717fa2b5979c19`  
		Last Modified: Wed, 13 May 2020 18:54:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed119e58b16c0727c096be5f489492947e6c14fa38726d290d671d3eb0b7ddc`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36668ca695daf89b18a9a9f22a1ab73b9caff740b5fe364c83b8752053bd520a`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda31fec458b3a7161e6b3a2ab63d82bb1ab9291b37081e70941e73a13d4cad6`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31dc3ae4fe27e8327f459ea65e33ab8c62ffdea360d1b9553ed5cae8d21e7b`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0ac6915dd1ededf8d058abfbf5bf18ae61704814448b2017af1b56ac222f`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3813123a037b3f32302ec2832c105f64f7e4a171a7c551709919d2a2fe50`  
		Last Modified: Wed, 13 May 2020 18:54:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5c9c51be87e873c5fd688f518a5287153de163472db0a1b8ef5219ebc4667`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b34839eed5be808ac4292dce3424594ea3cff620ab4c5abbb21d7175165bf`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e296d31b4d6061f26450d68b391b5d96928617c8bc8cbf385721f19db40f13`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a176c2fcfe281888b44bd6b42edc40ecb1f15fa70e3b46a4057a06a461d97`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80eb7786a112e5e30e573401f1db37e107bf00f6dd3cb2d5e4a5bfcff5864e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fc20b2cbd0d3d3009ab3518b6b3df01534f7bf771ac110e8d1d399a1d4c8e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2955b5f7006f6354828c6ed4286cecaf180196b00f8c315c9f6cf796a9cde`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc73cc73e699dfa7d295778821ae30a39417fe6ae6d52ad4d0ab252cf71976`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 250.3 KB (250292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebb1402ecee93e19be9f62d2148b518e2d255f5592ab44f8090e373ccd7eeb`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:23d7342a40c9a3961d73d2e2d31a7d18ea84b8bbfb2f189460661614613ffb5d
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
$ docker pull caddy@sha256:5dcf7aba2d86d1bd9d019b4431b683f78e674b0463ca17b2a7f46464bbc62332
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15145219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2721e97adcec739105d14978b5eafb916a9174c643402360ce0397d490c25f49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:39:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 13:39:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 13:39:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 19:20:49 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:21:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 80
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 443
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:21:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c92d2df695a8e1549e487fe6691311b8c3ccfdd90383c6ae37c578c4465c76`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 318.6 KB (318554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d779d752c63b3ccba5c5fbec57ae2361cef2059d83ea0770f389f1d9849ccde`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 5.8 KB (5765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e321d52b548add190f8f5974453da203fc605ed33865ced7b83cc1e8fddc904e`  
		Last Modified: Wed, 06 May 2020 16:21:33 GMT  
		Size: 12.0 MB (12007584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a81d694d3aa6fb71250200e1bd70d07066f22e9ac6a1951b3d6df18d03e12b20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14390606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19bc691ae372dac3178e3250246952c0abba5a58c5f48ae92782d9c02660ef6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:42:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 17:42:31 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 17:42:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:49:25 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:49:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:49:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:49:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:49:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:49:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:49:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4aecf4b3c455b15219e7ae2914078c1796d34e6b1c2916aab2fa79d0aecc97`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 318.9 KB (318932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f3e6c459120cfcfb844a46e1d5fa39f425743ad39e3265fdb6b4c4ea312b6`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6977aa451d29e02cfa0a60ee52aadf3bfa7fad7712ac1687007cbb0bd812f996`  
		Last Modified: Wed, 06 May 2020 15:50:14 GMT  
		Size: 11.4 MB (11445896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fc3097b3cd99187dca11658bd33e93e002c8c5cc7de8bc6a29e9ba97d9d405ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14164557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a168a021dfdb6e7170f3f10bb242384bb0946809b89047cc76cd4f0127f74bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 23:22:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 23:22:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 23:23:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:57:29 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:57:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:57:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:57:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:57:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:57:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:57:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:57:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:57:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:57:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:57:43 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:57:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf760b044fed05d609c6cc0dbc0163d673af839c2bd8b93be46a9dd9b3235d8d`  
		Last Modified: Thu, 23 Apr 2020 23:23:51 GMT  
		Size: 317.9 KB (317871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702db93291bb8c691008d86b00d866d87fd9904461e56e447408436f67069d12`  
		Last Modified: Thu, 23 Apr 2020 23:23:50 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a240b5e189e2da028c9e14c55e560dda7eebabe89a0fdc68bd063df8ac5403`  
		Last Modified: Wed, 06 May 2020 15:58:14 GMT  
		Size: 11.4 MB (11418780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:fda3e6c211e921c164d446eb0db4516b3100092ac6906e34142f02d2a1467ed8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14099349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6718b41c65682371b1c36f12939c112979db7a4cabdd180ceb046dc80a3653`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 03:41:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 03:41:27 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 03:41:30 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:39:39 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:39:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:39:44 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:39:45 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:39:47 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:39:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:39:57 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:39:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:40:01 GMT
EXPOSE 80
# Wed, 06 May 2020 16:40:02 GMT
EXPOSE 443
# Wed, 06 May 2020 16:40:04 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:40:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1dd90474a5634d83eea66237a34342ba1aa7b9660127d7a6168f9dd16a6800`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 319.1 KB (319109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523ce157ee2040adfd1d897f97c884c8df6de54df4581f3982d4114fea063843`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45586f3cd2c78aa4e4ec308b720449bd298ff8184489fc23ed1b63329d5bfba`  
		Last Modified: Wed, 06 May 2020 16:40:28 GMT  
		Size: 11.0 MB (11049973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d41420be541ff741166121a337ab2380a37986b80e2c198d33cfa2716b89eebc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14000265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620e8e504bd843011d47928ba3108b784ab917c2b4e49c91f9b5e7a1ed0488e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:29:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:01 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:10 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:25 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:29 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:34 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:31:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:31:03 GMT
EXPOSE 80
# Wed, 06 May 2020 15:31:09 GMT
EXPOSE 443
# Wed, 06 May 2020 15:31:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:31:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5a8966b60d898cbfd9fb53281860fcb82df54d8f66c9142f4038d0e3d8afb8`  
		Last Modified: Wed, 06 May 2020 15:36:35 GMT  
		Size: 321.6 KB (321641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdcee6bf7f07bf2e87c36762756faa63a587b445b5112371d799d9983a38d7f`  
		Last Modified: Wed, 06 May 2020 15:36:34 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912d87d0a8415f3b9ba60c72fc6309c0c67fb08b2834913add34eb8344ce0826`  
		Last Modified: Wed, 06 May 2020 15:36:42 GMT  
		Size: 10.9 MB (10850936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:befbf95ceefa9c63c3cb86d06d19549d32b0e79546b943634e906584a01fec1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14740576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b4e73e6c6c10833f75c31436b5903780a5cf76d6d767633538129d7d9cef2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:30:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:05 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:30:19 GMT
EXPOSE 80
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 443
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:30:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1098bec6a96fa022c5d1e1043cbd10f41d1b5e0788cdeb71e1cbdf3ba0f6b6`  
		Last Modified: Wed, 06 May 2020 15:32:28 GMT  
		Size: 319.2 KB (319200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b06bf33ed224c71042842eaa50af6440423bb48f5cf032ce51277c7d08cb79f`  
		Last Modified: Wed, 06 May 2020 15:32:27 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b3c02c4f07ca031406ddeefa20f1428b199d11370f5548cffe6bf3c294088c`  
		Last Modified: Wed, 06 May 2020 15:32:29 GMT  
		Size: 11.8 MB (11832677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:28f0cf06fba1b6793c9361e07152168aef953c25bb7926e57a25b376a2e90ebc
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
$ docker pull caddy@sha256:314112e7e538aad27ede8a097431e901de18f3a9f4fed0512816b32116025369
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322819655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588eb5c82cbfc00ca6e34669701cfbd7d65215fd3826e5ae3e7307375001838d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:29:00 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 14:29:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 08:15:50 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 08:18:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 08:18:10 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 08:18:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 08:18:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 08:18:11 GMT
WORKDIR /go
# Sat, 16 May 2020 17:18:39 GMT
WORKDIR /src
# Sat, 16 May 2020 17:18:40 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 17:18:40 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 17:18:41 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 17:18:42 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 17:18:55 GMT
RUN go get -d ./...
# Sat, 16 May 2020 17:18:56 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 17:18:56 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408f875501273f3af2a9cbff2a23e736585641e73da80dd81712518b28e7843c`  
		Last Modified: Fri, 24 Apr 2020 14:36:50 GMT  
		Size: 301.3 KB (301282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe522b08c9798748151fec9b7a908aca712cd102cfcbb8ed79d57d05b71e6cc4`  
		Last Modified: Fri, 24 Apr 2020 14:36:50 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246889057fdc27b4bfdcba5f23c6ecb8dbd3fd185b68b5e7360a1c77e1aefda3`  
		Last Modified: Sat, 16 May 2020 08:25:28 GMT  
		Size: 132.1 MB (132107153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526388c839c017e34cf6c6009299d7920b5ac497bf82e303d285e02e7357c624`  
		Last Modified: Sat, 16 May 2020 08:25:07 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e4344283bec8c883625b45b98960f3179decaca01774d777d5f5939325c64e`  
		Last Modified: Sat, 16 May 2020 17:19:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788a8e724dbfdc591bbd3ea4ea12a305c2df8fe785e57f1698f1a8356c72fc09`  
		Last Modified: Sat, 16 May 2020 17:19:06 GMT  
		Size: 8.2 MB (8177808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd575b65357c1c07d5c69f38b32da4715855921770530e306477113b0b70ba0b`  
		Last Modified: Sat, 16 May 2020 17:19:05 GMT  
		Size: 2.7 MB (2706660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6f4a684203b8ecf5843083b75559e27e25f5d19a1169656d2c788b112316e2`  
		Last Modified: Sat, 16 May 2020 17:19:26 GMT  
		Size: 176.7 MB (176712412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d71a8ff7e62ba3ea3e2ea4f399f4192bf32bbc5a3ff2e021afe24ce4387824`  
		Last Modified: Sat, 16 May 2020 17:19:05 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ec187a487fdd916686a8c1b48c3510a916851a10c59e28436d0115a24388a`  
		Last Modified: Sat, 16 May 2020 17:19:05 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67ffeabbdb3a9f1cb9e2ad6cd54232dcdd34982c8385c5dd02c9ff8832abafc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318365877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63190c4a0b594a90ad4c3da68dd98c39a7019a6864b6fa15b72ddc347514306`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:43:41 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 23 Apr 2020 17:43:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 May 2020 20:53:00 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 21:42:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 15 May 2020 21:42:49 GMT
ENV GOPATH=/go
# Fri, 15 May 2020 21:42:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 21:42:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 15 May 2020 21:42:53 GMT
WORKDIR /go
# Fri, 15 May 2020 23:28:04 GMT
WORKDIR /src
# Fri, 15 May 2020 23:28:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 15 May 2020 23:28:07 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Fri, 15 May 2020 23:28:14 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 15 May 2020 23:28:15 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 15 May 2020 23:29:26 GMT
RUN go get -d ./...
# Fri, 15 May 2020 23:29:30 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 15 May 2020 23:29:31 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ace047eafbdd1d41e753db1fd1004be452f749a7de56a3d24b2614a64577f5`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 301.6 KB (301629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d0031acb1953f56f2c2592c1c5882b29aa828d45deccabbb9a1b5483090a43`  
		Last Modified: Thu, 23 Apr 2020 18:03:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22048f6afd75ef565a9cc612911b01c67d897625b9ca36c60b894d6084696f92`  
		Last Modified: Fri, 15 May 2020 22:59:43 GMT  
		Size: 128.2 MB (128224697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b650a1fbc6e89ab4e30a8124c1986a5b57af9f767ce14247c12ab4626406211d`  
		Last Modified: Fri, 15 May 2020 22:58:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2953b4a08d70d0c5e852f46f654fb76fc4a3f4d84c10378f27537298ac4b0bc9`  
		Last Modified: Fri, 15 May 2020 23:29:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca20c0d8a5fd7c97070d7b2afbfbdf070ef8516d1444d97a7aef420012244f8`  
		Last Modified: Fri, 15 May 2020 23:29:47 GMT  
		Size: 7.8 MB (7794700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ae08a0ea808be3631e7222fe61adb555d0e0b72701058ae4c7f7e24990d8f0`  
		Last Modified: Fri, 15 May 2020 23:29:46 GMT  
		Size: 2.7 MB (2706779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4819b2bd69dec9549694cb4f3c2366750c619b6a5750ea944b035e0aa7b1e8c`  
		Last Modified: Fri, 15 May 2020 23:30:32 GMT  
		Size: 176.7 MB (176717010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b429e222d20612559d02209fa2408af52a51ad89b46a1077ca5391f01fb6f05`  
		Last Modified: Fri, 15 May 2020 23:29:45 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6052a006c556287b947a63516cf4be70b400cb52a23a9a7c55200d505394c706`  
		Last Modified: Fri, 15 May 2020 23:29:45 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:9d6434e970f35955684d4641cac3aa549b0c08f4bb862d040261536b655d456f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (317024290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51393629ba564a6804df4ec7bca16f3196ba14ac48f47a9e12a801296e0a471`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:27:40 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 02:27:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 00:47:38 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 01:12:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 01:12:52 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 01:12:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 01:12:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 01:12:55 GMT
WORKDIR /go
# Sat, 16 May 2020 06:38:01 GMT
WORKDIR /src
# Sat, 16 May 2020 06:38:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 06:38:05 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 06:38:13 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 06:38:14 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 06:39:12 GMT
RUN go get -d ./...
# Sat, 16 May 2020 06:39:20 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 06:39:21 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a35d9f7887ef683587262c6f5ed88364f59775ff882c71bde03cc59f382ffd`  
		Last Modified: Fri, 24 Apr 2020 03:39:46 GMT  
		Size: 300.6 KB (300593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce21b09ea3d1107df35d9f41a664183faabfc461b8f093ab8e9a34d91e8e71b`  
		Last Modified: Fri, 24 Apr 2020 03:39:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888e8edf526a315ecceea6785f665113ffce2e1e0c8617daaf91786d53f6fb27`  
		Last Modified: Sat, 16 May 2020 01:57:54 GMT  
		Size: 127.8 MB (127843769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf78654cd341d4acd2a92217585b18547f1b6afc166ac4334420966a2065e4`  
		Last Modified: Sat, 16 May 2020 01:57:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576e21e89111ed713cfd2dc75fe1261b364c56592b204bf170ab6a15dae771a6`  
		Last Modified: Sat, 16 May 2020 06:39:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d9c785f332b55c2da9f65c5c333bdb5d5b344fb2fae6ad8ccbcc14c49eaa9c`  
		Last Modified: Sat, 16 May 2020 06:39:44 GMT  
		Size: 7.0 MB (7026776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a632ccf2a4dfc372007b6d317687a7cd3ae291df232549a54931d4d1dc5615d2`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 2.7 MB (2712787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beceec94d37853479988bfc576c12e97abc44224d1dbcf2658758ebd3c70a54f`  
		Last Modified: Sat, 16 May 2020 06:40:30 GMT  
		Size: 176.7 MB (176717178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcfee5b8c65815cd602ead3301a71126aff85ea944cb5c52ffad126a99dc74d`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845f02b705caa5b416e93e2f497db8bb6c8f8c370b210e564b478adf0047774f`  
		Last Modified: Sat, 16 May 2020 06:39:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:85598ec4328ea8e4338167229b822aa78ffccf80b6f7dbaca35db1c6fcf7e245
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317317127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138fc47d6bf2f7d51df909cdd50e870cb5b8a932cdf173c99a7208c096a20995`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 09:30:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 May 2020 11:38:29 GMT
ENV GOLANG_VERSION=1.14.3
# Sat, 16 May 2020 11:41:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 16 May 2020 11:41:57 GMT
ENV GOPATH=/go
# Sat, 16 May 2020 11:41:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 May 2020 11:42:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 16 May 2020 11:42:00 GMT
WORKDIR /go
# Sat, 16 May 2020 21:07:53 GMT
WORKDIR /src
# Sat, 16 May 2020 21:07:55 GMT
RUN apk add --no-cache     git     ca-certificates
# Sat, 16 May 2020 21:07:56 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Sat, 16 May 2020 21:08:03 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Sat, 16 May 2020 21:08:04 GMT
WORKDIR /src/caddy/cmd/caddy
# Sat, 16 May 2020 21:08:32 GMT
RUN go get -d ./...
# Sat, 16 May 2020 21:08:40 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Sat, 16 May 2020 21:08:41 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fc45ca0357821724e2824e141e2062d236dedad3d8654e0a390419ec9fe393`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 301.8 KB (301770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6332e392c90a454bd9f70a303cda942eb0e131e321e82cb70b9346ece4a52a64`  
		Last Modified: Fri, 24 Apr 2020 09:38:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e5db1d0ef9915cb0b4afdfd9e60bb8b3a9b7a84ab2337f7530913f5f409ab0`  
		Last Modified: Sat, 16 May 2020 11:51:50 GMT  
		Size: 126.5 MB (126495381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0906e356942b8e087e8982ed4f04ebdbbb1825a6a7aa3c4524922dc719d32aab`  
		Last Modified: Sat, 16 May 2020 11:51:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65ed62e222b8c20ce0eb3fa80d0ccd2bf5ed567449bb793b530e8673d63b146`  
		Last Modified: Sat, 16 May 2020 21:09:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c2d440dab2e7731db565370b6fc8bd57331ec4b1878bdfd04710c395c20755`  
		Last Modified: Sat, 16 May 2020 21:09:00 GMT  
		Size: 8.4 MB (8365416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c662237ed4d96c57331738fd0a718901532068bdf824ac16ee260c62e8cac115`  
		Last Modified: Sat, 16 May 2020 21:08:59 GMT  
		Size: 2.7 MB (2712771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dee8bbd90b3f06e9a7785463798ffe66608e0c7f8cbf8dba427cad51a7d218`  
		Last Modified: Sat, 16 May 2020 21:09:34 GMT  
		Size: 176.7 MB (176716241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75212b58ca1bfee309442a84fff53deaf5f449a432df0a5ca8040b3c5879e25`  
		Last Modified: Sat, 16 May 2020 21:08:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7d87b1e2fd291b5edc9551976bfbf1b74e2f42ea52a0746422532e8995539d`  
		Last Modified: Sat, 16 May 2020 21:08:59 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:6a3387dae653c19a3d97054a8c741e92b5c58b5ce10073d2739db46953edcb94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316592169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c7582a4a1356df3e5f5a6f0d2b4c5d28518b2c64502f86c9790bc08e912ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:54:40 GMT
RUN apk add --no-cache 		ca-certificates
# Fri, 24 Apr 2020 02:54:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 May 2020 14:03:06 GMT
ENV GOLANG_VERSION=1.14.3
# Mon, 18 May 2020 14:05:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Mon, 18 May 2020 14:06:02 GMT
ENV GOPATH=/go
# Mon, 18 May 2020 14:06:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 May 2020 14:06:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Mon, 18 May 2020 14:06:26 GMT
WORKDIR /go
# Tue, 19 May 2020 00:28:09 GMT
WORKDIR /src
# Tue, 19 May 2020 00:28:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 19 May 2020 00:28:20 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Tue, 19 May 2020 00:28:29 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 19 May 2020 00:28:32 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 19 May 2020 00:30:45 GMT
RUN go get -d ./...
# Tue, 19 May 2020 00:30:52 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 19 May 2020 00:30:55 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20efe26326b88a40e960e9cd11fce1b701b2cf370e8328f66fc846d23b5408`  
		Last Modified: Fri, 24 Apr 2020 03:02:11 GMT  
		Size: 304.0 KB (303974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7438e1bdec433812841560459973aca70d85a3b7661615d9c632998dd366f248`  
		Last Modified: Fri, 24 Apr 2020 03:02:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a70b696c0f75daf440b2cb86e131e2aebd5f745ff174e2298f19542b196469`  
		Last Modified: Mon, 18 May 2020 14:24:03 GMT  
		Size: 125.3 MB (125260524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f81ae7b8c66e0e3a08346392ac117ed85d99a7606f57b5a8af24e902e8267c`  
		Last Modified: Mon, 18 May 2020 14:22:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da03111595c5fac6cd7dbb294a0a5856b84ae07b77ac518de6d61bd000010ba`  
		Last Modified: Tue, 19 May 2020 00:31:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be2b93661cbfc2dcbe9e33756005b45eea44bf7d032ff03cd1e4da55cc82987`  
		Last Modified: Tue, 19 May 2020 00:31:16 GMT  
		Size: 8.8 MB (8784618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd33c49ce02b993eb68ea16faf12fb3938bdd2b96e913a10fe1fa01093369a`  
		Last Modified: Tue, 19 May 2020 00:31:15 GMT  
		Size: 2.7 MB (2706163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9009795505c8692ea4c45ff3fea72dc42bacb795b6928b6d8d93bb4e7540d6f3`  
		Last Modified: Tue, 19 May 2020 00:31:41 GMT  
		Size: 176.7 MB (176713920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbc967ec797454f12dac39372f4e53767ed0ecc897d8c896f6ac1bd7cb85a98`  
		Last Modified: Tue, 19 May 2020 00:31:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc607b9110a234b71888aa2de42ac5a665bd241419680e19081e1462f389588`  
		Last Modified: Tue, 19 May 2020 00:31:15 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:577597322d9dfafa1285515c8fad56c80e2e6666687c460c504ff9057ec8051e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322380651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67498fdb89e44ca98ffe0ed90f15059e1c785c58d997469a86c95815bca8e153`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 20:01:10 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 23 Apr 2020 20:01:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 May 2020 20:44:43 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 20:45:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '93023778d4d1797b7bc6a53e86c3a9b150c923953225f8a48a2d5fabc971af56 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 15 May 2020 20:45:56 GMT
ENV GOPATH=/go
# Fri, 15 May 2020 20:45:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 20:45:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 15 May 2020 20:45:57 GMT
WORKDIR /go
# Fri, 15 May 2020 21:45:40 GMT
WORKDIR /src
# Fri, 15 May 2020 21:45:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 15 May 2020 21:45:42 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0
# Fri, 15 May 2020 21:45:47 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 15 May 2020 21:45:47 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 15 May 2020 21:46:02 GMT
RUN go get -d ./...
# Fri, 15 May 2020 21:46:09 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Fri, 15 May 2020 21:46:09 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bb5699ff3d626466b57d4c92bbf8a5410490fcece2b350c368cad50778b96d`  
		Last Modified: Thu, 23 Apr 2020 20:06:33 GMT  
		Size: 301.9 KB (301908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf86b8de56aab63659ca622083cd8174db3525f6baa42836863267efa18de0e2`  
		Last Modified: Thu, 23 Apr 2020 20:06:33 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953996d17e01ab26a510ab21d1b8e140a2a82a3a6d470890ee321abc0bd59fd3`  
		Last Modified: Fri, 15 May 2020 20:50:46 GMT  
		Size: 131.9 MB (131858758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef8c1c28767148ade729d11932d2312b1410b36186d0a9cde1e36c9ba3d301e`  
		Last Modified: Fri, 15 May 2020 20:50:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ed906c938756832f1f51a17e0d0646a48609eb7bb7748b193efcee9dab0764`  
		Last Modified: Fri, 15 May 2020 21:46:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53c7446c5e8e872a9d2bdfc7cc7f72ca494f91a3e1f8cb14508032e27f6abc2`  
		Last Modified: Fri, 15 May 2020 21:46:22 GMT  
		Size: 8.2 MB (8212441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d78bef69b13c0f6ef34dee6b17c2db47e19e4c33287e433e415481d9b3a3ce9`  
		Last Modified: Fri, 15 May 2020 21:46:21 GMT  
		Size: 2.7 MB (2708215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5eb0f1d42c2b99f724659a6fdfe4ed355920ecd7849c101c2f4fd300bf6f01`  
		Last Modified: Fri, 15 May 2020 21:46:42 GMT  
		Size: 176.7 MB (176715349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473a5b493d958f1054c96c252c5d6147a49bcc11a5262b58b54319e9b9fe558c`  
		Last Modified: Fri, 15 May 2020 21:46:52 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47634dd72ea6c819d83f449fe1b61d55c6a3866fcf9c2f0cb9fb92e1cf93d341`  
		Last Modified: Fri, 15 May 2020 21:46:52 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:a318e53203be65b120d2bfc2a887838fe32bcc839c02df83571d101429bc4f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:5dcf7aba2d86d1bd9d019b4431b683f78e674b0463ca17b2a7f46464bbc62332
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15145219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2721e97adcec739105d14978b5eafb916a9174c643402360ce0397d490c25f49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 13:39:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 13:39:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 13:39:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 19:20:49 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:21:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:21:10 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:21:11 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:21:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:21:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 80
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 443
# Wed, 06 May 2020 16:21:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:21:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c92d2df695a8e1549e487fe6691311b8c3ccfdd90383c6ae37c578c4465c76`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 318.6 KB (318554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d779d752c63b3ccba5c5fbec57ae2361cef2059d83ea0770f389f1d9849ccde`  
		Last Modified: Fri, 24 Apr 2020 13:39:22 GMT  
		Size: 5.8 KB (5765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e321d52b548add190f8f5974453da203fc605ed33865ced7b83cc1e8fddc904e`  
		Last Modified: Wed, 06 May 2020 16:21:33 GMT  
		Size: 12.0 MB (12007584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a81d694d3aa6fb71250200e1bd70d07066f22e9ac6a1951b3d6df18d03e12b20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14390606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19bc691ae372dac3178e3250246952c0abba5a58c5f48ae92782d9c02660ef6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 17:42:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 17:42:31 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 17:42:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:49:25 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:49:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:49:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:49:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:49:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:49:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:49:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:49:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:49:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:49:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:49:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:49:42 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4aecf4b3c455b15219e7ae2914078c1796d34e6b1c2916aab2fa79d0aecc97`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 318.9 KB (318932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f3e6c459120cfcfb844a46e1d5fa39f425743ad39e3265fdb6b4c4ea312b6`  
		Last Modified: Thu, 23 Apr 2020 17:43:07 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6977aa451d29e02cfa0a60ee52aadf3bfa7fad7712ac1687007cbb0bd812f996`  
		Last Modified: Wed, 06 May 2020 15:50:14 GMT  
		Size: 11.4 MB (11445896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fc3097b3cd99187dca11658bd33e93e002c8c5cc7de8bc6a29e9ba97d9d405ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14164557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a168a021dfdb6e7170f3f10bb242384bb0946809b89047cc76cd4f0127f74bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 23:22:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 23 Apr 2020 23:22:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 23 Apr 2020 23:23:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:57:29 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:57:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:57:34 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:57:35 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:57:36 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:57:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:57:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:57:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:57:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:57:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:57:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:57:41 GMT
EXPOSE 80
# Wed, 06 May 2020 15:57:42 GMT
EXPOSE 443
# Wed, 06 May 2020 15:57:43 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:57:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf760b044fed05d609c6cc0dbc0163d673af839c2bd8b93be46a9dd9b3235d8d`  
		Last Modified: Thu, 23 Apr 2020 23:23:51 GMT  
		Size: 317.9 KB (317871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702db93291bb8c691008d86b00d866d87fd9904461e56e447408436f67069d12`  
		Last Modified: Thu, 23 Apr 2020 23:23:50 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a240b5e189e2da028c9e14c55e560dda7eebabe89a0fdc68bd063df8ac5403`  
		Last Modified: Wed, 06 May 2020 15:58:14 GMT  
		Size: 11.4 MB (11418780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:fda3e6c211e921c164d446eb0db4516b3100092ac6906e34142f02d2a1467ed8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14099349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6718b41c65682371b1c36f12939c112979db7a4cabdd180ceb046dc80a3653`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 03:41:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 24 Apr 2020 03:41:27 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Fri, 24 Apr 2020 03:41:30 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Mon, 04 May 2020 18:39:39 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 16:39:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 16:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 16:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 16:39:44 GMT
VOLUME [/config]
# Wed, 06 May 2020 16:39:45 GMT
VOLUME [/data]
# Wed, 06 May 2020 16:39:47 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 16:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 16:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 16:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 16:39:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 16:39:56 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 16:39:57 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 16:39:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 16:40:01 GMT
EXPOSE 80
# Wed, 06 May 2020 16:40:02 GMT
EXPOSE 443
# Wed, 06 May 2020 16:40:04 GMT
EXPOSE 2019
# Wed, 06 May 2020 16:40:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1dd90474a5634d83eea66237a34342ba1aa7b9660127d7a6168f9dd16a6800`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 319.1 KB (319109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523ce157ee2040adfd1d897f97c884c8df6de54df4581f3982d4114fea063843`  
		Last Modified: Fri, 24 Apr 2020 03:42:02 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45586f3cd2c78aa4e4ec308b720449bd298ff8184489fc23ed1b63329d5bfba`  
		Last Modified: Wed, 06 May 2020 16:40:28 GMT  
		Size: 11.0 MB (11049973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:d41420be541ff741166121a337ab2380a37986b80e2c198d33cfa2716b89eebc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14000265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620e8e504bd843011d47928ba3108b784ab917c2b4e49c91f9b5e7a1ed0488e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:29:56 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:01 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:10 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:25 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:29 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:34 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:36 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:31:01 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:31:03 GMT
EXPOSE 80
# Wed, 06 May 2020 15:31:09 GMT
EXPOSE 443
# Wed, 06 May 2020 15:31:13 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:31:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5a8966b60d898cbfd9fb53281860fcb82df54d8f66c9142f4038d0e3d8afb8`  
		Last Modified: Wed, 06 May 2020 15:36:35 GMT  
		Size: 321.6 KB (321641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdcee6bf7f07bf2e87c36762756faa63a587b445b5112371d799d9983a38d7f`  
		Last Modified: Wed, 06 May 2020 15:36:34 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912d87d0a8415f3b9ba60c72fc6309c0c67fb08b2834913add34eb8344ce0826`  
		Last Modified: Wed, 06 May 2020 15:36:42 GMT  
		Size: 10.9 MB (10850936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:befbf95ceefa9c63c3cb86d06d19549d32b0e79546b943634e906584a01fec1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14740576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b4e73e6c6c10833f75c31436b5903780a5cf76d6d767633538129d7d9cef2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2020 15:30:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 06 May 2020 15:30:03 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 06 May 2020 15:30:05 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 06 May 2020 15:30:05 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 06 May 2020 15:30:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='3b00c705caa3162750dfea9cacd3f05ae1dda798e346293ba320ee63682a94e5e26c994fee75677324d841962757b098d2f696e4c5a0044131a0cd9b0e54b9fd' ;; 		armhf)   binArch='armv6'; checksum='c8d054eed16910a3fe84d275b3705f61dab204572d5afac4ca02e735fc5741823413e749dcaa9055f930cf8bbaf7a7c28e3cec94527d44111e3de7ed990d685f' ;; 		armv7)   binArch='armv7'; checksum='786fab05ea32e24d3b36b020087b9e05cac507f5b0677b398730ecbd3559030574c7b0c6ff3950978678ee218afa8b912731a31ce187c28d1c19375c5c742a96' ;; 		aarch64) binArch='arm64'; checksum='8864e9bfa0007f2c8fc0823a729b02e8eb53d41857b4b7ce419102e11a225a975420b36e926c754b2247acc286cbb06fcb705f8cc7258ea1c5f3aea0dc3b44f1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2440fed6d7e240cedc92fd570893ad056195386e369960e1fba3a4de5dbce32871e809841acc926b0cef0afb6ded39073748afe9c39745fb5609472d495d2828' ;; 		s390x)   binArch='s390x'; checksum='b09561e089a0d2deeedfccbd8f0a608068dbc986dc7f1118f0a24e50b5173d90482e1105f9e3249381f2d4815ca316fb7e343fed82b75ea2b070c039bd76324b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 06 May 2020 15:30:13 GMT
ENV XDG_DATA_HOME=/data
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/config]
# Wed, 06 May 2020 15:30:14 GMT
VOLUME [/data]
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 06 May 2020 15:30:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 06 May 2020 15:30:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 06 May 2020 15:30:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 06 May 2020 15:30:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 06 May 2020 15:30:19 GMT
EXPOSE 80
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 443
# Wed, 06 May 2020 15:30:20 GMT
EXPOSE 2019
# Wed, 06 May 2020 15:30:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1098bec6a96fa022c5d1e1043cbd10f41d1b5e0788cdeb71e1cbdf3ba0f6b6`  
		Last Modified: Wed, 06 May 2020 15:32:28 GMT  
		Size: 319.2 KB (319200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b06bf33ed224c71042842eaa50af6440423bb48f5cf032ce51277c7d08cb79f`  
		Last Modified: Wed, 06 May 2020 15:32:27 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b3c02c4f07ca031406ddeefa20f1428b199d11370f5548cffe6bf3c294088c`  
		Last Modified: Wed, 06 May 2020 15:32:29 GMT  
		Size: 11.8 MB (11832677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.1217; amd64

```console
$ docker pull caddy@sha256:72fb2769c5bca3a826c2d20272955543ae0505293b8a21f9d7be902c4024462d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1731274652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de5663795f5d4dcdda76bf3051f819c10c1b278328fcf09e429e336ca484f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:46:58 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:47:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:47:22 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:47:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:47:52 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:47:53 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:47:54 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:47:55 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:47:56 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:47:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:47:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:48:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:48:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:48:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:48:03 GMT
EXPOSE 80
# Wed, 13 May 2020 18:48:04 GMT
EXPOSE 443
# Wed, 13 May 2020 18:48:05 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:48:22 GMT
RUN caddy version
# Wed, 13 May 2020 18:48:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cc8f1346629803094aa24186a3ffc8662b4a2ee69dc801d795f005d4a0d95`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18106f83313e5d34a070612d3f1c39e8cf8d9848e2b227296adfffd3965ba25d`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 355.3 KB (355269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f287fd10774920755d67b6de43826c118ec5fc4e8f9702a55be22da2df6358`  
		Last Modified: Wed, 13 May 2020 18:53:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffcf71efbb212a67332d8465f099b447811876b9e83c74eec3c01de1fcb9d0`  
		Last Modified: Wed, 13 May 2020 18:53:10 GMT  
		Size: 12.3 MB (12275873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0eb7cc61a3acb2499d87ea010471ade578b24271a239602554546a519ffbf9`  
		Last Modified: Wed, 13 May 2020 18:53:04 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafa5496993eb381a49e7fbbadd58834e3ddc0c0e33a83a2b81965beaa664e0`  
		Last Modified: Wed, 13 May 2020 18:53:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8269f4f8903d1aef05afd562fda930223dee66a331d0047620fd05dfc076caa`  
		Last Modified: Wed, 13 May 2020 18:53:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0ba135849e8ad69d2e177204089724847fea899770d08be4f326960779471`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775de502a9e90f88c9d9c68063a1aed6775b8a8eaa4f680ea12b84c7a86997aa`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8993d7ccb4765510c6cd037e5115c7af0ce11df1c85256085067fdc1fc433`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3755d5c96e8367ee1c769a90f6e6cfc081fdaf18343af918f815188b334e9`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601866b20fd891e3cb277f3f8f172047a2f71d4ff1d97f310c3b94093dc46a50`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01551299aef213dc22bc7224e912b43e5787201c29b0c31153423f15c5db0a94`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a51580e4218eb251ae8f64eadc2ec6762034308a4057de80eb7472494393b`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be3a4f0438b1d7c8f2a308cb89fea8bbe8fb3b40f143a62069975f86ba1b059`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118019e0b8aa2d8afae2f438d7ff8005a9e4099624fab2c12ea86fec750c64f2`  
		Last Modified: Wed, 13 May 2020 18:52:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ef0c9522d683451d62dee32a69cde84172241d69c164110f784f78162e2a0`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b1c41daa7f57c8fe29b16a91ac4e60b636df159ed486ca9f9dc35bab92154`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96904d7376e44abc396e46bb450c2da8dcfba33355155f6240e07a878423a5`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27936f5bc0bfbebee69fb6ffdd7bb368b4894c8388b64ee02ad1c7c467677`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 288.9 KB (288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2f832bbb7958dfa84ad0d27ee64e1f200e10eb27024304f6f7cac63a1be89`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.14393.3686; amd64

```console
$ docker pull caddy@sha256:934fdbcbab89ce90c31479b6686014c304c2e4025f40ab12a0184d7d7031e77c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5754870634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3efc2e9d649455a51c1e525b202723307ac0807d3a66606f8b89e8e1722425`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:48:38 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:49:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:49:58 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:51:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:51:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:51:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:51:25 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:51:26 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:51:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:51:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:51:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:51:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:51:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:51:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:51:35 GMT
EXPOSE 80
# Wed, 13 May 2020 18:51:36 GMT
EXPOSE 443
# Wed, 13 May 2020 18:51:37 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:52:21 GMT
RUN caddy version
# Wed, 13 May 2020 18:52:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8d9441a5da81d2777cfc76980d60cc19b098fe856021de5a9895613a07a917`  
		Last Modified: Wed, 13 May 2020 18:54:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c45322765cd792196713eabac6cc04ae89c4fa85c29b1ca626b72c62996f6`  
		Last Modified: Wed, 13 May 2020 18:54:27 GMT  
		Size: 5.4 MB (5392506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b93c4954c5f72c6e382ba1480c3d976f845f42c19bb5e0a085798079bb636`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4516cd556129c57a85ef8c01db6dd2122853c304e58bf1d1594fdd77424509`  
		Last Modified: Wed, 13 May 2020 18:54:26 GMT  
		Size: 17.3 MB (17316249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b2c917ea7e1658aee4b4fa5144174055d3138552746c780d9540a188c3d7`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159ba07aef82e0d25aaef42f0ea5a8f3e9ac5979006bb5cfd717fa2b5979c19`  
		Last Modified: Wed, 13 May 2020 18:54:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed119e58b16c0727c096be5f489492947e6c14fa38726d290d671d3eb0b7ddc`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36668ca695daf89b18a9a9f22a1ab73b9caff740b5fe364c83b8752053bd520a`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda31fec458b3a7161e6b3a2ab63d82bb1ab9291b37081e70941e73a13d4cad6`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31dc3ae4fe27e8327f459ea65e33ab8c62ffdea360d1b9553ed5cae8d21e7b`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0ac6915dd1ededf8d058abfbf5bf18ae61704814448b2017af1b56ac222f`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3813123a037b3f32302ec2832c105f64f7e4a171a7c551709919d2a2fe50`  
		Last Modified: Wed, 13 May 2020 18:54:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5c9c51be87e873c5fd688f518a5287153de163472db0a1b8ef5219ebc4667`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b34839eed5be808ac4292dce3424594ea3cff620ab4c5abbb21d7175165bf`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e296d31b4d6061f26450d68b391b5d96928617c8bc8cbf385721f19db40f13`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a176c2fcfe281888b44bd6b42edc40ecb1f15fa70e3b46a4057a06a461d97`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80eb7786a112e5e30e573401f1db37e107bf00f6dd3cb2d5e4a5bfcff5864e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fc20b2cbd0d3d3009ab3518b6b3df01534f7bf771ac110e8d1d399a1d4c8e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2955b5f7006f6354828c6ed4286cecaf180196b00f8c315c9f6cf796a9cde`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc73cc73e699dfa7d295778821ae30a39417fe6ae6d52ad4d0ab252cf71976`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 250.3 KB (250292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebb1402ecee93e19be9f62d2148b518e2d255f5592ab44f8090e373ccd7eeb`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:eb74da93a470a6eca2a9da48f7cf6a3f3d87d333c4516745c41fef8363cca1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1217; amd64

```console
$ docker pull caddy@sha256:72fb2769c5bca3a826c2d20272955543ae0505293b8a21f9d7be902c4024462d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1731274652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de5663795f5d4dcdda76bf3051f819c10c1b278328fcf09e429e336ca484f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:46:58 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:47:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:47:22 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:47:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:47:52 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:47:53 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:47:54 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:47:55 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:47:56 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:47:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:47:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:48:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:48:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:48:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:48:03 GMT
EXPOSE 80
# Wed, 13 May 2020 18:48:04 GMT
EXPOSE 443
# Wed, 13 May 2020 18:48:05 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:48:22 GMT
RUN caddy version
# Wed, 13 May 2020 18:48:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cc8f1346629803094aa24186a3ffc8662b4a2ee69dc801d795f005d4a0d95`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18106f83313e5d34a070612d3f1c39e8cf8d9848e2b227296adfffd3965ba25d`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 355.3 KB (355269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f287fd10774920755d67b6de43826c118ec5fc4e8f9702a55be22da2df6358`  
		Last Modified: Wed, 13 May 2020 18:53:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffcf71efbb212a67332d8465f099b447811876b9e83c74eec3c01de1fcb9d0`  
		Last Modified: Wed, 13 May 2020 18:53:10 GMT  
		Size: 12.3 MB (12275873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0eb7cc61a3acb2499d87ea010471ade578b24271a239602554546a519ffbf9`  
		Last Modified: Wed, 13 May 2020 18:53:04 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafa5496993eb381a49e7fbbadd58834e3ddc0c0e33a83a2b81965beaa664e0`  
		Last Modified: Wed, 13 May 2020 18:53:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8269f4f8903d1aef05afd562fda930223dee66a331d0047620fd05dfc076caa`  
		Last Modified: Wed, 13 May 2020 18:53:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0ba135849e8ad69d2e177204089724847fea899770d08be4f326960779471`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775de502a9e90f88c9d9c68063a1aed6775b8a8eaa4f680ea12b84c7a86997aa`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8993d7ccb4765510c6cd037e5115c7af0ce11df1c85256085067fdc1fc433`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3755d5c96e8367ee1c769a90f6e6cfc081fdaf18343af918f815188b334e9`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601866b20fd891e3cb277f3f8f172047a2f71d4ff1d97f310c3b94093dc46a50`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01551299aef213dc22bc7224e912b43e5787201c29b0c31153423f15c5db0a94`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a51580e4218eb251ae8f64eadc2ec6762034308a4057de80eb7472494393b`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be3a4f0438b1d7c8f2a308cb89fea8bbe8fb3b40f143a62069975f86ba1b059`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118019e0b8aa2d8afae2f438d7ff8005a9e4099624fab2c12ea86fec750c64f2`  
		Last Modified: Wed, 13 May 2020 18:52:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ef0c9522d683451d62dee32a69cde84172241d69c164110f784f78162e2a0`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b1c41daa7f57c8fe29b16a91ac4e60b636df159ed486ca9f9dc35bab92154`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96904d7376e44abc396e46bb450c2da8dcfba33355155f6240e07a878423a5`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27936f5bc0bfbebee69fb6ffdd7bb368b4894c8388b64ee02ad1c7c467677`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 288.9 KB (288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2f832bbb7958dfa84ad0d27ee64e1f200e10eb27024304f6f7cac63a1be89`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull caddy@sha256:934fdbcbab89ce90c31479b6686014c304c2e4025f40ab12a0184d7d7031e77c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5754870634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3efc2e9d649455a51c1e525b202723307ac0807d3a66606f8b89e8e1722425`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:48:38 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:49:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:49:58 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:51:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:51:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:51:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:51:25 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:51:26 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:51:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:51:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:51:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:51:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:51:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:51:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:51:35 GMT
EXPOSE 80
# Wed, 13 May 2020 18:51:36 GMT
EXPOSE 443
# Wed, 13 May 2020 18:51:37 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:52:21 GMT
RUN caddy version
# Wed, 13 May 2020 18:52:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8d9441a5da81d2777cfc76980d60cc19b098fe856021de5a9895613a07a917`  
		Last Modified: Wed, 13 May 2020 18:54:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c45322765cd792196713eabac6cc04ae89c4fa85c29b1ca626b72c62996f6`  
		Last Modified: Wed, 13 May 2020 18:54:27 GMT  
		Size: 5.4 MB (5392506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b93c4954c5f72c6e382ba1480c3d976f845f42c19bb5e0a085798079bb636`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4516cd556129c57a85ef8c01db6dd2122853c304e58bf1d1594fdd77424509`  
		Last Modified: Wed, 13 May 2020 18:54:26 GMT  
		Size: 17.3 MB (17316249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b2c917ea7e1658aee4b4fa5144174055d3138552746c780d9540a188c3d7`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159ba07aef82e0d25aaef42f0ea5a8f3e9ac5979006bb5cfd717fa2b5979c19`  
		Last Modified: Wed, 13 May 2020 18:54:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed119e58b16c0727c096be5f489492947e6c14fa38726d290d671d3eb0b7ddc`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36668ca695daf89b18a9a9f22a1ab73b9caff740b5fe364c83b8752053bd520a`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda31fec458b3a7161e6b3a2ab63d82bb1ab9291b37081e70941e73a13d4cad6`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31dc3ae4fe27e8327f459ea65e33ab8c62ffdea360d1b9553ed5cae8d21e7b`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0ac6915dd1ededf8d058abfbf5bf18ae61704814448b2017af1b56ac222f`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3813123a037b3f32302ec2832c105f64f7e4a171a7c551709919d2a2fe50`  
		Last Modified: Wed, 13 May 2020 18:54:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5c9c51be87e873c5fd688f518a5287153de163472db0a1b8ef5219ebc4667`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b34839eed5be808ac4292dce3424594ea3cff620ab4c5abbb21d7175165bf`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e296d31b4d6061f26450d68b391b5d96928617c8bc8cbf385721f19db40f13`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a176c2fcfe281888b44bd6b42edc40ecb1f15fa70e3b46a4057a06a461d97`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80eb7786a112e5e30e573401f1db37e107bf00f6dd3cb2d5e4a5bfcff5864e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fc20b2cbd0d3d3009ab3518b6b3df01534f7bf771ac110e8d1d399a1d4c8e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2955b5f7006f6354828c6ed4286cecaf180196b00f8c315c9f6cf796a9cde`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc73cc73e699dfa7d295778821ae30a39417fe6ae6d52ad4d0ab252cf71976`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 250.3 KB (250292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebb1402ecee93e19be9f62d2148b518e2d255f5592ab44f8090e373ccd7eeb`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:bede09a6d63958ebd133c5da1d5e2eca5ed0147061b4835cf2d31373c05e815f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull caddy@sha256:72fb2769c5bca3a826c2d20272955543ae0505293b8a21f9d7be902c4024462d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1731274652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de5663795f5d4dcdda76bf3051f819c10c1b278328fcf09e429e336ca484f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:46:58 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:47:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:47:22 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:47:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:47:52 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:47:53 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:47:54 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:47:55 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:47:56 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:47:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:47:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:47:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:48:00 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:48:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:48:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:48:03 GMT
EXPOSE 80
# Wed, 13 May 2020 18:48:04 GMT
EXPOSE 443
# Wed, 13 May 2020 18:48:05 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:48:22 GMT
RUN caddy version
# Wed, 13 May 2020 18:48:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543cc8f1346629803094aa24186a3ffc8662b4a2ee69dc801d795f005d4a0d95`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18106f83313e5d34a070612d3f1c39e8cf8d9848e2b227296adfffd3965ba25d`  
		Last Modified: Wed, 13 May 2020 18:53:28 GMT  
		Size: 355.3 KB (355269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f287fd10774920755d67b6de43826c118ec5fc4e8f9702a55be22da2df6358`  
		Last Modified: Wed, 13 May 2020 18:53:26 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffcf71efbb212a67332d8465f099b447811876b9e83c74eec3c01de1fcb9d0`  
		Last Modified: Wed, 13 May 2020 18:53:10 GMT  
		Size: 12.3 MB (12275873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0eb7cc61a3acb2499d87ea010471ade578b24271a239602554546a519ffbf9`  
		Last Modified: Wed, 13 May 2020 18:53:04 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbafa5496993eb381a49e7fbbadd58834e3ddc0c0e33a83a2b81965beaa664e0`  
		Last Modified: Wed, 13 May 2020 18:53:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8269f4f8903d1aef05afd562fda930223dee66a331d0047620fd05dfc076caa`  
		Last Modified: Wed, 13 May 2020 18:53:00 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0ba135849e8ad69d2e177204089724847fea899770d08be4f326960779471`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775de502a9e90f88c9d9c68063a1aed6775b8a8eaa4f680ea12b84c7a86997aa`  
		Last Modified: Wed, 13 May 2020 18:52:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d8993d7ccb4765510c6cd037e5115c7af0ce11df1c85256085067fdc1fc433`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3755d5c96e8367ee1c769a90f6e6cfc081fdaf18343af918f815188b334e9`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601866b20fd891e3cb277f3f8f172047a2f71d4ff1d97f310c3b94093dc46a50`  
		Last Modified: Wed, 13 May 2020 18:52:55 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01551299aef213dc22bc7224e912b43e5787201c29b0c31153423f15c5db0a94`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a51580e4218eb251ae8f64eadc2ec6762034308a4057de80eb7472494393b`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be3a4f0438b1d7c8f2a308cb89fea8bbe8fb3b40f143a62069975f86ba1b059`  
		Last Modified: Wed, 13 May 2020 18:52:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118019e0b8aa2d8afae2f438d7ff8005a9e4099624fab2c12ea86fec750c64f2`  
		Last Modified: Wed, 13 May 2020 18:52:52 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72ef0c9522d683451d62dee32a69cde84172241d69c164110f784f78162e2a0`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b1c41daa7f57c8fe29b16a91ac4e60b636df159ed486ca9f9dc35bab92154`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c96904d7376e44abc396e46bb450c2da8dcfba33355155f6240e07a878423a5`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27936f5bc0bfbebee69fb6ffdd7bb368b4894c8388b64ee02ad1c7c467677`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 288.9 KB (288908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea2f832bbb7958dfa84ad0d27ee64e1f200e10eb27024304f6f7cac63a1be89`  
		Last Modified: Wed, 13 May 2020 18:52:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:30a4b139e0d207bbd7ffcd349fea87d2de3512fdaccb941fd4da396d9931f484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull caddy@sha256:934fdbcbab89ce90c31479b6686014c304c2e4025f40ab12a0184d7d7031e77c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5754870634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3efc2e9d649455a51c1e525b202723307ac0807d3a66606f8b89e8e1722425`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 18:48:38 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 13 May 2020 18:49:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 May 2020 18:49:58 GMT
ENV CADDY_VERSION=v2.0.0
# Wed, 13 May 2020 18:51:21 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.0.0/caddy_2.0.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('636bb25c9738400b480ca243a605da74988deb1bc856a1cabe7ee36511db0e048ec0a2688b1640d7b157bc239d437944e43500d91881c8acc7f2b8aa138945f9')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 May 2020 18:51:23 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 May 2020 18:51:24 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 May 2020 18:51:25 GMT
VOLUME [c:/config]
# Wed, 13 May 2020 18:51:26 GMT
VOLUME [c:/data]
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.version=v2.0.0
# Wed, 13 May 2020 18:51:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 May 2020 18:51:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 May 2020 18:51:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 May 2020 18:51:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 May 2020 18:51:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 May 2020 18:51:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 May 2020 18:51:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 May 2020 18:51:35 GMT
EXPOSE 80
# Wed, 13 May 2020 18:51:36 GMT
EXPOSE 443
# Wed, 13 May 2020 18:51:37 GMT
EXPOSE 2019
# Wed, 13 May 2020 18:52:21 GMT
RUN caddy version
# Wed, 13 May 2020 18:52:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8d9441a5da81d2777cfc76980d60cc19b098fe856021de5a9895613a07a917`  
		Last Modified: Wed, 13 May 2020 18:54:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c45322765cd792196713eabac6cc04ae89c4fa85c29b1ca626b72c62996f6`  
		Last Modified: Wed, 13 May 2020 18:54:27 GMT  
		Size: 5.4 MB (5392506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b93c4954c5f72c6e382ba1480c3d976f845f42c19bb5e0a085798079bb636`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4516cd556129c57a85ef8c01db6dd2122853c304e58bf1d1594fdd77424509`  
		Last Modified: Wed, 13 May 2020 18:54:26 GMT  
		Size: 17.3 MB (17316249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b2c917ea7e1658aee4b4fa5144174055d3138552746c780d9540a188c3d7`  
		Last Modified: Wed, 13 May 2020 18:54:21 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159ba07aef82e0d25aaef42f0ea5a8f3e9ac5979006bb5cfd717fa2b5979c19`  
		Last Modified: Wed, 13 May 2020 18:54:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed119e58b16c0727c096be5f489492947e6c14fa38726d290d671d3eb0b7ddc`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36668ca695daf89b18a9a9f22a1ab73b9caff740b5fe364c83b8752053bd520a`  
		Last Modified: Wed, 13 May 2020 18:54:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda31fec458b3a7161e6b3a2ab63d82bb1ab9291b37081e70941e73a13d4cad6`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f31dc3ae4fe27e8327f459ea65e33ab8c62ffdea360d1b9553ed5cae8d21e7b`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b0ac6915dd1ededf8d058abfbf5bf18ae61704814448b2017af1b56ac222f`  
		Last Modified: Wed, 13 May 2020 18:54:18 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3813123a037b3f32302ec2832c105f64f7e4a171a7c551709919d2a2fe50`  
		Last Modified: Wed, 13 May 2020 18:54:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5c9c51be87e873c5fd688f518a5287153de163472db0a1b8ef5219ebc4667`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741b34839eed5be808ac4292dce3424594ea3cff620ab4c5abbb21d7175165bf`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e296d31b4d6061f26450d68b391b5d96928617c8bc8cbf385721f19db40f13`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094a176c2fcfe281888b44bd6b42edc40ecb1f15fa70e3b46a4057a06a461d97`  
		Last Modified: Wed, 13 May 2020 18:54:16 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80eb7786a112e5e30e573401f1db37e107bf00f6dd3cb2d5e4a5bfcff5864e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fc20b2cbd0d3d3009ab3518b6b3df01534f7bf771ac110e8d1d399a1d4c8e`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2955b5f7006f6354828c6ed4286cecaf180196b00f8c315c9f6cf796a9cde`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc73cc73e699dfa7d295778821ae30a39417fe6ae6d52ad4d0ab252cf71976`  
		Last Modified: Wed, 13 May 2020 18:54:14 GMT  
		Size: 250.3 KB (250292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ebb1402ecee93e19be9f62d2148b518e2d255f5592ab44f8090e373ccd7eeb`  
		Last Modified: Wed, 13 May 2020 18:54:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
