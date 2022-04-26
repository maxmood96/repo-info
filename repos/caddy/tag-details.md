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
-	[`caddy:2.5.0`](#caddy250)
-	[`caddy:2.5.0-alpine`](#caddy250-alpine)
-	[`caddy:2.5.0-builder`](#caddy250-builder)
-	[`caddy:2.5.0-builder-alpine`](#caddy250-builder-alpine)
-	[`caddy:2.5.0-builder-windowsservercore-1809`](#caddy250-builder-windowsservercore-1809)
-	[`caddy:2.5.0-builder-windowsservercore-ltsc2022`](#caddy250-builder-windowsservercore-ltsc2022)
-	[`caddy:2.5.0-windowsservercore`](#caddy250-windowsservercore)
-	[`caddy:2.5.0-windowsservercore-1809`](#caddy250-windowsservercore-1809)
-	[`caddy:2.5.0-windowsservercore-ltsc2022`](#caddy250-windowsservercore-ltsc2022)
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
$ docker pull caddy@sha256:e42e57a219aa11138f3f147fb0c80b364c57fb063f85568664136ca9f7dd0048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2803; amd64
	-	windows version 10.0.20348.643; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:9fd29c443b9632275c7dee65b736044bf3eef7f0ff0acde17524d6bfa565d9c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16780958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd701a89dc68bf9b2f5f06994371e9c57d3991f35dd25eae9b72aa30fdb2d99`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:25:00 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:25:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:30:30 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:30:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:30:33 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:30:35 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:30:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ed6b8c4412bcd2bb1f40611012b40444b12071baf4884d0e75044fc1f32c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 291.5 KB (291522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff7bd6e2c9d7717705a52c1d27654581f987e1a43d2c9f3220ce850a5cdad`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a338b6679706fd2d1cd3856187d469aa5666daeaec9011f4a36dec026c557`  
		Last Modified: Tue, 26 Apr 2022 00:30:58 GMT  
		Size: 13.7 MB (13668896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0522358bf40c87db949e3b98ad737bc00126a5c9204927ead005f2c8c6d1f40`  
		Last Modified: Tue, 26 Apr 2022 00:30:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:4fb2aa089fe64de9452ea153e8fcd45f77433bb884944de7ddaf659e776f9e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16046721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd6649c19066b2dfa04d56d12bf7a3c093a73b6b1cf203cd9502a608efcae7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:15:01 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:15:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:49:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:49:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:49:37 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:49:38 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:49:38 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:49:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b230dd773e10769a2eb3e507260d2470a646efd48a639739ba8852b2915302`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 291.7 KB (291685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac48280871fa0cc6e20550e9909af62acb5b3793a4ada967e49e60367ec386e`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e13dd2006703558a44bf92c22d7b86267519c8e0a45876f765416420a52c8b`  
		Last Modified: Mon, 25 Apr 2022 20:51:11 GMT  
		Size: 13.1 MB (13127083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4eba6efd59e2065bc9bace41408b8e28e21c5f13233e039ac9f22fa7114e0`  
		Last Modified: Mon, 25 Apr 2022 20:51:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:4b653da1faf978146d3f353f96f5fec6a3d3dbe61eb226a9bc88310f8a7ac539
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15830530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e429c13a17afa4f600f294adcd8fb8fcd0e02f7d2b3a710e1e74c227c6b5307`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:33:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:33:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:57:32 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:57:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:57:38 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:57:39 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:57:44 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03203881a2568530a735b6e0e7a40ebb79adedc5193a675807b04eeb92cc6ed1`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 290.7 KB (290668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2de87d2e387fcc410ddd706bbe177b2a04b5137087a6ffca70b45c80dc976e0`  
		Last Modified: Tue, 05 Apr 2022 06:35:08 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8925c0c6962de2061a8f0a52f33e90a84c0d94c419622219a02b70ea6029831`  
		Last Modified: Mon, 25 Apr 2022 20:59:12 GMT  
		Size: 13.1 MB (13109556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a04801b9fe9d62e96942e841a278e2961fe3a50e31db66650c473be128e86`  
		Last Modified: Mon, 25 Apr 2022 20:59:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:69ab7c3ae40b72983a025617186f81a14adfe4e65bf060d6a8ded0b2027ad049
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15515390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1ed8512d16f85e28c907452f68a543b178d498bd69a88a4205b07809810c69`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:12:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:45:10 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:45:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:45:15 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:45:16 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:45:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:45:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:45:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:45:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:45:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:45:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:45:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:45:24 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:45:25 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:45:26 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:45:27 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:45:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa37f2341b1e6d98420668c9bc849a47f2c471d159b2303885040bd8d0a92f`  
		Last Modified: Tue, 05 Apr 2022 03:13:38 GMT  
		Size: 291.3 KB (291301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e87f72d84fd403dc0ea7d95672e5865925fca64a932f046b39035e8d3b43aae`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 5.7 KB (5747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffedcd6293512f192bfd7798cf59a8f7121658d14b7da6b8ed96d43b9ea1bd4`  
		Last Modified: Tue, 26 Apr 2022 00:46:14 GMT  
		Size: 12.5 MB (12501711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182c8210bf3bfdf3f311ac5ca0c803504516aa3979d448446e4b23a7414555db`  
		Last Modified: Tue, 26 Apr 2022 00:46:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:a20a2a180cce249a16be3b791cdde01779ffd91a4a9463bba45043e550f0bbab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11db83c89ecf795051de8117ab85b76db190a2f1bc5afd8ac113742dfd90522`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:08:34 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:08:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:17:24 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:17:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:17:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:17:50 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:17:53 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:17:58 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:18:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:18:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:18:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:18:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:18:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:18:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:18:31 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:18:35 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:18:39 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:18:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:18:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743509d6ced044a369685ebb068417e8757981a39d1b397c7b0182ab89f83528`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 293.7 KB (293721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029325992e21f613a5b486751627c7d5e5c7622ec29d4d170549f4dac13ad291`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadee40bb24012aa5a86d9d08c35465ea6747b388276fba98b2b23d8ab36e83d`  
		Last Modified: Mon, 25 Apr 2022 20:20:00 GMT  
		Size: 12.1 MB (12087346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aff6b8f6a27a0579cb3553f1b5da34c73a8d13bc2c46b71a42bffcbb433332`  
		Last Modified: Mon, 25 Apr 2022 20:19:58 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:70f645012314bf2deafbf43b697acd07d73a9dea2fc00a9e37ef66208f682fd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3584f54e8dcb7110aa2a2d26dd4917d281cf487e69e4a327ffb2b497250bdf95`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:41:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:41:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:41:42 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:41:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:41:47 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:41:49 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:41:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8cc7c7c7ffd67f5740add448d341753330a2abdc6ed06e995cb7d28de381ab`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 291.8 KB (291821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f8e9524a50422cbb86b1c5e3af26710e4b65591ecc118a5079f1aa7fe5a67`  
		Last Modified: Tue, 05 Apr 2022 06:20:45 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ec2ded8fc151b5e2f97ea39505dda37e06f7e69f7e6b71e482b6959c5d72a8`  
		Last Modified: Mon, 25 Apr 2022 20:42:47 GMT  
		Size: 13.2 MB (13226741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636e08e595808f97112a31aecb09c32c3139808cf61e83ca37ba447853ecc421`  
		Last Modified: Mon, 25 Apr 2022 20:42:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:ac6afd8f502178001d3c6631753a6e4457830f2945acfb4f223b359312151739
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730628642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be5151970c967a41fa277f73d3ea5c6c2441dd532017ff7ba63f94b90b5815`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:38:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:14:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:16:13 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:16:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:16:23 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:16:24 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:16:25 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:17:17 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8129805e9e333a66c903463c3cbf8ee34716da4665df9a65dd4176eba5c5f06`  
		Last Modified: Wed, 13 Apr 2022 04:49:35 GMT  
		Size: 378.1 KB (378101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df92a93e366c3079de7a894225b5af047aced370ac7cc37db8a6a1efda1d68`  
		Last Modified: Mon, 25 Apr 2022 21:21:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83100cacadedcaa12031a24db1db453af535c1d938ebff9871930a6890125a4`  
		Last Modified: Mon, 25 Apr 2022 21:21:39 GMT  
		Size: 14.0 MB (14007463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2025016da8c10d71dc51b48c0c1b4c09cd52cfb337da6fd522df0f1d942ac2e`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d207d693dada181cafd0c7fb97ab2dfa21fdc798356667ebf3e18615af2cc1`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf8198462811b78954d0490e9bd2654c63af7f5590b0a316abcd6873b887f6c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982c6b1d8f9c21d5422f34061954adc18f796ee38efba6b7c7a5efc4ab11d2c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf52c26accb9bf3880af82d0bd3e1df4bf2de7d5e977e42fccdf515d198b190`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dc5e7fac918f26a223bdc96e1913d856b1bfa82e49af4dcbb9ee132dd0079`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0620c742ae20f8c7f4a81d372f9a25b706bf19be63e67271f504c9581a3a23a`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c575b1dbcfc0a0a68adcf4e48d4e2977a495bbd529fa0453b1a132185f45d8`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced94298b1f6c583462eee02e7ff2fbe680380e9e4081e9f33820bb0f0cf0c55`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda180811a77093bcc12e90c6f09509b092e2a3c5351635fa3a3711d54073137`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec34e60db92a527d1bcaacf30b0263c1aad257b56e842915b61ca4f467854253`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684c375495ff3e6194436cd4ad2d1b3b152576f3700e90e201efccc84457816`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07262f33fbd716916cd70767bb9863a076ed51716250ceec3769e039dec513`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b340376e6b0dbbfb01d19a74849b15f4d430e8634f8fedb81851637648dae26`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 300.0 KB (299995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa021badff18bcd5b01c95b400972c8b76fcf354efc8805e2f1821ba968775`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:28e63cb2eaf6998239e5b537831968ba4d9906a8058257d528fd6fe756e37a1e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242202428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d82ba894be8f5d6526b7dc7396408664a9b19a32405c5d33476ac90538ab384`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:45:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:17:35 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:18:07 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:18:08 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:18:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:18:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:18:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:18:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:18:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:18:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:18:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:18:17 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:18:18 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:18:19 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:18:38 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:18:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ff8ee97053f0fd2c04d1416858c55ed3909995cfc0831aa8f5a40204afd05`  
		Last Modified: Wed, 13 Apr 2022 04:50:46 GMT  
		Size: 638.3 KB (638318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b7414fa4e0939433774e287ba09191bca7e808e728adc8bf3c3ce1b26ea50`  
		Last Modified: Mon, 25 Apr 2022 21:21:59 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21af46560c679f5ccc42a3c6459c86ec83319e919f8f889665cb122dbb465e`  
		Last Modified: Mon, 25 Apr 2022 21:22:15 GMT  
		Size: 14.2 MB (14238735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b0f775ed9f809c59455ec9625c83c18ba9ac32b456cf504d0c8a3bb7b15f8`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a421645aec5009da45834b2835830b440c3da7f8b0f14889a32b64015b79fb5`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0fbeeb7476cfecc4f610d18fa06e3faf4cb08844806174e62bd8ca56cd10a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cc3d5e7a3f1b072138f955361688a44e041209f404662fd53b00cb54e758a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29529d78e3af49ca347462d245bb89c20b5897986acec557b8c17d8fe568ca86`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d59dbb39cb3b1525d9595055e2116e7fde476b1af040e47e500e7ddf460e52`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112715a31629216318fb61cfb76dce5c4ddad55b5aca9dd265d4abb009660a`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7274608e1c2e3e6a98f0d9eee200338a3eb77a2d315eeeef18ef8ba33682`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028a09180fa423ea4167dbce9d52b10d0ef23f4c05538d9be8012f7f63da154`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a568da62c45dafbbc16dfeb8b91cd1e67b9b549e72d8f7c6c76202c52a4426`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda8364a6d90b372db004dd3d1cebeb76cc8650fdbd5157eca53edca7b864d6`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65cc32ef8c70486456808de6df2222050d907cfb239fd48f9c7ac8c0748a5e7`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefe909dafbf401bfed81021f3d8d6c1ef9daff428c5cec6184db94484167b4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf8775a48ae02e9ac48a56ebf7808412b9f1c60876f9f3447b282d4ffccfe4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 347.8 KB (347758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136a5dca0069e8c5e5d3fc44538572f5aaf0c7abfbde605abf6df2c1ecdf28f`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:e602ecd5eed4cae0d809ef6cdd2b0faa091da3cea6f71dbfdfa924411c744b99
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
$ docker pull caddy@sha256:9fd29c443b9632275c7dee65b736044bf3eef7f0ff0acde17524d6bfa565d9c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16780958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd701a89dc68bf9b2f5f06994371e9c57d3991f35dd25eae9b72aa30fdb2d99`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:25:00 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:25:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:30:30 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:30:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:30:33 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:30:35 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:30:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ed6b8c4412bcd2bb1f40611012b40444b12071baf4884d0e75044fc1f32c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 291.5 KB (291522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff7bd6e2c9d7717705a52c1d27654581f987e1a43d2c9f3220ce850a5cdad`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a338b6679706fd2d1cd3856187d469aa5666daeaec9011f4a36dec026c557`  
		Last Modified: Tue, 26 Apr 2022 00:30:58 GMT  
		Size: 13.7 MB (13668896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0522358bf40c87db949e3b98ad737bc00126a5c9204927ead005f2c8c6d1f40`  
		Last Modified: Tue, 26 Apr 2022 00:30:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:4fb2aa089fe64de9452ea153e8fcd45f77433bb884944de7ddaf659e776f9e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16046721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd6649c19066b2dfa04d56d12bf7a3c093a73b6b1cf203cd9502a608efcae7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:15:01 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:15:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:49:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:49:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:49:37 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:49:38 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:49:38 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:49:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b230dd773e10769a2eb3e507260d2470a646efd48a639739ba8852b2915302`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 291.7 KB (291685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac48280871fa0cc6e20550e9909af62acb5b3793a4ada967e49e60367ec386e`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e13dd2006703558a44bf92c22d7b86267519c8e0a45876f765416420a52c8b`  
		Last Modified: Mon, 25 Apr 2022 20:51:11 GMT  
		Size: 13.1 MB (13127083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4eba6efd59e2065bc9bace41408b8e28e21c5f13233e039ac9f22fa7114e0`  
		Last Modified: Mon, 25 Apr 2022 20:51:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:4b653da1faf978146d3f353f96f5fec6a3d3dbe61eb226a9bc88310f8a7ac539
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15830530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e429c13a17afa4f600f294adcd8fb8fcd0e02f7d2b3a710e1e74c227c6b5307`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:33:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:33:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:57:32 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:57:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:57:38 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:57:39 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:57:44 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03203881a2568530a735b6e0e7a40ebb79adedc5193a675807b04eeb92cc6ed1`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 290.7 KB (290668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2de87d2e387fcc410ddd706bbe177b2a04b5137087a6ffca70b45c80dc976e0`  
		Last Modified: Tue, 05 Apr 2022 06:35:08 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8925c0c6962de2061a8f0a52f33e90a84c0d94c419622219a02b70ea6029831`  
		Last Modified: Mon, 25 Apr 2022 20:59:12 GMT  
		Size: 13.1 MB (13109556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a04801b9fe9d62e96942e841a278e2961fe3a50e31db66650c473be128e86`  
		Last Modified: Mon, 25 Apr 2022 20:59:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:69ab7c3ae40b72983a025617186f81a14adfe4e65bf060d6a8ded0b2027ad049
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15515390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1ed8512d16f85e28c907452f68a543b178d498bd69a88a4205b07809810c69`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:12:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:45:10 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:45:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:45:15 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:45:16 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:45:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:45:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:45:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:45:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:45:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:45:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:45:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:45:24 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:45:25 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:45:26 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:45:27 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:45:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa37f2341b1e6d98420668c9bc849a47f2c471d159b2303885040bd8d0a92f`  
		Last Modified: Tue, 05 Apr 2022 03:13:38 GMT  
		Size: 291.3 KB (291301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e87f72d84fd403dc0ea7d95672e5865925fca64a932f046b39035e8d3b43aae`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 5.7 KB (5747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffedcd6293512f192bfd7798cf59a8f7121658d14b7da6b8ed96d43b9ea1bd4`  
		Last Modified: Tue, 26 Apr 2022 00:46:14 GMT  
		Size: 12.5 MB (12501711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182c8210bf3bfdf3f311ac5ca0c803504516aa3979d448446e4b23a7414555db`  
		Last Modified: Tue, 26 Apr 2022 00:46:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:a20a2a180cce249a16be3b791cdde01779ffd91a4a9463bba45043e550f0bbab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11db83c89ecf795051de8117ab85b76db190a2f1bc5afd8ac113742dfd90522`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:08:34 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:08:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:17:24 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:17:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:17:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:17:50 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:17:53 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:17:58 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:18:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:18:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:18:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:18:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:18:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:18:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:18:31 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:18:35 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:18:39 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:18:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:18:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743509d6ced044a369685ebb068417e8757981a39d1b397c7b0182ab89f83528`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 293.7 KB (293721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029325992e21f613a5b486751627c7d5e5c7622ec29d4d170549f4dac13ad291`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadee40bb24012aa5a86d9d08c35465ea6747b388276fba98b2b23d8ab36e83d`  
		Last Modified: Mon, 25 Apr 2022 20:20:00 GMT  
		Size: 12.1 MB (12087346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aff6b8f6a27a0579cb3553f1b5da34c73a8d13bc2c46b71a42bffcbb433332`  
		Last Modified: Mon, 25 Apr 2022 20:19:58 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:70f645012314bf2deafbf43b697acd07d73a9dea2fc00a9e37ef66208f682fd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3584f54e8dcb7110aa2a2d26dd4917d281cf487e69e4a327ffb2b497250bdf95`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:41:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:41:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:41:42 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:41:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:41:47 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:41:49 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:41:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8cc7c7c7ffd67f5740add448d341753330a2abdc6ed06e995cb7d28de381ab`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 291.8 KB (291821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f8e9524a50422cbb86b1c5e3af26710e4b65591ecc118a5079f1aa7fe5a67`  
		Last Modified: Tue, 05 Apr 2022 06:20:45 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ec2ded8fc151b5e2f97ea39505dda37e06f7e69f7e6b71e482b6959c5d72a8`  
		Last Modified: Mon, 25 Apr 2022 20:42:47 GMT  
		Size: 13.2 MB (13226741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636e08e595808f97112a31aecb09c32c3139808cf61e83ca37ba447853ecc421`  
		Last Modified: Mon, 25 Apr 2022 20:42:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:e67e63adda0c63a6e2897ccbe67d257d363986bb0add0a87460e7e5b21f68fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2803; amd64
	-	windows version 10.0.20348.643; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:9650c5d624699fbfc7797f0a97d951f569f8bbfef959e02876be98384c53c32a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126769661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9e8161d584d9f23032b2316b7eb8438879699e1486ad8d0090e8e2c15f8de6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:20:33 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 02:34:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 02:34:25 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 02:34:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 02:34:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 02:34:25 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:19:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:30:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:30:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:30:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6858aa20941bdfe0d406b2e4db477feeccf42ca6e40478043b721c6a66f9d1b6`  
		Last Modified: Thu, 14 Apr 2022 02:37:21 GMT  
		Size: 115.6 MB (115569906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8029b02d49777774618d41ab3a1f7f4f32f7d4b10453afd26a184b8787beaa`  
		Last Modified: Thu, 14 Apr 2022 02:37:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8852fa41bd6ab92e973a3316d6db4a27e9b1844abac8363c94c241958de8ad22`  
		Last Modified: Thu, 14 Apr 2022 18:20:07 GMT  
		Size: 6.8 MB (6823100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e8b043cf75cf1c9c8457f53b1bd377c3efd34c07cee9f55c8bde83b13ef585`  
		Last Modified: Tue, 26 Apr 2022 00:31:10 GMT  
		Size: 1.3 MB (1289413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f16575d63df54107d98c6de6302604e3baecf850fcfeb0a0dd6cfd9408c9d`  
		Last Modified: Tue, 26 Apr 2022 00:31:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:8166e6393ad9b0c4953d6c5bf47942e76921dd3f1ee0b6348fefe6b301effbcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122763889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccdbba9972abfdc57c2b74bb66ed897a9d5237e00a1bc42323578d365b7f392`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:49:35 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:03:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:03:33 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:03:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:03:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:03:36 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:50:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:49:59 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:49:59 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:50:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:50:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:50:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:50:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d487bef959ea51d4b707107d10bc8bb2cabb35c3d0e890400da9558498fcfae9`  
		Last Modified: Thu, 14 Apr 2022 00:10:34 GMT  
		Size: 112.0 MB (111960610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232d226d7216d6a78d6f22f1281ea887106f683641e6690999b23c156756d175`  
		Last Modified: Thu, 14 Apr 2022 00:09:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7dcd4972b24cf7ffe78c888061ef282e320f7a4c8aaa1384a55e7e28bd933c`  
		Last Modified: Thu, 14 Apr 2022 18:52:06 GMT  
		Size: 6.7 MB (6679287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be30e34b457ad8574d39820dcb20ff46f0329eec7498768b15691e314e82c308`  
		Last Modified: Mon, 25 Apr 2022 20:51:27 GMT  
		Size: 1.2 MB (1229164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1fabe7aa5b43f66bb040de9a4159250cec20a1d1f03c1bb56a94ca7857424b`  
		Last Modified: Mon, 25 Apr 2022 20:51:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f4a9899c053b29a3ae89a39cb76179c4f1a1b2c9480182e1785e7a4934de6672
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121607328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254d9278b4582c41c742295083ee2604578f59a1724d4ad9de237f56bc606d91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:16:49 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 03:23:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 03:23:16 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 03:23:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 03:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 03:23:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:56:20 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:58:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:58:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0a2cd126c67e6f9de5c0d2b9a8677d1f9ddf783df14e2ee2b65a4b837f781f`  
		Last Modified: Thu, 14 Apr 2022 03:32:44 GMT  
		Size: 111.7 MB (111729644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862413253fa7da1bfa2e411396d8013220cad00d664feea8f1757d91782065a3`  
		Last Modified: Thu, 14 Apr 2022 03:31:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edfefe81ed126a91f93489eb7294d5726270035f8a8af38291865530e667992`  
		Last Modified: Thu, 14 Apr 2022 18:57:58 GMT  
		Size: 6.0 MB (5953508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e680043769b7413a92b4bc4acb8e48a9e5ef164dc1c0e4685f3ebcc82c1c8`  
		Last Modified: Mon, 25 Apr 2022 20:59:27 GMT  
		Size: 1.2 MB (1228017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96a371a805895e54abe0b94c02a933bcbb6d1c50fa2fe09cbb9ca01bc4bdf09`  
		Last Modified: Mon, 25 Apr 2022 20:59:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:5bf6a3ce425975a90be678060a078ca9a13f0edb86b1755feadda66023a21ad5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121531748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65178889870010211120234bf1de0f8fe1154f42a122aec6d31ef5f44ca8ac9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:41:03 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:46:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:46:11 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:46:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:46:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:46:14 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:40:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:45:37 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:45:37 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:45:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:45:42 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:45:42 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59105010ca6c9ed528dc03f6c683c1bc8cd362cabe6df8b6ffe5cb7ea9a5d7a6`  
		Last Modified: Wed, 13 Apr 2022 23:49:58 GMT  
		Size: 110.4 MB (110425230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a657773900190e59f0ba6a0b06f6708be5a593336955df99496b40dd24e06d`  
		Last Modified: Wed, 13 Apr 2022 23:49:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb01e300b70916735527d066ade51d96bf1499fcc73f8e20921d8e6583b2ac7`  
		Last Modified: Thu, 14 Apr 2022 18:41:03 GMT  
		Size: 6.9 MB (6928572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324f0194c126d51157b32379352f8b4f91de641fa18400652f8d8f63a5100a10`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 1.2 MB (1189015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9690c7f39dbf1884a401e00ac496f19a144843007e3c3fd6c0b0ff1d216a812`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:2691a6ee70d65bd303bad70ee1acecd1ea7f27bee204ae088f61718ea5abc728
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122163242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a8e7dfa0559e1a8dbb14192d1d213837b57b559b2eb52d99526000967eaaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:52 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:33:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:33:21 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:33:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:33:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:33:37 GMT
WORKDIR /go
# Thu, 14 Apr 2022 19:18:31 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:19:04 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:19:08 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:19:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:19:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:19:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7b70e9365a42d1502d1309f3dc8545df5b5eb802bf656ac8d1a9adc0ca38e`  
		Last Modified: Thu, 14 Apr 2022 00:38:51 GMT  
		Size: 110.6 MB (110577271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52b4fb28789c7d8a190d4b1275b480c68ef6db3f548db9e61dc0bd5f2287c2`  
		Last Modified: Thu, 14 Apr 2022 00:38:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90034960a371e7877490974def61ec2afab2b9037cf021f8b268adf23f745b1f`  
		Last Modified: Thu, 14 Apr 2022 19:19:39 GMT  
		Size: 7.3 MB (7323527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b419307a290fa200d4ee1d283b336f67595b3dae2a96a545da0076a8f2f0b3a8`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 1.2 MB (1176369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbfaebc331dbb2554a5f8e3bc4ab37cab3cdbc0bee0ae7c0105a46e734b23bb`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:6254569039892bf2b972edc670fa1d0c02a4dbe158b5a6fc7503294d2ca02867
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124533779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1144cfb81d01915e8fe650368df288819b27dcb6e48f6742561aff5bfcb0e692`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:49 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:53:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:54:15 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:54:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:54:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:54:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:41:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:42:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:42:00 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:42:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:42:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:42:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:42:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ce7cc2608f8fa7ccebc2bd15f044fe91007681fdf9e3497b835c6671ea698`  
		Last Modified: Thu, 14 Apr 2022 00:01:54 GMT  
		Size: 113.5 MB (113483469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eebd463aa6406b85ba12e73255070fbd1566b013a0ca9f3fb5d3ccf5887df95`  
		Last Modified: Thu, 14 Apr 2022 00:01:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7324a2146e85ce6ede318cd28053e0977db3f0488b3ce78af656c65965e9001c`  
		Last Modified: Thu, 14 Apr 2022 18:42:50 GMT  
		Size: 6.9 MB (6933814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea609b474b313d4fd8f799684994c78a72930632aef028aef80beccb66e2b1`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 1.2 MB (1243136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378733785688e297f1ea3489b24dc76f584f16e7e7c75272ab18709fb8f18969`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:5e1112c2b251cd713257f116402a8b08c70b02536221f1c00e35ede48df2712f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888993144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a554cab996e7da76ef02819ef330a4fb26f3f9c493a7491141f84a9a33cfdce8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:34:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:34:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:34:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:34:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:37:05 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:38:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:55:20 GMT
ENV GOLANG_VERSION=1.17.9
# Wed, 13 Apr 2022 03:02:03 GMT
RUN $url = 'https://dl.google.com/go/go1.17.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '82752c3313cc6c1e1b5d73743a3ec569b09a14246fc2cb0824cf30f9f42a6005'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 03:02:09 GMT
WORKDIR C:\go
# Wed, 13 Apr 2022 04:41:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:18:48 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:18:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:19:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:19:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b761254212cd472f566f902a9830a91c33e94d06fb02a0192e29fe447bf98`  
		Last Modified: Wed, 13 Apr 2022 03:15:11 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210c142bbabba5cac6b3d06dc265578eafda02e9f54b2b955129652065abba5`  
		Last Modified: Wed, 13 Apr 2022 03:15:05 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24b5fea0cadfc385f0501b3cd52647d69ba5dd030f05bc637848ed7298ed45e`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1490fa326c6ac4254cc7e87bd773641c1a74d6d68ef0ee562e1296aa6e5ba09`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5425f63a29b9eb9b5bbbf135d080f8b1d2415a665b41591175a49f41da70d`  
		Last Modified: Wed, 13 Apr 2022 03:15:23 GMT  
		Size: 25.5 MB (25453409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf5f939642f2aaa6426ec58683c461b2fc27f9b92ed53ceea3d53e5f5b8d18d`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ec6181c5a38a1257f1181b0b390b0fa168627daeb103a617f04cf11c9666`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 328.4 KB (328368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6a29e70c078bf2fc470013ea504caa6d82ef66cd3af18be02f62f0d134dff6`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73a058a0e83dbc0674b085ab0d0151f94531062126dc4b1f43b0084df40fb62`  
		Last Modified: Wed, 13 Apr 2022 03:21:14 GMT  
		Size: 145.6 MB (145578329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde9b48a173bb3f29a006a2592b0bd8c63b07c7323137db4862e9a98fdde16b0`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49552906c9650efac10c4f00d5c31cebf6f940a05f00b03588df052cff5966c5`  
		Last Modified: Wed, 13 Apr 2022 04:50:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3892f065d9ae068931752897908cf2f42b7e70c10612f0d0c861d34b10c392d`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141d6a6f4de9ad79b32cd3b282f72556c753906066f6c959c90b9c98ed469f3`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151094a4fbe124963e13c2d1fb1c5868cfbaa169c003276af989cacbfe5d34b8`  
		Last Modified: Mon, 25 Apr 2022 21:22:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765cbaf262dc38339a50daa75e2a3bfdc536965075ef0683019b9c561b043cec`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.7 MB (1694161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df9d46dbf2556d53c3e38d0059f2c965b2ec2ec1362b393b4b1f1f9faeeec55`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:1b97052faeb50ea5c75cf73629d9b2ffe166382726774f8374c33fc821f12756
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408056049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd58e6419e1957d39f41478ff42606b54104872bb714df26c7bbfd10105c196`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:27:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:28:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:28:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:28:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:29:19 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:30:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:30:08 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:33:47 GMT
RUN $url = 'https://dl.google.com/go/go1.18.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c30bc3f1f7314a953fe208bd9cd5e24bd9403392a6c556ced3677f9f70f71fe1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:33:49 GMT
WORKDIR C:\go
# Thu, 14 Apr 2022 19:21:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:20:16 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:20:17 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:20:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:20:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:20:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df2c1d7d7b9748c6ddb8e9f196dfb2526451470a1256ab4047bece8468ff7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:50 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395e3155b04f913275d2f0e2bd07626c8d9b889b0646bb3fb44414d2df4130d`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3d0b098f175d5015767a5bb9a5641f1a1966ea2e2863b55cae5ae54f7edeb9`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff921731e5c58ad62f0eb62e698dd3033694fd15898c3e94d8021c0097dd912`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b89723742f5296cfb0b6d93c8b65a4995ee4a964d59eae8e96557dffc8f9e`  
		Last Modified: Wed, 13 Apr 2022 03:14:02 GMT  
		Size: 25.7 MB (25714775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0e7bcbbef7fb8a566a25556fc4b487c323359badbd7ab1bc58ab41729a7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67794576dcaaf4ef811c935b4ed0b40efe1487f0d0ab09462473b606d1fd89`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 562.2 KB (562186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2932986f0f385a406d2115ccb58dbf32a1730cf7e1f7f9f520863fcaa3e20d64`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f896ebd03d7af93409bcfb6bbbbd64481e6f575754cf0c600003a48a32d7a0b`  
		Last Modified: Wed, 13 Apr 2022 03:14:42 GMT  
		Size: 152.9 MB (152877366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f82b1974e8addd899731575590ff20cf09b3e97cdfe2ed285fc081b742b331`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52686327c4846c19f28b539d50b9d61e28b6fea5b5fddd0b921f8cbeb53d872e`  
		Last Modified: Thu, 14 Apr 2022 19:23:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe428ae1fd559625e6a41270985f292ad390b7b989a29f33178fbaeb59adaec`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce095f3f10565fda2a8540deb040f3ba4ec12ae51c7de87a7f39a507ee678bd9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808a55a0aa8fdfb2f5ae17966be5e1b3a39b399fd284db0372e9c29f67e2c9c`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4436fe9c1e94384199b902992ccbf1563c9a287bac0825d092d2e9b4d4f5be`  
		Last Modified: Mon, 25 Apr 2022 21:22:46 GMT  
		Size: 1.9 MB (1928477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e271d06fad4e820c1f2d2dd4029cc1c0fb472290b34a50751423c06751f032d9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:2cf9717916c3411cda2bfd15db21f1f40b43626eac201327da49ce01d40628dd
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
$ docker pull caddy@sha256:9650c5d624699fbfc7797f0a97d951f569f8bbfef959e02876be98384c53c32a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126769661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9e8161d584d9f23032b2316b7eb8438879699e1486ad8d0090e8e2c15f8de6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:20:33 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 02:34:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 02:34:25 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 02:34:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 02:34:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 02:34:25 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:19:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:30:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:30:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:30:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6858aa20941bdfe0d406b2e4db477feeccf42ca6e40478043b721c6a66f9d1b6`  
		Last Modified: Thu, 14 Apr 2022 02:37:21 GMT  
		Size: 115.6 MB (115569906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8029b02d49777774618d41ab3a1f7f4f32f7d4b10453afd26a184b8787beaa`  
		Last Modified: Thu, 14 Apr 2022 02:37:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8852fa41bd6ab92e973a3316d6db4a27e9b1844abac8363c94c241958de8ad22`  
		Last Modified: Thu, 14 Apr 2022 18:20:07 GMT  
		Size: 6.8 MB (6823100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e8b043cf75cf1c9c8457f53b1bd377c3efd34c07cee9f55c8bde83b13ef585`  
		Last Modified: Tue, 26 Apr 2022 00:31:10 GMT  
		Size: 1.3 MB (1289413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f16575d63df54107d98c6de6302604e3baecf850fcfeb0a0dd6cfd9408c9d`  
		Last Modified: Tue, 26 Apr 2022 00:31:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:8166e6393ad9b0c4953d6c5bf47942e76921dd3f1ee0b6348fefe6b301effbcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122763889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccdbba9972abfdc57c2b74bb66ed897a9d5237e00a1bc42323578d365b7f392`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:49:35 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:03:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:03:33 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:03:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:03:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:03:36 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:50:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:49:59 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:49:59 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:50:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:50:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:50:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:50:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d487bef959ea51d4b707107d10bc8bb2cabb35c3d0e890400da9558498fcfae9`  
		Last Modified: Thu, 14 Apr 2022 00:10:34 GMT  
		Size: 112.0 MB (111960610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232d226d7216d6a78d6f22f1281ea887106f683641e6690999b23c156756d175`  
		Last Modified: Thu, 14 Apr 2022 00:09:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7dcd4972b24cf7ffe78c888061ef282e320f7a4c8aaa1384a55e7e28bd933c`  
		Last Modified: Thu, 14 Apr 2022 18:52:06 GMT  
		Size: 6.7 MB (6679287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be30e34b457ad8574d39820dcb20ff46f0329eec7498768b15691e314e82c308`  
		Last Modified: Mon, 25 Apr 2022 20:51:27 GMT  
		Size: 1.2 MB (1229164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1fabe7aa5b43f66bb040de9a4159250cec20a1d1f03c1bb56a94ca7857424b`  
		Last Modified: Mon, 25 Apr 2022 20:51:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f4a9899c053b29a3ae89a39cb76179c4f1a1b2c9480182e1785e7a4934de6672
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121607328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254d9278b4582c41c742295083ee2604578f59a1724d4ad9de237f56bc606d91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:16:49 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 03:23:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 03:23:16 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 03:23:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 03:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 03:23:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:56:20 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:58:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:58:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0a2cd126c67e6f9de5c0d2b9a8677d1f9ddf783df14e2ee2b65a4b837f781f`  
		Last Modified: Thu, 14 Apr 2022 03:32:44 GMT  
		Size: 111.7 MB (111729644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862413253fa7da1bfa2e411396d8013220cad00d664feea8f1757d91782065a3`  
		Last Modified: Thu, 14 Apr 2022 03:31:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edfefe81ed126a91f93489eb7294d5726270035f8a8af38291865530e667992`  
		Last Modified: Thu, 14 Apr 2022 18:57:58 GMT  
		Size: 6.0 MB (5953508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e680043769b7413a92b4bc4acb8e48a9e5ef164dc1c0e4685f3ebcc82c1c8`  
		Last Modified: Mon, 25 Apr 2022 20:59:27 GMT  
		Size: 1.2 MB (1228017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96a371a805895e54abe0b94c02a933bcbb6d1c50fa2fe09cbb9ca01bc4bdf09`  
		Last Modified: Mon, 25 Apr 2022 20:59:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:5bf6a3ce425975a90be678060a078ca9a13f0edb86b1755feadda66023a21ad5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121531748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65178889870010211120234bf1de0f8fe1154f42a122aec6d31ef5f44ca8ac9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:41:03 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:46:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:46:11 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:46:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:46:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:46:14 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:40:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:45:37 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:45:37 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:45:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:45:42 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:45:42 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59105010ca6c9ed528dc03f6c683c1bc8cd362cabe6df8b6ffe5cb7ea9a5d7a6`  
		Last Modified: Wed, 13 Apr 2022 23:49:58 GMT  
		Size: 110.4 MB (110425230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a657773900190e59f0ba6a0b06f6708be5a593336955df99496b40dd24e06d`  
		Last Modified: Wed, 13 Apr 2022 23:49:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb01e300b70916735527d066ade51d96bf1499fcc73f8e20921d8e6583b2ac7`  
		Last Modified: Thu, 14 Apr 2022 18:41:03 GMT  
		Size: 6.9 MB (6928572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324f0194c126d51157b32379352f8b4f91de641fa18400652f8d8f63a5100a10`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 1.2 MB (1189015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9690c7f39dbf1884a401e00ac496f19a144843007e3c3fd6c0b0ff1d216a812`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:2691a6ee70d65bd303bad70ee1acecd1ea7f27bee204ae088f61718ea5abc728
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122163242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a8e7dfa0559e1a8dbb14192d1d213837b57b559b2eb52d99526000967eaaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:52 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:33:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:33:21 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:33:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:33:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:33:37 GMT
WORKDIR /go
# Thu, 14 Apr 2022 19:18:31 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:19:04 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:19:08 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:19:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:19:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:19:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7b70e9365a42d1502d1309f3dc8545df5b5eb802bf656ac8d1a9adc0ca38e`  
		Last Modified: Thu, 14 Apr 2022 00:38:51 GMT  
		Size: 110.6 MB (110577271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52b4fb28789c7d8a190d4b1275b480c68ef6db3f548db9e61dc0bd5f2287c2`  
		Last Modified: Thu, 14 Apr 2022 00:38:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90034960a371e7877490974def61ec2afab2b9037cf021f8b268adf23f745b1f`  
		Last Modified: Thu, 14 Apr 2022 19:19:39 GMT  
		Size: 7.3 MB (7323527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b419307a290fa200d4ee1d283b336f67595b3dae2a96a545da0076a8f2f0b3a8`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 1.2 MB (1176369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbfaebc331dbb2554a5f8e3bc4ab37cab3cdbc0bee0ae7c0105a46e734b23bb`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:6254569039892bf2b972edc670fa1d0c02a4dbe158b5a6fc7503294d2ca02867
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124533779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1144cfb81d01915e8fe650368df288819b27dcb6e48f6742561aff5bfcb0e692`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:49 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:53:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:54:15 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:54:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:54:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:54:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:41:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:42:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:42:00 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:42:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:42:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:42:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:42:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ce7cc2608f8fa7ccebc2bd15f044fe91007681fdf9e3497b835c6671ea698`  
		Last Modified: Thu, 14 Apr 2022 00:01:54 GMT  
		Size: 113.5 MB (113483469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eebd463aa6406b85ba12e73255070fbd1566b013a0ca9f3fb5d3ccf5887df95`  
		Last Modified: Thu, 14 Apr 2022 00:01:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7324a2146e85ce6ede318cd28053e0977db3f0488b3ce78af656c65965e9001c`  
		Last Modified: Thu, 14 Apr 2022 18:42:50 GMT  
		Size: 6.9 MB (6933814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea609b474b313d4fd8f799684994c78a72930632aef028aef80beccb66e2b1`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 1.2 MB (1243136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378733785688e297f1ea3489b24dc76f584f16e7e7c75272ab18709fb8f18969`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:b9480bf84ce2dace3248013b5c66c97e54e689c11831f8ab0c4d5f1849780caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:5e1112c2b251cd713257f116402a8b08c70b02536221f1c00e35ede48df2712f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888993144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a554cab996e7da76ef02819ef330a4fb26f3f9c493a7491141f84a9a33cfdce8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:34:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:34:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:34:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:34:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:37:05 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:38:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:55:20 GMT
ENV GOLANG_VERSION=1.17.9
# Wed, 13 Apr 2022 03:02:03 GMT
RUN $url = 'https://dl.google.com/go/go1.17.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '82752c3313cc6c1e1b5d73743a3ec569b09a14246fc2cb0824cf30f9f42a6005'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 03:02:09 GMT
WORKDIR C:\go
# Wed, 13 Apr 2022 04:41:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:18:48 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:18:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:19:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:19:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b761254212cd472f566f902a9830a91c33e94d06fb02a0192e29fe447bf98`  
		Last Modified: Wed, 13 Apr 2022 03:15:11 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210c142bbabba5cac6b3d06dc265578eafda02e9f54b2b955129652065abba5`  
		Last Modified: Wed, 13 Apr 2022 03:15:05 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24b5fea0cadfc385f0501b3cd52647d69ba5dd030f05bc637848ed7298ed45e`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1490fa326c6ac4254cc7e87bd773641c1a74d6d68ef0ee562e1296aa6e5ba09`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5425f63a29b9eb9b5bbbf135d080f8b1d2415a665b41591175a49f41da70d`  
		Last Modified: Wed, 13 Apr 2022 03:15:23 GMT  
		Size: 25.5 MB (25453409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf5f939642f2aaa6426ec58683c461b2fc27f9b92ed53ceea3d53e5f5b8d18d`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ec6181c5a38a1257f1181b0b390b0fa168627daeb103a617f04cf11c9666`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 328.4 KB (328368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6a29e70c078bf2fc470013ea504caa6d82ef66cd3af18be02f62f0d134dff6`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73a058a0e83dbc0674b085ab0d0151f94531062126dc4b1f43b0084df40fb62`  
		Last Modified: Wed, 13 Apr 2022 03:21:14 GMT  
		Size: 145.6 MB (145578329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde9b48a173bb3f29a006a2592b0bd8c63b07c7323137db4862e9a98fdde16b0`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49552906c9650efac10c4f00d5c31cebf6f940a05f00b03588df052cff5966c5`  
		Last Modified: Wed, 13 Apr 2022 04:50:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3892f065d9ae068931752897908cf2f42b7e70c10612f0d0c861d34b10c392d`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141d6a6f4de9ad79b32cd3b282f72556c753906066f6c959c90b9c98ed469f3`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151094a4fbe124963e13c2d1fb1c5868cfbaa169c003276af989cacbfe5d34b8`  
		Last Modified: Mon, 25 Apr 2022 21:22:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765cbaf262dc38339a50daa75e2a3bfdc536965075ef0683019b9c561b043cec`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.7 MB (1694161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df9d46dbf2556d53c3e38d0059f2c965b2ec2ec1362b393b4b1f1f9faeeec55`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4ae9973b09d5f6d1623aaf1cba218c72ea57e553d3bbdbfbf2ee3ecb4d96bdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:1b97052faeb50ea5c75cf73629d9b2ffe166382726774f8374c33fc821f12756
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408056049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd58e6419e1957d39f41478ff42606b54104872bb714df26c7bbfd10105c196`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:27:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:28:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:28:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:28:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:29:19 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:30:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:30:08 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:33:47 GMT
RUN $url = 'https://dl.google.com/go/go1.18.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c30bc3f1f7314a953fe208bd9cd5e24bd9403392a6c556ced3677f9f70f71fe1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:33:49 GMT
WORKDIR C:\go
# Thu, 14 Apr 2022 19:21:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:20:16 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:20:17 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:20:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:20:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:20:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df2c1d7d7b9748c6ddb8e9f196dfb2526451470a1256ab4047bece8468ff7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:50 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395e3155b04f913275d2f0e2bd07626c8d9b889b0646bb3fb44414d2df4130d`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3d0b098f175d5015767a5bb9a5641f1a1966ea2e2863b55cae5ae54f7edeb9`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff921731e5c58ad62f0eb62e698dd3033694fd15898c3e94d8021c0097dd912`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b89723742f5296cfb0b6d93c8b65a4995ee4a964d59eae8e96557dffc8f9e`  
		Last Modified: Wed, 13 Apr 2022 03:14:02 GMT  
		Size: 25.7 MB (25714775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0e7bcbbef7fb8a566a25556fc4b487c323359badbd7ab1bc58ab41729a7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67794576dcaaf4ef811c935b4ed0b40efe1487f0d0ab09462473b606d1fd89`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 562.2 KB (562186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2932986f0f385a406d2115ccb58dbf32a1730cf7e1f7f9f520863fcaa3e20d64`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f896ebd03d7af93409bcfb6bbbbd64481e6f575754cf0c600003a48a32d7a0b`  
		Last Modified: Wed, 13 Apr 2022 03:14:42 GMT  
		Size: 152.9 MB (152877366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f82b1974e8addd899731575590ff20cf09b3e97cdfe2ed285fc081b742b331`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52686327c4846c19f28b539d50b9d61e28b6fea5b5fddd0b921f8cbeb53d872e`  
		Last Modified: Thu, 14 Apr 2022 19:23:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe428ae1fd559625e6a41270985f292ad390b7b989a29f33178fbaeb59adaec`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce095f3f10565fda2a8540deb040f3ba4ec12ae51c7de87a7f39a507ee678bd9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808a55a0aa8fdfb2f5ae17966be5e1b3a39b399fd284db0372e9c29f67e2c9c`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4436fe9c1e94384199b902992ccbf1563c9a287bac0825d092d2e9b4d4f5be`  
		Last Modified: Mon, 25 Apr 2022 21:22:46 GMT  
		Size: 1.9 MB (1928477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e271d06fad4e820c1f2d2dd4029cc1c0fb472290b34a50751423c06751f032d9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:0382e21e9d9d4449ad0dbe82519f107c4fe3eb88d5b32bd149c017f51b6784e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2803; amd64
	-	windows version 10.0.20348.643; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:ac6afd8f502178001d3c6631753a6e4457830f2945acfb4f223b359312151739
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730628642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be5151970c967a41fa277f73d3ea5c6c2441dd532017ff7ba63f94b90b5815`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:38:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:14:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:16:13 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:16:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:16:23 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:16:24 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:16:25 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:17:17 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8129805e9e333a66c903463c3cbf8ee34716da4665df9a65dd4176eba5c5f06`  
		Last Modified: Wed, 13 Apr 2022 04:49:35 GMT  
		Size: 378.1 KB (378101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df92a93e366c3079de7a894225b5af047aced370ac7cc37db8a6a1efda1d68`  
		Last Modified: Mon, 25 Apr 2022 21:21:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83100cacadedcaa12031a24db1db453af535c1d938ebff9871930a6890125a4`  
		Last Modified: Mon, 25 Apr 2022 21:21:39 GMT  
		Size: 14.0 MB (14007463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2025016da8c10d71dc51b48c0c1b4c09cd52cfb337da6fd522df0f1d942ac2e`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d207d693dada181cafd0c7fb97ab2dfa21fdc798356667ebf3e18615af2cc1`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf8198462811b78954d0490e9bd2654c63af7f5590b0a316abcd6873b887f6c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982c6b1d8f9c21d5422f34061954adc18f796ee38efba6b7c7a5efc4ab11d2c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf52c26accb9bf3880af82d0bd3e1df4bf2de7d5e977e42fccdf515d198b190`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dc5e7fac918f26a223bdc96e1913d856b1bfa82e49af4dcbb9ee132dd0079`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0620c742ae20f8c7f4a81d372f9a25b706bf19be63e67271f504c9581a3a23a`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c575b1dbcfc0a0a68adcf4e48d4e2977a495bbd529fa0453b1a132185f45d8`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced94298b1f6c583462eee02e7ff2fbe680380e9e4081e9f33820bb0f0cf0c55`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda180811a77093bcc12e90c6f09509b092e2a3c5351635fa3a3711d54073137`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec34e60db92a527d1bcaacf30b0263c1aad257b56e842915b61ca4f467854253`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684c375495ff3e6194436cd4ad2d1b3b152576f3700e90e201efccc84457816`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07262f33fbd716916cd70767bb9863a076ed51716250ceec3769e039dec513`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b340376e6b0dbbfb01d19a74849b15f4d430e8634f8fedb81851637648dae26`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 300.0 KB (299995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa021badff18bcd5b01c95b400972c8b76fcf354efc8805e2f1821ba968775`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:28e63cb2eaf6998239e5b537831968ba4d9906a8058257d528fd6fe756e37a1e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242202428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d82ba894be8f5d6526b7dc7396408664a9b19a32405c5d33476ac90538ab384`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:45:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:17:35 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:18:07 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:18:08 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:18:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:18:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:18:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:18:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:18:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:18:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:18:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:18:17 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:18:18 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:18:19 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:18:38 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:18:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ff8ee97053f0fd2c04d1416858c55ed3909995cfc0831aa8f5a40204afd05`  
		Last Modified: Wed, 13 Apr 2022 04:50:46 GMT  
		Size: 638.3 KB (638318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b7414fa4e0939433774e287ba09191bca7e808e728adc8bf3c3ce1b26ea50`  
		Last Modified: Mon, 25 Apr 2022 21:21:59 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21af46560c679f5ccc42a3c6459c86ec83319e919f8f889665cb122dbb465e`  
		Last Modified: Mon, 25 Apr 2022 21:22:15 GMT  
		Size: 14.2 MB (14238735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b0f775ed9f809c59455ec9625c83c18ba9ac32b456cf504d0c8a3bb7b15f8`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a421645aec5009da45834b2835830b440c3da7f8b0f14889a32b64015b79fb5`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0fbeeb7476cfecc4f610d18fa06e3faf4cb08844806174e62bd8ca56cd10a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cc3d5e7a3f1b072138f955361688a44e041209f404662fd53b00cb54e758a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29529d78e3af49ca347462d245bb89c20b5897986acec557b8c17d8fe568ca86`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d59dbb39cb3b1525d9595055e2116e7fde476b1af040e47e500e7ddf460e52`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112715a31629216318fb61cfb76dce5c4ddad55b5aca9dd265d4abb009660a`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7274608e1c2e3e6a98f0d9eee200338a3eb77a2d315eeeef18ef8ba33682`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028a09180fa423ea4167dbce9d52b10d0ef23f4c05538d9be8012f7f63da154`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a568da62c45dafbbc16dfeb8b91cd1e67b9b549e72d8f7c6c76202c52a4426`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda8364a6d90b372db004dd3d1cebeb76cc8650fdbd5157eca53edca7b864d6`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65cc32ef8c70486456808de6df2222050d907cfb239fd48f9c7ac8c0748a5e7`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefe909dafbf401bfed81021f3d8d6c1ef9daff428c5cec6184db94484167b4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf8775a48ae02e9ac48a56ebf7808412b9f1c60876f9f3447b282d4ffccfe4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 347.8 KB (347758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136a5dca0069e8c5e5d3fc44538572f5aaf0c7abfbde605abf6df2c1ecdf28f`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:bc778a53e3357f5c8a9c100b8750dc0a3a608315519c727b0b944b910ebc066b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:ac6afd8f502178001d3c6631753a6e4457830f2945acfb4f223b359312151739
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730628642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be5151970c967a41fa277f73d3ea5c6c2441dd532017ff7ba63f94b90b5815`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:38:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:14:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:16:13 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:16:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:16:23 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:16:24 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:16:25 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:17:17 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8129805e9e333a66c903463c3cbf8ee34716da4665df9a65dd4176eba5c5f06`  
		Last Modified: Wed, 13 Apr 2022 04:49:35 GMT  
		Size: 378.1 KB (378101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df92a93e366c3079de7a894225b5af047aced370ac7cc37db8a6a1efda1d68`  
		Last Modified: Mon, 25 Apr 2022 21:21:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83100cacadedcaa12031a24db1db453af535c1d938ebff9871930a6890125a4`  
		Last Modified: Mon, 25 Apr 2022 21:21:39 GMT  
		Size: 14.0 MB (14007463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2025016da8c10d71dc51b48c0c1b4c09cd52cfb337da6fd522df0f1d942ac2e`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d207d693dada181cafd0c7fb97ab2dfa21fdc798356667ebf3e18615af2cc1`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf8198462811b78954d0490e9bd2654c63af7f5590b0a316abcd6873b887f6c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982c6b1d8f9c21d5422f34061954adc18f796ee38efba6b7c7a5efc4ab11d2c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf52c26accb9bf3880af82d0bd3e1df4bf2de7d5e977e42fccdf515d198b190`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dc5e7fac918f26a223bdc96e1913d856b1bfa82e49af4dcbb9ee132dd0079`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0620c742ae20f8c7f4a81d372f9a25b706bf19be63e67271f504c9581a3a23a`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c575b1dbcfc0a0a68adcf4e48d4e2977a495bbd529fa0453b1a132185f45d8`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced94298b1f6c583462eee02e7ff2fbe680380e9e4081e9f33820bb0f0cf0c55`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda180811a77093bcc12e90c6f09509b092e2a3c5351635fa3a3711d54073137`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec34e60db92a527d1bcaacf30b0263c1aad257b56e842915b61ca4f467854253`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684c375495ff3e6194436cd4ad2d1b3b152576f3700e90e201efccc84457816`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07262f33fbd716916cd70767bb9863a076ed51716250ceec3769e039dec513`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b340376e6b0dbbfb01d19a74849b15f4d430e8634f8fedb81851637648dae26`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 300.0 KB (299995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa021badff18bcd5b01c95b400972c8b76fcf354efc8805e2f1821ba968775`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:03edcc30e55a42bb6833408159e70252c0f2f3d51191a6ae23dfe882a87681fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:28e63cb2eaf6998239e5b537831968ba4d9906a8058257d528fd6fe756e37a1e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242202428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d82ba894be8f5d6526b7dc7396408664a9b19a32405c5d33476ac90538ab384`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:45:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:17:35 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:18:07 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:18:08 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:18:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:18:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:18:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:18:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:18:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:18:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:18:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:18:17 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:18:18 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:18:19 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:18:38 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:18:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ff8ee97053f0fd2c04d1416858c55ed3909995cfc0831aa8f5a40204afd05`  
		Last Modified: Wed, 13 Apr 2022 04:50:46 GMT  
		Size: 638.3 KB (638318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b7414fa4e0939433774e287ba09191bca7e808e728adc8bf3c3ce1b26ea50`  
		Last Modified: Mon, 25 Apr 2022 21:21:59 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21af46560c679f5ccc42a3c6459c86ec83319e919f8f889665cb122dbb465e`  
		Last Modified: Mon, 25 Apr 2022 21:22:15 GMT  
		Size: 14.2 MB (14238735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b0f775ed9f809c59455ec9625c83c18ba9ac32b456cf504d0c8a3bb7b15f8`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a421645aec5009da45834b2835830b440c3da7f8b0f14889a32b64015b79fb5`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0fbeeb7476cfecc4f610d18fa06e3faf4cb08844806174e62bd8ca56cd10a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cc3d5e7a3f1b072138f955361688a44e041209f404662fd53b00cb54e758a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29529d78e3af49ca347462d245bb89c20b5897986acec557b8c17d8fe568ca86`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d59dbb39cb3b1525d9595055e2116e7fde476b1af040e47e500e7ddf460e52`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112715a31629216318fb61cfb76dce5c4ddad55b5aca9dd265d4abb009660a`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7274608e1c2e3e6a98f0d9eee200338a3eb77a2d315eeeef18ef8ba33682`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028a09180fa423ea4167dbce9d52b10d0ef23f4c05538d9be8012f7f63da154`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a568da62c45dafbbc16dfeb8b91cd1e67b9b549e72d8f7c6c76202c52a4426`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda8364a6d90b372db004dd3d1cebeb76cc8650fdbd5157eca53edca7b864d6`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65cc32ef8c70486456808de6df2222050d907cfb239fd48f9c7ac8c0748a5e7`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefe909dafbf401bfed81021f3d8d6c1ef9daff428c5cec6184db94484167b4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf8775a48ae02e9ac48a56ebf7808412b9f1c60876f9f3447b282d4ffccfe4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 347.8 KB (347758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136a5dca0069e8c5e5d3fc44538572f5aaf0c7abfbde605abf6df2c1ecdf28f`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0`

```console
$ docker pull caddy@sha256:e42e57a219aa11138f3f147fb0c80b364c57fb063f85568664136ca9f7dd0048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2803; amd64
	-	windows version 10.0.20348.643; amd64

### `caddy:2.5.0` - linux; amd64

```console
$ docker pull caddy@sha256:9fd29c443b9632275c7dee65b736044bf3eef7f0ff0acde17524d6bfa565d9c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16780958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd701a89dc68bf9b2f5f06994371e9c57d3991f35dd25eae9b72aa30fdb2d99`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:25:00 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:25:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:30:30 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:30:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:30:33 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:30:35 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:30:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ed6b8c4412bcd2bb1f40611012b40444b12071baf4884d0e75044fc1f32c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 291.5 KB (291522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff7bd6e2c9d7717705a52c1d27654581f987e1a43d2c9f3220ce850a5cdad`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a338b6679706fd2d1cd3856187d469aa5666daeaec9011f4a36dec026c557`  
		Last Modified: Tue, 26 Apr 2022 00:30:58 GMT  
		Size: 13.7 MB (13668896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0522358bf40c87db949e3b98ad737bc00126a5c9204927ead005f2c8c6d1f40`  
		Last Modified: Tue, 26 Apr 2022 00:30:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0` - linux; arm variant v6

```console
$ docker pull caddy@sha256:4fb2aa089fe64de9452ea153e8fcd45f77433bb884944de7ddaf659e776f9e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16046721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd6649c19066b2dfa04d56d12bf7a3c093a73b6b1cf203cd9502a608efcae7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:15:01 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:15:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:49:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:49:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:49:37 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:49:38 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:49:38 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:49:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b230dd773e10769a2eb3e507260d2470a646efd48a639739ba8852b2915302`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 291.7 KB (291685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac48280871fa0cc6e20550e9909af62acb5b3793a4ada967e49e60367ec386e`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e13dd2006703558a44bf92c22d7b86267519c8e0a45876f765416420a52c8b`  
		Last Modified: Mon, 25 Apr 2022 20:51:11 GMT  
		Size: 13.1 MB (13127083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4eba6efd59e2065bc9bace41408b8e28e21c5f13233e039ac9f22fa7114e0`  
		Last Modified: Mon, 25 Apr 2022 20:51:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0` - linux; arm variant v7

```console
$ docker pull caddy@sha256:4b653da1faf978146d3f353f96f5fec6a3d3dbe61eb226a9bc88310f8a7ac539
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15830530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e429c13a17afa4f600f294adcd8fb8fcd0e02f7d2b3a710e1e74c227c6b5307`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:33:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:33:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:57:32 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:57:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:57:38 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:57:39 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:57:44 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03203881a2568530a735b6e0e7a40ebb79adedc5193a675807b04eeb92cc6ed1`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 290.7 KB (290668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2de87d2e387fcc410ddd706bbe177b2a04b5137087a6ffca70b45c80dc976e0`  
		Last Modified: Tue, 05 Apr 2022 06:35:08 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8925c0c6962de2061a8f0a52f33e90a84c0d94c419622219a02b70ea6029831`  
		Last Modified: Mon, 25 Apr 2022 20:59:12 GMT  
		Size: 13.1 MB (13109556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a04801b9fe9d62e96942e841a278e2961fe3a50e31db66650c473be128e86`  
		Last Modified: Mon, 25 Apr 2022 20:59:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:69ab7c3ae40b72983a025617186f81a14adfe4e65bf060d6a8ded0b2027ad049
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15515390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1ed8512d16f85e28c907452f68a543b178d498bd69a88a4205b07809810c69`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:12:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:45:10 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:45:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:45:15 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:45:16 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:45:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:45:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:45:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:45:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:45:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:45:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:45:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:45:24 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:45:25 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:45:26 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:45:27 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:45:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa37f2341b1e6d98420668c9bc849a47f2c471d159b2303885040bd8d0a92f`  
		Last Modified: Tue, 05 Apr 2022 03:13:38 GMT  
		Size: 291.3 KB (291301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e87f72d84fd403dc0ea7d95672e5865925fca64a932f046b39035e8d3b43aae`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 5.7 KB (5747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffedcd6293512f192bfd7798cf59a8f7121658d14b7da6b8ed96d43b9ea1bd4`  
		Last Modified: Tue, 26 Apr 2022 00:46:14 GMT  
		Size: 12.5 MB (12501711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182c8210bf3bfdf3f311ac5ca0c803504516aa3979d448446e4b23a7414555db`  
		Last Modified: Tue, 26 Apr 2022 00:46:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0` - linux; ppc64le

```console
$ docker pull caddy@sha256:a20a2a180cce249a16be3b791cdde01779ffd91a4a9463bba45043e550f0bbab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11db83c89ecf795051de8117ab85b76db190a2f1bc5afd8ac113742dfd90522`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:08:34 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:08:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:17:24 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:17:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:17:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:17:50 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:17:53 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:17:58 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:18:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:18:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:18:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:18:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:18:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:18:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:18:31 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:18:35 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:18:39 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:18:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:18:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743509d6ced044a369685ebb068417e8757981a39d1b397c7b0182ab89f83528`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 293.7 KB (293721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029325992e21f613a5b486751627c7d5e5c7622ec29d4d170549f4dac13ad291`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadee40bb24012aa5a86d9d08c35465ea6747b388276fba98b2b23d8ab36e83d`  
		Last Modified: Mon, 25 Apr 2022 20:20:00 GMT  
		Size: 12.1 MB (12087346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aff6b8f6a27a0579cb3553f1b5da34c73a8d13bc2c46b71a42bffcbb433332`  
		Last Modified: Mon, 25 Apr 2022 20:19:58 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0` - linux; s390x

```console
$ docker pull caddy@sha256:70f645012314bf2deafbf43b697acd07d73a9dea2fc00a9e37ef66208f682fd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3584f54e8dcb7110aa2a2d26dd4917d281cf487e69e4a327ffb2b497250bdf95`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:41:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:41:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:41:42 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:41:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:41:47 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:41:49 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:41:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8cc7c7c7ffd67f5740add448d341753330a2abdc6ed06e995cb7d28de381ab`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 291.8 KB (291821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f8e9524a50422cbb86b1c5e3af26710e4b65591ecc118a5079f1aa7fe5a67`  
		Last Modified: Tue, 05 Apr 2022 06:20:45 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ec2ded8fc151b5e2f97ea39505dda37e06f7e69f7e6b71e482b6959c5d72a8`  
		Last Modified: Mon, 25 Apr 2022 20:42:47 GMT  
		Size: 13.2 MB (13226741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636e08e595808f97112a31aecb09c32c3139808cf61e83ca37ba447853ecc421`  
		Last Modified: Mon, 25 Apr 2022 20:42:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:ac6afd8f502178001d3c6631753a6e4457830f2945acfb4f223b359312151739
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730628642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be5151970c967a41fa277f73d3ea5c6c2441dd532017ff7ba63f94b90b5815`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:38:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:14:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:16:13 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:16:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:16:23 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:16:24 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:16:25 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:17:17 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8129805e9e333a66c903463c3cbf8ee34716da4665df9a65dd4176eba5c5f06`  
		Last Modified: Wed, 13 Apr 2022 04:49:35 GMT  
		Size: 378.1 KB (378101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df92a93e366c3079de7a894225b5af047aced370ac7cc37db8a6a1efda1d68`  
		Last Modified: Mon, 25 Apr 2022 21:21:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83100cacadedcaa12031a24db1db453af535c1d938ebff9871930a6890125a4`  
		Last Modified: Mon, 25 Apr 2022 21:21:39 GMT  
		Size: 14.0 MB (14007463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2025016da8c10d71dc51b48c0c1b4c09cd52cfb337da6fd522df0f1d942ac2e`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d207d693dada181cafd0c7fb97ab2dfa21fdc798356667ebf3e18615af2cc1`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf8198462811b78954d0490e9bd2654c63af7f5590b0a316abcd6873b887f6c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982c6b1d8f9c21d5422f34061954adc18f796ee38efba6b7c7a5efc4ab11d2c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf52c26accb9bf3880af82d0bd3e1df4bf2de7d5e977e42fccdf515d198b190`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dc5e7fac918f26a223bdc96e1913d856b1bfa82e49af4dcbb9ee132dd0079`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0620c742ae20f8c7f4a81d372f9a25b706bf19be63e67271f504c9581a3a23a`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c575b1dbcfc0a0a68adcf4e48d4e2977a495bbd529fa0453b1a132185f45d8`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced94298b1f6c583462eee02e7ff2fbe680380e9e4081e9f33820bb0f0cf0c55`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda180811a77093bcc12e90c6f09509b092e2a3c5351635fa3a3711d54073137`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec34e60db92a527d1bcaacf30b0263c1aad257b56e842915b61ca4f467854253`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684c375495ff3e6194436cd4ad2d1b3b152576f3700e90e201efccc84457816`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07262f33fbd716916cd70767bb9863a076ed51716250ceec3769e039dec513`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b340376e6b0dbbfb01d19a74849b15f4d430e8634f8fedb81851637648dae26`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 300.0 KB (299995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa021badff18bcd5b01c95b400972c8b76fcf354efc8805e2f1821ba968775`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:28e63cb2eaf6998239e5b537831968ba4d9906a8058257d528fd6fe756e37a1e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242202428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d82ba894be8f5d6526b7dc7396408664a9b19a32405c5d33476ac90538ab384`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:45:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:17:35 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:18:07 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:18:08 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:18:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:18:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:18:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:18:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:18:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:18:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:18:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:18:17 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:18:18 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:18:19 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:18:38 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:18:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ff8ee97053f0fd2c04d1416858c55ed3909995cfc0831aa8f5a40204afd05`  
		Last Modified: Wed, 13 Apr 2022 04:50:46 GMT  
		Size: 638.3 KB (638318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b7414fa4e0939433774e287ba09191bca7e808e728adc8bf3c3ce1b26ea50`  
		Last Modified: Mon, 25 Apr 2022 21:21:59 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21af46560c679f5ccc42a3c6459c86ec83319e919f8f889665cb122dbb465e`  
		Last Modified: Mon, 25 Apr 2022 21:22:15 GMT  
		Size: 14.2 MB (14238735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b0f775ed9f809c59455ec9625c83c18ba9ac32b456cf504d0c8a3bb7b15f8`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a421645aec5009da45834b2835830b440c3da7f8b0f14889a32b64015b79fb5`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0fbeeb7476cfecc4f610d18fa06e3faf4cb08844806174e62bd8ca56cd10a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cc3d5e7a3f1b072138f955361688a44e041209f404662fd53b00cb54e758a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29529d78e3af49ca347462d245bb89c20b5897986acec557b8c17d8fe568ca86`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d59dbb39cb3b1525d9595055e2116e7fde476b1af040e47e500e7ddf460e52`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112715a31629216318fb61cfb76dce5c4ddad55b5aca9dd265d4abb009660a`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7274608e1c2e3e6a98f0d9eee200338a3eb77a2d315eeeef18ef8ba33682`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028a09180fa423ea4167dbce9d52b10d0ef23f4c05538d9be8012f7f63da154`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a568da62c45dafbbc16dfeb8b91cd1e67b9b549e72d8f7c6c76202c52a4426`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda8364a6d90b372db004dd3d1cebeb76cc8650fdbd5157eca53edca7b864d6`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65cc32ef8c70486456808de6df2222050d907cfb239fd48f9c7ac8c0748a5e7`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefe909dafbf401bfed81021f3d8d6c1ef9daff428c5cec6184db94484167b4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf8775a48ae02e9ac48a56ebf7808412b9f1c60876f9f3447b282d4ffccfe4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 347.8 KB (347758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136a5dca0069e8c5e5d3fc44538572f5aaf0c7abfbde605abf6df2c1ecdf28f`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-alpine`

```console
$ docker pull caddy@sha256:e602ecd5eed4cae0d809ef6cdd2b0faa091da3cea6f71dbfdfa924411c744b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.5.0-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:9fd29c443b9632275c7dee65b736044bf3eef7f0ff0acde17524d6bfa565d9c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16780958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd701a89dc68bf9b2f5f06994371e9c57d3991f35dd25eae9b72aa30fdb2d99`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:25:00 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:25:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:30:30 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:30:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:30:33 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:30:35 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:30:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ed6b8c4412bcd2bb1f40611012b40444b12071baf4884d0e75044fc1f32c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 291.5 KB (291522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff7bd6e2c9d7717705a52c1d27654581f987e1a43d2c9f3220ce850a5cdad`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a338b6679706fd2d1cd3856187d469aa5666daeaec9011f4a36dec026c557`  
		Last Modified: Tue, 26 Apr 2022 00:30:58 GMT  
		Size: 13.7 MB (13668896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0522358bf40c87db949e3b98ad737bc00126a5c9204927ead005f2c8c6d1f40`  
		Last Modified: Tue, 26 Apr 2022 00:30:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:4fb2aa089fe64de9452ea153e8fcd45f77433bb884944de7ddaf659e776f9e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16046721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd6649c19066b2dfa04d56d12bf7a3c093a73b6b1cf203cd9502a608efcae7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:15:01 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:15:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:49:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:49:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:49:37 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:49:38 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:49:38 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:49:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b230dd773e10769a2eb3e507260d2470a646efd48a639739ba8852b2915302`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 291.7 KB (291685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac48280871fa0cc6e20550e9909af62acb5b3793a4ada967e49e60367ec386e`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e13dd2006703558a44bf92c22d7b86267519c8e0a45876f765416420a52c8b`  
		Last Modified: Mon, 25 Apr 2022 20:51:11 GMT  
		Size: 13.1 MB (13127083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4eba6efd59e2065bc9bace41408b8e28e21c5f13233e039ac9f22fa7114e0`  
		Last Modified: Mon, 25 Apr 2022 20:51:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:4b653da1faf978146d3f353f96f5fec6a3d3dbe61eb226a9bc88310f8a7ac539
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15830530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e429c13a17afa4f600f294adcd8fb8fcd0e02f7d2b3a710e1e74c227c6b5307`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:33:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:33:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:57:32 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:57:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:57:38 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:57:39 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:57:44 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03203881a2568530a735b6e0e7a40ebb79adedc5193a675807b04eeb92cc6ed1`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 290.7 KB (290668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2de87d2e387fcc410ddd706bbe177b2a04b5137087a6ffca70b45c80dc976e0`  
		Last Modified: Tue, 05 Apr 2022 06:35:08 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8925c0c6962de2061a8f0a52f33e90a84c0d94c419622219a02b70ea6029831`  
		Last Modified: Mon, 25 Apr 2022 20:59:12 GMT  
		Size: 13.1 MB (13109556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a04801b9fe9d62e96942e841a278e2961fe3a50e31db66650c473be128e86`  
		Last Modified: Mon, 25 Apr 2022 20:59:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:69ab7c3ae40b72983a025617186f81a14adfe4e65bf060d6a8ded0b2027ad049
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15515390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1ed8512d16f85e28c907452f68a543b178d498bd69a88a4205b07809810c69`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:12:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:45:10 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:45:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:45:15 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:45:16 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:45:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:45:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:45:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:45:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:45:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:45:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:45:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:45:24 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:45:25 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:45:26 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:45:27 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:45:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa37f2341b1e6d98420668c9bc849a47f2c471d159b2303885040bd8d0a92f`  
		Last Modified: Tue, 05 Apr 2022 03:13:38 GMT  
		Size: 291.3 KB (291301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e87f72d84fd403dc0ea7d95672e5865925fca64a932f046b39035e8d3b43aae`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 5.7 KB (5747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffedcd6293512f192bfd7798cf59a8f7121658d14b7da6b8ed96d43b9ea1bd4`  
		Last Modified: Tue, 26 Apr 2022 00:46:14 GMT  
		Size: 12.5 MB (12501711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182c8210bf3bfdf3f311ac5ca0c803504516aa3979d448446e4b23a7414555db`  
		Last Modified: Tue, 26 Apr 2022 00:46:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:a20a2a180cce249a16be3b791cdde01779ffd91a4a9463bba45043e550f0bbab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11db83c89ecf795051de8117ab85b76db190a2f1bc5afd8ac113742dfd90522`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:08:34 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:08:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:17:24 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:17:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:17:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:17:50 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:17:53 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:17:58 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:18:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:18:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:18:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:18:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:18:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:18:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:18:31 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:18:35 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:18:39 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:18:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:18:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743509d6ced044a369685ebb068417e8757981a39d1b397c7b0182ab89f83528`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 293.7 KB (293721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029325992e21f613a5b486751627c7d5e5c7622ec29d4d170549f4dac13ad291`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadee40bb24012aa5a86d9d08c35465ea6747b388276fba98b2b23d8ab36e83d`  
		Last Modified: Mon, 25 Apr 2022 20:20:00 GMT  
		Size: 12.1 MB (12087346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aff6b8f6a27a0579cb3553f1b5da34c73a8d13bc2c46b71a42bffcbb433332`  
		Last Modified: Mon, 25 Apr 2022 20:19:58 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:70f645012314bf2deafbf43b697acd07d73a9dea2fc00a9e37ef66208f682fd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3584f54e8dcb7110aa2a2d26dd4917d281cf487e69e4a327ffb2b497250bdf95`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:41:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:41:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:41:42 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:41:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:41:47 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:41:49 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:41:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8cc7c7c7ffd67f5740add448d341753330a2abdc6ed06e995cb7d28de381ab`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 291.8 KB (291821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f8e9524a50422cbb86b1c5e3af26710e4b65591ecc118a5079f1aa7fe5a67`  
		Last Modified: Tue, 05 Apr 2022 06:20:45 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ec2ded8fc151b5e2f97ea39505dda37e06f7e69f7e6b71e482b6959c5d72a8`  
		Last Modified: Mon, 25 Apr 2022 20:42:47 GMT  
		Size: 13.2 MB (13226741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636e08e595808f97112a31aecb09c32c3139808cf61e83ca37ba447853ecc421`  
		Last Modified: Mon, 25 Apr 2022 20:42:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-builder`

```console
$ docker pull caddy@sha256:e67e63adda0c63a6e2897ccbe67d257d363986bb0add0a87460e7e5b21f68fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2803; amd64
	-	windows version 10.0.20348.643; amd64

### `caddy:2.5.0-builder` - linux; amd64

```console
$ docker pull caddy@sha256:9650c5d624699fbfc7797f0a97d951f569f8bbfef959e02876be98384c53c32a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126769661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9e8161d584d9f23032b2316b7eb8438879699e1486ad8d0090e8e2c15f8de6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:20:33 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 02:34:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 02:34:25 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 02:34:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 02:34:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 02:34:25 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:19:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:30:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:30:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:30:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6858aa20941bdfe0d406b2e4db477feeccf42ca6e40478043b721c6a66f9d1b6`  
		Last Modified: Thu, 14 Apr 2022 02:37:21 GMT  
		Size: 115.6 MB (115569906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8029b02d49777774618d41ab3a1f7f4f32f7d4b10453afd26a184b8787beaa`  
		Last Modified: Thu, 14 Apr 2022 02:37:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8852fa41bd6ab92e973a3316d6db4a27e9b1844abac8363c94c241958de8ad22`  
		Last Modified: Thu, 14 Apr 2022 18:20:07 GMT  
		Size: 6.8 MB (6823100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e8b043cf75cf1c9c8457f53b1bd377c3efd34c07cee9f55c8bde83b13ef585`  
		Last Modified: Tue, 26 Apr 2022 00:31:10 GMT  
		Size: 1.3 MB (1289413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f16575d63df54107d98c6de6302604e3baecf850fcfeb0a0dd6cfd9408c9d`  
		Last Modified: Tue, 26 Apr 2022 00:31:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:8166e6393ad9b0c4953d6c5bf47942e76921dd3f1ee0b6348fefe6b301effbcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122763889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccdbba9972abfdc57c2b74bb66ed897a9d5237e00a1bc42323578d365b7f392`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:49:35 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:03:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:03:33 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:03:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:03:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:03:36 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:50:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:49:59 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:49:59 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:50:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:50:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:50:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:50:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d487bef959ea51d4b707107d10bc8bb2cabb35c3d0e890400da9558498fcfae9`  
		Last Modified: Thu, 14 Apr 2022 00:10:34 GMT  
		Size: 112.0 MB (111960610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232d226d7216d6a78d6f22f1281ea887106f683641e6690999b23c156756d175`  
		Last Modified: Thu, 14 Apr 2022 00:09:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7dcd4972b24cf7ffe78c888061ef282e320f7a4c8aaa1384a55e7e28bd933c`  
		Last Modified: Thu, 14 Apr 2022 18:52:06 GMT  
		Size: 6.7 MB (6679287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be30e34b457ad8574d39820dcb20ff46f0329eec7498768b15691e314e82c308`  
		Last Modified: Mon, 25 Apr 2022 20:51:27 GMT  
		Size: 1.2 MB (1229164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1fabe7aa5b43f66bb040de9a4159250cec20a1d1f03c1bb56a94ca7857424b`  
		Last Modified: Mon, 25 Apr 2022 20:51:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f4a9899c053b29a3ae89a39cb76179c4f1a1b2c9480182e1785e7a4934de6672
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121607328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254d9278b4582c41c742295083ee2604578f59a1724d4ad9de237f56bc606d91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:16:49 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 03:23:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 03:23:16 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 03:23:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 03:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 03:23:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:56:20 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:58:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:58:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0a2cd126c67e6f9de5c0d2b9a8677d1f9ddf783df14e2ee2b65a4b837f781f`  
		Last Modified: Thu, 14 Apr 2022 03:32:44 GMT  
		Size: 111.7 MB (111729644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862413253fa7da1bfa2e411396d8013220cad00d664feea8f1757d91782065a3`  
		Last Modified: Thu, 14 Apr 2022 03:31:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edfefe81ed126a91f93489eb7294d5726270035f8a8af38291865530e667992`  
		Last Modified: Thu, 14 Apr 2022 18:57:58 GMT  
		Size: 6.0 MB (5953508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e680043769b7413a92b4bc4acb8e48a9e5ef164dc1c0e4685f3ebcc82c1c8`  
		Last Modified: Mon, 25 Apr 2022 20:59:27 GMT  
		Size: 1.2 MB (1228017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96a371a805895e54abe0b94c02a933bcbb6d1c50fa2fe09cbb9ca01bc4bdf09`  
		Last Modified: Mon, 25 Apr 2022 20:59:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:5bf6a3ce425975a90be678060a078ca9a13f0edb86b1755feadda66023a21ad5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121531748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65178889870010211120234bf1de0f8fe1154f42a122aec6d31ef5f44ca8ac9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:41:03 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:46:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:46:11 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:46:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:46:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:46:14 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:40:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:45:37 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:45:37 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:45:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:45:42 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:45:42 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59105010ca6c9ed528dc03f6c683c1bc8cd362cabe6df8b6ffe5cb7ea9a5d7a6`  
		Last Modified: Wed, 13 Apr 2022 23:49:58 GMT  
		Size: 110.4 MB (110425230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a657773900190e59f0ba6a0b06f6708be5a593336955df99496b40dd24e06d`  
		Last Modified: Wed, 13 Apr 2022 23:49:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb01e300b70916735527d066ade51d96bf1499fcc73f8e20921d8e6583b2ac7`  
		Last Modified: Thu, 14 Apr 2022 18:41:03 GMT  
		Size: 6.9 MB (6928572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324f0194c126d51157b32379352f8b4f91de641fa18400652f8d8f63a5100a10`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 1.2 MB (1189015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9690c7f39dbf1884a401e00ac496f19a144843007e3c3fd6c0b0ff1d216a812`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:2691a6ee70d65bd303bad70ee1acecd1ea7f27bee204ae088f61718ea5abc728
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122163242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a8e7dfa0559e1a8dbb14192d1d213837b57b559b2eb52d99526000967eaaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:52 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:33:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:33:21 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:33:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:33:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:33:37 GMT
WORKDIR /go
# Thu, 14 Apr 2022 19:18:31 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:19:04 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:19:08 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:19:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:19:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:19:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7b70e9365a42d1502d1309f3dc8545df5b5eb802bf656ac8d1a9adc0ca38e`  
		Last Modified: Thu, 14 Apr 2022 00:38:51 GMT  
		Size: 110.6 MB (110577271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52b4fb28789c7d8a190d4b1275b480c68ef6db3f548db9e61dc0bd5f2287c2`  
		Last Modified: Thu, 14 Apr 2022 00:38:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90034960a371e7877490974def61ec2afab2b9037cf021f8b268adf23f745b1f`  
		Last Modified: Thu, 14 Apr 2022 19:19:39 GMT  
		Size: 7.3 MB (7323527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b419307a290fa200d4ee1d283b336f67595b3dae2a96a545da0076a8f2f0b3a8`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 1.2 MB (1176369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbfaebc331dbb2554a5f8e3bc4ab37cab3cdbc0bee0ae7c0105a46e734b23bb`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder` - linux; s390x

```console
$ docker pull caddy@sha256:6254569039892bf2b972edc670fa1d0c02a4dbe158b5a6fc7503294d2ca02867
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124533779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1144cfb81d01915e8fe650368df288819b27dcb6e48f6742561aff5bfcb0e692`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:49 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:53:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:54:15 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:54:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:54:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:54:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:41:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:42:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:42:00 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:42:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:42:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:42:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:42:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ce7cc2608f8fa7ccebc2bd15f044fe91007681fdf9e3497b835c6671ea698`  
		Last Modified: Thu, 14 Apr 2022 00:01:54 GMT  
		Size: 113.5 MB (113483469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eebd463aa6406b85ba12e73255070fbd1566b013a0ca9f3fb5d3ccf5887df95`  
		Last Modified: Thu, 14 Apr 2022 00:01:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7324a2146e85ce6ede318cd28053e0977db3f0488b3ce78af656c65965e9001c`  
		Last Modified: Thu, 14 Apr 2022 18:42:50 GMT  
		Size: 6.9 MB (6933814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea609b474b313d4fd8f799684994c78a72930632aef028aef80beccb66e2b1`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 1.2 MB (1243136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378733785688e297f1ea3489b24dc76f584f16e7e7c75272ab18709fb8f18969`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:5e1112c2b251cd713257f116402a8b08c70b02536221f1c00e35ede48df2712f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888993144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a554cab996e7da76ef02819ef330a4fb26f3f9c493a7491141f84a9a33cfdce8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:34:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:34:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:34:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:34:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:37:05 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:38:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:55:20 GMT
ENV GOLANG_VERSION=1.17.9
# Wed, 13 Apr 2022 03:02:03 GMT
RUN $url = 'https://dl.google.com/go/go1.17.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '82752c3313cc6c1e1b5d73743a3ec569b09a14246fc2cb0824cf30f9f42a6005'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 03:02:09 GMT
WORKDIR C:\go
# Wed, 13 Apr 2022 04:41:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:18:48 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:18:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:19:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:19:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b761254212cd472f566f902a9830a91c33e94d06fb02a0192e29fe447bf98`  
		Last Modified: Wed, 13 Apr 2022 03:15:11 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210c142bbabba5cac6b3d06dc265578eafda02e9f54b2b955129652065abba5`  
		Last Modified: Wed, 13 Apr 2022 03:15:05 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24b5fea0cadfc385f0501b3cd52647d69ba5dd030f05bc637848ed7298ed45e`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1490fa326c6ac4254cc7e87bd773641c1a74d6d68ef0ee562e1296aa6e5ba09`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5425f63a29b9eb9b5bbbf135d080f8b1d2415a665b41591175a49f41da70d`  
		Last Modified: Wed, 13 Apr 2022 03:15:23 GMT  
		Size: 25.5 MB (25453409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf5f939642f2aaa6426ec58683c461b2fc27f9b92ed53ceea3d53e5f5b8d18d`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ec6181c5a38a1257f1181b0b390b0fa168627daeb103a617f04cf11c9666`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 328.4 KB (328368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6a29e70c078bf2fc470013ea504caa6d82ef66cd3af18be02f62f0d134dff6`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73a058a0e83dbc0674b085ab0d0151f94531062126dc4b1f43b0084df40fb62`  
		Last Modified: Wed, 13 Apr 2022 03:21:14 GMT  
		Size: 145.6 MB (145578329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde9b48a173bb3f29a006a2592b0bd8c63b07c7323137db4862e9a98fdde16b0`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49552906c9650efac10c4f00d5c31cebf6f940a05f00b03588df052cff5966c5`  
		Last Modified: Wed, 13 Apr 2022 04:50:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3892f065d9ae068931752897908cf2f42b7e70c10612f0d0c861d34b10c392d`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141d6a6f4de9ad79b32cd3b282f72556c753906066f6c959c90b9c98ed469f3`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151094a4fbe124963e13c2d1fb1c5868cfbaa169c003276af989cacbfe5d34b8`  
		Last Modified: Mon, 25 Apr 2022 21:22:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765cbaf262dc38339a50daa75e2a3bfdc536965075ef0683019b9c561b043cec`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.7 MB (1694161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df9d46dbf2556d53c3e38d0059f2c965b2ec2ec1362b393b4b1f1f9faeeec55`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:1b97052faeb50ea5c75cf73629d9b2ffe166382726774f8374c33fc821f12756
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408056049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd58e6419e1957d39f41478ff42606b54104872bb714df26c7bbfd10105c196`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:27:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:28:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:28:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:28:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:29:19 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:30:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:30:08 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:33:47 GMT
RUN $url = 'https://dl.google.com/go/go1.18.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c30bc3f1f7314a953fe208bd9cd5e24bd9403392a6c556ced3677f9f70f71fe1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:33:49 GMT
WORKDIR C:\go
# Thu, 14 Apr 2022 19:21:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:20:16 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:20:17 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:20:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:20:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:20:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df2c1d7d7b9748c6ddb8e9f196dfb2526451470a1256ab4047bece8468ff7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:50 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395e3155b04f913275d2f0e2bd07626c8d9b889b0646bb3fb44414d2df4130d`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3d0b098f175d5015767a5bb9a5641f1a1966ea2e2863b55cae5ae54f7edeb9`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff921731e5c58ad62f0eb62e698dd3033694fd15898c3e94d8021c0097dd912`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b89723742f5296cfb0b6d93c8b65a4995ee4a964d59eae8e96557dffc8f9e`  
		Last Modified: Wed, 13 Apr 2022 03:14:02 GMT  
		Size: 25.7 MB (25714775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0e7bcbbef7fb8a566a25556fc4b487c323359badbd7ab1bc58ab41729a7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67794576dcaaf4ef811c935b4ed0b40efe1487f0d0ab09462473b606d1fd89`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 562.2 KB (562186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2932986f0f385a406d2115ccb58dbf32a1730cf7e1f7f9f520863fcaa3e20d64`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f896ebd03d7af93409bcfb6bbbbd64481e6f575754cf0c600003a48a32d7a0b`  
		Last Modified: Wed, 13 Apr 2022 03:14:42 GMT  
		Size: 152.9 MB (152877366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f82b1974e8addd899731575590ff20cf09b3e97cdfe2ed285fc081b742b331`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52686327c4846c19f28b539d50b9d61e28b6fea5b5fddd0b921f8cbeb53d872e`  
		Last Modified: Thu, 14 Apr 2022 19:23:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe428ae1fd559625e6a41270985f292ad390b7b989a29f33178fbaeb59adaec`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce095f3f10565fda2a8540deb040f3ba4ec12ae51c7de87a7f39a507ee678bd9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808a55a0aa8fdfb2f5ae17966be5e1b3a39b399fd284db0372e9c29f67e2c9c`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4436fe9c1e94384199b902992ccbf1563c9a287bac0825d092d2e9b4d4f5be`  
		Last Modified: Mon, 25 Apr 2022 21:22:46 GMT  
		Size: 1.9 MB (1928477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e271d06fad4e820c1f2d2dd4029cc1c0fb472290b34a50751423c06751f032d9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-builder-alpine`

```console
$ docker pull caddy@sha256:2cf9717916c3411cda2bfd15db21f1f40b43626eac201327da49ce01d40628dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.5.0-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:9650c5d624699fbfc7797f0a97d951f569f8bbfef959e02876be98384c53c32a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126769661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9e8161d584d9f23032b2316b7eb8438879699e1486ad8d0090e8e2c15f8de6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:20:33 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 02:34:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 02:34:25 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 02:34:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 02:34:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 02:34:25 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:19:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:30:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:30:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:30:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6858aa20941bdfe0d406b2e4db477feeccf42ca6e40478043b721c6a66f9d1b6`  
		Last Modified: Thu, 14 Apr 2022 02:37:21 GMT  
		Size: 115.6 MB (115569906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8029b02d49777774618d41ab3a1f7f4f32f7d4b10453afd26a184b8787beaa`  
		Last Modified: Thu, 14 Apr 2022 02:37:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8852fa41bd6ab92e973a3316d6db4a27e9b1844abac8363c94c241958de8ad22`  
		Last Modified: Thu, 14 Apr 2022 18:20:07 GMT  
		Size: 6.8 MB (6823100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e8b043cf75cf1c9c8457f53b1bd377c3efd34c07cee9f55c8bde83b13ef585`  
		Last Modified: Tue, 26 Apr 2022 00:31:10 GMT  
		Size: 1.3 MB (1289413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f16575d63df54107d98c6de6302604e3baecf850fcfeb0a0dd6cfd9408c9d`  
		Last Modified: Tue, 26 Apr 2022 00:31:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:8166e6393ad9b0c4953d6c5bf47942e76921dd3f1ee0b6348fefe6b301effbcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122763889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccdbba9972abfdc57c2b74bb66ed897a9d5237e00a1bc42323578d365b7f392`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:49:35 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:03:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:03:33 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:03:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:03:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:03:36 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:50:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:49:59 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:49:59 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:50:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:50:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:50:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:50:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d487bef959ea51d4b707107d10bc8bb2cabb35c3d0e890400da9558498fcfae9`  
		Last Modified: Thu, 14 Apr 2022 00:10:34 GMT  
		Size: 112.0 MB (111960610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232d226d7216d6a78d6f22f1281ea887106f683641e6690999b23c156756d175`  
		Last Modified: Thu, 14 Apr 2022 00:09:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7dcd4972b24cf7ffe78c888061ef282e320f7a4c8aaa1384a55e7e28bd933c`  
		Last Modified: Thu, 14 Apr 2022 18:52:06 GMT  
		Size: 6.7 MB (6679287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be30e34b457ad8574d39820dcb20ff46f0329eec7498768b15691e314e82c308`  
		Last Modified: Mon, 25 Apr 2022 20:51:27 GMT  
		Size: 1.2 MB (1229164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1fabe7aa5b43f66bb040de9a4159250cec20a1d1f03c1bb56a94ca7857424b`  
		Last Modified: Mon, 25 Apr 2022 20:51:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f4a9899c053b29a3ae89a39cb76179c4f1a1b2c9480182e1785e7a4934de6672
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121607328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254d9278b4582c41c742295083ee2604578f59a1724d4ad9de237f56bc606d91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:16:49 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 03:23:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 03:23:16 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 03:23:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 03:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 03:23:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:56:20 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:58:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:58:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0a2cd126c67e6f9de5c0d2b9a8677d1f9ddf783df14e2ee2b65a4b837f781f`  
		Last Modified: Thu, 14 Apr 2022 03:32:44 GMT  
		Size: 111.7 MB (111729644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862413253fa7da1bfa2e411396d8013220cad00d664feea8f1757d91782065a3`  
		Last Modified: Thu, 14 Apr 2022 03:31:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edfefe81ed126a91f93489eb7294d5726270035f8a8af38291865530e667992`  
		Last Modified: Thu, 14 Apr 2022 18:57:58 GMT  
		Size: 6.0 MB (5953508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e680043769b7413a92b4bc4acb8e48a9e5ef164dc1c0e4685f3ebcc82c1c8`  
		Last Modified: Mon, 25 Apr 2022 20:59:27 GMT  
		Size: 1.2 MB (1228017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96a371a805895e54abe0b94c02a933bcbb6d1c50fa2fe09cbb9ca01bc4bdf09`  
		Last Modified: Mon, 25 Apr 2022 20:59:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:5bf6a3ce425975a90be678060a078ca9a13f0edb86b1755feadda66023a21ad5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121531748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65178889870010211120234bf1de0f8fe1154f42a122aec6d31ef5f44ca8ac9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:41:03 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:46:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:46:11 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:46:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:46:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:46:14 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:40:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:45:37 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:45:37 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:45:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:45:42 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:45:42 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59105010ca6c9ed528dc03f6c683c1bc8cd362cabe6df8b6ffe5cb7ea9a5d7a6`  
		Last Modified: Wed, 13 Apr 2022 23:49:58 GMT  
		Size: 110.4 MB (110425230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a657773900190e59f0ba6a0b06f6708be5a593336955df99496b40dd24e06d`  
		Last Modified: Wed, 13 Apr 2022 23:49:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb01e300b70916735527d066ade51d96bf1499fcc73f8e20921d8e6583b2ac7`  
		Last Modified: Thu, 14 Apr 2022 18:41:03 GMT  
		Size: 6.9 MB (6928572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324f0194c126d51157b32379352f8b4f91de641fa18400652f8d8f63a5100a10`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 1.2 MB (1189015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9690c7f39dbf1884a401e00ac496f19a144843007e3c3fd6c0b0ff1d216a812`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:2691a6ee70d65bd303bad70ee1acecd1ea7f27bee204ae088f61718ea5abc728
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122163242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a8e7dfa0559e1a8dbb14192d1d213837b57b559b2eb52d99526000967eaaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:52 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:33:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:33:21 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:33:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:33:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:33:37 GMT
WORKDIR /go
# Thu, 14 Apr 2022 19:18:31 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:19:04 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:19:08 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:19:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:19:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:19:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7b70e9365a42d1502d1309f3dc8545df5b5eb802bf656ac8d1a9adc0ca38e`  
		Last Modified: Thu, 14 Apr 2022 00:38:51 GMT  
		Size: 110.6 MB (110577271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52b4fb28789c7d8a190d4b1275b480c68ef6db3f548db9e61dc0bd5f2287c2`  
		Last Modified: Thu, 14 Apr 2022 00:38:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90034960a371e7877490974def61ec2afab2b9037cf021f8b268adf23f745b1f`  
		Last Modified: Thu, 14 Apr 2022 19:19:39 GMT  
		Size: 7.3 MB (7323527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b419307a290fa200d4ee1d283b336f67595b3dae2a96a545da0076a8f2f0b3a8`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 1.2 MB (1176369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbfaebc331dbb2554a5f8e3bc4ab37cab3cdbc0bee0ae7c0105a46e734b23bb`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:6254569039892bf2b972edc670fa1d0c02a4dbe158b5a6fc7503294d2ca02867
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124533779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1144cfb81d01915e8fe650368df288819b27dcb6e48f6742561aff5bfcb0e692`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:49 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:53:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:54:15 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:54:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:54:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:54:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:41:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:42:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:42:00 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:42:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:42:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:42:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:42:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ce7cc2608f8fa7ccebc2bd15f044fe91007681fdf9e3497b835c6671ea698`  
		Last Modified: Thu, 14 Apr 2022 00:01:54 GMT  
		Size: 113.5 MB (113483469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eebd463aa6406b85ba12e73255070fbd1566b013a0ca9f3fb5d3ccf5887df95`  
		Last Modified: Thu, 14 Apr 2022 00:01:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7324a2146e85ce6ede318cd28053e0977db3f0488b3ce78af656c65965e9001c`  
		Last Modified: Thu, 14 Apr 2022 18:42:50 GMT  
		Size: 6.9 MB (6933814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea609b474b313d4fd8f799684994c78a72930632aef028aef80beccb66e2b1`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 1.2 MB (1243136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378733785688e297f1ea3489b24dc76f584f16e7e7c75272ab18709fb8f18969`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:b9480bf84ce2dace3248013b5c66c97e54e689c11831f8ab0c4d5f1849780caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `caddy:2.5.0-builder-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:5e1112c2b251cd713257f116402a8b08c70b02536221f1c00e35ede48df2712f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888993144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a554cab996e7da76ef02819ef330a4fb26f3f9c493a7491141f84a9a33cfdce8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:34:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:34:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:34:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:34:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:37:05 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:38:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:55:20 GMT
ENV GOLANG_VERSION=1.17.9
# Wed, 13 Apr 2022 03:02:03 GMT
RUN $url = 'https://dl.google.com/go/go1.17.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '82752c3313cc6c1e1b5d73743a3ec569b09a14246fc2cb0824cf30f9f42a6005'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 03:02:09 GMT
WORKDIR C:\go
# Wed, 13 Apr 2022 04:41:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:18:48 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:18:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:19:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:19:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b761254212cd472f566f902a9830a91c33e94d06fb02a0192e29fe447bf98`  
		Last Modified: Wed, 13 Apr 2022 03:15:11 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210c142bbabba5cac6b3d06dc265578eafda02e9f54b2b955129652065abba5`  
		Last Modified: Wed, 13 Apr 2022 03:15:05 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24b5fea0cadfc385f0501b3cd52647d69ba5dd030f05bc637848ed7298ed45e`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1490fa326c6ac4254cc7e87bd773641c1a74d6d68ef0ee562e1296aa6e5ba09`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5425f63a29b9eb9b5bbbf135d080f8b1d2415a665b41591175a49f41da70d`  
		Last Modified: Wed, 13 Apr 2022 03:15:23 GMT  
		Size: 25.5 MB (25453409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf5f939642f2aaa6426ec58683c461b2fc27f9b92ed53ceea3d53e5f5b8d18d`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ec6181c5a38a1257f1181b0b390b0fa168627daeb103a617f04cf11c9666`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 328.4 KB (328368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6a29e70c078bf2fc470013ea504caa6d82ef66cd3af18be02f62f0d134dff6`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73a058a0e83dbc0674b085ab0d0151f94531062126dc4b1f43b0084df40fb62`  
		Last Modified: Wed, 13 Apr 2022 03:21:14 GMT  
		Size: 145.6 MB (145578329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde9b48a173bb3f29a006a2592b0bd8c63b07c7323137db4862e9a98fdde16b0`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49552906c9650efac10c4f00d5c31cebf6f940a05f00b03588df052cff5966c5`  
		Last Modified: Wed, 13 Apr 2022 04:50:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3892f065d9ae068931752897908cf2f42b7e70c10612f0d0c861d34b10c392d`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141d6a6f4de9ad79b32cd3b282f72556c753906066f6c959c90b9c98ed469f3`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151094a4fbe124963e13c2d1fb1c5868cfbaa169c003276af989cacbfe5d34b8`  
		Last Modified: Mon, 25 Apr 2022 21:22:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765cbaf262dc38339a50daa75e2a3bfdc536965075ef0683019b9c561b043cec`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.7 MB (1694161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df9d46dbf2556d53c3e38d0059f2c965b2ec2ec1362b393b4b1f1f9faeeec55`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4ae9973b09d5f6d1623aaf1cba218c72ea57e553d3bbdbfbf2ee3ecb4d96bdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `caddy:2.5.0-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:1b97052faeb50ea5c75cf73629d9b2ffe166382726774f8374c33fc821f12756
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408056049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd58e6419e1957d39f41478ff42606b54104872bb714df26c7bbfd10105c196`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:27:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:28:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:28:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:28:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:29:19 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:30:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:30:08 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:33:47 GMT
RUN $url = 'https://dl.google.com/go/go1.18.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c30bc3f1f7314a953fe208bd9cd5e24bd9403392a6c556ced3677f9f70f71fe1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:33:49 GMT
WORKDIR C:\go
# Thu, 14 Apr 2022 19:21:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:20:16 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:20:17 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:20:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:20:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:20:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df2c1d7d7b9748c6ddb8e9f196dfb2526451470a1256ab4047bece8468ff7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:50 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395e3155b04f913275d2f0e2bd07626c8d9b889b0646bb3fb44414d2df4130d`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3d0b098f175d5015767a5bb9a5641f1a1966ea2e2863b55cae5ae54f7edeb9`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff921731e5c58ad62f0eb62e698dd3033694fd15898c3e94d8021c0097dd912`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b89723742f5296cfb0b6d93c8b65a4995ee4a964d59eae8e96557dffc8f9e`  
		Last Modified: Wed, 13 Apr 2022 03:14:02 GMT  
		Size: 25.7 MB (25714775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0e7bcbbef7fb8a566a25556fc4b487c323359badbd7ab1bc58ab41729a7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67794576dcaaf4ef811c935b4ed0b40efe1487f0d0ab09462473b606d1fd89`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 562.2 KB (562186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2932986f0f385a406d2115ccb58dbf32a1730cf7e1f7f9f520863fcaa3e20d64`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f896ebd03d7af93409bcfb6bbbbd64481e6f575754cf0c600003a48a32d7a0b`  
		Last Modified: Wed, 13 Apr 2022 03:14:42 GMT  
		Size: 152.9 MB (152877366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f82b1974e8addd899731575590ff20cf09b3e97cdfe2ed285fc081b742b331`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52686327c4846c19f28b539d50b9d61e28b6fea5b5fddd0b921f8cbeb53d872e`  
		Last Modified: Thu, 14 Apr 2022 19:23:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe428ae1fd559625e6a41270985f292ad390b7b989a29f33178fbaeb59adaec`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce095f3f10565fda2a8540deb040f3ba4ec12ae51c7de87a7f39a507ee678bd9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808a55a0aa8fdfb2f5ae17966be5e1b3a39b399fd284db0372e9c29f67e2c9c`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4436fe9c1e94384199b902992ccbf1563c9a287bac0825d092d2e9b4d4f5be`  
		Last Modified: Mon, 25 Apr 2022 21:22:46 GMT  
		Size: 1.9 MB (1928477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e271d06fad4e820c1f2d2dd4029cc1c0fb472290b34a50751423c06751f032d9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-windowsservercore`

```console
$ docker pull caddy@sha256:0382e21e9d9d4449ad0dbe82519f107c4fe3eb88d5b32bd149c017f51b6784e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2803; amd64
	-	windows version 10.0.20348.643; amd64

### `caddy:2.5.0-windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:ac6afd8f502178001d3c6631753a6e4457830f2945acfb4f223b359312151739
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730628642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be5151970c967a41fa277f73d3ea5c6c2441dd532017ff7ba63f94b90b5815`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:38:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:14:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:16:13 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:16:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:16:23 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:16:24 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:16:25 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:17:17 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8129805e9e333a66c903463c3cbf8ee34716da4665df9a65dd4176eba5c5f06`  
		Last Modified: Wed, 13 Apr 2022 04:49:35 GMT  
		Size: 378.1 KB (378101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df92a93e366c3079de7a894225b5af047aced370ac7cc37db8a6a1efda1d68`  
		Last Modified: Mon, 25 Apr 2022 21:21:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83100cacadedcaa12031a24db1db453af535c1d938ebff9871930a6890125a4`  
		Last Modified: Mon, 25 Apr 2022 21:21:39 GMT  
		Size: 14.0 MB (14007463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2025016da8c10d71dc51b48c0c1b4c09cd52cfb337da6fd522df0f1d942ac2e`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d207d693dada181cafd0c7fb97ab2dfa21fdc798356667ebf3e18615af2cc1`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf8198462811b78954d0490e9bd2654c63af7f5590b0a316abcd6873b887f6c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982c6b1d8f9c21d5422f34061954adc18f796ee38efba6b7c7a5efc4ab11d2c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf52c26accb9bf3880af82d0bd3e1df4bf2de7d5e977e42fccdf515d198b190`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dc5e7fac918f26a223bdc96e1913d856b1bfa82e49af4dcbb9ee132dd0079`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0620c742ae20f8c7f4a81d372f9a25b706bf19be63e67271f504c9581a3a23a`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c575b1dbcfc0a0a68adcf4e48d4e2977a495bbd529fa0453b1a132185f45d8`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced94298b1f6c583462eee02e7ff2fbe680380e9e4081e9f33820bb0f0cf0c55`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda180811a77093bcc12e90c6f09509b092e2a3c5351635fa3a3711d54073137`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec34e60db92a527d1bcaacf30b0263c1aad257b56e842915b61ca4f467854253`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684c375495ff3e6194436cd4ad2d1b3b152576f3700e90e201efccc84457816`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07262f33fbd716916cd70767bb9863a076ed51716250ceec3769e039dec513`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b340376e6b0dbbfb01d19a74849b15f4d430e8634f8fedb81851637648dae26`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 300.0 KB (299995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa021badff18bcd5b01c95b400972c8b76fcf354efc8805e2f1821ba968775`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-windowsservercore` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:28e63cb2eaf6998239e5b537831968ba4d9906a8058257d528fd6fe756e37a1e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242202428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d82ba894be8f5d6526b7dc7396408664a9b19a32405c5d33476ac90538ab384`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:45:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:17:35 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:18:07 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:18:08 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:18:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:18:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:18:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:18:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:18:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:18:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:18:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:18:17 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:18:18 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:18:19 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:18:38 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:18:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ff8ee97053f0fd2c04d1416858c55ed3909995cfc0831aa8f5a40204afd05`  
		Last Modified: Wed, 13 Apr 2022 04:50:46 GMT  
		Size: 638.3 KB (638318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b7414fa4e0939433774e287ba09191bca7e808e728adc8bf3c3ce1b26ea50`  
		Last Modified: Mon, 25 Apr 2022 21:21:59 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21af46560c679f5ccc42a3c6459c86ec83319e919f8f889665cb122dbb465e`  
		Last Modified: Mon, 25 Apr 2022 21:22:15 GMT  
		Size: 14.2 MB (14238735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b0f775ed9f809c59455ec9625c83c18ba9ac32b456cf504d0c8a3bb7b15f8`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a421645aec5009da45834b2835830b440c3da7f8b0f14889a32b64015b79fb5`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0fbeeb7476cfecc4f610d18fa06e3faf4cb08844806174e62bd8ca56cd10a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cc3d5e7a3f1b072138f955361688a44e041209f404662fd53b00cb54e758a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29529d78e3af49ca347462d245bb89c20b5897986acec557b8c17d8fe568ca86`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d59dbb39cb3b1525d9595055e2116e7fde476b1af040e47e500e7ddf460e52`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112715a31629216318fb61cfb76dce5c4ddad55b5aca9dd265d4abb009660a`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7274608e1c2e3e6a98f0d9eee200338a3eb77a2d315eeeef18ef8ba33682`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028a09180fa423ea4167dbce9d52b10d0ef23f4c05538d9be8012f7f63da154`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a568da62c45dafbbc16dfeb8b91cd1e67b9b549e72d8f7c6c76202c52a4426`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda8364a6d90b372db004dd3d1cebeb76cc8650fdbd5157eca53edca7b864d6`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65cc32ef8c70486456808de6df2222050d907cfb239fd48f9c7ac8c0748a5e7`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefe909dafbf401bfed81021f3d8d6c1ef9daff428c5cec6184db94484167b4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf8775a48ae02e9ac48a56ebf7808412b9f1c60876f9f3447b282d4ffccfe4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 347.8 KB (347758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136a5dca0069e8c5e5d3fc44538572f5aaf0c7abfbde605abf6df2c1ecdf28f`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-windowsservercore-1809`

```console
$ docker pull caddy@sha256:bc778a53e3357f5c8a9c100b8750dc0a3a608315519c727b0b944b910ebc066b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `caddy:2.5.0-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:ac6afd8f502178001d3c6631753a6e4457830f2945acfb4f223b359312151739
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730628642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be5151970c967a41fa277f73d3ea5c6c2441dd532017ff7ba63f94b90b5815`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:38:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:14:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:16:13 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:16:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:16:23 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:16:24 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:16:25 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:17:17 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8129805e9e333a66c903463c3cbf8ee34716da4665df9a65dd4176eba5c5f06`  
		Last Modified: Wed, 13 Apr 2022 04:49:35 GMT  
		Size: 378.1 KB (378101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df92a93e366c3079de7a894225b5af047aced370ac7cc37db8a6a1efda1d68`  
		Last Modified: Mon, 25 Apr 2022 21:21:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83100cacadedcaa12031a24db1db453af535c1d938ebff9871930a6890125a4`  
		Last Modified: Mon, 25 Apr 2022 21:21:39 GMT  
		Size: 14.0 MB (14007463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2025016da8c10d71dc51b48c0c1b4c09cd52cfb337da6fd522df0f1d942ac2e`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d207d693dada181cafd0c7fb97ab2dfa21fdc798356667ebf3e18615af2cc1`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf8198462811b78954d0490e9bd2654c63af7f5590b0a316abcd6873b887f6c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982c6b1d8f9c21d5422f34061954adc18f796ee38efba6b7c7a5efc4ab11d2c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf52c26accb9bf3880af82d0bd3e1df4bf2de7d5e977e42fccdf515d198b190`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dc5e7fac918f26a223bdc96e1913d856b1bfa82e49af4dcbb9ee132dd0079`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0620c742ae20f8c7f4a81d372f9a25b706bf19be63e67271f504c9581a3a23a`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c575b1dbcfc0a0a68adcf4e48d4e2977a495bbd529fa0453b1a132185f45d8`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced94298b1f6c583462eee02e7ff2fbe680380e9e4081e9f33820bb0f0cf0c55`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda180811a77093bcc12e90c6f09509b092e2a3c5351635fa3a3711d54073137`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec34e60db92a527d1bcaacf30b0263c1aad257b56e842915b61ca4f467854253`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684c375495ff3e6194436cd4ad2d1b3b152576f3700e90e201efccc84457816`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07262f33fbd716916cd70767bb9863a076ed51716250ceec3769e039dec513`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b340376e6b0dbbfb01d19a74849b15f4d430e8634f8fedb81851637648dae26`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 300.0 KB (299995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa021badff18bcd5b01c95b400972c8b76fcf354efc8805e2f1821ba968775`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:03edcc30e55a42bb6833408159e70252c0f2f3d51191a6ae23dfe882a87681fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `caddy:2.5.0-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:28e63cb2eaf6998239e5b537831968ba4d9906a8058257d528fd6fe756e37a1e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242202428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d82ba894be8f5d6526b7dc7396408664a9b19a32405c5d33476ac90538ab384`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:45:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:17:35 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:18:07 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:18:08 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:18:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:18:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:18:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:18:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:18:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:18:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:18:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:18:17 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:18:18 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:18:19 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:18:38 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:18:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ff8ee97053f0fd2c04d1416858c55ed3909995cfc0831aa8f5a40204afd05`  
		Last Modified: Wed, 13 Apr 2022 04:50:46 GMT  
		Size: 638.3 KB (638318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b7414fa4e0939433774e287ba09191bca7e808e728adc8bf3c3ce1b26ea50`  
		Last Modified: Mon, 25 Apr 2022 21:21:59 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21af46560c679f5ccc42a3c6459c86ec83319e919f8f889665cb122dbb465e`  
		Last Modified: Mon, 25 Apr 2022 21:22:15 GMT  
		Size: 14.2 MB (14238735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b0f775ed9f809c59455ec9625c83c18ba9ac32b456cf504d0c8a3bb7b15f8`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a421645aec5009da45834b2835830b440c3da7f8b0f14889a32b64015b79fb5`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0fbeeb7476cfecc4f610d18fa06e3faf4cb08844806174e62bd8ca56cd10a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cc3d5e7a3f1b072138f955361688a44e041209f404662fd53b00cb54e758a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29529d78e3af49ca347462d245bb89c20b5897986acec557b8c17d8fe568ca86`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d59dbb39cb3b1525d9595055e2116e7fde476b1af040e47e500e7ddf460e52`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112715a31629216318fb61cfb76dce5c4ddad55b5aca9dd265d4abb009660a`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7274608e1c2e3e6a98f0d9eee200338a3eb77a2d315eeeef18ef8ba33682`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028a09180fa423ea4167dbce9d52b10d0ef23f4c05538d9be8012f7f63da154`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a568da62c45dafbbc16dfeb8b91cd1e67b9b549e72d8f7c6c76202c52a4426`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda8364a6d90b372db004dd3d1cebeb76cc8650fdbd5157eca53edca7b864d6`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65cc32ef8c70486456808de6df2222050d907cfb239fd48f9c7ac8c0748a5e7`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefe909dafbf401bfed81021f3d8d6c1ef9daff428c5cec6184db94484167b4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf8775a48ae02e9ac48a56ebf7808412b9f1c60876f9f3447b282d4ffccfe4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 347.8 KB (347758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136a5dca0069e8c5e5d3fc44538572f5aaf0c7abfbde605abf6df2c1ecdf28f`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:e602ecd5eed4cae0d809ef6cdd2b0faa091da3cea6f71dbfdfa924411c744b99
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
$ docker pull caddy@sha256:9fd29c443b9632275c7dee65b736044bf3eef7f0ff0acde17524d6bfa565d9c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16780958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd701a89dc68bf9b2f5f06994371e9c57d3991f35dd25eae9b72aa30fdb2d99`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:25:00 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:25:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:30:30 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:30:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:30:33 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:30:35 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:30:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ed6b8c4412bcd2bb1f40611012b40444b12071baf4884d0e75044fc1f32c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 291.5 KB (291522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff7bd6e2c9d7717705a52c1d27654581f987e1a43d2c9f3220ce850a5cdad`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a338b6679706fd2d1cd3856187d469aa5666daeaec9011f4a36dec026c557`  
		Last Modified: Tue, 26 Apr 2022 00:30:58 GMT  
		Size: 13.7 MB (13668896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0522358bf40c87db949e3b98ad737bc00126a5c9204927ead005f2c8c6d1f40`  
		Last Modified: Tue, 26 Apr 2022 00:30:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:4fb2aa089fe64de9452ea153e8fcd45f77433bb884944de7ddaf659e776f9e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16046721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd6649c19066b2dfa04d56d12bf7a3c093a73b6b1cf203cd9502a608efcae7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:15:01 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:15:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:49:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:49:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:49:37 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:49:38 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:49:38 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:49:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b230dd773e10769a2eb3e507260d2470a646efd48a639739ba8852b2915302`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 291.7 KB (291685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac48280871fa0cc6e20550e9909af62acb5b3793a4ada967e49e60367ec386e`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e13dd2006703558a44bf92c22d7b86267519c8e0a45876f765416420a52c8b`  
		Last Modified: Mon, 25 Apr 2022 20:51:11 GMT  
		Size: 13.1 MB (13127083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4eba6efd59e2065bc9bace41408b8e28e21c5f13233e039ac9f22fa7114e0`  
		Last Modified: Mon, 25 Apr 2022 20:51:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:4b653da1faf978146d3f353f96f5fec6a3d3dbe61eb226a9bc88310f8a7ac539
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15830530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e429c13a17afa4f600f294adcd8fb8fcd0e02f7d2b3a710e1e74c227c6b5307`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:33:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:33:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:57:32 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:57:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:57:38 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:57:39 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:57:44 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03203881a2568530a735b6e0e7a40ebb79adedc5193a675807b04eeb92cc6ed1`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 290.7 KB (290668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2de87d2e387fcc410ddd706bbe177b2a04b5137087a6ffca70b45c80dc976e0`  
		Last Modified: Tue, 05 Apr 2022 06:35:08 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8925c0c6962de2061a8f0a52f33e90a84c0d94c419622219a02b70ea6029831`  
		Last Modified: Mon, 25 Apr 2022 20:59:12 GMT  
		Size: 13.1 MB (13109556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a04801b9fe9d62e96942e841a278e2961fe3a50e31db66650c473be128e86`  
		Last Modified: Mon, 25 Apr 2022 20:59:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:69ab7c3ae40b72983a025617186f81a14adfe4e65bf060d6a8ded0b2027ad049
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15515390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1ed8512d16f85e28c907452f68a543b178d498bd69a88a4205b07809810c69`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:12:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:45:10 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:45:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:45:15 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:45:16 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:45:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:45:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:45:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:45:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:45:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:45:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:45:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:45:24 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:45:25 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:45:26 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:45:27 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:45:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa37f2341b1e6d98420668c9bc849a47f2c471d159b2303885040bd8d0a92f`  
		Last Modified: Tue, 05 Apr 2022 03:13:38 GMT  
		Size: 291.3 KB (291301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e87f72d84fd403dc0ea7d95672e5865925fca64a932f046b39035e8d3b43aae`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 5.7 KB (5747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffedcd6293512f192bfd7798cf59a8f7121658d14b7da6b8ed96d43b9ea1bd4`  
		Last Modified: Tue, 26 Apr 2022 00:46:14 GMT  
		Size: 12.5 MB (12501711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182c8210bf3bfdf3f311ac5ca0c803504516aa3979d448446e4b23a7414555db`  
		Last Modified: Tue, 26 Apr 2022 00:46:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:a20a2a180cce249a16be3b791cdde01779ffd91a4a9463bba45043e550f0bbab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11db83c89ecf795051de8117ab85b76db190a2f1bc5afd8ac113742dfd90522`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:08:34 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:08:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:17:24 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:17:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:17:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:17:50 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:17:53 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:17:58 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:18:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:18:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:18:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:18:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:18:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:18:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:18:31 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:18:35 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:18:39 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:18:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:18:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743509d6ced044a369685ebb068417e8757981a39d1b397c7b0182ab89f83528`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 293.7 KB (293721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029325992e21f613a5b486751627c7d5e5c7622ec29d4d170549f4dac13ad291`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadee40bb24012aa5a86d9d08c35465ea6747b388276fba98b2b23d8ab36e83d`  
		Last Modified: Mon, 25 Apr 2022 20:20:00 GMT  
		Size: 12.1 MB (12087346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aff6b8f6a27a0579cb3553f1b5da34c73a8d13bc2c46b71a42bffcbb433332`  
		Last Modified: Mon, 25 Apr 2022 20:19:58 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:70f645012314bf2deafbf43b697acd07d73a9dea2fc00a9e37ef66208f682fd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3584f54e8dcb7110aa2a2d26dd4917d281cf487e69e4a327ffb2b497250bdf95`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:41:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:41:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:41:42 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:41:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:41:47 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:41:49 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:41:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8cc7c7c7ffd67f5740add448d341753330a2abdc6ed06e995cb7d28de381ab`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 291.8 KB (291821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f8e9524a50422cbb86b1c5e3af26710e4b65591ecc118a5079f1aa7fe5a67`  
		Last Modified: Tue, 05 Apr 2022 06:20:45 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ec2ded8fc151b5e2f97ea39505dda37e06f7e69f7e6b71e482b6959c5d72a8`  
		Last Modified: Mon, 25 Apr 2022 20:42:47 GMT  
		Size: 13.2 MB (13226741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636e08e595808f97112a31aecb09c32c3139808cf61e83ca37ba447853ecc421`  
		Last Modified: Mon, 25 Apr 2022 20:42:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:e67e63adda0c63a6e2897ccbe67d257d363986bb0add0a87460e7e5b21f68fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2803; amd64
	-	windows version 10.0.20348.643; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:9650c5d624699fbfc7797f0a97d951f569f8bbfef959e02876be98384c53c32a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126769661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9e8161d584d9f23032b2316b7eb8438879699e1486ad8d0090e8e2c15f8de6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:20:33 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 02:34:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 02:34:25 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 02:34:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 02:34:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 02:34:25 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:19:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:30:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:30:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:30:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6858aa20941bdfe0d406b2e4db477feeccf42ca6e40478043b721c6a66f9d1b6`  
		Last Modified: Thu, 14 Apr 2022 02:37:21 GMT  
		Size: 115.6 MB (115569906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8029b02d49777774618d41ab3a1f7f4f32f7d4b10453afd26a184b8787beaa`  
		Last Modified: Thu, 14 Apr 2022 02:37:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8852fa41bd6ab92e973a3316d6db4a27e9b1844abac8363c94c241958de8ad22`  
		Last Modified: Thu, 14 Apr 2022 18:20:07 GMT  
		Size: 6.8 MB (6823100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e8b043cf75cf1c9c8457f53b1bd377c3efd34c07cee9f55c8bde83b13ef585`  
		Last Modified: Tue, 26 Apr 2022 00:31:10 GMT  
		Size: 1.3 MB (1289413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f16575d63df54107d98c6de6302604e3baecf850fcfeb0a0dd6cfd9408c9d`  
		Last Modified: Tue, 26 Apr 2022 00:31:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:8166e6393ad9b0c4953d6c5bf47942e76921dd3f1ee0b6348fefe6b301effbcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122763889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccdbba9972abfdc57c2b74bb66ed897a9d5237e00a1bc42323578d365b7f392`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:49:35 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:03:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:03:33 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:03:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:03:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:03:36 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:50:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:49:59 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:49:59 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:50:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:50:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:50:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:50:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d487bef959ea51d4b707107d10bc8bb2cabb35c3d0e890400da9558498fcfae9`  
		Last Modified: Thu, 14 Apr 2022 00:10:34 GMT  
		Size: 112.0 MB (111960610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232d226d7216d6a78d6f22f1281ea887106f683641e6690999b23c156756d175`  
		Last Modified: Thu, 14 Apr 2022 00:09:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7dcd4972b24cf7ffe78c888061ef282e320f7a4c8aaa1384a55e7e28bd933c`  
		Last Modified: Thu, 14 Apr 2022 18:52:06 GMT  
		Size: 6.7 MB (6679287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be30e34b457ad8574d39820dcb20ff46f0329eec7498768b15691e314e82c308`  
		Last Modified: Mon, 25 Apr 2022 20:51:27 GMT  
		Size: 1.2 MB (1229164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1fabe7aa5b43f66bb040de9a4159250cec20a1d1f03c1bb56a94ca7857424b`  
		Last Modified: Mon, 25 Apr 2022 20:51:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f4a9899c053b29a3ae89a39cb76179c4f1a1b2c9480182e1785e7a4934de6672
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121607328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254d9278b4582c41c742295083ee2604578f59a1724d4ad9de237f56bc606d91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:16:49 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 03:23:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 03:23:16 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 03:23:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 03:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 03:23:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:56:20 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:58:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:58:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0a2cd126c67e6f9de5c0d2b9a8677d1f9ddf783df14e2ee2b65a4b837f781f`  
		Last Modified: Thu, 14 Apr 2022 03:32:44 GMT  
		Size: 111.7 MB (111729644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862413253fa7da1bfa2e411396d8013220cad00d664feea8f1757d91782065a3`  
		Last Modified: Thu, 14 Apr 2022 03:31:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edfefe81ed126a91f93489eb7294d5726270035f8a8af38291865530e667992`  
		Last Modified: Thu, 14 Apr 2022 18:57:58 GMT  
		Size: 6.0 MB (5953508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e680043769b7413a92b4bc4acb8e48a9e5ef164dc1c0e4685f3ebcc82c1c8`  
		Last Modified: Mon, 25 Apr 2022 20:59:27 GMT  
		Size: 1.2 MB (1228017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96a371a805895e54abe0b94c02a933bcbb6d1c50fa2fe09cbb9ca01bc4bdf09`  
		Last Modified: Mon, 25 Apr 2022 20:59:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:5bf6a3ce425975a90be678060a078ca9a13f0edb86b1755feadda66023a21ad5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121531748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65178889870010211120234bf1de0f8fe1154f42a122aec6d31ef5f44ca8ac9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:41:03 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:46:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:46:11 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:46:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:46:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:46:14 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:40:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:45:37 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:45:37 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:45:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:45:42 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:45:42 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59105010ca6c9ed528dc03f6c683c1bc8cd362cabe6df8b6ffe5cb7ea9a5d7a6`  
		Last Modified: Wed, 13 Apr 2022 23:49:58 GMT  
		Size: 110.4 MB (110425230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a657773900190e59f0ba6a0b06f6708be5a593336955df99496b40dd24e06d`  
		Last Modified: Wed, 13 Apr 2022 23:49:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb01e300b70916735527d066ade51d96bf1499fcc73f8e20921d8e6583b2ac7`  
		Last Modified: Thu, 14 Apr 2022 18:41:03 GMT  
		Size: 6.9 MB (6928572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324f0194c126d51157b32379352f8b4f91de641fa18400652f8d8f63a5100a10`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 1.2 MB (1189015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9690c7f39dbf1884a401e00ac496f19a144843007e3c3fd6c0b0ff1d216a812`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:2691a6ee70d65bd303bad70ee1acecd1ea7f27bee204ae088f61718ea5abc728
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122163242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a8e7dfa0559e1a8dbb14192d1d213837b57b559b2eb52d99526000967eaaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:52 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:33:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:33:21 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:33:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:33:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:33:37 GMT
WORKDIR /go
# Thu, 14 Apr 2022 19:18:31 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:19:04 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:19:08 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:19:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:19:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:19:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7b70e9365a42d1502d1309f3dc8545df5b5eb802bf656ac8d1a9adc0ca38e`  
		Last Modified: Thu, 14 Apr 2022 00:38:51 GMT  
		Size: 110.6 MB (110577271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52b4fb28789c7d8a190d4b1275b480c68ef6db3f548db9e61dc0bd5f2287c2`  
		Last Modified: Thu, 14 Apr 2022 00:38:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90034960a371e7877490974def61ec2afab2b9037cf021f8b268adf23f745b1f`  
		Last Modified: Thu, 14 Apr 2022 19:19:39 GMT  
		Size: 7.3 MB (7323527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b419307a290fa200d4ee1d283b336f67595b3dae2a96a545da0076a8f2f0b3a8`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 1.2 MB (1176369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbfaebc331dbb2554a5f8e3bc4ab37cab3cdbc0bee0ae7c0105a46e734b23bb`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:6254569039892bf2b972edc670fa1d0c02a4dbe158b5a6fc7503294d2ca02867
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124533779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1144cfb81d01915e8fe650368df288819b27dcb6e48f6742561aff5bfcb0e692`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:49 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:53:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:54:15 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:54:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:54:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:54:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:41:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:42:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:42:00 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:42:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:42:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:42:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:42:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ce7cc2608f8fa7ccebc2bd15f044fe91007681fdf9e3497b835c6671ea698`  
		Last Modified: Thu, 14 Apr 2022 00:01:54 GMT  
		Size: 113.5 MB (113483469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eebd463aa6406b85ba12e73255070fbd1566b013a0ca9f3fb5d3ccf5887df95`  
		Last Modified: Thu, 14 Apr 2022 00:01:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7324a2146e85ce6ede318cd28053e0977db3f0488b3ce78af656c65965e9001c`  
		Last Modified: Thu, 14 Apr 2022 18:42:50 GMT  
		Size: 6.9 MB (6933814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea609b474b313d4fd8f799684994c78a72930632aef028aef80beccb66e2b1`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 1.2 MB (1243136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378733785688e297f1ea3489b24dc76f584f16e7e7c75272ab18709fb8f18969`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:5e1112c2b251cd713257f116402a8b08c70b02536221f1c00e35ede48df2712f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888993144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a554cab996e7da76ef02819ef330a4fb26f3f9c493a7491141f84a9a33cfdce8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:34:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:34:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:34:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:34:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:37:05 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:38:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:55:20 GMT
ENV GOLANG_VERSION=1.17.9
# Wed, 13 Apr 2022 03:02:03 GMT
RUN $url = 'https://dl.google.com/go/go1.17.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '82752c3313cc6c1e1b5d73743a3ec569b09a14246fc2cb0824cf30f9f42a6005'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 03:02:09 GMT
WORKDIR C:\go
# Wed, 13 Apr 2022 04:41:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:18:48 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:18:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:19:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:19:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b761254212cd472f566f902a9830a91c33e94d06fb02a0192e29fe447bf98`  
		Last Modified: Wed, 13 Apr 2022 03:15:11 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210c142bbabba5cac6b3d06dc265578eafda02e9f54b2b955129652065abba5`  
		Last Modified: Wed, 13 Apr 2022 03:15:05 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24b5fea0cadfc385f0501b3cd52647d69ba5dd030f05bc637848ed7298ed45e`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1490fa326c6ac4254cc7e87bd773641c1a74d6d68ef0ee562e1296aa6e5ba09`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5425f63a29b9eb9b5bbbf135d080f8b1d2415a665b41591175a49f41da70d`  
		Last Modified: Wed, 13 Apr 2022 03:15:23 GMT  
		Size: 25.5 MB (25453409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf5f939642f2aaa6426ec58683c461b2fc27f9b92ed53ceea3d53e5f5b8d18d`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ec6181c5a38a1257f1181b0b390b0fa168627daeb103a617f04cf11c9666`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 328.4 KB (328368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6a29e70c078bf2fc470013ea504caa6d82ef66cd3af18be02f62f0d134dff6`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73a058a0e83dbc0674b085ab0d0151f94531062126dc4b1f43b0084df40fb62`  
		Last Modified: Wed, 13 Apr 2022 03:21:14 GMT  
		Size: 145.6 MB (145578329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde9b48a173bb3f29a006a2592b0bd8c63b07c7323137db4862e9a98fdde16b0`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49552906c9650efac10c4f00d5c31cebf6f940a05f00b03588df052cff5966c5`  
		Last Modified: Wed, 13 Apr 2022 04:50:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3892f065d9ae068931752897908cf2f42b7e70c10612f0d0c861d34b10c392d`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141d6a6f4de9ad79b32cd3b282f72556c753906066f6c959c90b9c98ed469f3`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151094a4fbe124963e13c2d1fb1c5868cfbaa169c003276af989cacbfe5d34b8`  
		Last Modified: Mon, 25 Apr 2022 21:22:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765cbaf262dc38339a50daa75e2a3bfdc536965075ef0683019b9c561b043cec`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.7 MB (1694161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df9d46dbf2556d53c3e38d0059f2c965b2ec2ec1362b393b4b1f1f9faeeec55`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:1b97052faeb50ea5c75cf73629d9b2ffe166382726774f8374c33fc821f12756
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408056049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd58e6419e1957d39f41478ff42606b54104872bb714df26c7bbfd10105c196`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:27:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:28:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:28:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:28:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:29:19 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:30:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:30:08 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:33:47 GMT
RUN $url = 'https://dl.google.com/go/go1.18.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c30bc3f1f7314a953fe208bd9cd5e24bd9403392a6c556ced3677f9f70f71fe1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:33:49 GMT
WORKDIR C:\go
# Thu, 14 Apr 2022 19:21:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:20:16 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:20:17 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:20:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:20:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:20:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df2c1d7d7b9748c6ddb8e9f196dfb2526451470a1256ab4047bece8468ff7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:50 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395e3155b04f913275d2f0e2bd07626c8d9b889b0646bb3fb44414d2df4130d`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3d0b098f175d5015767a5bb9a5641f1a1966ea2e2863b55cae5ae54f7edeb9`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff921731e5c58ad62f0eb62e698dd3033694fd15898c3e94d8021c0097dd912`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b89723742f5296cfb0b6d93c8b65a4995ee4a964d59eae8e96557dffc8f9e`  
		Last Modified: Wed, 13 Apr 2022 03:14:02 GMT  
		Size: 25.7 MB (25714775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0e7bcbbef7fb8a566a25556fc4b487c323359badbd7ab1bc58ab41729a7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67794576dcaaf4ef811c935b4ed0b40efe1487f0d0ab09462473b606d1fd89`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 562.2 KB (562186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2932986f0f385a406d2115ccb58dbf32a1730cf7e1f7f9f520863fcaa3e20d64`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f896ebd03d7af93409bcfb6bbbbd64481e6f575754cf0c600003a48a32d7a0b`  
		Last Modified: Wed, 13 Apr 2022 03:14:42 GMT  
		Size: 152.9 MB (152877366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f82b1974e8addd899731575590ff20cf09b3e97cdfe2ed285fc081b742b331`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52686327c4846c19f28b539d50b9d61e28b6fea5b5fddd0b921f8cbeb53d872e`  
		Last Modified: Thu, 14 Apr 2022 19:23:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe428ae1fd559625e6a41270985f292ad390b7b989a29f33178fbaeb59adaec`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce095f3f10565fda2a8540deb040f3ba4ec12ae51c7de87a7f39a507ee678bd9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808a55a0aa8fdfb2f5ae17966be5e1b3a39b399fd284db0372e9c29f67e2c9c`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4436fe9c1e94384199b902992ccbf1563c9a287bac0825d092d2e9b4d4f5be`  
		Last Modified: Mon, 25 Apr 2022 21:22:46 GMT  
		Size: 1.9 MB (1928477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e271d06fad4e820c1f2d2dd4029cc1c0fb472290b34a50751423c06751f032d9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:2cf9717916c3411cda2bfd15db21f1f40b43626eac201327da49ce01d40628dd
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
$ docker pull caddy@sha256:9650c5d624699fbfc7797f0a97d951f569f8bbfef959e02876be98384c53c32a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126769661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9e8161d584d9f23032b2316b7eb8438879699e1486ad8d0090e8e2c15f8de6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:20:33 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 02:34:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 02:34:25 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 02:34:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 02:34:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 02:34:25 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:19:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:30:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:30:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:30:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6858aa20941bdfe0d406b2e4db477feeccf42ca6e40478043b721c6a66f9d1b6`  
		Last Modified: Thu, 14 Apr 2022 02:37:21 GMT  
		Size: 115.6 MB (115569906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8029b02d49777774618d41ab3a1f7f4f32f7d4b10453afd26a184b8787beaa`  
		Last Modified: Thu, 14 Apr 2022 02:37:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8852fa41bd6ab92e973a3316d6db4a27e9b1844abac8363c94c241958de8ad22`  
		Last Modified: Thu, 14 Apr 2022 18:20:07 GMT  
		Size: 6.8 MB (6823100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e8b043cf75cf1c9c8457f53b1bd377c3efd34c07cee9f55c8bde83b13ef585`  
		Last Modified: Tue, 26 Apr 2022 00:31:10 GMT  
		Size: 1.3 MB (1289413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f16575d63df54107d98c6de6302604e3baecf850fcfeb0a0dd6cfd9408c9d`  
		Last Modified: Tue, 26 Apr 2022 00:31:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:8166e6393ad9b0c4953d6c5bf47942e76921dd3f1ee0b6348fefe6b301effbcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122763889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccdbba9972abfdc57c2b74bb66ed897a9d5237e00a1bc42323578d365b7f392`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:49:35 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:03:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:03:33 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:03:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:03:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:03:36 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:50:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:49:59 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:49:59 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:50:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:50:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:50:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:50:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d487bef959ea51d4b707107d10bc8bb2cabb35c3d0e890400da9558498fcfae9`  
		Last Modified: Thu, 14 Apr 2022 00:10:34 GMT  
		Size: 112.0 MB (111960610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232d226d7216d6a78d6f22f1281ea887106f683641e6690999b23c156756d175`  
		Last Modified: Thu, 14 Apr 2022 00:09:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7dcd4972b24cf7ffe78c888061ef282e320f7a4c8aaa1384a55e7e28bd933c`  
		Last Modified: Thu, 14 Apr 2022 18:52:06 GMT  
		Size: 6.7 MB (6679287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be30e34b457ad8574d39820dcb20ff46f0329eec7498768b15691e314e82c308`  
		Last Modified: Mon, 25 Apr 2022 20:51:27 GMT  
		Size: 1.2 MB (1229164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1fabe7aa5b43f66bb040de9a4159250cec20a1d1f03c1bb56a94ca7857424b`  
		Last Modified: Mon, 25 Apr 2022 20:51:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f4a9899c053b29a3ae89a39cb76179c4f1a1b2c9480182e1785e7a4934de6672
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121607328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254d9278b4582c41c742295083ee2604578f59a1724d4ad9de237f56bc606d91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:16:49 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 03:23:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 03:23:16 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 03:23:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 03:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 03:23:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:56:20 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:58:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:58:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0a2cd126c67e6f9de5c0d2b9a8677d1f9ddf783df14e2ee2b65a4b837f781f`  
		Last Modified: Thu, 14 Apr 2022 03:32:44 GMT  
		Size: 111.7 MB (111729644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862413253fa7da1bfa2e411396d8013220cad00d664feea8f1757d91782065a3`  
		Last Modified: Thu, 14 Apr 2022 03:31:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edfefe81ed126a91f93489eb7294d5726270035f8a8af38291865530e667992`  
		Last Modified: Thu, 14 Apr 2022 18:57:58 GMT  
		Size: 6.0 MB (5953508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e680043769b7413a92b4bc4acb8e48a9e5ef164dc1c0e4685f3ebcc82c1c8`  
		Last Modified: Mon, 25 Apr 2022 20:59:27 GMT  
		Size: 1.2 MB (1228017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96a371a805895e54abe0b94c02a933bcbb6d1c50fa2fe09cbb9ca01bc4bdf09`  
		Last Modified: Mon, 25 Apr 2022 20:59:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:5bf6a3ce425975a90be678060a078ca9a13f0edb86b1755feadda66023a21ad5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121531748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65178889870010211120234bf1de0f8fe1154f42a122aec6d31ef5f44ca8ac9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:41:03 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:46:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:46:11 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:46:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:46:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:46:14 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:40:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 26 Apr 2022 00:45:37 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 26 Apr 2022 00:45:37 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 26 Apr 2022 00:45:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 26 Apr 2022 00:45:42 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 26 Apr 2022 00:45:42 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59105010ca6c9ed528dc03f6c683c1bc8cd362cabe6df8b6ffe5cb7ea9a5d7a6`  
		Last Modified: Wed, 13 Apr 2022 23:49:58 GMT  
		Size: 110.4 MB (110425230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a657773900190e59f0ba6a0b06f6708be5a593336955df99496b40dd24e06d`  
		Last Modified: Wed, 13 Apr 2022 23:49:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb01e300b70916735527d066ade51d96bf1499fcc73f8e20921d8e6583b2ac7`  
		Last Modified: Thu, 14 Apr 2022 18:41:03 GMT  
		Size: 6.9 MB (6928572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324f0194c126d51157b32379352f8b4f91de641fa18400652f8d8f63a5100a10`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 1.2 MB (1189015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9690c7f39dbf1884a401e00ac496f19a144843007e3c3fd6c0b0ff1d216a812`  
		Last Modified: Tue, 26 Apr 2022 00:46:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:2691a6ee70d65bd303bad70ee1acecd1ea7f27bee204ae088f61718ea5abc728
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122163242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624a8e7dfa0559e1a8dbb14192d1d213837b57b559b2eb52d99526000967eaaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:52 GMT
ENV GOLANG_VERSION=1.18.1
# Thu, 14 Apr 2022 00:33:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 14 Apr 2022 00:33:21 GMT
ENV GOPATH=/go
# Thu, 14 Apr 2022 00:33:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Apr 2022 00:33:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 14 Apr 2022 00:33:37 GMT
WORKDIR /go
# Thu, 14 Apr 2022 19:18:31 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:19:04 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:19:08 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:19:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:19:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:19:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b7b70e9365a42d1502d1309f3dc8545df5b5eb802bf656ac8d1a9adc0ca38e`  
		Last Modified: Thu, 14 Apr 2022 00:38:51 GMT  
		Size: 110.6 MB (110577271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de52b4fb28789c7d8a190d4b1275b480c68ef6db3f548db9e61dc0bd5f2287c2`  
		Last Modified: Thu, 14 Apr 2022 00:38:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90034960a371e7877490974def61ec2afab2b9037cf021f8b268adf23f745b1f`  
		Last Modified: Thu, 14 Apr 2022 19:19:39 GMT  
		Size: 7.3 MB (7323527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b419307a290fa200d4ee1d283b336f67595b3dae2a96a545da0076a8f2f0b3a8`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 1.2 MB (1176369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbfaebc331dbb2554a5f8e3bc4ab37cab3cdbc0bee0ae7c0105a46e734b23bb`  
		Last Modified: Mon, 25 Apr 2022 20:20:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:6254569039892bf2b972edc670fa1d0c02a4dbe158b5a6fc7503294d2ca02867
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124533779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1144cfb81d01915e8fe650368df288819b27dcb6e48f6742561aff5bfcb0e692`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:49 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 23:53:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 13 Apr 2022 23:54:15 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 23:54:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 23:54:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 23:54:18 GMT
WORKDIR /go
# Thu, 14 Apr 2022 18:41:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 25 Apr 2022 20:42:00 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 20:42:00 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:42:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 20:42:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='889b63098037e4641cce5b355bd82535a4b6bbbc4aa16b8214108d0d847d288b52cd19017a477eedc9c066c2ec623310dd7909251888bc9432a7d7553ba9037e' ;; 		armhf)   binArch='armv6'; checksum='decfc298b900b62ee16e0dc92a05d3b61926b961de5ee10138ce9fc6cde85dba732928d4481e02e4290750c85a92c4c24c1850045eb16c0d6a75781ff1506964' ;; 		armv7)   binArch='armv7'; checksum='99819ca7b2d37ab93e0b6af8f41dbc16dec5844c47b64993c1c1c2df0567e4abbff55ca6e9642231bd68a1789d0ebbef36822362f0c29d6dcdb01d55b3669cba' ;; 		aarch64) binArch='arm64'; checksum='24203b66ed47ba5aaa358a9e84c6a13f48737d8dc2902fdc7e2218409ac1bde9f043f0bbdf7b66697c9f9263cf1272a73784e51a26eca94ff37bcda4c21ece87' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b96d1e6bfced6288678d45b120988e0c9e386671526688d229ace91b8f40ae03ae98a31aca9bdbbdbb9b865037e606801e434594d49cb1654398f53b4f904fd4' ;; 		s390x)   binArch='s390x'; checksum='6af5190825ac0ff01a60c7bfe5dbfea999841b9b1cf8dfca337c30eabc4aa7c03ad4da948f3472954a94f53552c1ab0a7bbd76894af6eb218ae118de68481f78' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 25 Apr 2022 20:42:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 25 Apr 2022 20:42:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ce7cc2608f8fa7ccebc2bd15f044fe91007681fdf9e3497b835c6671ea698`  
		Last Modified: Thu, 14 Apr 2022 00:01:54 GMT  
		Size: 113.5 MB (113483469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eebd463aa6406b85ba12e73255070fbd1566b013a0ca9f3fb5d3ccf5887df95`  
		Last Modified: Thu, 14 Apr 2022 00:01:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7324a2146e85ce6ede318cd28053e0977db3f0488b3ce78af656c65965e9001c`  
		Last Modified: Thu, 14 Apr 2022 18:42:50 GMT  
		Size: 6.9 MB (6933814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea609b474b313d4fd8f799684994c78a72930632aef028aef80beccb66e2b1`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 1.2 MB (1243136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378733785688e297f1ea3489b24dc76f584f16e7e7c75272ab18709fb8f18969`  
		Last Modified: Mon, 25 Apr 2022 20:42:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:b9480bf84ce2dace3248013b5c66c97e54e689c11831f8ab0c4d5f1849780caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:5e1112c2b251cd713257f116402a8b08c70b02536221f1c00e35ede48df2712f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888993144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a554cab996e7da76ef02819ef330a4fb26f3f9c493a7491141f84a9a33cfdce8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:34:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:34:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:34:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:34:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:37:05 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:38:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:55:20 GMT
ENV GOLANG_VERSION=1.17.9
# Wed, 13 Apr 2022 03:02:03 GMT
RUN $url = 'https://dl.google.com/go/go1.17.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '82752c3313cc6c1e1b5d73743a3ec569b09a14246fc2cb0824cf30f9f42a6005'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 03:02:09 GMT
WORKDIR C:\go
# Wed, 13 Apr 2022 04:41:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:18:48 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:18:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:19:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:19:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b761254212cd472f566f902a9830a91c33e94d06fb02a0192e29fe447bf98`  
		Last Modified: Wed, 13 Apr 2022 03:15:11 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210c142bbabba5cac6b3d06dc265578eafda02e9f54b2b955129652065abba5`  
		Last Modified: Wed, 13 Apr 2022 03:15:05 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24b5fea0cadfc385f0501b3cd52647d69ba5dd030f05bc637848ed7298ed45e`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1490fa326c6ac4254cc7e87bd773641c1a74d6d68ef0ee562e1296aa6e5ba09`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5425f63a29b9eb9b5bbbf135d080f8b1d2415a665b41591175a49f41da70d`  
		Last Modified: Wed, 13 Apr 2022 03:15:23 GMT  
		Size: 25.5 MB (25453409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf5f939642f2aaa6426ec58683c461b2fc27f9b92ed53ceea3d53e5f5b8d18d`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ec6181c5a38a1257f1181b0b390b0fa168627daeb103a617f04cf11c9666`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 328.4 KB (328368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6a29e70c078bf2fc470013ea504caa6d82ef66cd3af18be02f62f0d134dff6`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73a058a0e83dbc0674b085ab0d0151f94531062126dc4b1f43b0084df40fb62`  
		Last Modified: Wed, 13 Apr 2022 03:21:14 GMT  
		Size: 145.6 MB (145578329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde9b48a173bb3f29a006a2592b0bd8c63b07c7323137db4862e9a98fdde16b0`  
		Last Modified: Wed, 13 Apr 2022 03:20:24 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49552906c9650efac10c4f00d5c31cebf6f940a05f00b03588df052cff5966c5`  
		Last Modified: Wed, 13 Apr 2022 04:50:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3892f065d9ae068931752897908cf2f42b7e70c10612f0d0c861d34b10c392d`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141d6a6f4de9ad79b32cd3b282f72556c753906066f6c959c90b9c98ed469f3`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151094a4fbe124963e13c2d1fb1c5868cfbaa169c003276af989cacbfe5d34b8`  
		Last Modified: Mon, 25 Apr 2022 21:22:29 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765cbaf262dc38339a50daa75e2a3bfdc536965075ef0683019b9c561b043cec`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.7 MB (1694161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df9d46dbf2556d53c3e38d0059f2c965b2ec2ec1362b393b4b1f1f9faeeec55`  
		Last Modified: Mon, 25 Apr 2022 21:22:30 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4ae9973b09d5f6d1623aaf1cba218c72ea57e553d3bbdbfbf2ee3ecb4d96bdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:1b97052faeb50ea5c75cf73629d9b2ffe166382726774f8374c33fc821f12756
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408056049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd58e6419e1957d39f41478ff42606b54104872bb714df26c7bbfd10105c196`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:27:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:28:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:28:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:28:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:29:19 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:30:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:30:08 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:33:47 GMT
RUN $url = 'https://dl.google.com/go/go1.18.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c30bc3f1f7314a953fe208bd9cd5e24bd9403392a6c556ced3677f9f70f71fe1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:33:49 GMT
WORKDIR C:\go
# Thu, 14 Apr 2022 19:21:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Apr 2022 21:20:16 GMT
ENV XCADDY_VERSION=v0.3.0
# Mon, 25 Apr 2022 21:20:17 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:20:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 25 Apr 2022 21:20:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 25 Apr 2022 21:20:49 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df2c1d7d7b9748c6ddb8e9f196dfb2526451470a1256ab4047bece8468ff7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:50 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395e3155b04f913275d2f0e2bd07626c8d9b889b0646bb3fb44414d2df4130d`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3d0b098f175d5015767a5bb9a5641f1a1966ea2e2863b55cae5ae54f7edeb9`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff921731e5c58ad62f0eb62e698dd3033694fd15898c3e94d8021c0097dd912`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b89723742f5296cfb0b6d93c8b65a4995ee4a964d59eae8e96557dffc8f9e`  
		Last Modified: Wed, 13 Apr 2022 03:14:02 GMT  
		Size: 25.7 MB (25714775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0e7bcbbef7fb8a566a25556fc4b487c323359badbd7ab1bc58ab41729a7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67794576dcaaf4ef811c935b4ed0b40efe1487f0d0ab09462473b606d1fd89`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 562.2 KB (562186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2932986f0f385a406d2115ccb58dbf32a1730cf7e1f7f9f520863fcaa3e20d64`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f896ebd03d7af93409bcfb6bbbbd64481e6f575754cf0c600003a48a32d7a0b`  
		Last Modified: Wed, 13 Apr 2022 03:14:42 GMT  
		Size: 152.9 MB (152877366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f82b1974e8addd899731575590ff20cf09b3e97cdfe2ed285fc081b742b331`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52686327c4846c19f28b539d50b9d61e28b6fea5b5fddd0b921f8cbeb53d872e`  
		Last Modified: Thu, 14 Apr 2022 19:23:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe428ae1fd559625e6a41270985f292ad390b7b989a29f33178fbaeb59adaec`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce095f3f10565fda2a8540deb040f3ba4ec12ae51c7de87a7f39a507ee678bd9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808a55a0aa8fdfb2f5ae17966be5e1b3a39b399fd284db0372e9c29f67e2c9c`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4436fe9c1e94384199b902992ccbf1563c9a287bac0825d092d2e9b4d4f5be`  
		Last Modified: Mon, 25 Apr 2022 21:22:46 GMT  
		Size: 1.9 MB (1928477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e271d06fad4e820c1f2d2dd4029cc1c0fb472290b34a50751423c06751f032d9`  
		Last Modified: Mon, 25 Apr 2022 21:22:44 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:e42e57a219aa11138f3f147fb0c80b364c57fb063f85568664136ca9f7dd0048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2803; amd64
	-	windows version 10.0.20348.643; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:9fd29c443b9632275c7dee65b736044bf3eef7f0ff0acde17524d6bfa565d9c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16780958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd701a89dc68bf9b2f5f06994371e9c57d3991f35dd25eae9b72aa30fdb2d99`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:25:00 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:25:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:30:30 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:30:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:30:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:30:33 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:30:33 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:30:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:30:34 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:30:35 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:30:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ed6b8c4412bcd2bb1f40611012b40444b12071baf4884d0e75044fc1f32c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 291.5 KB (291522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff7bd6e2c9d7717705a52c1d27654581f987e1a43d2c9f3220ce850a5cdad`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637a338b6679706fd2d1cd3856187d469aa5666daeaec9011f4a36dec026c557`  
		Last Modified: Tue, 26 Apr 2022 00:30:58 GMT  
		Size: 13.7 MB (13668896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0522358bf40c87db949e3b98ad737bc00126a5c9204927ead005f2c8c6d1f40`  
		Last Modified: Tue, 26 Apr 2022 00:30:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:4fb2aa089fe64de9452ea153e8fcd45f77433bb884944de7ddaf659e776f9e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16046721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd6649c19066b2dfa04d56d12bf7a3c093a73b6b1cf203cd9502a608efcae7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:15:01 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:15:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:49:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:49:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:49:37 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:49:38 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:49:38 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:49:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:49:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:49:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:49:42 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:49:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:49:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b230dd773e10769a2eb3e507260d2470a646efd48a639739ba8852b2915302`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 291.7 KB (291685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac48280871fa0cc6e20550e9909af62acb5b3793a4ada967e49e60367ec386e`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e13dd2006703558a44bf92c22d7b86267519c8e0a45876f765416420a52c8b`  
		Last Modified: Mon, 25 Apr 2022 20:51:11 GMT  
		Size: 13.1 MB (13127083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac4eba6efd59e2065bc9bace41408b8e28e21c5f13233e039ac9f22fa7114e0`  
		Last Modified: Mon, 25 Apr 2022 20:51:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:4b653da1faf978146d3f353f96f5fec6a3d3dbe61eb226a9bc88310f8a7ac539
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15830530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e429c13a17afa4f600f294adcd8fb8fcd0e02f7d2b3a710e1e74c227c6b5307`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:33:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:33:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:57:32 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:57:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:57:38 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:57:39 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:57:39 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:57:43 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:57:44 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03203881a2568530a735b6e0e7a40ebb79adedc5193a675807b04eeb92cc6ed1`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 290.7 KB (290668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2de87d2e387fcc410ddd706bbe177b2a04b5137087a6ffca70b45c80dc976e0`  
		Last Modified: Tue, 05 Apr 2022 06:35:08 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8925c0c6962de2061a8f0a52f33e90a84c0d94c419622219a02b70ea6029831`  
		Last Modified: Mon, 25 Apr 2022 20:59:12 GMT  
		Size: 13.1 MB (13109556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a04801b9fe9d62e96942e841a278e2961fe3a50e31db66650c473be128e86`  
		Last Modified: Mon, 25 Apr 2022 20:59:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:69ab7c3ae40b72983a025617186f81a14adfe4e65bf060d6a8ded0b2027ad049
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15515390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1ed8512d16f85e28c907452f68a543b178d498bd69a88a4205b07809810c69`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:12:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 26 Apr 2022 00:45:10 GMT
ENV CADDY_VERSION=v2.5.0
# Tue, 26 Apr 2022 00:45:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 26 Apr 2022 00:45:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 26 Apr 2022 00:45:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 26 Apr 2022 00:45:15 GMT
ENV XDG_DATA_HOME=/data
# Tue, 26 Apr 2022 00:45:16 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Tue, 26 Apr 2022 00:45:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 26 Apr 2022 00:45:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 26 Apr 2022 00:45:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 26 Apr 2022 00:45:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 26 Apr 2022 00:45:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 26 Apr 2022 00:45:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 26 Apr 2022 00:45:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 26 Apr 2022 00:45:24 GMT
EXPOSE 80
# Tue, 26 Apr 2022 00:45:25 GMT
EXPOSE 443
# Tue, 26 Apr 2022 00:45:26 GMT
EXPOSE 2019
# Tue, 26 Apr 2022 00:45:27 GMT
WORKDIR /srv
# Tue, 26 Apr 2022 00:45:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa37f2341b1e6d98420668c9bc849a47f2c471d159b2303885040bd8d0a92f`  
		Last Modified: Tue, 05 Apr 2022 03:13:38 GMT  
		Size: 291.3 KB (291301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e87f72d84fd403dc0ea7d95672e5865925fca64a932f046b39035e8d3b43aae`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 5.7 KB (5747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffedcd6293512f192bfd7798cf59a8f7121658d14b7da6b8ed96d43b9ea1bd4`  
		Last Modified: Tue, 26 Apr 2022 00:46:14 GMT  
		Size: 12.5 MB (12501711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182c8210bf3bfdf3f311ac5ca0c803504516aa3979d448446e4b23a7414555db`  
		Last Modified: Tue, 26 Apr 2022 00:46:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:a20a2a180cce249a16be3b791cdde01779ffd91a4a9463bba45043e550f0bbab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11db83c89ecf795051de8117ab85b76db190a2f1bc5afd8ac113742dfd90522`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:08:34 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:08:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:17:24 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:17:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:17:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:17:50 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:17:53 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:17:58 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:18:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:18:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:18:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:18:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:18:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:18:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:18:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:18:31 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:18:35 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:18:39 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:18:43 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:18:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743509d6ced044a369685ebb068417e8757981a39d1b397c7b0182ab89f83528`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 293.7 KB (293721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029325992e21f613a5b486751627c7d5e5c7622ec29d4d170549f4dac13ad291`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadee40bb24012aa5a86d9d08c35465ea6747b388276fba98b2b23d8ab36e83d`  
		Last Modified: Mon, 25 Apr 2022 20:20:00 GMT  
		Size: 12.1 MB (12087346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aff6b8f6a27a0579cb3553f1b5da34c73a8d13bc2c46b71a42bffcbb433332`  
		Last Modified: Mon, 25 Apr 2022 20:19:58 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:70f645012314bf2deafbf43b697acd07d73a9dea2fc00a9e37ef66208f682fd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3584f54e8dcb7110aa2a2d26dd4917d281cf487e69e4a327ffb2b497250bdf95`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Mon, 25 Apr 2022 20:41:30 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 20:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9acd4fb788ed19bfe0718e67b23f259d8af3715e87670fce63667aebdc615351eac438066d617a8869da1dcf44cb643694dd479212065b2b79a5ccb52d667ae6' ;; 		armhf)   binArch='armv6'; checksum='af1f44c727849ac65a7d842de5f3f8c12e09d0c05f02a84c298e360ea0d0b285927bf1c5a3df6e9eb5f328b576fee6742a0357bd4a8d4cf329e7d624d630b93c' ;; 		armv7)   binArch='armv7'; checksum='a5ad120205237d1a2914dba5670c7ffd930fdfd3523bd2779616995bf7a6560de76a4b6e32a1c557cf9217f6cb802299f46ad076c4718d00fdb4b21c8ff55647' ;; 		aarch64) binArch='arm64'; checksum='37be9629eae6dadd257c5beaf32102564b77d7b8c8d97aac5a2bc8e93962a55afe25fa315f36a5f132665cb4124e9f33c0f5d8a253c60a994bc44d20a4428381' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='53dfd99f56ee682f88a4d631d3e8b34bad91ca51af39298bb07bab9290d66d6a4c2557e5103a1600a875cfa928be44febc88544ae0d42692d6c9a9479ab8479e' ;; 		s390x)   binArch='s390x'; checksum='b65614c618d3a9e8200389c2434291556283ffc39b834523893c75b2a335e7253bf8a571b310e2a4c60e24141fd32a5e66d0774434f443002753331b42ec3737' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 25 Apr 2022 20:41:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 25 Apr 2022 20:41:41 GMT
ENV XDG_DATA_HOME=/data
# Mon, 25 Apr 2022 20:41:42 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 20:41:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 20:41:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 20:41:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 20:41:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 20:41:47 GMT
EXPOSE 80
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 443
# Mon, 25 Apr 2022 20:41:48 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 20:41:49 GMT
WORKDIR /srv
# Mon, 25 Apr 2022 20:41:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8cc7c7c7ffd67f5740add448d341753330a2abdc6ed06e995cb7d28de381ab`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 291.8 KB (291821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f8e9524a50422cbb86b1c5e3af26710e4b65591ecc118a5079f1aa7fe5a67`  
		Last Modified: Tue, 05 Apr 2022 06:20:45 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ec2ded8fc151b5e2f97ea39505dda37e06f7e69f7e6b71e482b6959c5d72a8`  
		Last Modified: Mon, 25 Apr 2022 20:42:47 GMT  
		Size: 13.2 MB (13226741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636e08e595808f97112a31aecb09c32c3139808cf61e83ca37ba447853ecc421`  
		Last Modified: Mon, 25 Apr 2022 20:42:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:ac6afd8f502178001d3c6631753a6e4457830f2945acfb4f223b359312151739
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730628642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be5151970c967a41fa277f73d3ea5c6c2441dd532017ff7ba63f94b90b5815`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:38:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:14:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:16:13 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:16:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:16:23 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:16:24 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:16:25 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:17:17 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8129805e9e333a66c903463c3cbf8ee34716da4665df9a65dd4176eba5c5f06`  
		Last Modified: Wed, 13 Apr 2022 04:49:35 GMT  
		Size: 378.1 KB (378101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df92a93e366c3079de7a894225b5af047aced370ac7cc37db8a6a1efda1d68`  
		Last Modified: Mon, 25 Apr 2022 21:21:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83100cacadedcaa12031a24db1db453af535c1d938ebff9871930a6890125a4`  
		Last Modified: Mon, 25 Apr 2022 21:21:39 GMT  
		Size: 14.0 MB (14007463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2025016da8c10d71dc51b48c0c1b4c09cd52cfb337da6fd522df0f1d942ac2e`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d207d693dada181cafd0c7fb97ab2dfa21fdc798356667ebf3e18615af2cc1`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf8198462811b78954d0490e9bd2654c63af7f5590b0a316abcd6873b887f6c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982c6b1d8f9c21d5422f34061954adc18f796ee38efba6b7c7a5efc4ab11d2c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf52c26accb9bf3880af82d0bd3e1df4bf2de7d5e977e42fccdf515d198b190`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dc5e7fac918f26a223bdc96e1913d856b1bfa82e49af4dcbb9ee132dd0079`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0620c742ae20f8c7f4a81d372f9a25b706bf19be63e67271f504c9581a3a23a`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c575b1dbcfc0a0a68adcf4e48d4e2977a495bbd529fa0453b1a132185f45d8`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced94298b1f6c583462eee02e7ff2fbe680380e9e4081e9f33820bb0f0cf0c55`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda180811a77093bcc12e90c6f09509b092e2a3c5351635fa3a3711d54073137`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec34e60db92a527d1bcaacf30b0263c1aad257b56e842915b61ca4f467854253`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684c375495ff3e6194436cd4ad2d1b3b152576f3700e90e201efccc84457816`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07262f33fbd716916cd70767bb9863a076ed51716250ceec3769e039dec513`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b340376e6b0dbbfb01d19a74849b15f4d430e8634f8fedb81851637648dae26`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 300.0 KB (299995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa021badff18bcd5b01c95b400972c8b76fcf354efc8805e2f1821ba968775`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:28e63cb2eaf6998239e5b537831968ba4d9906a8058257d528fd6fe756e37a1e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242202428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d82ba894be8f5d6526b7dc7396408664a9b19a32405c5d33476ac90538ab384`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:45:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:17:35 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:18:07 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:18:08 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:18:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:18:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:18:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:18:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:18:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:18:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:18:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:18:17 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:18:18 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:18:19 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:18:38 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:18:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ff8ee97053f0fd2c04d1416858c55ed3909995cfc0831aa8f5a40204afd05`  
		Last Modified: Wed, 13 Apr 2022 04:50:46 GMT  
		Size: 638.3 KB (638318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b7414fa4e0939433774e287ba09191bca7e808e728adc8bf3c3ce1b26ea50`  
		Last Modified: Mon, 25 Apr 2022 21:21:59 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21af46560c679f5ccc42a3c6459c86ec83319e919f8f889665cb122dbb465e`  
		Last Modified: Mon, 25 Apr 2022 21:22:15 GMT  
		Size: 14.2 MB (14238735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b0f775ed9f809c59455ec9625c83c18ba9ac32b456cf504d0c8a3bb7b15f8`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a421645aec5009da45834b2835830b440c3da7f8b0f14889a32b64015b79fb5`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0fbeeb7476cfecc4f610d18fa06e3faf4cb08844806174e62bd8ca56cd10a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cc3d5e7a3f1b072138f955361688a44e041209f404662fd53b00cb54e758a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29529d78e3af49ca347462d245bb89c20b5897986acec557b8c17d8fe568ca86`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d59dbb39cb3b1525d9595055e2116e7fde476b1af040e47e500e7ddf460e52`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112715a31629216318fb61cfb76dce5c4ddad55b5aca9dd265d4abb009660a`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7274608e1c2e3e6a98f0d9eee200338a3eb77a2d315eeeef18ef8ba33682`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028a09180fa423ea4167dbce9d52b10d0ef23f4c05538d9be8012f7f63da154`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a568da62c45dafbbc16dfeb8b91cd1e67b9b549e72d8f7c6c76202c52a4426`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda8364a6d90b372db004dd3d1cebeb76cc8650fdbd5157eca53edca7b864d6`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65cc32ef8c70486456808de6df2222050d907cfb239fd48f9c7ac8c0748a5e7`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefe909dafbf401bfed81021f3d8d6c1ef9daff428c5cec6184db94484167b4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf8775a48ae02e9ac48a56ebf7808412b9f1c60876f9f3447b282d4ffccfe4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 347.8 KB (347758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136a5dca0069e8c5e5d3fc44538572f5aaf0c7abfbde605abf6df2c1ecdf28f`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:0382e21e9d9d4449ad0dbe82519f107c4fe3eb88d5b32bd149c017f51b6784e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2803; amd64
	-	windows version 10.0.20348.643; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:ac6afd8f502178001d3c6631753a6e4457830f2945acfb4f223b359312151739
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730628642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be5151970c967a41fa277f73d3ea5c6c2441dd532017ff7ba63f94b90b5815`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:38:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:14:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:16:13 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:16:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:16:23 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:16:24 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:16:25 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:17:17 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8129805e9e333a66c903463c3cbf8ee34716da4665df9a65dd4176eba5c5f06`  
		Last Modified: Wed, 13 Apr 2022 04:49:35 GMT  
		Size: 378.1 KB (378101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df92a93e366c3079de7a894225b5af047aced370ac7cc37db8a6a1efda1d68`  
		Last Modified: Mon, 25 Apr 2022 21:21:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83100cacadedcaa12031a24db1db453af535c1d938ebff9871930a6890125a4`  
		Last Modified: Mon, 25 Apr 2022 21:21:39 GMT  
		Size: 14.0 MB (14007463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2025016da8c10d71dc51b48c0c1b4c09cd52cfb337da6fd522df0f1d942ac2e`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d207d693dada181cafd0c7fb97ab2dfa21fdc798356667ebf3e18615af2cc1`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf8198462811b78954d0490e9bd2654c63af7f5590b0a316abcd6873b887f6c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982c6b1d8f9c21d5422f34061954adc18f796ee38efba6b7c7a5efc4ab11d2c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf52c26accb9bf3880af82d0bd3e1df4bf2de7d5e977e42fccdf515d198b190`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dc5e7fac918f26a223bdc96e1913d856b1bfa82e49af4dcbb9ee132dd0079`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0620c742ae20f8c7f4a81d372f9a25b706bf19be63e67271f504c9581a3a23a`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c575b1dbcfc0a0a68adcf4e48d4e2977a495bbd529fa0453b1a132185f45d8`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced94298b1f6c583462eee02e7ff2fbe680380e9e4081e9f33820bb0f0cf0c55`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda180811a77093bcc12e90c6f09509b092e2a3c5351635fa3a3711d54073137`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec34e60db92a527d1bcaacf30b0263c1aad257b56e842915b61ca4f467854253`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684c375495ff3e6194436cd4ad2d1b3b152576f3700e90e201efccc84457816`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07262f33fbd716916cd70767bb9863a076ed51716250ceec3769e039dec513`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b340376e6b0dbbfb01d19a74849b15f4d430e8634f8fedb81851637648dae26`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 300.0 KB (299995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa021badff18bcd5b01c95b400972c8b76fcf354efc8805e2f1821ba968775`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:28e63cb2eaf6998239e5b537831968ba4d9906a8058257d528fd6fe756e37a1e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242202428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d82ba894be8f5d6526b7dc7396408664a9b19a32405c5d33476ac90538ab384`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:45:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:17:35 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:18:07 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:18:08 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:18:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:18:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:18:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:18:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:18:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:18:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:18:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:18:17 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:18:18 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:18:19 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:18:38 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:18:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ff8ee97053f0fd2c04d1416858c55ed3909995cfc0831aa8f5a40204afd05`  
		Last Modified: Wed, 13 Apr 2022 04:50:46 GMT  
		Size: 638.3 KB (638318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b7414fa4e0939433774e287ba09191bca7e808e728adc8bf3c3ce1b26ea50`  
		Last Modified: Mon, 25 Apr 2022 21:21:59 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21af46560c679f5ccc42a3c6459c86ec83319e919f8f889665cb122dbb465e`  
		Last Modified: Mon, 25 Apr 2022 21:22:15 GMT  
		Size: 14.2 MB (14238735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b0f775ed9f809c59455ec9625c83c18ba9ac32b456cf504d0c8a3bb7b15f8`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a421645aec5009da45834b2835830b440c3da7f8b0f14889a32b64015b79fb5`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0fbeeb7476cfecc4f610d18fa06e3faf4cb08844806174e62bd8ca56cd10a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cc3d5e7a3f1b072138f955361688a44e041209f404662fd53b00cb54e758a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29529d78e3af49ca347462d245bb89c20b5897986acec557b8c17d8fe568ca86`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d59dbb39cb3b1525d9595055e2116e7fde476b1af040e47e500e7ddf460e52`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112715a31629216318fb61cfb76dce5c4ddad55b5aca9dd265d4abb009660a`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7274608e1c2e3e6a98f0d9eee200338a3eb77a2d315eeeef18ef8ba33682`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028a09180fa423ea4167dbce9d52b10d0ef23f4c05538d9be8012f7f63da154`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a568da62c45dafbbc16dfeb8b91cd1e67b9b549e72d8f7c6c76202c52a4426`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda8364a6d90b372db004dd3d1cebeb76cc8650fdbd5157eca53edca7b864d6`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65cc32ef8c70486456808de6df2222050d907cfb239fd48f9c7ac8c0748a5e7`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefe909dafbf401bfed81021f3d8d6c1ef9daff428c5cec6184db94484167b4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf8775a48ae02e9ac48a56ebf7808412b9f1c60876f9f3447b282d4ffccfe4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 347.8 KB (347758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136a5dca0069e8c5e5d3fc44538572f5aaf0c7abfbde605abf6df2c1ecdf28f`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:bc778a53e3357f5c8a9c100b8750dc0a3a608315519c727b0b944b910ebc066b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull caddy@sha256:ac6afd8f502178001d3c6631753a6e4457830f2945acfb4f223b359312151739
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730628642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be5151970c967a41fa277f73d3ea5c6c2441dd532017ff7ba63f94b90b5815`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:38:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:14:49 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:16:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:16:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:16:11 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:16:13 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:16:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:16:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:16:23 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:16:24 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:16:25 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:17:17 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:17:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8129805e9e333a66c903463c3cbf8ee34716da4665df9a65dd4176eba5c5f06`  
		Last Modified: Wed, 13 Apr 2022 04:49:35 GMT  
		Size: 378.1 KB (378101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df92a93e366c3079de7a894225b5af047aced370ac7cc37db8a6a1efda1d68`  
		Last Modified: Mon, 25 Apr 2022 21:21:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83100cacadedcaa12031a24db1db453af535c1d938ebff9871930a6890125a4`  
		Last Modified: Mon, 25 Apr 2022 21:21:39 GMT  
		Size: 14.0 MB (14007463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2025016da8c10d71dc51b48c0c1b4c09cd52cfb337da6fd522df0f1d942ac2e`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d207d693dada181cafd0c7fb97ab2dfa21fdc798356667ebf3e18615af2cc1`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf8198462811b78954d0490e9bd2654c63af7f5590b0a316abcd6873b887f6c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982c6b1d8f9c21d5422f34061954adc18f796ee38efba6b7c7a5efc4ab11d2c`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf52c26accb9bf3880af82d0bd3e1df4bf2de7d5e977e42fccdf515d198b190`  
		Last Modified: Mon, 25 Apr 2022 21:21:34 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dc5e7fac918f26a223bdc96e1913d856b1bfa82e49af4dcbb9ee132dd0079`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0620c742ae20f8c7f4a81d372f9a25b706bf19be63e67271f504c9581a3a23a`  
		Last Modified: Mon, 25 Apr 2022 21:21:32 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c575b1dbcfc0a0a68adcf4e48d4e2977a495bbd529fa0453b1a132185f45d8`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced94298b1f6c583462eee02e7ff2fbe680380e9e4081e9f33820bb0f0cf0c55`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda180811a77093bcc12e90c6f09509b092e2a3c5351635fa3a3711d54073137`  
		Last Modified: Mon, 25 Apr 2022 21:21:31 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec34e60db92a527d1bcaacf30b0263c1aad257b56e842915b61ca4f467854253`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684c375495ff3e6194436cd4ad2d1b3b152576f3700e90e201efccc84457816`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b07262f33fbd716916cd70767bb9863a076ed51716250ceec3769e039dec513`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b340376e6b0dbbfb01d19a74849b15f4d430e8634f8fedb81851637648dae26`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 300.0 KB (299995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa021badff18bcd5b01c95b400972c8b76fcf354efc8805e2f1821ba968775`  
		Last Modified: Mon, 25 Apr 2022 21:21:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:03edcc30e55a42bb6833408159e70252c0f2f3d51191a6ae23dfe882a87681fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull caddy@sha256:28e63cb2eaf6998239e5b537831968ba4d9906a8058257d528fd6fe756e37a1e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242202428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d82ba894be8f5d6526b7dc7396408664a9b19a32405c5d33476ac90538ab384`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 04:45:42 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Apr 2022 21:17:35 GMT
ENV CADDY_VERSION=v2.5.0
# Mon, 25 Apr 2022 21:18:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0/caddy_2.5.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('bdd4080106c861512a0b879349cc1526c4e025cec7b2be756bb8d5a3ee704e4911959cfb81f3af3004fe0862fb0dfadbb8e0a9ea728a3f6586a5527df010bacc')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Apr 2022 21:18:06 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Apr 2022 21:18:07 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Apr 2022 21:18:08 GMT
LABEL org.opencontainers.image.version=v2.5.0
# Mon, 25 Apr 2022 21:18:09 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Apr 2022 21:18:10 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Apr 2022 21:18:11 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Apr 2022 21:18:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Apr 2022 21:18:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Apr 2022 21:18:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Apr 2022 21:18:16 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Apr 2022 21:18:17 GMT
EXPOSE 80
# Mon, 25 Apr 2022 21:18:18 GMT
EXPOSE 443
# Mon, 25 Apr 2022 21:18:19 GMT
EXPOSE 2019
# Mon, 25 Apr 2022 21:18:38 GMT
RUN caddy version
# Mon, 25 Apr 2022 21:18:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ff8ee97053f0fd2c04d1416858c55ed3909995cfc0831aa8f5a40204afd05`  
		Last Modified: Wed, 13 Apr 2022 04:50:46 GMT  
		Size: 638.3 KB (638318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b7414fa4e0939433774e287ba09191bca7e808e728adc8bf3c3ce1b26ea50`  
		Last Modified: Mon, 25 Apr 2022 21:21:59 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21af46560c679f5ccc42a3c6459c86ec83319e919f8f889665cb122dbb465e`  
		Last Modified: Mon, 25 Apr 2022 21:22:15 GMT  
		Size: 14.2 MB (14238735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b0f775ed9f809c59455ec9625c83c18ba9ac32b456cf504d0c8a3bb7b15f8`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a421645aec5009da45834b2835830b440c3da7f8b0f14889a32b64015b79fb5`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0fbeeb7476cfecc4f610d18fa06e3faf4cb08844806174e62bd8ca56cd10a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cc3d5e7a3f1b072138f955361688a44e041209f404662fd53b00cb54e758a`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29529d78e3af49ca347462d245bb89c20b5897986acec557b8c17d8fe568ca86`  
		Last Modified: Mon, 25 Apr 2022 21:21:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d59dbb39cb3b1525d9595055e2116e7fde476b1af040e47e500e7ddf460e52`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25112715a31629216318fb61cfb76dce5c4ddad55b5aca9dd265d4abb009660a`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7274608e1c2e3e6a98f0d9eee200338a3eb77a2d315eeeef18ef8ba33682`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028a09180fa423ea4167dbce9d52b10d0ef23f4c05538d9be8012f7f63da154`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a568da62c45dafbbc16dfeb8b91cd1e67b9b549e72d8f7c6c76202c52a4426`  
		Last Modified: Mon, 25 Apr 2022 21:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda8364a6d90b372db004dd3d1cebeb76cc8650fdbd5157eca53edca7b864d6`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65cc32ef8c70486456808de6df2222050d907cfb239fd48f9c7ac8c0748a5e7`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefe909dafbf401bfed81021f3d8d6c1ef9daff428c5cec6184db94484167b4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf8775a48ae02e9ac48a56ebf7808412b9f1c60876f9f3447b282d4ffccfe4`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 347.8 KB (347758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9136a5dca0069e8c5e5d3fc44538572f5aaf0c7abfbde605abf6df2c1ecdf28f`  
		Last Modified: Mon, 25 Apr 2022 21:21:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
